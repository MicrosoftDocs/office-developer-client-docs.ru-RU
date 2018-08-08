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
ms.openlocfilehash: e485079de800c63b02d71b3c3ccb90d66101c64b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809769"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="747e8-103">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="747e8-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="747e8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="747e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="747e8-105">Документация для каждого интерфейса состоит из вводный раздел, который содержит краткое описание назначения интерфейса следуют таблицы, содержащей следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="747e8-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="747e8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="747e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="747e8-107">Файл заголовка, где интерфейс определен и, должны быть включены при компиляции исходного кода.</span><span class="sxs-lookup"><span data-stu-id="747e8-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="747e8-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="747e8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="747e8-109">Объект, который предоставляет доступ к интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="747e8-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="747e8-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="747e8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="747e8-111">Список компонентов, которые обеспечивают реализация интерфейса.</span><span class="sxs-lookup"><span data-stu-id="747e8-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="747e8-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="747e8-112">Called by:</span></span>  <br/> |<span data-ttu-id="747e8-113">Список компонентов, которые обычно могут вызывать методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="747e8-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="747e8-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="747e8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="747e8-115">Идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="747e8-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="747e8-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="747e8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="747e8-117">Тип указателя для объекта, который предоставляет доступ к интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="747e8-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="747e8-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="747e8-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="747e8-119">Для интерфейсов, полученных от [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="747e8-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="747e8-120">Если не входящих в транзакции, изменения вступят в силу немедленно; Если в рамках транзакции, изменения не вступят в силу до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="747e8-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="747e8-121">После первой таблицы является другой таблицей, в котором приведены все методы этого интерфейса в порядке vtable.</span><span class="sxs-lookup"><span data-stu-id="747e8-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="747e8-122">Таблица представляет собой массив из указателей функций, созданных компилятором, содержащий один указатель функции для каждого метода объект MAPI.</span><span class="sxs-lookup"><span data-stu-id="747e8-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="747e8-123">Методы, перечислены в том же порядке, в том, что они объявлены.</span><span class="sxs-lookup"><span data-stu-id="747e8-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="747e8-124">Методы, наследуемые от других интерфейсов в порядке Vtable таблицы не отображаются, но можно использовать так же, как описано в интерфейс, который определяет их.</span><span class="sxs-lookup"><span data-stu-id="747e8-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="747e8-125">После каждого раздела интерфейс методов интерфейса, затем приведены в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="747e8-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="747e8-126">Для каждого метода Документация включает краткое цель инструкции, синтаксис блока и следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="747e8-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="747e8-127">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="747e8-127">**Heading**</span></span>|<span data-ttu-id="747e8-128">**Контентная**</span><span class="sxs-lookup"><span data-stu-id="747e8-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="747e8-129">Параметры</span><span class="sxs-lookup"><span data-stu-id="747e8-129">Parameters</span></span>  <br/> |<span data-ttu-id="747e8-130">Описание каждого параметра метода.</span><span class="sxs-lookup"><span data-stu-id="747e8-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="747e8-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="747e8-131">Return Value</span></span>  <br/> |<span data-ttu-id="747e8-132">Описание уникальные значения, которые можно вернуть метода.</span><span class="sxs-lookup"><span data-stu-id="747e8-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="747e8-133">Далее представлены значения, которые должно проверять звонящих в своем коде.</span><span class="sxs-lookup"><span data-stu-id="747e8-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="747e8-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="747e8-134">Remarks</span></span>  <br/> |<span data-ttu-id="747e8-135">Описание причины и как используется метод.</span><span class="sxs-lookup"><span data-stu-id="747e8-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="747e8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="747e8-136">See Also</span></span>  <br/> |<span data-ttu-id="747e8-137">Перекрестные ссылки на другие разделы в этой справке.</span><span class="sxs-lookup"><span data-stu-id="747e8-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="747e8-138">См. также</span><span class="sxs-lookup"><span data-stu-id="747e8-138">See also</span></span>



[<span data-ttu-id="747e8-139">Справочник по MAPI</span><span class="sxs-lookup"><span data-stu-id="747e8-139">MAPI Reference</span></span>](mapi-reference.md)

