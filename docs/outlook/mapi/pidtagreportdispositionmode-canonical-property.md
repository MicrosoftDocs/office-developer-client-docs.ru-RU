---
title: Каноническое свойство PidTagReportDispositionMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d598337a4a66b6345b2f7c827b62a2ccd8af366
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428972"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a>Каноническое свойство PidTagReportDispositionMode

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает расположение квитанции для сообщений, запрашивает квитанции. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W  <br/> |
|Идентификатор:  <br/> |0x0081  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Возможные значения для этого свойства : "вручную-действие/MDN-sent-automatically" и "ручное действие/MDN-sent-manually".
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
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

