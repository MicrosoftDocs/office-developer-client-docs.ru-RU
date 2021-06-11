---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Добавляет пользователя, идентифицированного параметром emailAddress как друга для зарегистрированного пользователя в социальной сети.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423260"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Добавляет пользователя, идентифицированного  _параметром emailAddress_ как друга для зарегистрированного пользователя в социальной сети. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Parameters

_emailAddress_
  
> [in] Строка, содержаная адрес электронной почты человека.
    
## <a name="remarks"></a>Примечания

Параметр  _emailAddress_ должен быть допустимым SMTP-адресом. Если поставщик Outlook social Connector (OSC) задает метод  **followPerson** как верный в возможностях, и аргумент для _emailAddress_ не соответствует пользователю в сети, поставщик должен вернуть OSC_E_NOT_FOUND ошибку. Если поставщик установил **followPerson** как ложный в возможностях, поставщик должен вернуть OSC_E_FAIL ошибку.  
  
Если поставщик реализует [интерфейс ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** как верный в возможностях, OSC будет вызывать [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо  **ISocialSession::FollowPerperson**.  Если поставщик не реализует интерфейс **ISocialSession2** или **ISocialSession2::FollowPersonEx** возвращает ошибку OSC_E_NOTIMPL, OSC будет вызывать **ISocialSession:::FollowPerson** до тех пор, пока поставщик установил **followPerson** **как** верный в **возможностях**. Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
При принятии решения о внедрении **ISocalSession:::FollowPerson** или **ISocialSession2::FollowPersonEx** необходимо учитывать, нужны ли вашему поставщику другие методы в **ISocialSession2** и можно ли использовать параметр  _djsplayName_ в **FollowPersonEx**.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

