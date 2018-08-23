---
title: Каноническое свойство PidTagParentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 48627c6d6eb2100e7dfcab832c86c1ec2e4ec8bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582807"
---
# <a name="pidtagparententryid-canonical-property"></a>Каноническое свойство PidTagParentEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи папка, содержащая папки или сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PARENT_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0E09  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство вычисляется путем хранилищ сообщений для всех папок и сообщений.
  
Для корневой папки хранилища сообщений это свойство содержит идентификатор записи папки собственные.
  
 **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) и это свойство не связаны друг с другом. Они принадлежат совершенно различных контекстах.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Определяет структуры основных данных, которые используются для удаленных операций.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)
  
> Задает метод доставки автономной адресной книги (OAB) данных от сервера к клиенту.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

