---
title: Непечатаемые ячейки (раздел Разное)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Параметры печати и отключает для выбранной фигуры.
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814299"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="04e2a-103">Непечатаемые ячейки (раздел Разное)</span><span class="sxs-lookup"><span data-stu-id="04e2a-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="04e2a-104">Параметры печати и отключает для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="04e2a-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="04e2a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="04e2a-105">**Value**</span></span>|<span data-ttu-id="04e2a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04e2a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="04e2a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="04e2a-107">TRUE</span></span>  <br/> | <span data-ttu-id="04e2a-108">Печать отключена, но фигуры отображаются в окне документа.</span><span class="sxs-lookup"><span data-stu-id="04e2a-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="04e2a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="04e2a-109">FALSE</span></span>  <br/> | <span data-ttu-id="04e2a-110">Печать включена.</span><span class="sxs-lookup"><span data-stu-id="04e2a-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04e2a-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="04e2a-111">Remarks</span></span>

<span data-ttu-id="04e2a-112">Можно распечатать руководства, выбрав его, а затем устанавливает значение ячейки его непечатаемый значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="04e2a-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="04e2a-113">Для получения ссылки на ячейки непечатаемый по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="04e2a-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04e2a-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="04e2a-114">Cell name:</span></span>  <br/> | <span data-ttu-id="04e2a-115">Непечатаемый</span><span class="sxs-lookup"><span data-stu-id="04e2a-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="04e2a-116">Для получения ссылки на ячейки непечатаемый по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="04e2a-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04e2a-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="04e2a-117">Section index:</span></span>  <br/> |<span data-ttu-id="04e2a-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04e2a-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="04e2a-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="04e2a-119">Row index:</span></span>  <br/> |<span data-ttu-id="04e2a-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="04e2a-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="04e2a-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="04e2a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="04e2a-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="04e2a-122">**visNonPrinting**</span></span> <br/> |
   

