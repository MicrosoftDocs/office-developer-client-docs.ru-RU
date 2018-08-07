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
description: Выполняет дополнительного компонента или макроса в Microsoft Visual Basic для приложений (VBA) проект.
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814720"
---
# <a name="runaddon-function"></a><span data-ttu-id="7bb70-103">Функция RUNADDON</span><span class="sxs-lookup"><span data-stu-id="7bb70-103">RUNADDON Function</span></span>

<span data-ttu-id="7bb70-104">Выполняет дополнительного компонента или макроса в Microsoft Visual Basic для приложений (VBA) проект.</span><span class="sxs-lookup"><span data-stu-id="7bb70-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7bb70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bb70-105">Syntax</span></span>

<span data-ttu-id="7bb70-106">RUNADDON (" *string* ")</span><span class="sxs-lookup"><span data-stu-id="7bb70-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7bb70-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bb70-107">Parameters</span></span>

|<span data-ttu-id="7bb70-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7bb70-108">**Name**</span></span>|<span data-ttu-id="7bb70-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7bb70-109">**Required/Optional**</span></span>|<span data-ttu-id="7bb70-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7bb70-110">**Data Type**</span></span>|<span data-ttu-id="7bb70-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7bb70-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7bb70-112">_string_</span><span class="sxs-lookup"><span data-stu-id="7bb70-112">_string_</span></span> <br/> |<span data-ttu-id="7bb70-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7bb70-113">Required</span></span>  <br/> |<span data-ttu-id="7bb70-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7bb70-114">**String**</span></span> <br/> | <span data-ttu-id="7bb70-115">Имя дополнительного компонента в коллекцию **надстроек** и макросов в VBA project.</span><span class="sxs-lookup"><span data-stu-id="7bb70-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bb70-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="7bb70-116">Remarks</span></span>

<span data-ttu-id="7bb70-117">Если проект документа, содержащего вызов функции RUNADDON (или другой проект, если она была вызвана) не имеет макрос (процедура без аргументов) с именем _string_, Microsoft Visio запускает дополнительный компонент, с именем _строки_.</span><span class="sxs-lookup"><span data-stu-id="7bb70-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="7bb70-118">Если нет дополнительный компонент с именем _строка_ не найден, Visio не выполняет никаких действий и сообщает об ошибке не.</span><span class="sxs-lookup"><span data-stu-id="7bb70-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="7bb70-119">(Свойство **TraceFlags** можно использовать для отслеживания процедуры и надстроек, Visio пытается выполнить.)</span><span class="sxs-lookup"><span data-stu-id="7bb70-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="7bb70-120">При вызове процедуры в стандартном модуле, рекомендуется префикс строки с помощью имени модуля, содержащий процедуры (например, *moduleName.procName*), так как более одного модуль может иметь процедуру с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="7bb70-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="7bb70-121">Вызов процедуры в проекте отличный от проекта документа, содержащего вызов функции RUNADDON, используйте синтаксис *projName.modName.procName* (необходимо явно задания ссылки на *имя_проекта* проекта VBA).</span><span class="sxs-lookup"><span data-stu-id="7bb70-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="7bb70-122">Приступая к работе с Visio 2002, функция RUNADDON не удается выполнить строка, содержащая произвольный код VBA.</span><span class="sxs-lookup"><span data-stu-id="7bb70-122">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code.</span></span> <span data-ttu-id="7bb70-123">Код, который ранее был передан в функцию RUNADDON можно перемещать в процедуру проекта VBA документа, который будет вызываться из функции RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="7bb70-123">Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="7bb70-124">Дополнительные сведения о запуске кода в Visio содержатся в разделе [о параметров безопасности и выполнить код в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) этот справочник по таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="7bb70-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="7bb70-125">В более ранних версиях Visio эта функция отображается в виде _RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="7bb70-125">In earlier versions of Visio, this function appears as _RUNADDON.</span></span> <span data-ttu-id="7bb70-126">Visio версии 4.0 и более поздних версий принимать любого из стилей.</span><span class="sxs-lookup"><span data-stu-id="7bb70-126">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7bb70-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7bb70-127">Example 1</span></span>

<span data-ttu-id="7bb70-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="7bb70-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="7bb70-129">Запускает дополнительного компонента, называется Calendar.exe.</span><span class="sxs-lookup"><span data-stu-id="7bb70-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7bb70-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7bb70-130">Example 2</span></span>

<span data-ttu-id="7bb70-131">RUNADDON ("массива фигуры")</span><span class="sxs-lookup"><span data-stu-id="7bb70-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="7bb70-132">Запускает надстройку ((VSL для) реализации), имя которого массива фигур.</span><span class="sxs-lookup"><span data-stu-id="7bb70-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7bb70-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7bb70-133">Example 3</span></span>

<span data-ttu-id="7bb70-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="7bb70-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="7bb70-135">Вызывает макрос ReportStatistics в модуле **ThisDocument** в проект документ, содержащий этот вызов функции.</span><span class="sxs-lookup"><span data-stu-id="7bb70-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="7bb70-136">Для вызова макроса в модуле **ThisDocument** , необходимо указать перед строка длиной «ThisDocument», как показано.</span><span class="sxs-lookup"><span data-stu-id="7bb70-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="7bb70-137">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7bb70-137">Example 4</span></span>

<span data-ttu-id="7bb70-138">RUNADDON (" *имя_модуля* . ReportStatistics»)</span><span class="sxs-lookup"><span data-stu-id="7bb70-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="7bb70-139">Вызывает макрос ReportStatistics *ИмяМодуля* в проект документ, содержащий этот вызов функции.</span><span class="sxs-lookup"><span data-stu-id="7bb70-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

