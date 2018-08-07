---
title: Ячейка ShapeShdwObliqueAngle (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: Задает угол наклона тени фигуры.
ms.openlocfilehash: 11f172de33dfbb65d0176733f5c0bf8b33db483d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814791"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a><span data-ttu-id="1ffc8-103">Ячейка ShapeShdwObliqueAngle (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="1ffc8-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span></span>

<span data-ttu-id="1ffc8-104">Задает угол наклона тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="1ffc8-104">Specifies the angle of oblique direction of a shape's shadow.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ffc8-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ffc8-105">Remarks</span></span>

<span data-ttu-id="1ffc8-106">Значение нуль (0) в этой ячейке указывает, что направление угол — вверх и измеряется стрелке.</span><span class="sxs-lookup"><span data-stu-id="1ffc8-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
<span data-ttu-id="1ffc8-107">Это значение соответствует значению параметра **направление** в диалоговом окне **теневой** (на вкладке **Главная** в группе **фигуру** нажмите кнопку **тень**и нажмите кнопку **Параметры тени**).</span><span class="sxs-lookup"><span data-stu-id="1ffc8-107">This value corresponds to the value of the **Direction** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="1ffc8-108">Чтобы получить ссылку на ячейку ShapeShdwObliqueAngle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1ffc8-108">To get a reference to the ShapeShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ffc8-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1ffc8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1ffc8-110">ShapeShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="1ffc8-110">ShapeShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="1ffc8-111">Для получения ссылки на ячейки ShapeShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1ffc8-111">To get a reference to the ShapeShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ffc8-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1ffc8-112">Section index:</span></span>  <br/> |<span data-ttu-id="1ffc8-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1ffc8-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1ffc8-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1ffc8-114">Row index:</span></span>  <br/> |<span data-ttu-id="1ffc8-115">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="1ffc8-115">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="1ffc8-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1ffc8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1ffc8-117">**visFillShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="1ffc8-117">**visFillShdwObliqueAngle**</span></span> <br/> |
   

