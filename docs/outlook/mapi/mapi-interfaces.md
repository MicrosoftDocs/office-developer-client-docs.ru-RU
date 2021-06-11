---
title: Интерфейсы MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422665"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="ec3dd-103">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ec3dd-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="ec3dd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec3dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec3dd-105">Документация для каждого интерфейса состоит из вводного раздела, в который входит краткое описание цели интерфейса, а затем таблица со следующей информацией.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec3dd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec3dd-107">Файл загона, в котором определен интерфейс и который должен быть включен при компиляции исходных кодов.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ec3dd-109">Объект, который предоставляет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ec3dd-111">Список компонентов, которые обеспечивают реализацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-112">Called by:</span></span>  <br/> |<span data-ttu-id="ec3dd-113">Список компонентов, которые обычно называют методами интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ec3dd-115">GUID идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ec3dd-117">Тип указателя для объекта, который предоставляет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="ec3dd-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="ec3dd-119">Для интерфейсов, полученных из [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ec3dd-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="ec3dd-120">Если они не принимаются, изменения вступает в силу немедленно; если они будут внесены, изменения не вступает в силу до тех пор, пока не будет [вызвана IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="ec3dd-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="ec3dd-121">За первой таблицей следует еще одна таблица, в которую перечислены все методы этого интерфейса в порядке vtable.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="ec3dd-122">Vtable — это массив указателей функций, созданных компилятором, содержащим по одной указатель функции для каждого метода объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="ec3dd-123">Методы перечислены в том же порядке, что и объявленные.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="ec3dd-124">Методы, унаследованные от других интерфейсов, не показаны в таблице Vtable Order, но могут использоваться так же, как описаны в интерфейсе, который их определяет.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="ec3dd-125">После каждой темы интерфейса методы интерфейса затем документируются в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="ec3dd-126">Для каждого метода документация включает краткое заявление о назначении, блок синтаксиса и следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="ec3dd-127">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ec3dd-127">**Heading**</span></span>|<span data-ttu-id="ec3dd-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="ec3dd-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec3dd-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="ec3dd-129">Parameters</span></span>  <br/> |<span data-ttu-id="ec3dd-130">Описание каждого параметра метода.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec3dd-131">Return Value</span></span>  <br/> |<span data-ttu-id="ec3dd-132">Описание уникальных значений, которые может возвращать метод.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="ec3dd-133">Это значения, которые должны проверяться в коде звонители.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec3dd-134">Remarks</span></span>  <br/> |<span data-ttu-id="ec3dd-135">Описание причины и способа использования метода.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="ec3dd-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ec3dd-136">See Also</span></span>  <br/> |<span data-ttu-id="ec3dd-137">Перекрестные ссылки на другие темы в этом справочнике.</span><span class="sxs-lookup"><span data-stu-id="ec3dd-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec3dd-138">См. также</span><span class="sxs-lookup"><span data-stu-id="ec3dd-138">See also</span></span>



[<span data-ttu-id="ec3dd-139">Справочник по MAPI</span><span class="sxs-lookup"><span data-stu-id="ec3dd-139">MAPI Reference</span></span>](mapi-reference.md)

