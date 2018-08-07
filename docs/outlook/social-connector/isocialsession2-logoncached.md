---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Журналы входа на сайт социальной сети с помощью кэшированных учетных данных.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812756"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="c94bd-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="c94bd-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="c94bd-104">Журналы входа на сайт социальной сети с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c94bd-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="c94bd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c94bd-105">Parameters</span></span>

<span data-ttu-id="c94bd-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="c94bd-106">_connectIn_</span></span>
  
> <span data-ttu-id="c94bd-107">[in] Строка, которая может быть пустой или содержит учетные данные для входа, в зависимости от контекста, в котором OSC звонит **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="c94bd-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="c94bd-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="c94bd-108">_userName_</span></span>
  
> <span data-ttu-id="c94bd-109">[in] Строка, содержащая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c94bd-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="c94bd-110">_password_</span><span class="sxs-lookup"><span data-stu-id="c94bd-110">_password_</span></span>
  
> <span data-ttu-id="c94bd-111">[in] Строка, содержащая пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="c94bd-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="c94bd-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="c94bd-112">_connectOut_</span></span>
  
> <span data-ttu-id="c94bd-113">[out] Непрозрачную строку, содержащее учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c94bd-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c94bd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c94bd-114">Remarks</span></span>

<span data-ttu-id="c94bd-115">Этот метод вызывается для проверки подлинности только в том случае, если **useLogonCached** задано **значение true** в **возможности** XML, возвращенные [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="c94bd-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="c94bd-116">Outlook Social Connector (OSC) вызывает **LogonCached**и передает пустую строку для _connectIn_ и непустые строки _имя пользователя_ и _пароль_ .</span><span class="sxs-lookup"><span data-stu-id="c94bd-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="c94bd-117">Поставщик использует _имя пользователя_ и _пароль_ для входа в социальной сети и возвращает параметр непрозрачный _connectOut_ OSC, если проверка подлинности выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c94bd-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="c94bd-118">Если происходит сбой проверки подлинности, поставщик возвращает ошибку OSC_E_LOGON_FAILURE для OSC.</span><span class="sxs-lookup"><span data-stu-id="c94bd-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="c94bd-119">Параметр _connectOut_ представляет собой непрозрачную строку для OSC и передается параметр _connectIn_ в последующих попыток с OSC войти в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="c94bd-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="c94bd-120">Поставщик следует поместить все учетные данные в строку _connectOut_ , предоставляющей OSC для хранения через подключения.</span><span class="sxs-lookup"><span data-stu-id="c94bd-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="c94bd-121">OSC не распознает строку в _connectOut_и зашифровывает строку в целях безопасности перед его сохранения в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="c94bd-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c94bd-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c94bd-122">See also</span></span>

- [<span data-ttu-id="c94bd-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c94bd-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

