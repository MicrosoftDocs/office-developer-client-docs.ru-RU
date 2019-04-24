---
title: Иолкаккаунтжетаккаунтинфо
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Получает сведения о типе и категориях для указанной учетной записи.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318188"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="fb7f2-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="fb7f2-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="fb7f2-104">Получает сведения о типе и категориях для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fb7f2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fb7f2-105">Quick info</span></span>

<span data-ttu-id="fb7f2-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="fb7f2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="fb7f2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb7f2-107">Parameters</span></span>

<span data-ttu-id="fb7f2-108">_Пклсидтипе_</span><span class="sxs-lookup"><span data-stu-id="fb7f2-108">_pclsidType_</span></span>
  
> <span data-ttu-id="fb7f2-109">вышли Идентификатор класса для типа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="fb7f2-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="fb7f2-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="fb7f2-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="fb7f2-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="fb7f2-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="fb7f2-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="fb7f2-113">Клсид_олкмапиаккаунт</span><span class="sxs-lookup"><span data-stu-id="fb7f2-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="fb7f2-114">Клсид_олкхотмаилаккаунт</span><span class="sxs-lookup"><span data-stu-id="fb7f2-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="fb7f2-115">Клсид_олклдапаккаунт</span><span class="sxs-lookup"><span data-stu-id="fb7f2-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="fb7f2-116">_Пккатегориес_</span><span class="sxs-lookup"><span data-stu-id="fb7f2-116">_pcCategories_</span></span>
  
> <span data-ttu-id="fb7f2-117">вышли Количество категорий в _пргклсидкатегори_.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="fb7f2-118">_Пргклсидкатегори_</span><span class="sxs-lookup"><span data-stu-id="fb7f2-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="fb7f2-119">вышли Массив категорий, с которыми связана эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="fb7f2-120">Массив имеет размер \* _пккатегориес_.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="fb7f2-121">Значение каждой категории в массиве должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="fb7f2-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="fb7f2-122">Клсид_олкмаил</span><span class="sxs-lookup"><span data-stu-id="fb7f2-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="fb7f2-123">Клсид_олкаддрессбук</span><span class="sxs-lookup"><span data-stu-id="fb7f2-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="fb7f2-124">Клсид_олксторе</span><span class="sxs-lookup"><span data-stu-id="fb7f2-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fb7f2-125">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fb7f2-125">Return values</span></span>

<span data-ttu-id="fb7f2-126">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb7f2-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="fb7f2-127">Remarks</span></span>

<span data-ttu-id="fb7f2-128">После возврата этого метода необходимо освободить *пргклсидкатегори* с помощью [Иолкаккаунт:: фримемори](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="fb7f2-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="fb7f2-129">**Иолкаккаунт:: жетаккаунтинфо** не поддерживает категорию адресной книги для учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="fb7f2-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="fb7f2-130">Если учетная запись является учетной записью Exchange (*пклсидтипе* — **клсид_олкмапиаккаунт** ), а учетная запись реализует адресную книгу, вызов **иолкаккаунт:: Жетаккаунтинфо** не будет возвращать **клсид_олкаддрессбук** в качестве категории в \* Пргклсидкатегори\* .</span><span class="sxs-lookup"><span data-stu-id="fb7f2-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb7f2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="fb7f2-131">See also</span></span>

- [<span data-ttu-id="fb7f2-132">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="fb7f2-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="fb7f2-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="fb7f2-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

