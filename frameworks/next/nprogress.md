# NProgress

```js
import NProgress from 'nprogress';

NProgress.configure({ showSpinner: false });

function MyApp({ Component, pageProps }: AppProps) {
	const router = useRouter();

	// Integrate nprogress
	useEffect(() => {
		router.events.on('routeChangeStart', () => NProgress.start());
		router.events.on('routeChangeComplete', () => NProgress.done());
		router.events.on('routeChangeError', () => NProgress.done());
	// eslint-disable-next-line react-hooks/exhaustive-deps
	}, []);

...
}
```