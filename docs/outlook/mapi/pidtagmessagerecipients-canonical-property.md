---
title: Каноническое свойство PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355687"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Каноническое свойство PidTagMessageRecipients

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу ограничений, которые можно применить к таблице содержимого, чтобы найти все сообщения, содержащие подобекцы получателей, которые соответствуют ограничениям. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Идентификатор:  <br/> |0x0E12  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство можно исключить в [операциях IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в [операции IMAPIProp::CopyProps.](imapiprop-copyprops.md) Как свойство типа **PT_OBJECT,** его невозможно успешно получить [методом IMAPIProp::GetProps.](imapiprop-getprops.md) Его содержимое должно быть доступны [методом IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивая **идентификатор IID_IMAPITable** интерфейса. Поставщики услуг должны сообщить об этом [методу IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он за установлен, но может сообщить об этом или нет, если он не установлен. 
  
Чтобы получить содержимое таблицы, клиентская заявка должна вызвать [метод IMessage::GetRecipientTable.](imessage-getrecipienttable.md) 
  
Это свойство можно использовать для ограничения субобекции, указав его в [структуре SSubRestriction.](ssubrestriction.md) Это позволяет клиенту ограничить представление контейнера сообщениями с данными критериями для получателей. Сообщение имеет право на просмотр, если хотя бы одна строка в таблице получателей, то есть один получатель удовлетворяет ограничению subobject. 
  
 **Примечание** Использование результатов ограничения subobject эквивалентно вызову [IMAPISession::OpenEntry](imapisession-openentry.md) для каждого сообщения в таблице. В зависимости от клиентского приложения и количества сообщений, которые будут искаться, это может повлиять на производительность. 
  
Свойство **PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)и это свойство аналогично по использованию. Несколько свойств MAPI предоставляют доступ к таблицам: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)  <br/> |Таблица контента  <br/> |
|**PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)  <br/> |Таблица иерархии  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)  <br/> |Связанная таблица контента  <br/> |
|**PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)  <br/> |Таблица вложений  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Таблица получателей  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

