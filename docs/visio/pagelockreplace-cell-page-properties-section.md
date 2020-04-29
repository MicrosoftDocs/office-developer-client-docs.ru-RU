---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Указывает, следует ли отключить кнопку заменить фигуру на этой странице.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433103"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="7a56a-103">PageLockReplace Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="7a56a-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="7a56a-104">Указывает, следует ли отключить кнопку **заменить фигуру** на этой странице.</span><span class="sxs-lookup"><span data-stu-id="7a56a-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="7a56a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7a56a-105">**Value**</span></span>|<span data-ttu-id="7a56a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7a56a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a56a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7a56a-107">TRUE</span></span>  <br/> |<span data-ttu-id="7a56a-108">Кнопка **Изменить фигуру** неактивна, когда эта страница активна.</span><span class="sxs-lookup"><span data-stu-id="7a56a-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="7a56a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7a56a-109">FALSE</span></span>  <br/> |<span data-ttu-id="7a56a-110">Кнопка **Изменить фигуру** не отключается на этой странице.</span><span class="sxs-lookup"><span data-stu-id="7a56a-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="7a56a-111">Кнопка по-прежнему может быть недоступна, если: для параметра **DocLockReplace** в **DocumentSheet** задано **значение true**; ячейка **LockReplace** для выбранной фигуры имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="7a56a-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a56a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a56a-112">Remarks</span></span>

<span data-ttu-id="7a56a-113">Чтобы получить ссылку на ячейку **PageLockReplace** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="7a56a-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a56a-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7a56a-114">Cell name:</span></span>  <br/> | <span data-ttu-id="7a56a-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="7a56a-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="7a56a-116">Чтобы получить ссылку на ячейку **PageLockReplace** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7a56a-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a56a-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7a56a-117">Section index:</span></span>  <br/> |<span data-ttu-id="7a56a-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7a56a-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7a56a-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7a56a-119">Row index:</span></span>  <br/> |<span data-ttu-id="7a56a-120">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="7a56a-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="7a56a-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7a56a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7a56a-122">**виспажелоккреплаце**</span><span class="sxs-lookup"><span data-stu-id="7a56a-122">**visPageLockReplace**</span></span> <br/> |
   

