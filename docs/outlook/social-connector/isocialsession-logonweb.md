---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Войдите на сайт социальной сети с помощью проверки подлинности на основе форм.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430338"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Войдите на сайт социальной сети с помощью проверки подлинности на основе форм.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Parameters

_connectIn_
  
> [in] Строка **null**, URL-адрес формы логотипа в Интернете или строка, содержаная учетные данные логотипа, в зависимости от контекста процесса логона при назвав этот метод.
    
_connectOut_
  
> [вышел] Строка, содержаная учетные данные с логотипом.
    
## <a name="remarks"></a>Примечания

Социальный соединитатель Outlook (OSC) вызывает метод **LogonWeb** только в том случае, если поставщик указывает, что он поддерживает проверку подлинности на основе форм. Поставщик указывает, что для этого требуется проверка подлинности на основе форм, задав **параметр useLogonWebAuth** как true **в** XML для **возможностей.** Если поставщик задает **использованиеLogonWebAuth** как **ложное,** OSC использует базовую проверку подлинности и вызывает [метод ISocialSession::Logon.](isocialsession-logon.md) 
  
Вход на сайт социальной сети с помощью проверки подлинности на основе форм включает вызов методов **LogonWeb** и [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) в определенном порядке: 
  
1. OsC вызывает **LogonWeb** в первый раз, передав **null** _параметру connectIn._ 
    
2. Поставщик повышает OSC_E_AUTH_ERROR ошибку в OSC.
    
3. Далее OSC вызывает **GetLogonUrl**.
    
4. Поставщик возвращает соответствующий URL-адрес на страницу logon в **методе GetLogonUrl.** 
    
5. OsC использует URL-адрес, возвращенный **GetLogonUrl** для отображения страницы логотипа на основе форм. 
    
6. Затем OSC вызывает **LogonWeb** во второй раз, передав URL-адрес в форму логотипа в _параметре connectIn._ 
    
7. Если проверка подлинности будет успешной, поставщик возвращает учетные данные с логотипом в  _параметре connectOut_ в OSC. Если проверка подлинности не удается, поставщик повышает OSC_E_AUTH_ERROR ошибку в OSC. 
    
Если поставщик OSC поддерживает ведение журнала с помощью кэшных учетных данных,  он указывает, что **useLogonCached** является верным в возможностях **XML.** Поставщик должен разместить все учетные данные с логотипом в строке  _connectOut,_ которую поставщик хочет, чтобы OSC хранился в подключениях. OsC не интерпретирует _строку connectOut._ После проверки osC, которая **используетLogonCached,** это **верно,** OSC шифрует строку для безопасности, прежде чем хранить ее в Windows реестре. OsC передает эту строку  _параметру connectIn_ при последующих попытках войти в социальную сеть по вызову [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Проверка подлинности на основе форм](forms-based-authentication.md)

