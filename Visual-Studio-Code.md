# Visual-Studio-Code

## 目录

* [配置文件](#配置文件)
* [用户片段](#用户片段)

### 配置文件

```json
{
	/* 指定编辑器主题 */
	"workbench.colorTheme": "One Dark Pro Vivid",
	/* 指定编辑器字体 */
	"editor.fontFamily": "'Fira Code', 'YouYuan',  Consolas, 'Courier New', monospace",
	/* 编辑器字体大小 */
	"editor.fontSize": 16,
	/* 编辑器行高 */
	"editor.lineHeight": 26,
	/* 编辑器字体间隔1像素 */
	"editor.letterSpacing": 1,
	/* 让编辑器支持连体字 */
	"editor.fontLigatures": true,
	/* 编辑器右侧mini地图宽度 */
	"editor.minimap.maxColumn": 40,
	/* 让编辑器右侧mini地图只渲染色块，而不是字符 */
	"editor.minimap.renderCharacters": false,
	/* 让编辑器启动tab补全 */
	"editor.tabCompletion": "on",
	/* JAVA代码注释生成器 */
	"java.codeGeneration.generateComments": true,
	/* JAVA的环境变量，这里指向绝对地址，JAVA安装目录 */
	"java.home": "D:\\Program Files (x86)\\JAVA",
	/* MAVEN的安装目录 */
	"maven.executable.path": "D:\\Program Files (x86)\\apache-maven-3.6.1\\bin\\mvn",
	/* JAVA的MAVEN用户配置 */
	"java.configuration.maven.userSettings": "D:\\Program Files (x86)\\apache-maven-3.6.1\\conf\\settings.xml",
	/* MAVEN命令行模式环境变量 */
	"maven.terminal.customEnv": [
		{
			"environmentVariable": "JAVA_HOME",
			"value": "D:\\Program Files (x86)\\JAVA"
		}
	],
	/* 控制在建议列表中如何预先选择建议。 */
	"editor.suggestSelection": "first",
	"vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
	"files.exclude": {
		"**/.classpath": true,
		"**/.project": true,
		"**/.settings": true,
		"**/.factorypath": true
	},
	"vetur.completion.autoImport": true,
	"vetur.format.defaultFormatter.html": "js-beautify-html",
	"vetur.format.defaultFormatter.css": "prettier",
	"vetur.format.defaultFormatter.js": "vscode-typescript",
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
		  "wrapAttributes": false,
		  "sortAttributes": true
		},
		"prettier": {
			"semi": true,
			"singleQuote": false
		}
	},
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
		// 函数参数括号内两侧用空格
		"space_in_paren": true,
		// 让整个文档最后一个行空出一个空行
		"end_with_newline": true,
		// 函数后用空格
		"space_after_anon_function": true,
		// 函数前用空格
		"space_before_conditional": true,
		// 函数名后用空格
		"space_after_named_function": true,
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
		],
		"java": {
			"type": "java"
		}
	},
	/* JavaScript文件默认用 beautify 格式化代码 */
	"[javascript]": {
		"editor.defaultFormatter": "HookyQR.beautify"
	},
	/* TypeScript同上 */
	"[typescript]": {
		"editor.defaultFormatter": "HookyQR.beautify"
	},
	"[json]": {
		"editor.defaultFormatter": "HookyQR.beautify"
	}
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



