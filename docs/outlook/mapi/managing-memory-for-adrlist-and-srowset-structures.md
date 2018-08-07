---
title: Управление памятью для структуры ADRLIST и SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ab582b869fb5a53d7ac4e97e039d9bde4a4f0430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809681"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="34707-103">Управление памятью для структуры ADRLIST и SRowSet»</span><span class="sxs-lookup"><span data-stu-id="34707-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="34707-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34707-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34707-105">Требования для выделения памяти все буфера, когда это возможно с помощью одного вызова **MAPIAllocateBuffer** не применяется при использовании списка адресов или **ADRLIST**и набор строк или **SRowSet**структуры.</span><span class="sxs-lookup"><span data-stu-id="34707-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="34707-106">Эти две структуры, исключения из стандартного правил для распределения и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="34707-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="34707-107">Они содержат несколько уровней структуры, которые предназначены для включения отдельные элементы, чтобы добавить или удалить.</span><span class="sxs-lookup"><span data-stu-id="34707-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="34707-108">Таким образом каждое свойство должно быть отдельные выделения.</span><span class="sxs-lookup"><span data-stu-id="34707-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="34707-109">Где большинство структур высвобождаются с помощью одного вызова к **MAPIFreeBuffer**, каждая отдельная запись **ADRLIST** или **SRowSet** структура освобождения с собственной вызов **MAPIFreeBuffer** или один вызов **FreeProws** или ** FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="34707-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="34707-110">Для получения дополнительных сведений см [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)и [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="34707-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="34707-111">**FreeProws** и **FreePadrlist** являются функций, предоставляемых MAPI для упрощения освобождение эти структуры данных.</span><span class="sxs-lookup"><span data-stu-id="34707-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="34707-112">Для получения дополнительных сведений см [FreeProws](freeprows.md) и [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="34707-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="34707-113">**FreePadrlist** освобождает память для структуры **ADRLIST** , а также все связанные с ним памяти членов структуры. **FreeProws** делает то же самое для структуры **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="34707-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="34707-114">На следующей схеме показана макет структуру данных **ADRLIST** , указывающее, отдельные необходимые там.</span><span class="sxs-lookup"><span data-stu-id="34707-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="34707-115">Серая поля показывают объем памяти, который можно выделить и выпущен с помощью одного вызова.</span><span class="sxs-lookup"><span data-stu-id="34707-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="34707-116">**Выделение памяти ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="34707-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="34707-117">![Выделение памяти adrlist] (media/amapi_52.gif "Выделение памяти adrlist")</span><span class="sxs-lookup"><span data-stu-id="34707-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34707-118">См. также</span><span class="sxs-lookup"><span data-stu-id="34707-118">See also</span></span>

- [<span data-ttu-id="34707-119">Управление памятью в MAPI</span><span class="sxs-lookup"><span data-stu-id="34707-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

