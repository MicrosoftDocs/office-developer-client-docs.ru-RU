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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357220"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="00e27-103">UIVisibility Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="00e27-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="00e27-104">Определяет, отображается ли имя страницы в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="00e27-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="00e27-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="00e27-105">**Value**</span></span>|<span data-ttu-id="00e27-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00e27-106">**Description**</span></span>|<span data-ttu-id="00e27-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="00e27-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00e27-108">нуль</span><span class="sxs-lookup"><span data-stu-id="00e27-108">0</span></span>  <br/> |<span data-ttu-id="00e27-109">Отображение имени страницы в ПОЛЬЗОВАТЕЛЬСКОМ ИНТЕРФЕЙСе (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="00e27-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="00e27-110">**Висуивнормал**</span><span class="sxs-lookup"><span data-stu-id="00e27-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="00e27-111">1,1</span><span class="sxs-lookup"><span data-stu-id="00e27-111">1</span></span>  <br/> |<span data-ttu-id="00e27-112">Не выводите имя страницы в ПОЛЬЗОВАТЕЛЬСКОМ ИНТЕРФЕЙСе.</span><span class="sxs-lookup"><span data-stu-id="00e27-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="00e27-113">**Висуивхидден**</span><span class="sxs-lookup"><span data-stu-id="00e27-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00e27-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="00e27-114">Remarks</span></span>

<span data-ttu-id="00e27-115">Если задать для ячейки UIVisibility значение **висуивхидден** , страница не будет отображаться в любом месте пользовательского интерфейса, где отображается строка, содержащая имя страницы.</span><span class="sxs-lookup"><span data-stu-id="00e27-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="00e27-116">Например, страница не будет отображаться в виде параметра в **проводнике** по документу или на вкладках страниц.</span><span class="sxs-lookup"><span data-stu-id="00e27-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="00e27-117">Тем не менее, страница остается доступной, но если вы используете автоматизацию или пути к ПОЛЬЗОВАТЕЛЬСКОМу ИНТЕРФЕЙСу, которые не содержат имени страницы, например, команда " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="00e27-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="00e27-118">Эта ячейка предназначена для использования с страницами документа; Он не предназначен для использования с разворотными страницами, для которых в ячейке UIVisibility по умолчанию задано значение **висуивхидден** , и его не следует изменять.</span><span class="sxs-lookup"><span data-stu-id="00e27-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00e27-119">Чтобы скрыть страницу из команды **печати** документа, сделайте ее фоновой страницей (свойство**Type** — **вистипебаккграунд** ), которое не используется в качестве фона любой страницы (фигуры на страницах заднего плана печатаются, когда страница использует ее в качестве фона). Печать).</span><span class="sxs-lookup"><span data-stu-id="00e27-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="00e27-120">Команда " **Печать** " документа работает только с индексированными страницами, а фоновые страницы не индексируются.</span><span class="sxs-lookup"><span data-stu-id="00e27-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="00e27-121">Чтобы получить ссылку на ячейку UIVisibility по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="00e27-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00e27-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="00e27-122">Cell name:</span></span>  <br/> |<span data-ttu-id="00e27-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="00e27-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="00e27-124">Чтобы получить ссылку на ячейку UIVisibility по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="00e27-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00e27-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="00e27-125">Section index:</span></span>  <br/> |<span data-ttu-id="00e27-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00e27-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="00e27-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="00e27-127">Row index:</span></span>  <br/> |<span data-ttu-id="00e27-128">**Висровпаже**</span><span class="sxs-lookup"><span data-stu-id="00e27-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="00e27-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="00e27-129">Cell index:</span></span>  <br/> |<span data-ttu-id="00e27-130">**Виспажеуивисибилити**</span><span class="sxs-lookup"><span data-stu-id="00e27-130">**visPageUIVisibility**</span></span> <br/> |
   

