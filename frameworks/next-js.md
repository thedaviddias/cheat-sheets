# Next.js



## Remove console logs in prod

```js
const nextConfig = {
  compiler: {
    removeConsole: process.env.NODE_ENV !== 'development',
  },
}
```