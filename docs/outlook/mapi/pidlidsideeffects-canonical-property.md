---
title: Каноническое свойство PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810538"
---
# <a name="pidlidsideeffects-canonical-property"></a>Каноническое свойство PidLidSideEffects

  
  
**Относится к**: Outlook 
  
Позволяет определить способ обработки объекта message клиентом при работе на входные данные конечных пользователей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSideEffects  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008510  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Конфигурация во время выполнения  <br/> |
   
## <a name="remarks"></a>Замечания

Необходимо установить значение битовую или ноль или несколько из следующих флагов.
  
|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |При удалении на объект message требуется дополнительной обработки.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Пользовательского интерфейса не связан с объектом сообщения.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Требуется дополнительной обработки на объект сообщения, когда перемещение и копирование объект folder со свойством **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) «IPF. Обратите внимание на то».  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |При копировании в другую папку на объект message требуется дополнительной обработки.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |При переходе на другую папку на объект message требуется дополнительной обработки.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |При отображении команд для конечных пользователей на объект message требуется дополнительной обработки.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Не удается отменить операцию удаления, не должен быть установлен, если не имеет значение «seOpenToDelete».  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Не удается отменить операцию копирования, не должен быть установлен, если не имеет значение «seOpenTocopy».  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Не удается отменить операцию перемещения, не должен быть установлен, если не имеет значение «seOpenToMove».  <br/> |
|seHasScript  <br/> |0x2000  <br/> |Объект сообщения содержит скрипт конечных пользователей.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Чтобы окончательно удалить объект message требуется дополнительной обработки.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

