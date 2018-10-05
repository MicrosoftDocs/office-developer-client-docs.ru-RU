---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389738"
---
# <a name="iolkenum"></a><span data-ttu-id="4d3dd-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="4d3dd-102">IOlkEnum</span></span>

<span data-ttu-id="4d3dd-103">Поддерживает перечисления учетных записей как объекты [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4d3dd-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4d3dd-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4d3dd-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d3dd-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="4d3dd-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="4d3dd-106">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d3dd-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="4d3dd-107">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4d3dd-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="4d3dd-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="4d3dd-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="4d3dd-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="4d3dd-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="4d3dd-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="4d3dd-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="4d3dd-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4d3dd-111">Called by:</span></span>  <br/> |<span data-ttu-id="4d3dd-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="4d3dd-112">Client</span></span>  <br/> |
|<span data-ttu-id="4d3dd-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="4d3dd-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4d3dd-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="4d3dd-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4d3dd-115">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="4d3dd-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4d3dd-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="4d3dd-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="4d3dd-117">Получает число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="4d3dd-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="4d3dd-118">Reset (Сбросить)</span><span class="sxs-lookup"><span data-stu-id="4d3dd-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="4d3dd-119">Сбрасывает перечислитель к началу.</span><span class="sxs-lookup"><span data-stu-id="4d3dd-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="4d3dd-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="4d3dd-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="4d3dd-121">Получает перечислитель следующего учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4d3dd-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="4d3dd-122">Пропустить</span><span class="sxs-lookup"><span data-stu-id="4d3dd-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="4d3dd-123">Пропускает указанное число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="4d3dd-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d3dd-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d3dd-124">Remarks</span></span>

<span data-ttu-id="4d3dd-125">Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении перечислитель учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4d3dd-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d3dd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="4d3dd-126">See also</span></span>

- [<span data-ttu-id="4d3dd-127">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="4d3dd-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="4d3dd-128">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="4d3dd-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

