---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Идентифицирует пользователя, который может не иметь сведений о доступности данных, которые доступны.
ms.openlocfilehash: edfc9980445fcc2e111045650667d93bffa94153
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565139"
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
  
> Длина записи идентификатор пользователя почты, представленных в интерфейсе [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) . 
    
_m_lpEid_
  
> Идентификатор записи пользователя почты, представленных в интерфейсе **IMailUser** . 
    
_m_ulReserved_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_m_pwszReserved_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.
    
## <a name="see-also"></a>См. также

- [About the Free/Busy API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

