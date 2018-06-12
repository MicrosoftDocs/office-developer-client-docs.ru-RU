---
title: Ячейка ShapeShdwScaleFactor (раздел формата заливки)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Указывает процент, с помощью которого можно увеличена или уменьшена тени фигуры.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814815"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="ee199-103">Ячейка ShapeShdwScaleFactor (раздел формата заливки)</span><span class="sxs-lookup"><span data-stu-id="ee199-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="ee199-104">Указывает процент, с помощью которого можно увеличена или уменьшена тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="ee199-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee199-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee199-105">Remarks</span></span>

<span data-ttu-id="ee199-106">Каждый теневой имеет расположении тенью ПИН-кода, то есть точку на тени, соответствующий фигуры ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ee199-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="ee199-107">К примеру Если фигуры ПИН-код находится в центр фигуры, расположение тенью ПИН-код будет точка в центре тени.</span><span class="sxs-lookup"><span data-stu-id="ee199-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="ee199-108">При применении масштаба для простого тени, масштаб по центру расположении тенью ПИН-кода; При применении масштаба наклон тени, увеличения применяются наклона.</span><span class="sxs-lookup"><span data-stu-id="ee199-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="ee199-109">Чтобы задать это значение для всех фигур на странице, используйте ShdwScaleFactor ячейки в разделе Свойства страницы.</span><span class="sxs-lookup"><span data-stu-id="ee199-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="ee199-110">Это значение соответствует значению параметра **увеличения** в диалоговом окне **теневой** (на вкладке **Главная** в группе **фигуру** нажмите кнопку **тень**и нажмите кнопку **Параметры тени**).</span><span class="sxs-lookup"><span data-stu-id="ee199-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="ee199-111">Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ee199-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee199-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ee199-112">Cell name:</span></span>  <br/> |<span data-ttu-id="ee199-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="ee199-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="ee199-114">Для получения ссылки на ячейки ShapeShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ee199-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee199-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ee199-115">Section index:</span></span>  <br/> |<span data-ttu-id="ee199-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee199-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ee199-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ee199-117">Row index:</span></span>  <br/> |<span data-ttu-id="ee199-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="ee199-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="ee199-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ee199-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ee199-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="ee199-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

