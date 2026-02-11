#### SwiftMessageDTO

| Поле | Тип | Описание |
|------|-----|----------|
| messageId | string (UUID) | Уникальный идентификатор сообщения |
| messageType | string | Тип SWIFT (MT103, MT202, MT940…) |
| senderBic | string | BIC отправителя |
| receiverBic | string | BIC получателя |
| currency | string | Валюта операции |
| amount | decimal | Сумма |
| valueDate | date | Дата валютирования |
| rawPayload | string | Оригинальное SWIFT сообщение |
| createdAt | datetime | Время приема |

---

#### RoutingResultDTO

| Поле | Тип | Описание |
|------|-----|----------|
| messageId | string | ID сообщения |
| route | string | Название целевого сервиса |
| status | string | RECEIVED / ROUTED / FAILED |
| reason | string | Причина ошибки (если есть) |
| processedAt | datetime | Время обработки |

---

#### RoutingRuleDTO

| Поле | Тип | Описание |
|------|-----|----------|
| ruleId | string | ID правила |
| messageType | string | Тип MT |
| senderBic | string | Фильтр по отправителю |
| currency | string | Фильтр по валюте |
| targetSystem | string | Целевая система |
| priority | int | Приоритет правила |
| active | boolean | Активность правила |
