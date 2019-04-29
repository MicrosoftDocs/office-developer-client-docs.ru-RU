---
title: Иолкенумжетнекст
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Получает следующую учетную запись в перечислителе.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405991"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="7da3b-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="7da3b-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="7da3b-104">Получает следующую учетную запись в перечислителе.</span><span class="sxs-lookup"><span data-stu-id="7da3b-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7da3b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7da3b-105">Quick info</span></span>

<span data-ttu-id="7da3b-106">Обратитесь к разделу [иолкенум](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="7da3b-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="7da3b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7da3b-107">Parameters</span></span>

<span data-ttu-id="7da3b-108">_ппунк_</span><span class="sxs-lookup"><span data-stu-id="7da3b-108">_ppunk_</span></span>
  
> <span data-ttu-id="7da3b-109">возврата Указатель на интерфейс **IUnknown** , который клиент может запрашивать для получения интерфейса [иолкаккаунт](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="7da3b-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7da3b-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7da3b-110">Return values</span></span>

|<span data-ttu-id="7da3b-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7da3b-111">**HRESULT**</span></span>|<span data-ttu-id="7da3b-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="7da3b-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7da3b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7da3b-113">S_OK</span></span>  <br/> |<span data-ttu-id="7da3b-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="7da3b-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="7da3b-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7da3b-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="7da3b-116">Достигнут конец перечислителя.</span><span class="sxs-lookup"><span data-stu-id="7da3b-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7da3b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="7da3b-117">Remarks</span></span>

<span data-ttu-id="7da3b-118">Интерфейс, указанный *ппунк* , наследуется от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="7da3b-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="7da3b-119">Клиент может запросить этот интерфейс (с помощью **IUnknown:: QueryInterface**), чтобы получить указатель на интерфейс **иолкаккаунт** , а также получить или задать сведения для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7da3b-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7da3b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7da3b-120">See also</span></span>

- [<span data-ttu-id="7da3b-121">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="7da3b-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="7da3b-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="7da3b-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="7da3b-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="7da3b-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="7da3b-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="7da3b-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

