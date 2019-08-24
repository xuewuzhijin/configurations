# TSLINT

## 目录
 * [配置文件](#配置文件)

### 配置文件

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
        "curly": false,
        "eofline": true,
        "no-console": false,
        "member-access": true,
        "arrow-parens": false,
        "no-var-keyword": true,
        "import-spacing": true,
        "trailing-comma": false,
        "interface-name": false,
        "ordered-imports": false,
        "no-var-requires": false,
        "space-within-parens": false,
        "no-unused-expression": false,
        "no-trailing-whitespace": true,
        "object-literal-sort-keys": false,
        "no-consecutive-blank-lines": false,
        "indent": [
            true,
            "tabs",
            2
        ],
        "quotemark": [
            true,
            "double"
        ],
        "semicolon": [
            false,
            "always"
        ],
        "comment-format": [
            true,
            "check-space"
        ]
    }
}
```