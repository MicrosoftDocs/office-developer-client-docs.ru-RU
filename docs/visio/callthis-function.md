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
# <a name="callthis-function"></a><span data-ttu-id="0a040-103">Функция CALLTHIS</span><span class="sxs-lookup"><span data-stu-id="0a040-103">CALLTHIS Function</span></span>

<span data-ttu-id="0a040-104">Вызывает процедуру в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="0a040-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0a040-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a040-105">Syntax</span></span>

<span data-ttu-id="0a040-106">CALLTHIS(" \*\* *процедура* \*\* ",[" \*\*\*\* project \*\* "],[\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="0a040-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a040-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a040-107">Parameters</span></span>

|<span data-ttu-id="0a040-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0a040-108">**Name**</span></span>|<span data-ttu-id="0a040-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0a040-109">**Required/Optional**</span></span>|<span data-ttu-id="0a040-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0a040-110">**Data Type**</span></span>|<span data-ttu-id="0a040-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a040-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a040-112">_procedure_</span><span class="sxs-lookup"><span data-stu-id="0a040-112">_procedure_</span></span> <br/> |<span data-ttu-id="0a040-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a040-113">Required</span></span>  <br/> |<span data-ttu-id="0a040-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0a040-114">**String**</span></span> <br/> | <span data-ttu-id="0a040-115">Имя вызываемой процедуры.</span><span class="sxs-lookup"><span data-stu-id="0a040-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="0a040-116">_проект_</span><span class="sxs-lookup"><span data-stu-id="0a040-116">_project_</span></span> <br/> |<span data-ttu-id="0a040-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0a040-117">Optional</span></span>  <br/> |<span data-ttu-id="0a040-118">**String**</span><span class="sxs-lookup"><span data-stu-id="0a040-118">**String**</span></span> <br/> |<span data-ttu-id="0a040-119">Проект, содержащий процедуру.</span><span class="sxs-lookup"><span data-stu-id="0a040-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="0a040-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="0a040-120">_arg_</span></span> <br/> |<span data-ttu-id="0a040-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0a040-121">Optional</span></span>  <br/> |<span data-ttu-id="0a040-122">**Число, строка, дата или валюта**</span><span class="sxs-lookup"><span data-stu-id="0a040-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="0a040-123">Передается в качестве параметров процедуры.</span><span class="sxs-lookup"><span data-stu-id="0a040-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a040-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a040-124">Remarks</span></span>

<span data-ttu-id="0a040-125">В проекте VBA процедура  *определяется*  следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a040-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="0a040-126">процедуры *(vsoShape* As Visio. Shape [arg1 As type, arg2 As type...])</span><span class="sxs-lookup"><span data-stu-id="0a040-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="0a040-127">где  *vsoShape*  является ссылкой на объект **Shape,** содержащий оцениваемую формулу CALLTHIS,  _и arg1_,  *arg2*  ... аргументы, указанные в этой формуле.</span><span class="sxs-lookup"><span data-stu-id="0a040-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="0a040-128">Обратите  *внимание, что vsoShape*  очень похож на аргумент "этот", переданный процедуре участника C++; отсюда и имя "CALLTHIS".</span><span class="sxs-lookup"><span data-stu-id="0a040-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="0a040-129">По сути, ячейку с формулой CALLTHIS можно прочитать так: "Вызывай эту процедуру и передай ссылку на мою фигуру".</span><span class="sxs-lookup"><span data-stu-id="0a040-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="0a040-130">Если _задан_ проект, корпорация Майкрософт Visio все открытые документы  для одного из них, содержащего проект, и процедуру вызовов _в_ этом проекте.</span><span class="sxs-lookup"><span data-stu-id="0a040-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="0a040-131">Если _проект_ опущен или null (""), Visio  предполагает, что процедура находится в проекте VBA документа, который содержит формулу CALLTHIS, которая оценивается.</span><span class="sxs-lookup"><span data-stu-id="0a040-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="0a040-132">Номера  _в arg1,_  _arg2..._ передаются в внешних единицах.</span><span class="sxs-lookup"><span data-stu-id="0a040-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="0a040-133">Например, если вы передаете значение ячейки Height из фигуры высотой 3 см, передается 3.</span><span class="sxs-lookup"><span data-stu-id="0a040-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="0a040-134">Чтобы передать различные единицы с номером, используйте функцию FORMATEX или явно принудительные единицы, добавив null number-unit pair, например, 0 ft + Height.</span><span class="sxs-lookup"><span data-stu-id="0a040-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="0a040-135">Вторая запятая в функции CALLTHIS необязательна.</span><span class="sxs-lookup"><span data-stu-id="0a040-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="0a040-136">Это соответствует количеству дополнительных параметров, добавленных в процедуру.</span><span class="sxs-lookup"><span data-stu-id="0a040-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="0a040-137">Если вы не используете какие-либо дополнительные параметры, за исключением, не добавляйте вторую запятую;  `(vsoShape as Visio.Shape)` используйте CALLTHIS ("",).</span><span class="sxs-lookup"><span data-stu-id="0a040-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="0a040-138">Если вы добавляете два дополнительных параметра, например, используйте CALLTHIS (",,,).</span><span class="sxs-lookup"><span data-stu-id="0a040-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="0a040-139">Функция CALLTHIS всегда оценивается до 0,  а вызов на процедуру возникает во время простоя после завершения процесса пересчета.</span><span class="sxs-lookup"><span data-stu-id="0a040-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="0a040-140">_Процедура_ может вернуть значение, но Visio игнорирует его.</span><span class="sxs-lookup"><span data-stu-id="0a040-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="0a040-141">_Процедура_ возвращает значение Visio которое можно распознать, установив формулу или результат другой ячейки в документе, но не ячейку, вызываемую процедурой, если вы не хотите перезаписать формулу CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="0a040-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="0a040-142">Функция CALLTHIS отличается от функции RUNADDON тем, что проекту документа не нужно ссылаться на другой проект для вызова в этот проект.</span><span class="sxs-lookup"><span data-stu-id="0a040-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="0a040-143">Код VBA, который вызывается, когда экземпляр Visio оценивает функцию CALLTHIS в формуле, не должен закрывать документ, содержащий ячейку с помощью функции, так как результаты ошибки приложения и Visio завершаются.</span><span class="sxs-lookup"><span data-stu-id="0a040-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="0a040-144">Если необходимо закрыть документ, содержащий ячейку, использующую функцию CALLTHIS, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="0a040-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="0a040-145">Закрой документ из кода, который не является VBA.</span><span class="sxs-lookup"><span data-stu-id="0a040-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="0a040-146">Закрой документ из проекта, кроме закрываемого.</span><span class="sxs-lookup"><span data-stu-id="0a040-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="0a040-147">Вывешить сообщения о окне, чтобы закрыть окна в документе, а не закрыть документ.</span><span class="sxs-lookup"><span data-stu-id="0a040-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="0a040-148">Дополнительные сведения о запуске кода в Visio см. в Параметры и [running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой справке ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="0a040-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0a040-149">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a040-149">Example 1</span></span>

<span data-ttu-id="0a040-150">CALLTHIS ("p", FORMATEX(Height,#.00 u", "cm"))</span><span class="sxs-lookup"><span data-stu-id="0a040-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="0a040-151">Вызывает процедуру с именем p, расположенную в модуле, и передает значение Высоты в сантиметрах, например 7,62 см.</span><span class="sxs-lookup"><span data-stu-id="0a040-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0a040-152">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0a040-152">Example 2</span></span>

<span data-ttu-id="0a040-153">CALLTHIS ("q", 0 см+высота, ширина)</span><span class="sxs-lookup"><span data-stu-id="0a040-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="0a040-154">Вызывает процедуру q, расположенную в модуле, и передает высоту ячейки в сантиметры и ширину во внутренних единицах.</span><span class="sxs-lookup"><span data-stu-id="0a040-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0a040-155">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0a040-155">Example 3</span></span>

<span data-ttu-id="0a040-156">Используйте следующую процедуру в модуле *класса ThisDocument.*</span><span class="sxs-lookup"><span data-stu-id="0a040-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="0a040-157">Используйте любой из следующих синтаксис в ячейке EventDblClick фигуры с предыдущими процедурами.</span><span class="sxs-lookup"><span data-stu-id="0a040-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="0a040-158">CALLTHIS ("ThisDocument.A",))</span><span class="sxs-lookup"><span data-stu-id="0a040-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="0a040-159">CALLTHIS ("ThisDocument.B", "Click")</span><span class="sxs-lookup"><span data-stu-id="0a040-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="0a040-160">CALLTHIS ("ThisDocument.C", "Click", "OK.")</span><span class="sxs-lookup"><span data-stu-id="0a040-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

