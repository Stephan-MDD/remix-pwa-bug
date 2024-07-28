### Run

```
docker-compose up
```

### The project runs without any issues if you remove `remix-pwa`

```ts
import { vitePlugin as remix } from '@remix-run/dev';
import { defineConfig } from 'vite';
import tsconfigPaths from 'vite-tsconfig-paths';
// import { remixPWA } from '@remix-pwa/dev';

export default defineConfig({
	server: {
		port: process.env.PORT as number | undefined,
	},

	plugins: [
		remix({
			future: {
				v3_fetcherPersist: true,
				v3_relativeSplatPath: true,
				v3_throwAbortReason: true,
			},
		}),
		tsconfigPaths(),
		// remixPWA(),
	],
});
```
