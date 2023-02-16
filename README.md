# esbuild-plugin-vue

building vue 3.x SFC files with esbuild.

# Quickstart

- install

```
npm install -D esbuild-plugin-vue-next
// or
yarn add -D esbuild-plugin-vue-next
```

- use plugin

```js
// build.js
const { build } = require('esbuild')
const pluginVue = require('esbuild-plugin-vue-next')

build({
    entryPoints: ['index.js'], // your entry file
    bundle: true,
    outfile: 'bundle.js',
    plugins: [pluginVue()]
})
```

- run esbuild

```
node build.js
```

## Options

```js
export interface Options {
	isProduction?: boolean

	extractCss?: boolean

	sourceMap?: boolean

	template?: Pick<
		SFCTemplateCompileOptions,
		'compiler' | 'compilerOptions' | 'preprocessLang' | 'preprocessOptions' | 'preprocessCustomRequire' | 'transformAssetUrls'
		>

	script?: Pick<SFCScriptCompileOptions, 'babelParserPlugins'>

	style?: Pick<
		SFCAsyncStyleCompileOptions,
		'modulesOptions' | 'preprocessLang' | 'preprocessOptions' | 'postcssOptions' | 'postcssPlugins'
		>
}

```
