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
  
Для отчетов о состоянии доставки для получателей присутствуют следующие свойства. **PR_DELIVER_TIME** ([PidTagDeliverTime)](pidtagdelivertime-canonical-property.md)не используется в отчетах о доставке. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode)](pidtagnondeliveryreportdiagcode-canonical-property.md)и **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode)](pidtagnondeliveryreportreasoncode-canonical-property.md)используются только в отчетах о невыставке.
  
**Название таблицы**

|**Property**|**Расшифровка**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime)](pidtagdelivertime-canonical-property.md)  <br/> |Содержит дату и время доставки исходного сообщения.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |Содержит отображаемую имя для заданного объекта MAPI.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Содержит идентификатор записи MAPI, используемый для открытия и изменения свойств определенного объекта MAPI.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode)](pidtagnondeliveryreportdiagcode-canonical-property.md)  <br/> |Содержит диагностический код, который является частью отчета о не доставке.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)  <br/> |Содержит текстовую строку, идентифицирующую определяемый отправителем класс сообщений, например IPM.Note.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode)](pidtagnondeliveryreportreasoncode-canonical-property.md)  <br/> |Содержит закодированную причину не доставки, которая является частью отчета о не доставке.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Содержит исходное отображаемое имя записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId)](pidtagoriginalentryid-canonical-property.md)  <br/> |Содержит исходный идентификатор записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey)](pidtagoriginalsearchkey-canonical-property.md)  <br/> |Содержит исходный ключ поиска для записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)  <br/> |Содержит тип получателя сообщения.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText)](pidtagreporttext-canonical-property.md)  <br/> |Содержит необязательный текст для отчета, сгенерированного системой обмена сообщениями.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime)](pidtagreporttime-canonical-property.md)  <br/> |Содержит дату и время, когда система обмена сообщениями создает отчет.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)  <br/> |Содержит схожий двоичный ключ, который идентифицирует связанные объекты для поиска.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |Содержит значение, используемого для связи значка с определенной строкой таблицы.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Содержит тип объекта.  <br/> |
   

