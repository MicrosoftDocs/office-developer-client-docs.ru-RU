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
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355617"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Каноническое свойство PidTagRemoteValidateOk

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит значение TRUE, если удаленному средству просмотра разрешено вызывать метод [имапистатус:: валидатестате](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕМОТЕ_ВАЛИДАТЕ_ОК  <br/> |
|Идентификатор:  <br/> |0x3E0D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство отображается в таблице состояние и предоставляет некоторый контроль над производительностью транспорта. Его можно рассматривать как другой способ, позволяющий удаленному средству просмотра переключаться в состояние простоя. Если задано значение TRUE, удаленное средство просмотра может вызывать **имапистатус:: валидатестате** как можно чаще. Значение FALSE указывает на то, что удаленное средство просмотра не может совершать другие вызовы. 
  
Поставщик транспорта обычно задает это свойство динамически, устанавливая значение FALSE, чтобы отключить дополнительные вызовы, когда у поставщика транспорта достаточно объема обработки для выполнения. После завершения работы поставщика транспорта устанавливается значение TRUE, чтобы разрешить клиентскому приложению выполнять дальнейшие **действия имапистатус:: валидатестате** Calls. 
  
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

