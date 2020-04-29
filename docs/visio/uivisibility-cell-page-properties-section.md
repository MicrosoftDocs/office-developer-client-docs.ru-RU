---
title: UIVisibility Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Определяет, отображается ли имя страницы в пользовательском интерфейсе.
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437331"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="e996e-103">UIVisibility Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="e996e-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="e996e-104">Определяет, отображается ли имя страницы в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e996e-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="e996e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e996e-105">**Value**</span></span>|<span data-ttu-id="e996e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e996e-106">**Description**</span></span>|<span data-ttu-id="e996e-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e996e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e996e-108">нуль</span><span class="sxs-lookup"><span data-stu-id="e996e-108">0</span></span>  <br/> |<span data-ttu-id="e996e-109">Отображение имени страницы в пользовательском интерфейсе (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e996e-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="e996e-110">**висуивнормал**</span><span class="sxs-lookup"><span data-stu-id="e996e-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="e996e-111">1,1</span><span class="sxs-lookup"><span data-stu-id="e996e-111">1</span></span>  <br/> |<span data-ttu-id="e996e-112">Не выводите имя страницы в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e996e-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="e996e-113">**висуивхидден**</span><span class="sxs-lookup"><span data-stu-id="e996e-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e996e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e996e-114">Remarks</span></span>

<span data-ttu-id="e996e-115">Если задать для ячейки UIVisibility значение **висуивхидден** , страница не будет отображаться в любом месте пользовательского интерфейса, где отображается строка, содержащая имя страницы.</span><span class="sxs-lookup"><span data-stu-id="e996e-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="e996e-116">Например, страница не будет отображаться в виде параметра в **Проводнике по документу** или на вкладках страниц.</span><span class="sxs-lookup"><span data-stu-id="e996e-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="e996e-117">Тем не менее, страница остается доступной, но если вы используете автоматизацию или пути к пользовательскому интерфейсу, которые не содержат имени страницы, например, команда " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="e996e-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="e996e-118">Эта ячейка предназначена для использования с страницами документа; Он не предназначен для использования с разворотными страницами, для которых в ячейке UIVisibility по умолчанию задано значение **висуивхидден** , и его не следует изменять.</span><span class="sxs-lookup"><span data-stu-id="e996e-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e996e-119">Чтобы скрыть страницу из команды **печати** документа, сделайте ее фоновой страницей (свойство**Type** — **вистипебаккграунд** ), которое не используется в качестве фона любой страницы (фигуры на страницах заднего плана печатаются, когда печатается страница, использующая ее в качестве фона).</span><span class="sxs-lookup"><span data-stu-id="e996e-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="e996e-120">Команда " **Печать** " документа работает только с индексированными страницами, а фоновые страницы не индексируются.</span><span class="sxs-lookup"><span data-stu-id="e996e-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="e996e-121">Чтобы получить ссылку на ячейку UIVisibility по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e996e-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e996e-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e996e-122">Cell name:</span></span>  <br/> |<span data-ttu-id="e996e-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="e996e-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="e996e-124">Чтобы получить ссылку на ячейку UIVisibility по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e996e-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e996e-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e996e-125">Section index:</span></span>  <br/> |<span data-ttu-id="e996e-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e996e-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e996e-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e996e-127">Row index:</span></span>  <br/> |<span data-ttu-id="e996e-128">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="e996e-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="e996e-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e996e-129">Cell index:</span></span>  <br/> |<span data-ttu-id="e996e-130">**виспажеуивисибилити**</span><span class="sxs-lookup"><span data-stu-id="e996e-130">**visPageUIVisibility**</span></span> <br/> |
   

