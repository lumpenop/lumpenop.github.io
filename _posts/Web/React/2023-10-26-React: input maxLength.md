---
date : YYYY-MM-DD HH:MM:SS +09:00
categories: [Web, React]
tags: [React]
published: true
---

```tsx
<input
    onInput={(e) => {
      if (e.currentTarget.value.length > e.currentTarget.maxLength)
        e.currentTarget.value = e.currentTarget.value.slice(0, e.currentTarget.maxLength);
    }}
    type="number"
    maxlength={9}
/>
```