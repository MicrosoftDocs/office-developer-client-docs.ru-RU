---
title: Иолкаккаунтманажержетордер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает упорядочивание указанной категории учетных записей.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424625"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="c7baa-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="c7baa-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="c7baa-104">Получает упорядочивание указанной категории учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c7baa-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c7baa-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c7baa-105">Quick info</span></span>

<span data-ttu-id="c7baa-106">Просмотр [иолкаккаунтманажер](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="c7baa-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="c7baa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7baa-107">Parameters</span></span>

<span data-ttu-id="c7baa-108">_Пклсидкатегори_</span><span class="sxs-lookup"><span data-stu-id="c7baa-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="c7baa-109">возврата Идентификатор класса Category, для которого требуется получить порядок.</span><span class="sxs-lookup"><span data-stu-id="c7baa-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="c7baa-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="c7baa-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="c7baa-111">Клсид_олкмаил</span><span class="sxs-lookup"><span data-stu-id="c7baa-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="c7baa-112">Клсид_олкаддрессбук</span><span class="sxs-lookup"><span data-stu-id="c7baa-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="c7baa-113">Клсид_олксторе</span><span class="sxs-lookup"><span data-stu-id="c7baa-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="c7baa-114">_Пкакктс_</span><span class="sxs-lookup"><span data-stu-id="c7baa-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="c7baa-115">вышли Число учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c7baa-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="c7baa-116">_Пргакктс_</span><span class="sxs-lookup"><span data-stu-id="c7baa-116">_prgAccts_</span></span>
  
> <span data-ttu-id="c7baa-117">вышли Указатель на массив учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c7baa-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c7baa-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c7baa-118">Return values</span></span>

|<span data-ttu-id="c7baa-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c7baa-119">**HRESULT**</span></span>|<span data-ttu-id="c7baa-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="c7baa-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7baa-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7baa-121">S_OK</span></span>  <br/> |<span data-ttu-id="c7baa-122">Вызов выполнен успешно</span><span class="sxs-lookup"><span data-stu-id="c7baa-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="c7baa-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c7baa-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="c7baa-124">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="c7baa-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="c7baa-125">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="c7baa-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c7baa-126">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="c7baa-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7baa-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7baa-127">Remarks</span></span>

<span data-ttu-id="c7baa-128">Перед вызовом этого метода вызывающий абонент выделяет только указатель массива *пргакктс* , но не память для массива, в котором точки *пргакктс* .</span><span class="sxs-lookup"><span data-stu-id="c7baa-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="c7baa-129">После возврата этого метода вызывающий должен использовать [иолкаккаунтманажер:: фримемори](iolkaccountmanager-freememory.md) для освобождения памяти, выделенной для *пргакктс* .</span><span class="sxs-lookup"><span data-stu-id="c7baa-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7baa-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c7baa-130">See also</span></span>

- [<span data-ttu-id="c7baa-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="c7baa-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="c7baa-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="c7baa-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

