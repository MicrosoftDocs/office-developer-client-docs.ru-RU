---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Добавляет пользователя, идентифицируемого параметрами emailAddresses и displayName, как Friend для вошедшего в сеть пользователя в социальной сети.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429833"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Добавляет пользователя, идентифицируемого параметрами _EmailAddresses_ и _DisplayName_ , как Friend для вошедшего в сеть пользователя в социальной сети. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Параметры

_emailAddresses_
  
> возврата Массив, содержащий один или несколько допустимых SMTP-адресов для пользователя в социальной сети.
    
_displayName_
  
> возврата Строка, содержащая отображаемое имя человека, которого требуется добавить в качестве друга.
    
## <a name="remarks"></a>Примечания

Если Outlook Social Connector (OSC) предоставляет более чем адрес SMTP в массиве параметра **EmailAddresses** , то поставщик OSC может предположить, что первый элемент является основным SMTP-адресом. 
  
Если у поставщика для элемента **фолловперсон** в XML-файле **возможностей** задано **значение true** , а ни один из элементов для _EmailAddresses_ не соответствует пользователю в сети, то поставщик должен возвратить ошибку оск_е_нот_фаунд. Если у поставщика для **фолловперсон** задано **значение false** в возможностях, поставщик должен возвратить ошибку оск_е_фаил. **** 
  
Если метод **фолловперсонекс** завершается успешно, поставщик может использовать строку в параметре _DisplayName_ , чтобы обращаться к пользователю во всех последующих сообщениях с дружественным подтверждением, а не по адресу SMTP. С другой стороны, поставщик должен уметь обрабатывать OSC, передающий пустую строку для параметра _DisplayName_ . 
  
Если поставщик реализует интерфейс [ISocialSession2](isocialsession2iunknown.md) и приСвоить **фолловперсон** значение **true** в XML-коде возможностей, то OSC вызывает **фолловперсонекс** вместо [настроенный ISocialSession:: фолловперсон](isocialsession-followperson.md). Если у поставщика задано значение **фолловперсон** , но не реализован интерфейс **ISocialSession2** , или **ФОЛЛОВПЕРСОНЕКС** возвращает ошибку оск_е_нотимпл, OSC вызывает **настроенный ISocialSession:: фолловперсон**. ****
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

