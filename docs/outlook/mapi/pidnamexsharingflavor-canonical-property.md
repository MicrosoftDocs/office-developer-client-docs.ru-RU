---
title: Каноническое свойство PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392125"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>Каноническое свойство PidNameXSharingFlavor

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет значение свойства **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).
  
|||
|:-----|:-----|
|Понятные имена:  <br/> |Отсутствует  <br/> |
|Набор свойств:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Имя свойства:  <br/> |Общий доступ к конфигурация X  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Замечания

Свойство **dispidSharingFlavor** должно быть одно из следующих значений. 
  
|**Значение**|**Тип общего доступа к сообщения**|
|:-----|:-----|
|0x00020310  <br/> |Приглашения на общий доступ для отдельной папки.  <br/> |
|0x00000310  <br/> |Приглашения на общий доступ к папке, которая не является отдельной папки.  <br/> |
|0x00020500  <br/> |Запрос на общий доступ.  <br/> |
|0x00020710  <br/> |Оба приглашения на общий доступ для отдельной папки и запрос на общий доступ для получателя соответствует специальную папку.  <br/> |
|0x00025100  <br/> |Ответ общего доступа, не дает запрос.  <br/> |
|0x00023310  <br/> |Ответ общего доступа, который принимает запрос (также тип приглашение для совместного использования).  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Открывает общий доступ папки почтовых ящиков между клиентами.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

