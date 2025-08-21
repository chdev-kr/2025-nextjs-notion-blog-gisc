# Giscus 연결 레포지토리

GitHub Discussions를 활용한 giscus 댓글 기능을 연결하기 위한 레포지토리입니다.

## Giscus 연결 방법

### 1. GitHub Repository 설정

1. 이 저장소에서 **Settings** → **Features** → **Discussions** 활성화
2. [giscus.app](https://giscus.app)에 접속
3. 저장소를 선택하고 설정 완료

### 2. 생성된 코드 사용

giscus.app에서 생성된 스크립트를 복사하여 블로그에 붙여넣으세요:

```html
<script
  src="https://giscus.app/client.js"
  data-repo="chdev-kr/2025-nextjs-notion-blog-gisc"
  data-repo-id="[REPO_ID]"
  data-category="General"
  data-category-id="[CATEGORY_ID]"
  data-mapping="pathname"
  data-strict="0"
  data-reactions-enabled="1"
  data-emit-metadata="0"
  data-input-position="bottom"
  data-theme="preferred_color_scheme"
  data-lang="ko"
  crossorigin="anonymous"
  async
></script>
```

### 3. React 컴포넌트로 사용 (Next.js)

```jsx
'use client';

import { useEffect, useRef } from 'react';

export default function Giscus() {
  const ref = useRef(null);

  useEffect(() => {
    const script = document.createElement('script');
    script.src = 'https://giscus.app/client.js';
    script.setAttribute('data-repo', 'chdev-kr/2025-nextjs-notion-blog-gisc');
    script.setAttribute('data-repo-id', '[REPO_ID]');
    script.setAttribute('data-category', 'General');
    script.setAttribute('data-category-id', '[CATEGORY_ID]');
    script.setAttribute('data-mapping', 'pathname');
    script.setAttribute('data-strict', '0');
    script.setAttribute('data-reactions-enabled', '1');
    script.setAttribute('data-emit-metadata', '0');
    script.setAttribute('data-input-position', 'bottom');
    script.setAttribute('data-theme', 'preferred_color_scheme');
    script.setAttribute('data-lang', 'ko');
    script.async = true;

    ref.current?.appendChild(script);

    return () => {
      ref.current?.innerHTML = '';
    };
  }, []);

  return <div ref={ref} />;
}
```

사용할 때는 `[REPO_ID]`와 `[CATEGORY_ID]`를 giscus.app에서 생성된 실제 값으로 교체하세요.
