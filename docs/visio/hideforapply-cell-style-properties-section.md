---
title: HideForApply Cell (Style Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Определяет, где отображается стиль в пользовательском интерфейсе Microsoft Visio.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329955"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="2fdac-103">HideForApply Cell (Style Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2fdac-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="2fdac-104">Определяет, где отображается стиль в пользовательском интерфейсе Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="2fdac-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="2fdac-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="2fdac-105">**Value**</span></span>|<span data-ttu-id="2fdac-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2fdac-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2fdac-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2fdac-107">TRUE</span></span>  <br/> | <span data-ttu-id="2fdac-108">Отображение стиля только в проводнике по **документам**.</span><span class="sxs-lookup"><span data-stu-id="2fdac-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="2fdac-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2fdac-109">FALSE</span></span>  <br/> | <span data-ttu-id="2fdac-110">Отображение стиля в проводнике по **документам**.</span><span class="sxs-lookup"><span data-stu-id="2fdac-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fdac-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fdac-111">Remarks</span></span>

<span data-ttu-id="2fdac-112">Когда вы создаете новый стиль для скрытого стиля, новый стиль не наследует этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="2fdac-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="2fdac-113">Чтобы получить ссылку на ячейку HideForApply по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="2fdac-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2fdac-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2fdac-114">Cell name:</span></span>  <br/> | <span data-ttu-id="2fdac-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="2fdac-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="2fdac-116">Чтобы получить ссылку на ячейку HideForApply по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2fdac-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2fdac-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2fdac-117">Section index:</span></span>  <br/> |<span data-ttu-id="2fdac-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2fdac-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2fdac-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2fdac-119">Row index:</span></span>  <br/> |<span data-ttu-id="2fdac-120">**Висровстиле**</span><span class="sxs-lookup"><span data-stu-id="2fdac-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="2fdac-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2fdac-121">Cell index:</span></span>  <br/> |<span data-ttu-id="2fdac-122">**Висстилехидден**</span><span class="sxs-lookup"><span data-stu-id="2fdac-122">**visStyleHidden**</span></span> <br/> |
   

