---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Регистрация клиента диспетчером учетной записи для уведомлений о всех учетных записей.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807839"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="6f7ed-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="6f7ed-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="6f7ed-104">Регистрация клиента диспетчером учетной записи для уведомлений о всех учетных записей.</span><span class="sxs-lookup"><span data-stu-id="6f7ed-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6f7ed-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="6f7ed-105">Quick info</span></span>

<span data-ttu-id="6f7ed-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="6f7ed-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="6f7ed-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6f7ed-107">Parameters</span></span>

<span data-ttu-id="6f7ed-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="6f7ed-108">_pNotify_</span></span>
  
> <span data-ttu-id="6f7ed-109">[in] Интерфейс [IOlkAccountNotify](iolkaccountnotify.md) , диспетчер учетных записей для отправки уведомлений для клиента.</span><span class="sxs-lookup"><span data-stu-id="6f7ed-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="6f7ed-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="6f7ed-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="6f7ed-111">[out] Файл cookie, [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) будет использоваться при удалении регистрации учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6f7ed-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6f7ed-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6f7ed-112">Return values</span></span>

|<span data-ttu-id="6f7ed-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f7ed-113">**HRESULT**</span></span>|<span data-ttu-id="6f7ed-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f7ed-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f7ed-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6f7ed-115">S_OK</span></span>  <br/> |<span data-ttu-id="6f7ed-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="6f7ed-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="6f7ed-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6f7ed-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="6f7ed-118">Указан недопустимый аргумент было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="6f7ed-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="6f7ed-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="6f7ed-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="6f7ed-120">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="6f7ed-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f7ed-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6f7ed-121">See also</span></span>

- [<span data-ttu-id="6f7ed-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="6f7ed-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="6f7ed-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6f7ed-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

