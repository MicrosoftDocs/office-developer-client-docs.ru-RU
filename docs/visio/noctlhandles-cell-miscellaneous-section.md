---
title: Ячейка NoCtlHandles (раздел Разное)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Включает или отключает отображение управляющих маркеров и отключает для выбранной фигуры.
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814292"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a><span data-ttu-id="36ef9-103">Ячейка NoCtlHandles (раздел Разное)</span><span class="sxs-lookup"><span data-stu-id="36ef9-103">NoCtlHandles Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="36ef9-104">Включает или отключает отображение управляющих маркеров и отключает для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="36ef9-104">Switches the display of control handles on and off for the selected shape.</span></span>
  
|<span data-ttu-id="36ef9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="36ef9-105">**Value**</span></span>|<span data-ttu-id="36ef9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36ef9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36ef9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="36ef9-107">TRUE</span></span>  <br/> | <span data-ttu-id="36ef9-108">Управляющие маркеры не отображаются при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="36ef9-108">Control handles are not displayed when a shape is selected.</span></span>  <br/> |
| <span data-ttu-id="36ef9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="36ef9-109">FALSE</span></span>  <br/> | <span data-ttu-id="36ef9-110">Управляющие маркеры отображаются при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="36ef9-110">Control handles are displayed when a shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36ef9-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="36ef9-111">Remarks</span></span>

<span data-ttu-id="36ef9-112">Чтобы получить ссылку на ячейку NoCtlHandles по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="36ef9-112">To get a reference to the NoCtlHandles cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="36ef9-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="36ef9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="36ef9-114">NoCtlHandles</span><span class="sxs-lookup"><span data-stu-id="36ef9-114">NoCtlHandles</span></span>  <br/> |
   
<span data-ttu-id="36ef9-115">Для получения ссылки на ячейки NoCtlHandles по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="36ef9-115">To get a reference to the NoCtlHandles cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="36ef9-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="36ef9-116">Section index:</span></span>  <br/> |<span data-ttu-id="36ef9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36ef9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="36ef9-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="36ef9-118">Row index:</span></span>  <br/> |<span data-ttu-id="36ef9-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="36ef9-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="36ef9-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="36ef9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="36ef9-121">**visNoCtlHandles**</span><span class="sxs-lookup"><span data-stu-id="36ef9-121">**visNoCtlHandles**</span></span> <br/> |
   

