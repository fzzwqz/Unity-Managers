# Unity Managers

收集整理 Unity 项目中常用的各种管理类，方便复用和参考。

##  包含内容

| 管理类      | 说明                                                      |
| ----------- | --------------------------------------------------------- |
| JsonManager | Json 数据管理，支持 LitJson 与 JsonUtility 两种序列化方案 |

> 后续会陆续添加音频、场景、事件等管理类。

## 使用方式

1. 将需要的管理类脚本（如 `JsonManager.cs`）复制到你的 Unity 项目 `Assets` 目录下。
2. 确保项目已导入对应的依赖库（如 LitJson）。
3. 通过单例调用：

```csharp
// 保存数据
JsonManager.Instance.SaveData(playerData, "player");

// 读取数据
PlayerData data = JsonManager.Instance.LoadData<PlayerData>("player");