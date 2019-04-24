---
title: Пересылка сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328065"
---
# <a name="forwarding-a-message"></a>Пересылка сообщения

**Область применения**: Outlook 2013 | Outlook 2016 
  
ПереСылка сообщения включает в себя множество таких же задач, как отправка исходного сообщения. Для начала необходимо открыть хранилище сообщений по умолчанию и папку, предназначенную для хранения исходящих сообщений, как правило, в папке "исХодящие", и вызвать метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания переадресованного сообщения. Кроме того, необходимо открыть папку, в которой находится исходное сообщение, обычно это папка "Входящие". Сведения о том, как открывать другие папки, можно найти [в разделе Открытие папки хранилища сообщений](opening-a-message-store-folder.md).
  
Основное различие между созданием перенаправляемого и созданием исходного сообщения заключается в том, что в переадресованном сообщении большинство свойств либо основано на, либо копируются непосредственно из свойств исходного сообщения. 
  
**Пересылка сообщения**
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. [в разделе Открытие хранилища сообщений по умолчанию](opening-the-default-message-store.md).
    
2. Откройте папку "исХодящие". Дополнительную информацию можно узнать в статье [Открытие папки хранилища сообщений](opening-a-message-store-folder.md).
    
3. ВыЗовите метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) , чтобы создать новое переадресованное сообщение. 
    
4. ВыЗовите метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать следующие свойства в переадресованное сообщение: 
    
   - **Текст\_** ([PidTagBody](pidtagbody-canonical-property.md)) (), **\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **Пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в зависимости от того, поддерживает ли формат RTF, обычный текст или HTML.
    
   - **PR\_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Скопируйте вложения сообщения из исходного сообщения, вызвав метод **IMAPIProp:: CopyTo** исходного сообщения, чтобы скопировать свойство **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) или вызвав следующий метод: три пошаговых процедуры для копирования каждого вложения:
    
   1. Для создания нового вложения выЗовите метод [iMessage:: креатеаттач](imessage-createattach.md) нового переадресованного сообщения::. 
      
   2. ВыЗовите метод [iMessage:: опенаттач](imessage-openattach.md) исходного сообщения, чтобы открыть вложение, которое необходимо скопировать. 
      
   3. ВыЗовите метод **IMAPIProp:: CopyTo** исходного сообщения, чтобы скопировать все свойства вложений из старого вложения в новое. 
    
6. Не включайте в вызов IMAPIProp следующие свойства: **: CopyTo**: 
    
|||
|:-----|:-----|
|**Пр_клиент_субмит_тиме** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**Пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**Пр_мессаже_довнлоад_тиме** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**Пр_оригинатор_деливери_репорт_рекуестед** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |Свойства **пр_рквд_репресентинг**  <br/> |
|**Пр_реад_рецеипт_ентрид** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**Пр_реад_рецеипт_рекуестед** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|Свойства **пр_рецеивед_би**  <br/> |Свойства **пр_репли_реЦипиент**  <br/> |
|**Пр_репорт_ентрид** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |Свойства **пр_сендер**  <br/> |
|Свойства **пр_сент_репресентинг**  <br/> |**Пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**Пр_субжект_префикс** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Форматирование текста сообщения путем добавления отступа и абзаца заголовка, включающего исходный отправитель, дату передачи, тему и список получателей. Не включайте в контент символы префиксов из Интернета.
    
2. ВыЗовите [сккреатеконверсатиониндекс](sccreateconversationindex.md), передав значение свойства **пр_конверсатион_индекс** исходного сообщения ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
3. Задайте префикс для переадресованного сообщения. Если вы используете стандарт "FW:", объедините эти символы в начале **пр_нормализед_субжект** и установите **пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md)) в эту новую строку. Не задавайте **пр_субжект_префикс** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Если вы используете нестандартный префикс, например строку длиной более трех символов, сохраните ее в **пр_субжект_префикс**. 
    
4. Задайте для свойств **пр_сент_репресентинг** соответствующие значения в свойствах **пр_рквд_репресентинг** . 
    
5. Создайте список получателей. Дополнительную информацию можно узнать [в статье Создание списка получателей](creating-a-recipient-list.md).
    
6. ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) переадресованного сообщения, чтобы сохранить его или [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы сохранить и отправить его. 
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

