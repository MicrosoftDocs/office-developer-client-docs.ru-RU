---
title: Иолкаккаунтманажеренумератеаккаунтс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Gets an enumerator for the accounts of the specific category or type.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322052"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="ba53e-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="ba53e-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="ba53e-104">Gets an enumerator for the accounts of the specific category or type.</span><span class="sxs-lookup"><span data-stu-id="ba53e-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ba53e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ba53e-105">Quick info</span></span>

<span data-ttu-id="ba53e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="ba53e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="ba53e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba53e-107">Parameters</span></span>

<span data-ttu-id="ba53e-108">_Пклсидкатегори_</span><span class="sxs-lookup"><span data-stu-id="ba53e-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="ba53e-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="ba53e-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="ba53e-111">Клсид_олкмаил</span><span class="sxs-lookup"><span data-stu-id="ba53e-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="ba53e-112">Клсид_олкаддрессбук</span><span class="sxs-lookup"><span data-stu-id="ba53e-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="ba53e-113">Клсид_олксторе</span><span class="sxs-lookup"><span data-stu-id="ba53e-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="ba53e-114">_Пклсидтипе_</span><span class="sxs-lookup"><span data-stu-id="ba53e-114">_pclsidType_</span></span>
  
> <span data-ttu-id="ba53e-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="ba53e-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="ba53e-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="ba53e-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="ba53e-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="ba53e-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="ba53e-119">Клсид_олкмапиаккаунт</span><span class="sxs-lookup"><span data-stu-id="ba53e-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="ba53e-120">Клсид_олкхотмаилаккаунт</span><span class="sxs-lookup"><span data-stu-id="ba53e-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="ba53e-121">Клсид_олклдапаккаунт</span><span class="sxs-lookup"><span data-stu-id="ba53e-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="ba53e-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="ba53e-122">_dwFlags_</span></span>
  
> <span data-ttu-id="ba53e-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="ba53e-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="ba53e-125">_Ппенум_</span><span class="sxs-lookup"><span data-stu-id="ba53e-125">_ppEnum_</span></span>
  
> <span data-ttu-id="ba53e-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="ba53e-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ba53e-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ba53e-127">Return values</span></span>

|<span data-ttu-id="ba53e-128">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ba53e-128">**HRESULT**</span></span>|<span data-ttu-id="ba53e-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ba53e-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba53e-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba53e-130">S_OK</span></span>  <br/> |<span data-ttu-id="ba53e-131">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ba53e-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="ba53e-132">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="ba53e-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="ba53e-133">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="ba53e-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba53e-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="ba53e-134">Remarks</span></span>

<span data-ttu-id="ba53e-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span><span class="sxs-lookup"><span data-stu-id="ba53e-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="ba53e-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span><span class="sxs-lookup"><span data-stu-id="ba53e-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="ba53e-138">Если учетная запись является учетной записью Exchange (*пклсидтипе* — **клсид_олкмапиаккаунт** ), и вы пытаетесь перечислить учетные записи, которые реализуют адресную книгу (*пргклсидкатегори* — **клсид_олкаддрессбук** ), вызов \*\* Иолкаккаунтманажер:: EnumerateAccounts\*\* не будет возвращать учетную запись Exchange в перечислителе учетных записей *ппенум* .</span><span class="sxs-lookup"><span data-stu-id="ba53e-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ba53e-139">См. также</span><span class="sxs-lookup"><span data-stu-id="ba53e-139">See also</span></span>

- [<span data-ttu-id="ba53e-140">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="ba53e-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="ba53e-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="ba53e-141">IOlkEnum</span></span>](iolkenum.md)

