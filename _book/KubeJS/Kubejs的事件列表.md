# 2、KubeJS的事件列表

#### 一、事件列表

| 脚本类型        | 方法                                            | 描述                               | 是否可取消 |
| --------------- | ----------------------------------------------- | ---------------------------------- | ---------- |
| startup_scripts | `StartupEvents.init`                            | -                                  | ❌          |
| startup_scripts | `StartupEvents.postInit`                        | -                                  | ❌          |
| startup_scripts | `StartupEvents.registry`                        | 注册游戏内容(用于添加物品，附魔等) | ❌          |
| client_scripts  | `ClientEvents.highPriorityAssets`               | -                                  | ❌          |
| client_scripts  | `ClientEvents.init`                             | -                                  | ❌          |
| client_scripts  | `ClientEvents.loggedIn`                         | 登入世界                           | ❌          |
| client_scripts  | `ClientEvents.loggedOut`                        | 登出世界                           | ❌          |
| client_scripts  | `ClientEvents.tick`                             | 客户端Tick事件                     | ❌          |
| client_scripts  | `ClientEvents.painterUpdated`                   | Painter API                        | ❌          |
| client_scripts  | `ClientEvents.leftDebugInfo`                    | F3界面左侧信息                     | ❌          |
| client_scripts  | `ClientEvents.rightDebugInfo`                   | F3界面右侧信息                     | ❌          |
| client_scripts  | `ClientEvents.paintScreen`                      | 绘制Screen                         | ❌          |
| server_scripts  | `ServerEvents.lowPriorityData`                  | 数据包事件 - 低优先度              | ❌          |
| server_scripts  | `ServerEvents.highPriorityData`                 | 数据包事件 - 高优先度              | ❌          |
| server_scripts  | `SeverEvents.loaded`                            | 服务端加载                         | ❌          |
| server_scripts  | `ServerEvents.unloaded`                         | 服务端卸载                         | ❌          |
| server_scripts  | `ServerEvents.tick`                             | 服务端Tick事件                     | ❌          |
| server_scripts  | `ServerEvents.tags`                             | 标签添加或修改                     | ❌          |
| server_scripts  | `ServerEvents.commandRegistry`                  | 命令注册事件                       | ❌          |
| server_scripts  | `ServerEvents.command`                          | 命令执行事件                       | ✔          |
| server_scripts  | `ServerEvents.customCommand`                    | 自定义命令事件                     | ✔          |
| server_scripts  | `ServerEvents.recipes`                          | 配方添加或修改                     | ❌          |
| server_scripts  | `ServerEvents.afterRecipes`                     | 配方加载完成后事件                 | ❌          |
| server_scripts  | `ServerEvents.specialRecipeSerializers`         | 配方序列化相关事件                 | ❌          |
| server_scripts  | `ServerEvents.compostableRecipes`               | 堆肥配方添加或修改                 | ❌          |
| server_scripts  | `ServerEvents.recipeTypeRegistry`               | 配方类型注册                       | ❌          |
| server_scripts  | `ServerEvents.genericLootTable`等，详见后续章节 | LootTable相关事件                  | ❌          |
| server_scripts  | `LevelEvents.loaded`                            | 世界加载事件                       | ❌          |
| server_scripts  | `LevelEvents.unloaded`                          | 世界卸载事件                       | ❌          |
| server_scripts  | `LevelEvents.tick`                              | 世界Tick事件                       | ❌          |
| server_scripts  | `LevelEvents.beforeExplosion`                   | 爆炸发生前事件                     | ✔          |
| server_scripts  | `LevelEvents.afterExplosion`                    | 爆炸发生后事件                     | ❌          |
| server_scripts  | `WorldgenEvents.add`                            | 添加世界生成（如矿石等）           | ❌          |
| server_scripts  | `WorldgenEvents.remove`                         | 移除世界生成（如矿石等）           | ❌          |
| server_scripts  | `NetworkEvents.fromServer`                      | 客户端接收服务端网络包             | ✔          |
| server_scripts  | `NetworkEvents.fromClient`                      | 服务端接收客户端网络包             | ✔          |
| server_scripts  | `ItemEvents.modification`                       | 游戏内容修改(用于修改物品)         | ❌          |
| server_scripts  | `ItemEvents.toolTierRegistry`                   | 工具等级注册                       | ❌          |
| server_scripts  | `ItemEvents.armorTierRegistry`                  | 护甲等级注册                       | ❌          |
| server_scripts  | `ItemEvents.pickedUp`                           | 捡起物品事件                       | ❌          |
| server_scripts  | `ItemEvents.dropped`                            | 丢弃物品事件                       | ❌          |
| server_scripts  | `ItemEvents.entityInteracted`                   | 物品与实体交互事件                 | ❌          |
| server_scripts  | `ItemEvents.crafted`                            | 物品合成事件                       | ❌          |
| server_scripts  | `ItemEvents.smelted`                            | 物品烧炼事件                       | ❌          |
| server_scripts  | `ItemEvents.foodEaten`                          | 食用食物类物品事件                 | ❌          |
| client_scripts  | `ItemEvents.clientLeftClicked`                  | 左键单击事件(客户端侧)             | ❌          |
| server_scripts  | `ItemEvents.firstLeftClicked`                   | 左键单击事件(服务端侧)             | ❌          |
| client_scripts  | `ItemEvents.clientLeftClicked`                  | 右键单击事件(客户端侧)             | ❌          |
| server_scripts  | `ItemEvents.firstRightClicked`                  | 右键单击事件(服务端侧)             | ❌          |
| server_scripts  | `ItemEvents.tooltip`                            | 物品悬浮提示修改                   | ❌          |
| server_scripts  | `ItemEvents.modelProperties`                    | 物品模型修改                       | ❌          |
| server_scripts  | `BlockEvents.modification`                      | 游戏内容修改(用于修改方块)         | ❌          |
| server_scripts  | `BlockEvents.rightClicked`                      | 方块右键单击事件                   | ❌          |
| server_scripts  | `BlockEvents.leftClicked`                       | 方块左键单击事件                   | ❌          |
| server_scripts  | `BlockEvents.placed`                            | 方块放置事件                       | ❌          |
| server_scripts  | `BlockEvents.broken`                            | 方块被破坏事件                     | ❌          |
| server_scripts  | `BlockEvents.detectorChanged`                   | 检测方块状态改变事件               | ❌          |
| server_scripts  | `BlockEvents.detectorPowered`                   | 检测方块被红石充能事件             | ❌          |
| server_scripts  | `BlockEvents.detectorUnpowered`                 | 检测方块红石充能结束事件           | ❌          |
| server_scripts  | `EntityEvents.death`                            | 实体死亡事件                       | ❌          |
| server_scripts  | `EntityEvents.hurt`                             | 实体受伤事件                       | ❌          |
| server_scripts  | `EntityEvents.checkSpawn`                       | 实体检查生成位置事件               | ❌          |
| server_scripts  | `EntityEvents.spawned`                          | 实体生成事件                       | ❌          |
| server_scripts  | `PlayerEvents.loggedIn`                         | 玩家登入事件                       | ❌          |
| server_scripts  | `PlayerEvents.loggedOut`                        | 玩家登出事件                       | ❌          |
| server_scripts  | `PlayerEvents.cloned`                           | 玩家克隆事件                       | ❌          |
| server_scripts  | `PlayerEvents.tick`                             | 玩家Tick事件                       | ❌          |
| server_scripts  | `PlayerEvents.chat`                             | 玩家聊天事件                       | ❌          |
| server_scripts  | `PlayerEvents.decorateChat`                     | -                                  | ❌          |
| server_scripts  | `PlayerEvents.advancement`                      | 玩家成就事件                       | ✔          |
| server_scripts  | `PlayerEvents.inventoryOpened`                  | 玩家打开背包事件                   | ❌          |
| server_scripts  | `PlayerEvents.inventoryClosed`                  | 玩家关闭背包事件                   | ❌          |
| server_scripts  | `PlayerEvents.inventoryChanged`                 | 玩家背包物品变更事件               | ❌          |
| server_scripts  | `PlayerEvents.chestOpened`                      | 玩家打开箱子事件                   | ❌          |
| server_scripts  | `PlayerEvents.chestClosed`                      | 玩家关闭箱子事件                   | ❌          |

#### 二、常用模组事件

**JEI：**

| 脚本类型       | 方法                         | 描述           | 是否可被取消 |
| -------------- | ---------------------------- | -------------- | ------------ |
| client_scripts | `JEIEvents.subtypes`         | 子类型         | ❌            |
| client_scripts | `JEIEvents.hideItems`        | 隐藏物品       | ❌            |
| client_scripts | `JEIEvents.hideFluids`       | 隐藏流体       | ❌            |
| client_scripts | `JEIEvents.hideCustom`       | 隐藏自定义类型 | ❌            |
| client_scripts | `JEIEvents.removeCategories` | 移除类型       | ❌            |
| client_scripts | `JEIEvents.removeRecipes`    | 移除配方       | ❌            |
| client_scripts | `JEIEvents.addItems`         | 添加物品       | ❌            |
| client_scripts | `JEIEvents.addFluids`        | 添加流体       | ❌            |
| client_scripts | `JEIEvents.information`      | -              | ❌            |

**REI：**

| 脚本类型       | 方法                         | 描述     | 是否可被取消 |
| -------------- | ---------------------------- | -------- | ------------ |
| client_scripts | `REIEvents.hide`             | 隐藏类型 | No           |
| client_scripts | `REIEvents.add`              | 添加类型 | No           |
| client_scripts | `REIEvents.information`      | -        | No           |
| client_scripts | `REIEvents.removeCategories` | 移除类别 | No           |
| client_scripts | `REIEvents.groupEntries`     | 注册表   | No           |

**GameStages：**

| 脚本类型       | 方法                           | 描述     | 是否可被取消 |
| -------------- | ------------------------------ | -------- | ------------ |
| server_scripts | `GameStageEvents.stageAdded`   | 添加阶段 | No           |
| server_scripts | `GameStageEvents.stageRemoved` | 移除阶段 | No           |