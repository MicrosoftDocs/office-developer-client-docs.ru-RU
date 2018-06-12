---
title: Меню ячейки (раздела "действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Определяет имя элемента меню, которое отображается в контекстном или меню тегов действий для фигуры или страницы.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814303"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="5566b-103">Меню ячейки (раздела "действия")</span><span class="sxs-lookup"><span data-stu-id="5566b-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="5566b-104">Определяет имя элемента меню, которое отображается в контекстном или меню тегов действий для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="5566b-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5566b-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="5566b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5566b-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="5566b-106">Remarks</span></span>

<span data-ttu-id="5566b-107">Чтобы вставить разделитель в меню над этот элемент, используйте BeginGroup ячейки.</span><span class="sxs-lookup"><span data-stu-id="5566b-107">To insert a separator into the menu above this item, use the BeginGroup cell.</span></span> <span data-ttu-id="5566b-108">Чтобы отобразить команды в нижней части меню, перед именем со знаком процента (%).</span><span class="sxs-lookup"><span data-stu-id="5566b-108">To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="5566b-109">Чтобы получить ссылку на ячейку меню по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="5566b-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5566b-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5566b-110">Cell name:</span></span>  <br/> |<span data-ttu-id="5566b-111">Действия.</span><span class="sxs-lookup"><span data-stu-id="5566b-111">Actions.</span></span> <span data-ttu-id="5566b-112">*имя* . Menuwhere действия.</span><span class="sxs-lookup"><span data-stu-id="5566b-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="5566b-113">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="5566b-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="5566b-114">Для получения ссылки на ячейки меню по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5566b-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5566b-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5566b-115">Section index:</span></span>  <br/> |<span data-ttu-id="5566b-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="5566b-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="5566b-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5566b-117">Row index:</span></span>  <br/> |<span data-ttu-id="5566b-118">**visRowAction** +  *i* где я = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="5566b-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="5566b-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5566b-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5566b-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="5566b-120">**visActionMenu**</span></span> <br/> |
   

