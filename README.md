# Demo

## 目前状态
更新时间：2022/07/27 11点30分  
包含双手剑主角的基础位移动画，攻击动画

Developed with Unreal Engine 4.27.2

## 已有操作信息
### 双手剑主角
--W:前移  S:后移  A:左移  D:右移  
--鼠标左键【普通攻击】：左A1，左A2，左A3，左A4  
--鼠标右键【特殊攻击（理想目标：能击飞小怪）】：可在左A1、左A2、左A3后施放；目前也可以在特殊攻击后继续施放特殊攻击  
--按住方向键后点按Shift：朝方向键指定方向闪避  

**※ 关于闪避机制的说明：  
①闪避在移动、攻击招式的后半段可以释放，并会刷新普攻段数；  
②闪避无法在招式动作开始时、闪避过程中、空中释放；  
③闪避后角色面朝闪避后方向**  

## 内容说明
### 一. Config 文件夹
--内部配置了基本操作映射，后续如果有更改的话可以覆盖push。  
### 二. Content 文件夹
#### 1. ParagonWraith 文件夹
--主要包含了主角用到的材质、纹理。
#### 2. 主角 文件夹
--含主角的角色蓝图*最终主角_BP*与动画蓝图*最终主角_AnimBlueprint*，以及游戏模式*BaseDemo_GameMode*。  
--**Character** 主要包含双手剑主角的骨骼。  
--**Maps** 含测试地图。  
--**双手剑** 里是双手剑静态网格体模型。  
--**双手剑动画** 里有三个文件夹，Battle放战斗姿态动作，Common放基础姿态动作（暂未添加），Hit放受击动作（暂未添加）。  

**Boss的一些注意事项：**
 1.使用arg插件：在虚幻商城下载，需要在项目中启用（不然会报错）    在编辑->插件 里需要启用
 2.测试用的关卡在BOSS/1    测试用的玩家 按E攻击 ， 别跑过于远超出导航网格
3.触发boss的蓝图写在关卡蓝图里
4.boss打玩家用的arg的插件  玩家如何接受伤害可参考我写的玩家
5.boss/flyBoss/data  里面的cd1和damage可改 cd和伤害
6.玩家打boss的自定义事件在boss_BP里 我将伤害提升成 伤害 变量（默认为10） ，看着用吧 
7.目前受击只有写一个动画

