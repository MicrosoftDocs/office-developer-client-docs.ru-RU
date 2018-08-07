---
title: Каноническое свойство PidTagIpmTaskEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811289"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a>Каноническое свойство PidTagIpmTaskEntryId

  
  
**Относится к**: Outlook 
  
Содержит **идентификатор записи** папки задач Outlook. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IPM_TASK_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x36D4  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство чтения или записи с помощью протокола свойство и объект Stream. Чтение из и в папке "Входящие" или корневой. Реализация необходимо использовать папку "Входящие" при хранилище, является основной пользователь обмена мгновенными сообщениями, и в ней должна использоваться в корневую папку, когда хранилище пользователя делегатом.
  
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

