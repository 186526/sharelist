# 后台管理
访问 ```http://localhost:33001/manage```，填写口令即可进入后台管理。

## 常规

#### 切换语言
切换ShareList界面语言，默认使用访问者的系统语言。

#### 目录索引
默认启用。如果只提供下载功能，可禁用此项。

?> 系统管理员处于登录状态时，此项始终为```启用```。

#### 详情预览
默认启用。支持文档、图片、音频、视频的在线预览。

#### 显示README.md内容
默认启用。启用此项时，当前文件夹内的README.md文件将会被解析显示在页面底部。

#### 开放上传
默认禁用。

#### 下载限制
限制指定文件的下载权限。可使用正则表达式。例如:
* 禁止所有文件下载 ```^$```
* doc、pdf文件禁止下载 ```(?<!(doc|pdf))$```
* abc 路径下的文件禁止下载 ```^((?!abc).)*$```
* 允许 def 路径下的文件下载 ```def(?=\/)```

#### 中转
一般而言，下载使用的是各自挂载源的直连下载。启用此项后，所有下载都将使用本机中转。
!> 某些挂载源因使用了Cookie的原因，会强制中转。

#### 中转路径
设置需要使用中转的路径。留空表示所有。

#### 中转服务器
如果不想使用本机中转，可在此处填写对应的中转服务器。当前支持：
1. [cloudflare](zh-cn/advance?id=cf-worker中转)

#### 目录缓存时长
单位 秒。ShareList内部会对文件夹数据进行缓存，设置此项可调整。

#### 链接缓存时长
同上。

#### 下载链接有效期
单位 秒。设置后，下载链接将在此时间段内有效。若要关闭此功能，请设置为0。  

#### 忽略文件类型
设置后对应类型的文件将不会显示。
例如忽略图片：```jpg,png,gif,webp,bmp,jpeg```

?> 系统管理员处于登录状态时，可见所有文件。

#### 忽略路径
设置后对应路径下的文件将不会显示。

?> 系统管理员处于登录状态时，可见所有文件。

#### WebDAV路径
ShareList支持WebDAV导出，此处可设置访问路径。

#### 验证码识别接口
设置打码接口。

#### 自定义样式
设置自定义样式

#### 自定义脚本
设置自定义脚本，脚本将插入在页面的末尾。你可以在此处定义统计代码。

## 插件配置

## 口令
设置后台管理密码。

## 网站标题
设置网站标题。

## 虚拟路径
设置网盘挂载源。参考 [挂载源](zh-cn/plugins/README.md) 部分。