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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384439"
---
# <a name="pidtaginconflict-canonical-property"></a>Каноническое свойство PidTagInConflict

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, когда вложение представляет альтернативного реплики.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IN_CONFLICT  <br/> |
|Идентификатор:  <br/> |0x666C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Примечание конфликта  <br/> |
   
## <a name="remarks"></a>Замечания

Сервером и клиентом электронной почты необходимо создать сообщение устранением конфликтов при обнаружении конфликта с текущей версией сообщение в реплике во время синхронизации. Важно понимать, что это и возможно, что текущая версия сообщения в локальной реплики передавался во время текущей операции синхронизации. Это происходит конфликт уже существует на сервере перед конфликтующие сообщения были загружены для локальной реплики. Устраните конфликт сообщения должны быть синхронизированы как независимые реплики с конфликтующие PCLs. Конфликт устранить сообщения не должны быть синхронизированы между клиентом и сервером; только независимой реплик обмена. Партнер синхронизации необходимо создать новое сообщение, которое совпадает со структурой сообщение о конфликте. Таким образом важно, что клиент и сервер используют тот же алгоритм для обнаружения элемента «по результатам». Для обнаружения «результатам» должны применяться следующие правила:
  
1. Время последнего изменения.
    
2. Выше CN идентификатор GUID (compare памяти) чтобы разорвать связи.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

