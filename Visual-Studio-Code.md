# Visual-Studio-Code

## 目录

* [配置文件](#配置文件)
* [用户片段](#用户片段)

### 配置文件

该配置文件依赖于 VS-Code `Beautify` / `Prettier - Code formatter` 插件，在启用该配置文件前，下载前面所依赖的文件

```json
{
  "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
  /* 指定编辑器字体 */
	"editor.fontFamily": "'Fira Code', 'YouYuan',  Consolas, 'Courier New', monospace",
	/* 编辑器字体大小 */
	"editor.fontSize": 14,
	/* 编辑器行高 */
	"editor.lineHeight": 26,
	"editor.tabSize": 2,
	/* 编辑器字体间隔1像素 */
	"editor.letterSpacing": 1,
	/* 让编辑器支持连体字 */
	"editor.fontLigatures": true,
	/* 编辑器右侧mini地图宽度 */
	"editor.minimap.maxColumn": 80,
	/* 让编辑器右侧mini地图只渲染色块，而不是字符 */
	"editor.minimap.renderCharacters": false,
	/* 让编辑器启动tab补全 */
	"editor.tabCompletion": "on",
	"editor.detectIndentation": false,
	/* 控制在建议列表中如何预先选择建议。 */
	"editor.suggestSelection": "first",
	"files.exclude": {
		"**/.classpath": true,
		"**/.project": true,
		"**/.settings": true,
		"**/.factorypath": true
  },
  // 每行最大字符数(0 = 禁用)。
  "html.format.wrapLineLength": 480,
  // 控制是否保留元素前已有的换行符。仅适用于元素前，不适用于标记内或文本。
  "html.format.preserveNewLines": true,
  /** 
  * 对属性进行换行。
  * aligned-multiple: 当超出折行长度时，将属性进行垂直对齐。
  * auto: 仅在超出行长度时才对属性进行换行
  * force: 对除第一个属性外的其他每个属性进行换行。
  * force-aligned: 对除第一个属性外的其他每个属性进行换行，并保持对齐。
  * force-expand-multiline: 对每个属性进行换行
  * preserve: 保留属性的包装
  * preserve-aligned: 保留属性的包装，但对齐。
  */
  "html.format.wrapAttributes": "preserve",
	"vetur.completion.autoImport": true,
	"vetur.format.defaultFormatter.html": "js-beautify-html",
	"vetur.format.defaultFormatter.css": "prettier",
  "vetur.format.defaultFormatter.js": "prettier",
  "vetur.format.defaultFormatter.ts": "prettier",
  "vetur.format.defaultFormatter.stylus": "stylus-supremacy",
	"vetur.format.defaultFormatterOptions": {
		"wrap_attributes": "force-aligned",
		"js-beautify-html": {
			// force-aligned | force-expand-multiline
			"wrap_attributes": "force-aligned"
		},
		"prettyhtml": {
			"printWidth": 100,
			"singleQuote": false,
			"wrapAttributes": true,
			"sortAttributes": true
    }
  },
  // 自定义块
  "vetur.grammar.customBlocks": {
    "docs": "md",
    "i18n": "json"
  },
  // 是否加分号
  "prettier.semi": true,
  "prettier.useTabs": false,
  "prettier.tabWidth": 2,
  "prettier.proseWrap": "never",
  "prettier.endOfLine": "lf",
  "prettier.printWidth": 80,
  "prettier.quoteProps": "as-needed",
  // 箭头函数如果只有一个参数就去掉括号（avoid）否则一个参数也要括号（always）
  "prettier.arrowParens": "avoid",
  "prettier.singleQuote": false,
  "prettier.insertPragma":  true,
  "prettier.trailingComma": "es5",
  // 对象 {} 括号两遍有空间
  "prettier.bracketSpacing":  true,
  "prettier.jsxSingleQuote":  false,
  "prettier.requirePragma": true,
  // 标签属性的后面的 > 放在最后一个属性后，否则（false） 另起一行。 Vue template 没用
  "prettier.jsxBracketSameLine": true,
  "prettier.vueIndentScriptAndStyle": true,
  "prettier.htmlWhitespaceSensitivity": "strict",
  // stylus 格式化
  "stylusSupremacy.insertBraces": false,
  "stylusSupremacy.insertColons": false,
  "stylusSupremacy.insertSemicolons": false,
	/* 格式化代码 */
	"beautify.config": {
		// 空格缩进
		"indent_size": 2,
		// 使用tab缩进
		"tab_size": 2,
		// 把空格缩进变成用tab缩进
		"indent_with_tabs": true,
		"css": {
			"indent_size": 2
    },
    "brace-style": "collapse,preserve-inline",
		// 函数参数括号内两侧用空格
		"space_in_paren": true,
		// 让整个文档最后一个行空出一个空行
		"end_with_newline": true,
		// 函数后用空格
		"space_after_anon_function": true,
		// 函数前用空格
		"space_before_conditional": true,
		// 函数名后用空格
		"space_after_named_function": false,
		//
		"keep_function_indentation": true,
		// 通过import或components...{}内的插件或组件不换行
		"brace_style": "collapse,preserve-inline",
		"semi": true
	},
	"beautify.language": {
		"js": {
			// 支持的文件类型
			"type": [
				"javascript",
				"json",
				"jsonc",
				"typescript"
			],
			// 支持的没文件类型的文件
			"filename": [
				".jshintrc",
				".jsbeautifyrc"
			]
		},
		"css": [
			"css",
			"less",
			"scss",
			"styl",
			"stylus"
		],
		"html": [
			"htm",
			"html"
		]
	},
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "files.autoSave": "off",
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[vue]": {
    "editor.defaultFormatter": "octref.vetur"
  },
  "workbench.iconTheme": "minimalistic-icons",
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "workbench.colorTheme": "Atom One Dark",
  "editor.cursorBlinking": "smooth",
  "window.customMenuBarAltFocus": false,
  "window.enableMenuBarMnemonics": false,
  "window.menuBarVisibility": "toggle",
  "breadcrumbs.icons": false,
  "workbench.tree.renderIndentGuides": "none",
  "editor.renderIndentGuides": false,
  "workbench.tree.indent": 16,
  "breadcrumbs.enabled": false,
  "vetur.useWorkspaceDependencies": true,
  "vetur.validation.template": false,
}
```

### 用户片段

```json
    // 自定义的全局log输出
    "Custome Browser Print console.log": {
        "scope": "javascript,typescript,vue",
        "prefix": "log",
        "body": [
            "console.log($1);"
        ],
        "description": "Log output to console"
    }

    // 自定义的 vue 初始化模板
	"Vue Init Template": {
		"prefix": "vb",
		"body": [
			"<!--",
            "  功能：${1:功能描述}",
            "  作者：Bill",
            "  邮箱：1311409079@qq.com",
            "  时间：$CURRENT_YEAR年$CURRENT_MONTH月$CURRENT_DATE日 $CURRENT_HOUR:$CURRENT_MINUTE",
            "  版本：v1.0",
            "  修改记录：",
            "  修改内容：",
            "  修改人员：",
            "  修改时间：",
			"-->\n",
			"<i18n>",
			"{",
			"\t\"zhCN\": {",
			"\t},",
			"\t\"enUS\": {",
			"\t}",
			"}",
			"</i18n>\n",
            "<template>\n",
			"</template>\n",
			"<script lang=\"ts\">",
			"import { Vue, Component } from \"vue-property-decorator\";",
			"@Component",
			"export default class ${2:$TM_FILENAME_BASE} extends Vue {",
			"\tpublic name: string = \"${2:$TM_FILENAME_BASE}\"",
			"}\n",
			"</script>\n",
			"<style lang=\"stylus\" scoped></style>\n"
		],
		"description": "Log output to console"
	}
```
