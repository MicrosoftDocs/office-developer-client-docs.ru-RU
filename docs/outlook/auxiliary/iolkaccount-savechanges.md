---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Фиксирует изменения объекта учетной записи с помощью записи реестра хранилища.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807791"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="00542-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="00542-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="00542-104">Фиксирует изменения объекта учетной записи с помощью записи реестра хранилища.</span><span class="sxs-lookup"><span data-stu-id="00542-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="00542-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="00542-105">Quick info</span></span>

<span data-ttu-id="00542-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="00542-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="00542-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="00542-107">Parameters</span></span>

<span data-ttu-id="00542-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="00542-108">_dwFlags_</span></span>
  
> <span data-ttu-id="00542-109">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="00542-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="00542-110">OLK_ACCOUNT_NO_FLAGS — это поддерживается только значение.</span><span class="sxs-lookup"><span data-stu-id="00542-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="00542-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="00542-111">Return values</span></span>

|<span data-ttu-id="00542-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00542-112">**HRESULT**</span></span>|<span data-ttu-id="00542-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="00542-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00542-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="00542-114">S_OK</span></span>  <br/> |<span data-ttu-id="00542-115">Метод успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="00542-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="00542-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="00542-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="00542-117">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="00542-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="00542-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="00542-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="00542-119">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="00542-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00542-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="00542-120">Remarks</span></span>

<span data-ttu-id="00542-121">После изменения значения свойства учетной записи с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md), используйте **IOlkAccount::SaveChanges** для сохранения такие изменения.</span><span class="sxs-lookup"><span data-stu-id="00542-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00542-122">См. также</span><span class="sxs-lookup"><span data-stu-id="00542-122">See also</span></span>

- [<span data-ttu-id="00542-123">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="00542-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="00542-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="00542-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

