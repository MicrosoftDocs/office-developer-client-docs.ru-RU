---
title: Каноническое свойство PidNameExchangeJunkEmailMoveStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540947"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a>Каноническое свойство PidNameExchangeJunkEmailMoveStamp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение сохраняемой почты, которое указывает, что сообщение не должно быть обработано фильтром нежелательной почты, так как оно уже обработано или является безопасным.
  
|||
|:-----|:-----|
|Дружелюбные имена:  <br/> |Нет  <br/> |
|Набор свойств:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Имя свойства:  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Безопасный обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство помеется для каждого сообщения, которое перемещается правилом нежелательной почты или является иным доверенным содержимым.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списков разрешающих и заблокированных сообщений, а также определение нежелательных сообщений электронной почты.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые представляют элементы RSS.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

