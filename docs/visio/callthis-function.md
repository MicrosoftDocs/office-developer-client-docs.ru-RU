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
description: Вызывает процедуру в Microsoft Visual Basic для приложений (VBA) проект.
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813317"
---
# <a name="callthis-function"></a><span data-ttu-id="4e6fb-103">Функция CALLTHIS</span><span class="sxs-lookup"><span data-stu-id="4e6fb-103">CALLTHIS Function</span></span>

<span data-ttu-id="4e6fb-104">Вызывает процедуру в Microsoft Visual Basic для приложений (VBA) проект.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4e6fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e6fb-105">Syntax</span></span>

<span data-ttu-id="4e6fb-106">CALLTHIS ("** *процедуры* **", ["** *project* **"], [** *arg1* **, ** *arg2* **,...])</span><span class="sxs-lookup"><span data-stu-id="4e6fb-106">CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e6fb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e6fb-107">Parameters</span></span>

|<span data-ttu-id="4e6fb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-108">**Name**</span></span>|<span data-ttu-id="4e6fb-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-109">**Required/Optional**</span></span>|<span data-ttu-id="4e6fb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-110">**Data Type**</span></span>|<span data-ttu-id="4e6fb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e6fb-112">_процедура_</span><span class="sxs-lookup"><span data-stu-id="4e6fb-112">_procedure_</span></span> <br/> |<span data-ttu-id="4e6fb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4e6fb-113">Required</span></span>  <br/> |<span data-ttu-id="4e6fb-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-114">**String**</span></span> <br/> | <span data-ttu-id="4e6fb-115">Имя процедуры для вызова.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="4e6fb-116">_проекта_</span><span class="sxs-lookup"><span data-stu-id="4e6fb-116">_project_</span></span> <br/> |<span data-ttu-id="4e6fb-117">Optional</span><span class="sxs-lookup"><span data-stu-id="4e6fb-117">Optional</span></span>  <br/> |<span data-ttu-id="4e6fb-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-118">**String**</span></span> <br/> |<span data-ttu-id="4e6fb-119">Проект, содержащий процедуру.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="4e6fb-120">_Аргумент_</span><span class="sxs-lookup"><span data-stu-id="4e6fb-120">_arg_</span></span> <br/> |<span data-ttu-id="4e6fb-121">Optional</span><span class="sxs-lookup"><span data-stu-id="4e6fb-121">Optional</span></span>  <br/> |<span data-ttu-id="4e6fb-122">**Номер, строка, дата или валюта**</span><span class="sxs-lookup"><span data-stu-id="4e6fb-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="4e6fb-123">Передаются как параметры к процедуре.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e6fb-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e6fb-124">Remarks</span></span>

<span data-ttu-id="4e6fb-125">В проекте VBA *процедуры* определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e6fb-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="4e6fb-126">процедура (*vsoShape* как Visio.Shape [arg1 как тип arg2 как type...])</span><span class="sxs-lookup"><span data-stu-id="4e6fb-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="4e6fb-127">где *vsoShape* является ссылкой на объекта **Shape** , содержащий формулу CALLTHIS вычислением и _arg1_ *arg2* ... являются аргументов, указанных в формулу.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="4e6fb-128">Обратите внимание, что этот *vsoShape* очень похож «этот» аргумент, передаваемые в процедуру член C++; Поэтому имя «CALLTHIS».</span><span class="sxs-lookup"><span data-stu-id="4e6fb-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="4e6fb-129">В результате могут читать ячейка, которая содержит формулу, которая включает в себя CALLTHIS как «Вызвать эту процедуру и передать его ссылку на Мои фигуры».</span><span class="sxs-lookup"><span data-stu-id="4e6fb-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="4e6fb-130">Если _проект_ указан, Microsoft Visio сканирование всех открытых документов для одного содержащего _проекта_ и вызывает _процедуру_ в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="4e6fb-131">Если _проект_ является неправильных или значение null ("»), Visio предполагает _процедуры_ в проекте VBA документ, который содержит формулу CALLTHIS, которое было определено.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="4e6fb-132">Номера в _arg1_ _arg2..._ передаются в внешних единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="4e6fb-133">Например если передать значение высоту ячеек из формы, который является 3 см передается 3.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="4e6fb-134">Для передачи единиц с числом, используйте функцию FORMATEX или явно привести единиц измерения, добавив значение null, номер единицы пары, например 0 ft + высоту.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="4e6fb-135">Вторая запятая в функции CALLTHIS не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="4e6fb-136">Оно соответствует число дополнительных параметров, добавляемых в процедуру.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="4e6fb-137">Если вы не используете дополнительных параметров, за исключением `(vsoShape as Visio.Shape)` , не добавляйте второй запятой; с помощью CALLTHIS("",).</span><span class="sxs-lookup"><span data-stu-id="4e6fb-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="4e6fb-138">Если вы добавляете два дополнительных параметра, например, используйте CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="4e6fb-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="4e6fb-139">Функция CALLTHIS всегда имеет значение 0, и вызов _процедуры_ происходит во время простоя, после завершения процесса пересчета.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="4e6fb-140">_Процедура_ может возвратить значение, но он игнорирует Visio.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="4e6fb-141">_Процедура_ возвращает значение, которое может распознать Visio, задав формулу или результат другую ячейку в документе, но не ячейки, вызвавшей _процедуру_, если не перезаписать формула CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="4e6fb-142">Функция CALLTHIS отличается от функции RUNADDON, что проект документа не требуется ссылаться на другой проект для вызова этого проекта.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="4e6fb-143">Код VBA, которая вызывается при экземпляр Visio оценивает функции CALLTHIS в формуле не следует закрыть документ, содержащий ячейки, с помощью функции, так как возникает ошибка приложения и завершает Visio.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="4e6fb-144">Если необходимо закрыть документ, содержащий ячейки, которая использует функцию CALLTHIS, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="4e6fb-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="4e6fb-145">Закройте документ, из кода, который не является VBA.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="4e6fb-146">Закройте документ из проекта не закрывается.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="4e6fb-147">Публиковать сообщения окна для закрытия окна в документе, а не закрытия документа.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="4e6fb-148">Дополнительные сведения о запуске кода в Visio содержатся в разделе [о параметров безопасности и выполнить код в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) этот справочник по таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4e6fb-149">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e6fb-149">Example 1</span></span>

<span data-ttu-id="4e6fb-150">CALLTHIS («p»,, FORMATEX (высота, "#.00 u",, "cm"))</span><span class="sxs-lookup"><span data-stu-id="4e6fb-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="4e6fb-151">Вызывает процедуру с именем p, расположенной в модуле и передает значение высоты в см, такие как 7,62 см.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4e6fb-152">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4e6fb-152">Example 2</span></span>

<span data-ttu-id="4e6fb-153">CALLTHIS ("q",, 0 cm + высота, ширина)</span><span class="sxs-lookup"><span data-stu-id="4e6fb-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="4e6fb-154">Вызывает процедуру с именем q, расположенной в модуле и передает высоту ячеек в см и ширину в внутренних единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4e6fb-155">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4e6fb-155">Example 3</span></span>

<span data-ttu-id="4e6fb-156">В модуле класса *ThisDocument* , используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="4e6fb-157">В ячейке EventDblClick фигуры с помощью приведенных выше процедурах используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="4e6fb-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="4e6fb-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="4e6fb-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="4e6fb-159">CALLTHIS("ThisDocument.B",,"Click")</span><span class="sxs-lookup"><span data-stu-id="4e6fb-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="4e6fb-160">CALLTHIS ("ThisDocument.C",,"Click", "ОК".)</span><span class="sxs-lookup"><span data-stu-id="4e6fb-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

