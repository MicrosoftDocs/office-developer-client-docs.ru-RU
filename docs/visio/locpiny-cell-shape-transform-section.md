---
title: Ячейка LocPinY (раздел Преобразование фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Представляет y-координата ПИН-код фигуры (центр вращения) относительно начала фигуры. Формула для расчета LocPinX — это:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814166"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="3eab7-104">Ячейка LocPinY (раздел Преобразование фигуры)</span><span class="sxs-lookup"><span data-stu-id="3eab7-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="3eab7-105">Представляет *y* -координата ПИН-код фигуры (центр вращения) относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="3eab7-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="3eab7-106">Формула для расчета LocPinX — это:</span><span class="sxs-lookup"><span data-stu-id="3eab7-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="3eab7-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="3eab7-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3eab7-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3eab7-108">Remarks</span></span>

<span data-ttu-id="3eab7-109">Чтобы получить ссылку на ячейку LocPinY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3eab7-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3eab7-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3eab7-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3eab7-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="3eab7-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="3eab7-112">Для получения ссылки на ячейки LocPinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3eab7-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3eab7-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3eab7-113">Section index:</span></span>  <br/> |<span data-ttu-id="3eab7-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3eab7-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3eab7-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3eab7-115">Row index:</span></span>  <br/> |<span data-ttu-id="3eab7-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="3eab7-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="3eab7-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3eab7-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3eab7-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="3eab7-118">**visXFormLocPinY**</span></span> <br/> |
   

