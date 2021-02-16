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
  
Содержит двоичное значение проверки, которое позволяет получателю отчета о доставке проверить происхождение исходного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Идентификатор:  <br/> |0x0027  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет сторонним пользователям, например агенту передачи сообщений (MTA) или пользователю сообщения, получиваму отчет о доставке, для проверки источника отправленного сообщения. Если присутствует в полученном сообщении, это свойство следует скопировать во все отчеты о доставке, созданные в ответ на сообщение.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

