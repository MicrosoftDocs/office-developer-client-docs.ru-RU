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
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439424"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Каноническое свойство PidTagDeliveryPoint

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает природу функциональной сущности, с помощью которой сообщение было или было доставлено получателю. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELIVERY_POINT  <br/> |
|Идентификатор:  <br/> |0x0C07  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь одно из следующих значений: 
  
MAPI_MH_DP_ML 
  
> Доставленная в список рассылки точка доставки, которая, в свою очередь, может распространять сообщение среди многих получателей.
    
MAPI_MH_DP_MS 
  
> Доставляется в хранилище сообщений, а не непосредственно получателю.
    
MAPI_MH_DP_OTHER_AU 
  
> Доставляется в единицу доступа (AU), за исключением физического блока доступа к доставке (PDAU), например в систему факсимилов.
    
MAPI_MH_DP_PDAU 
  
> Доставляется в физическое подразделение доступа к доставке, например к почтовому оператору.
    
MAPI_MH_DP_PDS_PATRON 
  
> Доставляется в физический клиент системы доставки, например обычный почтовый ящик.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Доставляется частному агенту пользователей (UA), например клиенту в системе обмена сообщениями.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Доставлено агенту общедоступных пользователей или поставщику общедоступных услуг.
    
По умолчанию значение MAPI_MH_DP_PRIVATE_UA, то есть клиент MAPI. 
  
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

