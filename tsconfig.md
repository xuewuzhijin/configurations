# TSCONFIG

## 目录
 * [配置文件](#配置文件)

### 配置文件

```json
{
  "compilerOptions": {
    "target": "es2015", // 编译输出目标 ES5 版本
    // "module": "es2015", // 采用的模块系统 [ 'none', 'commonjs', 'amd', 'system', 'umd', 'es6', 'es2015', 'esnext' ]
    "module": "esnext", // 采用的模块系统 [ 'none', 'commonjs', 'amd', 'system', 'umd', 'es6', 'es2015', 'esnext' ]
    "strict": true,     // 以严格模式解析
    "jsx": "preserve",
    "importHelpers": true,                // 从 tslib 导入外部帮助库: 比如__extends，__rest等
    "moduleResolution": "node",           // 如何处理模块
    "experimentalDecorators": true,       // 启用装饰器
    "esModuleInterop": true,              
    // "noImplicitAny": false,
    "allowSyntheticDefaultImports": true, // 允许从没有设置默认导出的模块中默认导入
    "sourceMap": true,                    // 是否包含可以用于 debug 的 sourceMap
    "baseUrl": ".",                       // 解析非相对模块名的基准目录
    "allowJs": true,
    "strictNullChecks": false,
    "typeRoots": [
      "./src/types",
      "./node_modules/vue/types"
    ],
    "types": [
      "webpack-env"
    ],
    "paths": {  // 指定特殊模块的路径
      "@/*": [
        "src/*"
      ],
      "~/*": [
        "node_modules/*"
      ]
    },
    "lib": [  // 编译过程中需要引入的库文件的列表
      "esnext",
      "dom",
      "dom.iterable",
      "scripthost"
    ]
  },
  "include": [
    "src/**/*.ts",
    "src/**/*.tsx",
    "src/**/*.vue",
    "tests/**/*.ts",
    "tests/**/*.tsx"
  ],
  "exclude": [
    "node_modules"
  ]
}
```