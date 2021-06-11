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
description: Определяет расстояние в единицах страниц, на которое по вертикали смещена тень капля фигуры.
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438143"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="ccc34-103">ShdwOffsetY Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ccc34-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="ccc34-104">Определяет расстояние в единицах страниц, на которое по вертикали смещена тень капля фигуры.</span><span class="sxs-lookup"><span data-stu-id="ccc34-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccc34-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccc34-105">Remarks</span></span>

<span data-ttu-id="ccc34-106">Это значение заданной в диалоговом **окне Настройка** страницы (на вкладке **Дизайн** щелкните стрелку **установки страницы).**</span><span class="sxs-lookup"><span data-stu-id="ccc34-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="ccc34-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="ccc34-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="ccc34-108">Если рисунок масштабирован, смещение теней остается тем же.</span><span class="sxs-lookup"><span data-stu-id="ccc34-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="ccc34-109">Чтобы получить ссылку на ячейку ShdwOffsetY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ccc34-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccc34-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ccc34-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ccc34-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="ccc34-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="ccc34-112">Чтобы получить ссылку на ячейку ShdwOffsetY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ccc34-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccc34-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ccc34-113">Section index:</span></span>  <br/> |<span data-ttu-id="ccc34-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ccc34-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ccc34-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ccc34-115">Row index:</span></span>  <br/> |<span data-ttu-id="ccc34-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ccc34-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ccc34-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ccc34-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ccc34-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="ccc34-118">**visPageShdwOffsetY**</span></span> <br/> |
   

