---
title: PidTagRecipientReassignmentProhibited Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341113"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>PidTagRecipientReassignmentProhibited Canonical Property

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, запрещено ли добавлять дополнительных получателей при отправке сообщения для сообщения электронной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Идентификатор:  <br/> |0x002B  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство устанавливается на основе значения  PR_SENSITIVITY[(PidTagSensitivity).](pidtagsensitivity-canonical-property.md) Если **PR_SENSITIVITY** установлено значение "0x00000000" (нормальное) или "0x00000003" (конфиденциальное), это свойство должно быть заданной на значение "0x00" или отсутствовать, что допускается добавление дополнительных или разных получателей в сообщение электронной почты. Если PR_SENSITIVITY объекта  электронной почты задают "0x00000001" (личное) или "0x00000002" (частное), это свойство должно быть задано "0x01", чтобы предотвратить добавление дополнительных или разных получателей этой электронной почты путем переададки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые в сообщениях электронной почты.
    
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

