---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Входит на сайт социальной сети с использованием проверки подлинности на основе форм.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430338"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Входит на сайт социальной сети с использованием проверки подлинности на основе форм.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Параметры

_connectIn_
  
> [in] Строка, которая имеет **null,** URL-адрес формы входа в Интернет или строку, содержаную учетные данные для входа, в зависимости от контекста процесса входа, когда этот метод вызван.
    
_connectOut_
  
> [out] Строка, содержаная учетные данные для входа.
    
## <a name="remarks"></a>Примечания

Outlook Social Connector (OSC) вызывает метод **LogonWeb,** только если поставщик указывает, что он поддерживает проверку подлинности на основе форм. Поставщик указывает, что ему требуется проверка подлинности на основе форм,  задав для использования **параметра useLogonWebAuth** в XML **для возможностей.** Если поставщик задает **для useLogonWebAuth** **false,** OSC использует базовую проверку подлинности и вызывает метод [ISocialSession::Logon.](isocialsession-logon.md) 
  
Вход на сайт социальной сети с использованием проверки подлинности на основе форм включает вызов методов **LogonWeb** и [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) в определенном порядке: 
  
1. OsC вызывает **LogonWeb** в первый раз, передавая **null** _параметру connectIn._ 
    
2. Поставщик вызывает ошибку OSC_E_AUTH_ERROR osc.
    
3. Затем OSC вызывает **GetLogonUrl.**
    
4. Поставщик возвращает соответствующий URL-адрес страницы для логотипа в **методе GetLogonUrl.** 
    
5. OsC использует URL-адрес, возвращенный **GetLogonUrl,** для отображения страницы для логотипа на основе форм. 
    
6. Затем OSC вызывает **LogonWeb** второй раз, передавая URL-адрес в форму для логотипа в _параметре connectIn._ 
    
7. В случае успешной проверки подлинности поставщик возвращает учетные данные для входа в параметр  _connectOut_ в OSC. Если проверка подлинности не удаться, поставщик OSC_E_AUTH_ERROR ошибку osc. 
    
Если поставщик OSC поддерживает вход в систему с использованием кэшных учетных данных,  он указывает в XML-разных возможностях **метод useLogonCached** как **true.** Поставщик должен разместить учетные данные для входа в строку  _connectOut,_ которую поставщик хочет сохранить в разных подключениях. OsC не интерпретирует _строку connectOut._ После того как OSC проверяет правильность **использованияLogonCached,** OSC шифрует строку для обеспечения безопасности перед сохранением ее в реестре Windows.  OSC передает эту строку _параметру connectIn_ при последующих попытках входа в социальные сети путем вызова [ISocialSession2::LogonCached.](isocialsession2-logoncached.md) 
  
Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Проверка подлинности на основе форм](forms-based-authentication.md)

