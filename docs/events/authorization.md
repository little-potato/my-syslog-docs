# Authorization Events

以下表格描述了授权类 Syslog 事件的字段。

| 字段名 | 类型 | 描述 |
| ------ | ---- | ---- |
| event_id | int | 事件唯一 ID |
| user | string | 发生事件的用户 |
| action | string | 授权操作 |
| resource | string | 被授权的资源 |
| result | string | 是否授权成功 |

示例：

```plaintext
event_id: 2001
user: alice
action: read
resource: /secure-data
result: granted
```
```
