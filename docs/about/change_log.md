# 更新日志

v2.23.0
------------------------
2022年06月16日

!!! info "新增功能 🌱"
    - feat: 支持 OpenID 认证设置用户属性映射字段
    - feat: JumpServer 客户端拉起工具支持图形化 (GNOME) 的 Linux 系统
    - feat: 支持对数据库命令进行复核（通过 CLI 和 Web CLI 方式连接的数据库） (KoKo)【企业版】
    - feat: 新增 Web Terminal (Luna) 页面组织切换功能【企业版】
    - feat: 新增 Razor 组件（代替原有的 XRDP 组件），大幅提升对 RDP 协议资产使用原生客户端连接的操作体验【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化管理页面响应速度
    - perf: 优化 Luna 页面访问资产显示 Loading 动画
    - perf: 优化克隆角色权限时包含权限位
    - perf: 增加配置项 CONNECTION_TOKEN_EXPIRATION 控制连接 Token 的过期时间，默认/至少 5 分钟
    - perf: 优化 RBAC 模块的数据库迁移逻辑，提升升级速度
    - perf: 优化授权规则过期通知文案
    - perf: 优化系统用户、改密任务密码字段不支持输入单双引号
    - perf: 优化命令过滤器详情页面，增加快速选择用户、用户组、应用等资源
    - perf: 优化管理页面中技术支持菜单也包含工具下载链接
    - perf: 优化文件上传成功的提示信息 (Lion)
    - perf: 优化命令记录中文字符记录乱码的问题 (Lion)
    - perf: 优化 Web 终端显示最大滚动行数 1000 -> 5000 行 (KoKo)
    - perf: 优化支持 MySQL 8.0 (Magnus)
    - perf: 优化 OpenID 用户登录时默认邮件后缀使用配置项
    - perf: 优化会话记录的登录 IP 地址问题，去掉记录端口号 (Magnus)
    - perf: 优化支持 PostgrepSQL Scram 认证 (Magnus）【企业版】

!!! success "问题修复 🐛"
    - fix: 修复用户更新自己密码地址不正确的问题
    - fix: 修复获取登录 IP 城市时不准确的问题
    - fix: 修复公告设置内容不显示的问题
    - fix: 修复 LDAP 用户属性映射配置了用户组字段后导致用户登录失败的问题
    - fix: 修复推送动态用户时 comment 中包含空格导致推送失败的问题
    - fix: 修复命令列表模糊搜索时报错的问题
    - fix: 修复资产树右击查看节点详情不显示的问题
    - fix: 修复列表自定义搜索时再次返回页面显示 true 的问题
    - fix: 修复用户首次登录页面提交后，会取消三方绑定账号的问题
    - fix: 修复 OmniDB 占用 CPU 资源高的问题，提升性能【企业版】
    - fix: 修复手动登录的系统用户连接 RemoteApp 应用时获取不到认证信息导致登录失败的问题【企业版】

!!! tip "依赖升级 🧰"
    - ansible==2.10.7
    - oracle=instantclient-19-10
    - redis==4.3.1

v2.22.3
------------------------
2022年06月16日

!!! summary "功能优化 🚀"
    - perf: 优化 RBAC 模块的数据库迁移逻辑，提升升级速度

!!! success "问题修复 🐛"
    - fix: 修复通过 XRDP 连接的资产会话录像上传失败的问题【企业版】
    - fix: 修复手动登录的系统用户连接 RemoteApp 应用时获取不到认证信息导致登录失败的问题【企业版】

v2.22.2
------------------------
2022年06月08日

!!! success "问题修复 🐛"
    - fix: 修复公告不显示的问题
    - fix: 修复开启 AD/LDAP 用户认证后登录失败的问题（配置了同步用户组的情况）
    - fix: 修复 Magnus 会话地址问题（Magnus）
    - fix: 优化 PostgreSQL 数据库支持 SCRAM 认证机制（Magnus）
    - fix: 修复 XRDP 上传录像文件的日期问题【企业版】
    - fix: 修复 OmniDB 跳过原生 LogHistory 记录提升性能【企业版】

v2.22.1
------------------------
2022年05月25日

!!! success "问题修复 🐛"
    - fix: 修复 Migrations 错误
    - fix: 修复用户更新自己密码跳转地址失败的问题
    - fix: 修复获取 IP 城市可能报错的问题
    - fix: 修复 连接 MySQL8 数据库时，由于默认认证方式的改变导致连接失败的问题（Magnus）

v2.22.0
------------------------
2022年05月19日

!!! info "新增功能 🌱"
    - feat: ⽀持记录查看资产账号密码⽇志
    - feat: 支持 Elasticsearch 命令存储根据日期建立索引
    - feat: 支持 LDAP 同步用户组（Windows AD）
    - feat: 支持通过本地客户端直连 Redis 数据库（Magnus）
    - feat: 支持 AIX 系统平台进行批量改密【企业版】
    - feat: 支持 Fusion Compute 私有云资产同步【企业版】
    - feat: 支持通过 Web CLI 方式连接 PostgreSQL 数据库 (KoKo)【企业版】
    - feat: 支持企业微信、钉钉直接审批工单【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化前后端敏感信息传输使用 AES 进行加密传输
    - perf: 优化日志记录中登录 IP 城市查询不准确的问题
    - perf: 优化用户 Session 在浏览器关闭后失效
    - perf: 优化 SAML2 metadata 文件内容及属性映射后台处理逻辑
    - perf: 优化 OpenID 认证可以选择认证方式，如：client_secret_basic、client_secret_post
    - perf: 优化拆分 Connection Token API 和 Super Connection Token API
    - perf: 优化拆分 Public Setting API 和 Open Public Setting API
    - perf: 优化视图切换提示
    - perf: 优化支持资产账号管理进行批量删除
    - perf: 优化 Luna 页面 ESC 快捷键冲突问题，支持长按 ESC 键可退出全屏模式
    - perf: 优化 Luna 页面加载 iFrame 组件的超时时间从 10s 延长至 30s
    - perf: 优化 SSH 终端方式的国际化语言
    - perf: 优化 Web GUI / CLI 方式连接 Windows、Linux 资产右侧操作菜单的样式（KoKo、Lion）
    - perf: 优化 Lion 组件向第三方存储上传录像失败后，尝试保存至本地默认存储（Lion）
    - perf: 优化一些已知翻译问题
    - perf: 优化开启 http2（Installer）
    - perf: 优化部署/卸载脚本（Installer）
    - perf: 优化恢复工单启用全局配置项【企业版】
    - feat: 优化工单审批人中排除当前工单的申请人【企业版】
    - perf: 优化资产数量超过 License 数量限制后进行提示【企业版】
    - perf: 优化通过原生客户端连接 Windows 资产时，支持控制是否记录录像功能（XRDP）【企业版】

!!! success "问题修复 🐛"
    - fix: 修复开源版登录后页面跳转问题
    - fix: 修复组织管理员无查看系统平台的权限问题【企业版】
    - fix: 修复 Windows 执行 Ansible 任务显示 sudo 命令执行失败的问题
    - fix: 修复指定系统/组织角色获取关联用户失败的问题
    - fix: 修复获取类型为 null 的命令存储日志中显示不支持的问题
    - fix: 修复 LDAP 同步用户后仪表盘总数没有更新的问题
    - fix: 修复兼容 AWS 上 redis[ssl] 无证书无法部署的问题
    - fix: 修复未开启 MFA 二次认证时的企业微信、钉钉、飞书登录跳转问题
    - fix: 修改组织资源统计时 org 为 None 的问题
    - fix: 修复公告不显示的问题
    - fix: 修复资产树移动资产时右击菜单无法关闭问题
    - fix: 修复 SSH Client 连接方式的选项不能关闭的问题
    - fix: 修复公钥情况下通过 VSCode 连接 Linux 资产失败的问题
    - fix: 修复 Luna 页面快速连接多个 Linux 资产出现卡住的问题
    - fix: 修复 SSH 终端登录后数据库列表不显示 IP 问题
    - fix: 修复 SSH 共享会话在线人数不准确问题
    - fix: 修复日志级别不生效的问题（Magnus）
    - fix: 修复 Kill 命令执行不生效的问题（Magnus）
    - fix: 修复 Azure MySQL 无法认证的问题（Magnus）
    - fix: 修复工单详情跳转资产授权、应用授权权限位判断问题【企业版】

!!! tip "依赖升级 🧰"
    - ipip-ipdb==1.6.1

v2.21.4
------------------------
2022年05月11日

!!! success "问题修复 🐛"
    - fix: 修复获取系统/组织角色关联用户失败的问题
    - fix: 修复 Magnus 支持 Auth-switch 操作
    - fix: 修复 Magnus 执行 kill 命令不生效的问题
    - fix: 修复 Magnus 日志级别修改不生效的问题

v2.21.3
------------------------
2022年05月06日

!!! success "问题修复 🐛"
    - fix: 修复 Windows 资产执行 Ansible 任务失败的问题
    - fix: 修复 Luna 页面资产连接弹框中 SSH-Client 方式的显示隐藏控制问题

v2.21.2
------------------------
2022年04月29日

!!! success "问题修复 🐛"
    - fix: 修复组织管理员创建资产不能选择系统平台的问题

v2.21.1
------------------------
2022年04月25日

!!! success "问题修复 🐛"
    - fix: 修复拉起 SSH 客户端失败的问题
    - fix: 修复使用弱算法认证的交换机不能连接的问题
    - fix: 修复使用公钥通过 Visual Studio Code 连接资产失败的问题
    - fix: 修复特殊情况下页面跳转不能打开的问题
    - fix: 修复申请工单不能选择组织的问题【企业版】

!!! summary "功能优化 🚀"
    - perf: 修改临时密码提示信息文案不准确的问题

v2.21.0
------------------------
2022年04月21日

!!! info "新增功能 🌱"
    - feat: 支持使用原生数据库客户端（如：Navicat、DataGrip）直连数据库，数据库类型目前支持：MySQL、MariaDB 和 PostgreSQL（ Magnus 组件）
    - feat: 支持使用分布式策略访问资产，在系统设置 / 终端设置 中通过配置服务端点和端点规则进行使用
    - feat: 支持企业微信和钉钉进行免密登录，在企业微信和钉钉开放平台配置应用地址进行使用
    - feat: 支持日语国际化
    - feat: 支持通过拉起 SSH 客户端的方式连接 Linux 资产
    - feat: 支持纳管 MongoDB 数据库
    - feat: 支持用户使用临时密码进行登录
    - feat: 支持纳管百度云资产【企业版】
    - feat: 支持纳管京东云资产【企业版】
    - feat: 支持用户在工作台视图中切换组织显示【企业版】
    - feat: 支持资产改密计划切换用户后执行改密【企业版】

!!! summary "功能优化 🚀"
    - perf: 支持部署使用 SSL Redis 数据库
    - perf: 优化站内信支持一键已读
    - perf: 优化角色绑定后台处理逻辑
    - perf: 优化连接 Windows 资产时的窗口大小问题
    - perf: 优化命令记录输入字段长度问题
    - perf: 优化资产序列编号字段长度问题
    - perf: 优化命令导出的时间可读性
    - perf: 优化移动端的页面显示和视图切换体验
    - perf: 优化连接 OpenSSH 8.0 协议资产的连接问题
    - feat: 优化 Web 连接 MySQL 数据库增加禁用自动补全参数
    - perf: 优化 LDAP 认证配置支持指定组织定时同步用户【企业版】

!!! success "问题修复 🐛"
    - fix: 修复仪表盘用户数量不准确的问题
    - fix: 修复 API Docs 访问失败的问题
    - fix: 修复一些已知权限位控制问题
    - fix: 修复远程应用认证信息获取错误的问题
    - fix: 修复系统组件的角色绑定问题
    - fix: 修复 FTP 日志未定时清理的问题
    - fix: 修复 VMware 同步实例 ID 为 None 时同步失败的问题
    - fix: 修复系统设置消息订阅不能更新的问题

!!! tip "依赖升级 🧰"
    - paramiko==2.10.1
    - Pillow==9.0.1
    - bce-python-sdk==0.8.64

v2.20.3
------------------------
2022年04月13日

!!! success "问题修复 🐛"
    - fix: 修复仪表盘页面用户数量不能及时刷新的问题
    - fix: 修复仪表盘页面资源数量点击不能跳转的问题
    - fix: 修复系统消息订阅设置不生效的问题
    - fix: 修复批量更新终端表单页面字段没有翻译的问题

!!! summary "功能优化 🚀"
    - perf: 优化创建按钮下拉菜单不能滚动的问题

v2.20.2
------------------------
2022年04月01日
!!! success "问题修复 🐛"
    - fix: 修复通过API创建用户时失败的问题
    - fix: 修复Kubernetes连接的已知问题
    - fix: 修复资产列表从节点移除权限位不准确的问题
    - fix: 修复云管中心同步实例ID为None的问题【企业版】
    - fix: 修复通过XRDP连接的资产不能使用复制粘贴的问题【企业版】
    - fix: 修复通过XRDP连接远程应用失败的问题【企业版】

v2.20.1
------------------------
2022年03月23日

!!! summary "功能优化 🚀"
    - perf: 优化移动端页面显示
    - perf: 优化用户API权限控制
    - perf: 关闭仪表盘权限
    - perf: 工单权限位移动到系统角色级别
    - perf: 关闭更新角色绑定权限
    - perf: 开放用户Access Key更新、删除权限

!!! success "问题修复 🐛"
    - fix: 修复 /api/docs API文档打不开的问题
    - fix: 修复创建SuperUser失败的问题
    - fix: 修复为用户绑定角色失败的问题
    - fix: 修复资产详情系统用户页面的权限控制
    - fix: 修复工单中会话卡片按钮的权限控制
    - fix: 修复从节点移除资产的权限控制
    - fix: 修复获取远程应用认证信息的问题
    - fix: 修复Luna页面连接Windows资产会显示XRDP连接方式的问题

v2.20.0
------------------------
2022年03月17日

!!! info "新增功能 🌱"
    - feat: 支持基于角色的权限访问控制（Role-based access control, RBAC）
    - feat: 支持使用腾讯云对象存储（COS）存放录像文件

!!! summary "功能优化 🚀"
    - perf: 优化资产授权创建时默认选中了点击的资产和节点问题
    - perf: 优化命令过滤器关联的系统用户包含rdp/vnc协议的问题
    - perf: 优化命令过滤器关联的应用不包含Kubernetes的问题
    - perf: 优化云管中心增加同步实例关联的资产IP字段【企业版】
    - perf: 优化通过XRDP连接的Windows资产默认全屏打开【企业版】

!!! success "问题修复 🐛"
    - fix: 修复手动登录的系统用户登录失败的问题
    - fix: 修复用户页面点击资产树节点提示对象找不到的问题
    - fix: 修复通过API创建节点不能指定ID的问题
    - fix: 修复Keycloak配置转换为OpenID不生效的问题
    - fix: 修复资产账号列表点击更新时弹窗不出现的问题
    - fix: 修复AWS（亚马逊云）未立即释放的实例获取私有IP失败的问题【企业版】
    - fix: 修复云管中心同步任务详情中同步实例状态不准确的问题【企业版】
    - fix: 修复改密计划执行显示失败实际已经修改成功的问题(安全模式关闭的情况)【企业版】
    - fix: 修复XRDP会话录像记录时间显示不准确的问题【企业版】
    - fix: 修复XRDP会话录像播放出现黑屏的问题【企业版】

!!! tip "依赖升级 🧰"
    - amqp==5.0.9
    - ansible==2.10
    - celery==5.2.2
    - cryptography==36.0.1
    - Django==3.1.14
    - django-celery-beat==2.2.1
    - django-timezone-field==4.1.0
    - kombu==5.2.2
    - Pillow==9.0.0
    - pycryptodome==3.12.0
    - pycryptodomex==3.12.0
    - PyNaCl==1.5.0
    - jms-storage==0.0.42
    - vine==5.0.0
    - python-ldap==3.4.0
    - flower==1.0.0
    - pyjwkest==1.4.2
    - jsonfield2==4.0.0.post0

v2.19.2
------------------------
2022年03月07日

!!! success "问题修复 🐛"
    - fix: 修复通过API创建节点不能指定ID的问题
    - fix: 修复Keycloak配置转换为OpenID不生效的问题
    - fix: 修复资产账号列表点击更新时弹窗不出现的问题
    - fix: 修复云管中心同步任务详情中同步实例状态不准确的问题【企业版】
    - fix: 修复改密计划执行显示失败实际已经修改成功的问题(安全模式关闭的情况)【企业版】
    - fix: 修复XRDP会话录像记录时间显示不准确的问题【企业版】
    - fix: 修复XRDP会话录像播放出现黑屏的问题【企业版】

v2.19.1
------------------------
2022年02月18日

!!! summary "功能优化 🚀"
    - perf: 优化创建Session分享链接后的复制按钮文案(复制链接及验证码)

!!! success "问题修复 🐛"
    - fix: 修复使用手动登录的系统用户登录资产失败的问题
    - fix: 修复用户关联的命令过滤器规则会在全局组织内生效的问题【企业版】
    - fix: 修复删除组织时组织内工单流程设置未删除的问题【企业版】

v2.19.0
------------------------
2022年02月17日

!!! info "新增功能 🌱"
    - feat: 支持控制第三方认证用户的MFA认证流程
    - feat: 支持设置命令过滤规则大小写匹配策略
    - feat: 新增Luna页面连接资产时自动保存上次使用的系统用户
    - feat: 新增Luna页面的退格键映射设置项，解决操作网络设备时退格键不生效的问题
    - feat: 支持通过工单申请Redis数据库应用【企业版】
    - feat: 支持通过XRDP连接远程应用时的复制粘贴、上传下载（磁盘挂载）权限控制【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化账号备份性能问题
    - perf: 优化表单提交时自动滚动到校验报错字段的位置
    - perf: 优化列表搜索支持多级自定义模糊搜索
    - perf: 优化会话录像回放窗口的自适应问题
    - perf: 优化用户授权树右击Kubernetes节点不自动展开
    - perf: 优化Lion组件的日志输出持久化
    - perf: 优化工单流程页面显示组织名称【企业版】
    - perf: 优化工单流程设置权限（只允许超级管理员查看和修改）【企业版】

!!! success "问题修复 🐛"
    - fix: 修复创建资产授权规则时默认填充资产或节点的问题
    - fix: 修复获取SAML 2.0协议的用户属性偶尔为空的问题
    - fix: 修复测试资产可连接性失败的问题（资产关联了多个系统用户）
    - fix: 修复站内信功能导致Redis数据库连接数量持续增加的问题
    - fix: 修复Syslog记录的日志不显示命令记录中远端地址的问题
    - fix: 修复会话录像文件未被定时清除的问题
    - fix: 修复操作日志添加、删除动作翻译问题
    - fix: 修复用户组名称翻译问题
    - fix: 修复更新资产账号秘钥不成功的问题
    - fix: 修复LDAP认证设置中定时同步配置翻译问题
    - fix: 修复资产账号列表数据重复问题
    - fix: 修复通过SSH连接资产时的复用问题（当资产IP修改后不再复用已有连接）
    - fix: 修复搜索框不能搜索false选项的问题
    - fix: 修复命令记录页面筛选数据时tree自动刷新问题
    - fix: 修复资产账号导出条数不准确的问题
    - fix: 修复通过XRDP连接资产时会生成用户登录日志的问题【企业版】

v2.18.2
------------------------
2022年02月11日

!!! success "问题修复 🐛"
    - fix: 修复密钥密码翻译问题
    - fix: 修复通过XRDP连接资产时生成用户登录日志的问题
    - fix: 修复Redis连接未正常关闭的问题
    - fix: 修复测试系统用户可连接性失败的问题

v2.18.1
------------------------
2022年01月24日

!!! success "问题修复 🐛"
    - fix: 修复会话记录中远端地址记录不准确的问题
    - fix: 修复命令记录中远端地址和资产信息（连接Kubernetes集群）记录不准确的问题
    - fix: 修复连接Kubernetes集群动态查看Pod日志时按下Ctrl+C不能退出的问题

v2.18.0
------------------------
2022年01月20日

!!! info "新增功能 🌱"
    - feat: 支持纳管Redis数据库
    - feat: 支持通过选中命令来调整录像回放的起始时间(字符类会话录像)
    - feat: 支持对资产、应用账号进行定时备份【企业版】
    - feat: 支持复核人审批同意资产登录复核工单后直接对会话发起控制【企业版】
    - feat: 支持对SQL Server数据库的批量改密【企业版】
    - feat: 支持查看Kubernetes的Namespace和Pod，并且支持对Pod内的Container进行连接和审计(Web Terminal连接方式)
    - feat: 支持导入SQL文件和导出查询数据集(支持CSV、XLSX格式)(Web数据库可视化页面)【企业版】
    - feat: 支持对Windows RemoteApp应用权限动作的单独控制，包括文件上传、下载、复制、粘贴(Web Terminal连接方式)【企业版】
    - feat: 支持显示License中的Copyright信息【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化应用程序下载页面入口(Web Terminal页面)
    - perf: 优化命令记录页面增加显示执行命令的远端地址
    - perf: 优化rdp协议的系统用户用户名校验规则(支持输入特殊字符`#%&~^`)
    - perf: 优化资产节点的创建支持使用完整名称(通过API创建方式)
    - perf: 优化系统用户支持填写自定义SSH Key passphrase
    - perf: 优化用户绑定第三方认证系统成功后及时向用户发送相关消息通知(如：绑定企业微信、钉钉、飞书等)
    - perf: 优化国际化问题(包括文件选择、任务名称、审计日志、KoKo、文件管理页面等)
    - perf: 优化工单信息增加工单序列号显示【企业版】
    - perf: 优化青云私有云资产同步支持自动解析API和使用自定义端口【企业版】
    - perf: 优化应用授权支持对Action进行控制【企业版】
    - perf: 优化命令复核工单中显示解析后的完整命令【企业版】

!!! success "问题修复 🐛"
    - fix: 修复列表页面中搜索框切换搜索字段后不能回车搜索的问题
    - fix: 优化celery异步任务中数据库连接数量会持续增加的问题
    - fix: 修复删除用户失败的问题，通过第三方模块创建过SSO Token信息(提示包含关联对象，但实际已无关联对象)
    - fix: 修复用户即将过期提醒消息未发送的问题
    - fix: 修复测试腾讯SMS平台验证码不通过的问题
    - fix: 修复执行SQL命令时光标移动可能会造成指令过滤匹配失败的问题
    - fix: 修复强制启用用户MFA后，个人信息页面设置按钮被禁用的问题
    - fix: 修复创建申请应用工单点击保存并继续添加后报错的问题【企业版】
    - fix: 修复克隆应用授权规则失败的问题【企业版】
    - fix: 修复云管中心同步资产报错后任务立即停止的问题【企业版】
    - fix: 修复工单审批流中复核人不能及时更新的问题【企业版】
    - fix: 修复删除组织失败的问题(提示包含关联对象，但实际已无关联对象)【企业版】

!!! tip "依赖升级 🧰"
    - PyYAML==6.0
    - numpy==1.22.0
    - pandas==1.3.5
    - pymssql==2.1.5
    - kubernetes==21.7.0
    - jms-storage==0.0.41
    - python-dateutil==2.8.2
    - websocket-client==1.2.3
    - python:3.8-slim
    - debian:libaio-dev、freetds-dev
    - guacd:1.4.0

v2.17.3
------------------------
2022年01月07日

!!! success "问题修复 🐛"
    - fix: 修复用户在用户页面中访问工单页面出现白屏的问题

v2.17.2
------------------------
2021年12月31日

!!! success "问题修复 🐛"
    - fix: 修复 sql 光标移动造成拦截失效的问题
    - fix: 修复XRDP组件统计内存使用率偏高的问题【企业版】

v2.17.1
------------------------
2021年12月27日

!!! summary "功能优化 🚀"
    - perf: 更新SAML 2.0登录页Logo
    - perf: 客户端下载页添加最新Jmservisor.msi程序链接
    - perf: 修改远程应用连接页面在Web Terminal中进行显示，不再通过弹窗打开
    - perf: 优化命令复核工单中记录完整命令【企业版】
    - perf: 优化改密计划保存认证信息逻辑【企业版】

!!! success "问题修复 🐛"
    - fix: 修复云管中心同步资产，如果遇到同步失败的情况则不终断继续向后同步【企业版】

v2.17.0
------------------------
2021年12月16日

!!! info "新增功能 🌱"
    - feat: 支持基于SAML 2.0的联合身份验证实现单点登录
    - feat: 字符类录像文件采用cast格式存储
    - feat: 支持对Windows资产的键盘操作进行记录和审计（仅支持Web连接的方式）
    - feat: 支持通过命令快速定位Windows资产会话录像（仅支持Web连接的方式）
    - feat: 支持对SQL Server数据库进行管理、连接、操作和审计（仅支持CLI和Web CLI方式连接）
    - feat: 支持对数据库操作的SQL语句进行过滤（仅支持允许、拒绝，暂不支持复核）
    - feat: 支持将改密计划执行结果发送给指定接收人（仅支持邮件方式）
    - feat: 支持通过XRDP方式连接Windows远程应用（需要使用最新Jmservisor脚本）【企业版】
    - feat: 支持对OpenStack私有云资产进行同步【企业版】
    - feat: 支持对Web GUI方式连接的数据库进行SQL补全【企业版】
    - feat: 支持通过工单申请资产节点下的所有资产【企业版】
    - feat: 重构Web GUI数据库连接组件OmniDB【企业版】

!!! summary "功能优化 🚀"
    - perf: 支持对命令过滤器进行多维度绑定
    - perf: 优化服务启动脚本执行速度
    - perf: 优化终端性能指标对内存使用率兼容Docker limit的设置
    - perf: 优化后台订阅模块的处理逻辑
    - perf: 优化命令过滤规则正则表达式生成逻辑
    - perf: 优化AD Domain系统用户不支持推送
    - perf: 优化命令过滤规则排序问题
    - perf: 优化消息通知类型支持Markdown格式
    - perf: 优化站内信文案和显示遮挡问题
    - perf: 优化JSON输入框支持一键格式化
    - perf: 移除远程应用右侧快捷键菜单栏【企业版】
    - perf: 优化创建申请资产、应用工单时默认选中当前组织【企业版】

!!! success "问题修复 🐛"
    - fix: 修复Redis集群环境下使用Redis锁机制报错的问题
    - fix: 修复openSUSE系统su切换用户失败的问题
    - fix: 修复根据节点、资产查询授权时报错的问题
    - fix: 修复CAS、OpenID用户登录时的跳转问题
    - fix: 修复根据资产IP查询资产显示不全的问题
    - fix: 修复数据库连接未关闭的问题
    - fix: 修复会话详情页命令列表排序失效的问题
    - fix: 修复获取应用类型系统用户认证信息失败的问题
    - fix: 修复青云私有云同步资产网段地址固定问题【企业版】
    - fix: 修复将应用从某个授权中移除时会从所有授权中移除的问题【企业版】

!!! tip "依赖升级 🧰"
    - jms-storage==0.0.40
    - python-redis-lock==3.7.0
    - python-novaclient==11.0.1
    - pyzipper==0.3.5
    - python3-saml==1.12.0
    - python-keystoneclient==4.3.0
    - go 1.17.5
    - docker 20.10.11

v2.16.3
------------------------
2021年11月25日

!!! success "问题修复 🐛"
    - fix: 修复重置MFA的提示问题
    - fix: 修复数据库连接关闭问题
    - fix: 修改绑定MFA去掉验证密码的步骤
    - fix: 修复根据IP搜索资产授权时数据不全的问题
    - fix: 修复OIDC、CAS登录时的跳转问题
    - fix: 修复终端列表指标数值显示问题
    - fix: 修复会话列表日期搜索的时区问题

v2.16.2
------------------------
2021年11月24日

!!! success "问题修复 🐛"
    - fix: 修复RADIUS MFA登录失败的问题
    - fix: 修复根据节点、资产查询资产授权时报错的问题
    - fix: 修复系统用户密码不再自动去除两侧的空白字符
    - fix: 修复Luna第一次访问登录时没有自动重定向的问题
    - fix: 修复开启MFA后CAS登录一直进行MFA重定向的问题

v2.16.1
------------------------
2021年11月19日

!!! success "问题修复 🐛"
    - fix: 修改全局IP黑、白名单控制逻辑
    - fix: 修改短信验证码认证逻辑
    - fix: 修改会话记录中系统用户名为实际登录资产使用的用户名
    - fix: 修复通过创建的Token登录资产出现白屏的问题

v2.16.0
------------------------
2021年11月18日

!!! info "新增功能 🌱"
    - feat: 新增Linux资产二级用户登录功能
    - feat: 支持使用OBS华为云存储会话录像
    - feat: 支持全局设置用户登录IP黑名单
    - perf: 支持管理员开启、关闭异地登录提醒功能
    - feat: 支持自定义修改导航栏中的文档、技术支持等链接地址【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化MFA认证、绑定流程
    - perf: 移动会话设置保留时间到定期清理设置页面
    - feat: 新增Esc和F11快捷键，通过Web Termianl连接Windows资产时进行使用
    - perf: 新增内置资产平台列表Windows-RDP、Windows-TLS，并设置Windows2016为外置平台
    - perf: 优化异地登录提醒不再对局域网地址进行检测
    - perf: 优化创建用户邮件信息支持部分标签定义
    - perf: 优化支持管理员手动修改资产硬件信息
    - perf: 优化创建命令、录像存储名称重复时的错误提示信息
    - perf: 优化重置公钥成功的消息格式
    - perf: 优化登录页面认证MFA失败的错误提示信息
    - perf: 优化终端列表指标数值保留一位小数
    - perf: 优化通过rz命令下载多文件时的显示问题
    - perf: 优化更新页面密码输入框风格
    - perf: 优化数据库改密支持MySQL 5.6版本、Oracle密码支持设置特殊字符【企业版】

!!! success "问题修复 🐛"
    - fix: 修复执行Ansible任务的日志输出中包含非UTF-8字符报错的问题
    - fix: 修复开启使用RADIUS OTP配置后，用户登录没有跳转至MFA认证页面的问题
    - fix: 修复创建用户Token偶尔失败的问题
    - fix: 修复终端删除后录像存储不能删除问题
    - fix: 修复LDAP设置多个OU时，包含空白字符测试连接会失败的问题
    - fix: 修复因光标移动造成命令拦截失败的问题
    - fix: 修复创建、更新表单下拉列表选项较多导致文字溢出的问题
    - fix: 修复应用授权详情中用户组不能删除问题
    - fix: 修复首次打开管理页面获取不到默认语言的问题
    - fix: 修复数据库连接没有关闭问题
    - fix: 修复进行MFA登录验证时没有自动选中输入框的问题
    - fix: 修复工单流更新后不生效的问题【企业版】
    - fix: 修复升级时OmniDB镜像会被删除的问题【企业版】
    - fix: 修复数据库改密成功后无法连接的问题【企业版】
    - fix: 修复通过XRDP连接Windows资产偶尔报错的问题【企业版】
    - fix: 修复通过XRDP连接资产时网关限制只能使用22端口的问题【企业版】

v2.15.4
------------------------
2021年11月12日

!!! success "问题修复 🐛"
    - fix: 修复Web Terminal页面不能自动下载XRDP客户端的问题
    - fix: 修改异地登录提醒不再对局域网地址进行检测

v2.15.3
------------------------
2021年11月01日

!!! success "问题修复 🐛"
    - fix: 修复特权、系统用户上传Key文件失败的问题

v2.15.2
------------------------
2021年10月29日

!!! success "问题修复 🐛"
    - fix: 修复创建用户登录规则失败的问题
    - fix: 修复系统设置开启水印功能不可见的问题

v2.15.1
------------------------
2021年10月29日

!!! success "问题修复 🐛"
    - fix: 修复数据库升级偶尔失败的问题

v2.15.0
------------------------
2021年10月28日

!!! info "新增功能 🌱"
    - feat: 新增公告栏功能
    - feat: 新增用户异地登录提醒功能
    - feat: 新增资产授权即将过期通知功能
    - feat: 资产详情页面支持查看已授权的用户和用户组
    - feat: 用户登录规则支持分时登录
    - feat: 用户登录规则支持登录复核【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化消息通知文案
    - perf: 系统用户列表添加应用数量列
    - perf: 优化操作日志资源名称翻译
    - perf: 优化资源创建页面中Crontab定期执行表达式的配置和校验
    - perf: 优化用户登录日志中IP城市获取算法
    - perf: 优化文件管理页面的网站图标支持动态更新
    - perf: 优化资源列表页面默认按名称排序显示
    - perf: 优化下载页面文案
    - perf: 优化通过Web终端登录资产时动态系统用户允许输入用户名
    - perf: 优化用户连接无权限资产时的错误提示信息
    - perf: 会话被管理员终断后提示信息中显示执行终断的管理员名称
    - perf: 优化监控、共享会话时文件传输的提示问题
    - perf: 优化资产编号信息可以通过调用API进行修改
    - perf: 用户未被授权应用时Web终端不显示应用授权树
    - perf: 通过VSCode连接资产时支持授权过期自动断开
    - perf: 支持Telnet协议的系统用户用户名输入中文字符
    - perf: 通过Web终端连接字符类协议资产时鼠标再次回到窗口取消自动滚动到底部
    - perf: 优化邀请用户时下拉列表最多显示的用户数量 (最多6个)
    - perf: 用户登录页面支持同时输入MFA、SMS动态认证码
    - perf: 修改资产平台Windows和Windows2016的配置信息保持一致
    - perf: 通过Web终端连接远程应用时开启新的浏览器窗口进行显示【企业版】
    - perf: 优化通过XRDP连接资产时鼠标存在阴影的问题【企业版】
    - perf: 优化通过XRDP连接资产时网关支持使用密钥认证【企业版】
    - perf: 优化通过XRDP连接的资产支持本地磁盘挂载（备注：授权中指定上传下载动作）【企业版】

!!! success "问题修复 🐛"
    - fix: 修复第三方认证错误提示信息
    - fix: 修改用户登录失败的提示信息颜色
    - fix: 修复通过Web终端连接字符类协议资产时窗口左侧字符无法选中的问题
    - fix: 修复Web终端页面批量命令发送失败的问题
    - fix: 修复系统用户和资产、节点进行关联时，资产的特权用户会被更新的问题
    - fix: 修复一些弹窗不能滚动的问题
    - fix: 修复通过KoKo登录时，未开启SMS服务的情况下二次认证出现了SMS选项的问题
    - fix: 修复用户登录失败未记录日志的问题
    - fix: 修复创建、更新页面初始化选择框报错的问题
    - fix: 修复获取系统用户密码为空的问题
    - fix: 修复系统用户认证方式从托管密码更新为手动输入模式后，不填写用户名报错的问题
    - fix: 修复测试邮件服务器偶尔失败的问题
    - fix: 修复用户加入共享会话成功后操作页面水印丢失的问题
    - fix: 修复获取普通系统用户认证信息逻辑，解决手动登录的系统用户未输入密码直接登录失败的问题
    - fix: 修复导出选中的命令记录时会导出全部命令的问题
    - fix: 修复使用OpenID作为第三方认证系统时，当OpenID服务异常后本地用户登录失败的问题
    - fix: 修复腾讯云同步地域信息获取不到雅加达区域的问题【企业版】
    - fix: 修复云管中心任务执行状态是否成功的判断条件【企业版】
    - fix: 修复数据库普通用户对PostgreSQL数据库进行批量改密时偶尔失败的问题【企业版】

!!! tip "依赖升级 🧰"
    - PyYAML==5.4
    - geoip2==4.4.0
    - Pillow==8.3.2
    - Django==3.1.13
    - eventlet==0.31.1
    - html2text==2020.1.16
    - jumpserver-django-oidc-rp==0.3.7.8

v2.14.2
------------------------
2021年09月24日

!!! summary "功能优化 🚀"
    - perf: 优化Lion组件的进程管理机制
    - perf: 优化当⽤户未授权应⽤时，Luna页⾯不显⽰⽤户应⽤授权树
    - perf: 优化改密计划执⾏⽇志⽂案【企业版】

!!! success "问题修复 🐛"
    - fix: 修复系统设置中测试邮件失败的问题
    - fix: 修复Lion组件服务退出后偶尔⾃启失败的问题
    - fix: 修复创建授权规则页⾯已选资产不能删除的问题
    - fix: 修复在特权⽤户详情中添加节点和资产时未及时更新资产特权⽤户的问题
    - fix: 修复Web Terminal连接字符类会话时复制粘贴（Ctrl+c/Ctrl+v）偶尔失效的问题
    - fix: 修复云管中⼼华为云获取地域信息时缺少拉美相关区域的问题【企业版】
    - fix: 修复通过XRDP组件连接Windows资产时⿏标偶尔会变为⿊⾊图标的问题【企业版

v2.14.1
------------------------
2021年09月22日

!!! success "问题修复 🐛"
    - fix: 修复登录页面错误提示信息颜色
    - fix: 修复在未开启SMS短信通知服务的情况下，在登录KoKo时会出现SMS二次认证选择项的问题
    - fix: 修复工单审批中只有当前审批人可以评论的问题
    - fix: 修复Web Terminal页面批量执行命令无响应的问题
    - fix: 修复表单页初始化提示错误信息的问题
    - fix: 修复弹出列表框滚动后看不到表头的问题
    - fix: 修复关闭XRDP后还可以使用上次的方式登录成功的问题

!!! summary "功能优化 🚀"
    - fix: 优化Web Terminal登录框允许动态用户输入用户名

v2.14.0
------------------------
2021年09月16日

!!! info "新增功能 🌱"
    - feat: 新增 会话活动页面（记录用户加入/离开共享会话的日志）
    - feat: 新增 个人信息页面用户可以开启消息接受方式（如：企业微信、钉钉等）
    - feat: 新增 Web Terminal 终端主题设置功能 (仅支持 SSH/Telnet 会话)
    - feat: 新增 会话共享、协同操作功能（目前仅支持通过 Web Terminal 连接的 SSH/Telnet 会话）
    - feat: 新增 数据库改密功能【企业版】
    - feat: 新增 工单二级审批功能【企业版】
    - feat: 新增 XRDP Windows 会话全屏的功能【企业版】
    - feat: 新增 XRDP Windows 会话可挂载本地磁盘的功能【企业版】
    - feat: 新增 Google Cloud Platform (谷歌云) 资产同步功能【企业版】
    - feat: 新增 短信 MFA 认证方式 (目前支持阿里云、腾讯云短信服务)【企业版】

!!! summary "功能优化 🚀"
    - perf: 优化 配置文件内容进行可视化
    - perf: 优化 Windows 会话支持移动端操作
    - perf: 优化 Windows 会话页面增加快捷键 Shift+Alt+Ctrl，可以快速呼出右侧栏
    - perf: 优化 针对第三方认证的用户 (如 OpenID、CAS 等) 登录时也进行 MFA 校验
    - perf: 优化 授权列表显示创建方式（如手动、工单）
    - perf: 优化 优化终端注册时名称长度处理逻辑
    - perf: 优化 XRDP 连接方式可以在配置中进行开启或关闭【企业版】
    - perf: 优化 创建授权时 (资产/应用) 系统用户字段不必填
    - perf: 优化 测试网关端口错误时的提示信息
    - perf: 优化 用户不能禁用或启用自己
    - perf: 优化 第三方认证的用户也可以通过企业微信、钉钉等扫码登录
    - perf: 优化 LDAP 同步提示信息
    - perf: 优化 终端注册的名称（包含宿主机 Hostname）
    - perf: 优化 资产选择列表显示 protocols 字段
    - perf: 优化 授权规则动作上传下载复制粘贴选择时，连接动作不可取消

!!! success "问题修复 🐛"
    - fix: 修复 XRDP Windows 会话偶尔终端失败的问题
    - fix: 修复 磁盘、内存等偶尔未告警的问题
    - fix: 修复 应用账号不能通过用户名过滤的问题
    - fix: 修复 已关联资产的特权用户删除失败的问题
    - fix: 修复 WebSocket 引起的 Redis 连接持续增加的问题
    - fix: 修复 设置未分组节点显示单独授权资产的配置时，用户授权树没有变化的问题
    - fix: 修复 资产和特权用户关系发生变化时，资产特权用户没有及时更新的问题
    - fix: 修复 批量更新组织失败的问题【企业版】

!!! tip "依赖升级 🧰"
    - PyYAML==5.2
    - PyMySQL==1.0.2
    - cx-Oracle==8.2.1
    - psycopg2-binary==2.9.1
    - google-cloud-compute==0.5.0
    - tencentcloud-sdk-python==3.0.477
    - jumpserver-django-oidc-rp==0.3.7.7
    - alibabacloud_dysmsapi20170525==2.0.2

v2.13.2
------------------------
2021年08月27日

!!! success "问题修复 🐛"
    - fix: 修复普通用户在"我的资产"页面看不到资产连接按钮的问题

v2.13.1
------------------------
2021年08月20日

!!! success "问题修复 🐛"
    - fix: 修复创建节点报错的问题
    - fix: 修复创建用户手动设置密码报错的问题
    - fix: 修复 WebSocket 引起的 Redis 连接数量持续增长的问题
    - fix: 优化 Celery 健康检测逻辑
    - fix: 优化资产 API 接口返回 platform、protocols 字段

v2.13.0
------------------------
2021年08月19日

!!! info "新增功能 🌱"
    - feat: 新增应用树视图
    - feat: 新增 Core、Celery 终端
    - feat: 支持服务数据库 MySQL 8.0 版本
    - feat: 支持 Core、Celery 终端的系统监控
    - feat: 支持管理员终断数据库会话
    - feat: 支持飞书认证实现用户登录
    - feat: 支持飞书通知以及消息订阅
    - feat: 支持会话录像水印功能
    - feat: 支持通过 ssh 协议登录已开启 MFA 二次认证的资产
    - feat: 支持 MariaDB 数据库连接（命令行方式）
    - feat: 支持对 rz、sz 命令上传下载文件的控制和日志审计
    - feat: 支持通过 ssh 命令直连资产的连接格式，使用分割符号 `#`，且可使用系统用户 ID 和资产 ID 登录（两者必须同时为 UUID）
    - feat: 支持通过拉起客户端建立 XRDP 会话【企业版】
    - feat: 支持云管中心同步任务设置同步 IP 网段和协议组【企业版】
    - feat: 支持云管中心同步任务设置 Unix 特权用户和 Windows 特权用户【企业版】
    - feat: 支持批量更改资产用户密钥（批量改密模块）【企业版】

!!! summary "功能优化 🚀"
    - perf: 新增配置项: Core 登录跳转时间间隔（0 表示直接跳转）`LOGIN_REDIRECT_FLASH_MESSAGE_INTERVAL`
    - perf: 新增配置项: Core 登录重定向后端（可选项: OPENID、CAS） `LOGIN_REDIRECT_TO_BACKEND`
    - perf: 新增配置项: Core 云管中心同步任务执行历史保留天数 `CLOUD_SYNC_TASK_EXECUTION_KEEP_DAYS`【企业版】
    - perf: 新增配置项: Lion 定时清理挂载盘文件的时间，默认 1 小时；当值 <= 0 时，不做清理 ``
    - perf: 优化服务启动脚本
    - perf: 优化资产账号列表、应用账号列表视图
    - perf: 优化应用列表支持多类型筛选
    - perf: 优化应用账号支持导出选中项
    - perf: 优化应用管理支持批量删除
    - perf: 优化网域网关密码支持输入特殊字符
    - perf: 优化测试网域可连接性的错误提示信息
    - perf: 优化支持资产账号通过节点过滤
    - perf: 优化资产详情页面支持查看关联系统用户
    - perf: 优化支持针对一个资产面向多个系统用户的推送和测试
    - perf: 优化工单推荐资产和应用的数量，分别为100、15
    - perf: 优化针对 LDAPServerURL 前缀进行的校验
    - perf: 优化 Luna 页面搜索资产后按资产名称排序
    - perf: 优化用户列表支持角色搜索
    - perf: 优化节点资产映射缓存清除逻辑
    - perf: 优化添加新的 es 时自动创建索引
    - perf: 优化修改日志时间格式（兼容 firefox 浏览器）
    - perf: 优化完善用户操作日志记录，如：资产节点的关系变化、组织成员的添加和移除等
    - perf: 优化用户创建资产操作体验，跳转到新页面进行创建，创建成功后自动重定向到资产详情页
    - perf: 优化针对系统用户和账号密码进行校验，不能包含特殊字符
    - perf: 优化校验改密计划密码不能包含字符 【企业版】
    - perf: 优化改密任务执行添加触发模式字段：手动触发、定时触发【企业版】
    - perf: 优化改密任务执行支持显示触发字段（手动触发、定时触发）【企业版】

!!! success "问题修复 🐛"
    - fix: 修复 /api/docs/ 访问异常的问题
    - fix: 修复 es 命令存储过滤不准确的问题
    - fix: 修复用户登录时偶尔会因为验证码校验超时的问题
    - fix: 修复 SSHPrivateKey 错误导致系统用户列表加载失败的问题
    - fix: 修复用户详情授权的资产页面收藏夹下拉报错的问题
    - fix: 修复删除远程应用关联的资产后，更页面显示资产 ID 的问题
    - fix: 修复资产批量推送和测试可连接性异常的问题
    - fix: 修复更新用户时校验用户密码规则偶尔异常的问题
    - fix: 修复在系统用户的账号列表中修改密码后偶尔登录资产失败的问题
    - fix: 修复创建网关没有密码的问题
    - fix: 修复配置消息订阅时所选用户为当前组织用户的问题
    - fix: 修复修复微信钉钉多次测试报错的问题
    - fix: 修复数据库应用更新页面异常问题
    - fix: 修复云管中心同步资产时重复创建的问题【企业版】
    - fix: 修复 XRDP 会话偶尔不能终断的问题【企业版】
    - fix: 修复查看应用授权列表报错的问题【企业版】
    - fix: 修复 XRDP 设置分辨率不生效的问题【企业版】
    - fix: 修复工单已关闭后可以再次审批的问题【企业版】
    - fix: 修复组织列表中系统用户与特权用户数量不准确的问题【企业版】
    - fix: 修复收集 Windows 资产用户时未收集到全部用户的问题【企业版】
    - fix: 修改迁移数据库时 default 值设置报错的问题，MySQL 8.0【企业版】
    - fix: 修复通过 OmniDB 连接包含 `-` 字符的数据库时失败的问题【企业版】

!!! tip "依赖升级 🧰"
    - ansible==2.9.24
    - boto3==1.18.11
    - botocore==1.21.11
    - Django==3.1.12
    - requests==2.25.1
    - urllib3==1.26.5
    - s3transfer==0.5.0
    - jms-storage==0.0.39

v2.12.2
------------------------
2021年08月12日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复访问`API文档`页面失败的问题
    - fix: 修复使用`es`存储时，搜索命令不准确的问题
    - fix: 修复`SshPrivateKey`错误导致系统用户列表加载失败的问题
    - fix: 修复由于`installer`不包含`nginx:alpine2`镜像导致`启用LB`失败的问题
    - fix: 修复云管中心同步资产时相同实例会重复创建的问题【企业版】

v2.12.1
------------------------
2021年07月21日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 网关密码支持使用`特殊字符`
    - fix: 修复`KoKo`显示资产节点树排序乱序问题
    - fix: 修复界面设置登录页面图片显示异常问题【企业版】
    - fix: 通过`XRDP`连接`Windows`资产支持自定义分辨率【企业版】
    - fix: 增加`申请资产工单`中推荐资产的数量（默认`100`）【企业版】

v2.12.0
------------------------
2021年07月15日

!!! tip "版本升级 What’s Upgraded"
    - qingcloud-sdk==1.2.12

!!! info "🌱 新功能 Features"
    - feat: **支持 `arm64` 架构部署**
    - feat: `Web Terminal`支持使用`rz`、 `sz`命令上传下载文件
    - feat: 支持设置`默认存储`（命令、录像）；针对`新注册`的终端使用管理员设置的默认存储
    - feat: 支持通过 `XRDP` 组件连接的资产，当`授权过期`和`空闲超时`自动断开
    - feat: `批量命令`支持更广泛的设备，如：思科等网络设备
    - feat: 将`管理用户`、`系统用户`模块统一成为`系统用户`模块，并按`普通用户`和`特权用户`进行展示
    - feat: 云管中心支持`华为私有云`、`青云私有云`的资产同步【企业版】

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复单独设置过的`系统用户认证信息`登录资产失败的问题
    - fix: 修改创建用户时如果没有在任何组织内默认添加到`Default`组织
    - fix: 修复`登录页面`的翻译问题
    - fix: 修复`应用`无法下载`xrdp`文件的问题
    - fix: 修复`OpenID`登录跳转问题
    - fix: 修复`系统消息通知`升级错误的问题
    - fix: 修复自动生成的系统用户密码中包含特殊双字符时测试可连接性失败的问题
    - fix: 修复`定时任务`偶尔不执行问题
    - fix: 修复`过期用户登录`提示不明确的问题
    - fix: 修复用户组删除时`授权树`不会自动更新的问题
    - fix: 修复全局组织`命令记录`显示为空的问题
    - fix: 修复用户列表`角色字段`不显示的问题
    - fix: 修复改密日志支持`模糊`搜索
    - fix: 修复导出系统用户资产列表时包含`组织名称`字段
    - fix: 修复当用户无效时`企业微信`、`钉钉`扫码登录后台报错的问题
    - fix: 修复`网关测试连接`后台报错的问题
    - fix: 修复`Lion`下载超过`1.6G`文件时失败的问题
    - fix: 修复`会话详情`中录像播放失败的问题
    - fix: 修复`审计员`可以点击`Dashboard`页面的资产/用户总数的问题
    - fix: 修复`消息订阅`取消按钮无法使用的问题
    - fix: 修复`XRDP`终端上报系统状态数据不准确的问题

!!! summary "🚀 功能优化 Optimization"
    - perf: 优化`LDAP`用户导入的组织为当前组织
    - perf: 优化`CAS`配置支持自定义属性映射
    - perf: 优化由于`SSH`连接复用造成的阻塞问题
    - perf: 优化`资产账号`不能导出所有的问题（默认显示所有账号）
    - perf: 优化`改密计划`任务日志【企业版】

v2.11.4
------------------------
2021年07月06日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复 Gateway Private Key 包含 passphrase 无法连接的问题
    - fix: 修复 Windows 安装的 Visual Studio Code 客户端无法使用 remote-ssh 插件的问题

!!! summary "🚀 功能优化 Optimization"
    - perf: 优化KoKo异步加载时取消自动补全

v2.11.3
------------------------
2021年06月29日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复`MySQL`数据库命令行连接方式命令无记录问题
    - fix: 修复通过`MySQL命令行`连接数据库失败的问题
    - fix: 修复`Windows会话`不能全屏的问题
    - fix: 修复`系统设置`中邮件没有更改就无法更新的问题
    - fix: 修复`改密任务`

v2.11.2
------------------------
2021年06月24日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复`OpenID`登录跳转的问题
    - fix: 修复`登录页面`部分中文未翻译的问题
    - fix: 修复`Luna`页面使用`Token`登录失败的问题
    - fix: 修复`第三方用户`登录成功后在用户列表不显示的问题
    - fix: 修复关联了`网域`(网域中没有网关)的资产登录失败的问题

!!! summary "🚀 功能优化 Optimization"
    - perf: 通过`LDAP`导入的用户默认加入到`当前组织`

v2.11.1
------------------------
2021年06月18日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复获取系统用户认证信息失败的问题（影响：单独设置过资产账号的密码的用户登录资产会失败）
    - fix: 修复升级问题（系统消息通知相关）
    - fix: 修复基础平台等可以删除更新问题
    - fix: 修复会话详情中不能播放录像的问题

!!! summary "🚀 功能优化 Optimization"
    - perf: 优化XRDP终端的默认名称

v2.11.0
------------------------
2021年06月17日

!!! tip "版本升级 What’s Upgraded"
    - jms-storage-sdk==0.0.37

!!! info "🌱 新功能 Features"
    - feat: 新增站内信模块，⽀持订阅、推送和查看内部消息提⽰。如：危险命令告警、监控告警等
    - feat: ⽀持通过 SSH ⼯具直连资产。如：ssh jumpserverUsername@systemUsername@AssetIP@jumpserverHostIP
    - feat: ⽀持通过 Visual Studio Code 的 Remote - SSH 插件连接资产进⾏远程开发（⽬前仅⽀持 Linux 资产)
    - feat: ⽀持使⽤华为云对象存储服务 OBS 对会话录像进⾏存储
    - feat: 新增账号管理模块。包括资产账号、应⽤账号、收集⽤户和批量改密等功能 【企业版】
    - feat: 新增XRDP组件，⽀持通过本地客户端直接连接资产，建⽴ RDP、VNC 等协议的图形会话 【企业版】

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复 Redis 服务异常时(如: 主从切换)⽤户 session ⽴即过期的问题
    - fix: 修复导⼊模版⽣成的列表中没有显⽰整数类型所在列的问题
    - fix: 修改周期监测任务的配置参数
    - fix: 修复 Default 组织中⽤户数量统计错误的问题
    - fix: 修复获取⽹关信息没有密码的问题
    - fix: 修复导⼊数据没有处理整数类型数据的问题
    - fix: 修复创建/更新⽤户时密码策略相关的问题
    - fix: 修复删除资产账号时报错的问题
    - fix: 修 复LDAP 提交时 json 报错的问题
    - fix: 修复我的资产页⾯按钮消失的问题
    - fix: 修复 Azure 云管账号创建必填字段提⽰信息 【企业版】
    - fix: 修复组织批量删除的问题，禁⽌批量删除 【企业版】

!!! summary "🚀 性能优化 Optimization"
    - perf: 获取资产⽤户信息返回 Name 和 BackendDisplay 字段
    - perf: 优化系统⽤户，⽀持⽤户设置临时密码
    - perf: 优化记录 Token 认证的登录⽇志
    - perf: 优化字符会话中命令解析的记录时间
    - perf: 优化 KoKo 组件的代码结构，并重构部分代码逻辑
    - perf: 优化连接 RDP 会话的窗⼜显⽰（可⾃适应窗⼜）
    - perf: 优化连接 RDP 会话的分辨率（可⼿动配置）
    - perf: 优化通过 Luna 页⾯登录资产时对系统⽤户的选择，提升⽤户使⽤体验
    - perf: 优化云账号测试失败的提⽰信息 【企业版】
    - perf: 优化云同步的资产创建者字段为 System 【企业版】

v2.10.4
------------------------
2021年06月08日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复在其他组织中创建的用户默认会添加到Default组织的问题【企业版】@fit2bot (https://github.com/jumpserver/jumpserver/pull/6235)
    - fix: 禁止批量删除组织【企业版】@fit2bot (https://github.com/jumpserver/jumpserver/pull/6221)
    - fix: 修改文件管理页面的标题文案

v2.10.3
------------------------
2021年06月02日

!!! success "🐛 Bug修复 Bug Fixes"
    - perf: 修改 Logo 和文案的显示
    - perf: 优化 RDP 右侧菜单

v2.10.2
------------------------
2021年05月26日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复创建/更新用户时密码策略相关的问题 (https://github.com/jumpserver/jumpserver/pull/6176)
    - fix: 修复Parser没有处理整数类型数据的问题 (https://github.com/jumpserver/jumpserver/pull/6174)
    - fix: 修复连接图形会话时，当鼠标移出操作窗口无法再正常输入的问题

v2.10.1
------------------------
2021年05月21日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复通过网关登录资产不成功的问题 (https://github.com/jumpserver/jumpserver/pull/6168)
    - fix: 修复仪表盘用户数量统计有误的问题 (https://github.com/jumpserver/jumpserver/pull/6163)
    - fix: 修复周期监测任务配置不生效的问题 (https://github.com/jumpserver/jumpserver/pull/6160)

v2.10.0
------------------------
2021年05月20日

!!! tip "组件说明"
    - Lion 是 JumpServer 新组件，使用 Golang 和 Vue 重构了 guacamole-client，自 v2.10.0 (含) 版本起 Lion 将负责 JumpServer 的 RDP 和 VNC 等图形会话连接功能

!!! tip "版本升级 What’s Upgraded"
    - jms-storage==0.0.36

!!! info "🌱 新功能 Features"
    - feat: 新增 Lion 图形化连接组件
    - feat: 支持用户通过企业微信、钉钉进行登录
    - feat: 支持RDP、VNC协议的会话监控
    - feat: 新增命令复核功能【企业版】

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复自动推送的系统用户很快过期的问题
    - fix: 修复创建动态系统用户时设置了home目录，使得所有推送的用户共用同一个home目录，导致目录权限只限制在第一个推送的用户，其他用户进行可连接性测试时失败的问题
    - fix: 修复对应用、应用授权、访问控制策略等操作未记录日志的问题
    - fix: 修复仪表盘在线用户数量不准确的问题
    - fix: 修复命令记录不可以导出选择项的问题
    - fix: 修复自动生成公钥优先使用dss格式的问题(修改为默认优先使用rsa)
    - fix: 修复创建资产时protocols字段默认值有误的问题
    - fix: 修复创建资产不传nodes报错的问题
    - fix: 修复OPTION资产API时报JSON序列化失败的问题
    - fix: 修复上传xslx文件中包含数字类型数据时报错的问题
    - fix: 修复RemoteApp获取资产信息失败的问题
    - fix: 修复存在在线会话的终端可以被删除的问题
    - fix: 修复网关更新可以获取到明文密码的问题
    - fix: 修复点击修改密码时密码框丢失的问题
    - fix: 修复系统用户VNC用户名必填的问题
    - fix: 修复系统用户详情中没有更多操作的问题
    - fix: 修复详情页面包含多个Tab页引起的设置和弹窗问题
    - fix: 修复上传超大文件超时问题
    - fix: 修复同步不存在Parent的VMware虚拟机时失败的问题【企业版】
    - fix: 修复数据库组件创建Session时user字段中间不添加空格【企业版】
    - fix: 修复数据库组件网关不传递密码报错的问题【企业版】
    - fix: 修复组织详情关联用户报错的问题【企业版】
    - fix: 修复改密计划页面更新资产、节点报错的问题【企业版】
    - fix: 修复云管账号详情页面点击更新失败的问题【企业版】
    - fix: 修复云管中心创建账户后跳转到任务列表页面的问题【企业版】
    - fix: 修复收集用户任务创建不填写周期执行报错的问题【企业版】
    - fix: 修复包含组织管理员、组织审计员时可以删除组织的问题【企业版】

!!! summary "🚀 性能优化 Optimization"
    - perf: 优化过期用户可以立即退出登录
    - perf: 优化资产授权过期时在线会话自动断开
    - perf: 优化创建es命令存储时可设置是否忽略SSL证书
    - perf: 优化用户公钥设置功能，管理员可配置是否允许用户设置公钥
    - perf: 优化用户登录体验，用户使用CAS、OpenID等第三方认证时，实现延时自动登录
    - perf: 优化用户更改密码时不可使用前n次历史密码，管理员可设置历史密码不可重复次数
    - perf: 优化授权导入功能，支持使用用户名、资产名、ip、节点路径、系统用户名称进行导入
    - perf: 优化系统用户可以对指定资产进行可连接性测试
    - perf: 优化管理员可以设置用户下次登录前是否需要修改密码
    - perf: 优化节点删除时可以包含子孙节点但不包含子孙资产的节点
    - perf: 优化添加无效的es命令存储时抛出错误提示
    - perf: 优化DB协议类型系统用户手动登录时用户名必填
    - perf: 优化MFA认证提示信息
    - perf: 优化校验资产授权过期API响应中包含授权过期时间
    - perf: 优化工单邮件信息【企业版】
    - perf: 优化工单处理人只能同意或拒绝【企业版】
    - perf: 收集用户任务添加详情页面和执行历史页面【企业版】
    - perf: 申请资产详情工单添加 action 字段、资产授权详情链接【企业版】
    - perf: 优化云主机同步创建资产节点/网域名称时，Provider默认使用英文【企业版】

v2.9.2
------------------------
2021年04月20日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复操作应用/应用授权/访问控制等未记录日志的问题 @fit2bot (https://github.com/jumpserver/lina/pull/5990)
    - fix: 修复自动推送的系统用户不可用（立即过期）的问题 @fit2bot (https://github.com/jumpserver/lina/pull/5986)
    - fix: 修复通过网域连接数据库，网关使用PrivateKey后台时报错的问题【企业版】

v2.9.1
------------------------
2021年04月19日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 临时移除 Database 协议的用户名与密码相同 选项 @fit2bot (https://github.com/jumpserver/lina/pull/755)
    - fix: 修复创建的系统用户很快过期的问题 @fit2bot (https://github.com/jumpserver/jumpserver/pull/5980)

v2.9.0
------------------------
2021年04月15日

!!! tip "版本升级 What’s Upgraded"
    - cryptography==3.3.2
    - Django==3.1.6
    - Jinja2==2.11.3
    - Pillow==8.1.1

!!! info "🌱 新功能 Features"
    - feat: 重构资源`导入导出`功能
    - feat: 新增`Dashboard`页面打印和`PDF导出`功能
    - feat: 新增云管中心`Nutanix云`同步功能【企业版】

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复`Default`组织下出现`App`用户的问题
    - fix: 修复`管理用户`输入带密码的秘钥报错的问题
    - fix: 修复访问`tokens`接口时用户最后登录时间未更新的问题
    - fix: 修复过期用户登录提示`用户无效`的问题
    - fix: 修复`Elasticsearch`命令存储索引未创建不可用的问题
    - fix: 修复`系统设置`配置项未即时更新的问题
    - fix: 修复组件和终端列表中`在线会话数量`有时不准确的问题
    - fix: 修复连接`k8s`资产不能使用`vim`编辑的问题
    - fix: 修复`rz`上传文件慢的问题
    - fix: 修复创建远程应用默认`Path`丢失的问题
    - fix: 修复更新命令存储失败的问题
    - fix: 修复更新资产更多信息失败的问题
    - fix: 完善页面邮箱地址校验规则
    - fix: 修复`AWS`账号测试可连接性问题【企业版】

!!! summary "🚀 性能优化 Optimization"
    - perf: 优化`授权节点`和`授权资产`的排列顺序
    - perf: 支持`Elasticsearch`命令存储可指定`忽略证书认证`
    - perf: 优化`访问控制`登录失败提示信息
    - perf: 优化`nodes/<uuid>/children/add/`API支持`put`和`patch`方法
    - perf: 资产授权支持按`名称`进行模糊搜索
    - perf: 优化授权资产列表显示`platform`名称
    - perf: 配置文件支持修改`全局组织`的名称
    - perf: 支持`MFA`登录失败次数限制
    - perf: 移除`components/state/`API，使用`terminal/status/`API进行替换
    - perf: 优化`健康检测`API，返回`DB`、`Redis`等状态信息
    - perf: 添加`SSO`用户登录日志记录
    - perf: 登录`KoKo`进行资产搜索支持自动补全
    - perf: 创建`RDP系统用户`可填写用户附属组
    - perf: 优化`全局组织`下禁止用户更新用户组
    - perf: 修改创建`K8S系统用户`的权限问题
    - perf: 非`Local`用户禁止更新密码
    - perf: 优化推送系统用户，设置有效期

v2.8.4
------------------------
2021年04月14日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复升级后Default组织下资产节点树为空的问题 @fit2bot (https://github.com/jumpserver/jumpserver/pull/5957)

v2.8.3
------------------------
2021年04月09日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复 `test cookie` 问题 @fit2bot (https://github.com/jumpserver/jumpserver/pull/5931)
    - fix: 管理用户输入带密码的秘钥报错 @fit2bot (https://github.com/jumpserver/jumpserver/pull/5899)
    - fix: 修复 `Default` 组织下出现 app user @fit2bot (https://github.com/jumpserver/jumpserver/pull/5863)
    - fix: 修复使用 rz 命令上传文件慢的问题 @fit2bot (https://github.com/jumpserver/koko/pull/578)
    - fix: 修复AWS国际区账号测试可连接性的异常问题【企业版】
    - fix: 修复资产更多信息更新失败的问题 @fit2bot (https://github.com/jumpserver/lina/pull/726)
    - fix: 修复命令存储更新失败的问题 @fit2bot (https://github.com/jumpserver/lina/pull/717)

v2.8.2
------------------------
2021年03月24日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 授权树节点排序 @fit2bot (https://github.com/jumpserver/jumpserver/pull/5836)
    - fix: 修改mfa强制启用的文案 @fit2bot (https://github.com/jumpserver/jumpserve/pull/5833)
    - perf: 添加会话来源 rdp terminal @fit2bot (https://github.com/jumpserver/jumpserve/pull/5830)
    - fix: 修复登录ip限制提示 @fit2bot (https://github.com/jumpserver/jumpserve/pull/5823)
    - fix: 修复创建远程应用默认Path丢失的问题 @fit2bot (https://github.com/jumpserver/lina/pull/712)
    - fix: 修复创建K8S系统用户的权限问题 @fit2bot (https://github.com/jumpserver/lina/pull/706)
    - fix: 恢复RDP系统用户user_group字段 @fit2bot (https://github.com/jumpserver/lina/pull/711)
    - fix: k8s vim编辑问题 @fit2bot (https://github.com/jumpserver/koko/pull/569)

!!! summary "🚀 性能优化 Optimization"
    - perf: 优化全局组织下禁止用户更新用户组 @fit2bot (https://github.com/jumpserver/lina/pull/708)

v2.8.1
------------------------
2021年03月19日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复创建用户失败的问题
    - fix: 修复`LDAP导入的用户`用户名中包含空白字符的问题
    - fix: 修复`LDAP配置`属性映射字段不显示默认值的问题
    - fix: 修复可以登录`已禁用资产`的问题
    - fix: 修复文件管理可以看到`已禁用资产目录`的问题
    - fix: 修复更多`更多操作按钮`下拉菜单为空仍然显示的问题

!!! summary "🚀 性能优化 Optimization"
    - perf: 优化`云管中心导入主机`异常捕获逻辑【企业版】

v2.8.0
------------------------
2021年03月18日

!!! tip "版本升级 What’s Upgraded"
    - paramiko==2.7.2
    - jumpserver-django-oidc-rp=0.3.7.6
    - pycryptodome==3.10.1
    - pycryptodomex==3.10.1
    - pyvmomi==7.0.1
    - termcolor==1.1.0
    - azure-identity==1.5.0
    - azure-mgmt-subscription==1.0.0
    - pycrypto==2.6.1 (移除)

!!! info "🌱 新功能 Features"
    - feat: 新增访问控制功能
    - feat: 新增用户登录限制功能，支持通过`IP地址`进行控制
    - feat: 新增用户登录资产复核功能，针对通过`ssh`和`telnet`协议登录的资产进行复核【企业版】
    - feat: 新增云管中心`VMware私有云`同步【企业版】
    - feat: 新增云管中心`Azure国际云`同步【企业版】
    - feat: 新增自定义表格列功能
    - feat: 新增限制用户只能从`Source`登录的功能
    - feat: 新增`Luna`左侧授权资产树右键全部展开的功能
    - feat: 新增全局组织功能，默认组织改为实体组织【企业版】

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 修复资源权限校验时组织切换的问题
    - fix: 修复组件状态上报`API`偶发报错的问题
    - fix: 修复命令存储`es`类型`主机`字段带用户名密码提交报错的问题
    - fix: 修复禁用`MFA`之后，短时间内还可以查看密码的问题
    - fix: 修复文件管理在当前目录下复制、粘贴文件报错的问题
    - fix: 修复存在无效`es`存储配置时命令记录页面访问失败的问题
    - fix: 修复`Luna`终端显示字符不完整的问题
    - fix: 修复系统用户名包含`/`字符无法使用文件管理功能的问题
    - fix: 修复由于`Chrome`版本兼容性问题导致的日期计算错误
    - fix: 修复工单列表字段展示错误的问题【企业版】
    - fix: 修复默认平台列表可删除的问题
    - fix: 修复访问用户页面无权限的问题

!!! summary "🚀 性能优化 Optimization"
    - perf: 优化用户登录页面
    - perf: 重构`celery`使用`Threads`模型，减少内存使用
    - perf: 优化`settings`配置，采用`redis`消息发布订阅机制
    - perf: 优化命令记录列表，添加命令存储树展示
    - perf: 设置用户`source(来源)`字段为可更新
    - perf: 会话列表支持模糊搜索
    - perf: 重构&优化资产树、用户授权树加载速度
    - perf: 优化用户详情页授权列表加载速度
    - perf: 资产授权规则添加是否有效的过滤条件
    - perf: 重置用户`MFA`发送邮件提醒邮件
    - perf: 优化批量更新会查询全部数据的问题
    - perf: `Ansible`任务执行增加结果汇总信息
    - perf: 优化定期检查磁盘，添加可控制配置
    - perf: 系统用户支持`OPENSSH`格式的私钥
    - perf: 优化系统用户生成密码的复杂度（包含数字、字母大小写、特殊字符）
    - perf: `OPTION` API添加默认值，前端可以直接使用
    - perf: 优化`org`获取逻辑，采用`redis`消息发布订阅机制维护`orgs_mapping`数据
    - perf: 移除资源创建时对于`Auditor`用户的限制
    - perf: 管理用户详情页添加认证方式与秘钥指纹
    - perf: 优化命令记录列表加载慢的问题
    - perf: 优化用户详情页的资产授权列表慢的问题
    - perf: 添加批量导入时将文件(csv, excel)解析为`JSON`数据格式的接口
    - perf: 支持修改`忘记密码`与`重置密码`的链接
    - perf: `Luna`页面获取资产系统用户按`name`排序
    - perf: 优化系统用户、命令过滤器等关于优先级的问题（数值越小越先）
    - perf: 点击登录页面右侧图片可直接跳转到`Github`工程项目
    - perf: 文件管理支持在当前目录进行复制、粘贴
    - perf: 修改终端登录页面的强制刷新接口
    - perf: 增加新的`SSH KexAlgorithms`算法【KoKo】
    - perf: 优化终端的节点展示（同一级节点以`Name`排序）
    - perf: 添加禁用资产颜色区分
    - perf: 优化列表页面下拉的配色
    - perf: 优化命令执行的输出
    - perf: 去掉`Remote App`中的网域选择
    - perf: 优化创建系统用户时先选择协议
    - perf: 优化移除用户和删除用户的行为

v2.7.1
------------------------
2021年02月03日

!!! success "🐛 Bug修复 Bug Fixes"
    * 修复Windows 2003 和 2008 等 RDP 连接失败的问题
    * 修复浏览器多个 tab 页连接 Windows 资产相互冲突的问题
    * 修复 Chrome 兼容性导致的日期显示问题
    * 修复 KoKo 终端窗口大小不一致造成的显示问题

!!! summary "🚀 性能优化 Optimization"
    * 减少 celery 启动数量
    * 会话列表支持模糊搜索
    * 还原用户来源字段的设置
    * 优化 KoKo 录像文件上传，减少内存使用
    * 添加工单申请人字段显示 【企业版】

v2.7.0
------------------------
2021年01月21日

!!! info "🌱 新功能 Features"
    * 支持批量测试资产的可连接性
    * 批量命令执行被拒绝时发送危险命令告警邮件
    * 管理用户详情页中添加关联的资产列表页面
    * 支持申请应用工单【企业版】
    * 组织管理中可查看组织资源的统计数量【企业版】

!!! success "🐛 Bug修复 Bug Fixes"
    * 修复系统设置提交失败的问题
    * 修复资产导入包含disk_info信息时失败的问题
    * 修复授权规则变更时系统用户关联资产没有更新的问题
    * 修复推送系统用户到资产偶尔失败的问题
    * 修复清除审计日志时循环调用的问题
    * 修复危险命令告警邮件发送失败的问题
    * 修复访问日志文件的漏洞
    * 修复创建系统平台时名称错误信息重复提示的问题
    * 修复当用户名超过64字符时命令记录保存失败的问题
    * 修复资产用户列表更新密码失败的问题
    * 修复资产树超过屏幕时右键菜单显示不完整的问题
    * 修复资产列表没有克隆按钮的问题
    * 修复应用详情中移除系统用户失败的问题

!!! summary "🚀 性能优化 Optimization"
    * 重构工单模块
    * 重构应用模块
    * 重构命令、录像存储模块
    * 优化Celery任务执行时包含的子任务日志保存问题
    * 支持获取多种协议类型的系统用户列表
    * 统一开源/企业版登录页面
    * 在登录页面添加CAS、OpenID等第三方登录链接，登录时不再自动跳转登录地址
    * 点击登录页面<忘记密码>链接时，不限制第三方认证的用户，在忘记密码页面进行判断与限制
    * 修改OPTION方法获取相关choices字段选项时对read_only属性的限制
    * 优化批量命令列表中用户字段显示格式
    * 优化登录日志的登录方式字段偶尔为空的问题
    * 优化Linux资产字符命令解析的问题
    * 优化录像文件上传超时的问题
    * 优化Web文件管理页面操作错误的提示信息
    * 优化测试存储可连接性的提示信息
    * 禁止更新系统用户的用户名与登录名相同字段
    * 重构云管中心的云管账号模块【企业版】

v2.6.2
------------------------
2021年01月14日

!!! success "Bug修复 Bug Fixes"
    * 修复远程执行漏洞

v2.6.1
------------------------
2020年12月21日

!!! tip "版本变化 What’s Changed"
    * 添加资产编号字段

!!! success "Bug修复 Bug Fixes"
    * 修复资产导入携带disk_info信息时失败的问题
    * 修复提交系统设置失败的问题
    * 修复系统用户私钥问题

v2.6.0
------------------------
2020年12月17日

!!! tip "版本变化 What’s Changed"
    * 升级 Python==3.8.6
    * 升级 Django==3.1

!!! info "新功能 Features"
    * 支持修改资产配置信息
    * 支持通过Excel文件对资源进行导入导出
    * 提供Prometheus的API调用进行各组件状态的监控
    * 新建jumpserver/installer工程，方便用户进行安装和升级
    * 系统用户详情页面增加资产列表子页面，可以对指定资产进行推送
    * 添加系统监控功能，方便监控各组件健康状态【企业版】

!!! success "Bug修复 Bug Fixes"
    * 修复列表克隆的问题
    * 修复我的资产页面数据问题
    * 兼容旧的组织用户关系接口
    * 修改判断活跃会话的判断逻辑
    * 修复清除幽灵会话失败的问题
    * 修复Default节点迁移问题
    * 修复搜索LDAP用户重复显示的问题
    * 修复命令过滤器添加系统用户问题
    * 修复只配置DC域时，LDAP用户认证失败的问题
    * 修改attrs不能为None的问题
    * 修复用户组授权树与资产问题
    * 修复推送动态系统用户时报错的问题
    * 当用户授权为空时清空旧的授权树
    * 修复在线会话时间显示问题
    * 修复节点创建时更新子节点错误日志输出问题
    * 修复动态系统用户和用户关系变化时没有推送到资产的问题
    * 修复首次登录页面重复出现的问题
    * 修复命令列表过滤使用session_id字段
    * 修复申请资产工单如果系统用户没填内容不推荐系统用户的问题
    * 修改访问/api/docs会产生的错误的问题
    * 修复用户详情页面中应用授权列表的过滤问题
    * 修复新建授权时动态用户可能推送不成功的问题
    * 修复创建应用授权后系统用户没有自动推送的问题
    * 修复工单申请资产审批时系统用户没有推荐的问题
    * 修复Luna无法隐藏侧边栏的问题
    * 修复Luna搜索过滤应用树的问题
    * 修改Luna登录跳转URL路径问题，解决直接访问Luna重定向问题
    * 修复腾讯云获取实例公网IP为None的问题【企业版】
    * 修复AWS同步时获取系统平台为None的问题【企业版】
    * 修复用户离开组织后授权的资产没主动刷新的问题【企业版】
    * 修复终端签名认证时取消校验host值，解决使用集群部署架构导致数据库组件注册不成功的问题【企业版】

!!! summary "性能优化 Optimization"
    * 添加表头过滤字段
    * 优化资产树节点排序问题
    * 修复申请工单错误提示信息
    * 资产模块添加批量删除操作
    * 优化telnet资产连接问题
    * 优化登录页面的验证码模块
    * 禁用应用列表的导入导出功能
    * 优化用户授权资产列表加载速度
    * 优化org_name数据库查询次数
    * 优化批量删除管理用户报错信息
    * 修复命令列表过滤字段文案会话ID
    * 密码过期后引导用户进行重置密码
    * 用户登录日志添加认证方式字段
    * 优化限制搜索授权资产返回的条数
    * 恢复Web终端入口到页面左侧菜单中
    * 用户禁止修改用户来源字段
    * 用户授权应用树按组织节点进行区分
    * 优化用户授权树返回org_name字段
    * 禁用对命令存储Elasticsearch的文档类型值进行修改
    * 优化检查节点资产数量的Celery任务
    * 优化用户列表响应慢的问题
    * Luna资产授权树根节点增加强制刷新Tree的右键菜单
    * 资产树右键菜单，增加手动计算节点下资产数量的选项
    * 支持应用分组织展示【企业版】
    * 禁止删除组织根节点的问题【企业版】

v2.5.3
------------------------
2020年12月7日

!!! success "Bug修复 Bug Fixes"
    * 修复centos的mirror问题
    * Node ordering [parent_key, value]
    * 修复默认组织Default节点显示问题(存在key为0的Default节点)
    * 新建授权时动态用户可能推送不成功
    * 锁定pip版本

v2.5.2
------------------------
2020年11月27日

!!! summary "性能优化 Optimization"
    * 优化用户列表在大规模数据下慢的问题
    * 修改节点资产数量自检程序的执行周期

!!! success "Bug修复 Bug Fixes"
    * Node 保存的时候，在信号里设置 parent_key
    * 修复动态系统用户和用户关系变化时没有推送到资产的问题
    * 兼容旧的组织用户关系API
    * 修复在动态用户所绑定的授权规则中，如授权给用户组，当用户组增加成员后，动态系统用户下没有相应增加用户，因此也不会自动推送的问题
    * 恢复Web终端入口
    * 修复列表克隆的bug

v2.5.1
------------------------
2020年11月23日

!!! summary "性能优化 Optimization"
    * 优化使用 pip mirror
    * 优化构建时用的 mirror
    * 获取用户所有授权时转换成 list 数据结构
    * 优化用户授权资产列表加载速度
    * 优化检查节点资产数量的 Celery 任务
    * 限制搜索授权资产返回的数据条数

!!! success "Bug修复 Bug Fixes"
    * 修复我的资产页面问题
    * 修复用户组授权树与资产问题
    * 当用户授权为空时，清空旧的授权树
    * 调整旧的组织与用户关联接口
    * 修复无法隐藏侧边栏的Bug
    * 修复过滤应用树bug
    * 修复批量更新组件的问题

v2.5.0
------------------------
2020年11月18日

!!! info "新功能 Features"
    * 支持Web版数据库审计；
    * 资源创建/更新表单增加克隆操作
    * 增加危险命令告警功能
    * 支持国密算法加密敏感信息
    * 支持Azure云主机同步【企业版】
    * 数据库应用连接支持网域网关

!!! success "Bug修复 Bug Fixes"
    * 修复资产授权规则导入失败的问题
    * 修复用户的资产不区分组织的问题
    * 修复网域端口可能随便填写的问题
    * 修复资产可以根据IP进行过滤
    * 资产列表添加默认date_created排序
    * 修复工单申请资产授权通过人显示不对的问题
    * 修改收藏夹的翻译
    * 修复系统用户与用户组发生变化时的报错信息
    * 设置网关的密码不能包含特殊字符
    * 修复用户登录失败次数出现0次的问题
    * 系统用户添加AD域字段
    * 把drf异常放到单独的日志文件中
    * 修复向资产推送系统用户时的问题
    * 修复创建申请资产工单的时候审批人不能搜索的问题
    * 修复SSO登录日志中没有登录方式的问题
    * 修改系统用户节点关系的搜索
    * org-member-relation的url拼写错误
    * 修复重置密码时的i18n翻译问题
    * 扩展Terminal的name字段长度
    * 修复删除节点下资产授权报错的问题
    * 修复华为云没有获取全部region下的vpc导致同步资产设置网域为default的问题【企业版】
    * 修复用户界面字段显示问题
    * 修复拖动组件窗口移动问题
    * 修复资产树根节点不显示title的问题

!!! summary "性能优化 Optimization"
    * 重构Application模块
    * 重构ApplicationPermission模块
    * 去掉Session中Terminal的外键关系
    * 用户界面隐藏左侧侧边栏web终端入口
    * 修改GatewayModel的ip字段类型为CharField
    * 添加资产导入时可以直接写节点名称
    * 推送系统用户增加comment
    * Task支持批量操作
    * 设置所有db协议类型会话不可被终断和监控
    * Session列表返回can_terminate；
    * 添加系统用户资产列表API
    * 管理用户的资产列表增加OPTIONS方法
    * 用户详情页面添加K8S应用
    * 修改文案Google Authenticator为手机验证器
    * 优化审计日志保存策略
    * 优化清除过期Session策略
    * 优化系统用户家目录权限更改
    * LDAP用户搜索，忽略大小写并支持模糊搜索
    * 统一用户授权详情列表的宽度
    * 修复表格兼容safari，不错位
    * 修复license过期提醒，开源版本出现split提示问题
    * 修复重命名节点，同名时有两条错误提示信息的问题
    * 改密计划详情中的资产选择，禁选已存在的资产
    * 优化网络请求，超时自动重试
    * 支持批量删除任务信息
    * 优化语言切换
    * 添加密码过期提醒
    * 升级依赖版本jms-storage==0.0.35
    * 升级依赖django-timezone-field==4.0
    * 升级依赖django-celery-beat==2.0
    * 添加依赖django-mysql==3.9.0
    * 添加Azure依赖包
    * 优化共享监控，可返回最新数据
    * MySQL连接支持使用网域网关
    * 优化elasticsearch的命令记录，增加时间字段
    * 优化KoKo注册机制
    * 优化云管中心同步逻辑【企业版】
    * 修改SyncInstanceDetail的asset字段可以为None，防止删除资产后当前同步实例详情记录也会被 删除，导致同步历史中的数量与同步实例不匹配的问题【企业版】
    * 改密计划生成默认密码规则为长度30，包含大小写，数字，特殊字符【企业版】

v2.4.4
------------------------
2020年11月12日

!!! tip "版本变化 What’s Changed"
    * 优化Tree加载
    * 添加Tree加载重试组件
    * 修复组织url拼写错误
    * 用户授权树重建冲突时弹出提示信息，并保留之前的树
    * 添加409错误信息

!!! summary "性能优化 Optimization"
    * 优化网络请求，超时自动重试

!!! success "Bug修复 Bug Fixes"
    * 当用户授权为空时，清空旧的授权树
    * 由于组织不对，导致生成或显示授权树错误
    * 优化授权树生成速度
    * org-member-relation url 拼写错误
    * 重建授权树冲突时，响应里加 code
    * 优化用户授权资产列表加载速度

v2.4.3
------------------------
2020年10月30日

!!! summary "性能优化 Optimization"
    * 优化根据资产获取授权的系统用户

v2.4.2
------------------------
2020年10月27日

!!! success "Bug修复 Bug Fixes"
    * 系统用户与用户组发生变化时报错
    * 资产列表添加默认 date_created 排序
    * 修复asset permission导入的bug
    * 修复asset permission导入的bug
    * AttributeError: 'UUID' object has no attribute 'name'
    * 修复删除节点下资产授权报错的问题

v2.4.1
------------------------
2020年10月20日

!!! success "Bug修复 Bug Fixes"
    * 修复用户的资产不区分组织的问题
    * 更新用户时org_roles参数为None时不更新组织角色

v2.4.0
------------------------
2020年10月15日

!!! tip "版本变化 What’s Changed"
    * 优化用户列表角色长度

!!! info "新功能 Features"
    * Server 类型的录像存储可以上传到其他外部对象存储，如：OSS
    * 用户重置密码成功后，发送用户重置密码成功邮件
    * 添加禁用资产链接提示
    * 新窗口打开可以指定系统用户功能
    * 禁止未激活资产链接
    * 工单入口移动至Header栏
    * 添加邀请用户进入组织功能
    * 添加403请求拦截器
    * 新增批量更新协议组

!!! summary "性能优化 Optimization"
    * 优化资产树策略，提升性能
    * 优化Middleware的使用
    * 优化构建docker，经常变动的包不使用镜像
    * 修改依赖包版本jms-storage==0.0.34
    * 修改依赖包版本Pillow==7.1.0
    * 应用授权树返回授权应用的总数量
    * 保证同时只有一个Beat在运行
    * 完善检查资产授权过期的Celery Task
    * 修改用户登录页面，使用其他方式认证时点击忘记密码提示联系管理员
    * 申请资产工单支持授权多个系统用户【企业版】
    * 优化左侧的树
    * 优化树节点搜索
    * 去掉websocket连接的代码
    * 优化iframe的url使用
    * 修复添加组织成员有更多按钮出现的问题
    * 管理员有license过期提醒，其它用户无license过期提醒
    * 去掉系统设置里面license过期提醒
    * 添加组织成员合并成一个card
    * 批量更新协议组给默认值
    * 优化授权详情页中的添加资产，将已添加的资产disable掉
    * 优化relationCard以及添加组织成员翻译
    * 优化授权工单，支持填写系统用户，审批时系统用户支持选多个
    * 优化license过期提醒
    * 修改界面设置的一些字段翻译
    * 在页面右上角添加web终端

!!! success "Bug修复 Bug Fixes"
    * 修复任务schedule属性的Bug
    * 修改检查资产授权过期策略的Bug
    * 修复正在使用的命令/录像存储可以被删除的Bug
    * 修复录像存储有问题导致下载录像的Bug
    * 修复组织管理添加用户失败的Bug
    * 调整刷新树时的API
    * 修复版本更新Index.html不刷新的问题
    * 修复页面title设置不生效问题
    * 修复命令执行选择资产报错问题
    * 如果数量为0 隐藏工单Badge
    * 调整未激活资产展示样式
    * 在Default组织下隐藏隐藏邀请用户按钮
    * 隐藏用户界面工单
    * 修复工单数量为0不显示工单按钮的问题
    * 修复改密计划创建时定期任务创建冲突的问题
    * 修复时间选择器显示宽度问题
    * 修改Tree的刷新Url
    * 修复表格的时间过滤问题
    * 修改添加用户API
    * 调整badge位置
    * 修复工单审批时系统用户多选参数配置问题
    * 临时禁用树节点移动
    * 修复测试网关端口数据类型：String改为Int类型
    * 修复命令存储更新问题
    * 修复命令过滤详情添加系统用户的问题
    * 修复更改组织时路径跳转的问题

v2.3.2
------------------------
2020年10月1日

!!! success "Bug修复 Bug Fixes"
    * 修复刷新资产列表有时报错的问题
    * 修复更新用户组织角色时报错的问题
    * 修复华为云同步实例获取vpc默认分页导致创建网域为default的问题
    * inject javascript script
    * G drive enable or not

v2.3.1
------------------------
2020年9月24

!!! success "Bug修复 Bug Fixes"
    * 修复使用 Token 连接资产失败的问题
    * 修复Redis连接未正常关闭而导致Redis服务异常的问题

v2.3.0
------------------------
2020年9月17日

!!! tip "版本变化 What’s Changed"
    * 设置对话框中增加可以设置是否开启右键快速复制功能，默认是不开启右键快速复制功能

!!! info "新功能 Features"
    * 使用新版KOKO终端页面接入

!!! summary "性能优化 Optimization"
    * 优化license的路由判断

!!! success "Bug修复 Bug Fixes"
    * 修正页面 ScrollBar 显示问题
    * 修复克隆窗口的 title 问题
    * 修复 settings 存储的 bug
    * 修复 windows 引起的构建问题
    * 检查本地语言版本
    * 修复Build失败的问题
    * 禁用命令记录列表导出选择项
    * 修复切换组织时权限展示问题

v2.2.3
------------------------
2020年9月15日

!!! summary "功能优化"
    * 修复系统用户导入模版没有密码字段的问题
    * 修复管理员未设置 Email 主题前缀导致发送邮件失败的问题
    * 请求时刷新 session age

v2.2.2
------------------------
2020年09月01日

!!! success "修复Bug"
    * 修复用户在不同组织引起的问题
    * 修复K8S系统用户更新时令牌是必填项的问题
    * use k8s app name

v2.2.1
------------------------
2020年08月25日

!!! note "修复Bug"
    * 修复init-kubectl兼容Centos系统

v2.2.0
------------------------
2020年08月20日

!!! info "新增功能"
    * 工单申请授权
    * Kubernetes 应用支持
    * 系统管理员首次登录，强制更新密码
    * 支持对RDP/VNC会话的复制、粘贴和上传、下载权限进行单独控制
    * 支持第三方系统SSO登录
    * 优化系统用户页面，新增home和groups字段
    * 添加用户界面K8S应用
    * 添加kubenetes应用
    * feat(Kubernetes): 添加K8S 应用支持

!!! summary "功能优化"
    * 修改组织删除失败翻译信息
    * 修改默认登录日志保存时间
    * 优化提示信息
    * 优化kubernetes更新页面翻译
    * 优化ip字段宽度，以及修改kubernetes apps翻译
    * 优化详情页bool值字段的显示
    * 增加ssh终端选中复制右键黏贴，增加批量发送ssh命令，增加tab标题右键功能
    * 重写luna翻译模块，默认中文

!!! success "修复Bug"
    * 修复工单comment
    * 创建组织用户不必填
    * 修复登录时有时解密失败
    * 登录复核 Not found
    * 修改用户角色显示名称
    * 远程应用MySQL Workbench添加port字段
    * file descriptor leaks
    * 去掉API请求的加载条
    * 优化用户列表和用户创建的角色
    * 创建mysql_workbench表单添加端口字段
    * 创建K8S系统用户时允许填写username
    * 修正新窗口打开的应用的问题
    * 修正翻译
    * 修改顶部菜单排列顺序以及调整Tree的隐藏显示
    * 修改翻译加载路由
    * 修复TS类型检查
    * 修复K8S应用链接问题

v2.1.2
------------------------
2020年08月13日

!!! success "修复Bug"
    * 修复JMSCSVParser调用serializer导致循环调用问题
    * default zh language code
    * 去掉任务详情中多余的ID字段
    * 修复打开多Tab引起Tab折叠的问题

v2.1.1
------------------------
2020年08月04日

!!! success "修复Bug"
    * 修复 es7 数据结构引起的命令无法查询的问题
    * 修复 cas 校验不通过的问题
    * 修复 perms api UserPermissionMixin 中 kwargs 参数传递（未发现引出其他问题）
    * 修复 radius decode error 的问题
    * 修复用户认证 Radius 认证中参数传递错误问题 `*kwargs -> **kwargs`
    * 设置环境语言 en_US.utf8
    * 修复中文输入
    * 修复当有搜索条件时禁用导出所有选项
    * 修复创建远程应用密码框显示明文的问题
    * 开启 Preload
    * 修复详情页数据如果没有 ID 字段，则不显示 ID
    * 优化工单详情
    * 优化列表组件一些字段的宽度
    * 优化创建命令存储的提示文案
    * 更新 xpack 指向
    * 优化资产详情中网域字段名的显示
    * detailCard 增加 ID 字段
    * 优化授权列表添加刷新按钮
    * 修复命令过滤执行的系统用户选择
    * 修复翻页搜索结果不正确的问题
    * 默认添加 clearable 属性
    * 更新 xpack 指向
    * 添加 form 组件的 refs
    * 修复 Luna 资产树搜索异常
    * 添加 Cookie 时间

v2.1.0
------------------------
2020年07月17日

!!! info "新增功能"
    * 添加Token匿名链接功能

!!! summary "功能优化"
    * 修改celery队列数量: 2 -> 4
    * 登录密码加密传输
    * 用户组中添加用户，取消审计员的限制
    * 组织管理员创建用户时，角色只能选择: 用户
    * 修改网域唯一字段为(org_id, name)
    * 系统用户添加过滤字段
    * 批量命令执行配置添加默认值True
    * 会话搜索添加登录来源选项
    * 修改ftp日志记录按开始日期排序
    * 限制上传CSV文件的大小10M
    * 组织管理ViewSet添加搜索字段【企业版】
    * 删除组织失败时返回对应错误信息【企业版】
    * 云管中心，同步历史列表、同步实例列表API添加filter_fields: status字段【企业版】
    * 创建同步实例唯一性约束报错【企业版】
    * 修改改密任务执行锁机制，解决相同任务请求锁时，由于等待堵塞任务队列的问题【企业版】

!!! success "修复Bug"
    * 修复radius认证失败问题
    * 修复系统用户测试可连接性失败问题
    * 修复管理用户单独测试某台资产可连接性失败的情况
    * 修复节点、资产关系发生变化时，关联系统用户引起的问题（重复添加）
    * 修复用户name字段长度与资产created_by字段长度不一致导致创建资产失败的问题
    * 修改创建AuthBook对象锁机制，使用select_for_update替换redis_lock
    * 命令过滤器唯一应该为(name, org_id)
    * 修复命令记录没有根据sesion进行过滤的问题
    * 操作日志中的动作搜索条件，删除文件字段改成删除
    * 修复创建资源时，created_by字段长度限制导致创建失败的问题
    * 构建资产id时，返回UUID类型
    * 修复收集资产用户日志中用户名显示不完整的问题
    * platform json data unmarshal error
    * default utf8 charset option
    * 统一时间格式
    * 更新Xpack代码，用户界面资产添加备注选项
    * 创建资产网域选项可清空
    * 优化ldap用户列表勾选后关闭页面，再次打开时，上一次选中的状态还存在的问题
    * 修复命令详情参数及在线会话快捷操作组件
    * 修复登录密码后没有立即提示退出登录等问题
    * 添加changePassword创建页面中的翻译
    * 去掉删除资产的前端提示，改为由后端提示
    * 修复LDAP一键导入不选择用户，导入了全部用户的问题
    * 修复创建资源后跳转到列表页，左侧菜单没有高亮问题
    * 优化安全设置的一些字段提醒
    * 修改有些列表页面的时间在firefox上显示不出来的问题
    * 添加禁止更新和禁止删除的权限判断
    * 修改弹窗按钮高亮提示
    * 用户来源不为Local的时候禁止更新密码
    * 修复创建远程应用页面系统用户的获取
    * 修改Dockerfile，统一使用build.sh构建
    * 修复安全设置页面更新不了的问题
    * 更新Master Xpack代码
    * 更新Xpack代码
    * 修复创建远程应用页面系统用户的获取
    * 优化资产树 mini-button 添加 cursor:pointer
    * lina dev中xpack的commit号指向xpack master
    * 修复时间显示兼容firefox

2.0.2
------------------------
2020年07月09日

!!! info "新增功能"
    * 添加平台编码选项
    * 修改 release，支持交叉编译
    * 添加workflow，自动构建发布
    * 构建CI相关的actions
    * 修改生成的release手动指定tag
    * assets/gathered_user 添加过滤字段
    * System user 添加新过滤项：协议
    * 修改 github issue 模板

!!! summary "功能优化"
    * 优化表格组件
    * 优化导入、导出提示信息，以及优化一些表格显示不友好问题

!!! success "修复Bug"
    * 优化命令存储创建页面，主机字段提示信息的翻译问题
    * 修改关系卡片的bug
    * 修改资产详情网域字段显示，以及去掉一些多余的东西
    * 修复时间兼容firefox
    * 修复资产列表批量操作提交报错的问题
    * 修改翻译
    * 修复系统用户添加空资产成功的问题
    * 修复用户界面可以创建节点的问题
    * 修复已知Issues
    * 统一详情中左右侧布局组件
    * 修复终端详情获取异常的问题
    * 修复批量删除链接的bug
    * 优化表格宽度，优化资产树显示的位置大小可等比例缩放
    * 优化Ldap认证设置
    * 优化lina一些细节问题
    * 修复登录鉴权提示
    * 修复资产 Dialog Title显示错误问题
    * 修复资产页面Bug,更新Xpack依赖
    * 修复资产和前端bugs
    * 修改 ftp 日志按开始日期排序
    * 修改一些翻译
    * 修改csv导出，最大限制条目数从100->10000条
    * 升级guacamole server到1.2.0版本，修复Guacamole之前版本存在的漏洞CVE-2020-9497和CVE-2020-9498。
    * 本次guacamole紧急升级，和 API Koko Luna Lina 2.x 版本兼容，API koko lina luna 后续发布

2.0.1
------------------------
2020年06月22日

!!! summary "功能优化"
    * 优化路由
    * 优化权限验证

!!! success "修复Bug"
    * 修复MFA绑定漏洞
    * 修复批量改密Bug【企业版】
    * 修复安装过程中的bug

2.0.0
------------------------
2020年06月18日

!!! tip "v2.0 版本"
    * 使用Vue重构前端工程 (Lina)，实现前后端分离
    * 优化、添加部分 API
    * 优化、删除大部分 View 及 Template 模块
    * 重构 Web 前端

!!! summary "优化功能"
    * 优化API请求
    * 支持使用授权token连接资产

!!! success "修复Bug"
    * 修复分页造成的进程退出

1.5.9
------------------------
2020年05月21日

!!! tip
    - [新版 OpenID Connect 认证配置文档](../../admin-guide/authentication/openid/)

!!! note "新增功能"
    * 支持标准 OpenID Connect

!!! summary "优化功能"
    * 优化仪表盘加载速度
    * 优化资产查询速度
    * 更新云管中心中各云服务提供商支持的地域列表（比如：阿里云-西南1）【XPack】
    * 优化连接日志信息
    * 调整TreeAPI请求地址
    * 添加支持直接连接数据库应用

!!! success "修复Bug"
    * 修复MFA二次认证的异常问题
    * 修复API Key不能删除的问题
    * 修复多组织下仪表盘数据显示不准确问题
    * 修复FTP日志没有按照组织进行存放的问题
    * 修复用户授权资产树及列表数据显示不稳定问题
    * 修复用户页面更新MFA时解除管理员强制启用的问题
    * 修复任务列表执行历史中统计数据显示不准确的问题
    * 修复资产授权用户/用户组页面删除用户组失败的问题
    * 修复右击资产树点击仅显示当前节点下资产不生效的问题
    * 修复授权模块的信号处理器由于不能正常监控而导致的系统用户不能自动推送到资产以及没有关联资产的问题
    * 修复连接资产无反应问题

!!! info "升级依赖"
    * jumpserver-django-oidc-rp==0.3.7.4

1.5.8
------------------------
2020年04月16日

!!! note "新增功能"
    * 在线会话监控（备注：目前仅支持协议类型为ssh、telnet、mysql的在线会话）
    * 批量改密（支持修改root、administrator等特殊用户）【XPack】
    * 创建云管中心同步实例任务时，可选择是否覆盖同步的资产信息【XPack】
    * 新增在线会话监控【koko】

!!! summary "优化功能"
    * 创建录像存储时自动清除空白字符
    * 修改中间件中获取当前组织的优先级
    * 更新播放器下载地址链接
    * 优化创建AuthBook逻辑（添加互斥锁机制）
    * 修改组织获取优先级
    * 禁用ansible的ssh连接复用
    * 修改项目使用的cache default(redis_cache -> redis_lock)
    * 更新用户时显示CAS用户来源选项

!!! success "修复Bug"
    * 修复列表中日期显示问题
    * 修复资产用户列表删除失败的问题
    * 修复命令记录导出问题（导出满足搜索条件的命令记录）
    * 修复因数据不支持timezone引起的仪表盘数据为空的问题
    * 修复自定义平台列表在详情页删除失败的问题
    * 修复命令记录/操作/改密日志搜索字段没清空的问题
    * 修复系统设置-终端设置-资产排序设置不生效的问题
    * 修复点击测试邮件后，配置信息获取不稳定的问题
    * 修复使用容器时，Azure录像上传问题（ 镜像添加ca-certificates依赖 ）【koko】

!!! info "更新依赖"
    * python-redis-lock==3.5.0
    * jms-storage-sdk==0.0.29

1.5.7
------------------------
2020年3月19日

!!! note "新增功能"
    * 支持 CAS Server （中央认证服务）用户登录认证
    * 提出动态系统用户的概念，当用户登录资产时自动使用与其 JumpServer用户名相同的系统用户连接资产
    * 自定义配置文件上传路径，允许管理员为不同系统用户指定不同的SFTP挂载目录，目前仅支持Linux资产
    * 支持下载会话录像，可配合JumpServer Video Player 进行离线播放，并附带录像的操作信息，JumpServer Video Player 适配 Mac 、Windows 和 Linux
    * 云管中心支持同步华为云实例；对云上已释放实例进行本地标记 【XPack】
    * 批量改密针对特殊用户（如root、administrator等）开放改密操作【XPack】
    * 支持动态的系统用户名
    * 增加命令记录风险标记
    * 增加用户 SSH 连接心跳设置，默认30s
    * 隔离 MySql 连接的进程空间

!!! summary "优化功能"
    * 优化Dashboard页面加载速度
    * 优化MFA登录页面
    * 优化资产授权规则，当用户、用户组、资产、节点、系统用户等变更时，实时刷新与其他实体之间的关联关系
    * 优化资产用户列表展示和API性能优化
    * 优化LDAP/AD配置模块的测试可连接性逻辑，并添加测试用户登录的功能
    * 优化可连接性测试逻辑
    * 优化部分API（包括资产、系统用户、管理用户等相关API）处理逻辑
    * 优化改密计划执行流程【XPack】
    * 增强 SSH Client 复用连接，免受 SSH MaxSessions 限制
    * 增强 Websocket 连接处理能力
    * 增强 Web 文件管理功能，支持软连接目录，增加错误信息提示
    * 增强 SFTP 功能，根目录可依据系统用户动态配置
    * 增强 Telnet Client 连接
    * 录像存储配置动态更新

!!! success "修复Bug"
    * 修复无法删除空节点的问题
    * 修复命令记录、批量命令没有针对组织进行分组显示的问题
    * 修复存在无效 ES 存储时访问命令记录页面失效的问题
    * 修复会对第三方认证用户发送创建用户成功邮件、密码过期提醒邮件的问题
    * 修复部分pip依赖包版本不兼容的问题
    * 修复 Telnet 资产网关连接未关闭问题
    * 修复主进程假死问题
    * 修复首次启动获取录像存储类型为 Null 的问题

1.5.6
------------------------
2020年1月2日

!!! info "漏洞修复"
    * 修复用户被强制开启使用 MFA 二次认证后可以自主绕过绑定的问题

!!! note "新增功能"
    * 全面支持 IPv6
    * 数据库应用【商业版】
    * Windows 批量命令
    * 录像存储类型：Swift、Ceph
    * 节点详情（右击节点显示）
    * 资产平台列表

!!! summary "优化功能"
    * 录像/命令存储配置迁移到 Terminal 模块
    * 优化用户详情页面
    * 用户列表添加移除操作（非DEFAULT组织）【商业版】
    * 用户第三方认证后，只在创建时修改用户来源信息
    * 优化前端 Form 渲染逻辑（存储配置、RemoteApp、DatabaseApp）
    * 统一导入导出组件
    * 统一了树列表基础模板
    * 优化日志审计（操作日志，改密日志）
    * API 采用 serializer_classes 字段（default, display）
    * 统一系统配置的 Tab 切换
    * 统一没有nav的页面（重置密码，忘记密码，重置中设置密码，独立 message 页面）
    * 优化用户组列表页（不返回组中用户，只返回数量）
    * 组织的一些方法变为layzproperty，避免重复计算
    * 用户组增加删除用户（用户组详情页）
    * 优化Ops Task表结构，减少数据库查询次数
    * 优化基础的 Encryptjsonfield
    * 修改 Adhoc 返回的 become 字段，避免密码泄露
    * 修改校验用户资产权限API不使用缓存
    * 用户登录日志，采用同步机制
    * 右击节点菜单位置计算
    * 命令存储（ES）相关字段设置为 required
    * 操作日志文案，用户修改为操作者
    * 调整 Web 文件管理为节点树结构
    * 支持 Web 文件管理的资产搜索
    * 增加 SSH 连接的加密算法以支持旧设备

!!! success "修复Bug"
    * 检验用户有效性逻辑（解决启用LDAP等认证时，显示用户名不存在）
    * 工单按用户搜索无效的问题
    * 密码匣子选择 id 导出时的问题
    * 解决密码匣子翻页再次选择资产时不能设置到选择框的问题
    * 解决管理员重置用户MFA后，自动退出的问题
    * 修复无法使用中文搜索资产
    * 修复因自定义正则造成的程序异常
    * 修复因S3配置造成的程序异常
    * 优化部分代码

!!! info "更新依赖"
    * psutil==5.6.5
    * go-elasticsearch v6.8.5

1.5.5
------------------------
2019年12月4日

!!! note "新增功能"
    * 工单管理【商业版】
    * 二次复合（用户登录）【商业版】
    * 二次认证（MFA Radius）
    * 重启后支持自动上传遗留录像
    * 支持 Windows 连接超时断开

!!! summary "优化功能"
    * LDAP/AD 逻辑
    * 可修改用户来源（用户创建）
    * 收集资产用户（显示用户最后登录时间）
    * 左侧组织增加搜索过滤
    * 可关闭页面提示信息
    * 资产用户列表支持模糊搜索
    * 跳过手动输入密码配置（Windows）
    * 优化授权资产分页展示
    * 支持授权资产的多级搜索
    * 支持用户登录的二次审核

!!! success "修复Bug"
    * 修复用户授权资产问题（用户组/用户授权变更刷新问题）
    * 修复因版本不一致造成的异常
    * 修复部分 telnet 登录问题

1.5.4
------------------------
2019年10月23日

!!! note "新增功能"
    * 用户收藏资产（用户页面 -> 我的资产）
    * LDAP 登录认证添加配置项：只有在用户列表中的用户会被允许认证（配置项可在 config_example.yml 中查找 AUTH_LDAP_USER_LOGIN_ONLY_IN_USERS）

!!! summary "优化功能"
    * 优化 LDAP 用户导入/搜索的逻辑（采用用户过滤器方式）
    * 优化命令列表中命令的显示（解决命令太长的问题）
    * 优化 select2 js/css 依赖版本(4.0.10)（解决多选下拉框自动回跳到顶部的问题）
    * 优化 celery log 显示（采用 Websocket 方式）
    * 优化节点删除 API，返回删除失败原因（包含子节点或资产）
    * 限制系统用户 name 字段使用特殊字符
    * 添加脚本：get_no_parent_nodes.py
    * 更新创建/更新用户组的取消按钮->重置按钮（避免引起歧义）
    * 优化所有 API 的 get_queryset 方式
    * 修改获取系统用户 API 为只返回节点数量（之前是返回节点列表）
    * 修改 session 支持 protocol 搜索
    * 修改 form serializer 对应的多对多字段
    * 修改命令批量执行左侧选择系统用户
    * 修改查看资产用户 Auth info 可配置关闭 MFA 校验
    * 优化创建用户邮件内容
    * 优化用户组详情页面选择用户下拉列表使用异步加载
    * 优化命令过滤详情绑定到系统用户点击下拉框自动关闭的问题
    * 优化提交 api 报错时滚动到错误提示行
    * 优化 table 页面某些列宽度
    * 修改 jms 启动脚本，stop 时增加超时检测
    * 修改导出登录日志的日期选择从开始日期的00:00:00，到结束日期的23:59:59
    * 修改返回资产树包含组织信息
    * 限制组织名称中使用的特殊字符【X-pack 企业版】

!!! success "修复Bug"
    * 修复调用系统用户资产 API 时 Connectivity is not JSON serializable 的 Bug
    * 修复命令记录从 es 中获取失败（原因：时间日期格式不匹配）
    * 修改终端命令类型 MAPPING（elasticsearch -> es）
    * 修复资产授权列表搜索 invalid:false 时出现 500 错误
    * 修复导出资产 csv 文件为空的问题
    * 修复导致 favorite 和 empty 同时出现的问题
    * 修复读取日志时可能解码失败的问题
    * 修复组织管理员在资产详情页面不显示（删除/更新）按钮的问题【X-pack 企业版】
    * 修复组织管理员查看用户权限失败问题【X-pack 企业版】

!!! info "更新依赖"
    * select2 升级版本 4.0.10（解决多选下拉框选择跳到顶部的问题）

1.5.3
------------------------
2019年9月24日

!!! info "组件说明"
    * 自 v1.5.3 版本起（包含 v1.5.3），Koko 将担任 Coco 在 JumpServer 项目中的重要角色，之后的版本将不会再对 Coco 进行升级维护。

!!! note "新增功能"
    * 添加页面创建 API Key 的功能（右上角点击账号下拉列表 -> API Key）
    * 在线会话列表中允许终断 RDP Session
    * 添加用户树缓存

!!! summary "优化功能"
    * 优化资产树加载逻辑
    * 优化资产授权树、授权规则加载、过滤逻辑
    * 优化前端 asset modal table
    * 统一 URL 地址
    * 修改 Swagger
    * 允许批量删除用户，修改前端提示信息逻辑
    * 推送系统用户时，在资产上创建同名的用户组
    * 资产协议修改：telnet (beta) => telnet
    * WebTerminal 跳转时添加时间戳

!!! success "修复Bug"
    * 修复授权规则列表同一条数据重复显示的问题
    * 修复授权规则列表翻页后重复展示前几页中数据的问题
    * 修复授权详情中授权资产或节点添加资产失败的问题
    * 修复系统设置的配置偶尔不生效的问题
    * 修复命令执行左侧树点击问题
    * 修复用户认证序列类获取 request 的问题
    * 修复批量创建系统用户等资源时，initial_data 获取数据失败的问题
    * 修复创建授权规则授权节点时，系统用户不自动推送的问题
    * 修复浏览器关闭后 Session 不失效的问题
    * 解决授权了一个节点，当移动节点后，被移动的节点下的资产会放到未分组节点下的问题
    * 修复刷新资产硬件信息时无法检测 NVMe 的硬盘的问题
    * 解决命令执行宽度问题

!!! info "更新依赖"
    * 升级 jQuery v3.1.1

1.5.2
------------------------
2019年7月16日

!!! note "新增功能"

    * 系统设置-安全设置中添加配置项：终端注册

!!! summary "优化功能"
    * 获取系统用户授权资产时，只返回资产协议支持的系统用户。
    * 表单使用API进行提交
    * 优化授权规则资产列表页面
    * 在线/历史会话页面去掉协议搜索选项

!!! success "修复Bug"
    * 解决命令过滤器详情添加系统用户失败的问题
    * 解决命令过滤器详情页删除功能不可用的问题
    * 解决可以创建同名命令过滤器的问题（修复资产授权详情页删除弹出框的权限名显示不对)
    * 解决在资产授权详情页删除授权规则时弹出框中名称显示不正确的问题
    * 解决网域详情页删除功能不可用的问题
    * 解决资产列表数量显示不正确的问题
    * 解决创建命令过滤规则类型为正则表达式时创建不成功的问题
    * 解决授权规则详情用户组数量显示不正确的问题
    * 解决日期显示差8小时的问题
    * 解决创建资产失败的问题（原因：协议的添加、删除逻辑）
    * 解决授权页面不显示资产的问题
    * 解决授权资产包含已禁用资产的问题
    * 解决系统用户、管理用户提交会重置密码的问题
    * 解决批量执行命令没有选择资产的问题

1.5.1
------------------------
2019年7月6日

!!! note "新增功能"
    * 审计员（用户添加审计员角色）

!!! summary "优化功能"
    * 用户页面优化资产标签过滤功能
    * 用户创建添加到当前组织（API调用）
    * 资产授权树显示策略（将单独授权的资产添加到自定义的默认节点下）
    * 资产创建支持添加多个协议
    * 资产创建设置节点策略（API/CSV，解决总是会添加到默认节点的问题）
    * 邮件设置添加发送账号选项（解决SMTP账号和发送账号不一致的问题）
    * 安全设置添加批量命令选项（解决禁止普通用户批量执行命令的问题）
    * 终端(coco/guacamole)上报Session/FTP用户信息使用 name（username）格式
    * Windows资产可通过SSH协议连接
    * Windows资产支持直接复制粘贴文本（浏览器授权剪切板权限）
    * 添加一键禁用LDAP认证脚本
    * 解决连接windows资产出现幽灵会话的问题
    * 优化创建授权规则时，授权动作的展示
    * 解决操作日志中出现coco/guamole更新Default节点的问题
    * 优化命令记录列表/在线/历史会话列表（提高响应速度，取消返回所有资产）

!!! success "修复Bug"
    * 修复文件导出使用excel打开乱码的问题
    * 解决用户授权资产/节点为空时，前端构建资产授权树的Bug

1.5.0
------------------------
2019年5月29日

!!! note "新增功能"
    * 支持启用MFA的管理员查看资产用户密码
    * 可自定义创建用户时发送创建用户成功的邮件内容
    * 创建用户时，可选择用户密码设置策略(可解决客户没有邮件系统的场景)
    * (用户/用户组/资产/管理用户/系统用户)资源支持使用csv文件类型进行导入、导出、更新操作
    * LDAP支持SSL (pem路径 jumpserver/data/certs/ldap_ca.pem)
    * 支持Option方法请求API获取对应其他HTTP方法的所需的字段说明
    * 支持RemoteApp

!!! summary "优化功能"
    * 创建资产时允许ip字段填写为host地址
    * OpenID Middleware去掉输出日志
    * 资产节点API添加search功能
    * 解决ldap映射is_active等字段为bool值的问题(可解决LDAP禁用用户后，同时禁止用户登录JumpServer的场景)

!!! success "修复Bug"
    * 修复LDAP不能导入用户名中包含空格的用户
    * 修复LDAP可导入跨页面选取的所有用户
    * 修复资产用户管理器获取用户名为""的对象时返回多个结果的bug

1.4.10
------------------------
2019年4月30日

!!! note "新增功能"
    * 新增权限控制：可分别对连接、上传、下载等动作单独授权；

!!! summary "优化功能"
    * 权限优化：组织管理员不允许对超级管理员进行操作；
    * Luna优化：Luna搜索优化功能；

!!! success "修复Bug"
    * 修复通过API批量更新用户的bug
    * 修复luna页面刷新不跳转OpeID认证的bug
    * 修复创建azure类型的录像存储时前端的bug
    * 修复其他前端页面bug
    * 修复录像上传到Azure的bug

1.4.9
------------------------
2019年3月26日

!!! success "修复Bug"
    * 修复创建定时任务时的时区问题
    * 修复celery日志可能操作关闭文件的bug
    * 修复一些设置缓存的问题
    * 修复用户token过期的时间策略
    * 修复第一次登录跳转组织页面的bug

!!! summary "优化功能"
    * sudo命令添加帮助说明，并兼容换行形式
    * 认证逻辑，从users模块中移动到authentication
    * 合并一些migrations
    * 任务列表去掉日期
    * docker build升级Mysql client版本
    * coco,guacamole上传完录像上报api，页面上如果没有录像则播放按钮是禁用的
    * 定时清理登陆日志
    * 用户授权增加两层缓存，授权资产数量很大时也不怕了
    * 资产模块添加资产用户管理器，可以为资产单独设置 管理用户、系统用户的密码
    * 登陆日志的导出
    * 数据库支持ssl
    * ldap用户一键导入
    * 使用网关同样添加心跳信息
    * 用户授权资产列表增加缓存
    * 修复一些sftp的小bug
    * 修复上传命令记录decode的错误
    * 支持系统用户在不同机器上密码不一致的场景
    * 支持左侧列表缓存

1.4.8
------------------------
2019年2月22日

!!! tip ""
    * 修复command filter 不记录操作日志的问题
    * LDAP支持无密码
    * 录像上传设置中去掉了ceph，s3兼容cepht
    * gunicorn日志切割
    * telnet支持在设置中修改成功的正则表达式
    * 修复session 10分钟后不在线的问题

1.4.7
------------------------
2019年1月29日

!!! tip ""
    * 支持 radius认证
    * 统一生成coco的host key，这样部署多个coco也不需要再复制 Host key
    * 权限列表增加详细过滤
    * 更改配置文件类型为 yml格式
    * 修改心跳方式
    * 优化任务执行的日志记录方式
    * 修复节点右击测试连接资产为节点下所有资产，而不是直接资产
    * sftp支持修改home目录，支持不显示隐藏文件
    * 修复luna隐藏侧边栏的bug
    * luna支持直接登录到某个资产

1.4.6
------------------------
2018年12月19日

!!! tip ""
    * 推送资产上已存在的系统用户会覆盖该用户的home目录权限
    * 会话日志可以定时清理，保证硬盘够用
    * coco里 p可以自定义是否分页了
    * 优化树形结构，不怕资产太多了
    * 其他bug

1.4.5
------------------------
2018年12月12日

!!! tip ""
    * 统一维护migrations数据库表结构变更
    * 系统配置内容支持热加载，不用再重启 jumpserver
    * coco，guacamole注册机制更改，使用预共享秘钥自动注册，不再需要接受注册
    * 用户密码过期时间设置
    * ldap不可以修改密码
    * 默认组织里可以看到所有用户
    * 日志审计修改密码日志中只能看到当前组织用户的更改
    * luna列表回滚为原来方式，不再是异步加载
    * rdp支持分辨率更改

1.4.4
------------------------
2018年11月11日

!!! tip ""
    * 录像存储设置，使用表单来填写
    * 支持luna异步加载
    * 各列表统一使用分页
    * 授权时间精确到分钟
    * 支持openid认证

1.4.3
------------------------
2018年10月12日

!!! tip ""
    * 支持命令过滤

1.4.2
------------------------
2018年10月8日

!!! tip ""
    * 支持web sftp，支持跨资产复制粘贴文件
    * 优化一些内容

1.4.1
------------------------
2018年9月4日

!!! tip ""
    * 系统设置支持加密存储
    * 单独推送系统用户到某个资产
    * 支持了用户改密日志和操作日志
    * 翻译更加完善，支持切换语言
    * 不记录zmodem信息
    * 支持空闲间隔自动断开
    * 修复session无法中断问题
    * 增加ssh用户黑名单和白名单
    * luna支持搜索支持IP
    * 优化一些内容

1.4.0
------------------------
2018年8月7日

!!! tip ""
    * 超级管理员创建组织，为改组织添加管理员，管理员可以负责该组织下 用户、资产、授权等管理
    * Sftp显示同名资产为 主机名.组织
    * Luna支持根据IP搜索
    * 鼠标悬停可以显示主机ip
    * 其他修复Bug等

1.3.3
------------------------
2018年7月17日

!!! tip ""
    * 支持telnet协议
    * 支持用户手动输入密码登陆，密码不用托管到JumpServer
    * 登陆日志增加失败原因
    * session增加登陆源
    * 修复网关端口和密码bug
    * 添加用户登陆失败次数限制

1.3.2
------------------------
2018年6月11日

!!! tip ""
    * 可以在系统设置中指定密码强度，包含大小写字母特殊字符长度等
    * 可以全局开启MFA
    * 修改EMAIL不需要重启
    * 设置公钥交互改变
    * 修改一些BUG
    * 修改窗口大小策略
    * 统一requirements版本
    * 修改luna树形结构，从根开始展示
    * 修改luna树形搜索
    * 修改初始窗口大小不对的bug
    * 修改录像播放的部分bug

1.3.1
------------------------
2018年5月24日

!!! tip ""
    * 用户授权节点逻辑更改
    * 去掉window无用信息
    * 修复节点创建bug
    * 创建节点 从0开始，新节点0 新节点1
    * 修复拖动节点引起的父节点异常
    * 资产树增加视图，只显示本节点资产和显示子节点资产

1.3.0
------------------------
2018年5月2日

!!! tip ""
    * 支持二次认证(Google Authenticator)
    * 修复一些bug
    * 优化第一次登录页面

1.2.0
------------------------
2018年4月13日

!!! tip ""
    * sftp上传文件支持
    * 支持sftp日志审计

1.1.1
------------------------
2018年4月6日

!!! tip ""
    * 加强任务执行
    * 支持查看各个任务的详细执行日志
    * 支持实时查看任务执行输出

1.1.0
------------------------
2018年4月3日

!!! tip ""
    * 支持混合云多网络环境
    * 网域概念加入
    * 网关概念加入
    * rdp gateway概念加入
    * 修复一些bug

1.0.0
------------------------
2018年3月15日

!!! tip ""
    * Windows支持
    * 容器化部署
    * 资产树
    * 录像/命令存储支持OSS/S3和ES
    * 分布式部署
    * 系统用户自动推送
    * 标签管理
    * 命令统计增加输出展示
    * Web Terminal改进
    * 系统设置
    * LDAP支持
