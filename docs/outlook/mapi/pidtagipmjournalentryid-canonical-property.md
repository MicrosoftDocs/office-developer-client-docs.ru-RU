---
title: Каноническое свойство PidTagIpmJournalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmJournalEntryId
api_type:
- HeaderDef
ms.assetid: a3765b9d-a108-46d7-a97c-a825ae3980be
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b1fc2beaa85f8bbc82debe6b39ea02429aeeea16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578691"
---
# <a name="pidtagipmjournalentryid-canonical-property"></a>Каноническое свойство PidTagIpmJournalEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит **идентификатор записи** журнала Outlook папки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IPM_JOURNAL_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x36D2  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство хранится в папке "Входящие", а также в корневую папку хранилища сообщений. Доступ к свойству для хранилища определенное сообщение, выполните следующие действия. 
  
1. Во-первых найдите свойство в папке "Входящие". Используйте [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) для получения ссылки на **Код записи** для папки "Входящие". 
    
2. Если **IMsgStore::GetReceiveFolder** выполнена успешно, используйте ссылку на файл **EntryID** для папки "Входящие" и [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки «Входящие» и получить ссылку на объект **IMAPIFolder** . 
    
3. Если **IMsgStore::OpenEntry** выполнена успешно, затем используйте возвращенный ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps](imapiprop-getprops.md) для получения нужное свойство. 
    
4. Если не удается выполнить шаг 1, 2 или 3, найдите свойство в корневой папке. Для этого используйте **IMsgStore::OpenEntry**, указание NULL для **lpEntryID**, чтобы открыть корневую папку хранилища сообщений и получить ссылку на объект **IMAPIFolder** . 
    
5. При успешном открытии в корневой папке затем используйте возвращенный ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужное свойство. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

