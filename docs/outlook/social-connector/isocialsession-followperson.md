---
title: исоЦиалсессионфолловперсон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Добавляет пользователя, указанного параметром emailAddress, в качестве друга для пользователя, выполнившего вход в социальной сети.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423260"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Добавляет пользователя, указанного параметром _EmailAddress_ , в качестве друга для пользователя, выполнившего вход в социальной сети. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Параметры

_emailAddress_
  
> возврата Строка, содержащая адрес электронной почты человека.
    
## <a name="remarks"></a>Примечания

Параметр _EmailAddress_ должен быть ДОПУСТИМЫМ SMTP-адресом. Если поставщик Outlook Social Connector (OSC) установил для метода **фолловперсон** **значение true** в **функциях**, а аргумент для _EmailAddress_ не соответствует пользователю в сети, то поставщик должен возвратить ошибку OSC_E_NOT_FOUND. Если поставщик установил для **фолловперсон** значение **false** в **возможностях**, поставщик должен возвратить ошибку OSC_E_FAIL.
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и присвоить свойству **фолловперсон** **значение true** в **возможностях**, OSC вызывает [ISocialSession2:: фолловперсонекс](isocialsession2-followpersonex.md) вместо **настроенный ISocialSession:: фолловперсон**. Если поставщик не реализует интерфейс **ISocialSession2** , или **ISocialSession2:: фолловперсонекс** ВОЗВРАЩАЕТ ошибку OSC_E_NOTIMPL, OSC вызывает метод **настроенный ISocialSession:: Фолловперсон** , если поставщик установил **фолловперсон** как **true** в **возможностях**. Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
Принимая решение о том, следует ли реализовать **исокалсессион:: фолловперсон** или **ISocialSession2:: фолловперсонекс**, следует определить, требуются ли поставщику другие методы в **ISocialSession2**, а также можно ли использовать параметр _джсплайнаме_ в **фолловперсонекс**.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

