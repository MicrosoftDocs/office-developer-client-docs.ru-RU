---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Unregisters клиент с менеджером учетной записи для уведомлений для всех учетных записей.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430989"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="fd343-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fd343-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="fd343-104">Unregisters клиент с менеджером учетной записи для уведомлений для всех учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fd343-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fd343-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fd343-105">Quick info</span></span>

<span data-ttu-id="fd343-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="fd343-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="fd343-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="fd343-107">Parameters</span></span>

<span data-ttu-id="fd343-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="fd343-108">_dwCookie_</span></span>
  
> <span data-ttu-id="fd343-109">[in] Файл cookie, возвращенный [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="fd343-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fd343-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fd343-110">Return values</span></span>

|<span data-ttu-id="fd343-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd343-111">**HRESULT**</span></span>|<span data-ttu-id="fd343-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd343-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd343-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd343-113">S_OK</span></span>  <br/> |<span data-ttu-id="fd343-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="fd343-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="fd343-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fd343-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="fd343-116">Один или несколько аргументов являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="fd343-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="fd343-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="fd343-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="fd343-118">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="fd343-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd343-119">См. также</span><span class="sxs-lookup"><span data-stu-id="fd343-119">See also</span></span>

- [<span data-ttu-id="fd343-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="fd343-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="fd343-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="fd343-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

