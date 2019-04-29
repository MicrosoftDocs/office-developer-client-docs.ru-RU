---
title: ИсоЦиалсессионфолловперсон
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

Параметр _EmailAddress_ должен быть ДОПУСТИМЫМ SMTP-адресом. Если поставщик Outlook Social Connector (OSC) установил для метода **фолловперсон** **значение true** в функциях ****, а аргумент для _EmailAddress_ не соответствует пользователю в сети, поставщик должен возвратить оск_е_нот_фаунд ошибкой. Если у поставщика для **фолловперсон** задано **значение false** в возможностях, поставщик должен возвратить ошибку оск_е_фаил. ****
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и присвоить свойству **фолловперсон** **значение true** в возможностях, OSC вызывает [ISocialSession2:: фолловперсонекс](isocialsession2-followpersonex.md) вместо **** **настроенный ISocialSession:: фолловперсон **. Если поставщик не реализует интерфейс **ISocialSession2** , или **ISocialSession2:: фолловперсонекс** возвращает сообщение об ошибке Оск_е_нотимпл, OSC вызывает **настроенный ISocialSession:: фолловперсон** , если для поставщика задано значение ** Фолловперсон** **имеет значение true** в возможностях. **** Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
Принимая решение о том, следует ли реализовать **исокалсессион:: фолловперсон** или **ISocialSession2:: фолловперсонекс**, следует определить, требуются ли поставщику другие методы в **ISocialSession2**, а также можно ли использовать _ параметр Джсплайнаме_ в **фолловперсонекс**.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

