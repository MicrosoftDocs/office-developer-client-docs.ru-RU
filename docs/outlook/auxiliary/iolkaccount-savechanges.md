---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Фиксация изменений в объекте учетной записи путем записи в хранилище реестра.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425836"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="511d1-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="511d1-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="511d1-104">Фиксация изменений в объекте учетной записи путем записи в хранилище реестра.</span><span class="sxs-lookup"><span data-stu-id="511d1-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="511d1-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="511d1-105">Quick info</span></span>

<span data-ttu-id="511d1-106">См. [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="511d1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="511d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="511d1-107">Parameters</span></span>

<span data-ttu-id="511d1-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="511d1-108">_dwFlags_</span></span>
  
> <span data-ttu-id="511d1-109">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="511d1-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="511d1-110">OLK_ACCOUNT_NO_FLAGS это единственное поддерживаемые значения.</span><span class="sxs-lookup"><span data-stu-id="511d1-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="511d1-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="511d1-111">Return values</span></span>

|<span data-ttu-id="511d1-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="511d1-112">**HRESULT**</span></span>|<span data-ttu-id="511d1-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="511d1-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="511d1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="511d1-114">S_OK</span></span>  <br/> |<span data-ttu-id="511d1-115">Метод был успешным.</span><span class="sxs-lookup"><span data-stu-id="511d1-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="511d1-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="511d1-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="511d1-117">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="511d1-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="511d1-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="511d1-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="511d1-119">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="511d1-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="511d1-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="511d1-120">Remarks</span></span>

<span data-ttu-id="511d1-121">После изменения значения свойств учетной записи с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md)используйте **IOlkAccount::SaveChanges** для сохранения таких изменений.</span><span class="sxs-lookup"><span data-stu-id="511d1-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="511d1-122">См. также</span><span class="sxs-lookup"><span data-stu-id="511d1-122">See also</span></span>

- [<span data-ttu-id="511d1-123">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="511d1-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="511d1-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="511d1-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

