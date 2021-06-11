---
title: Функция RUNADDON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Выполняет надстройки или макрос в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432011"
---
# <a name="runaddon-function"></a><span data-ttu-id="de5c1-103">Функция RUNADDON</span><span class="sxs-lookup"><span data-stu-id="de5c1-103">RUNADDON Function</span></span>

<span data-ttu-id="de5c1-104">Выполняет надстройки или макрос в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="de5c1-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="de5c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de5c1-105">Syntax</span></span>

<span data-ttu-id="de5c1-106">RUNADDON (" *строка*  ")</span><span class="sxs-lookup"><span data-stu-id="de5c1-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="de5c1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de5c1-107">Parameters</span></span>

|<span data-ttu-id="de5c1-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="de5c1-108">**Name**</span></span>|<span data-ttu-id="de5c1-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="de5c1-109">**Required/Optional**</span></span>|<span data-ttu-id="de5c1-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="de5c1-110">**Data Type**</span></span>|<span data-ttu-id="de5c1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de5c1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="de5c1-112">_string_</span><span class="sxs-lookup"><span data-stu-id="de5c1-112">_string_</span></span> <br/> |<span data-ttu-id="de5c1-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="de5c1-113">Required</span></span>  <br/> |<span data-ttu-id="de5c1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="de5c1-114">**String**</span></span> <br/> | <span data-ttu-id="de5c1-115">Имя надстройки в коллекции **Addons** или макроса в проекте VBA.</span><span class="sxs-lookup"><span data-stu-id="de5c1-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de5c1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="de5c1-116">Remarks</span></span>

<span data-ttu-id="de5c1-117">Если проект документа, содержащий вызов функции RUNADDON (или другой проект, если он ссылается), не имеет макроса (процедура без аргументов) с именем строки, Microsoft Visio запускает строку с именем надстройки _._</span><span class="sxs-lookup"><span data-stu-id="de5c1-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="de5c1-118">Если строка с  именем надстройки не найдена, Visio ничего не делает и не сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="de5c1-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="de5c1-119">(Свойство **TraceFlags** можно использовать для мониторинга процедур и надстройок, Visio попыток запуска.)</span><span class="sxs-lookup"><span data-stu-id="de5c1-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="de5c1-120">При вызове процедуры в стандартном модуле рекомендуется префиксировать строку с именем модуля, содержатую процедуру (например,  *moduleName.procName),* так как несколько модулей могут иметь процедуру с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="de5c1-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="de5c1-121">Чтобы вызвать процедуру в проекте, не в проекте документа, который содержит вызов функции RUNADDON, используйте синтаксис  *projName.modName.procName*  (вы должны явно задать ссылку на  *projName*  в проекте VBA).</span><span class="sxs-lookup"><span data-stu-id="de5c1-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="de5c1-122">Начиная с Visio 2002 г. функция RUNADDON не может выполнять строку, содержащую произвольный код VBA.</span><span class="sxs-lookup"><span data-stu-id="de5c1-122">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code.</span></span> <span data-ttu-id="de5c1-123">Код, который ранее был передан функции RUNADDON, может быть перемещен в процедуру в проекте VBA документа, который вызван из функции RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="de5c1-123">Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="de5c1-124">Дополнительные сведения о запуске кода в Visio см. в Параметры и [running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой справке ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="de5c1-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="de5c1-125">В более ранних версиях Visio эта функция отображается как _RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="de5c1-125">In earlier versions of Visio, this function appears as _RUNADDON.</span></span> <span data-ttu-id="de5c1-126">Visio версии 4.0 и более поздние версии принимают любой стиль.</span><span class="sxs-lookup"><span data-stu-id="de5c1-126">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="de5c1-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de5c1-127">Example 1</span></span>

<span data-ttu-id="de5c1-128">RUNADDON ("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="de5c1-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="de5c1-129">Запускает надстройка под названием Calendar.exe.</span><span class="sxs-lookup"><span data-stu-id="de5c1-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="de5c1-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="de5c1-130">Example 2</span></span>

<span data-ttu-id="de5c1-131">RUNADDON ("Формы массива")</span><span class="sxs-lookup"><span data-stu-id="de5c1-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="de5c1-132">Запускает надстройка (реализованная vsL) с именем Array Shapes.</span><span class="sxs-lookup"><span data-stu-id="de5c1-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="de5c1-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="de5c1-133">Example 3</span></span>

<span data-ttu-id="de5c1-134">RUNADDON ("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="de5c1-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="de5c1-135">Вызывает макрос ReportStatistics в модуле **ThisDocument** в проекте документа, содержащего этот вызов функции.</span><span class="sxs-lookup"><span data-stu-id="de5c1-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="de5c1-136">Чтобы вызвать макрос в модуле **ThisDocument,** необходимо предисловие строки с "ThisDocument", как показано.</span><span class="sxs-lookup"><span data-stu-id="de5c1-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="de5c1-137">Пример 4</span><span class="sxs-lookup"><span data-stu-id="de5c1-137">Example 4</span></span>

<span data-ttu-id="de5c1-138">RUNADDON(" *ModuleName*  . ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="de5c1-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="de5c1-139">Вызывает макрос ReportStatistics в  *ModuleName*  в проекте документа, который содержит этот вызов функции.</span><span class="sxs-lookup"><span data-stu-id="de5c1-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

