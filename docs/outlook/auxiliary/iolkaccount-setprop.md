---
title: иолкаккаунтсетпроп
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Задает значение указанного свойства учетной записи.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431990"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="b3923-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="b3923-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="b3923-104">Задает значение указанного свойства учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b3923-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b3923-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b3923-105">Quick info</span></span>

<span data-ttu-id="b3923-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b3923-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="b3923-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3923-107">Parameters</span></span>

<span data-ttu-id="b3923-108">_двпроп_</span><span class="sxs-lookup"><span data-stu-id="b3923-108">_dwProp_</span></span>
  
> <span data-ttu-id="b3923-109">возврата Тег свойства для свойства Account, которое необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="b3923-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="b3923-110">_пвар_</span><span class="sxs-lookup"><span data-stu-id="b3923-110">_pVar_</span></span>
  
> <span data-ttu-id="b3923-111">возврата Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="b3923-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b3923-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b3923-112">Return values</span></span>

|<span data-ttu-id="b3923-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b3923-113">**HRESULT**</span></span>|<span data-ttu-id="b3923-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3923-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3923-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3923-115">S_OK</span></span>  <br/> |<span data-ttu-id="b3923-116">Вызов метода выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b3923-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="b3923-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b3923-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="b3923-118">Указан недопустимый тег свойства.</span><span class="sxs-lookup"><span data-stu-id="b3923-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3923-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3923-119">Remarks</span></span>

<span data-ttu-id="b3923-120">Используйте [иолкаккаунт:: SaveChanges](iolkaccount-savechanges.md) , чтобы сохранить изменения в значении свойств учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b3923-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3923-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b3923-121">See also</span></span>

- [<span data-ttu-id="b3923-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="b3923-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="b3923-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="b3923-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

