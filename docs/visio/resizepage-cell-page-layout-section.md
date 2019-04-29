---
title: ResizePage Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Определяет, следует ли увеличить страницу, чтобы заключить рисунок после расположения фигур с помощью диалогового окна "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438094"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="893dd-103">ResizePage Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="893dd-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="893dd-104">Определяет, следует ли увеличить страницу, чтобы заключить рисунок после расположения фигур с помощью диалогового окна " **Настройка макета** " (на вкладке " **конструктор** ", в группе " **Макет** " выберите пункт **изменить макет** страницы, а затем нажмите кнопку **другие макеты. Параметры**).</span><span class="sxs-lookup"><span data-stu-id="893dd-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="893dd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="893dd-105">**Value**</span></span>|<span data-ttu-id="893dd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="893dd-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="893dd-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="893dd-107">TRUE</span></span>  <br/> | <span data-ttu-id="893dd-108">Разверните страницу.</span><span class="sxs-lookup"><span data-stu-id="893dd-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="893dd-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="893dd-109">FALSE</span></span>  <br/> | <span data-ttu-id="893dd-110">Не увеличивать страницу.</span><span class="sxs-lookup"><span data-stu-id="893dd-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="893dd-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="893dd-111">Remarks</span></span>

<span data-ttu-id="893dd-112">Чтобы получить ссылку на ячейку ResizePage по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="893dd-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="893dd-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="893dd-113">Cell name:</span></span>  <br/> | <span data-ttu-id="893dd-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="893dd-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="893dd-115">Чтобы получить ссылку на ячейку ResizePage по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="893dd-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="893dd-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="893dd-116">Section index:</span></span>  <br/> |<span data-ttu-id="893dd-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="893dd-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="893dd-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="893dd-118">Row index:</span></span>  <br/> |<span data-ttu-id="893dd-119">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="893dd-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="893dd-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="893dd-120">Cell index:</span></span>  <br/> |<span data-ttu-id="893dd-121">**Висплоресизепаже**</span><span class="sxs-lookup"><span data-stu-id="893dd-121">**visPLOResizePage**</span></span> <br/> |
   

