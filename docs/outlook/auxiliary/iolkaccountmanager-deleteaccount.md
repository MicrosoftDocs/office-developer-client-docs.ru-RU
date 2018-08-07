---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Удаляет указанную учетную запись.
ms.openlocfilehash: 1c0b246af10dac1af9c61f368d082a92c7b3616a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807847"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="7d24f-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="7d24f-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="7d24f-104">Удаляет указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="7d24f-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7d24f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7d24f-105">Quick info</span></span>

<span data-ttu-id="7d24f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7d24f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="7d24f-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d24f-107">Parameters</span></span>

<span data-ttu-id="7d24f-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="7d24f-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="7d24f-109">[in] Идентификатор учетной записи для удаления учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7d24f-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7d24f-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7d24f-110">Return values</span></span>

|<span data-ttu-id="7d24f-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7d24f-111">**HRESULT**</span></span>|<span data-ttu-id="7d24f-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d24f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d24f-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7d24f-113">S_OK</span></span>  <br/> |<span data-ttu-id="7d24f-114">Вызов успешно завершен</span><span class="sxs-lookup"><span data-stu-id="7d24f-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="7d24f-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7d24f-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="7d24f-116">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="7d24f-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="7d24f-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7d24f-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7d24f-118">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="7d24f-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d24f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7d24f-119">See also</span></span>

- [<span data-ttu-id="7d24f-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="7d24f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="7d24f-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="7d24f-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

