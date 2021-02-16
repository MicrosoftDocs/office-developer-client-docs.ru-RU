---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Определяет, следует ли отключить пользовательский интерфейс фигуры замены для этого документа.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413425"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="d415a-103">DocLockReplace Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="d415a-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="d415a-104">Определяет, следует ли отключить пользовательский интерфейс фигуры замены для этого документа.</span><span class="sxs-lookup"><span data-stu-id="d415a-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d415a-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="d415a-105">TRUE</span></span>  <br/> |<span data-ttu-id="d415a-106">Кнопка **"Заменить** фигуру" неауловимая в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d415a-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="d415a-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="d415a-107">FALSE</span></span>  <br/> |<span data-ttu-id="d415a-108">Кнопка **"Заменить** фигуру" активна в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d415a-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="d415a-109">Пользователи могут использовать функцию замены фигуры в этом документе.</span><span class="sxs-lookup"><span data-stu-id="d415a-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d415a-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d415a-110">Remarks</span></span>

<span data-ttu-id="d415a-111">Чтобы получить ссылку на ячейку **DocLockReplace** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d415a-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d415a-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d415a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="d415a-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="d415a-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="d415a-114">Чтобы получить ссылку на ячейку **DocLocReplace** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d415a-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d415a-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d415a-115">Section index:</span></span>  <br/> |<span data-ttu-id="d415a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d415a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d415a-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d415a-117">Row index:</span></span>  <br/> |<span data-ttu-id="d415a-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="d415a-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="d415a-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d415a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="d415a-120">\*\*visDocLockReplace \*\*</span><span class="sxs-lookup"><span data-stu-id="d415a-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

