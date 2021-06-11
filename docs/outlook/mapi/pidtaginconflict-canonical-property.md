---
title: Каноническое свойство PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358536"
---
# <a name="pidtaginconflict-canonical-property"></a>Каноническое свойство PidTagInConflict

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, когда вложение представляет альтернативную реплику.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IN_CONFLICT  <br/> |
|Идентификатор:  <br/> |0x666C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Заметка о конфликте  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент и сервер электронной почты должны создавать сообщение о разрешении конфликтов при обнаружении конфликта с текущей версией сообщения в реплике во время синхронизации. Важно понимать, что вполне возможно, что текущая версия сообщения в локальной реплике была передана во время текущей операции синхронизации. Это произойдет, когда конфликт уже существует на сервере перед скачиванием конфликтующих сообщений в локализованную реплику. Сообщение о разрешении конфликтов должно синхронизироваться как независимые реплики с конфликтующие PCLs. Само сообщение по разрешению конфликтов не должно синхронизироваться между клиентом и сервером; следует обмениваться только независимыми репликами. Затем партнер синхронизации должен создать новое сообщение, которое соответствует структуре сообщения о конфликте. Поэтому важно, чтобы клиент и сервер использовали тот же алгоритм для обнаружения элемента "победитель". Для обнаружения "победителя" необходимо применить следующие правила:
  
1. Время последней модификации.
    
2. Higher CN GUID (using memory compare) to break tie.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

