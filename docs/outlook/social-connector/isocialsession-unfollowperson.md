---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Удаляет лица, указанного с помощью параметра userID как friend в социальных сетях.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812750"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Удаляет лица, указанного с помощью параметра _userID_ как friend в социальных сетях. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameters

_идентификатор пользователя_
  
> [in] Строка, содержащая идентификатор пользователя социальной сети для пользователя.
    
## <a name="remarks"></a>Замечания

Параметр _идентификатор пользователя_ должен быть действительный ID пользователя для пользователя в социальных сетях. 
  
Если поставщик Outlook Social Connector (OSC) значение **doNotFollowPerson** как **true** в XML-КОДЕ для **возможностей**, поставщик должен возвращать ошибку OSC_E_NOT_FOUND в случае пользователя, переданный код не соответствует пользователя в сети. Если поставщик значение **doNotFollowPerson** **значение false** в **возможности**, поставщик должен возвращать ошибку OSC_E_FAIL. Сведения о кодах ошибок см в [Outlook Social Connector коды ошибок для поставщика](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

