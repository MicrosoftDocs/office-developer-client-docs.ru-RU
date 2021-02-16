---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: Возвращает строку, представляюную ИД пользователя в социальной сети, который в данный момент вошел в систему.
ms.openlocfilehash: edb61569829f7690c2284a083d2cbd5cfe2d32a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413572"
---
# <a name="isocialsessionloggedonuserid"></a>ISocialSession::LoggedOnUserID

Возвращает строку, представляюную ИД пользователя в социальной сети, который в данный момент вошел в систему. 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a>Значение свойства

Строка, содержаная ИД пользователя социальной сети во время входа в систему.
  
## <a name="see-also"></a>См. также

- [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)  
- [ISocialSession : IUnknown](isocialsessioniunknown.md)

