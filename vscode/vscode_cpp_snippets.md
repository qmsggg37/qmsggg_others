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

### 解释

其中最复杂的模式为：`${1:${TM_FILENAME/(.*)\\.C$/${1:/upcase}_H/i}}`，拆解为如下五部分： 
1. `${1:...}`：嵌套的 placeholder； 
1. `${TM_FILENAM/.../.../.}`：「variable transformations」中的「var_name」，表示带后缀的文件名； 
1. `${.../(.*)\\.C$/.../.}`：「variable transformations」中的「regular_expression」，表示匹配任意以「.C」为后缀的字符串； 
1. `${.../.../${1:/upcase}_H/.}}`：「variable transformations」中的「options」，表示将第一个捕捉项替换为大写的，并添加「_H」的后缀； 
1. `${.../.../.../i}`：「variable transformations」中的「options」，表示无视大小写。

--------------------- 
