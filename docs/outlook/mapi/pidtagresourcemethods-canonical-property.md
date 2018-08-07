---
title: Каноническое свойство PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811719"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Каноническое свойство PidTagResourceMethods

  
  
**Относится к**: Outlook 
  
Содержит битовую маску флагов, которые указывают методы в интерфейсе **IMAPIStatus** , поддерживаемых приложением объект состояния. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Идентификатор:  <br/> |0x3E02  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство указывает, какой из методов в реализации объектом состояние **IMAPIStatus** поддерживаются. Объекты состояния могут возвращать MAPI_E_NO_SUPPORT из методов не поддерживается. 
  
Клиенты используют свойство **PR_RESOURCE_METHODS** объекта состояния во избежание вызов методов не поддерживается. Если установлен флаг, соответствующий определенного метода, метод существует и могут вызываться. Если этот флажок снят, метод не должен вызываться. 
  
Объекты состояния реализован MAPI поддержки следующих методов:
  
|**Состояние объекта**|**Поддерживаемые методы**|
|:-----|:-----|
|Подсистема MAPI  <br/> |Только **ValidateState**  <br/> |
|Адресная книга MAPI  <br/> |Только **ValidateState**  <br/> |
|Диспетчер очереди MAPI  <br/> |**ValidateState** и **FlushQueues** <br/> |
   
Один или несколько из следующих флагов может быть установлено в **PR_RESOURCE_METHODS**:
  
STATUS_CHANGE_PASSWORD 
  
> Указывает, что поддерживается метод [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) . 
    
STATUS_FLUSH_QUEUES 
  
> Указывает, что поддерживается метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) . 
    
STATUS_SETTINGS_DIALOG 
  
> Указывает, что поддерживается метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) . 
    
STATUS_VALIDATE_STATE 
  
> Указывает, что поддерживается метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

