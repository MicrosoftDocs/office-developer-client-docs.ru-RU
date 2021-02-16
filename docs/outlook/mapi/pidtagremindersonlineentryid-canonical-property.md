---
title: Каноническое свойство PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d845a37f9248a30dadd4db7722d8bed0f9f8d264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355064"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a>Каноническое свойство PidTagRemindersOnlineEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит **EntryID** папки напоминаний. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REM_ONLINE_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x36D5  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство хранится в папке "Входящие" и в корневой папке в хранилище сообщений. Чтобы получить доступ к свойству в определенном хранилище сообщений, сделайте следующее. 
  
1. Сначала наберем свойство в папке "Входящие". Используйте [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить ссылку на **EntryID** для папки "Входящие". 
    
2. Если **IMsgStore::GetReceiveFolder** успешно, используйте ссылку на **EntryID** входящих сообщений и [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть "Входящие" и получить ссылку на объект **IMAPIFolder.** 
    
3. Если **IMsgStore::OpenEntry** успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить нужное свойство. 
    
4. Если шаг 1, 2 или 3 не удается, наберем свойство в корневой папке. Для этого используйте **IMsgStore::OpenEntry,** указав NULL для **lpEntryID,** чтобы открыть корневую папку в хранилище сообщений и получить ссылку на объект **IMAPIFolder.** 
    
5. Если открытие корневой папки успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps,** чтобы получить нужное свойство. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

