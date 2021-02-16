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
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="cfd3c-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="cfd3c-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="cfd3c-104">Входит на сайт социальной сети с использованием проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="cfd3c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfd3c-105">Parameters</span></span>

<span data-ttu-id="cfd3c-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="cfd3c-106">_connectIn_</span></span>
  
> <span data-ttu-id="cfd3c-107">[in] Строка, которая имеет **null,** URL-адрес формы входа в Интернет или строку, содержаную учетные данные для входа, в зависимости от контекста процесса входа, когда этот метод вызван.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="cfd3c-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="cfd3c-108">_connectOut_</span></span>
  
> <span data-ttu-id="cfd3c-109">[out] Строка, содержаная учетные данные для входа.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cfd3c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="cfd3c-110">Remarks</span></span>

<span data-ttu-id="cfd3c-111">Outlook Social Connector (OSC) вызывает метод **LogonWeb,** только если поставщик указывает, что он поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="cfd3c-112">Поставщик указывает, что ему требуется проверка подлинности на основе форм,  задав для использования **параметра useLogonWebAuth** в XML **для возможностей.**</span><span class="sxs-lookup"><span data-stu-id="cfd3c-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="cfd3c-113">Если поставщик задает **для useLogonWebAuth** **false,** OSC использует базовую проверку подлинности и вызывает метод [ISocialSession::Logon.](isocialsession-logon.md)</span><span class="sxs-lookup"><span data-stu-id="cfd3c-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="cfd3c-114">Вход на сайт социальной сети с использованием проверки подлинности на основе форм включает вызов методов **LogonWeb** и [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) в определенном порядке:</span><span class="sxs-lookup"><span data-stu-id="cfd3c-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="cfd3c-115">OsC вызывает **LogonWeb** в первый раз, передавая **null** _параметру connectIn._</span><span class="sxs-lookup"><span data-stu-id="cfd3c-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="cfd3c-116">Поставщик вызывает ошибку OSC_E_AUTH_ERROR osc.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="cfd3c-117">Затем OSC вызывает **GetLogonUrl.**</span><span class="sxs-lookup"><span data-stu-id="cfd3c-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="cfd3c-118">Поставщик возвращает соответствующий URL-адрес страницы для логотипа в **методе GetLogonUrl.**</span><span class="sxs-lookup"><span data-stu-id="cfd3c-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="cfd3c-119">OsC использует URL-адрес, возвращенный **GetLogonUrl,** для отображения страницы для логотипа на основе форм.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="cfd3c-120">Затем OSC вызывает **LogonWeb** второй раз, передавая URL-адрес в форму для логотипа в _параметре connectIn._</span><span class="sxs-lookup"><span data-stu-id="cfd3c-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="cfd3c-121">В случае успешной проверки подлинности поставщик возвращает учетные данные для входа в параметр  _connectOut_ в OSC.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="cfd3c-122">Если проверка подлинности не удаться, поставщик OSC_E_AUTH_ERROR ошибку osc.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="cfd3c-123">Если поставщик OSC поддерживает вход в систему с использованием кэшных учетных данных,  он указывает в XML-разных возможностях **метод useLogonCached** как **true.**</span><span class="sxs-lookup"><span data-stu-id="cfd3c-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="cfd3c-124">Поставщик должен разместить учетные данные для входа в строку  _connectOut,_ которую поставщик хочет сохранить в разных подключениях.</span><span class="sxs-lookup"><span data-stu-id="cfd3c-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="cfd3c-125">OsC не интерпретирует _строку connectOut._</span><span class="sxs-lookup"><span data-stu-id="cfd3c-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="cfd3c-126">После того как OSC проверяет правильность **использованияLogonCached,** OSC шифрует строку для обеспечения безопасности перед сохранением ее в реестре Windows. </span><span class="sxs-lookup"><span data-stu-id="cfd3c-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="cfd3c-127">OSC передает эту строку _параметру connectIn_ при последующих попытках входа в социальные сети путем вызова [ISocialSession2::LogonCached.](isocialsession2-logoncached.md)</span><span class="sxs-lookup"><span data-stu-id="cfd3c-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="cfd3c-128">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cfd3c-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cfd3c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="cfd3c-129">See also</span></span>

- [<span data-ttu-id="cfd3c-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfd3c-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="cfd3c-131">Проверка подлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="cfd3c-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

