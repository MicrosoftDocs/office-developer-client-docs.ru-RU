---
title: Каноническое свойство PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356303"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>Каноническое свойство PidTagOriginatorDeliveryReportRequested

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если отправитель сообщения запрашивает отчет о доставке определенного получателя из системы обмена сообщениями, прежде чем сообщение будет помещено в хранилище сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Идентификатор:  <br/> |0x0023  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для управления системой обмена сообщениями при обработке доставленных сообщений. В этом случае в сообщении  также должно быть PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED[(PidTagOriginatorNonDeliveryReportRequested)](pidtagoriginatornondeliveryreportrequested-canonical-property.md)со свойством FALSE.
  
Установка свойства **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** для сообщения — это способ запроса отчетов о состоянии доставки для всех получателей. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

