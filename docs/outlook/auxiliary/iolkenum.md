---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807880"
---
# <a name="iolkenum"></a><span data-ttu-id="bb736-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="bb736-102">IOlkEnum</span></span>

<span data-ttu-id="bb736-103">Поддерживает перечисления учетных записей как объекты [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bb736-103">Supports enumerating accounts as [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bb736-104">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bb736-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb736-105">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="bb736-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="bb736-106">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb736-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="bb736-107">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="bb736-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="bb736-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="bb736-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="bb736-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="bb736-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="bb736-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="bb736-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="bb736-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="bb736-111">Called by:</span></span>  <br/> |<span data-ttu-id="bb736-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="bb736-112">Client</span></span>  <br/> |
|<span data-ttu-id="bb736-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="bb736-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bb736-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="bb736-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bb736-115">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="bb736-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bb736-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="bb736-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="bb736-117">Получает число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="bb736-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="bb736-118">Сброс</span><span class="sxs-lookup"><span data-stu-id="bb736-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="bb736-119">Сбрасывает перечислитель к началу.</span><span class="sxs-lookup"><span data-stu-id="bb736-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="bb736-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="bb736-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="bb736-121">Получает перечислитель следующего учетной записи.</span><span class="sxs-lookup"><span data-stu-id="bb736-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="bb736-122">Пропустить</span><span class="sxs-lookup"><span data-stu-id="bb736-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="bb736-123">Пропускает указанное число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="bb736-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb736-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="bb736-124">Remarks</span></span>

<span data-ttu-id="bb736-125">Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении перечислитель учетных записей.</span><span class="sxs-lookup"><span data-stu-id="bb736-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb736-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bb736-126">See also</span></span>

- [<span data-ttu-id="bb736-127">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="bb736-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="bb736-128">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="bb736-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

