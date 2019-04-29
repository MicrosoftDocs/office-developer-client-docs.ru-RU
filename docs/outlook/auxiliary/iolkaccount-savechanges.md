---
title: Иолкаккаунтсавечанжес
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Фиксирует изменения объекта Account, записывая в хранилище реестра.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425836"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="1bbf5-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="1bbf5-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="1bbf5-104">Фиксирует изменения объекта Account, записывая в хранилище реестра.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1bbf5-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1bbf5-105">Quick info</span></span>

<span data-ttu-id="1bbf5-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="1bbf5-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="1bbf5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bbf5-107">Parameters</span></span>

<span data-ttu-id="1bbf5-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="1bbf5-108">_dwFlags_</span></span>
  
> <span data-ttu-id="1bbf5-109">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="1bbf5-110">ОЛК_АККАУНТ_НО_ФЛАГС — единственное поддерживаемое значение.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1bbf5-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1bbf5-111">Return values</span></span>

|<span data-ttu-id="1bbf5-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1bbf5-112">**HRESULT**</span></span>|<span data-ttu-id="1bbf5-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="1bbf5-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1bbf5-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bbf5-114">S_OK</span></span>  <br/> |<span data-ttu-id="1bbf5-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="1bbf5-116">Е_АККТ_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="1bbf5-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="1bbf5-117">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="1bbf5-118">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="1bbf5-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="1bbf5-119">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bbf5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bbf5-120">Remarks</span></span>

<span data-ttu-id="1bbf5-121">После изменения значения свойства учетной записи с помощью [иолкаккаунт:: сетпроп](iolkaccount-setprop.md), используйте **Иолкаккаунт:: SaveChanges** , чтобы сохранить такие изменения.</span><span class="sxs-lookup"><span data-stu-id="1bbf5-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1bbf5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1bbf5-122">See also</span></span>

- [<span data-ttu-id="1bbf5-123">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="1bbf5-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="1bbf5-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="1bbf5-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

