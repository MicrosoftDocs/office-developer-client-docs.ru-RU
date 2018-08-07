---
title: Каноническое свойство PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811737"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Каноническое свойство PidTagRequestedDeliveryMethod

  
  
**Относится к**: Outlook 
  
Это свойство содержит двоичные массив методы доставки (поставщиков услуг) в порядке предпочтения отправителя сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Идентификатор:  <br/> |0x0C18  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Массива, содержащихся в списке это свойство состоит из идентификаторы ASN.1 для каждого из поставщиков услуг.
  
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

