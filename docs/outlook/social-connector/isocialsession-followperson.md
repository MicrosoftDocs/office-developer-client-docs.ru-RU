---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Добавляет пользователя, определенного параметром emailAddress как friend для пользователя при входе в социальных сетях.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812741"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

Добавляет пользователя, определенного параметром _emailAddress_ как friend для пользователя при входе в социальных сетях. 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>Параметры

_emailAddress_
  
> [in] Строка, содержащая адрес электронной почты пользователя.
    
## <a name="remarks"></a>Замечания

Параметр _emailAddress_ должен быть допустимым адресом SMTP. Если аргумент для _emailAddress_ не соответствует пользователя в сети поставщика Outlook Social Connector (OSC) Выбор метода **followPerson** **значение true** в **возможности**, поставщик должен возвращать OSC_E_NOT_FOUND Ошибка. Если поставщик значение **followPerson** **значение false** в **возможности**, поставщик должен возвращать ошибку OSC_E_FAIL.
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и установил **followPerson** **значение true** в **возможности**, OSC выполняется звонок [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо **ISocialSession::FollowPerson **. Если поставщик не реализует интерфейс **ISocialSession2** или **ISocialSession2::FollowPersonEx** возвращает OSC_E_NOTIMPL ошибка, OSC выполняется звонок **ISocialSession::FollowPerson** до тех пор, пока поставщик установил ** followPerson** как **true** в **возможности**. Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
В решение о ли для реализации **ISocalSession::FollowPerson** или **ISocialSession2::FollowPersonEx**, следует ли поставщик должен другие методы в **ISocialSession2**и ли вы можете использовать _ djsplayName_ параметр в **FollowPersonEx**.
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

