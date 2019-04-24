---
title: Сведения о формулах
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Ключом к управлению действиями фигур является написание формул, определяющих требуемое поведение. Вы можете изменить формулу ячейки, чтобы изменить значение ячейки и, как следствие, изменить поведение конкретной фигуры. Например, ячейка Height в разделе Преобразование фигуры содержит формулу, которую можно изменить, чтобы изменить высоту фигуры.
ms.openlocfilehash: e8e1a2b77cc355e930af6f31f0b375dfba321e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344459"
---
# <a name="about-formulas"></a><span data-ttu-id="3f033-105">Сведения о формулах</span><span class="sxs-lookup"><span data-stu-id="3f033-105">About Formulas</span></span>

<span data-ttu-id="3f033-106">Ключом к управлению действиями фигур является написание формул, определяющих требуемое поведение.</span><span class="sxs-lookup"><span data-stu-id="3f033-106">The key to controlling shape actions is to write formulas that define the behavior you want.</span></span> <span data-ttu-id="3f033-107">Вы можете изменить формулу ячейки, чтобы изменить значение ячейки и, как следствие, изменить поведение конкретной фигуры.</span><span class="sxs-lookup"><span data-stu-id="3f033-107">You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior.</span></span> <span data-ttu-id="3f033-108">Например, ячейка Height в разделе Преобразование фигуры содержит формулу, которую можно изменить, чтобы изменить высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="3f033-108">For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="3f033-109">Формулы Microsoft Visio аналогичны типовым формулам электронных таблиц различными способами.</span><span class="sxs-lookup"><span data-stu-id="3f033-109">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways.</span></span> <span data-ttu-id="3f033-110">Visio рассчитает что-либо в ячейке, даже если это числовое значение или ссылка на простую ячейку, как формула.</span><span class="sxs-lookup"><span data-stu-id="3f033-110">Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="3f033-111">Формула в ячейке может быть унаследована от эквивалентной ячейки образца или стиля или определяться локально.</span><span class="sxs-lookup"><span data-stu-id="3f033-111">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally.</span></span> <span data-ttu-id="3f033-112">Visio оценивает формулу, а затем преобразует результаты в соответствующее значение и соответствующие единицы измерения для ячейки.</span><span class="sxs-lookup"><span data-stu-id="3f033-112">Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell.</span></span> <span data-ttu-id="3f033-113">В окне таблицы свойств фигуры можно отобразить содержимое ячейки в виде формул или значений.</span><span class="sxs-lookup"><span data-stu-id="3f033-113">In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="3f033-114">Элементы формулы</span><span class="sxs-lookup"><span data-stu-id="3f033-114">Elements of a formula</span></span>

<span data-ttu-id="3f033-115">Формула всегда начинается со знака равенства, который вставляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="3f033-115">A formula always starts with an equal sign, which is inserted automatically.</span></span> <span data-ttu-id="3f033-116">Формула может включать любой из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="3f033-116">A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="3f033-117">Числа</span><span class="sxs-lookup"><span data-stu-id="3f033-117">Numbers</span></span>
    
- <span data-ttu-id="3f033-118">Проверяем</span><span class="sxs-lookup"><span data-stu-id="3f033-118">Coordinates</span></span>
    
- <span data-ttu-id="3f033-119">Логические значения</span><span class="sxs-lookup"><span data-stu-id="3f033-119">Boolean values</span></span>
    
- <span data-ttu-id="3f033-120">Операторы</span><span class="sxs-lookup"><span data-stu-id="3f033-120">Operators</span></span>
    
- <span data-ttu-id="3f033-121">Функции</span><span class="sxs-lookup"><span data-stu-id="3f033-121">Functions</span></span>
    
- <span data-ttu-id="3f033-122">Строки</span><span class="sxs-lookup"><span data-stu-id="3f033-122">Strings</span></span>
    
- <span data-ttu-id="3f033-123">Ссылки на ячейки</span><span class="sxs-lookup"><span data-stu-id="3f033-123">Cell references</span></span>
    
- <span data-ttu-id="3f033-124">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="3f033-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="3f033-125">Формулы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3f033-125">Default formulas</span></span>

<span data-ttu-id="3f033-126">При создании фигуры Visio по умолчанию создает для нее формулы.</span><span class="sxs-lookup"><span data-stu-id="3f033-126">When you create a shape, Visio creates formulas for it by default.</span></span> <span data-ttu-id="3f033-127">Чтобы посмотреть, какие формулы используются по умолчанию, нарисуйте простую фигуру (например, прямоугольник, эллипс или прямую линию) и откройте окно таблицы свойств фигуры (на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) нажмите кнопку **Показать таблицу свойств фигуры**).</span><span class="sxs-lookup"><span data-stu-id="3f033-127">To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="3f033-128">НаСледуемые формулы</span><span class="sxs-lookup"><span data-stu-id="3f033-128">Inherited formulas</span></span>

<span data-ttu-id="3f033-129">По мере возможности Visio наследует формулы.</span><span class="sxs-lookup"><span data-stu-id="3f033-129">Visio inherits formulas whenever possible.</span></span> <span data-ttu-id="3f033-130">Вместо того чтобы создавать локальную копию каждой формулы в экземпляре, экземпляр наследует формулы из шаблона в наборе элементов документа и наследует форматирование из определения стиля, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="3f033-130">Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing.</span></span> <span data-ttu-id="3f033-131">Это приводит к уменьшению размера файлов, но также позволяет распространить изменения в формулах и определении стиля во все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="3f033-131">This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="3f033-132">Черный текст в ячейке указывает на наследуемую формулу.</span><span class="sxs-lookup"><span data-stu-id="3f033-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="3f033-133">Локальные формулы</span><span class="sxs-lookup"><span data-stu-id="3f033-133">Local formulas</span></span>

<span data-ttu-id="3f033-134">При написании локальной формулы для экземпляра заменяется Наследуемая формула в ячейке с помощью локального переопределения.</span><span class="sxs-lookup"><span data-stu-id="3f033-134">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override.</span></span> <span data-ttu-id="3f033-135">Будущие изменения этой ячейки в образце или стиле не повлияют на этот экземпляр, так как он заблокировал наследование для ячейки с локальным переопределением.</span><span class="sxs-lookup"><span data-stu-id="3f033-135">Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="3f033-136">При применении стиля все локальные формулы удаляются из связанных ячеек, если для их защиты не используется функция GUARD.</span><span class="sxs-lookup"><span data-stu-id="3f033-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="3f033-137">Синий текст указывает на локальную формулу либо на результат редактирования формулы в окне таблицы свойств фигуры, либо на изменение фигуры, которая привела к сбросу формулы для этой ячейки в Visio.</span><span class="sxs-lookup"><span data-stu-id="3f033-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="3f033-138">Автоматическое обновление формул</span><span class="sxs-lookup"><span data-stu-id="3f033-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="3f033-139">Visio автоматически обновляет определенные ячейки при каждом изменении фигуры в документе.</span><span class="sxs-lookup"><span data-stu-id="3f033-139">Visio automatically updates certain cells whenever you change a shape in a drawing.</span></span> <span data-ttu-id="3f033-140">Это означает, что в некоторых случаях вводимые формулы можно заменить.</span><span class="sxs-lookup"><span data-stu-id="3f033-140">This means that under some circumstances formulas you enter can be replaced.</span></span> <span data-ttu-id="3f033-141">Например, при перетаскивании углового маркера для изменения размера фигуры Visio сбрасывает формулы в ячейках PinX, PinY, Width и Height.</span><span class="sxs-lookup"><span data-stu-id="3f033-141">For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="3f033-142">При необходимости можно защитить формулы от изменений с помощью функции GUARD.</span><span class="sxs-lookup"><span data-stu-id="3f033-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

