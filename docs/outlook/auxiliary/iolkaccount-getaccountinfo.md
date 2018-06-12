---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Получает сведения о типа и категорий для указанной учетной записи.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807776"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="420a1-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="420a1-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="420a1-104">Получает сведения о типа и категорий для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="420a1-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="420a1-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="420a1-105">Quick info</span></span>

<span data-ttu-id="420a1-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="420a1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="420a1-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="420a1-107">Parameters</span></span>

<span data-ttu-id="420a1-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="420a1-108">_pclsidType_</span></span>
  
> <span data-ttu-id="420a1-109">[out] Идентификатор класса для типа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="420a1-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="420a1-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="420a1-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="420a1-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="420a1-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="420a1-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="420a1-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="420a1-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="420a1-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="420a1-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="420a1-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="420a1-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="420a1-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="420a1-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="420a1-116">_pcCategories_</span></span>
  
> <span data-ttu-id="420a1-117">[out] Число категорий в _prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="420a1-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="420a1-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="420a1-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="420a1-119">[out] Массив категории, которые связаны с этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="420a1-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="420a1-120">Массив имеет размер \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="420a1-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="420a1-121">Значение каждой категории в массиве должно быть одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="420a1-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="420a1-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="420a1-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="420a1-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="420a1-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="420a1-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="420a1-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="420a1-125">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="420a1-125">Return values</span></span>

<span data-ttu-id="420a1-126">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="420a1-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="420a1-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="420a1-127">Remarks</span></span>

<span data-ttu-id="420a1-128">После возврата этим методом, должен освободить *prgclsidCategory* с помощью [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="420a1-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="420a1-129">**IOlkAccount::GetAccountInfo** не поддерживает категории адресной книги для учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="420a1-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="420a1-130">Если учетная запись Exchange учетной записи (*pclsidType* — **CLSID_OlkMAPIAccount** ) и учетную запись реализует адресной книги, вызывающий **IOlkAccount::GetAccountInfo** не будет возвращать **CLSID_OlkAddressBook** как категории в * prgclsidCategory* .</span><span class="sxs-lookup"><span data-stu-id="420a1-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="420a1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="420a1-131">See also</span></span>

- [<span data-ttu-id="420a1-132">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="420a1-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="420a1-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="420a1-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

