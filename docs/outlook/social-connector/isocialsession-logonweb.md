---
title: ИсоЦиалсессионлогонвеб
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Выполняет вход на сайт социальных сетей с помощью проверки подлинности на основе форм.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430338"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="dbb3e-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="dbb3e-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="dbb3e-104">Выполняет вход на сайт социальных сетей с помощью проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="dbb3e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbb3e-105">Parameters</span></span>

<span data-ttu-id="dbb3e-106">_подключение_</span><span class="sxs-lookup"><span data-stu-id="dbb3e-106">_connectIn_</span></span>
  
> <span data-ttu-id="dbb3e-107">возврата Строка, которая имеет **значение NULL**, URL-адрес формы входа в Интернете или строку, содержащую учетные данные входа в систему, в зависимости от контекста в процессе входа при вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="dbb3e-108">_подключение_</span><span class="sxs-lookup"><span data-stu-id="dbb3e-108">_connectOut_</span></span>
  
> <span data-ttu-id="dbb3e-109">вышли Строка, содержащая учетные данные для входа.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbb3e-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbb3e-110">Remarks</span></span>

<span data-ttu-id="dbb3e-111">Outlook Social Connector (OSC) вызывает метод **логонвеб** , только если поставщик указывает, что он поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="dbb3e-112">Поставщик указывает, что требуется проверка подлинности на основе форм, задав для **уселогонвебаус** **значение true** в XML для **возможностей**.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="dbb3e-113">Если поставщик устанавливает **уселогонвебаус** как **false**, OSC использует обычную проверку подлинности и вызывает метод [настроенный ISocialSession:: logon](isocialsession-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="dbb3e-114">Вход на сайт социальной сети с помощью проверки подлинности на основе форм подразумевает вызов методов **логонвеб** и [настроенный ISocialSession:: жетлогонурл](isocialsession-getlogonurl.md) в определенном порядке:</span><span class="sxs-lookup"><span data-stu-id="dbb3e-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="dbb3e-115">OSC вызывает **логонвеб** в первый раз, передавая **значение NULL** параметру _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="dbb3e-116">Поставщик вызывает ошибку ОСК_Е_АУС_ЕРРОР для OSC.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="dbb3e-117">Следующий вызов OSC вызывает **жетлогонурл**.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="dbb3e-118">Поставщик возвращает соответствующий URL-адрес страницы входа в методе **жетлогонурл** .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="dbb3e-119">Для отображения страницы входа в систему на основе форм OSC использует URL-адрес, возвращенный **жетлогонурл** .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="dbb3e-120">Затем OSC вызывает **логонвеб** во второй раз, ПЕРЕДАВАЯ URL-адрес в форму входа в параметре _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="dbb3e-121">Если проверка подлинности прошла успешно, поставщик возвращает учетные данные входа в параметре _подключения_ к OSC.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="dbb3e-122">Если не удается выполнить проверку подлинности, поставщик вызовет ошибку ОСК_Е_АУС_ЕРРОР на OSC.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="dbb3e-123">Если поставщик OSC поддерживает вход в систему с использованием кэшированных учетных данных, он определяет **уселогонкачед** как **true** в XML-коде **возможностей** .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="dbb3e-124">Поставщик должен помещать все учетные данные для входа в строку _подключения_ , которую должен хранить OSC для каждого подключения.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="dbb3e-125">OSC не интерпретирует строку _подключения_ .</span><span class="sxs-lookup"><span data-stu-id="dbb3e-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="dbb3e-126">После того как OSC проверит, что **уселогонкачед** имеет **значение true**, OSC шифрует строку для обеспечения безопасности перед ее сохранением в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="dbb3e-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="dbb3e-127">OSC передает эту строку параметру _Connect_ при последующих попытках входа в социальную сеть, вызывая [ISocialSession2:: логонкачед](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="dbb3e-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="dbb3e-128">Сведения о кодах ошибок см. в статье [Коды ошибок поставщика Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dbb3e-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dbb3e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="dbb3e-129">See also</span></span>

- [<span data-ttu-id="dbb3e-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbb3e-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="dbb3e-131">Проверка поДлинности на основе форм</span><span class="sxs-lookup"><span data-stu-id="dbb3e-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

