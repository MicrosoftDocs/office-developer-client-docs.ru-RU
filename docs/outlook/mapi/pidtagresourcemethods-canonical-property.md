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
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436337"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Каноническое свойство PidTagResourceMethods

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовуюmask флагов, которые указывают методы в **интерфейсе IMAPIStatus,** поддерживаемые объектом состояния. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Идентификатор:  <br/> |0x3E02  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает, какие методы в реализации **объекта состояния IMAPIStatus** поддерживаются. Объекты состояния могут возвращать MAPI_E_NO_SUPPORT из неподтверченных методов. 
  
Клиенты используют свойство PR_RESOURCE_METHODS **состояния,** чтобы избежать вызовов неподтверченных методов. Если установлен флаг, соответствующий конкретному методу, метод существует и может быть вызван. Если этот флаг понятен, метод не должен быть вызван. 
  
Объекты состояния, реализованные с помощью MAPI, поддерживают следующие методы:
  
|**Объект Status**|**Поддерживаемые методы**|
|:-----|:-----|
|Подсистема MAPI  <br/> |**Только ValidateState**  <br/> |
|Адресная книга MAPI  <br/> |**Только ValidateState**  <br/> |
|MapI spooler  <br/> |**ValidateState** и **FlushQueues** <br/> |
   
Один или несколько из следующих флагов можно установить в **PR_RESOURCE_METHODS:**
  
STATUS_CHANGE_PASSWORD 
  
> Указывает, что метод [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) поддерживается. 
    
STATUS_FLUSH_QUEUES 
  
> Указывает, что метод [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) поддерживается. 
    
STATUS_SETTINGS_DIALOG 
  
> Указывает, что метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) поддерживается. 
    
STATUS_VALIDATE_STATE 
  
> Указывает, что метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) поддерживается. 
    
## <a name="related-resources"></a>Связанные ресурсы

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

