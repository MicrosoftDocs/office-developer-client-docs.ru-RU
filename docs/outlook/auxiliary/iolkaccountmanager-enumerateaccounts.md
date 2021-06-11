---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Gets an enumerator for the accounts of the specific category or type.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423050"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="097db-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="097db-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="097db-104">Gets an enumerator for the accounts of the specific category or type.</span><span class="sxs-lookup"><span data-stu-id="097db-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="097db-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="097db-105">Quick info</span></span>

<span data-ttu-id="097db-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="097db-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="097db-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="097db-107">Parameters</span></span>

<span data-ttu-id="097db-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="097db-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="097db-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="097db-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="097db-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="097db-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="097db-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="097db-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="097db-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="097db-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="097db-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="097db-114">_pclsidType_</span></span>
  
> <span data-ttu-id="097db-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="097db-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="097db-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="097db-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="097db-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="097db-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="097db-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="097db-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="097db-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="097db-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="097db-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="097db-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="097db-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="097db-122">_dwFlags_</span></span>
  
> <span data-ttu-id="097db-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="097db-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="097db-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="097db-125">_ppEnum_</span></span>
  
> <span data-ttu-id="097db-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="097db-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="097db-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="097db-127">Return values</span></span>

|<span data-ttu-id="097db-128">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="097db-128">**HRESULT**</span></span>|<span data-ttu-id="097db-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="097db-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="097db-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="097db-130">S_OK</span></span>  <br/> |<span data-ttu-id="097db-131">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="097db-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="097db-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="097db-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="097db-133">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="097db-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="097db-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="097db-134">Remarks</span></span>

<span data-ttu-id="097db-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span><span class="sxs-lookup"><span data-stu-id="097db-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="097db-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span><span class="sxs-lookup"><span data-stu-id="097db-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="097db-138">Если учетная запись является учетной записью Exchange *(pclsidType* — **CLSID_OlkMAPIAccount),** и вы пытаетесь учесть учетные записи, реализуя адресную книгу *(prgclsidCategory* — **CLSID_OlkAddressBook),** вызов **IOlkAccountManager::EnumerateAccounts** не возвращает учетную запись Exchange в переучете *счетов ppEnum* .</span><span class="sxs-lookup"><span data-stu-id="097db-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="097db-139">См. также</span><span class="sxs-lookup"><span data-stu-id="097db-139">See also</span></span>

- [<span data-ttu-id="097db-140">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="097db-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="097db-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="097db-141">IOlkEnum</span></span>](iolkenum.md)

