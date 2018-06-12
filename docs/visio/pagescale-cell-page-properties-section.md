---
title: Ячейка PageScale (раздел страницы свойств)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Определяет значение единицы страницы в текущем масштабе документа. Масштаб документа для страницы представляет собой отношение единицы страницы в ячейке PageScale к единице документа в ячейке DrawingScale.
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814378"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="cd4dc-104">Ячейка PageScale (раздел страницы свойств)</span><span class="sxs-lookup"><span data-stu-id="cd4dc-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="cd4dc-105">Определяет значение единицы страницы в текущем масштабе документа.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-105">Determines the value of the page unit in the current drawing scale.</span></span> <span data-ttu-id="cd4dc-106">Масштаб документа для страницы представляет собой отношение единицы страницы в ячейке PageScale к единице документа в ячейке DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-106">The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd4dc-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="cd4dc-107">Remarks</span></span>

<span data-ttu-id="cd4dc-108">Значение ячейки PageScale также можно настроить на вкладке **Масштаб документа** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="cd4dc-108">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="cd4dc-109">Значение ячейки это первая из двух чисел в поле **предопределенный масштаб** или **Настраиваемый масштаб** , в зависимости от того, размеры масштаба параметра, выбранного в разделе **Масштаб документа**.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-109">The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**.</span></span> <span data-ttu-id="cd4dc-110">Например при выборе архитектурные масштаба рисунка масштаб документа для страницы — 3/32 "= 1'0".</span><span class="sxs-lookup"><span data-stu-id="cd4dc-110">For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0".</span></span> <span data-ttu-id="cd4dc-111">Значение в ячейке PageScale — 0.0938 in.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-111">The value in the PageScale cell is 0.0938 in.</span></span> <span data-ttu-id="cd4dc-112">(или 3/32"), а значение в ячейке DrawingScale — 1 ft.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-112">(or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="cd4dc-113">Чтобы получить ссылку на ячейку PageScale по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd4dc-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="cd4dc-115">PageScale</span><span class="sxs-lookup"><span data-stu-id="cd4dc-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="cd4dc-116">Для получения ссылки на ячейки PageScale по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd4dc-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-117">Section index:</span></span>  <br/> |<span data-ttu-id="cd4dc-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cd4dc-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-119">Row index:</span></span>  <br/> |<span data-ttu-id="cd4dc-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="cd4dc-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="cd4dc-122">**visPageScale**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-122">**visPageScale**</span></span> <br/> |
   

