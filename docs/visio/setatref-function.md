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
description: Перенаправляет обновленные значения, которые являются результатом действий в пользовательском интерфейсе или автоматизации, в другую ячейку.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416806"
---
# <a name="setatref-function"></a><span data-ttu-id="ac605-103">Функция SETATREF</span><span class="sxs-lookup"><span data-stu-id="ac605-103">SETATREF Function</span></span>

<span data-ttu-id="ac605-104">Перенаправляет обновленные значения, которые являются результатом действий в пользовательском интерфейсе или автоматизации, в другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="ac605-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ac605-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac605-105">Syntax</span></span>

<span data-ttu-id="ac605-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span><span class="sxs-lookup"><span data-stu-id="ac605-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ac605-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac605-107">Parameters</span></span>

|<span data-ttu-id="ac605-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ac605-108">**Name**</span></span>|<span data-ttu-id="ac605-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ac605-109">**Required/Optional**</span></span>|<span data-ttu-id="ac605-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ac605-110">**Data Type**</span></span>|<span data-ttu-id="ac605-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac605-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ac605-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="ac605-112">_reference_</span></span> <br/> |<span data-ttu-id="ac605-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ac605-113">Required</span></span>  <br/> |<span data-ttu-id="ac605-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ac605-114">**String**</span></span> <br/> |<span data-ttu-id="ac605-115">Ссылка на ячейку, в которой перенаправляются обновления.</span><span class="sxs-lookup"><span data-stu-id="ac605-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="ac605-116">_set_expression_</span><span class="sxs-lookup"><span data-stu-id="ac605-116">_set_expression_</span></span> <br/> |<span data-ttu-id="ac605-117">Необязательна</span><span class="sxs-lookup"><span data-stu-id="ac605-117">Optional</span></span>  <br/> |<span data-ttu-id="ac605-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ac605-118">**String**</span></span> <br/> |<span data-ttu-id="ac605-119">Выражение, назначенное для _ссылки._</span><span class="sxs-lookup"><span data-stu-id="ac605-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="ac605-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="ac605-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="ac605-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ac605-121">Optional</span></span>  <br/> |<span data-ttu-id="ac605-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="ac605-122">**Boolean**</span></span> <br/> |<span data-ttu-id="ac605-123">Если установлено значение TRUE, функция SETATREF оценивается как (0) ноль; Если задается значение FALSE (по умолчанию), функция SETATREF оценивается как значение _ссылки._</span><span class="sxs-lookup"><span data-stu-id="ac605-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac605-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac605-124">Remarks</span></span>

<span data-ttu-id="ac605-125">Когда действие пользователя в окне рисования или метод автоматизации приводит к обновлению Microsoft Visio ячейки, содержащей формулу SETATREF, значение перенаправляется в ячейку, на которая ссылается формула SETATREF (ссылка).</span><span class="sxs-lookup"><span data-stu-id="ac605-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="ac605-126">Формула в ячейке, содержащей функцию SETATREF, остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="ac605-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="ac605-127">Если  _set_expression_ элементов опущен, значение, задамое в пользовательском интерфейсе или с помощью автоматизации, будет назначено ячейке, на который ссылается ссылка; в противном случае содержимое  _set_expression,_ назначенное ячейке, на который ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="ac605-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="ac605-128">Это позволяет изменять или преобразовывать новое значение перед присвоением ячейке, на который ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="ac605-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="ac605-129">Функция SETATREF имеет две связанные функции:</span><span class="sxs-lookup"><span data-stu-id="ac605-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="ac605-130">Функция SETATREFEXPR, которую можно использовать для представления нового значения  _в_ set_expression.</span><span class="sxs-lookup"><span data-stu-id="ac605-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="ac605-131">Например,  _set_expression_ setATREFEXPR()-2 in.</span><span class="sxs-lookup"><span data-stu-id="ac605-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="ac605-132">может использоваться для вычитания 2 дюйма из результата SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="ac605-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="ac605-133">Функция SETATREFEVAL, которую можно использовать, чтобы  указать, что некоторые части set_expression должны быть оценены и заменены ее результатом.</span><span class="sxs-lookup"><span data-stu-id="ac605-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="ac605-134">Функция SETATREF предназначена для использования в ячейках, которые можно изменить с помощью действий пользователя в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="ac605-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="ac605-135">Поддерживаются следующие ячейки:</span><span class="sxs-lookup"><span data-stu-id="ac605-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="ac605-136">Раздел ShapeTransform — ячейки Width, Height, Angle, PinX и PinY</span><span class="sxs-lookup"><span data-stu-id="ac605-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="ac605-137">Раздел "Преобразование текста" — ячейки TxtWidth, TxtHeight, TxtAngle, TxtPinX и TxtPinY</span><span class="sxs-lookup"><span data-stu-id="ac605-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="ac605-138">Раздел "1-D Endpoints" — ячейки BeginX, BeginY, EndX и EndY</span><span class="sxs-lookup"><span data-stu-id="ac605-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="ac605-139">Раздел "Элементы управления" — ячейки Controls.X и Controls.Y</span><span class="sxs-lookup"><span data-stu-id="ac605-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="ac605-140">Раздел "Данные фигуры"</span><span class="sxs-lookup"><span data-stu-id="ac605-140">Shape Data section</span></span>
    
<span data-ttu-id="ac605-141">Так как SETATREF изменяет расположение, в котором изменяются значения ячеей, это влияет на событие.</span><span class="sxs-lookup"><span data-stu-id="ac605-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="ac605-142">Если ячейка содержит SETATREF, события **FormulaChanged** и **CellChanged** сгораются для ячейки, на которую ссылается SETATREF, а не для ячейки, содержащей SETATREF.</span><span class="sxs-lookup"><span data-stu-id="ac605-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="ac605-143">Если ячейка, содержащая SETATREF, также содержит SETATREFEXPR, событие **FormulaChanged** также сгореет для ячейки, содержащей SETATREF, поскольку изменен параметр функции.</span><span class="sxs-lookup"><span data-stu-id="ac605-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="ac605-144">К другим важным моментам, которые следует обратить внимание на функцию SETATREF, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="ac605-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="ac605-145">Функции SETATREF могут сцеплять до 10 ссылок на другие функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="ac605-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="ac605-146">Ячейки могут содержать другие выражения в дополнение к функции SETATREF, включая несколько экземпляров SETATREF в одной ячейке.</span><span class="sxs-lookup"><span data-stu-id="ac605-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="ac605-147">Если фигуры привязались, Visio следует цепочке ссылок SETATREF на том же листе и помещает формулы привязок в ячейку со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="ac605-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="ac605-148">Автоматизация распознает функцию SETATREF и следует за цепочкой ячеек, на которые есть ссылка.</span><span class="sxs-lookup"><span data-stu-id="ac605-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="ac605-149">Как и GUARD, SETATREF не защищает ячейки от изменений, внесенных с помощью функции SETF в shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ac605-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="ac605-150">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac605-150">Example1</span></span>

<span data-ttu-id="ac605-151">Предположим, что фигура имеет настраиваемое свойство Width, а ячейка Width в разделе "Преобразование фигуры" содержит следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="ac605-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="ac605-152">=SETATREF(Prop.Width)</span><span class="sxs-lookup"><span data-stu-id="ac605-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="ac605-153">Если пользователь должен изменить ширину фигуры в пользовательском интерфейсе, новое значение будет назначено ячейке Prop.Width, а не ячейке Width в разделе ShapeTransform; формула в ячейке Width остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="ac605-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="ac605-154">Вы также можете установить ширину фигуры с помощью данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="ac605-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="ac605-155">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ac605-155">Example2</span></span>

<span data-ttu-id="ac605-156">Решения Visio часто имеют фигуры с иерархической связью, требующие перемещения родительских фигур при перемещении.</span><span class="sxs-lookup"><span data-stu-id="ac605-156">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved.</span></span> <span data-ttu-id="ac605-157">Ниже приводится пример управления этой связью с помощью функции SETATREF в shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ac605-157">Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="ac605-158">Следующие формулы содержатся в разделе "Преобразование фигуры" для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="ac605-158">The following formulas are contained in the Shape Transform section of the child shape.</span></span> <span data-ttu-id="ac605-159">Кроме того, мы определяем ячейки пользователей User.DeltaX и User.DeltaY, которые отслеживают измерение смещения от ParentShape.</span><span class="sxs-lookup"><span data-stu-id="ac605-159">Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape.</span></span> <span data-ttu-id="ac605-160">Это позволяет переместить родительская фигура при перемещении родительской фигуры, а также сохранить иерархическую связь при перемещении этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="ac605-160">This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="ac605-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape! PinX)) + ParentShape! PinX</span><span class="sxs-lookup"><span data-stu-id="ac605-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="ac605-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape! PinY)) + ParentShape! PinY</span><span class="sxs-lookup"><span data-stu-id="ac605-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="ac605-163">При перемещении фигуры с помощью пользовательского интерфейса новые значения PinX и PinY устанавливаются в качестве параметра в функции SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="ac605-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="ac605-164">Функция SETATREF оценивает формулу, заключенную в SETATREFEVAL, и заменяет PinX и PinY результатами, а затем итоговая формула назначена ячейкам пользователей, на которые ссылается функция SETATREF — User.DeltaX и User.DeltaY.</span><span class="sxs-lookup"><span data-stu-id="ac605-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="ac605-165">Наконец, значения, возвращенные SETATREF (User.DeltaX или User.DeltaY), добавляются в расположение закрепления ParentShape для вычисления расположения контактов для фигуры.</span><span class="sxs-lookup"><span data-stu-id="ac605-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

