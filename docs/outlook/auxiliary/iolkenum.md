---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592691"
---
# <a name="iolkenum"></a><span data-ttu-id="9600d-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="9600d-102">IOlkEnum</span></span>

<span data-ttu-id="9600d-103">Поддерживает перечисления учетных записей как объекты [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9600d-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9600d-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9600d-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9600d-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="9600d-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="9600d-106">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="9600d-106">IUnknown</span></span>](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="9600d-107">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9600d-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="9600d-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="9600d-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="9600d-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="9600d-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="9600d-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="9600d-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="9600d-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9600d-111">Called by:</span></span>  <br/> |<span data-ttu-id="9600d-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="9600d-112">Client</span></span>  <br/> |
|<span data-ttu-id="9600d-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9600d-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9600d-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="9600d-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9600d-115">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="9600d-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9600d-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="9600d-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="9600d-117">Получает число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="9600d-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="9600d-118">Reset (Сбросить)</span><span class="sxs-lookup"><span data-stu-id="9600d-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="9600d-119">Сбрасывает перечислитель к началу.</span><span class="sxs-lookup"><span data-stu-id="9600d-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="9600d-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="9600d-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="9600d-121">Получает перечислитель следующего учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9600d-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="9600d-122">Пропустить</span><span class="sxs-lookup"><span data-stu-id="9600d-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="9600d-123">Пропускает указанное число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="9600d-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9600d-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="9600d-124">Remarks</span></span>

<span data-ttu-id="9600d-125">Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении перечислитель учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9600d-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9600d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9600d-126">See also</span></span>

- [<span data-ttu-id="9600d-127">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="9600d-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="9600d-128">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="9600d-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

