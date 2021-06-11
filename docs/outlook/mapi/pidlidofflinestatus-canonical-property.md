---
title: Каноническое свойство PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418836"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Каноническое свойство PidLidOfflineStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет состояние файла документов на сервере, который реализует [MS-LISTSWS].
  
|||
|:-----|:-----|
|Связанные свойства  <br/> |dispidOfflineStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085B9  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

В следующей таблице показаны возможные значения этого свойства.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Документ не проверяется.  <br/> |
|1  <br/> |Документ проверяется текущему пользователю.  <br/> |
|2  <br/> |Документ не проверяется, но текущий пользователь имеет копию файла, сохраненного для редактирования на текущем компьютере.  <br/> |
   
Это свойство вычисляется локально и не отправляется на сервер в любое время, если пользователь не перетаскивать элемент на другую учетную запись. В этом случае оно рассматривается как настраиваемая собственность, определяемая пользователем.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

