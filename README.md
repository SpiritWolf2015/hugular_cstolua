# hugular_cstolua

此项目暂停维护 请迁移到 https://github.com/tenvick/hugula
======
Hugula 游戏框架 for cstolua
======
Hugula是一个基于unity3d+cstolua技术的全LUA免费开源游戏框架，适用于中大型游戏开发，已经开发过两款卡牌带arpg战斗游戏。
特点 全lua逻辑，基于状态模式，只需关心状态，无需关心UI隐藏和显示。
下载完成后切换到android平台。
qq群：19324776。
 
本框架需要以下条件
======
1)unity3d 版本为 5.0以上 （5.1以上需要自行清理lua wrap file，后重新make）

2)cstolua项目 地址 https://github.com/topameng/CsToLua

3)如需使用tools辅助功能 需要配置python2.7 lua5.1环境

4)友情支持 https://github.com/jarjin/SimpleFramework_UGUI

5)兄弟项目 https://github.com/tenvick/hugula

框架目录
======
Assets

-Config               （存放xxx.csv 配置文件 使用菜单 Hugula/export config [Assets\Config]导出）

-CustomerResource     （存放美术资源）

-Hugula               （核心代码）

-Lan                  （多国语言包 csv   使用菜单 Hugula/export language [Assets\Lan]导出 lua中可直接调用）

-Scene                （场景）

-uLua                 （ulua插件）

-Source               (cstolua插件)

-Tmp                  （编译lua文件临时存放目录）

-Lua                  （lua脚本）


运行发布
======
1 导出assetbundle资源 菜单 AssetBundles/Build AssetBundles

2 导出其他

 2.1 Hugula/export lua [Assets\Lua]          打包编译脚本 

 2.2 Hugula/export config [Assets\Config]    打包配置
 
 2.3 Hugula/export language [Assets\Lan]     打包语言包 

3 cstolua build
 3.1 Lua/Lua/Clear LuaBinder File --清理绑定
 
 3.2 Lua/Gen Lua Wrap Files     --创建warp文件 （BindLua.cs   LuaBinding.binds 下面的类，如是自定义类需要手动添加到这里）
 
 3.3 Lua/Gen u3d Wrap Files     --创建unityEngine 空间下的warp文件 可以不执行这步
 
 3.4 Lua/Gen LuaBinder File     --绑定warp文件
 

如果生成的warp还有错误需要自行处理注释错误。

俄罗斯方块小游戏
======
基于UGUI 
展示lua components的用法
是一种非典型的方式

apk下载地址：http://pan.baidu.com/s/1pJOk13l
