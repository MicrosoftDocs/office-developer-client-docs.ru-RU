---
title: иолкаккаунтманажерфиндаккаунт
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Находит учетную запись по значению свойства.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428804"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="8eacb-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="8eacb-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="8eacb-104">Находит учетную запись по значению свойства.</span><span class="sxs-lookup"><span data-stu-id="8eacb-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8eacb-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8eacb-105">Quick info</span></span>

<span data-ttu-id="8eacb-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="8eacb-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="8eacb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eacb-107">Parameters</span></span>

<span data-ttu-id="8eacb-108">_двпроп_</span><span class="sxs-lookup"><span data-stu-id="8eacb-108">_dwProp_</span></span>
  
> <span data-ttu-id="8eacb-109">возврата Свойство, по которому необходимо выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="8eacb-109">[in] The property to search on.</span></span> <span data-ttu-id="8eacb-110">Необходимо [PROP_ACCT_ID](prop_acct_id.md) или [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span><span class="sxs-lookup"><span data-stu-id="8eacb-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="8eacb-111">_пвар_</span><span class="sxs-lookup"><span data-stu-id="8eacb-111">_pVar_</span></span>
  
> <span data-ttu-id="8eacb-112">возврата Значение для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8eacb-112">[in] The value to match.</span></span>
    
<span data-ttu-id="8eacb-113">_ппаккаунт_</span><span class="sxs-lookup"><span data-stu-id="8eacb-113">_ppAccount_</span></span>
  
> <span data-ttu-id="8eacb-114">вышли Учетная запись найдена.</span><span class="sxs-lookup"><span data-stu-id="8eacb-114">[out] The account found.</span></span> <span data-ttu-id="8eacb-115">Этот объект поддерживает интерфейс [иолкаккаунт](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="8eacb-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8eacb-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8eacb-116">Return values</span></span>

|<span data-ttu-id="8eacb-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8eacb-117">**HRESULT**</span></span>|<span data-ttu-id="8eacb-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="8eacb-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8eacb-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8eacb-119">S_OK</span></span>  <br/> |<span data-ttu-id="8eacb-120">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="8eacb-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8eacb-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8eacb-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="8eacb-122">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="8eacb-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="8eacb-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8eacb-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8eacb-124">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="8eacb-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="8eacb-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8eacb-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="8eacb-126">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="8eacb-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8eacb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8eacb-127">See also</span></span>

- [<span data-ttu-id="8eacb-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="8eacb-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="8eacb-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="8eacb-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="8eacb-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="8eacb-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

