---
title: Каноническое свойство PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2d8157c761cd21d5c8fcdf04948646d8102e774a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580140"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Каноническое свойство PidTagDeliveryPoint

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет характер функциональным сущности, с помощью которого был или будет доставлено получателю сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELIVERY_POINT  <br/> |
|Идентификатор:  <br/> |0x0C07  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство может иметь только один из следующих значений: 
  
MAPI_MH_DP_ML 
  
> Доставлено в список рассылки, отделения который в свою очередь может распространять сообщения большому количеству получателей.
    
MAPI_MH_DP_MS 
  
> Доставлено сообщение магазин вместо непосредственно получателю.
    
MAPI_MH_DP_OTHER_AU 
  
> Доставки единице доступа (AU), отличный от физических доставки доступа единицу измерения (PDAU), таких как система ФАКСОВ.
    
MAPI_MH_DP_PDAU 
  
> Доставлено единицы доступа физических доставки, например человеческого почтовый поставщика.
    
MAPI_MH_DP_PDS_PATRON 
  
> Доставлено patron физических доставки системы, такие как обычное почтовый ящик.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Доставлено агент закрытый пользователя (UA), такие как клиент внутренних почтовых систем.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Доставлено агентов пользователей общедоступных служб или поставщик услуг public.
    
Значение по умолчанию — MAPI_MH_DP_PRIVATE_UA, то есть, клиент MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

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

