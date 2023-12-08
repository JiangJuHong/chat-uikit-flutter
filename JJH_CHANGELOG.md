# 改动说明
fork来源：https://github.com/TencentCloud/chat-uikit-flutter

此仓库：在原有基础上增加通用性适配扩展，此改动不涉及到具体项目业务，尽可能的在原有基础上增加通用适配性，适应更多场景，改动说明参考以下内容：

## 改动明细
### [tim_uikit_conversation_item.dart](lib%2Fui%2Fviews%2FTIMUIKitConversation%2Ftim_uikit_conversation_item.dart) 
* feat 增加参数：`avatarBuilder`，使用时可直接传入该构建器替换默认头像显示组件
* feat 修改参数：`nickName` 从 string 类型替换为 Widget 类型，并增加DefaultTextStyle保持原有样式不变
* feat 将 边框提取到 [tim_uikit_conversation.dart](lib%2Fui%2Fviews%2FTIMUIKitConversation%2Ftim_uikit_conversation.dart) 组件中

### [tim_uikit_conversation.dart](lib%2Fui%2Fviews%2FTIMUIKitConversation%2Ftim_uikit_conversation.dart)
* feat 将 ListView.builder 修改为 ListView.separated
* feat 增加属性 separatorBuilder，可通过外部传入自定义分割线样式

### [tim_uikit_conversation_draft_text.dart](lib%2Fui%2Fviews%2FTIMUIKitConversation%2Ftim_uikit_conversation_draft_text.dart)
* feat 以Rich的方式完全重写内容展示格式，解决：草稿字样和内容未对齐问题、显示草稿时和不显示草稿时样式有细微差别的问题

### [tim_uikit_conversation_last_msg.dart](lib%2Fui%2Fviews%2FTIMUIKitConversation%2Ftim_uikit_conversation_last_msg.dart)
* feat 以Rich的方式完全重写内容展示格式，解决显示草稿时和不显示草稿时样式有细微差别的问题，调整行高和草稿时的一致，均为1.0