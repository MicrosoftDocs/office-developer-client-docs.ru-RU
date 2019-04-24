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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315192"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="1b219-103">PrintGrid Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="1b219-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="1b219-104">Указывает, следует ли печатать сетку при печати страницы документа.</span><span class="sxs-lookup"><span data-stu-id="1b219-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="1b219-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="1b219-105">**Value**</span></span>|<span data-ttu-id="1b219-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1b219-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b219-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1b219-107">TRUE</span></span>  <br/> |<span data-ttu-id="1b219-108">Отображать сетку при печати этой страницы.</span><span class="sxs-lookup"><span data-stu-id="1b219-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="1b219-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1b219-109">FALSE</span></span>  <br/> |<span data-ttu-id="1b219-110">Не показывать сетку при печати этой страницы (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1b219-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b219-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b219-111">Remarks</span></span>

<span data-ttu-id="1b219-112">Это значение соответствует флажку " **линии сетки** " на вкладке " **Настройка печати** " диалогового окна " **Параметры страницы** " (на вкладке " **конструктор** " щелкните стрелку **настройки страницы** ).</span><span class="sxs-lookup"><span data-stu-id="1b219-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="1b219-113">Кроме цвета (Распечатанная версия серый), напечатанная сетка идентична сетке, которая отображается в окне документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="1b219-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="1b219-114">Вы можете выбрать, следует ли печатать сетку отдельно для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="1b219-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="1b219-115">Стиль сетка также может быть определен на отдельной странице в диалоговом окне \*\* &amp; линейка и сетка\*\* (на вкладке **вид** щелкните стрелку **Показать** ), когда страница активна.</span><span class="sxs-lookup"><span data-stu-id="1b219-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="1b219-116">Чтобы получить ссылку на ячейку PrintGrid по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="1b219-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b219-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b219-117">Cell name:</span></span>  <br/> |<span data-ttu-id="1b219-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="1b219-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="1b219-119">Чтобы получить ссылку на ячейку PrintGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1b219-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b219-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1b219-120">Section index:</span></span>  <br/> |<span data-ttu-id="1b219-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1b219-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1b219-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1b219-122">Row index:</span></span>  <br/> |<span data-ttu-id="1b219-123">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="1b219-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="1b219-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b219-124">Cell index:</span></span>  <br/> |<span data-ttu-id="1b219-125">**Виспринтпропертиеспринтгрид**</span><span class="sxs-lookup"><span data-stu-id="1b219-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

