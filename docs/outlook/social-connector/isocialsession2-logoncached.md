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
# <a name="isocialsession2logoncached"></a><span data-ttu-id="28b2d-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="28b2d-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="28b2d-104">Войдите на сайт социальной сети с помощью кэшных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="28b2d-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="28b2d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="28b2d-105">Parameters</span></span>

<span data-ttu-id="28b2d-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="28b2d-106">_connectIn_</span></span>
  
> <span data-ttu-id="28b2d-107">[in] Строка, которая может быть пустой или содержит учетные данные для входа, в зависимости от контекста, в котором OSC вызывает **LogonCached.**</span><span class="sxs-lookup"><span data-stu-id="28b2d-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="28b2d-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="28b2d-108">_userName_</span></span>
  
> <span data-ttu-id="28b2d-109">[in] Строка, содержаная имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="28b2d-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="28b2d-110">_password_</span><span class="sxs-lookup"><span data-stu-id="28b2d-110">_password_</span></span>
  
> <span data-ttu-id="28b2d-111">[in] Строка, содержаная пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="28b2d-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="28b2d-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="28b2d-112">_connectOut_</span></span>
  
> <span data-ttu-id="28b2d-113">[out] Непрозрачной строки, которая содержит учетные данные.</span><span class="sxs-lookup"><span data-stu-id="28b2d-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28b2d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="28b2d-114">Remarks</span></span>

<span data-ttu-id="28b2d-115">Этот метод используется для проверки подлинности, только если  **для useLogonCached** установлено true в **XML** возможностей, возвращаемом [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="28b2d-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="28b2d-116">Outlook Social Connector (OSC) вызывает **LogonCached** и передает пустую строку _для connectIn_ и непустых строк _userName_ и _password._</span><span class="sxs-lookup"><span data-stu-id="28b2d-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="28b2d-117">Поставщик использует _имя пользователя_ и пароль для входа в социальные сети и возвращает непрозрачные _параметры connectOut_ в OSC, если проверка подлинности будет успешной. </span><span class="sxs-lookup"><span data-stu-id="28b2d-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="28b2d-118">Если проверка подлинности не удалась, поставщик возвращает OSC_E_LOGON_FAILURE ошибку в OSC.</span><span class="sxs-lookup"><span data-stu-id="28b2d-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="28b2d-119">Параметр  _connectOut_ является непрозрачной строкой в OSC и передается  _параметру connectIn_ при последующих попытках OSC войти в социальные сети.</span><span class="sxs-lookup"><span data-stu-id="28b2d-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="28b2d-120">Поставщик должен разместить все учетные данные в  _строке connectOut,_ которую поставщик хочет сохранить в osC между подключениями.</span><span class="sxs-lookup"><span data-stu-id="28b2d-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="28b2d-121">OsC не интерпретирует строку в  _connectOut_ и шифрует строку в целях безопасности перед ее сохранением в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="28b2d-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="28b2d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="28b2d-122">See also</span></span>

- [<span data-ttu-id="28b2d-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="28b2d-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

