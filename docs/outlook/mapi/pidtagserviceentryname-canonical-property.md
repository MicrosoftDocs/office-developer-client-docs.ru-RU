---
title: Каноническое свойство PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811904"
---
# <a name="pidtagserviceentryname-canonical-property"></a>Каноническое свойство PidTagServiceEntryName

  
  
**Относится к**: Outlook 
  
Содержит имя функции точки входа для конфигурации службы сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|Идентификатор:  <br/> |0x3D0B  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется специалистов по внедрению службы сообщений предоставляют точка входа службы сообщение, что точка входа не является обязательным. Тем не менее точка входа должен задаваться только в том случае, если существует связанных с ними конфигурационные свойства. Если эти свойства не существует, MAPI предполагает, что точка входа не предоставляется.
  
Библиотека динамической компоновки (DLL), в котором содержится функция точки входа называется свойством **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).
  
Дополнительные сведения о точки входа службы сообщений [реализации функции точки входа поставщика службы](implementing-a-service-provider-entry-point-function.md)см.
  
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

