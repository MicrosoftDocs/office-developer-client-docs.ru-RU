---
title: Формулы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Ключ для управления действия фигуры является написание формул, которые определяют желаемое поведение. Вы можете изменить формулу ячейки изменять значение ячейки, и в результате изменить поведение конкретного фигуры. Например высота ячеек в разделе Преобразование фигуры содержит формулу, можно изменить для изменения фигуры высоту.
ms.openlocfilehash: 7df5ffe4d3dc32bcd5209bde353c39a92c7d422b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813105"
---
# <a name="about-formulas"></a><span data-ttu-id="43639-105">Формулы</span><span class="sxs-lookup"><span data-stu-id="43639-105">About Formulas</span></span>

<span data-ttu-id="43639-106">Ключ для управления действия фигуры является написание формул, которые определяют желаемое поведение.</span><span class="sxs-lookup"><span data-stu-id="43639-106">The key to controlling shape actions is to write formulas that define the behavior you want.</span></span> <span data-ttu-id="43639-107">Вы можете изменить формулу ячейки изменять значение ячейки, и в результате изменить поведение конкретного фигуры.</span><span class="sxs-lookup"><span data-stu-id="43639-107">You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior.</span></span> <span data-ttu-id="43639-108">Например высота ячеек в разделе Преобразование фигуры содержит формулу, можно изменить для изменения фигуры высоту.</span><span class="sxs-lookup"><span data-stu-id="43639-108">For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="43639-109">Microsoft Visio формулы похожи на типичной электронной таблице формулы различными способами.</span><span class="sxs-lookup"><span data-stu-id="43639-109">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways.</span></span> <span data-ttu-id="43639-110">Visio указаниям ничего в ячейке, даже если он является числовым значением или ссылка на ячейку простой, как формулы.</span><span class="sxs-lookup"><span data-stu-id="43639-110">Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="43639-111">Формулы в ячейке можно наследуется от эквивалентный ячейка главный или стиля или определенные локально.</span><span class="sxs-lookup"><span data-stu-id="43639-111">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally.</span></span> <span data-ttu-id="43639-112">Visio оцениваются формулы и затем преобразует результаты в соответствующее значение и соответствующие единицы измерения для ячейки.</span><span class="sxs-lookup"><span data-stu-id="43639-112">Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell.</span></span> <span data-ttu-id="43639-113">В окне таблицы свойств фигуры вы можете отобразить содержимое ячейки формулы или значения.</span><span class="sxs-lookup"><span data-stu-id="43639-113">In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="43639-114">Элементы формулы</span><span class="sxs-lookup"><span data-stu-id="43639-114">Elements of a formula</span></span>

<span data-ttu-id="43639-115">Формула всегда начинается с знак равенства, автоматически вставляется.</span><span class="sxs-lookup"><span data-stu-id="43639-115">A formula always starts with an equal sign, which is inserted automatically.</span></span> <span data-ttu-id="43639-116">Формула может содержать следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="43639-116">A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="43639-117">�����</span><span class="sxs-lookup"><span data-stu-id="43639-117">Numbers</span></span>
    
- <span data-ttu-id="43639-118">Координаты</span><span class="sxs-lookup"><span data-stu-id="43639-118">Coordinates</span></span>
    
- <span data-ttu-id="43639-119">Логические значения</span><span class="sxs-lookup"><span data-stu-id="43639-119">Boolean values</span></span>
    
- <span data-ttu-id="43639-120">Операторы</span><span class="sxs-lookup"><span data-stu-id="43639-120">Operators</span></span>
    
- <span data-ttu-id="43639-121">�������</span><span class="sxs-lookup"><span data-stu-id="43639-121">Functions</span></span>
    
- <span data-ttu-id="43639-122">������</span><span class="sxs-lookup"><span data-stu-id="43639-122">Strings</span></span>
    
- <span data-ttu-id="43639-123">Ссылки на ячейки</span><span class="sxs-lookup"><span data-stu-id="43639-123">Cell references</span></span>
    
- <span data-ttu-id="43639-124">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="43639-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="43639-125">По умолчанию формул</span><span class="sxs-lookup"><span data-stu-id="43639-125">Default formulas</span></span>

<span data-ttu-id="43639-126">При создании фигуры Visio создает формулы для него по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43639-126">When you create a shape, Visio creates formulas for it by default.</span></span> <span data-ttu-id="43639-127">Чтобы узнать, что формулы по умолчанию, нарисовать простую фигуру (прямоугольник, эллипс или прямой) и откройте его окно таблицы свойств фигуры (на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) выберите **Показать таблицу свойств фигуры**).</span><span class="sxs-lookup"><span data-stu-id="43639-127">To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="43639-128">Наследуемые формул</span><span class="sxs-lookup"><span data-stu-id="43639-128">Inherited formulas</span></span>

<span data-ttu-id="43639-129">Visio наследует формул, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="43639-129">Visio inherits formulas whenever possible.</span></span> <span data-ttu-id="43639-130">А не в экземпляре сделать локальной копии каждой формулы, экземпляр наследует формулы с его основного элементов документа и наследует параметры форматирования от определения стилей, хранятся вместе с документа.</span><span class="sxs-lookup"><span data-stu-id="43639-130">Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing.</span></span> <span data-ttu-id="43639-131">Это приводит к файлов меньшего размера, но также позволяет изменения главной формулы или определение стиля распространить все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="43639-131">This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="43639-132">Черный текст в ячейке указывает наследуемые формулы.</span><span class="sxs-lookup"><span data-stu-id="43639-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="43639-133">Локальные формулы</span><span class="sxs-lookup"><span data-stu-id="43639-133">Local formulas</span></span>

<span data-ttu-id="43639-134">При записи локального формулу для экземпляра замены унаследованного формулы в ячейке локального переопределения.</span><span class="sxs-lookup"><span data-stu-id="43639-134">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override.</span></span> <span data-ttu-id="43639-135">Будущие изменения в этой ячейке в основной или стиля не влияют на этот экземпляр, так как он был заблокирован наследования для ячейки с локального переопределения.</span><span class="sxs-lookup"><span data-stu-id="43639-135">Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="43639-136">Применение стиля удаляет все локальные формулы в ячейках, связанных с ними, если не использовать функцию защиты для защиты.</span><span class="sxs-lookup"><span data-stu-id="43639-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="43639-137">Синий текст указывает локальную формулу, либо в результате редактирования формулы в окне таблицы свойств фигуры или некоторые изменения фигуры, в которой обнаружен Visio Сброс формулу для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="43639-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="43639-138">Автоматические обновления для формул</span><span class="sxs-lookup"><span data-stu-id="43639-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="43639-139">При любом изменении фигуры в документе Visio автоматически обновляет определенные ячейки.</span><span class="sxs-lookup"><span data-stu-id="43639-139">Visio automatically updates certain cells whenever you change a shape in a drawing.</span></span> <span data-ttu-id="43639-140">Это означает, что в некоторых случаях формул при вводе может быть заменен.</span><span class="sxs-lookup"><span data-stu-id="43639-140">This means that under some circumstances formulas you enter can be replaced.</span></span> <span data-ttu-id="43639-141">Например при перетаскивании углового маркера для изменения размера фигуры Visio сбрасывает формулы в ячейках PinX, PinY, ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="43639-141">For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="43639-142">При необходимости можно защищать формулы от изменений с помощью функции защиты.</span><span class="sxs-lookup"><span data-stu-id="43639-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

