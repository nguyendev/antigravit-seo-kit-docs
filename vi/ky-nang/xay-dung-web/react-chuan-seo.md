# Lập Trình React/Next.js Chuẩn SEO

Kỹ năng `web-react` trong hệ sinh thái Antigravity SEO Kit giúp bạn tối ưu hóa Framework Next.js (App Router) để đạt Core Web Vitals xanh và tích hợp sẵn WebMCP.

## Tư Tưởng: Server-First

Khi dùng Antigravity, agent `web-frontend-specialist` sẽ mặc định áp dụng chiến lược **Server-First**.

### 1. Tránh Waterfalls Bằng Server Components
Nếu không cần tương tác UI (như onClick, useState), hãy dùng Server Components. Điều này giúp giảm thiểu bundle JavaScript tải xuống client.

**❌ Sai (Cách truyền thống - Gây Waterfall LCP):**
```tsx
"use client";
import { useEffect, useState } from 'react';

export default function BlogList() {
  const [posts, setPosts] = useState([]);
  
  useEffect(() => {
    fetch('/api/posts').then(res => res.json()).then(setPosts);
  }, []);

  return <div>{posts.map(p => <div key={p.id}>{p.title}</div>)}</div>;
}
```

**✅ Chuẩn Antigravity (Không có `"use client"`):**
```tsx
// Không dùng "use client", component render thẳng từ server
import { getPosts } from '@/lib/api';

export default async function BlogList() {
  const posts = await getPosts(); // Fetch server-side (tránh waterfall)

  return (
    <main>
      {posts.map(p => <article key={p.id}>{p.title}</article>)}
    </main>
  );
}
```

### 2. Tự Động Tích Hợp Schema & WebMCP
Đừng để khâu chèn Schema.org làm khó dev. Antigravity tự động generate Schema từ metadata object.

Ví dụ trong file `layout.tsx`:

```tsx
import { Metadata } from 'next';
import Script from 'next/script';

export const metadata: Metadata = {
  title: 'Blog Của Tôi',
  description: 'Trang blog được tối ưu 100% SEO',
  // Tag này giúp AI Agent tìm thấy API endpoint (WebMCP)
  alternates: {
    types: {
      'application/json': 'https://domain.com/.well-known/webmcp'
    }
  }
};

export default function RootLayout({ children }: { children: React.ReactNode }) {
  // Agent tự động sinh Schema Organization
  const jsonLd = {
    '@context': 'https://schema.org',
    '@type': 'Organization',
    name: 'My Blog'
  };

  return (
    <html lang="vi">
      <head>
        <Script
          id="schema-org"
          type="application/ld+json"
          dangerouslySetInnerHTML={{ __html: JSON.stringify(jsonLd) }}
        />
      </head>
      <body>{children}</body>
    </html>
  );
}
```

## Loại Bỏ Inline Utility Class
SEO Kit khuyến khích tách layer thiết kế. Tránh nhồi nhét Tailwind inline dài dòng làm phình to DOM và giảm tốc độ parse HTML của bot.

> [!TIP]
> Sử dụng `@apply` trong file css hoặc các plugin chuẩn để code sạch hơn. Tham khảo quy tắc tại `web-core.md`.
