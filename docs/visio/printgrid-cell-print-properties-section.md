---
title: PrintGrid Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Указывает, следует ли печатать сетку при печати страницы документа.
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433208"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="96c1b-103">PrintGrid Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="96c1b-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="96c1b-104">Указывает, следует ли печатать сетку при печати страницы документа.</span><span class="sxs-lookup"><span data-stu-id="96c1b-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="96c1b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="96c1b-105">**Value**</span></span>|<span data-ttu-id="96c1b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96c1b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96c1b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="96c1b-107">TRUE</span></span>  <br/> |<span data-ttu-id="96c1b-108">Откажите сетку при печати этой страницы.</span><span class="sxs-lookup"><span data-stu-id="96c1b-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="96c1b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="96c1b-109">FALSE</span></span>  <br/> |<span data-ttu-id="96c1b-110">Не показывать сетку при печати этой страницы (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="96c1b-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96c1b-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="96c1b-111">Remarks</span></span>

<span data-ttu-id="96c1b-112">Это значение соответствует  установленного на вкладке "Настройка  печати" в диалоговом  окне "Настройка страницы" (на вкладке "Конструктор" щелкните стрелку **"Настройка** страницы"). </span><span class="sxs-lookup"><span data-stu-id="96c1b-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="96c1b-113">Кроме цвета (печатная версия серая) печатная сетка идентична сетке, которая видна в окне рисования Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="96c1b-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="96c1b-114">Можно выбрать, следует ли печатать сетку по страницам.</span><span class="sxs-lookup"><span data-stu-id="96c1b-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="96c1b-115">Стиль сетки также можно определить по страницам в диалоговом окне **"Линейка &amp;** сетки" (на вкладке "Вид" щелкните стрелку "Показать"), когда страница активна.  </span><span class="sxs-lookup"><span data-stu-id="96c1b-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="96c1b-116">Чтобы получить ссылку на ячейку PrintGrid по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="96c1b-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96c1b-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="96c1b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="96c1b-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="96c1b-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="96c1b-119">Чтобы получить ссылку на ячейку PrintGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="96c1b-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96c1b-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="96c1b-120">Section index:</span></span>  <br/> |<span data-ttu-id="96c1b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="96c1b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="96c1b-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="96c1b-122">Row index:</span></span>  <br/> |<span data-ttu-id="96c1b-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="96c1b-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="96c1b-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="96c1b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="96c1b-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="96c1b-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

