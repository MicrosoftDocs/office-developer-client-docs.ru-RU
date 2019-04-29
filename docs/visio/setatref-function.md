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
description: Перенаправляет обновленные значения, полученные в результате действий в пользовательском интерфейсе или автоматизации, в другую ячейку.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416806"
---
# <a name="setatref-function"></a><span data-ttu-id="782d4-103">Функция SETATREF</span><span class="sxs-lookup"><span data-stu-id="782d4-103">SETATREF Function</span></span>

<span data-ttu-id="782d4-104">Перенаправляет обновленные значения, полученные в результате действий в пользовательском интерфейсе или автоматизации, в другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="782d4-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="782d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="782d4-105">Syntax</span></span>

<span data-ttu-id="782d4-106">SETATREF (\* \* *Reference* \* \* [, \* \* *Set_Expression* \* \* [, \* \* *игноре_евал* \* \*]])</span><span class="sxs-lookup"><span data-stu-id="782d4-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="782d4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="782d4-107">Parameters</span></span>

|<span data-ttu-id="782d4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="782d4-108">**Name**</span></span>|<span data-ttu-id="782d4-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="782d4-109">**Required/Optional**</span></span>|<span data-ttu-id="782d4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="782d4-110">**Data Type**</span></span>|<span data-ttu-id="782d4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="782d4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="782d4-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="782d4-112">_reference_</span></span> <br/> |<span data-ttu-id="782d4-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="782d4-113">Required</span></span>  <br/> |<span data-ttu-id="782d4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="782d4-114">**String**</span></span> <br/> |<span data-ttu-id="782d4-115">Ссылка на ячейку, в которую перенаправлены обновления.</span><span class="sxs-lookup"><span data-stu-id="782d4-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="782d4-116">_Set_Expression_</span><span class="sxs-lookup"><span data-stu-id="782d4-116">_set_expression_</span></span> <br/> |<span data-ttu-id="782d4-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="782d4-117">Optional</span></span>  <br/> |<span data-ttu-id="782d4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="782d4-118">**String**</span></span> <br/> |<span data-ttu-id="782d4-119">Выражение, которое присваивается _ссылке_.</span><span class="sxs-lookup"><span data-stu-id="782d4-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="782d4-120">_игноре_евал_</span><span class="sxs-lookup"><span data-stu-id="782d4-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="782d4-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="782d4-121">Optional</span></span>  <br/> |<span data-ttu-id="782d4-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="782d4-122">**Boolean**</span></span> <br/> |<span data-ttu-id="782d4-123">Если задано значение TRUE, функция SETATREF возвращает значение (0) ноль; Если задано значение FALSE (значение по умолчанию), функция SETATREF оценивается как _ссылка_.</span><span class="sxs-lookup"><span data-stu-id="782d4-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="782d4-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="782d4-124">Remarks</span></span>

<span data-ttu-id="782d4-125">Если пользовательское действие в окне документа или метод автоматизации приводит к тому, что Microsoft Visio обновляет ячейку, содержащую формулу SETATREF, это значение перенаправляется в ячейку, на которую ссылается формула SETATREF ( _ссылка_).</span><span class="sxs-lookup"><span data-stu-id="782d4-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="782d4-126">Формула в ячейке, содержащей функцию SETATREF, остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="782d4-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="782d4-127">Если аргумент _Set_Expression_ опущен, значение, заданное в пользовательском интерфейсе или с помощью автоматизации, назначается указанной ячейке; в противном случае содержимое объекта _Set_Expression_ назначается указанной ячейке.</span><span class="sxs-lookup"><span data-stu-id="782d4-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="782d4-128">Это позволяет изменить или преобразовать новое значение перед его присвоением указанной ячейке.</span><span class="sxs-lookup"><span data-stu-id="782d4-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="782d4-129">Функция SETATREF имеет две связанные функции:</span><span class="sxs-lookup"><span data-stu-id="782d4-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="782d4-130">Функция SETATREFEXPR, которую можно использовать для представления нового значения в списке _Set_Expression_.</span><span class="sxs-lookup"><span data-stu-id="782d4-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="782d4-131">Например, _SET_EXPRESSION_ SETATREFEXPR ()-2 в.</span><span class="sxs-lookup"><span data-stu-id="782d4-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="782d4-132">может использоваться для вычитания 2 сантиметров из результатов SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="782d4-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="782d4-133">Функция SETATREFEVAL, которую можно использовать, чтобы указать, что часть аргумента _Set_Expression_ должна быть оценена и заменена на результат.</span><span class="sxs-lookup"><span data-stu-id="782d4-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="782d4-134">Функция SETATREF предназначена для использования в ячейках, которые можно изменить с помощью действий пользователя в окне документа.</span><span class="sxs-lookup"><span data-stu-id="782d4-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="782d4-135">Поддерживаются следующие ячейки:</span><span class="sxs-lookup"><span data-stu-id="782d4-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="782d4-136">Раздел Шапетрансформ — ширина, высота, угол, PinX и PinY ячеек</span><span class="sxs-lookup"><span data-stu-id="782d4-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="782d4-137">Раздел "преобразование текста" — TxtWidth, TxtHeight, TxtAngle, TxtPinX и TxtPinY ячейки</span><span class="sxs-lookup"><span data-stu-id="782d4-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="782d4-138">раздел "1-D Endpoints" — BeginX, Begin, EndX и Енди Cells</span><span class="sxs-lookup"><span data-stu-id="782d4-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="782d4-139">Раздел "элементы управления" — Controls. X и Controls. Y.</span><span class="sxs-lookup"><span data-stu-id="782d4-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="782d4-140">Раздел "Данные фигуры"</span><span class="sxs-lookup"><span data-stu-id="782d4-140">Shape Data section</span></span>
    
<span data-ttu-id="782d4-141">Так как SETATREF изменяет расположение, в котором изменяются значения ячеек, оно влияет на срабатывание события.</span><span class="sxs-lookup"><span data-stu-id="782d4-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="782d4-142">Если ячейка содержит SETATREF, события **формулачанжед** и **CellChanged** срабатывают для ячейки, на которую ссылается SETATREF, а не ячейки, содержащие SETATREF.</span><span class="sxs-lookup"><span data-stu-id="782d4-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="782d4-143">Если ячейка, содержащая SETATREF, также содержит SETATREFEXPR, то событие **формулачанжед** также срабатывает для ячейки, содержащей SETATREF, так как параметр функции изменился.</span><span class="sxs-lookup"><span data-stu-id="782d4-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="782d4-144">Кроме того, обратите внимание на следующие важные моменты, касающиеся функции SETATREF:</span><span class="sxs-lookup"><span data-stu-id="782d4-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="782d4-145">Функции SETATREF могут создавать цепочки до 10 ссылок на другие функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="782d4-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="782d4-146">Ячейки могут содержать другие выражения в дополнение к функции SETATREF, в том числе несколько вхождений SETATREF в одной ячейке.</span><span class="sxs-lookup"><span data-stu-id="782d4-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="782d4-147">Если фигуры привязываются, Visio обращается к цепочке ссылок SETATREF в пределах одного листа и размещает формулы приклеить в ячейке, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="782d4-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="782d4-148">Автоматизация распознает функцию SETATREF и соответствует цепочке ячеек, на которые указывают ссылки.</span><span class="sxs-lookup"><span data-stu-id="782d4-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="782d4-149">Как и в случае с ЗАЩИТой, SETATREF не защищает ячейки от изменений, выполненных с помощью функции SETF в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="782d4-150">Example1</span><span class="sxs-lookup"><span data-stu-id="782d4-150">Example1</span></span>

<span data-ttu-id="782d4-151">Предположим, что фигура имеет настраиваемое свойство Width, а ячейка Width в разделе Преобразование фигуры содержит следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="782d4-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="782d4-152">= SETATREF (prop. Width)</span><span class="sxs-lookup"><span data-stu-id="782d4-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="782d4-153">Если пользователю необходимо изменить ширину фигуры в ПОЛЬЗОВАТЕЛЬСКОМ ИНТЕРФЕЙСе, то новое значение будет назначено ячейке prop. Width, а не ячейке Width в разделе Шапетрансформ. Формула в ячейке Width остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="782d4-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="782d4-154">Ширину фигуры также можно задать с помощью данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="782d4-155">Example2</span><span class="sxs-lookup"><span data-stu-id="782d4-155">Example2</span></span>

<span data-ttu-id="782d4-156">В решениях Visio часто используются фигуры с иерархической связью, требующие перемещения дочерних фигур при перемещении родительской фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-156">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved.</span></span> <span data-ttu-id="782d4-157">Ниже приведен пример того, как можно управлять этой связью с помощью функции SETATREF в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-157">Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="782d4-158">Следующие формулы включены в раздел "Преобразование фигуры" дочерней фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-158">The following formulas are contained in the Shape Transform section of the child shape.</span></span> <span data-ttu-id="782d4-159">Кроме того, мы определяем пользовательские ячейки с именем user. Делтакс и User. Delta, которые отслеживают размер смещения из Парентшапе.</span><span class="sxs-lookup"><span data-stu-id="782d4-159">Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape.</span></span> <span data-ttu-id="782d4-160">Это позволяет перемещать дочернюю фигуру при перемещении родительской фигуры, а также сохранять иерархические отношения при перемещении дочерней фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-160">This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="782d4-161">PinX = SETATREF (User. Делтакс, SETATREFEVAL (SETATREFEXPR ()-Парентшапе! PinX)) + Парентшапе! PinX</span><span class="sxs-lookup"><span data-stu-id="782d4-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="782d4-162">PinY = SETATREF (User. Deltaing, SETATREFEVAL (SETATREFEXPR ()-Парентшапе! PinY)) + Парентшапе! PinY</span><span class="sxs-lookup"><span data-stu-id="782d4-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="782d4-163">Когда дочерняя фигура перемещается с помощью ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, новые значения PinX и PinY задаются в качестве параметра в функции SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="782d4-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="782d4-164">Функция SETATREF оценивает формулу, заключенную в SETATREFEVAL, и заменяет PinX и PinY на результаты, а затем результирующую формулу присваиваются ячейкам пользователей, на которые ссылается функция SETATREF — User. Делтакс и User. Delta.</span><span class="sxs-lookup"><span data-stu-id="782d4-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="782d4-165">Наконец, значения, возвращаемые методом SETATREF (User. Делтакс или User. Delta), добавляются в расположение ПИН-кода Парентшапе для вычисления расположения ПИН-кода дочерней фигуры.</span><span class="sxs-lookup"><span data-stu-id="782d4-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

