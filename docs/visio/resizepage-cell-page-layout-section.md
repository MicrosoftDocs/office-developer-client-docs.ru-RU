---
title: Ячейка ResizePage (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Определяет, следует ли увеличить страницу для помещения документа после расположения фигур с помощью диалогового окна "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814607"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="581ac-103">Ячейка ResizePage (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="581ac-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="581ac-104">Определяет, следует ли увеличить страницу для помещения документа после расположения фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить** расположение и нажмите кнопку **более макета Параметры**).</span><span class="sxs-lookup"><span data-stu-id="581ac-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="581ac-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="581ac-105">**Value**</span></span>|<span data-ttu-id="581ac-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="581ac-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="581ac-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="581ac-107">TRUE</span></span>  <br/> | <span data-ttu-id="581ac-108">Увеличьте страницу.</span><span class="sxs-lookup"><span data-stu-id="581ac-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="581ac-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="581ac-109">FALSE</span></span>  <br/> | <span data-ttu-id="581ac-110">Не увеличить страницу.</span><span class="sxs-lookup"><span data-stu-id="581ac-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="581ac-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="581ac-111">Remarks</span></span>

<span data-ttu-id="581ac-112">Чтобы получить ссылку на ячейку ResizePage по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="581ac-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="581ac-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="581ac-113">Cell name:</span></span>  <br/> | <span data-ttu-id="581ac-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="581ac-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="581ac-115">Для получения ссылки на ячейки ResizePage по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="581ac-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="581ac-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="581ac-116">Section index:</span></span>  <br/> |<span data-ttu-id="581ac-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="581ac-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="581ac-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="581ac-118">Row index:</span></span>  <br/> |<span data-ttu-id="581ac-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="581ac-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="581ac-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="581ac-120">Cell index:</span></span>  <br/> |<span data-ttu-id="581ac-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="581ac-121">**visPLOResizePage**</span></span> <br/> |
   

