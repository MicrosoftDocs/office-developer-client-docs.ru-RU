---
title: Ячейка NoLine (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Определяет, будет ли линия вокруг границ пути.
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814295"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="0f40f-103">Ячейка NoLine (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="0f40f-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="0f40f-104">Определяет, будет ли линия вокруг границ пути.</span><span class="sxs-lookup"><span data-stu-id="0f40f-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="0f40f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0f40f-105">**Value**</span></span>|<span data-ttu-id="0f40f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f40f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0f40f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0f40f-107">TRUE</span></span>  <br/> | <span data-ttu-id="0f40f-108">Вокруг границ пути, который является границ заполненной области строки не отображается.</span><span class="sxs-lookup"><span data-stu-id="0f40f-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="0f40f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0f40f-109">FALSE</span></span>  <br/> | <span data-ttu-id="0f40f-110">Линия вокруг границы пути.</span><span class="sxs-lookup"><span data-stu-id="0f40f-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f40f-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="0f40f-111">Remarks</span></span>

<span data-ttu-id="0f40f-112">При изменении цвета линии Технический строка по-прежнему существует, даже если вы не видите на белым фоном.</span><span class="sxs-lookup"><span data-stu-id="0f40f-112">When you change the color of a line to white, the line still exists even though you can't see it on a white background.</span></span> <span data-ttu-id="0f40f-113">При установке значения ячейки имеет значение TRUE, строка не отображается.</span><span class="sxs-lookup"><span data-stu-id="0f40f-113">When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="0f40f-114">Чтобы получить ссылку на ячейку NoLine по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0f40f-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f40f-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0f40f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="0f40f-116">Геометрия *i* . NoLine где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0f40f-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0f40f-117">Для получения ссылки на ячейки NoLine по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0f40f-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f40f-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0f40f-118">Section index:</span></span>  <br/> |<span data-ttu-id="0f40f-119">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f40f-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0f40f-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0f40f-120">Row index:</span></span>  <br/> |<span data-ttu-id="0f40f-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="0f40f-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="0f40f-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0f40f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0f40f-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="0f40f-123">**visCompNoLine**</span></span> <br/> |
   

