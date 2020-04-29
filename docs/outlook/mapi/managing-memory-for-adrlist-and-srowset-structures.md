---
title: Управление памятью для структур ADRLIST и SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407867"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="080dc-103">Управление памятью для структур ADRLIST и SRowSet»</span><span class="sxs-lookup"><span data-stu-id="080dc-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="080dc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="080dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="080dc-105">Требование выделять всю память для буфера везде, где это возможно, при использовании одного вызова **мапиаллокатебуффер** не применяется при использовании списка адресов, **ADRLIST**, набора строк или **SRowSet**структуры.</span><span class="sxs-lookup"><span data-stu-id="080dc-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="080dc-106">Эти две структуры представляют собой исключения из стандартных правил выделения и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="080dc-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="080dc-107">Они содержат несколько уровней структуры и предназначены для добавления или удаления отдельных членов.</span><span class="sxs-lookup"><span data-stu-id="080dc-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="080dc-108">Таким образом, каждое свойство должно быть отдельным выделением.</span><span class="sxs-lookup"><span data-stu-id="080dc-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="080dc-109">Где большинство структур освобождаются с одним вызовом **мапифрибуффер**, каждая отдельная запись в структуре **ADRLIST** или **SRowSet** должна быть освобождена с помощью собственного вызова **Мапифрибуффер** или одного вызова в **фрипровс** или **фрипадрлист**.</span><span class="sxs-lookup"><span data-stu-id="080dc-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="080dc-110">Дополнительные сведения см. в статье [мапифрибуффер](mapifreebuffer.md), [ADRLIST](adrlist.md)и [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="080dc-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="080dc-111">**Фрипровс** и **фрипадрлист** — это функции, предоставляемые MAPI для упрощения освобождения этих структур данных.</span><span class="sxs-lookup"><span data-stu-id="080dc-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="080dc-112">Дополнительные сведения см. в статье [фрипровс](freeprows.md) and [фрипадрлист](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="080dc-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="080dc-113">**Фрипадрлист** освобождает память для структуры **ADRLIST** , а также всю связанную память для членов структуры; **Фрипровс** выполняет те же функции для структуры **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="080dc-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="080dc-114">На следующей схеме показана структура структуры данных **ADRLIST** , указывающая на необходимость в отдельных выделениях памяти.</span><span class="sxs-lookup"><span data-stu-id="080dc-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="080dc-115">В серых полях отображается память, которая может быть выделена и освобождена с помощью одного вызова.</span><span class="sxs-lookup"><span data-stu-id="080dc-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="080dc-116">**Выделение памяти ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="080dc-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="080dc-117">Выделение ![памяти ADRLIST](media/amapi_52.gif "ADRLIST выделение памяти")</span><span class="sxs-lookup"><span data-stu-id="080dc-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="080dc-118">См. также</span><span class="sxs-lookup"><span data-stu-id="080dc-118">See also</span></span>

- [<span data-ttu-id="080dc-119">Управление памятью в MAPI</span><span class="sxs-lookup"><span data-stu-id="080dc-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

