# esbuild-plugin-vue

building vue 3.x SFC files with esbuild.

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
