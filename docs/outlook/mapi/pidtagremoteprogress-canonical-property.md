---
title: Каноническое свойство PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569353"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Каноническое свойство PidTagRemoteProgress

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит число, указывающее состояние удаленной передачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Идентификатор:  <br/> |0x3E0B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Если передача не находится в стадии разработки, это свойство необходимо задать значение 1. При передаче находится в стадии разработки, оно должно быть присвоено значение от 0 до 100, указывающее процент завершения переноса.
  
Текст, связанный с кодом числовое состояние отображается в свойстве **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Следующие флаги можно задать для этого свойства:
  
MSGSTATUS_REMOTE_DELETE
  
> Передача сообщений будет удален.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Передача сообщений находится в стадии разработки.
    
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

