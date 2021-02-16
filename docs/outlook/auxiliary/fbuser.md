---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Определяет пользователя, у которого могут быть или недоступны сведения о занятости.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317663"
---
# <a name="fbuser"></a>FBUser

Определяет пользователя, у которого могут быть или недоступны сведения о занятости.
  
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

## <a name="members"></a>Элементы

_m_cbEid_
  
> Длина ИД записи пользователя почты, представленная интерфейсом [IMailUser.](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) 
    
_m_lpEid_
  
> ИД записи пользователя почты, представленный **интерфейсом IMailUser.** 
    
_m_ulReserved_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_m_pwszReserved_
  
> Этот параметр зарезервирован для внутреннего использования Outlook и не поддерживается.
    
## <a name="see-also"></a>См. также

- [О доступности API](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

