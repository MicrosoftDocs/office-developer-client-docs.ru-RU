---
title: Каноническое свойство PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342506"
---
# <a name="pidtagsensitivity-canonical-property"></a>Каноническое свойство PidTagSensitivity

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, которое указывает на мнение отправитель сообщения о чувствительности сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENSITIVITY  <br/> |
|Идентификатор:  <br/> |0x0036  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы объекты сообщений выставили это свойство.
  
Это свойство может иметь одно из следующих значений:
  
SENSITIVITY_NONE 
  
> Сообщение не имеет особой чувствительности.
    
SENSITIVITY_PERSONAL 
  
> Сообщение личное.
    
SENSITIVITY_PRIVATE 
  
> Сообщение закрыто.
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> Сообщение назначено конфиденциальной компанией.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

