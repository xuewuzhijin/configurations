# TSLINT

## 目录
 * [配置文件](#配置文件)

### 配置文件

[Tslint官网](#https://palantir.github.io/tslint/rules/)

`tslint.json` 粘贴后 去掉注释
```json
{
	"defaultSeverity": "warning",
	"extends": [
		"tslint:recommended"
	],
	"linterOptions": {
		"exclude": [
			"node_modules/**"
		]
	},
	"rules": {
    // 是否允许使用 arguments callee
    "no-arg": true,
    // 是否需使用any类型
    "no-any": true,
    // 是否禁止空接口 {}
    "no-empty-interface": true,
    // 是否禁止导入带有副作用的语句
    "no-import-side-effect": true,
    // 是否允许内部模块
    "no-internal-module" :true,
    // for if do while 是否要有括号
		"curly": false,
    // 新的一行结束
		"eofline": true,
    // 是否使用 console
		"no-console": false,
    // 类成员是否需要申明 public private protected
		"member-access": true,
    // 类成员是否排序
    "member-sort": false,
		"member-ordering": false,
    // 箭头函数定义的参数是否需要括号
		"arrow-parens": false,
    // 是否使用 var 申明变量
		"no-var-keyword": true,
		"no-var-requires": false,
		"import-spacing": true,
    // 是否校验尾随逗号
		"trailing-comma": false,
    // 定义的接口是否需要加前缀
		"interface-name": false,
    // 导入的模块是否排序
		"ordered-imports": false,
    // 是否允许未被使用的表达式
		"no-unused-expression": false,
		"no-trailing-whitespace": true,
		// "space-before-function-paren": true,
    // 不使用 tab 缩进，仅两个空格一个缩进
		"indent": [
			false,
			"tabs",
			2
		],
    // 使用双引号
		"quotemark": [
			true,
			"double"
		],
    // 分号结束
		"semicolon": [
			true,
			"always"
		],
		"comment-format": [
			true,
			"check-space"
		]
	}
}
```