---
title: Ячейка NoAlignBox (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: Включает или отключает отображение прямоугольник выделения и отключает для выбранной фигуры.
ms.openlocfilehash: c8e5fe28197a72b4cdb5306732dd155dc8f4f810
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814293"
---
# <a name="noalignbox-cell-miscellaneous-section"></a><span data-ttu-id="816fe-103">Ячейка NoAlignBox (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="816fe-103">NoAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="816fe-104">Включает или отключает отображение прямоугольник выделения и отключает для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="816fe-104">Switches the display of the selection rectangle on and off for the selected shape.</span></span>
  
|<span data-ttu-id="816fe-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="816fe-105">**Value**</span></span>|<span data-ttu-id="816fe-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="816fe-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="816fe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="816fe-107">TRUE</span></span>  <br/> | <span data-ttu-id="816fe-108">Прямоугольник выделения не отображаются при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="816fe-108">Selection rectangle is not displayed when the shape is selected.</span></span>  <br/> |
| <span data-ttu-id="816fe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="816fe-109">FALSE</span></span>  <br/> | <span data-ttu-id="816fe-110">Прямоугольник выделения отображается при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="816fe-110">Selection rectangle is displayed when the shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="816fe-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="816fe-111">Remarks</span></span>

<span data-ttu-id="816fe-112">Чтобы получить ссылку на ячейку NoAlignBox по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="816fe-112">To get a reference to the NoAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="816fe-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="816fe-113">Cell name:</span></span>  <br/> | <span data-ttu-id="816fe-114">NoAlignBox</span><span class="sxs-lookup"><span data-stu-id="816fe-114">NoAlignBox</span></span>  <br/> |
   
<span data-ttu-id="816fe-115">Для получения ссылки на ячейки NoAlignBox по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="816fe-115">To get a reference to the NoAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="816fe-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="816fe-116">Section index:</span></span>  <br/> |<span data-ttu-id="816fe-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="816fe-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="816fe-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="816fe-118">Row index:</span></span>  <br/> |<span data-ttu-id="816fe-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="816fe-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="816fe-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="816fe-120">Cell index:</span></span>  <br/> |<span data-ttu-id="816fe-121">**visNoAlignBox**</span><span class="sxs-lookup"><span data-stu-id="816fe-121">**visNoAlignBox**</span></span> <br/> |
   

