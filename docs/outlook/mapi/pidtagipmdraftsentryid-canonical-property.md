---
title: Каноническое свойство PidTagIpmDraftsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmDraftsEntryId
api_type:
- HeaderDef
ms.assetid: 17d64211-6265-41f4-b016-3677d75af966
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e259c86803147d782469c8d86b23694d8b54e69d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327890"
---
# <a name="pidtagipmdraftsentryid-canonical-property"></a>Каноническое свойство PidTagIpmDraftsEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит **entryID** папки Outlook черновиков. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IPM_DRAFTS_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x36D7  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство хранится в папке "Входящие", а также в корневой папке магазина сообщений. Чтобы получить доступ к свойству в определенном хранилище сообщений, сделайте следующее: 
  
1. Сначала найми свойство в папке "Входящие". Используйте [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить ссылку на **EntryID** для папки "Входящие". 
    
2. Если **IMsgStore::GetReceiveFolder** успешно, используйте ссылку на **EntryID** почтового ящика и [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть почтовый ящик и получить ссылку на объект **IMAPIFolder.** 
    
3. Если **IMsgStore::OpenEntry** успешно, используйте возвращаемую ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps](imapiprop-getprops.md) для получения нужного свойства. 
    
4. Если не удается сделать шаг 1, 2 или 3, и посмотрите свойство в корневой папке. Для этого используйте **IMsgStore::OpenEntry,** указав NULL для **lpEntryID,** чтобы открыть корневую папку магазина сообщений и получить ссылку на объект **IMAPIFolder.** 
    
5. Если открытие корневой папки успешно, используйте возвращаемую ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужного свойства. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.
    
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

