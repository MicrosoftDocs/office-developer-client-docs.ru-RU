---
title: Menu Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Определяет имя элемента меню, которое отображается в контекстном меню или меню тегов действий для фигуры или страницы.
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360657"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="a6064-103">Menu Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="a6064-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="a6064-104">Определяет имя элемента меню, которое отображается в контекстном меню или меню тегов действий для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="a6064-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a6064-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="a6064-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6064-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="a6064-106">Remarks</span></span>

<span data-ttu-id="a6064-107">Чтобы вставить разделитель в меню над элементом, используйте ячейку BeginGroup.</span><span class="sxs-lookup"><span data-stu-id="a6064-107">To insert a separator into the menu above this item, use the BeginGroup cell.</span></span> <span data-ttu-id="a6064-108">Чтобы отобразить команду в нижней части меню, введите перед именем символ процента (%).</span><span class="sxs-lookup"><span data-stu-id="a6064-108">To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="a6064-109">Чтобы получить ссылку на ячейку меню по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a6064-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6064-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a6064-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a6064-111">Действия.</span><span class="sxs-lookup"><span data-stu-id="a6064-111">Actions.</span></span> <span data-ttu-id="a6064-112">*Name (имя* ). Действия Менувхере.</span><span class="sxs-lookup"><span data-stu-id="a6064-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="a6064-113">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="a6064-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a6064-114">Чтобы получить ссылку на ячейку меню по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a6064-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6064-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a6064-115">Section index:</span></span>  <br/> |<span data-ttu-id="a6064-116">**Виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="a6064-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a6064-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a6064-117">Row index:</span></span>  <br/> |<span data-ttu-id="a6064-118">**висровактион** +  *i* , где i = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="a6064-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="a6064-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a6064-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a6064-120">**Висактионмену**</span><span class="sxs-lookup"><span data-stu-id="a6064-120">**visActionMenu**</span></span> <br/> |
   

