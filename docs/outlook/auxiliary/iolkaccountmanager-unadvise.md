---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей.
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807855"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="e184f-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e184f-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="e184f-104">Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e184f-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e184f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e184f-105">Quick info</span></span>

<span data-ttu-id="e184f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="e184f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="e184f-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e184f-107">Parameters</span></span>

<span data-ttu-id="e184f-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="e184f-108">_dwCookie_</span></span>
  
> <span data-ttu-id="e184f-109">[in] Файл cookie, возвращаемых [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="e184f-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e184f-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e184f-110">Return values</span></span>

|<span data-ttu-id="e184f-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e184f-111">**HRESULT**</span></span>|<span data-ttu-id="e184f-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="e184f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e184f-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e184f-113">S_OK</span></span>  <br/> |<span data-ttu-id="e184f-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="e184f-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="e184f-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e184f-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e184f-116">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="e184f-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="e184f-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e184f-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="e184f-118">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="e184f-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e184f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e184f-119">See also</span></span>

- [<span data-ttu-id="e184f-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="e184f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="e184f-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="e184f-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

