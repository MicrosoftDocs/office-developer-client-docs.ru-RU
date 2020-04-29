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
# <a name="isocialsession2logoncached"></a><span data-ttu-id="61d20-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="61d20-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="61d20-104">Выполняет вход на сайт социальных сетей с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="61d20-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="61d20-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="61d20-105">Parameters</span></span>

<span data-ttu-id="61d20-106">_подключение_</span><span class="sxs-lookup"><span data-stu-id="61d20-106">_connectIn_</span></span>
  
> <span data-ttu-id="61d20-107">возврата Строка, которая может быть пустой или содержать учетные данные для входа в зависимости от контекста, в котором OSC вызывает **логонкачед**.</span><span class="sxs-lookup"><span data-stu-id="61d20-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="61d20-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="61d20-108">_userName_</span></span>
  
> <span data-ttu-id="61d20-109">возврата Строка, содержащая имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="61d20-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="61d20-110">_password_</span><span class="sxs-lookup"><span data-stu-id="61d20-110">_password_</span></span>
  
> <span data-ttu-id="61d20-111">возврата Строка, содержащая пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="61d20-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="61d20-112">_подключение_</span><span class="sxs-lookup"><span data-stu-id="61d20-112">_connectOut_</span></span>
  
> <span data-ttu-id="61d20-113">вышли Непрозрачная строка, содержащая учетные данные.</span><span class="sxs-lookup"><span data-stu-id="61d20-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61d20-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="61d20-114">Remarks</span></span>

<span data-ttu-id="61d20-115">Этот метод вызывается для проверки подлинности только в том случае, если для **уселогонкачед** задано **значение true** в XML-коде **возможностей** , возвращаемом [исоЦиалпровидер::-Capabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="61d20-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="61d20-116">Outlook Social Connector (OSC) вызывает **логонкачед**и передает пустую строку для _подключения_ и непустых строк _имени пользователя_ и _пароля_ .</span><span class="sxs-lookup"><span data-stu-id="61d20-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="61d20-117">Поставщик использует _имя пользователя_ и _пароль_ для входа в социальную сеть и возвращает параметру непрозрачного _подключения_ к OSC, если проверка подлинности прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="61d20-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="61d20-118">Если произошел сбой проверки подлинности, поставщик возвращает ошибку OSC_E_LOGON_FAILURE на OSC.</span><span class="sxs-lookup"><span data-stu-id="61d20-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="61d20-119">Параметр _Connect_ — это непрозрачная строка для OSC и передается параметру _Connect_ при последующих попытках входа в социальную сеть с помощью OSC.</span><span class="sxs-lookup"><span data-stu-id="61d20-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="61d20-120">Поставщик должен помещать в строку _подключения_ любые учетные данные, необходимые поставщику для хранения OSC в подключениях.</span><span class="sxs-lookup"><span data-stu-id="61d20-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="61d20-121">OSC не интерпретирует строку в _подсоединении_и шифрует строку в целях безопасности перед ее сохранением в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="61d20-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61d20-122">См. также</span><span class="sxs-lookup"><span data-stu-id="61d20-122">See also</span></span>

- [<span data-ttu-id="61d20-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61d20-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

