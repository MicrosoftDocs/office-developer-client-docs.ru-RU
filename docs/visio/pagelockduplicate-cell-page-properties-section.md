---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Определяет, можно ли дублировать страницу в качестве boolean.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425983"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="a07a4-103">PageLockDuplicate Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="a07a4-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="a07a4-104">Определяет, можно ли дублировать страницу в качестве boolean.</span><span class="sxs-lookup"><span data-stu-id="a07a4-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a07a4-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="a07a4-105">TRUE</span></span>  <br/> |<span data-ttu-id="a07a4-106">**Дубликаты** в меню ярлыка страницы и метод автоматизации **Page.Duplicate** отключены для страницы.</span><span class="sxs-lookup"><span data-stu-id="a07a4-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="a07a4-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="a07a4-107">FALSE</span></span>  <br/> |<span data-ttu-id="a07a4-108">Страницу можно дублировать.</span><span class="sxs-lookup"><span data-stu-id="a07a4-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a07a4-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="a07a4-109">Remarks</span></span>

<span data-ttu-id="a07a4-110">Чтобы получить ссылку на ячейку **PageLockDuplicate** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a07a4-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a07a4-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a07a4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a07a4-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="a07a4-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="a07a4-113">Чтобы получить ссылку на ячейку **PageLockDuplicate** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a07a4-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a07a4-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a07a4-114">Section index:</span></span>  <br/> |<span data-ttu-id="a07a4-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a07a4-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a07a4-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a07a4-116">Row index:</span></span>  <br/> |<span data-ttu-id="a07a4-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="a07a4-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="a07a4-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a07a4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a07a4-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="a07a4-119">**visPageLockDuplicate**</span></span> <br/> |
   

