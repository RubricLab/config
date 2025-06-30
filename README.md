# @rubriclab/config

Developer config files such as Biome, TypeScript, and PostCSS.

## Usage

```bash
bun add @rubriclab/config
```

### Biome

```json
// biome.json
{
	"extends": ["@rubriclab/config/biome"]
}
```

### TypeScript

```json
// tsconfig.json
{
	"compilerOptions": {
		"baseUrl": ".",
		"paths": {
			"@/*": ["./src/*"]
		},
		"plugins": [{ "name": "next" }],
		"target": "esnext"
	},
	"exclude": ["node_modules"],
	"extends": "@rubriclab/config/tsconfig",
	"include": ["./src/**/*.ts", "./src/**/*.tsx", ".next/types/**/*.ts", "next-env.d.ts"]
}
```

### PostCSS

```json
// postcss.config.mjs
export default {
	plugins: ["@tailwindcss/postcss"]
}
```