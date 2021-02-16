---
title: Каноническое свойство PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346580"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a>Каноническое свойство PidTagInitialDetailsPane

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает страницу шаблона отображения, которая будет отображаться в первую очередь.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_INITIAL_DETAILS_PANE  <br/> |
|Идентификатор:  <br/> |0x3F08  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Таблицы отображения MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Он должен присутствовать во всех объектах адресной книги на сервере интерфейса поставщика службы имен (NSPI) и иметь нулевое значение (0). Он не должен быть определен для объектов в автономной адресной книге.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

