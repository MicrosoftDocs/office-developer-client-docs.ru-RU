---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Журналы входа на сайт социальной сети с помощью проверки подлинности на основе форм.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812749"
---
# <a name="isocialsessionlogonweb"></a>ISocialSession::LogonWeb

Журналы входа на сайт социальной сети с помощью проверки подлинности на основе форм.
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a>Параметры

_connectIn_
  
> [in] Строка, которая имеет **значение null**, URL-адрес в форму входа в систему на веб-сайте или строка, содержащая учетные данные для входа, в зависимости от контекста в процесс входа при вызове этого метода.
    
_connectOut_
  
> [out] Строка, содержащая учетные данные для входа.
    
## <a name="remarks"></a>Замечания

Outlook Social Connector (OSC) вызывает метод **LogonWeb** только в том случае, если поставщик указывает, что он поддерживает проверку подлинности на основе форм. Поставщик указывает необходимость проверки подлинности на основе форм, задав **useLogonWebAuth** как **true** в XML-КОДЕ для **возможностей**. Если поставщик устанавливает **useLogonWebAuth** **значение false**, OSC используется обычная проверка подлинности и вызывает метод [ISocialSession::Logon](isocialsession-logon.md) . 
  
Входа на сайт социальной сети с помощью проверки подлинности на основе форм включает в себя вызов методов **LogonWeb** и [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) в определенном порядке: 
  
1. OSC **LogonWeb** вызывает первый раз при передаче **значения null** параметр _connectIn_ . 
    
2. Поставщик сообщает об ошибках OSC_E_AUTH_ERROR для OSC.
    
3. Во-вторых, OSC вызывает **GetLogonUrl**.
    
4. Поставщик возвращает нужный URL-адрес на страницу входа в метод **GetLogonUrl** . 
    
5. OSC URL-адреса, возвращенные **GetLogonUrl** используется для отображения страницы входа в систему на основе форм. 
    
6. OSC вызывает **LogonWeb** еще раз, передача URL-адрес в форме входа в систему с помощью параметра _connectIn_ . 
    
7. Если проверка подлинности прошла успешно, поставщик возвращает учетные данные для входа с помощью параметра _connectOut_ OSC. Если происходит сбой проверки подлинности, поставщик вызывает ошибку OSC_E_AUTH_ERROR для OSC. 
    
Если поставщика OSC поддерживает вход в систему с использованием кэшированных учетных данных, он указывает **useLogonCached** **значение true** в **возможности** XML. Поставщик следует поместить все учетные данные для входа в строку _connectOut_ , предоставляющей OSC для хранения через подключения. OSC не распознает _connectOut_ строку. После OSC подтверждает, что этот **useLogonCached** имеет **значение true**, OSC шифрует строку для безопасности перед его сохранения в реестре Windows. OSC передает эта строка для параметра _connectIn_ на последующих попыток входа в систему в социальных сетях вызовом [ISocialSession2::LogonCached](isocialsession2-logoncached.md). 
  
Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)
- [Проверка подлинности на основе форм](forms-based-authentication.md)

