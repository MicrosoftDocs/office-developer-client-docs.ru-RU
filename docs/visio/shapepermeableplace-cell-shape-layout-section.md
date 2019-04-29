---
title: ShapePermeablePlace Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Определяет, могут ли размещаемые фигуры размещаться поверх фигуры при разметке фигур в диалоговом окне "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427222"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="d729a-103">ShapePermeablePlace Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="d729a-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="d729a-104">Определяет, могут ли размещаемые фигуры размещаться поверх фигуры при разметке фигур в диалоговом окне **Настройка макета** (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**, а затем щелкните \*\*Дополнительные параметры макета). \*\*).</span><span class="sxs-lookup"><span data-stu-id="d729a-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="d729a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d729a-105">**Value**</span></span>|<span data-ttu-id="d729a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d729a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d729a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d729a-107">TRUE</span></span>  <br/> |<span data-ttu-id="d729a-108">Включение фигур, размещаемых поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="d729a-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="d729a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d729a-109">FALSE</span></span>  <br/> |<span data-ttu-id="d729a-110">Не включайте фигуры, которые должны размещаться поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="d729a-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d729a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="d729a-111">Remarks</span></span>

<span data-ttu-id="d729a-112">Вы также можете задать значение этой ячейки на вкладке " **Размещение** " в диалоговом окне **поведение** (с выбранной фигурой на вкладке " [разработчик](run-in-developer-mode-display-the-developer-tab.md) ", в группе " **Макет фигуры** " щелкните **поведение**, а затем перейдите на вкладку **Размещение** . ).</span><span class="sxs-lookup"><span data-stu-id="d729a-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="d729a-113">В версиях, предшествующих Visio 2000, это поведение задается с помощью ячейки Обжинтеракт в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="d729a-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="d729a-114">Чтобы получить ссылку на ячейку ShapePermeablePlace по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="d729a-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d729a-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d729a-115">Cell name:</span></span>  <br/> |<span data-ttu-id="d729a-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="d729a-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="d729a-117">Чтобы получить ссылку на ячейку ShapePermeablePlace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d729a-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d729a-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d729a-118">Section index:</span></span>  <br/> |<span data-ttu-id="d729a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d729a-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d729a-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d729a-120">Row index:</span></span>  <br/> |<span data-ttu-id="d729a-121">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="d729a-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="d729a-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d729a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d729a-123">**Висслопермеаблеплаце**</span><span class="sxs-lookup"><span data-stu-id="d729a-123">**visSLOPermeablePlace**</span></span> <br/> |
   

