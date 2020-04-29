---
title: иолкаккаунтжетаккаунтинфо
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Получает сведения о типе и категориях для указанной учетной записи.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437905"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="74767-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="74767-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="74767-104">Получает сведения о типе и категориях для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="74767-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="74767-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="74767-105">Quick info</span></span>

<span data-ttu-id="74767-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="74767-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="74767-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="74767-107">Parameters</span></span>

<span data-ttu-id="74767-108">_пклсидтипе_</span><span class="sxs-lookup"><span data-stu-id="74767-108">_pclsidType_</span></span>
  
> <span data-ttu-id="74767-109">вышли Идентификатор класса для типа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="74767-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="74767-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="74767-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="74767-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="74767-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="74767-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="74767-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="74767-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="74767-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="74767-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="74767-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="74767-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="74767-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="74767-116">_пккатегориес_</span><span class="sxs-lookup"><span data-stu-id="74767-116">_pcCategories_</span></span>
  
> <span data-ttu-id="74767-117">вышли Количество категорий в _пргклсидкатегори_.</span><span class="sxs-lookup"><span data-stu-id="74767-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="74767-118">_пргклсидкатегори_</span><span class="sxs-lookup"><span data-stu-id="74767-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="74767-119">вышли Массив категорий, с которыми связана эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="74767-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="74767-120">Массив имеет размер \* _пккатегориес_.</span><span class="sxs-lookup"><span data-stu-id="74767-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="74767-121">Значение каждой категории в массиве должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="74767-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="74767-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="74767-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="74767-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="74767-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="74767-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="74767-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="74767-125">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="74767-125">Return values</span></span>

<span data-ttu-id="74767-126">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="74767-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74767-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="74767-127">Remarks</span></span>

<span data-ttu-id="74767-128">После возврата этого метода необходимо освободить *пргклсидкатегори* с помощью [Иолкаккаунт:: фримемори](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="74767-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="74767-129">**Иолкаккаунт:: жетаккаунтинфо** не поддерживает категорию адресной книги для учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="74767-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="74767-130">Если учетная запись является учетной записью Exchange (*пклсидтипе* **CLSID_OlkMAPIAccount** ), а учетная запись реализует адресную книгу, вызов **иолкаккаунт:: жетаккаунтинфо** не будет возвращать **CLSID_OlkAddressBook** в виде категории в *пргклсидкатегори* .</span><span class="sxs-lookup"><span data-stu-id="74767-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74767-131">См. также</span><span class="sxs-lookup"><span data-stu-id="74767-131">See also</span></span>

- [<span data-ttu-id="74767-132">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="74767-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="74767-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="74767-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

