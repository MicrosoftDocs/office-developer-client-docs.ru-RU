---
title: Ячейка LocPinX (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Представляет x-координата ПИН-код фигуры (центр вращения) относительно начала фигуры. Формула для расчета LocPinX — это:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814179"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="c4bb2-104">Ячейка LocPinX (раздел "Преобразование фигуры")</span><span class="sxs-lookup"><span data-stu-id="c4bb2-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="c4bb2-105">Представляет *x* -координата ПИН-код фигуры (центр вращения) относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="c4bb2-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="c4bb2-106">Формула для расчета LocPinX — это:</span><span class="sxs-lookup"><span data-stu-id="c4bb2-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="c4bb2-107">= Ширина \* 0,5</span><span class="sxs-lookup"><span data-stu-id="c4bb2-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4bb2-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4bb2-108">Remarks</span></span>

<span data-ttu-id="c4bb2-109">Для получения ссылки на ячейки LocPinX по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c4bb2-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4bb2-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c4bb2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c4bb2-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="c4bb2-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="c4bb2-112">Для получения ссылки на ячейки LocPinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c4bb2-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4bb2-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c4bb2-113">Section index:</span></span>  <br/> |<span data-ttu-id="c4bb2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4bb2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c4bb2-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c4bb2-115">Row index:</span></span>  <br/> |<span data-ttu-id="c4bb2-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="c4bb2-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="c4bb2-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c4bb2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c4bb2-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="c4bb2-118">**visXFormLocPinX**</span></span> <br/> |
   

