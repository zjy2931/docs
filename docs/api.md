## 直播相关api

### 1.连麦申请（男端）
#### 请求地址 /app/live/callGirl
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 期望连麦主播的id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 2.主播获取当前匹配客人是否可以开播（女端）
#### 请求地址 /app/live/getMatchInfo
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 连麦客人id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| matchStatus | int | 是 | 1客人同意可开播 2.客人未应答 3客人拒绝不可开播 |

### 3.主播直播中挂断（女端）
#### 请求地址 /app/live/hangUpMan
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 连麦客人id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 4.客人直播中挂断（男端）
#### 请求地址 /app/live/hangUpGirl
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 主播id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 5.送礼物（男端）
#### 请求地址 /app/live/sendGift
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| giftId | Long | 是 | 礼物id |
| amount | int | 否 | 默认1 |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 6.礼物列表（男端）
#### 请求地址 /app/live/getGiftList
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| itemList | item | 是 | 如下 |
#### item
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| giftId | long | 是 | 礼物id |
| giftName | string | 是 | 礼物名称 |
| giftImgUrl | string | 是 | 礼物图片 |
| giftCost | long | 是 | 礼物价值 |

### 7.男找女通话申请（男端）
#### 请求地址 /app/live/callApplyGirl
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 主播id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 8.女找男通话申请（女端）
#### 请求地址 /app/live/callApplyMan
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 期望的客人id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 9.女找男通话应答（男端）
#### 请求地址 /app/live/callReplyGirl
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 主播id |
| reply | int | 是 | 1同意 2拒绝 |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 10.视频服务创建房间（女端）
腾讯接口在bodyjson里增加参数
#### 请求地址 /weapp/live_room/create_room
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| guestId | long | 否 | 客人id |
#### 返回参数
见腾讯

### 11.找人列表（女端）
#### 请求地址 /app/user/getGuestList
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | long | 否 | 客人id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| itemList | item | 是 | 如下 |
#### item
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| userId | long | 是 | 用户id |
| nickname | string | 是 | 用户昵称 |
| headImg | string | 是 | 用户头像 |
| age | int | 是 | 用户年龄 |

### 12.女端开始聊天（女端）
#### 请求地址 /app/live/startCall
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| targetUserId | long | 是 | 客人id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 13.获取通话明细（女端）
#### 请求地址 /app/live/getCallRecordDesc
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| recordId | long | 是 | 记录id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| nickname | string | 是 | 昵称 |
| age | int | 是 | 年龄 |
| recordTime | string | 是 | 通话时间yyyy-MM-dd HH24:mm |
| status | int | 是 | 1未接 2接通 |
| unitPrice | string | 是 | 主播单价 XXX积分/分钟 |
| callTime | string | 是 | 通话时长 XXX分钟 |
| callPoint | string | 是 | 通话获得积分 获得XXX积分 |
| headImg | string | 是 | 头像URL |

### 14.当前主播基础信息（男端）
#### 请求地址 /app/live/getMasterInfo
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| masterId | long | 是 | 主播id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 接口返回文字 |
| masterId | Long | 是 | 主播id |
| liveStatus  | int | 是| 主播当前状态 1离线 3在播 4忙线 |
| nickname | string | 是 | 昵称 |
| age | int | 是 | 年龄 |
| imgUrl | string | 是 | 头像url |
| unitPrice | string | 是 | 单价  XXX积分 |
| unitPriceDiamond | string | 是 | 单价 XXX钻石 |

### 15.通话结算（男端）
#### 请求地址 /app/live/getCallResultGuest
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| roomInstanceId | long | 是 | 房间实例id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| nickname | string | 是 | 对方昵称 |
| unitPrice | string | 是 | 主播单价 XXX钻石/分钟 |
| callTime | string | 是 | 通话时长 XXX分钟 |
| callDiamond | string | 是 | 消耗钻石 消耗XXX钻石 |
| headImg | string | 是 | 对方头像URL |
| diamond | string | 是 | 当前钻石数 |
| title | string | 否 | 违规场景下的提示信息 非必填 |
| streamStatus | int | 否 | 0封号2禁播 其他值均忽略 非必填 |

### 16.通话结算（女端）
#### 请求地址 /app/live/getCallResultMaster
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| roomInstanceId | long | 是 | 房间实例id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| nickname | string | 是 | 对方昵称 |
| unitPrice | string | 是 | 主播单价 XXX积分/分钟 |
| callTime | string | 是 | 通话时长 XXX分钟 |
| callPoint | string | 是 | 获得积分 获得XXX积分 |
| headImg | string | 是 | 对方头像URL |
| point | string | 是 | 当前积分数 |
| title | string | 否 | 违规场景下的提示信息 非必填 |
| streamStatus | int | 否 | 0封号2禁播 其他值均忽略 非必填 |

### 17.当前用户钱币信息（男女端）
#### 请求地址 /app/user/getCurrentUserInfo
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| diamond | string | 否 | 男端钻石数 |
| unitPrice | string | 否 | 女端单价（积分） |
| display | int | 否 | 男端是否屏蔽 1屏蔽 0不屏蔽 |

### 18.更新单价（女端）
#### 请求地址 /app/user/updateUnitPrice
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| unitPrice | long | 是 | 单价积分 |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| unitPrice | long | 是 | 单价积分 |

### 19.更新屏蔽状态（男端）
#### 请求地址 /app/user/updateDisplay
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| display | int | 是 | 1屏蔽 0不屏蔽 |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| display | int | 是 | 1屏蔽 0不屏蔽 |

### 20.我的通话（男端）
#### 请求地址 /app/live/myCallRecord
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| itemList | list<Item> | 是 | 我的通话列表 |

##### Item
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| userId | long | 是 | 对方用户id |
| recordId | long | 是 | 通话记录id 用于明细查询 |
| nickName | string | 是 | 昵称 |
| recordDatetime | string | 是 | 通话日期 |
| age | string | 是 | 年龄 |
| imgUrl | string | 是 | 头像URL |

### 21.我的收益（女端）
#### 请求地址 /app/live/getMyIncome
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| point | string | 是 |  XXX积分 |
| callTime | string | 是 | XXX分钟 |

### 22.获取当前客人状态（女端）
#### 请求地址 /app/live/getGuestCurrentUserInfo
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| guestId | Long | 是 | 客人用户id |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| onlineStatus | int | 是 |  1离线 3在线 4忙线 |

### 23.支付记录（男端）
#### 请求地址 /app/pay/getOrderList
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| itemList | List | 是 |  记录列表 |
#### Item
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| payFee | long | 是 | 支付金额(分) |
| payStatusValue | string | 是 | 充值成功/充值失败 |
| payDateTime | string | 是 |  充值日期(yyyy-MM-dd hh:mm:ss) |

### 23.获取主播推流url（男端）
#### 请求地址 /weapp/live_room/get_push_url
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| userID | string | 是 | 当前用户ID(字符串)|
#### 请求参数json中
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| roomID | string | 是 | 房间号 |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| pushURL | string | 是 |  目标用户的推流地址 |

### 24.获取分享信息（男端）
#### 请求地址 /app/user/getShareInfo
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| title | string | 是 |  分享标题 |
| imgUrl | string | 是 |  分享图片 |

### 25.小程序功能开关（男端）
#### 请求地址 /app/login/weChatVersion
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| version | int | 是 | 版本(每次递增) | 
| terminalType | int | 是 | 3| 
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |

### 26.获取平台警告信息（女端）
#### 请求地址 /app/live/getWarnMessage
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| warnMessage | string | 是 | 警告信息 |

### 27.获取平台禁播信息（女端）
#### 请求地址 /app/live/getExitMessage
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |
| exitMessage | string | 是 | 禁播信息 |

### 28.模板消息触发表单（男端）
#### 请求地址 /app/live/messageForm
#### 请求方式 POST
#### 请求参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| token | string | 是 | token |
| formId | string | 是 | 小程序表单form_id 支付场景用prepay_id |
| moduleName | string | 是 | 模块名称 |
#### 模块名称对应关系 
| 描述 | value |
| ------ | ------ |
| 登录后 | login |
| 支付后 | pay |
| 首页 | main |
#### 返回参数
| 字段名 | 类型 | 是否必填 | 描述 |
| ------ | ------ | ------ | ------ |
| code | int | 是 | 0表示正常 |
| message | string | 是 | 返回的文字信息 |





