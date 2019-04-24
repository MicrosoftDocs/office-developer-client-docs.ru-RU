---
title: Иолкаккаунтманажерфиндаккаунт
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Находит учетную запись по значению свойства.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322080"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="daa77-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="daa77-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="daa77-104">Находит учетную запись по значению свойства.</span><span class="sxs-lookup"><span data-stu-id="daa77-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="daa77-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="daa77-105">Quick info</span></span>

<span data-ttu-id="daa77-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="daa77-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="daa77-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="daa77-107">Parameters</span></span>

<span data-ttu-id="daa77-108">_Двпроп_</span><span class="sxs-lookup"><span data-stu-id="daa77-108">_dwProp_</span></span>
  
> <span data-ttu-id="daa77-109">возврата Свойство, по которому необходимо выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="daa77-109">[in] The property to search on.</span></span> <span data-ttu-id="daa77-110">Должен быть [проп_аккт_ид](prop_acct_id.md) или [проп_аккт_ис_ексч](prop_acct_is_exch.md).</span><span class="sxs-lookup"><span data-stu-id="daa77-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="daa77-111">_ПВАР_</span><span class="sxs-lookup"><span data-stu-id="daa77-111">_pVar_</span></span>
  
> <span data-ttu-id="daa77-112">возврата Значение для сравнения.</span><span class="sxs-lookup"><span data-stu-id="daa77-112">[in] The value to match.</span></span>
    
<span data-ttu-id="daa77-113">_Ппаккаунт_</span><span class="sxs-lookup"><span data-stu-id="daa77-113">_ppAccount_</span></span>
  
> <span data-ttu-id="daa77-114">вышли Учетная запись найдена.</span><span class="sxs-lookup"><span data-stu-id="daa77-114">[out] The account found.</span></span> <span data-ttu-id="daa77-115">Этот объект поддерживает интерфейс [иолкаккаунт](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="daa77-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="daa77-116">Return values</span></span>

|<span data-ttu-id="daa77-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="daa77-117">**HRESULT**</span></span>|<span data-ttu-id="daa77-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="daa77-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="daa77-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="daa77-119">S_OK</span></span>  <br/> |<span data-ttu-id="daa77-120">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="daa77-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="daa77-121">Е_АККТ_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="daa77-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="daa77-122">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="daa77-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="daa77-123">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="daa77-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="daa77-124">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="daa77-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="daa77-125">Е_ОЛК_ПАРАМ_НОТ_СУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="daa77-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="daa77-126">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="daa77-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daa77-127">См. также</span><span class="sxs-lookup"><span data-stu-id="daa77-127">See also</span></span>

- [<span data-ttu-id="daa77-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="daa77-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="daa77-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="daa77-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="daa77-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="daa77-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

