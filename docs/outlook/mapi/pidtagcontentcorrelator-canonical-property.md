---
title: Каноническое свойство PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331978"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Каноническое свойство PidTagContentCorrelator

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, которое отправитель сообщения может использовать для сравнения отчета с исходным сообщением.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_КОНТЕНТ_КОРРЕЛАТОР  <br/> |
|Идентификатор:  <br/> |0x0007  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Комментарии

Содержимое двоичной строки определяется инициатором сообщения. Если для исходящих сообщений задано значение, это свойство должно быть скопировано в любые отчеты, созданные в ответ на сообщение.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

