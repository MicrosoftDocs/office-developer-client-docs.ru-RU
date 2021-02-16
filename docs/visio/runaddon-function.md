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
# <a name="runaddon-function"></a><span data-ttu-id="741ec-103">Функция RUNADDON</span><span class="sxs-lookup"><span data-stu-id="741ec-103">RUNADDON Function</span></span>

<span data-ttu-id="741ec-104">Выполняет надстройки или макрос в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="741ec-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="741ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="741ec-105">Syntax</span></span>

<span data-ttu-id="741ec-106">RUNADDON(" *string*  ")</span><span class="sxs-lookup"><span data-stu-id="741ec-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="741ec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="741ec-107">Parameters</span></span>

|<span data-ttu-id="741ec-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="741ec-108">**Name**</span></span>|<span data-ttu-id="741ec-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="741ec-109">**Required/Optional**</span></span>|<span data-ttu-id="741ec-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="741ec-110">**Data Type**</span></span>|<span data-ttu-id="741ec-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="741ec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="741ec-112">_string_</span><span class="sxs-lookup"><span data-stu-id="741ec-112">_string_</span></span> <br/> |<span data-ttu-id="741ec-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="741ec-113">Required</span></span>  <br/> |<span data-ttu-id="741ec-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="741ec-114">**String**</span></span> <br/> | <span data-ttu-id="741ec-115">Имя надстройки в коллекции **Addons** или макроса в проекте VBA.</span><span class="sxs-lookup"><span data-stu-id="741ec-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="741ec-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="741ec-116">Remarks</span></span>

<span data-ttu-id="741ec-117">Если проект документа, содержащий вызов функции RUNADDON (или другой проект, если на него есть ссылка), не содержит макрос (процедура без аргументов) с именем _строки,_ Microsoft Visio запускает именоваемую строку надстройки. </span><span class="sxs-lookup"><span data-stu-id="741ec-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="741ec-118">Если именоваемая строка надстройки не найдена, Visio ничего не делает и не сообщает об ошибке. </span><span class="sxs-lookup"><span data-stu-id="741ec-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="741ec-119">(С помощью свойства **TraceFlags** можно отслеживать процедуры и надстройки, которые пытается запустить Visio.)</span><span class="sxs-lookup"><span data-stu-id="741ec-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="741ec-120">При вызове процедуры в стандартном модуле рекомендуется префиксировать строку с именем модуля, содержаменем модуля, содержаменем процедуры (например,  *moduleName.procName),* так как несколько модулей могут иметь процедуру с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="741ec-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="741ec-121">Чтобы вызвать процедуру в проекте, который не является проектом документа, который содержит вызов функции RUNADDON, используйте синтаксис  *projName.modName.procName*  (необходимо явно установить ссылку на  *projName в*  проекте VBA).</span><span class="sxs-lookup"><span data-stu-id="741ec-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="741ec-122">Начиная с Visio 2002 функция RUNADDON не может выполнять строку, содержащую произвольный код VBA.</span><span class="sxs-lookup"><span data-stu-id="741ec-122">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code.</span></span> <span data-ttu-id="741ec-123">Код, который ранее был передан функции RUNADDON, может быть перемещен в процедуру в проекте VBA документа, который вызван из функции RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="741ec-123">Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="741ec-124">Дополнительные сведения о запуске кода в Visio см. в справочнике по настройкам безопасности и запуску кода [в Visio.](about-security-settings-and-running-code-in-visio-shapesheet.md)</span><span class="sxs-lookup"><span data-stu-id="741ec-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="741ec-125">В более ранних версиях Visio эта функция отображается как _RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="741ec-125">In earlier versions of Visio, this function appears as _RUNADDON.</span></span> <span data-ttu-id="741ec-126">Visio версий 4.0 и более поздних версий принимают любой стиль.</span><span class="sxs-lookup"><span data-stu-id="741ec-126">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="741ec-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="741ec-127">Example 1</span></span>

<span data-ttu-id="741ec-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="741ec-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="741ec-129">Запускает надстройки с названием Calendar.exe.</span><span class="sxs-lookup"><span data-stu-id="741ec-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="741ec-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="741ec-130">Example 2</span></span>

<span data-ttu-id="741ec-131">RUNADDON("Фигуры массива")</span><span class="sxs-lookup"><span data-stu-id="741ec-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="741ec-132">Запускает надстройки с именем Array Shapes (с реализацией VSL).</span><span class="sxs-lookup"><span data-stu-id="741ec-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="741ec-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="741ec-133">Example 3</span></span>

<span data-ttu-id="741ec-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="741ec-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="741ec-135">Вызывает макрос ReportStatistics в модуле **ThisDocument** проекта документа, содержащего этот вызов функции.</span><span class="sxs-lookup"><span data-stu-id="741ec-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="741ec-136">Чтобы вызвать макрос в модуле **ThisDocument,** необходимо использовать перед строкой "ThisDocument", как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="741ec-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="741ec-137">Пример 4</span><span class="sxs-lookup"><span data-stu-id="741ec-137">Example 4</span></span>

<span data-ttu-id="741ec-138">RUNADDON(" *ModuleName*  . ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="741ec-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="741ec-139">Вызывает макрос ReportStatistics в  *ModuleName*  в проекте документа, который содержит этот вызов функции.</span><span class="sxs-lookup"><span data-stu-id="741ec-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

