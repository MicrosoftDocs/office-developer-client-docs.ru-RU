---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Вход на сайт социальной сети с помощью кэшных учетных данных.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436624"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Вход на сайт социальной сети с помощью кэшных учетных данных.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Parameters

_connectIn_
  
> [in] Строка, которая может быть пустой или содержит учетные данные логотипа, в зависимости от контекста, в котором OSC вызывает **LogonCached.**
    
_userName_
  
> [in] Строка с именем пользователя.
    
_password_
  
> [in] Строка, содержаная пароль пользователя.
    
_connectOut_
  
> [вышел] Непрозрачной строки, которая содержит учетные данные.
    
## <a name="remarks"></a>Примечания

Этот метод вызван для проверки подлинности только в  том случае, если **useLogonCached** установлен как верный в возможностях **XML,** возвращенных [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)
  
Социальный соединитатель Outlook (OSC) вызывает **LogonCached** и передает пустую строку для  _connectIn_ и непустых имен пользователей и строк _паролей._ Поставщик использует _имя пользователя_ и пароль для входа в социальную сеть и возвращает непрозрачные _параметры connectOut_ в OSC, если проверка подлинности будет успешной.  Если проверка подлинности не удается, поставщик возвращает OSC_E_LOGON_FAILURE ошибку в OSC. 
  
Параметр  _connectOut_ является непрозрачной строкой в OSC и передается  _параметру connectIn_ при последующих попытках OSC войти в социальную сеть. Поставщик должен разместить все учетные данные в строке  _connectOut,_ которую поставщик хочет, чтобы OSC хранила через подключения. OsC не интерпретирует строку в _connectOut_ и шифрует строку в целях безопасности перед хранением Windows реестра.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

