---
title: IMessage IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage
api_type:
- COM
ms.assetid: 7e244d40-595e-432c-aa8c-f9f62ca3c138
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 217411dc8bae12a3d7544a4cfd189c4c8f863195
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432501"
---
# <a name="imessage--imapiprop"></a>IMessage : IMAPIProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Управляет сообщениями, вложениями и получателями.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объект Message  <br/> |
|Реализовано в:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имессаже  <br/> |
|Тип указателя:  <br/> |ЛПМЕССАЖЕ  <br/> |
|Модель транзакции:  <br/> |Транзакции  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Жетаттачменттабле](imessage-getattachmenttable.md) <br/> |Возвращает таблицу вложений сообщения.  <br/> |
|[Опенаттач](imessage-openattach.md) <br/> |Открывает вложение.  <br/> |
|[Креатеаттач](imessage-createattach.md) <br/> |Создает новое вложение.  <br/> |
|[Делетеаттач](imessage-deleteattach.md) <br/> |Удаляет вложение.  <br/> |
|[ЖетреЦипиенттабле](imessage-getrecipienttable.md) <br/> |Возвращает таблицу получателей сообщения.  <br/> |
|[МодифиреЦипиентс](imessage-modifyrecipients.md) <br/> |����������, �������� ��� �������� ����������� ���������.  <br/> |
|[Субмитмессаже](imessage-submitmessage.md) <br/> |Сохраняет все изменения, внесенные в сообщение, и помечает его как готовый для отправки.  <br/> |
|[Сетреадфлаг](imessage-setreadflag.md) <br/> |Задает или снимает флаг МСГФЛАГ_РЕАД в свойстве **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения и управляет отправкой отчетов о прочтении.  <br/> |
   
Следующие свойства необходимы для сообщений на некоторый момент времени жизненного цикла. Большинство свойств, доступных только для чтения, задаются поставщиком хранилища сообщений, когда клиент вызывает метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) объекта Message. Другие свойства, доступные только для чтения, устанавливаются поставщиком транспорта. 
  
|**Обязательные свойства для сообщений всех классов**|**Access**|
|:-----|:-----|
|**Пр_креатион_тиме** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_дисплай_бкк** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_дисплай_кк** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_ласт_модификатион_тиме** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мессаже_кк_ме** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мессаже_реЦип_ме** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мессаже_то_ме** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Только для чтения  <br/> |
|Свойства **пр_оригинатор**  <br/> |Только для чтения  <br/> |
|**Пр_парент_дисплай** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|Свойства **пр_рецеивед_би**  <br/> |Только для чтения  <br/> |
|**Пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|Свойства **пр_сендер**  <br/> |Только для чтения  <br/> |
|**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
Следующие свойства доступны только для чтения клиентам, за исключением **пр_боди**. Клиенты создают это свойство при обработке отчета.
  
|**Свойства для сообщений отчетов**|
|:-----|
|**Пр_боди** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |
|**ПР_МЕССАЖЕ_КЛАСС** <br/> |
|**Пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**Пр_оригинал_деливери_тиме** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |
|**Пр_оригинал_дисплай_бкк** ([PidTagOriginalDisplayBcc](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> |
|**Пр_оригинал_дисплай_кк** ([PidTagOriginalDisplayCc](pidtagoriginaldisplaycc-canonical-property.md))  <br/> |
|**Пр_оригинал_дисплай_то** ([PidTagOriginalDisplayTo](pidtagoriginaldisplayto-canonical-property.md))  <br/> |
|**Пр_оригинал_субжект** ([PidTagOriginalSubject](pidtagoriginalsubject-canonical-property.md))  <br/> |
|**Пр_оригинал_субмит_тиме** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md))  <br/> |
|**Пр_репорт_таг** ([PidTagReportTag](pidtagreporttag-canonical-property.md))  <br/> |
|**Пр_репорт_текст** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |
|**Пр_репорт_тиме** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |
|**PR_SEARCH_KEY** <br/> |
|Свойства **пр_сендер**  <br/> |
|**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**Свойства получателей сообщений**|**Access**|**Обязательная или необязательная**|
|:-----|:-----|:-----|
|**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Только для чтения  <br/> |Обязательный  <br/> |
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |Обязательный  <br/> |
|**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Чтение и запись  <br/> |Обязательный  <br/> |
|**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Только для чтения  <br/> |Необязательный  <br/> |
|**PR_ENTRYID** <br/> |Только для чтения  <br/> |Обязательный  <br/> |
|**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |Обязательный  <br/> |
|**PR_SEARCH_KEY** <br/> |Только для чтения  <br/> |Необязательная  <br/> |
   

