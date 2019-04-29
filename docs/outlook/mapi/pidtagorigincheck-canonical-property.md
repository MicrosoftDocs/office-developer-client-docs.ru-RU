---
title: Каноническое свойство PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435763"
---
# <a name="pidtagorigincheck-canonical-property"></a>Каноническое свойство PidTagOriginCheck

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит двоичное значение проверки, позволяющее получателю отчета о доставке проверять происхождение исходного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ОРИГИН_ЧЕКК  <br/> |
|Идентификатор:  <br/> |0x0027  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет средства для третьей стороны, например агента передачи сообщений (MTA) или пользователя обмена сообщениями, получающего отчет о доставке, для проверки источника отправленного сообщения. При наличии в полученном сообщении это свойство должно быть скопировано в отчет о доставке, созданный в ответ на сообщение.
  
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

