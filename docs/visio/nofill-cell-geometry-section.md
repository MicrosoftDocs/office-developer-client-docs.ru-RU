---
title: NoFill Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Указывает, можно ли заполнить путь.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357255"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="f2cd3-103">NoFill Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f2cd3-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="f2cd3-104">Указывает, можно ли заполнить путь.</span><span class="sxs-lookup"><span data-stu-id="f2cd3-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="f2cd3-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="f2cd3-105">**Value**</span></span>|<span data-ttu-id="f2cd3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f2cd3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f2cd3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2cd3-107">TRUE</span></span>  <br/> | <span data-ttu-id="f2cd3-108">Путь не заполняется, даже если другие пути в фигуре заполнены.</span><span class="sxs-lookup"><span data-stu-id="f2cd3-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="f2cd3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f2cd3-109">FALSE</span></span>  <br/> | <span data-ttu-id="f2cd3-110">Заливка фигуры применяется к пути, даже если она не закрыта.</span><span class="sxs-lookup"><span data-stu-id="f2cd3-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2cd3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2cd3-111">Remarks</span></span>

<span data-ttu-id="f2cd3-112">Если для узора заливки фигуры задано значение None (0), ни один из его путей не заполняется.</span><span class="sxs-lookup"><span data-stu-id="f2cd3-112">If you set a shape's fill pattern to none (0), none of its paths are filled.</span></span> <span data-ttu-id="f2cd3-113">Эта ячейка используется для того, чтобы отключить выборочную заливку для контура в фигуре.</span><span class="sxs-lookup"><span data-stu-id="f2cd3-113">This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="f2cd3-114">Чтобы получить ссылку на ячейку "FILLIN" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="f2cd3-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2cd3-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2cd3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="f2cd3-116">Геометрия *i* . Замещение, где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f2cd3-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f2cd3-117">Чтобы получить ссылку на ячейку "FILLIN" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f2cd3-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2cd3-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f2cd3-118">Section index:</span></span>  <br/> |<span data-ttu-id="f2cd3-119">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2cd3-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f2cd3-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f2cd3-120">Row index:</span></span>  <br/> |<span data-ttu-id="f2cd3-121">**Висровкомпонент**</span><span class="sxs-lookup"><span data-stu-id="f2cd3-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="f2cd3-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2cd3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f2cd3-123">**Вискомпнофилл**</span><span class="sxs-lookup"><span data-stu-id="f2cd3-123">**visCompNoFill**</span></span> <br/> |
   

