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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438528"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Каноническое свойство PidTagContentCorrelator

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, которое отправитель сообщения может использовать для совпадения отчета с исходным сообщением.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Идентификатор:  <br/> |0x0007  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Содержимое двоичной строки определяется составивщиком сообщений. Если задано исходяние сообщения, это свойство должно быть скопировано на любые отчеты, созданные в ответ на сообщение.
  
## <a name="related-resources"></a>Связанные ресурсы

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

