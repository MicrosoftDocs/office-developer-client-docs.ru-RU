---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Добавляет пользователя, заданного параметром emailAddress, в качестве друга во время входа пользователя в социальной сети.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423260"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Добавляет пользователя, заданного  _параметром emailAddress,_ в качестве друга во время входа пользователя в социальной сети. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Параметры

_emailAddress_
  
> [in] Строка, содержаная адрес электронной почты человека.
    
## <a name="remarks"></a>Примечания

Параметр  _emailAddress_ должен быть допустимым SMTP-адресом. Если поставщик Outlook Social Connector (OSC) установил в  возможностях метод **followPerson** как **true,** а аргумент _emailAddress_ не совпадает с пользователем в сети, поставщик должен вернуть OSC_E_NOT_FOUND ошибку. Если поставщик установил в возможностях **followPerson** как **false,** поставщик должен вернуть OSC_E_FAIL ошибку. 
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил для  **followPerson** в качестве true **возможности,** OSC будет вызывать [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо **ISocialSession::FollowPerson**. Если поставщик не реализует интерфейс **ISocialSession2** или **ISocialSession2::FollowPersonEx** возвращает ошибку OSC_E_NOTIMPL, OSC будет вызывать **ISocialSession::FollowPerson,** если поставщик установил **followPerson** как **true** в **возможностях**. Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
При принятии решения о внедрении **ISocalSession::FollowPerson** или **ISocialSession2::FollowPersonEx** следует учесть, нужны ли поставщику другие методы **в ISocialSession2** и можно ли использовать параметр  _djsplayName_ в **FollowPersonEx**.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

