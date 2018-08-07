---
title: Функция SETATREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Перенаправляет обновленные значения, полученные в результате действий в пользовательского интерфейса (UI) или автоматизации в другую ячейку.
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814748"
---
# <a name="setatref-function"></a><span data-ttu-id="c2632-103">Функция SETATREF</span><span class="sxs-lookup"><span data-stu-id="c2632-103">SETATREF Function</span></span>

<span data-ttu-id="c2632-104">Перенаправляет обновленные значения, полученные в результате действий в пользовательского интерфейса (UI) или автоматизации в другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="c2632-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c2632-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2632-105">Syntax</span></span>

<span data-ttu-id="c2632-106">Функции SETATREF (** *ссылку* ** [, ** *set_expression* ** [, ** *ignore_eval* **]])</span><span class="sxs-lookup"><span data-stu-id="c2632-106">SETATREF(** *reference* ** [, ** *set_expression* ** [, ** *ignore_eval* ** ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c2632-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2632-107">Parameters</span></span>

|<span data-ttu-id="c2632-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c2632-108">**Name**</span></span>|<span data-ttu-id="c2632-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c2632-109">**Required/Optional**</span></span>|<span data-ttu-id="c2632-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c2632-110">**Data Type**</span></span>|<span data-ttu-id="c2632-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c2632-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c2632-112">_Справочник по_</span><span class="sxs-lookup"><span data-stu-id="c2632-112">_reference_</span></span> <br/> |<span data-ttu-id="c2632-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c2632-113">Required</span></span>  <br/> |<span data-ttu-id="c2632-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c2632-114">**String**</span></span> <br/> |<span data-ttu-id="c2632-115">Ссылка на ячейку, куда перенаправляются обновлений.</span><span class="sxs-lookup"><span data-stu-id="c2632-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="c2632-116">_Set_Expression_</span><span class="sxs-lookup"><span data-stu-id="c2632-116">_set_expression_</span></span> <br/> |<span data-ttu-id="c2632-117">Optional</span><span class="sxs-lookup"><span data-stu-id="c2632-117">Optional</span></span>  <br/> |<span data-ttu-id="c2632-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c2632-118">**String**</span></span> <br/> |<span data-ttu-id="c2632-119">Выражение, которое назначается _ссылка_.</span><span class="sxs-lookup"><span data-stu-id="c2632-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="c2632-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="c2632-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="c2632-121">Optional</span><span class="sxs-lookup"><span data-stu-id="c2632-121">Optional</span></span>  <br/> |<span data-ttu-id="c2632-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2632-122">**Boolean**</span></span> <br/> |<span data-ttu-id="c2632-123">Если значение TRUE, функция функции SETATREF вычисляет (0) 0. Если задано значение FALSE (по умолчанию) ВЫРАЖЕНИЕ_МНОЖЕСТВА функции оценивается как значение _ссылки_.</span><span class="sxs-lookup"><span data-stu-id="c2632-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2632-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2632-124">Remarks</span></span>

<span data-ttu-id="c2632-125">Когда действие пользователя в окне документа или метод автоматизации вызывает Microsoft Visio для обновления на ячейку, содержащую формулу ВЫРАЖЕНИЕ_МНОЖЕСТВА, значение вместо перенаправляется в ячейку, ссылается формула ВЫРАЖЕНИЕ_МНОЖЕСТВА ( _ссылки_).</span><span class="sxs-lookup"><span data-stu-id="c2632-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="c2632-126">Формулу в ячейку, содержащую ВЫРАЖЕНИЕ_МНОЖЕСТВА функции не изменяется.</span><span class="sxs-lookup"><span data-stu-id="c2632-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="c2632-127">Если _set_expression_ указан, значением, заданным в пользовательском Интерфейсе или с помощью автоматизации назначается ссылкой; в противном случае содержимое _set_expression_ назначаются ссылкой.</span><span class="sxs-lookup"><span data-stu-id="c2632-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="c2632-128">Это позволяет новое значение изменения или преобразовать перед, присваиваемое ссылкой.</span><span class="sxs-lookup"><span data-stu-id="c2632-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="c2632-129">Функция ВЫРАЖЕНИЕ_МНОЖЕСТВА имеет две связанные функции:</span><span class="sxs-lookup"><span data-stu-id="c2632-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="c2632-130">Функция SETATREFEXPR, которая используется для присвоения нового значения в пределах _set_expression_.</span><span class="sxs-lookup"><span data-stu-id="c2632-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="c2632-131">Например, _set_expression_ (SETATREFEXPR)-2 в.</span><span class="sxs-lookup"><span data-stu-id="c2632-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="c2632-132">может использоваться для вычитания 2 дюйма от SETATREFEXPR результатов.</span><span class="sxs-lookup"><span data-stu-id="c2632-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="c2632-133">Функция SETATREFEVAL, который можно использовать для указания, что некоторые части _set_expression_ должен быть вычисляется и заменяется его результатом.</span><span class="sxs-lookup"><span data-stu-id="c2632-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="c2632-134">Функция ВЫРАЖЕНИЕ_МНОЖЕСТВА предназначена для использования в ячейках, которые могут быть изменены действиями пользователя в окне документа.</span><span class="sxs-lookup"><span data-stu-id="c2632-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="c2632-135">Поддерживаются следующие ячейки:</span><span class="sxs-lookup"><span data-stu-id="c2632-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="c2632-136">Раздел ShapeTransform, Width, Height, угол, PinX и PinY ячеек</span><span class="sxs-lookup"><span data-stu-id="c2632-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="c2632-137">Раздел Преобразование текст — ШиринаТекста, ВысотаТекста, TxtAngle, TxtPinX и TxtPinY ячеек</span><span class="sxs-lookup"><span data-stu-id="c2632-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="c2632-138">Раздел 1 D конечных точек, BeginX, BeginY, EndX и EndY ячеек</span><span class="sxs-lookup"><span data-stu-id="c2632-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="c2632-139">Элементы управления section—Controls.X и Controls.Y ячейки</span><span class="sxs-lookup"><span data-stu-id="c2632-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="c2632-140">Раздел данных фигуры</span><span class="sxs-lookup"><span data-stu-id="c2632-140">Shape Data section</span></span>
    
<span data-ttu-id="c2632-141">Поскольку функции SETATREF изменяется местоположение, где изменение значений ячеек, влияет на события Click.</span><span class="sxs-lookup"><span data-stu-id="c2632-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="c2632-142">Если ячейка содержит функции SETATREF, события **FormulaChanged** и **CellChanged** возникают для ячейки, на который ссылается ВЫРАЖЕНИЕ_МНОЖЕСТВА, не содержащий функции SETATREF ячейки.</span><span class="sxs-lookup"><span data-stu-id="c2632-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="c2632-143">Если на ячейку, содержащую ВЫРАЖЕНИЕ_МНОЖЕСТВА также содержит SETATREFEXPR, событие **FormulaChanged** также запускается для ячейки, содержащий ВЫРАЖЕНИЕ_МНОЖЕСТВА из-за изменения параметра функции.</span><span class="sxs-lookup"><span data-stu-id="c2632-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="c2632-144">Другие важные замечания о ВЫРАЖЕНИЕ_МНОЖЕСТВА функции относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="c2632-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="c2632-145">Функции SETATREF функции можно объединять до 10 ссылки на другие функции ВЫРАЖЕНИЕ_МНОЖЕСТВА.</span><span class="sxs-lookup"><span data-stu-id="c2632-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="c2632-146">Ячейки могут содержать другие выражения в дополнение к ВЫРАЖЕНИЕ_МНОЖЕСТВА функции, включая несколько вхождений ВЫРАЖЕНИЕ_МНОЖЕСТВА в одну ячейку.</span><span class="sxs-lookup"><span data-stu-id="c2632-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="c2632-147">Если фигуры являются связан, Visio цепочка Справочник по функции SETATREF в том же листе и помещает связывающих формул в указанной ячейке.</span><span class="sxs-lookup"><span data-stu-id="c2632-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="c2632-148">Автоматизация распознает ВЫРАЖЕНИЕ_МНОЖЕСТВА функции и цепочка ссылок на ячейки.</span><span class="sxs-lookup"><span data-stu-id="c2632-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="c2632-149">Как УСЛОВИЕ функции SETATREF не обеспечивает защиту ячеек из изменения, внесенные с помощью функции SETF в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2632-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="c2632-150">Example1</span><span class="sxs-lookup"><span data-stu-id="c2632-150">Example1</span></span>

<span data-ttu-id="c2632-151">Предположим, фигуры на наличие настраиваемое свойство Width и ширина ячеек в разделе Преобразование фигуры содержит следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="c2632-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="c2632-152">=SETATREF(prop.Width)</span><span class="sxs-lookup"><span data-stu-id="c2632-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="c2632-153">Если пользователь изменить ширину фигуры в пользовательском Интерфейсе, новое значение назначается Prop.Width ячейки, не следует ширину ячеек в разделе ShapeTransform; формулы в ячейке ширина не изменяется.</span><span class="sxs-lookup"><span data-stu-id="c2632-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="c2632-154">Можно также задать ширину фигуры с помощью данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2632-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="c2632-155">Example2</span><span class="sxs-lookup"><span data-stu-id="c2632-155">Example2</span></span>

<span data-ttu-id="c2632-156">Решения Visio часто имеют фигуры, которые имеют иерархическую связь, требующие дочерних фигуры, чтобы переместить при перемещении родительскую фигуру.</span><span class="sxs-lookup"><span data-stu-id="c2632-156">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved.</span></span> <span data-ttu-id="c2632-157">Ниже приведен пример как вы управляете связь с помощью функции ВЫРАЖЕНИЕ_МНОЖЕСТВА в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2632-157">Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="c2632-158">В разделе Преобразование фигуры фигуры дочерних содержатся следующие формулы.</span><span class="sxs-lookup"><span data-stu-id="c2632-158">The following formulas are contained in the Shape Transform section of the child shape.</span></span> <span data-ttu-id="c2632-159">Кроме того мы определить пользователя ячеек, User.DeltaX и User.DeltaY, что отслеживать смещения измерения из ParentShape.</span><span class="sxs-lookup"><span data-stu-id="c2632-159">Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape.</span></span> <span data-ttu-id="c2632-160">Это позволяет фигуры дочерних перемещение при перемещении родительскую фигуру и сохранить иерархической связи, при перемещении фигуры дочерних.</span><span class="sxs-lookup"><span data-stu-id="c2632-160">This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="c2632-161">PinX = ВЫРАЖЕНИЕ_МНОЖЕСТВА (User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape! PinX)) + ParentShape! PinX</span><span class="sxs-lookup"><span data-stu-id="c2632-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="c2632-162">PinY = ВЫРАЖЕНИЕ_МНОЖЕСТВА (User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape! PinY)) + ParentShape! PinY</span><span class="sxs-lookup"><span data-stu-id="c2632-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="c2632-163">При перемещении фигуры дочерних с помощью пользовательского интерфейса в качестве параметра в функции SETATREFEXPR устанавливаются новые значения PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="c2632-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="c2632-164">ВЫРАЖЕНИЕ_МНОЖЕСТВА функции оценивает формулу, заключенные в SETATREFEVAL и заменяет их результаты PinX и PinY, и затем Результирующая формула назначается ссылки в функции SETATREF function—User.DeltaX и User.DeltaY ячеек пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2632-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="c2632-165">И, наконец значения, возвращаемые функции SETATREF (User.DeltaX или User.DeltaY) добавляются к месту ПИН-код ParentShape для вычисления расположение фигуры дочерних ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c2632-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

