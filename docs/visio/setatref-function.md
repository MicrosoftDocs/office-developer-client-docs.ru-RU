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
description: Перенаправляет обновленные значения в результате действий в пользовательском интерфейсе (пользовательском интерфейсе) или автоматизации в другую ячейку.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416806"
---
# <a name="setatref-function"></a><span data-ttu-id="f8eb3-103">Функция SETATREF</span><span class="sxs-lookup"><span data-stu-id="f8eb3-103">SETATREF Function</span></span>

<span data-ttu-id="f8eb3-104">Перенаправляет обновленные значения в результате действий в пользовательском интерфейсе (пользовательском интерфейсе) или автоматизации в другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f8eb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8eb3-105">Syntax</span></span>

<span data-ttu-id="f8eb3-106">SETATREF (\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span><span class="sxs-lookup"><span data-stu-id="f8eb3-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f8eb3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8eb3-107">Parameters</span></span>

|<span data-ttu-id="f8eb3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-108">**Name**</span></span>|<span data-ttu-id="f8eb3-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-109">**Required/Optional**</span></span>|<span data-ttu-id="f8eb3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-110">**Data Type**</span></span>|<span data-ttu-id="f8eb3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f8eb3-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="f8eb3-112">_reference_</span></span> <br/> |<span data-ttu-id="f8eb3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8eb3-113">Required</span></span>  <br/> |<span data-ttu-id="f8eb3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-114">**String**</span></span> <br/> |<span data-ttu-id="f8eb3-115">Ссылка на ячейку, в которой перенаправляются обновления.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="f8eb3-116">_set_expression_</span><span class="sxs-lookup"><span data-stu-id="f8eb3-116">_set_expression_</span></span> <br/> |<span data-ttu-id="f8eb3-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f8eb3-117">Optional</span></span>  <br/> |<span data-ttu-id="f8eb3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-118">**String**</span></span> <br/> |<span data-ttu-id="f8eb3-119">Выражение, назначенное _ссылкой._</span><span class="sxs-lookup"><span data-stu-id="f8eb3-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="f8eb3-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="f8eb3-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="f8eb3-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f8eb3-121">Optional</span></span>  <br/> |<span data-ttu-id="f8eb3-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="f8eb3-122">**Boolean**</span></span> <br/> |<span data-ttu-id="f8eb3-123">Если ЗНАЧЕНИЕ TRUE, функция SETATREF оценивается до (0) ноль; если FALSE (по умолчанию) функция SETATREF оценивается до значения  _справки_.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8eb3-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8eb3-124">Remarks</span></span>

<span data-ttu-id="f8eb3-125">Если действие пользователя в окне рисования или метод автоматизации приводит к обновлению ячейки Visio содержащей формулу SETATREF, значение перенаправляется на ячейку, направляемую по формуле SETATREF _(ссылка)._</span><span class="sxs-lookup"><span data-stu-id="f8eb3-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="f8eb3-126">Формула в ячейке, содержащей функцию SETATREF, остается нетронутой.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="f8eb3-127">Если  _set_expression_ опущен, значение, задатое в пользовательском интерфейсе или с помощью автоматизации, назначено на ссылаемую ячейку; в противном случае содержимое  _set_expression_ назначено со ссылкой на ячейку.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="f8eb3-128">Это позволяет изменять или изменять новое значение перед тем, как ему назначена эталонная ячейка.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="f8eb3-129">Функция SETATREF имеет две связанные функции:</span><span class="sxs-lookup"><span data-stu-id="f8eb3-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="f8eb3-130">Функция SETATREFEXPR, которую можно использовать для представления нового значения в _set_expression._</span><span class="sxs-lookup"><span data-stu-id="f8eb3-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="f8eb3-131">Например,  _set_expression_ SETATREFEXPR()-2.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="f8eb3-132">может использоваться для вычитания 2 дюймов из результата SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="f8eb3-133">Функция SETATREFEVAL, с помощью  _которой_ можно указать, что часть set_expression должна быть оценена и заменена ее результатом.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="f8eb3-134">Функция SETATREF предназначена для использования в ячейках, которые могут быть изменены действиями пользователя в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="f8eb3-135">Поддерживаются следующие ячейки:</span><span class="sxs-lookup"><span data-stu-id="f8eb3-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="f8eb3-136">Раздел ShapeTransform — ячейки Ширина, Высота, Угол, PinX и PinY</span><span class="sxs-lookup"><span data-stu-id="f8eb3-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="f8eb3-137">Раздел Преобразование текста— ячейки TxtWidth, TxtHeight, TxtAngle, TxtPinX и TxtPinY</span><span class="sxs-lookup"><span data-stu-id="f8eb3-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="f8eb3-138">Раздел Конечные точки 1-D— ячейки BeginX, BeginY, EndX и EndY</span><span class="sxs-lookup"><span data-stu-id="f8eb3-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="f8eb3-139">Раздел Элементы управления— ячейки Controls.X и Controls.Y</span><span class="sxs-lookup"><span data-stu-id="f8eb3-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="f8eb3-140">Раздел "Данные фигуры"</span><span class="sxs-lookup"><span data-stu-id="f8eb3-140">Shape Data section</span></span>
    
<span data-ttu-id="f8eb3-141">Поскольку SETATREF изменяет расположение, в котором изменяются значения ячейки, это влияет на стрельбу события.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="f8eb3-142">Если ячейка содержит SETATREF, события **FormulaChanged** и **CellChanged** загорелись для ячейки, на которую ссылается SETATREF, а не ячейки, содержащей SETATREF.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="f8eb3-143">Если ячейка, содержащая SETATREF, также содержит SETATREFEXPR, событие **FormulaChanged** также включает ячейку, содержащую SETATREF, так как изменен параметр функции.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="f8eb3-144">Другие важные моменты, которые следует отметить в функции SETATREF, включают следующие:</span><span class="sxs-lookup"><span data-stu-id="f8eb3-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="f8eb3-145">Функции SETATREF могут цепи до 10 ссылок на другие функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="f8eb3-146">Ячейки могут содержать другие выражения в дополнение к функции SETATREF, в том числе несколько случаев SETATREF в одной ячейке.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="f8eb3-147">Если фигуры приклеены, Visio цепочку ссылок SETATREF в том же листе и помещает формулы клея в ссылаемую ячейку.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="f8eb3-148">Автоматизация распознает функцию SETATREF и следует по цепочке ссыланых ячеек.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="f8eb3-149">Как и GUARD, SETATREF не защищает ячейки от изменений, внесенных с помощью функции SETF в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="f8eb3-150">Пример1</span><span class="sxs-lookup"><span data-stu-id="f8eb3-150">Example1</span></span>

<span data-ttu-id="f8eb3-151">Предположим, что фигура имеет настраиваемое свойство Width и что ячейка Width в разделе Преобразование формы содержит следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="f8eb3-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="f8eb3-152">=SETATREF (Prop.Width)</span><span class="sxs-lookup"><span data-stu-id="f8eb3-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="f8eb3-153">Если пользователь должен был изменить ширину формы в пользовательском интерфейсе, новое значение назначено ячейке Prop.Width, а не ячейке Width в разделе ShapeTransform; формула в ячейке Ширина остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="f8eb3-154">Ширину фигуры можно также установить с помощью данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="f8eb3-155">Example2</span><span class="sxs-lookup"><span data-stu-id="f8eb3-155">Example2</span></span>

<span data-ttu-id="f8eb3-156">Visio решения часто имеют фигуры с иерархическими отношениями, требующие перемещения фигур ребенка при перемещении родительской фигуры.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-156">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved.</span></span> <span data-ttu-id="f8eb3-157">Ниже приводится пример управления этим отношением с помощью функции SETATREF в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-157">Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="f8eb3-158">Следующие формулы содержатся в разделе Преобразование формы фигуры ребенка.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-158">The following formulas are contained in the Shape Transform section of the child shape.</span></span> <span data-ttu-id="f8eb3-159">Кроме того, мы определяем ячейки пользователей, называемые User.DeltaX и User.DeltaY, которые отслеживают смещение измерения из ParentShape.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-159">Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape.</span></span> <span data-ttu-id="f8eb3-160">Это позволяет ребенку двигаться при перемещении родительской фигуры, а также сохранять иерархические отношения при перемещении фигуры ребенка.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-160">This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="f8eb3-161">PinX =SETATREF (User.DeltaX, SETATREFEVAL(SETATREFEXPR)-ParentShape! PinX)) + ParentShape! PinX</span><span class="sxs-lookup"><span data-stu-id="f8eb3-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="f8eb3-162">Piny =SETATREF (User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape! PinY)) + ParentShape! PinY</span><span class="sxs-lookup"><span data-stu-id="f8eb3-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="f8eb3-163">При перемещении фигуры ребенка с помощью пользовательского интерфейса в функции SETATREFEXPR заданы новые значения PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="f8eb3-164">Функция SETATREF оценивает формулу, заключенную в SETATREFEVAL, и заменяет результаты PinX и PinY, а затем выдаваемая формула назначена ячейкам пользователей, на которые ссылается функция SETATREF— User.DeltaX и User.DeltaY.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="f8eb3-165">Наконец, значения, возвращенные SETATREF (User.DeltaX или User.DeltaY), добавляются в расположение пин-кода ParentShape для вычисления расположения пин-кода фигуры ребенка.</span><span class="sxs-lookup"><span data-stu-id="f8eb3-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

