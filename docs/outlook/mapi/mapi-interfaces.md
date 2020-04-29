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
# <a name="mapi-interfaces"></a><span data-ttu-id="c07e9-103">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="c07e9-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="c07e9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c07e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c07e9-105">Документация по каждому интерфейсу состоит из вводного раздела, содержащего краткое описание назначения интерфейса, за которым следует таблица, содержащая следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="c07e9-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c07e9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c07e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="c07e9-107">Файл заголовка, в котором определен интерфейс, и который необходимо включить при компиляции исходного кода.</span><span class="sxs-lookup"><span data-stu-id="c07e9-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="c07e9-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="c07e9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c07e9-109">Объект, предоставляющий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c07e9-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="c07e9-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c07e9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c07e9-111">Список компонентов, предоставляющих реализацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c07e9-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="c07e9-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c07e9-112">Called by:</span></span>  <br/> |<span data-ttu-id="c07e9-113">Список компонентов, которые обычно вызывают методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c07e9-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="c07e9-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="c07e9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c07e9-115">GUID идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c07e9-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="c07e9-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="c07e9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c07e9-117">Тип указателя для объекта, предоставляющего интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c07e9-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="c07e9-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="c07e9-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="c07e9-119">Для интерфейсов, производных от [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c07e9-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="c07e9-120">В противном случае изменения вступают в силу немедленно; в противном случае изменения вступают в силу только после вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="c07e9-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="c07e9-121">После первой таблицы приведена другая таблица, в которой перечислены все методы этого интерфейса в порядке vtable.</span><span class="sxs-lookup"><span data-stu-id="c07e9-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="c07e9-122">Виртуальная таблица — это массив указателей на функции, созданный компилятором, содержащим один указатель функции для каждого метода объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="c07e9-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="c07e9-123">Методы перечислены в том же порядке, в котором они объявляются.</span><span class="sxs-lookup"><span data-stu-id="c07e9-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="c07e9-124">Методы, наследуемые от других интерфейсов, не отображаются в таблице порядка vtable, но их можно использовать так же, как и в описании в интерфейсе, в котором они определены.</span><span class="sxs-lookup"><span data-stu-id="c07e9-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="c07e9-125">После каждого раздела Interface методы интерфейса задокументированы в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="c07e9-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="c07e9-126">Для каждого метода документация включает в себя оператор краткого назначения, блок синтаксиса и следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="c07e9-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="c07e9-127">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c07e9-127">**Heading**</span></span>|<span data-ttu-id="c07e9-128">**Статья**</span><span class="sxs-lookup"><span data-stu-id="c07e9-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c07e9-129">Параметры</span><span class="sxs-lookup"><span data-stu-id="c07e9-129">Parameters</span></span>  <br/> |<span data-ttu-id="c07e9-130">Описание каждого параметра в методе.</span><span class="sxs-lookup"><span data-stu-id="c07e9-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="c07e9-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c07e9-131">Return Value</span></span>  <br/> |<span data-ttu-id="c07e9-132">Описание уникальных значений, которые может возвращать метод.</span><span class="sxs-lookup"><span data-stu-id="c07e9-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="c07e9-133">Ниже приведены значения, по которым абоненты должны проверять код.</span><span class="sxs-lookup"><span data-stu-id="c07e9-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="c07e9-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="c07e9-134">Remarks</span></span>  <br/> |<span data-ttu-id="c07e9-135">Описание причин и способа использования метода.</span><span class="sxs-lookup"><span data-stu-id="c07e9-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="c07e9-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c07e9-136">See Also</span></span>  <br/> |<span data-ttu-id="c07e9-137">Перекрестные ссылки на другие темы в этой справочной ссылке.</span><span class="sxs-lookup"><span data-stu-id="c07e9-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c07e9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c07e9-138">See also</span></span>



[<span data-ttu-id="c07e9-139">Справочник по MAPI</span><span class="sxs-lookup"><span data-stu-id="c07e9-139">MAPI Reference</span></span>](mapi-reference.md)

