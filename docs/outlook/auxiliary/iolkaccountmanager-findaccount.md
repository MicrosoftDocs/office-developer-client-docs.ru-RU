---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Поиск учетной записи по значению свойства.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807846"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="15897-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="15897-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="15897-104">Поиск учетной записи по значению свойства.</span><span class="sxs-lookup"><span data-stu-id="15897-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="15897-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="15897-105">Quick info</span></span>

<span data-ttu-id="15897-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="15897-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="15897-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="15897-107">Parameters</span></span>

<span data-ttu-id="15897-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="15897-108">_dwProp_</span></span>
  
> <span data-ttu-id="15897-109">[in] Свойство для поиска.</span><span class="sxs-lookup"><span data-stu-id="15897-109">[in] The property to search on.</span></span> <span data-ttu-id="15897-110">Должно быть [PROP_ACCT_ID](prop_acct_id.md) или [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span><span class="sxs-lookup"><span data-stu-id="15897-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="15897-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="15897-111">_pVar_</span></span>
  
> <span data-ttu-id="15897-112">[in] Значение в соответствии с.</span><span class="sxs-lookup"><span data-stu-id="15897-112">[in] The value to match.</span></span>
    
<span data-ttu-id="15897-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="15897-113">_ppAccount_</span></span>
  
> <span data-ttu-id="15897-114">[out] Учетная запись найдена.</span><span class="sxs-lookup"><span data-stu-id="15897-114">[out] The account found.</span></span> <span data-ttu-id="15897-115">Этот объект поддерживает интерфейс [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="15897-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="15897-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="15897-116">Return values</span></span>

|<span data-ttu-id="15897-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15897-117">**HRESULT**</span></span>|<span data-ttu-id="15897-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="15897-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15897-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="15897-119">S_OK</span></span>  <br/> |<span data-ttu-id="15897-120">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="15897-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="15897-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="15897-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="15897-122">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="15897-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="15897-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="15897-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="15897-124">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="15897-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="15897-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="15897-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="15897-126">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="15897-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15897-127">См. также</span><span class="sxs-lookup"><span data-stu-id="15897-127">See also</span></span>

- [<span data-ttu-id="15897-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="15897-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="15897-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="15897-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="15897-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="15897-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

