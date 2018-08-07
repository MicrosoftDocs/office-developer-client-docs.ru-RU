---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Журналы входа на сайт социальной сети с помощью кэшированных учетных данных.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812756"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Журналы входа на сайт социальной сети с помощью кэшированных учетных данных.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Параметры

_connectIn_
  
> [in] Строка, которая может быть пустой или содержит учетные данные для входа, в зависимости от контекста, в котором OSC звонит **LogonCached**.
    
_userName_
  
> [in] Строка, содержащая имя пользователя.
    
_password_
  
> [in] Строка, содержащая пароль пользователя.
    
_connectOut_
  
> [out] Непрозрачную строку, содержащее учетные данные.
    
## <a name="remarks"></a>Замечания

Этот метод вызывается для проверки подлинности только в том случае, если **useLogonCached** задано **значение true** в **возможности** XML, возвращенные [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).
  
Outlook Social Connector (OSC) вызывает **LogonCached**и передает пустую строку для _connectIn_ и непустые строки _имя пользователя_ и _пароль_ . Поставщик использует _имя пользователя_ и _пароль_ для входа в социальной сети и возвращает параметр непрозрачный _connectOut_ OSC, если проверка подлинности выполнена успешно. Если происходит сбой проверки подлинности, поставщик возвращает ошибку OSC_E_LOGON_FAILURE для OSC. 
  
Параметр _connectOut_ представляет собой непрозрачную строку для OSC и передается параметр _connectIn_ в последующих попыток с OSC войти в социальных сетях. Поставщик следует поместить все учетные данные в строку _connectOut_ , предоставляющей OSC для хранения через подключения. OSC не распознает строку в _connectOut_и зашифровывает строку в целях безопасности перед его сохранения в реестре Windows.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

