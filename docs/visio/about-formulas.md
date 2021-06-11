---
title: О формулах
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Ключ к управлению действиями фигуры — это написание формул, определяющих нужное поведение. Вы можете изменить формулу ячейки, чтобы изменить значение ячейки и, как следствие, изменить поведение определенной фигуры. Например, ячейка Height в разделе Преобразование фигуры содержит формулу, которую можно изменить, чтобы изменить высоту фигуры.
ms.openlocfilehash: e8e1a2b77cc355e930af6f31f0b375dfba321e74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426263"
---
# <a name="about-formulas"></a><span data-ttu-id="13e63-105">О формулах</span><span class="sxs-lookup"><span data-stu-id="13e63-105">About Formulas</span></span>

<span data-ttu-id="13e63-106">Ключ к управлению действиями фигуры — это написание формул, определяющих нужное поведение.</span><span class="sxs-lookup"><span data-stu-id="13e63-106">The key to controlling shape actions is to write formulas that define the behavior you want.</span></span> <span data-ttu-id="13e63-107">Вы можете изменить формулу ячейки, чтобы изменить значение ячейки и, как следствие, изменить поведение определенной фигуры.</span><span class="sxs-lookup"><span data-stu-id="13e63-107">You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior.</span></span> <span data-ttu-id="13e63-108">Например, ячейка Height в разделе Преобразование фигуры содержит формулу, которую можно изменить, чтобы изменить высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="13e63-108">For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="13e63-109">Формулы microsoft Visio похожи на типичные формулы таблиц во многих отношениях.</span><span class="sxs-lookup"><span data-stu-id="13e63-109">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways.</span></span> <span data-ttu-id="13e63-110">Visio что-либо в ячейке, даже если это числовая ссылка или простая ссылка ячейки, в качестве формулы.</span><span class="sxs-lookup"><span data-stu-id="13e63-110">Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="13e63-111">Формула в ячейке может быть унаследована от эквивалентной ячейки мастера или стиля или определена локально.</span><span class="sxs-lookup"><span data-stu-id="13e63-111">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally.</span></span> <span data-ttu-id="13e63-112">Visio оценивает формулу, а затем преобразует результаты в соответствующее значение и соответствующие единицы для ячейки.</span><span class="sxs-lookup"><span data-stu-id="13e63-112">Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell.</span></span> <span data-ttu-id="13e63-113">В окне ShapeSheet содержимое ячейки можно отображать как формулы, так и значения.</span><span class="sxs-lookup"><span data-stu-id="13e63-113">In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="13e63-114">Элементы формулы</span><span class="sxs-lookup"><span data-stu-id="13e63-114">Elements of a formula</span></span>

<span data-ttu-id="13e63-115">Формула всегда начинается с равного знака, который вставляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="13e63-115">A formula always starts with an equal sign, which is inserted automatically.</span></span> <span data-ttu-id="13e63-116">Формула может включать любой из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="13e63-116">A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="13e63-117">Числа</span><span class="sxs-lookup"><span data-stu-id="13e63-117">Numbers</span></span>
    
- <span data-ttu-id="13e63-118">Координаты</span><span class="sxs-lookup"><span data-stu-id="13e63-118">Coordinates</span></span>
    
- <span data-ttu-id="13e63-119">Значения Boolean</span><span class="sxs-lookup"><span data-stu-id="13e63-119">Boolean values</span></span>
    
- <span data-ttu-id="13e63-120">Операторы</span><span class="sxs-lookup"><span data-stu-id="13e63-120">Operators</span></span>
    
- <span data-ttu-id="13e63-121">Functions</span><span class="sxs-lookup"><span data-stu-id="13e63-121">Functions</span></span>
    
- <span data-ttu-id="13e63-122">Строки</span><span class="sxs-lookup"><span data-stu-id="13e63-122">Strings</span></span>
    
- <span data-ttu-id="13e63-123">Ссылки на ячейки</span><span class="sxs-lookup"><span data-stu-id="13e63-123">Cell references</span></span>
    
- <span data-ttu-id="13e63-124">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="13e63-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="13e63-125">Формулы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="13e63-125">Default formulas</span></span>

<span data-ttu-id="13e63-126">При создании фигуры Visio формулы для нее по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13e63-126">When you create a shape, Visio creates formulas for it by default.</span></span> <span data-ttu-id="13e63-127">Чтобы узнать, что такое формулы по умолчанию, нарисуйте простую форму (например, прямоугольник, эллипс или [](run-in-developer-mode-display-the-developer-tab.md) прямая линия) и откройте окно ShapeSheet (на вкладке Разработчик щелкните **Show ShapeSheet).**</span><span class="sxs-lookup"><span data-stu-id="13e63-127">To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="13e63-128">Унаследованные формулы</span><span class="sxs-lookup"><span data-stu-id="13e63-128">Inherited formulas</span></span>

<span data-ttu-id="13e63-129">Visio наследует формулы по мере возможности.</span><span class="sxs-lookup"><span data-stu-id="13e63-129">Visio inherits formulas whenever possible.</span></span> <span data-ttu-id="13e63-130">Вместо того, чтобы сделать локализованную копию каждой формулы в экземпляре, экземпляр наследует формулы своего мастера на трафарете документа и наследует форматирование из определения стиля, хранимого с помощью рисунка.</span><span class="sxs-lookup"><span data-stu-id="13e63-130">Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing.</span></span> <span data-ttu-id="13e63-131">Это поведение приводит к меньшему размеру файлов, но также позволяет распространять во все экземпляры изменения формул мастера или определения стиля.</span><span class="sxs-lookup"><span data-stu-id="13e63-131">This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="13e63-132">Черный текст в ячейке указывает унаследованные формулы.</span><span class="sxs-lookup"><span data-stu-id="13e63-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="13e63-133">Локальные формулы</span><span class="sxs-lookup"><span data-stu-id="13e63-133">Local formulas</span></span>

<span data-ttu-id="13e63-134">При написании локальной формулы экземпляра наследуемая формула в ячейке заменяется локальной переопределяемой.</span><span class="sxs-lookup"><span data-stu-id="13e63-134">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override.</span></span> <span data-ttu-id="13e63-135">Будущие изменения в этой ячейке в мастере или стиле не влияют на этот экземпляр, так как он заблокировал наследование ячейки с локальным переопределить.</span><span class="sxs-lookup"><span data-stu-id="13e63-135">Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="13e63-136">Применение стиля удаляет все локальные формулы в связанных ячейках, если только вы не используете функцию GUARD для их защиты.</span><span class="sxs-lookup"><span data-stu-id="13e63-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="13e63-137">Синий текст указывает локализованную формулу: либо результат редактирования формулы в окне ShapeSheet, либо изменение формы, из-за чего Visio для сброса формулы для этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="13e63-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="13e63-138">Автоматическое обновление формул</span><span class="sxs-lookup"><span data-stu-id="13e63-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="13e63-139">Visio автоматически обновляет определенные ячейки при изменении фигуры в рисунке.</span><span class="sxs-lookup"><span data-stu-id="13e63-139">Visio automatically updates certain cells whenever you change a shape in a drawing.</span></span> <span data-ttu-id="13e63-140">Это означает, что при определенных обстоятельствах введите формулы можно заменить.</span><span class="sxs-lookup"><span data-stu-id="13e63-140">This means that under some circumstances formulas you enter can be replaced.</span></span> <span data-ttu-id="13e63-141">Например, если перетаскивать угловую ручку для повторного размеров фигуры, Visio сбрасывает формулы в ячейках PinX, PinY, Width и Height.</span><span class="sxs-lookup"><span data-stu-id="13e63-141">For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="13e63-142">При необходимости можно защитить формулы от изменений с помощью функции GUARD.</span><span class="sxs-lookup"><span data-stu-id="13e63-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

