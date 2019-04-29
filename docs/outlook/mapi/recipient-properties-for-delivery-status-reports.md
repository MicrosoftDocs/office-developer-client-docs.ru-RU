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
ms.openlocfilehash: 784cac21aac5de18952f3768af9b8f189f604981
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411087"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Свойства получателей для отчетов о состоянии доставки

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В отчетах о состоянии доставки для получателей имеются следующие свойства. **Пр_деливер_тиме** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) не используется в отчетах о недоставке. **Пр_ндр_диаг_коде** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) и **пр_ндр_реасон_коде** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) используются только в отчетах о недоставке.
  
**Заголовок таблицы**

|**Property**|**Декриптион**|
|:-----|:-----|
|**Пр_деливер_тиме** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Содержит дату и время доставки исходного сообщения.  <br/> |
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Содержит отображаемое имя для данного объекта MAPI.  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Содержит идентификатор записи MAPI, используемый для открытия и изменения свойств определенного объекта MAPI.  <br/> |
|**Пр_ндр_диаг_коде** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Содержит диагностический код, который формирует часть отчета о недоставке.  <br/> |
|**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Содержит текстовую строку, определяющую класс сообщений, определенный отправителем, например IPM. Ноте.  <br/> |
|**Пр_ндр_реасон_коде** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Содержит закодированную причину непоставки, которая является частью отчета о недоставке.  <br/> |
|**Пр_оригинал_дисплай_наме** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Содержит исходное отображаемое имя для записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.  <br/> |
|**Пр_оригинал_ентрид** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Содержит исходный идентификатор записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.  <br/> |
|**Пр_оригинал_сеарч_кэй** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Содержит исходный ключ поиска для записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.  <br/> |
|**Пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Содержит тип получателя сообщения.  <br/> |
|**Пр_репорт_текст** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Содержит необязательный текст для отчета, созданного системой обмена сообщениями.  <br/> |
|**Пр_репорт_тиме** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Содержит дату и время создания отчета системой обмена сообщениями.  <br/> |
|**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Содержит ключ, сравнимый с двоичным кодом, который определяет коррелированные объекты для поиска.  <br/> |
|**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Содержит значение, используемое для связи значка с определенной строкой таблицы.  <br/> |
|**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Содержит тип объекта.  <br/> |
   

