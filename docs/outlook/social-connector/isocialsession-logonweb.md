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
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="86cdd-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="86cdd-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="86cdd-104">Войдите на сайт социальной сети с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="86cdd-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="86cdd-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="86cdd-105">Parameters</span></span>

<span data-ttu-id="86cdd-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="86cdd-106">_connectIn_</span></span>
  
> <span data-ttu-id="86cdd-107">[in] Строка **null**, URL-адрес формы логотипа в Интернете или строка, содержаная учетные данные логотипа, в зависимости от контекста процесса логона при назвав этот метод.</span><span class="sxs-lookup"><span data-stu-id="86cdd-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="86cdd-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="86cdd-108">_connectOut_</span></span>
  
> <span data-ttu-id="86cdd-109">[вышел] Строка, содержаная учетные данные с логотипом.</span><span class="sxs-lookup"><span data-stu-id="86cdd-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86cdd-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="86cdd-110">Remarks</span></span>

<span data-ttu-id="86cdd-111">Социальный соединитатель Outlook (OSC) вызывает метод **LogonWeb** только в том случае, если поставщик указывает, что он поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="86cdd-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="86cdd-112">Поставщик указывает, что для этого требуется проверка подлинности на основе форм, задав **параметр useLogonWebAuth** как true **в** XML для **возможностей.**</span><span class="sxs-lookup"><span data-stu-id="86cdd-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="86cdd-113">Если поставщик задает **использованиеLogonWebAuth** как **ложное,** OSC использует базовую проверку подлинности и вызывает [метод ISocialSession::Logon.](isocialsession-logon.md)</span><span class="sxs-lookup"><span data-stu-id="86cdd-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="86cdd-114">Вход на сайт социальной сети с помощью проверки подлинности на основе форм включает вызов методов **LogonWeb** и [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) в определенном порядке:</span><span class="sxs-lookup"><span data-stu-id="86cdd-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="86cdd-115">OsC вызывает **LogonWeb** в первый раз, передав **null** _параметру connectIn._</span><span class="sxs-lookup"><span data-stu-id="86cdd-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="86cdd-116">Поставщик повышает OSC_E_AUTH_ERROR ошибку в OSC.</span><span class="sxs-lookup"><span data-stu-id="86cdd-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="86cdd-117">Далее OSC вызывает **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="86cdd-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="86cdd-118">Поставщик возвращает соответствующий URL-адрес на страницу logon в **методе GetLogonUrl.**</span><span class="sxs-lookup"><span data-stu-id="86cdd-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="86cdd-119">OsC использует URL-адрес, возвращенный **GetLogonUrl** для отображения страницы логотипа на основе форм.</span><span class="sxs-lookup"><span data-stu-id="86cdd-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="86cdd-120">Затем OSC вызывает **LogonWeb** во второй раз, передав URL-адрес в форму логотипа в _параметре connectIn._</span><span class="sxs-lookup"><span data-stu-id="86cdd-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="86cdd-121">Если проверка подлинности будет успешной, поставщик возвращает учетные данные с логотипом в  _параметре connectOut_ в OSC.</span><span class="sxs-lookup"><span data-stu-id="86cdd-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="86cdd-122">Если проверка подлинности не удается, поставщик повышает OSC_E_AUTH_ERROR ошибку в OSC.</span><span class="sxs-lookup"><span data-stu-id="86cdd-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="86cdd-123">Если поставщик OSC поддерживает ведение журнала с помощью кэшных учетных данных,  он указывает, что **useLogonCached** является верным в возможностях **XML.**</span><span class="sxs-lookup"><span data-stu-id="86cdd-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="86cdd-124">Поставщик должен разместить все учетные данные с логотипом в строке  _connectOut,_ которую поставщик хочет, чтобы OSC хранился в подключениях.</span><span class="sxs-lookup"><span data-stu-id="86cdd-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="86cdd-125">OsC не интерпретирует _строку connectOut._</span><span class="sxs-lookup"><span data-stu-id="86cdd-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="86cdd-126">После проверки osC, которая **используетLogonCached,** это **верно,** OSC шифрует строку для безопасности, прежде чем хранить ее в Windows реестре.</span><span class="sxs-lookup"><span data-stu-id="86cdd-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="86cdd-127">OsC передает эту строку  _параметру connectIn_ при последующих попытках войти в социальную сеть по вызову [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="86cdd-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="86cdd-128">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="86cdd-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86cdd-129">См. также</span><span class="sxs-lookup"><span data-stu-id="86cdd-129">See also</span></span>

- [<span data-ttu-id="86cdd-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86cdd-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="86cdd-131">Проверка подлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="86cdd-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

