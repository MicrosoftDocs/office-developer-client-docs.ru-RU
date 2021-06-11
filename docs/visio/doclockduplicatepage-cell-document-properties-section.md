---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Определяет, можно ли дублировать страницы в документе, как boolean.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439662"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="6260f-103">DocLockDuplicatePage Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="6260f-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="6260f-104">Определяет, можно ли дублировать страницы в документе, как boolean.</span><span class="sxs-lookup"><span data-stu-id="6260f-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6260f-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="6260f-105">TRUE</span></span>  <br/> |<span data-ttu-id="6260f-106">**Дубликат** в меню ярлыка страницы и **метод автоматизации Page.Duplicate** отключены.</span><span class="sxs-lookup"><span data-stu-id="6260f-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="6260f-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="6260f-107">FALSE</span></span>  <br/> |<span data-ttu-id="6260f-108">Страницу можно дублировать.</span><span class="sxs-lookup"><span data-stu-id="6260f-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6260f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="6260f-109">Remarks</span></span>

<span data-ttu-id="6260f-110">Чтобы получить ссылку на **ячейку DocLockDuplicatePage** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="6260f-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6260f-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6260f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="6260f-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="6260f-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="6260f-113">Чтобы получить ссылку на **ячейку DocLockDuplicatePage** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6260f-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6260f-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6260f-114">Section index:</span></span>  <br/> |<span data-ttu-id="6260f-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6260f-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6260f-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6260f-116">Row index:</span></span>  <br/> |<span data-ttu-id="6260f-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="6260f-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="6260f-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6260f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6260f-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="6260f-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

