---
title: Ячейка ShapePermeableY (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Определяет ли соединитель могут перенаправлять вертикально через фигуру.
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814769"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="9b999-103">Ячейка ShapePermeableY (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="9b999-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9b999-104">Определяет ли соединитель могут перенаправлять вертикально через фигуру.</span><span class="sxs-lookup"><span data-stu-id="9b999-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="9b999-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9b999-105">**Value**</span></span>|<span data-ttu-id="9b999-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9b999-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b999-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9b999-107">TRUE</span></span>  <br/> |<span data-ttu-id="9b999-108">Включение соединителей для маршрутизации вертикально через фигуру.</span><span class="sxs-lookup"><span data-stu-id="9b999-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="9b999-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9b999-109">FALSE</span></span>  <br/> |<span data-ttu-id="9b999-110">Нельзя допускать маршрут соединители вертикально через фигуру.</span><span class="sxs-lookup"><span data-stu-id="9b999-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b999-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b999-111">Remarks</span></span>

<span data-ttu-id="9b999-112">Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ).</span><span class="sxs-lookup"><span data-stu-id="9b999-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="9b999-113">В версии более ранней, чем Visio 2000 устанавливаются это поведение с помощью ObjInteract ячейки в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="9b999-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="9b999-114">Чтобы получить ссылку на ячейку ShapePermeableY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9b999-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b999-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9b999-115">Cell name:</span></span>  <br/> |<span data-ttu-id="9b999-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="9b999-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="9b999-117">Для получения ссылки на ячейки ShapePermeableY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9b999-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b999-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9b999-118">Section index:</span></span>  <br/> |<span data-ttu-id="9b999-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b999-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9b999-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9b999-120">Row index:</span></span>  <br/> |<span data-ttu-id="9b999-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9b999-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9b999-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b999-122">Cell index:</span></span>  <br/> |<span data-ttu-id="9b999-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="9b999-123">**visSLOPermY**</span></span> <br/> |
   

