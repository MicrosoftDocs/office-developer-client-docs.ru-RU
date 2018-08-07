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
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="fa65a-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="fa65a-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="fa65a-104">Журналы входа на сайт социальной сети с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="fa65a-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="fa65a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa65a-105">Parameters</span></span>

<span data-ttu-id="fa65a-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="fa65a-106">_connectIn_</span></span>
  
> <span data-ttu-id="fa65a-107">[in] Строка, которая имеет **значение null**, URL-адрес в форму входа в систему на веб-сайте или строка, содержащая учетные данные для входа, в зависимости от контекста в процесс входа при вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="fa65a-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="fa65a-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="fa65a-108">_connectOut_</span></span>
  
> <span data-ttu-id="fa65a-109">[out] Строка, содержащая учетные данные для входа.</span><span class="sxs-lookup"><span data-stu-id="fa65a-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa65a-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="fa65a-110">Remarks</span></span>

<span data-ttu-id="fa65a-111">Outlook Social Connector (OSC) вызывает метод **LogonWeb** только в том случае, если поставщик указывает, что он поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="fa65a-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="fa65a-112">Поставщик указывает необходимость проверки подлинности на основе форм, задав **useLogonWebAuth** как **true** в XML-КОДЕ для **возможностей**.</span><span class="sxs-lookup"><span data-stu-id="fa65a-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="fa65a-113">Если поставщик устанавливает **useLogonWebAuth** **значение false**, OSC используется обычная проверка подлинности и вызывает метод [ISocialSession::Logon](isocialsession-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="fa65a-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="fa65a-114">Входа на сайт социальной сети с помощью проверки подлинности на основе форм включает в себя вызов методов **LogonWeb** и [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) в определенном порядке:</span><span class="sxs-lookup"><span data-stu-id="fa65a-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="fa65a-115">OSC **LogonWeb** вызывает первый раз при передаче **значения null** параметр _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="fa65a-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="fa65a-116">Поставщик сообщает об ошибках OSC_E_AUTH_ERROR для OSC.</span><span class="sxs-lookup"><span data-stu-id="fa65a-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="fa65a-117">Во-вторых, OSC вызывает **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="fa65a-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="fa65a-118">Поставщик возвращает нужный URL-адрес на страницу входа в метод **GetLogonUrl** .</span><span class="sxs-lookup"><span data-stu-id="fa65a-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="fa65a-119">OSC URL-адреса, возвращенные **GetLogonUrl** используется для отображения страницы входа в систему на основе форм.</span><span class="sxs-lookup"><span data-stu-id="fa65a-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="fa65a-120">OSC вызывает **LogonWeb** еще раз, передача URL-адрес в форме входа в систему с помощью параметра _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="fa65a-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="fa65a-121">Если проверка подлинности прошла успешно, поставщик возвращает учетные данные для входа с помощью параметра _connectOut_ OSC.</span><span class="sxs-lookup"><span data-stu-id="fa65a-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="fa65a-122">Если происходит сбой проверки подлинности, поставщик вызывает ошибку OSC_E_AUTH_ERROR для OSC.</span><span class="sxs-lookup"><span data-stu-id="fa65a-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="fa65a-123">Если поставщика OSC поддерживает вход в систему с использованием кэшированных учетных данных, он указывает **useLogonCached** **значение true** в **возможности** XML.</span><span class="sxs-lookup"><span data-stu-id="fa65a-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="fa65a-124">Поставщик следует поместить все учетные данные для входа в строку _connectOut_ , предоставляющей OSC для хранения через подключения.</span><span class="sxs-lookup"><span data-stu-id="fa65a-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="fa65a-125">OSC не распознает _connectOut_ строку.</span><span class="sxs-lookup"><span data-stu-id="fa65a-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="fa65a-126">После OSC подтверждает, что этот **useLogonCached** имеет **значение true**, OSC шифрует строку для безопасности перед его сохранения в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="fa65a-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="fa65a-127">OSC передает эта строка для параметра _connectIn_ на последующих попыток входа в систему в социальных сетях вызовом [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="fa65a-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="fa65a-128">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fa65a-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa65a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fa65a-129">See also</span></span>

- [<span data-ttu-id="fa65a-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa65a-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="fa65a-131">Проверка подлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="fa65a-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

