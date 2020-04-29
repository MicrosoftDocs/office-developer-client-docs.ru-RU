---
title: иолкаккаунтманажерадвисе
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Регистрирует клиента с помощью диспетчера учетных записей для уведомлений, касающихся всех учетных записей.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427712"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="c838a-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="c838a-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="c838a-104">Регистрирует клиента с помощью диспетчера учетных записей для уведомлений, касающихся всех учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c838a-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c838a-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c838a-105">Quick info</span></span>

<span data-ttu-id="c838a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="c838a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="c838a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c838a-107">Parameters</span></span>

<span data-ttu-id="c838a-108">_пнотифи_</span><span class="sxs-lookup"><span data-stu-id="c838a-108">_pNotify_</span></span>
  
> <span data-ttu-id="c838a-109">возврата Интерфейс [иолкаккаунтнотифи](iolkaccountnotify.md) , который диспетчер учетных записей будет использовать для отправки уведомлений клиенту.</span><span class="sxs-lookup"><span data-stu-id="c838a-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="c838a-110">_пдвкукие_</span><span class="sxs-lookup"><span data-stu-id="c838a-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="c838a-111">вышли Файл cookie, [иолкаккаунтманажер:: unadvise](iolkaccountmanager-unadvise.md) будет использоваться при удалении регистрации для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c838a-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c838a-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c838a-112">Return values</span></span>

|<span data-ttu-id="c838a-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c838a-113">**HRESULT**</span></span>|<span data-ttu-id="c838a-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="c838a-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c838a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c838a-115">S_OK</span></span>  <br/> |<span data-ttu-id="c838a-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="c838a-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="c838a-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c838a-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="c838a-118">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="c838a-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="c838a-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c838a-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c838a-120">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="c838a-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c838a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c838a-121">See also</span></span>

- [<span data-ttu-id="c838a-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="c838a-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="c838a-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c838a-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

