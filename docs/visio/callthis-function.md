---
title: Функция CALLTHIS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Вызывает процедуру в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413817"
---
# <a name="callthis-function"></a><span data-ttu-id="01bee-103">Функция CALLTHIS</span><span class="sxs-lookup"><span data-stu-id="01bee-103">CALLTHIS Function</span></span>

<span data-ttu-id="01bee-104">Вызывает процедуру в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="01bee-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="01bee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01bee-105">Syntax</span></span>

<span data-ttu-id="01bee-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="01bee-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="01bee-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01bee-107">Parameters</span></span>

|<span data-ttu-id="01bee-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="01bee-108">**Name**</span></span>|<span data-ttu-id="01bee-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="01bee-109">**Required/Optional**</span></span>|<span data-ttu-id="01bee-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="01bee-110">**Data Type**</span></span>|<span data-ttu-id="01bee-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01bee-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="01bee-112">_procedure_</span><span class="sxs-lookup"><span data-stu-id="01bee-112">_procedure_</span></span> <br/> |<span data-ttu-id="01bee-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="01bee-113">Required</span></span>  <br/> |<span data-ttu-id="01bee-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="01bee-114">**String**</span></span> <br/> | <span data-ttu-id="01bee-115">Имя вызываемой процедуры.</span><span class="sxs-lookup"><span data-stu-id="01bee-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="01bee-116">_project_</span><span class="sxs-lookup"><span data-stu-id="01bee-116">_project_</span></span> <br/> |<span data-ttu-id="01bee-117">Необязательна</span><span class="sxs-lookup"><span data-stu-id="01bee-117">Optional</span></span>  <br/> |<span data-ttu-id="01bee-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="01bee-118">**String**</span></span> <br/> |<span data-ttu-id="01bee-119">Проект, содержащий процедуру.</span><span class="sxs-lookup"><span data-stu-id="01bee-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="01bee-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="01bee-120">_arg_</span></span> <br/> |<span data-ttu-id="01bee-121">Необязательна</span><span class="sxs-lookup"><span data-stu-id="01bee-121">Optional</span></span>  <br/> |<span data-ttu-id="01bee-122">**Число, строка, дата или валюта**</span><span class="sxs-lookup"><span data-stu-id="01bee-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="01bee-123">Передается в процедуру в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="01bee-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01bee-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="01bee-124">Remarks</span></span>

<span data-ttu-id="01bee-125">В проекте VBA процедура определяется следующим образом: </span><span class="sxs-lookup"><span data-stu-id="01bee-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="01bee-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span><span class="sxs-lookup"><span data-stu-id="01bee-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="01bee-127">где  *vsoShape*  — это ссылка на объект **Shape,** содержащий оцениваемую формулу CALLTHIS, и  _arg1_,  *arg2*  ... аргументы, указанные в этой формуле.</span><span class="sxs-lookup"><span data-stu-id="01bee-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="01bee-128">Обратите  *внимание, что vsoShape*  очень похож на аргумент "this", переданный процедуре-члену C++; следовательно, имя CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="01bee-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="01bee-129">По сути, ячейку, содержаную формулу, которая включает CALLTHIS, можно прочитать как "Вызовите эту процедуру и передайте ссылку на мою фигуру".</span><span class="sxs-lookup"><span data-stu-id="01bee-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="01bee-130">Если _указан_ проект, Microsoft Visio сканирует все открытые документы на тот, который содержит проект, и вызывает процедуру _в_ этом проекте. </span><span class="sxs-lookup"><span data-stu-id="01bee-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="01bee-131">Если _проект_ опущен или имеет null (""), Visio предполагает, что процедура находится в проекте VBA документа, который содержит формулу CALLTHIS, которая оценивается. </span><span class="sxs-lookup"><span data-stu-id="01bee-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="01bee-132">Числа  _в arg1_,  _arg2..._ передаются во внешних единицах.</span><span class="sxs-lookup"><span data-stu-id="01bee-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="01bee-133">Например, если передать значение ячейки Height из фигуры высотой 3 cm, передается 3.</span><span class="sxs-lookup"><span data-stu-id="01bee-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="01bee-134">Чтобы передать разные единицы с числом, используйте функцию FORMATEX или явно привязите единицы, добавив нулевую пару "число-единица", например 0 ft + Height.</span><span class="sxs-lookup"><span data-stu-id="01bee-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="01bee-135">Вторая запятая в функции CALLTHIS является необязательной.</span><span class="sxs-lookup"><span data-stu-id="01bee-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="01bee-136">Он соответствует количеству дополнительных параметров, добавленных в процедуру.</span><span class="sxs-lookup"><span data-stu-id="01bee-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="01bee-137">Если дополнительные параметры не используются, за исключением , не добавляйте вторую запятую; используйте  `(vsoShape as Visio.Shape)` CALLTHIS("",).</span><span class="sxs-lookup"><span data-stu-id="01bee-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="01bee-138">При добавлении двух дополнительных параметров, например, используйте CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="01bee-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="01bee-139">Функция CALLTHIS всегда оценивается как 0,  а вызов процедуры происходит во время простоя после завершения процесса пересчета.</span><span class="sxs-lookup"><span data-stu-id="01bee-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="01bee-140">_Процедура_ может возвращать значение, но Visio игнорирует его.</span><span class="sxs-lookup"><span data-stu-id="01bee-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="01bee-141">_Процедура_ возвращает значение, которое Visio может распознать, установив формулу или результат другой ячейки в документе, но не ячейку, которая вызвала процедуру, если вы не хотите перезаписать формулу CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="01bee-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="01bee-142">Функция CALLTHIS отличается от функции RUNADDON тем, что проекту документа не нужно ссылаться на другой проект для вызова этого проекта.</span><span class="sxs-lookup"><span data-stu-id="01bee-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="01bee-143">Код VBA, который вызывается, когда экземпляр Visio оценивает функцию CALLTHIS в формуле, не должен закрывать документ, содержащий ячейку, с помощью функции, так как ошибка приложения приводит к завершению Visio.</span><span class="sxs-lookup"><span data-stu-id="01bee-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="01bee-144">Если необходимо закрыть документ, содержащий ячейку, использующую функцию CALLTHIS, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="01bee-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="01bee-145">Закроем документ из кода, который не является VBA.</span><span class="sxs-lookup"><span data-stu-id="01bee-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="01bee-146">Закроем документ из проекта, который не закрывается.</span><span class="sxs-lookup"><span data-stu-id="01bee-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="01bee-147">Сообщения в окне публикации, чтобы закрыть окна в документе, а не закрывать документ.</span><span class="sxs-lookup"><span data-stu-id="01bee-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="01bee-148">Дополнительные сведения о запуске кода в Visio см. в справочнике по настройкам безопасности и запуску кода [в Visio.](about-security-settings-and-running-code-in-visio-shapesheet.md)</span><span class="sxs-lookup"><span data-stu-id="01bee-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="01bee-149">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01bee-149">Example 1</span></span>

<span data-ttu-id="01bee-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u","cm"))</span><span class="sxs-lookup"><span data-stu-id="01bee-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="01bee-151">Вызывает процедуру с именем p, расположенную в модуле, и передает значение Height в смах, например 7,62 cm.</span><span class="sxs-lookup"><span data-stu-id="01bee-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="01bee-152">Пример 2</span><span class="sxs-lookup"><span data-stu-id="01bee-152">Example 2</span></span>

<span data-ttu-id="01bee-153">CALLTHIS("q",0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="01bee-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="01bee-154">Вызывает процедуру q, расположенную в модуле, и передает высоту ячейки в смесях и ширину во внутренних единицах.</span><span class="sxs-lookup"><span data-stu-id="01bee-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="01bee-155">Пример 3</span><span class="sxs-lookup"><span data-stu-id="01bee-155">Example 3</span></span>

<span data-ttu-id="01bee-156">Используйте следующую процедуру в модуле класса *ThisDocument.*</span><span class="sxs-lookup"><span data-stu-id="01bee-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="01bee-157">Используйте любой из следующих синтаксис в ячейке EventDblClick фигуры с предыдущими процедурами.</span><span class="sxs-lookup"><span data-stu-id="01bee-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="01bee-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="01bee-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="01bee-159">CALLTHIS("ThisDocument.B","Click")</span><span class="sxs-lookup"><span data-stu-id="01bee-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="01bee-160">CALLTHIS("ThisDocument.C","Click", "OK.")</span><span class="sxs-lookup"><span data-stu-id="01bee-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

