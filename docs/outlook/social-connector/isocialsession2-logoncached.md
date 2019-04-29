---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Выполняет вход на сайт социальных сетей с помощью кэшированных учетных данных.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436624"
---
# <a name="isocialsession2logoncached"></a>ISocialSession2::LogonCached

Выполняет вход на сайт социальных сетей с помощью кэшированных учетных данных.
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a>Параметры

_подключение_
  
> возврата Строка, которая может быть пустой или содержать учетные данные для входа в зависимости от контекста, в котором OSC вызывает **логонкачед**.
    
_userName_
  
> возврата Строка, содержащая имя пользователя.
    
_password_
  
> возврата Строка, содержащая пароль пользователя.
    
_подключение_
  
> вышли Непрозрачная строка, содержащая учетные данные.
    
## <a name="remarks"></a>Примечания

Этот метод вызывается для проверки подлинности только в том случае, если для **уселогонкачед** задано **значение true** в XML-коде **возможностей** , возвращаемом [исоЦиалпровидер::-Capabilities](isocialprovider-getcapabilities.md).
  
Outlook Social Connector (OSC) вызывает **логонкачед**и передает пустую строку для _подключения_ и непустых строк _имени пользователя_ и _пароля_ . Поставщик использует _имя пользователя_ и _пароль_ для входа в социальную сеть и возвращает параметру непрозрачного _подключения_ к OSC, если проверка подлинности прошла успешно. Если происходит сбой проверки подлинности, поставщик возвращает ошибку ОСК_Е_ЛОГОН_ФАИЛУРЕ на OSC. 
  
Параметр _Connect_ — это непрозрачная строка для OSC и передается параметру _Connect_ при последующих попытках входа в социальНУЮ сеть с помощью OSC. Поставщик должен помещать в строку _подключения_ любые учетные данные, необходимые поставщику для хранения OSC в подключениях. OSC не интерпретирует строку в подсоединении __ и шифрует строку в целях безопасности перед ее сохранением в реестре Windows.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

