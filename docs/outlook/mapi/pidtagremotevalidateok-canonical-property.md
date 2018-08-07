---
title: Каноническое свойство PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811704"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Каноническое свойство PidTagRemoteValidateOk

  
  
**Относится к**: Outlook 
  
Это свойство содержит значение TRUE, если удаленного просмотра может вызвать метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Идентификатор:  <br/> |0x3E0D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство отображается в таблице состояния и предлагает управлять производительности транспорта. Его можно рассматривать как другим способом направления удаленного просмотра для бездействующих. Если он имеет значение TRUE, средство просмотра удаленных можно вызвать **IMAPIStatus::ValidateState** необходимое. Значение FALSE указывает, что средство просмотра удаленных не может выполнять любые дополнительные вызовы. 
  
Поставщика транспорта обычно этому свойству динамически, задав значение FALSE, чтобы отключить дополнительные вызовы, когда поставщика транспорта имеет достаточные объем обработки для выполнения. По завершении поставщика транспорта его устанавливает значение значение TRUE, чтобы разрешить клиентское приложение для дальнейшей **IMAPIStatus::ValidateState** вызовов. 
  
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

