---
title: ИсоЦиалсессионлогон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Выполняет вход на сайт социальных сетей с использованием указанных имени пользователя и пароля.
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361042"
---
# <a name="isocialsessionlogon"></a><span data-ttu-id="f121c-103">ISocialSession::Logon</span><span class="sxs-lookup"><span data-stu-id="f121c-103">ISocialSession::Logon</span></span>

<span data-ttu-id="f121c-104">Выполняет вход на сайт социальных сетей с использованием указанных имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="f121c-104">Logs on to the social network site by using the specified user name and password.</span></span>
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a><span data-ttu-id="f121c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f121c-105">Parameters</span></span>

<span data-ttu-id="f121c-106">_имя пользователя_</span><span class="sxs-lookup"><span data-stu-id="f121c-106">_username_</span></span>
  
> <span data-ttu-id="f121c-107">возврата Строка, содержащая имя пользователя для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="f121c-107">[in] A string that contains the user name to log on.</span></span>
    
<span data-ttu-id="f121c-108">_Ввод_</span><span class="sxs-lookup"><span data-stu-id="f121c-108">_password_</span></span>
  
> <span data-ttu-id="f121c-109">возврата Строка, содержащая пароль для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="f121c-109">[in] A string that contains the password to log on.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f121c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f121c-110">See also</span></span>

- [<span data-ttu-id="f121c-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f121c-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

