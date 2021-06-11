---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Удаляет пользователя, идентифицированного параметром userID в качестве друга в социальной сети.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418437"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Удаляет пользователя, идентифицированного  _параметром userID_ в качестве друга в социальной сети. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Parameters

_userID_
  
> [in] Строка, которая содержит ID пользователя социальной сети для человека.
    
## <a name="remarks"></a>Примечания

Параметр  _userID_ должен быть действительным удостоверением пользователя для пользователя в социальной сети. 
  
Если поставщик Outlook social Connector (OSC) задает **doNotFollowPerson** как true в XML для **возможностей,** поставщик должен вернуть OSC_E_NOT_FOUND ошибку в случае, если пользовательский ID, переданный, не соответствует пользователю в сети.  Если поставщик установил **doNotFollowPerson** как ложный в возможностях, поставщик должен вернуть OSC_E_FAIL ошибку.   Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

