---
title: Ячейка ResizeMode (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Отображает текущий изменения размера для фигуры.
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814638"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="d9aaf-103">Ячейка ResizeMode (раздел "Преобразование фигуры")</span><span class="sxs-lookup"><span data-stu-id="d9aaf-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="d9aaf-104">Отображает текущий изменения размера для фигуры.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="d9aaf-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-105">**Value**</span></span>|<span data-ttu-id="d9aaf-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-106">**Description**</span></span>|<span data-ttu-id="d9aaf-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9aaf-108">0</span><span class="sxs-lookup"><span data-stu-id="d9aaf-108">0</span></span>  <br/> |<span data-ttu-id="d9aaf-109">Используйте значение группы.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="d9aaf-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="d9aaf-111">1</span><span class="sxs-lookup"><span data-stu-id="d9aaf-111">1</span></span>  <br/> |<span data-ttu-id="d9aaf-112">Только перемещение.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="d9aaf-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="d9aaf-114">2</span><span class="sxs-lookup"><span data-stu-id="d9aaf-114">2</span></span>  <br/> |<span data-ttu-id="d9aaf-115">Масштабирование с группой.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="d9aaf-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9aaf-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9aaf-117">Remarks</span></span>

<span data-ttu-id="d9aaf-118">Это значение также можно настроить на вкладке **поведение** в диалоговом окне " **поведение** " (на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md)в группе **Разработки фигуры** выберите **поведение**).</span><span class="sxs-lookup"><span data-stu-id="d9aaf-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="d9aaf-119">Чтобы получить ссылку на ячейку ResizeMode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d9aaf-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9aaf-120">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-120">Cell name:</span></span>  <br/> |<span data-ttu-id="d9aaf-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="d9aaf-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="d9aaf-122">Для получения ссылки на ячейки ResizeMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d9aaf-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9aaf-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d9aaf-123">Section index:</span></span>  <br/> |<span data-ttu-id="d9aaf-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d9aaf-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d9aaf-125">Row index:</span></span>  <br/> |<span data-ttu-id="d9aaf-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="d9aaf-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d9aaf-127">Cell index:</span></span>  <br/> |<span data-ttu-id="d9aaf-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="d9aaf-128">**visXFormResizeMode**</span></span> <br/> |
   

