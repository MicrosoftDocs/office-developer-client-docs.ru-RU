---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Определяет, могут ли страницы в документе дублироваться в виде логического значения.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439662"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="033fc-103">DocLockDuplicatePage Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="033fc-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="033fc-104">Определяет, могут ли страницы в документе дублироваться в виде логического значения.</span><span class="sxs-lookup"><span data-stu-id="033fc-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="033fc-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="033fc-105">TRUE</span></span>  <br/> |<span data-ttu-id="033fc-106">**Дублировать** в контекстном меню страницы и на **странице. повторяющиеся** методы автоматизации отключены.</span><span class="sxs-lookup"><span data-stu-id="033fc-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="033fc-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="033fc-107">FALSE</span></span>  <br/> |<span data-ttu-id="033fc-108">Страница может дублироваться.</span><span class="sxs-lookup"><span data-stu-id="033fc-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="033fc-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="033fc-109">Remarks</span></span>

<span data-ttu-id="033fc-110">Чтобы получить ссылку на ячейку **DocLockDuplicatePage** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="033fc-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="033fc-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="033fc-111">Cell name:</span></span>  <br/> | <span data-ttu-id="033fc-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="033fc-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="033fc-113">Чтобы получить ссылку на ячейку **DocLockDuplicatePage** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="033fc-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="033fc-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="033fc-114">Section index:</span></span>  <br/> |<span data-ttu-id="033fc-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="033fc-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="033fc-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="033fc-116">Row index:</span></span>  <br/> |<span data-ttu-id="033fc-117">**Висровдок**</span><span class="sxs-lookup"><span data-stu-id="033fc-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="033fc-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="033fc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="033fc-119">**Висдоклоккдупликатепаже**</span><span class="sxs-lookup"><span data-stu-id="033fc-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

