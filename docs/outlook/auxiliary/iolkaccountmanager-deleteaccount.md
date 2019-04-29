---
title: Иолкаккаунтманажерделетеаккаунт
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Удаляет указанную учетную запись.
ms.openlocfilehash: 3e39b7b9af57f64dd124e1bf836db68664709b8c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431241"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="f3f08-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="f3f08-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="f3f08-104">Удаляет указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f3f08-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f3f08-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f3f08-105">Quick info</span></span>

<span data-ttu-id="f3f08-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f3f08-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="f3f08-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3f08-107">Parameters</span></span>

<span data-ttu-id="f3f08-108">_Двакктид_</span><span class="sxs-lookup"><span data-stu-id="f3f08-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="f3f08-109">возврата Идентификатор учетной записи, которая должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="f3f08-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f3f08-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f3f08-110">Return values</span></span>

|<span data-ttu-id="f3f08-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f3f08-111">**HRESULT**</span></span>|<span data-ttu-id="f3f08-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="f3f08-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3f08-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3f08-113">S_OK</span></span>  <br/> |<span data-ttu-id="f3f08-114">Вызов выполнен успешно</span><span class="sxs-lookup"><span data-stu-id="f3f08-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="f3f08-115">Е_АККТ_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="f3f08-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="f3f08-116">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f3f08-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="f3f08-117">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="f3f08-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f3f08-118">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="f3f08-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3f08-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f3f08-119">See also</span></span>

- [<span data-ttu-id="f3f08-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="f3f08-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="f3f08-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="f3f08-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

