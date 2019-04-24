---
title: ShdwOffsetY Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Определяет расстояние в единицах страницы, на которое тень фигуры смещается по вертикали от фигуры.
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349058"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="3f7d3-103">ShdwOffsetY Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="3f7d3-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="3f7d3-104">Определяет расстояние в единицах страницы, на которое тень фигуры смещается по вертикали от фигуры.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f7d3-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f7d3-105">Remarks</span></span>

<span data-ttu-id="3f7d3-106">Это значение задается в диалоговом окне " **Параметры страницы** " (на вкладке " **конструктор** " щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="3f7d3-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="3f7d3-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="3f7d3-108">Если масштаб документа изменяется, смещение тени остается прежним.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="3f7d3-109">Чтобы получить ссылку на ячейку ShdwOffsetY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3f7d3-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f7d3-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3f7d3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3f7d3-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="3f7d3-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="3f7d3-112">Чтобы получить ссылку на ячейку ShdwOffsetY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3f7d3-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f7d3-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3f7d3-113">Section index:</span></span>  <br/> |<span data-ttu-id="3f7d3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f7d3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3f7d3-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3f7d3-115">Row index:</span></span>  <br/> |<span data-ttu-id="3f7d3-116">**Висровпаже**</span><span class="sxs-lookup"><span data-stu-id="3f7d3-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="3f7d3-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3f7d3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3f7d3-118">**Виспажешдвоффсети**</span><span class="sxs-lookup"><span data-stu-id="3f7d3-118">**visPageShdwOffsetY**</span></span> <br/> |
   

