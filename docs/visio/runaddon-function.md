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
description: Выполняет надстройку или макрос в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432011"
---
# <a name="runaddon-function"></a><span data-ttu-id="ea54c-103">Функция RUNADDON</span><span class="sxs-lookup"><span data-stu-id="ea54c-103">RUNADDON Function</span></span>

<span data-ttu-id="ea54c-104">Выполняет надстройку или макрос в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="ea54c-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ea54c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea54c-105">Syntax</span></span>

<span data-ttu-id="ea54c-106">RUNADDON (" *строка* ")</span><span class="sxs-lookup"><span data-stu-id="ea54c-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ea54c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea54c-107">Parameters</span></span>

|<span data-ttu-id="ea54c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ea54c-108">**Name**</span></span>|<span data-ttu-id="ea54c-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ea54c-109">**Required/Optional**</span></span>|<span data-ttu-id="ea54c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ea54c-110">**Data Type**</span></span>|<span data-ttu-id="ea54c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ea54c-112">_string_</span><span class="sxs-lookup"><span data-stu-id="ea54c-112">_string_</span></span> <br/> |<span data-ttu-id="ea54c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ea54c-113">Required</span></span>  <br/> |<span data-ttu-id="ea54c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ea54c-114">**String**</span></span> <br/> | <span data-ttu-id="ea54c-115">Имя надстройки в коллекции **надстроек** или макросе в проекте VBA.</span><span class="sxs-lookup"><span data-stu-id="ea54c-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea54c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea54c-116">Remarks</span></span>

<span data-ttu-id="ea54c-117">Если проект документа, который содержит вызов функции RUNADDON (или другой проект, если он указан), не имеет именованной _строки_(процедура без аргументов), Microsoft Visio выполняет именованную _строку_надстройки.</span><span class="sxs-lookup"><span data-stu-id="ea54c-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="ea54c-118">Если не удается найти _строку_ с именованной надстройкой, Visio ничего не делает и не сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ea54c-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="ea54c-119">(Вы можете использовать свойство **трацефлагс** для отслеживания процедур и надстроек, которые Visio пытается запустить.)</span><span class="sxs-lookup"><span data-stu-id="ea54c-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="ea54c-120">При вызове процедуры в стандартном модуле рекомендуется помечать строку именем модуля, который содержит процедуру (например, *ModuleName., CNAME*), так как несколько модулей могут содержать процедуру с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="ea54c-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="ea54c-121">Чтобы вызвать процедуру в проекте, отличном от проекта документа, содержащего вызов функции RUNADDON, используйте синтаксис *projName. моднаме., CNAME* (необходимо явно задать ссылку на *ProjName* в проекте VBA).</span><span class="sxs-lookup"><span data-stu-id="ea54c-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="ea54c-122">Начиная с Visio 2002, функция RUNADDON не может выполнить строку, содержащую произвольный код VBA.</span><span class="sxs-lookup"><span data-stu-id="ea54c-122">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code.</span></span> <span data-ttu-id="ea54c-123">Код, который ранее был передан в функцию RUNADDON, можно переместить в процедуру в проекте VBA документа, вызываемой из функции RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="ea54c-123">Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="ea54c-124">Дополнительные сведения о запуске кода в Visio можно найти в статье [о параметрах безопасности и выполнении кода в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой ссылке на таблицу свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ea54c-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="ea54c-125">В более ранних версиях Visio Эта функция отображается как _RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="ea54c-125">In earlier versions of Visio, this function appears as _RUNADDON.</span></span> <span data-ttu-id="ea54c-126">Visio версии 4,0 и более поздних принимают любой из этих стилей.</span><span class="sxs-lookup"><span data-stu-id="ea54c-126">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ea54c-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea54c-127">Example 1</span></span>

<span data-ttu-id="ea54c-128">RUNADDON ("Calendar. exe")</span><span class="sxs-lookup"><span data-stu-id="ea54c-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="ea54c-129">Запускает надстройку с именем Calendar. exe.</span><span class="sxs-lookup"><span data-stu-id="ea54c-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ea54c-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea54c-130">Example 2</span></span>

<span data-ttu-id="ea54c-131">RUNADDON ("фигуры массива")</span><span class="sxs-lookup"><span data-stu-id="ea54c-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="ea54c-132">Запускает надстройку с (с расширением VSL), имя которой состоит из фигур массива.</span><span class="sxs-lookup"><span data-stu-id="ea54c-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ea54c-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ea54c-133">Example 3</span></span>

<span data-ttu-id="ea54c-134">RUNADDON ("ThisDocument. Репортстатистикс")</span><span class="sxs-lookup"><span data-stu-id="ea54c-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="ea54c-135">Вызывает макрос Репортстатистикс в модуле **ThisDocument** в проекте документа, содержащем вызов этой функции.</span><span class="sxs-lookup"><span data-stu-id="ea54c-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="ea54c-136">Чтобы вызвать макрос в модуле **ThisDocument** , необходимо перед строкой ввести "ThisDocument", как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ea54c-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="ea54c-137">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ea54c-137">Example 4</span></span>

<span data-ttu-id="ea54c-138">RUNADDON (" *ModuleName* . Репортстатистикс ")</span><span class="sxs-lookup"><span data-stu-id="ea54c-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="ea54c-139">Вызывает макрос Репортстатистикс в *ModuleName* в проекте документа, содержащем вызов этой функции.</span><span class="sxs-lookup"><span data-stu-id="ea54c-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

