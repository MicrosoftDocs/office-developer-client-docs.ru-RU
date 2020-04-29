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
  
Содержит битовую маску флагов, указывающих методы в интерфейсе **имапистатус** , поддерживаемые объектом Status. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Идентификатор:  <br/> |0x3E02  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает, какие методы в реализации объекта Status поддерживаются в **имапистатус** . Объектам состояния разрешено возвращать MAPI_E_NO_SUPPORT из неподдерживаемых методов. 
  
Клиенты используют свойство **PR_RESOURCE_METHODS** объекта status, чтобы избежать вызовов неподдерживаемых методов. Если установлен флаг, соответствующий определенному методу, метод существует и может вызываться. Если этот флаг снят, метод не должен вызываться. 
  
Объекты состояния, реализованные MAPI, поддерживают следующие методы:
  
|**Объект Status**|**Поддерживаемые методы**|
|:-----|:-----|
|Подсистема MAPI  <br/> |Только **валидатестате**  <br/> |
|Адресная книга MAPI  <br/> |Только **валидатестате**  <br/> |
|Диспетчер очереди MAPI  <br/> |**Валидатестате** и **FlushQueues** <br/> |
   
В **PR_RESOURCE_METHODS**можно задать один или несколько из следующих флагов:
  
STATUS_CHANGE_PASSWORD 
  
> Указывает на то, что метод [имапистатус:: ChangePassword](imapistatus-changepassword.md) поддерживается. 
    
STATUS_FLUSH_QUEUES 
  
> Указывает, что поддерживается метод [имапистатус:: FlushQueues](imapistatus-flushqueues.md) . 
    
STATUS_SETTINGS_DIALOG 
  
> Указывает, что поддерживается метод [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) . 
    
STATUS_VALIDATE_STATE 
  
> Указывает, что поддерживается метод [имапистатус:: валидатестате](imapistatus-validatestate.md) . 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

