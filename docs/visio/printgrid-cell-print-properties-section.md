---
title: Ячейка PrintGrid (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Указывает, следует ли печатать сетку на странице документа.
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814502"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="019ec-103">Ячейка PrintGrid (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="019ec-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="019ec-104">Указывает, следует ли печатать сетку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="019ec-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="019ec-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="019ec-105">**Value**</span></span>|<span data-ttu-id="019ec-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="019ec-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="019ec-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="019ec-107">TRUE</span></span>  <br/> |<span data-ttu-id="019ec-108">Показать сетку при печати на этой странице.</span><span class="sxs-lookup"><span data-stu-id="019ec-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="019ec-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="019ec-109">FALSE</span></span>  <br/> |<span data-ttu-id="019ec-110">Не показывать сетку при печати на этой странице (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="019ec-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="019ec-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="019ec-111">Remarks</span></span>

<span data-ttu-id="019ec-112">Это значение соответствует флажок **линии сетки** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="019ec-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="019ec-113">Кроме цвет (печатная версия — серый цвет) распечатанных сетки идентична сетки, отображаемые в окне документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="019ec-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="019ec-114">Можно ли печатать сетку страницу по отдельности.</span><span class="sxs-lookup"><span data-stu-id="019ec-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="019ec-115">Также можно определить стиль сетки на основе страницу по **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ), если страница находится active.</span><span class="sxs-lookup"><span data-stu-id="019ec-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="019ec-116">Чтобы получить ссылку на ячейку PrintGrid по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="019ec-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="019ec-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="019ec-117">Cell name:</span></span>  <br/> |<span data-ttu-id="019ec-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="019ec-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="019ec-119">Для получения ссылки на ячейки PrintGrid по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="019ec-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="019ec-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="019ec-120">Section index:</span></span>  <br/> |<span data-ttu-id="019ec-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="019ec-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="019ec-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="019ec-122">Row index:</span></span>  <br/> |<span data-ttu-id="019ec-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="019ec-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="019ec-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="019ec-124">Cell index:</span></span>  <br/> |<span data-ttu-id="019ec-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="019ec-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

