---
title: Иолкаккаунтманажерунадвисе
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322010"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="424d4-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="424d4-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="424d4-104">Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей.</span><span class="sxs-lookup"><span data-stu-id="424d4-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="424d4-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="424d4-105">Quick info</span></span>

<span data-ttu-id="424d4-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="424d4-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="424d4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="424d4-107">Parameters</span></span>

<span data-ttu-id="424d4-108">_Двкукие_</span><span class="sxs-lookup"><span data-stu-id="424d4-108">_dwCookie_</span></span>
  
> <span data-ttu-id="424d4-109">возврата Файл cookie, возвращенный функцией [иолкаккаунтманажер:: Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="424d4-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="424d4-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="424d4-110">Return values</span></span>

|<span data-ttu-id="424d4-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="424d4-111">**HRESULT**</span></span>|<span data-ttu-id="424d4-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="424d4-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="424d4-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="424d4-113">S_OK</span></span>  <br/> |<span data-ttu-id="424d4-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="424d4-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="424d4-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="424d4-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="424d4-116">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="424d4-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="424d4-117">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="424d4-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="424d4-118">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="424d4-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="424d4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="424d4-119">See also</span></span>

- [<span data-ttu-id="424d4-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="424d4-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="424d4-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="424d4-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

