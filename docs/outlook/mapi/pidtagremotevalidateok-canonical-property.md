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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424226"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Каноническое свойство PidTagRemoteValidateOk

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит true, если удаленному просмотру разрешено вызывать метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Идентификатор:  <br/> |0x3E0D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство отображается в таблице состояния и обеспечивает некоторый контроль над производительностью транспорта. Его можно рассматривать как еще один способ перенаправки удаленного просмотра в режим простоя. Если установлено true, удаленный просмотр может вызывать **IMAPIStatus::ValidateState** как можно чаще. Значение FALSE указывает на то, что удаленное представление больше не может делать вызовы. 
  
Поставщик транспорта обычно динамически задает это свойство, установив значение FALSE, чтобы отключить дополнительные вызовы, если у поставщика транспорта достаточно объема обработки для выполнения. После завершения работы поставщика транспорта он устанавливает значение TRUE, чтобы разрешить клиентского приложения дальнейшие **вызовы IMAPIStatus::ValidateState.** 
  
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

