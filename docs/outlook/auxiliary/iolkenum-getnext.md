---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Получает следующую учетную запись в переуметоре.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405991"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="97976-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="97976-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="97976-104">Получает следующую учетную запись в переуметоре.</span><span class="sxs-lookup"><span data-stu-id="97976-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="97976-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="97976-105">Quick info</span></span>

<span data-ttu-id="97976-106">См. [iOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="97976-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="97976-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="97976-107">Parameters</span></span>

<span data-ttu-id="97976-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="97976-108">_ppunk_</span></span>
  
> <span data-ttu-id="97976-109">[in] Указатель на **интерфейс IUnknown,** который клиент может запрашивать для получения [интерфейса IOlkAccount.](iolkaccount.md)</span><span class="sxs-lookup"><span data-stu-id="97976-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="97976-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="97976-110">Return values</span></span>

|<span data-ttu-id="97976-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="97976-111">**HRESULT**</span></span>|<span data-ttu-id="97976-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="97976-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97976-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="97976-113">S_OK</span></span>  <br/> |<span data-ttu-id="97976-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="97976-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="97976-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="97976-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="97976-116">Переумывчик достиг конца.</span><span class="sxs-lookup"><span data-stu-id="97976-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97976-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="97976-117">Remarks</span></span>

<span data-ttu-id="97976-118">Интерфейс, указанный  *ppunk наследует* **от IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="97976-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="97976-119">Клиент может запрашивать этот интерфейс (с помощью **IUnknown::QueryInterface)** для получения указателя на **интерфейс IOlkAccount** и получения или набора сведений для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="97976-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97976-120">См. также</span><span class="sxs-lookup"><span data-stu-id="97976-120">See also</span></span>

- [<span data-ttu-id="97976-121">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="97976-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="97976-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="97976-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="97976-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="97976-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="97976-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="97976-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

