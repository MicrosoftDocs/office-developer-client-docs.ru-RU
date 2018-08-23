---
title: Свойства получателей для отчетов о состоянии доставки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 58711a18fa6dc512cca10644437bee2ecd4d2143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592999"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Свойства получателей для отчетов о состоянии доставки

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Выполнение следующих условий для отчетов о состоянии доставки для получателей. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) не используется на отчеты о недоставке. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) и **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) используются только для отчетов о недоставке.
  
**Заголовок таблицы**

|**Свойство**|**Описание**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Содержит дату и время, когда исходное сообщение было доставлено.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Содержит отображаемое имя для данного объекта MAPI.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Содержит идентификатор запись MAPI, используемый для открытия и изменения свойств конкретного объекта MAPI.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Содержит код диагностики, часть отчет о недоставке.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Содержит текстовую строку, которая определяет класс отправителя определенное сообщение, такие как IPM. Примечание.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Содержит зашифрованный причина недоставке, часть отчет о недоставке.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Содержит отображаемое имя записи копируются из адресной книги Личная адресная книга или других для записи адресной книги.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Содержит исходный идентификатор записи для входа, скопированные из адресной книги для Личная адресная книга или других доступным для записи адресной книги.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Содержит исходного ключа поиска для записи, скопированные из адресной книги для Личная адресная книга или других доступным для записи адресной книги.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Содержит тип получателя для получателя сообщения.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Содержит необязательный атрибут типа text для отчета, созданных функцией системы обмена сообщениями.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Содержит дату и время создания отчета в системе обмена сообщениями.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Содержит двоичный сравнимые ключ, который определяет соответствующих объектов для поиска.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Содержит значение, используемое для сопоставления значка с конкретной строки таблицы.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Содержит тип объекта.  <br/> |
   

