# Authentication Events

以下表格描述了认证类 Syslog 事件的字段。

| 字段名 | 类型 | 描述 |
| ------ | ---- | ---- |
| event_id | int | 事件唯一 ID |
| user | string | 发生事件的用户 |
| timestamp | datetime | 时间戳 |
| status | string | 成功或失败 |

示例：

```plaintext
event_id: 1001
user: admin
timestamp: 2024-07-08T12:00:00Z
status: success
