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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415021"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="1831f-103">NoFill Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="1831f-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="1831f-104">Указывает, можно ли заполнить путь.</span><span class="sxs-lookup"><span data-stu-id="1831f-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="1831f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1831f-105">**Value**</span></span>|<span data-ttu-id="1831f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1831f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1831f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1831f-107">TRUE</span></span>  <br/> | <span data-ttu-id="1831f-108">Путь не заполняется, даже если заполнены другие пути в фигуре.</span><span class="sxs-lookup"><span data-stu-id="1831f-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="1831f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1831f-109">FALSE</span></span>  <br/> | <span data-ttu-id="1831f-110">Заливка фигуры применяется к пути, даже если она не закрыта.</span><span class="sxs-lookup"><span data-stu-id="1831f-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1831f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="1831f-111">Remarks</span></span>

<span data-ttu-id="1831f-112">Если для шаблона заливки фигуры установлено ни одно (0), ни один из его путей не заполняется.</span><span class="sxs-lookup"><span data-stu-id="1831f-112">If you set a shape's fill pattern to none (0), none of its paths are filled.</span></span> <span data-ttu-id="1831f-113">Эта ячейка используется для выборочного отключения заливки для пути в фигуре.</span><span class="sxs-lookup"><span data-stu-id="1831f-113">This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="1831f-114">Чтобы получить ссылку на ячейку NoFill по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="1831f-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1831f-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1831f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="1831f-116">Геометрия  *i*  . NoFill,  *где i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1831f-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1831f-117">Чтобы получить ссылку на ячейку NoFill по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1831f-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1831f-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1831f-118">Section index:</span></span>  <br/> |<span data-ttu-id="1831f-119">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1831f-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1831f-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1831f-120">Row index:</span></span>  <br/> |<span data-ttu-id="1831f-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="1831f-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="1831f-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1831f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="1831f-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="1831f-123">**visCompNoFill**</span></span> <br/> |
   

