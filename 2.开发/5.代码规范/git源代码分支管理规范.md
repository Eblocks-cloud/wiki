一、分支分类
Git主分支（保留分支）：master 、release

Git辅助分支（临时分支）：dev-*、bugfix-*、release-*

 二、分支简介
2.1 master 主分支

对应线上（正式环境）的代码，一旦版本上线由测试人员发送合并matser邮件，开发人员将对应上线tag版本合并至master分支。

 2.2 release 主分支

同 master 分支，预发环境通过之后，上线之前，合并 release 分支。

 2.3 dev-* 辅助分支

从 master 拉取，用于新需求（版本）开发

*号为版本号+期次号

2.4 bugfix-* 辅助分支

从 master 拉取，用于快速修复线上Bug

*号为bug英文简称+期次号

 2.5 release-* 辅助分支

从 master 拉取，用于确保当前版本是基于线上最新版本迭代，可处理与线上代码存在的冲突。

任务辅助分支在测试环境通过之后，上预发环境之前，务必拉取一个 release-* 分支。

三、分支管理
3.1 需求（版本）开发

从 master 拉取 dev 分支

分支命名规则 ：类型 - 版本号 

 Tag命名规则： 类型 - 版本号 - 期次号

 例子：

 分支：

 dev-v2.0.1

 release-v2.0.1

 Tag:

 dev-v2.0.1-102401

 release-v2.0.1-102401

 3.2 线上问题处理

从 master 拉取 bugfix 分支

分支命名规则：类型 - bug英文简称

Tag命名规则： 类型 - bug英文简称 - 期次号

 例子：

 分支：

 bugtfix-dateError

 release-dateError

 Tag:

 bugfix-dateError-102401

四、我们实行规则

1.每次迭代版本使用新的develop分支进行开发。

2.在测试环境通过之后，上生产环境之前，务必拉取一个 release-* 分支。

3.生产上线、线上验证无问题后，测试通知相关开发合并到master。

4.bugfix-* 辅助分支从 master 拉取，用于快速修复线上Bug，线上验证无问题后，测试通知相关开发合并到master和开发分支。



