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
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="2fe9f-103">PrintGrid Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2fe9f-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="2fe9f-104">Указывает, следует ли печатать сетку при печати страницы документа.</span><span class="sxs-lookup"><span data-stu-id="2fe9f-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="2fe9f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2fe9f-105">**Value**</span></span>|<span data-ttu-id="2fe9f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2fe9f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2fe9f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2fe9f-107">TRUE</span></span>  <br/> |<span data-ttu-id="2fe9f-108">Отображать сетку при печати этой страницы.</span><span class="sxs-lookup"><span data-stu-id="2fe9f-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="2fe9f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2fe9f-109">FALSE</span></span>  <br/> |<span data-ttu-id="2fe9f-110">Не показывать сетку при печати этой страницы (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="2fe9f-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fe9f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fe9f-111">Remarks</span></span>

<span data-ttu-id="2fe9f-112">Это значение соответствует флажку " **линии сетки** " на вкладке " **Настройка печати** " диалогового окна " **Параметры страницы** " (на вкладке " **конструктор** " щелкните стрелку **настройки страницы** ).</span><span class="sxs-lookup"><span data-stu-id="2fe9f-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="2fe9f-113">Кроме цвета (Распечатанная версия серый), напечатанная сетка идентична сетке, которая отображается в окне документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="2fe9f-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="2fe9f-114">Вы можете выбрать, следует ли печатать сетку отдельно для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="2fe9f-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="2fe9f-115">Стиль сетка также может быть определен на отдельной странице в диалоговом окне \*\* &amp; линейка и сетка\*\* (на вкладке **вид** щелкните стрелку **Показать** ), когда страница активна.</span><span class="sxs-lookup"><span data-stu-id="2fe9f-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="2fe9f-116">Чтобы получить ссылку на ячейку PrintGrid по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="2fe9f-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fe9f-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2fe9f-117">Cell name:</span></span>  <br/> |<span data-ttu-id="2fe9f-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="2fe9f-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="2fe9f-119">Чтобы получить ссылку на ячейку PrintGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2fe9f-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fe9f-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2fe9f-120">Section index:</span></span>  <br/> |<span data-ttu-id="2fe9f-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2fe9f-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2fe9f-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2fe9f-122">Row index:</span></span>  <br/> |<span data-ttu-id="2fe9f-123">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="2fe9f-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="2fe9f-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2fe9f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2fe9f-125">**Виспринтпропертиеспринтгрид**</span><span class="sxs-lookup"><span data-stu-id="2fe9f-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

