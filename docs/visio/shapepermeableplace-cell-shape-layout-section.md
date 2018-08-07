---
title: Ячейка ShapePermeablePlace (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Определяет, можно было включить размещаемые фигуры поверх фигуры при размещении фигур в диалоговом окне "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814772"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="fba45-103">Ячейка ShapePermeablePlace (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="fba45-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="fba45-104">Определяет, можно было включить размещаемые фигуры поверх фигуры при размещении фигур в диалоговом окне " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку **Дополнительные параметры расположения **).</span><span class="sxs-lookup"><span data-stu-id="fba45-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="fba45-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fba45-105">**Value**</span></span>|<span data-ttu-id="fba45-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fba45-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fba45-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fba45-107">TRUE</span></span>  <br/> |<span data-ttu-id="fba45-108">Включение фигуры, чтобы поместить поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="fba45-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="fba45-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fba45-109">FALSE</span></span>  <br/> |<span data-ttu-id="fba45-110">Не следует включать фигуры, чтобы поместить поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="fba45-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fba45-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="fba45-111">Remarks</span></span>

<span data-ttu-id="fba45-112">Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ).</span><span class="sxs-lookup"><span data-stu-id="fba45-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="fba45-113">Более ранних чем Visio 2000 в версиях задайте это поведение, с помощью ObjInteract ячеек в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="fba45-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="fba45-114">Чтобы получить ссылку на ячейку ShapePermeablePlace по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="fba45-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fba45-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fba45-115">Cell name:</span></span>  <br/> |<span data-ttu-id="fba45-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="fba45-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="fba45-117">Для получения ссылки на ячейки ShapePermeablePlace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fba45-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fba45-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fba45-118">Section index:</span></span>  <br/> |<span data-ttu-id="fba45-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fba45-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fba45-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fba45-120">Row index:</span></span>  <br/> |<span data-ttu-id="fba45-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="fba45-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="fba45-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fba45-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fba45-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="fba45-123">**visSLOPermeablePlace**</span></span> <br/> |
   

