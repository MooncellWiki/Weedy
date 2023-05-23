# Weedy

Weedy**将**是一个~~基于Mirai~~视情况选择框架的开源的明日方舟QQ机器人，是Weedy Project的一部分。  
该项目包括：  

- Weedy
- Weedy Server (提供接口以获取来自游戏服务器的数据)
  - Weedy Friends Server (提供接口以根据请求返回符合条件的，已提交给服务器的好友列表)
- Weedy Secret (为Weedy Server更新数据)

## Weedy Server

开发期测试用接口(由[StarHeartHunt](https://github.com/StarHeartHunt)提供)：<https://weedy.baka.icu>  
以下所有的接口返回均为国服数据，因为仍在开发期间，返回格式可能出现变动，所以暂不提供具体的响应体结构。

### 卡池

#### 卡池内容

```
GET /gacha/{poolId}
```

返回指定卡池（由poolId指定）的可出现干员列表和各星级出现的概率。

### 危机合约

#### ACT38D1
```
GET /activity/act38d1
```

返回尖灭行动（ACT38D1）服务器数据。

#### 当天的合约内容

```
GET /crisis/today
```

在赛季期间返回常驻地图和轮换地图的任务和词条内容。  
在非赛季期间返回每日训练轮换地图的词条内容。

#### 当天的合约内容（服务器原始数据）

```
GET /crisis/today/internal
```

### 采购中心

### 机密圣所（危机合约商店）

```
GET /shop/crisis
```

返回危机合约-机密圣所（危机合约商店）内容。  

#### 源石交易所

```
GET /shop/cash
```

返回采购中心-源石交易所（氪金）内容。  

#### 组合包

```
GET /shop/gp
```

返回采购中心-组合包内容。  

#### 时装商店

```
GET /shop/skin
```

返回采购中心-时装商店（皮肤）内容。  

#### 凭证交易所

```
GET /shop/low
```

返回资质凭证区（绿票）内容。  

```
GET /shop/high
```

返回高级凭证区（黄票）内容。  

```
GET /shop/extra
```

返回采购凭证区（红票）内容。  

```
GET /shop/epgs
```

返回寻访参数模型（天井常驻商店）内容。  

```
GET /shop/lmtgs
```

返回寻访数据契约（天井商店）内容。  

```
GET /shop/rep
```

返回情报凭证（复刻商店）内容。  

#### 家具商店

```
GET /shop/furni
```

返回采购中心-家具商店内容。  

#### 好友库(WIP)

开发中，预计通过Weedy实现一个查找好友~~抱大腿~~用的功能
