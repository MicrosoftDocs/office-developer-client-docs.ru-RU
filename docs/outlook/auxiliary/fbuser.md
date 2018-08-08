---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Идентифицирует пользователя, который может не иметь сведений о доступности данных, которые доступны.
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807684"
---
# <a name="fbuser"></a>FBUser

Идентифицирует пользователя, который может не иметь сведений о доступности данных, которые доступны.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a>Members

_m_cbEid_
  
> Длина записи идентификатор пользователя почты, представленных в интерфейсе [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx) . 
    
_m_lpEid_
  
> Идентификатор записи пользователя почты, представленных в интерфейсе **IMailUser** . 
    
_m_ulReserved_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_m_pwszReserved_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.
    
## <a name="see-also"></a>См. также

- [About the Free/Busy API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

