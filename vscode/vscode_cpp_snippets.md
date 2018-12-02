### vscode cpp snippets头文件创建自动生成预定义内容和签名！

```
	"Print to console": {
		"scope": "cpp,c",
		"prefix": "qmsggg",
		"body": [
			"// Copyright (C) $CURRENT_YEAR qmsggg",
			"",
			"#ifndef ${1:${TM_FILENAME/(.*)\\.h$/${1:/upcase}_H/i}}",
			"#define ${1:${TM_FILENAME/(.*)\\.h$/${1:/upcase}_H/i}}",
			" ",
			"$0",
			" ",
			"#endif"
		],
		"description": "qmsggg output to console"
	}
```
