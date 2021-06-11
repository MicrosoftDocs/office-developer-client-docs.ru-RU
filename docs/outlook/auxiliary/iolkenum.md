---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322101"
---
# <a name="iolkenum"></a><span data-ttu-id="8104b-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="8104b-102">IOlkEnum</span></span>

<span data-ttu-id="8104b-103">Поддерживает учетные записи в качестве [объектов IUnknown.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="8104b-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8104b-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8104b-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8104b-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="8104b-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="8104b-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="8104b-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="8104b-107">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8104b-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="8104b-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="8104b-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="8104b-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="8104b-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="8104b-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="8104b-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="8104b-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8104b-111">Called by:</span></span>  <br/> |<span data-ttu-id="8104b-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="8104b-112">Client</span></span>  <br/> |
|<span data-ttu-id="8104b-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8104b-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8104b-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="8104b-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8104b-115">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="8104b-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8104b-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="8104b-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="8104b-117">Получает количество учетных записей в этом переуметоре.</span><span class="sxs-lookup"><span data-stu-id="8104b-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="8104b-118">Reset</span><span class="sxs-lookup"><span data-stu-id="8104b-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="8104b-119">Сбрасывает переустановку в начале.</span><span class="sxs-lookup"><span data-stu-id="8104b-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="8104b-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="8104b-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="8104b-121">Получает следующую учетную запись в переуметоре.</span><span class="sxs-lookup"><span data-stu-id="8104b-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="8104b-122">Skip</span><span class="sxs-lookup"><span data-stu-id="8104b-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="8104b-123">Пропускает указанное количество учетных записей в этом переуметоре.</span><span class="sxs-lookup"><span data-stu-id="8104b-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8104b-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="8104b-124">Remarks</span></span>

<span data-ttu-id="8104b-125">Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении переучета учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8104b-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8104b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8104b-126">See also</span></span>

- [<span data-ttu-id="8104b-127">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="8104b-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="8104b-128">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="8104b-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

