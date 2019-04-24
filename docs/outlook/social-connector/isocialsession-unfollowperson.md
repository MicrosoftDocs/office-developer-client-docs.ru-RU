---
title: ИсоЦиалсессионунфолловперсон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Удаляет пользователя, определенного параметром userID, в качестве друга в социальной сети.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336780"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

Удаляет пользователя, определенного параметром _UserID_ , в качестве друга в социальной сети. 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>Параметры

_userID_
  
> возврата Строка, содержащая идентификатор пользователя социальной сети для человека.
    
## <a name="remarks"></a>Комментарии

Параметр _UserID_ должен быть ДОПУСТИМЫм идентификатором пользователя для пользователя в социальной сети. 
  
Если у поставщика Outlook Social Connector (OSC) для **возможностей**XML задано **значение** **донотфолловперсон** , поставщик должен возвратить ошибку оск_е_нот_фаунд в том случае, если переданный идентификатор пользователя не соответствует пользователю в сети. Если у поставщика для **донотфолловперсон** задано **значение false** в возможностях, поставщик должен возвратить ошибку оск_е_фаил. **** Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

