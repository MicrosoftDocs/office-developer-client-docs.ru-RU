---
title: Ячейка NoFill (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Указывает, можно ли заполнить путь.
ms.openlocfilehash: 3f5bab76fc38b6e82aeaeee45b75bd733afdbd26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814300"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="a414f-103">Ячейка NoFill (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="a414f-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="a414f-104">Указывает, можно ли заполнить путь.</span><span class="sxs-lookup"><span data-stu-id="a414f-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="a414f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a414f-105">**Value**</span></span>|<span data-ttu-id="a414f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a414f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a414f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a414f-107">TRUE</span></span>  <br/> | <span data-ttu-id="a414f-108">Путь не указана, даже в том случае, если заполняются других путей к папкам в форме.</span><span class="sxs-lookup"><span data-stu-id="a414f-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="a414f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a414f-109">FALSE</span></span>  <br/> | <span data-ttu-id="a414f-110">Заливки фигуры применяется к пути, даже в том случае, если оно не будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="a414f-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a414f-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="a414f-111">Remarks</span></span>

<span data-ttu-id="a414f-112">Если значение none (0) значение узора заливки фигуры, ни один из его пути не будут заполнены.</span><span class="sxs-lookup"><span data-stu-id="a414f-112">If you set a shape's fill pattern to none (0), none of its paths are filled.</span></span> <span data-ttu-id="a414f-113">В этой ячейке используется для отключить заливки выборочно для пути внутри фигуры.</span><span class="sxs-lookup"><span data-stu-id="a414f-113">This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="a414f-114">Чтобы получить ссылку на ячейку NoFill по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a414f-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a414f-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a414f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a414f-116">Геометрия *i* . NoFill где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a414f-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a414f-117">Для получения ссылки на ячейки NoFill по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a414f-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a414f-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a414f-118">Section index:</span></span>  <br/> |<span data-ttu-id="a414f-119">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a414f-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a414f-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a414f-120">Row index:</span></span>  <br/> |<span data-ttu-id="a414f-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="a414f-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="a414f-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a414f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a414f-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="a414f-123">**visCompNoFill**</span></span> <br/> |
   

