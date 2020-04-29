---
title: NoCtlHandles Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Включает и выключает отображение управляющих маркеров для выбранной фигуры.
ms.openlocfilehash: cbe4d6a8b6fdd4b66acf064884d20999ff7e3b4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416127"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a><span data-ttu-id="52a45-103">NoCtlHandles Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="52a45-103">NoCtlHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="52a45-104">Включает и выключает отображение управляющих маркеров для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="52a45-104">Switches the display of control handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="52a45-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="52a45-105">**Value**</span></span>|<span data-ttu-id="52a45-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="52a45-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="52a45-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="52a45-107">TRUE</span></span>  <br/> | <span data-ttu-id="52a45-108">Управляющие маркеры не отображаются, если выбрана фигура.</span><span class="sxs-lookup"><span data-stu-id="52a45-108">Control handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="52a45-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="52a45-109">FALSE</span></span>  <br/> | <span data-ttu-id="52a45-110">Управляющие маркеры отображаются при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="52a45-110">Control handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52a45-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="52a45-111">Remarks</span></span>

<span data-ttu-id="52a45-112">Чтобы получить ссылку на ячейку NoCtlHandles по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="52a45-112">To get a reference to the NoCtlHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52a45-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="52a45-113">Cell name:</span></span>  <br/> | <span data-ttu-id="52a45-114">NoCtlHandles</span><span class="sxs-lookup"><span data-stu-id="52a45-114">NoCtlHandles</span></span>  <br/> |
   
<span data-ttu-id="52a45-115">Чтобы получить ссылку на ячейку NoCtlHandles по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="52a45-115">To get a reference to the NoCtlHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52a45-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="52a45-116">Section index:</span></span>  <br/> |<span data-ttu-id="52a45-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52a45-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="52a45-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="52a45-118">Row index:</span></span>  <br/> |<span data-ttu-id="52a45-119">**висровмиск**</span><span class="sxs-lookup"><span data-stu-id="52a45-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="52a45-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="52a45-120">Cell index:</span></span>  <br/> |<span data-ttu-id="52a45-121">**висноктлхандлес**</span><span class="sxs-lookup"><span data-stu-id="52a45-121">**visNoCtlHandles**</span></span> <br/> |
   

