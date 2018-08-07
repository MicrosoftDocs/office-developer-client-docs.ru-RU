---
title: Ячейка NoLiveDynamics (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Определяет фигуры динамически изменяет размер или поворот при работе с ней.
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814297"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="ce629-103">Ячейка NoLiveDynamics (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="ce629-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ce629-104">Определяет фигуры динамически изменяет размер или поворот при работе с ней.</span><span class="sxs-lookup"><span data-stu-id="ce629-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="ce629-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ce629-105">**Value**</span></span>|<span data-ttu-id="ce629-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce629-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ce629-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ce629-107">TRUE</span></span>  <br/> | <span data-ttu-id="ce629-108">Не обновляются динамически фигуры во время при работе с ней.</span><span class="sxs-lookup"><span data-stu-id="ce629-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="ce629-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ce629-109">FALSE</span></span>  <br/> | <span data-ttu-id="ce629-110">Динамическое обновление фигуры во время при работе с ней.</span><span class="sxs-lookup"><span data-stu-id="ce629-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce629-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="ce629-111">Remarks</span></span>

<span data-ttu-id="ce629-112">Как изменить размер или поворот двухмерных фигуры (2-D) без динамическое обновление появится прямоугольник выделения.</span><span class="sxs-lookup"><span data-stu-id="ce629-112">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box.</span></span> <span data-ttu-id="ce629-113">Если имеет одномерный (1-D), визуально основано на значения ячейки DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="ce629-113">If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="ce629-114">Чтобы получить ссылку на ячейку NoLiveDynamics по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ce629-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ce629-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ce629-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ce629-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="ce629-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="ce629-117">Для получения ссылки на ячейки NoLiveDynamics по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ce629-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ce629-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ce629-118">Section index:</span></span>  <br/> |<span data-ttu-id="ce629-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ce629-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ce629-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ce629-120">Row index:</span></span>  <br/> |<span data-ttu-id="ce629-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ce629-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ce629-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ce629-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ce629-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="ce629-123">**visNoLiveDynamics**</span></span> <br/> |
   

