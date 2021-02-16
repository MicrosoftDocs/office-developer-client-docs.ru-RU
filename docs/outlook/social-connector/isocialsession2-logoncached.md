---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Войдите на сайт социальной сети с помощью кэшных учетных данных.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436624"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Войдите на сайт социальной сети с помощью кэшных учетных данных.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Параметры

_connectIn_
  
> [in] Строка, которая может быть пустой или содержит учетные данные для входа, в зависимости от контекста, в котором OSC вызывает **LogonCached.**
    
_userName_
  
> [in] Строка, содержаная имя пользователя.
    
_password_
  
> [in] Строка, содержаная пароль пользователя.
    
_connectOut_
  
> [out] Непрозрачной строки, которая содержит учетные данные.
    
## <a name="remarks"></a>Примечания

Этот метод используется для проверки подлинности, только если  **для useLogonCached** установлено true в **XML** возможностей, возвращаемом [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)
  
Outlook Social Connector (OSC) вызывает **LogonCached** и передает пустую строку _для connectIn_ и непустых строк _userName_ и _password._ Поставщик использует _имя пользователя_ и пароль для входа в социальные сети и возвращает непрозрачные _параметры connectOut_ в OSC, если проверка подлинности будет успешной.  Если проверка подлинности не удалась, поставщик возвращает OSC_E_LOGON_FAILURE ошибку в OSC. 
  
Параметр  _connectOut_ является непрозрачной строкой в OSC и передается  _параметру connectIn_ при последующих попытках OSC войти в социальные сети. Поставщик должен разместить все учетные данные в  _строке connectOut,_ которую поставщик хочет сохранить в osC между подключениями. OsC не интерпретирует строку в  _connectOut_ и шифрует строку в целях безопасности перед ее сохранением в реестре Windows.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

