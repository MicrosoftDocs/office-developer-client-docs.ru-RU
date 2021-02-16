---
title: Функция RUNMACRO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Вызывает макрос в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428090"
---
# <a name="runmacro-function"></a><span data-ttu-id="ed2b7-103">Функция RUNMACRO</span><span class="sxs-lookup"><span data-stu-id="ed2b7-103">RUNMACRO Function</span></span>

<span data-ttu-id="ed2b7-104">Вызывает макрос в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="ed2b7-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed2b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed2b7-105">Syntax</span></span>

<span data-ttu-id="ed2b7-106">RUNMACRO (\*\* *macroname* \*\* [, \*\* *projname_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="ed2b7-106">RUNMACRO (\*\* *macroname* \*\* [, \*\* *projname_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed2b7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed2b7-107">Parameters</span></span>

|<span data-ttu-id="ed2b7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ed2b7-108">**Name**</span></span>|<span data-ttu-id="ed2b7-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ed2b7-109">**Required/Optional**</span></span>|<span data-ttu-id="ed2b7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ed2b7-110">**Data Type**</span></span>|<span data-ttu-id="ed2b7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed2b7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed2b7-112">_macroname_</span><span class="sxs-lookup"><span data-stu-id="ed2b7-112">_macroname_</span></span> <br/> |<span data-ttu-id="ed2b7-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ed2b7-113">Required</span></span>  <br/> |<span data-ttu-id="ed2b7-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ed2b7-114">**String**</span></span> <br/> |<span data-ttu-id="ed2b7-115">Имя вызываемого макроса.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="ed2b7-116">_projname_opt_</span><span class="sxs-lookup"><span data-stu-id="ed2b7-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="ed2b7-117">Необязательна</span><span class="sxs-lookup"><span data-stu-id="ed2b7-117">Optional</span></span>  <br/> |<span data-ttu-id="ed2b7-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ed2b7-118">**String**</span></span> <br/> | <span data-ttu-id="ed2b7-119">Проект, содержащий макрос.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed2b7-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed2b7-120">Remarks</span></span>

<span data-ttu-id="ed2b7-121">Если указан проект, Microsoft Visio сканирует все открытые документы на тот,  _который содержит_ projname_opt и вызывает макрос  _в_ этом проекте.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="ed2b7-122">Если  _projname_opt_ опущен или имеет null  _(""),_ предполагается, что имя макроса находится в проекте VBA документа, содержаном формулу RUNMACRO, для оценки.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="ed2b7-123">Функция RUNMACRO отличается от функции CALLTHIS тем, что она не передает ссылку на фигуру, которая владеет формулой, оцениваемой в _имени макроса._</span><span class="sxs-lookup"><span data-stu-id="ed2b7-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="ed2b7-124">Как и CALLTHIS, функция RUNMACRO не требует ссылки на projname_opt _вызова._</span><span class="sxs-lookup"><span data-stu-id="ed2b7-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="ed2b7-125">Код VBA, который вызывается, когда экземпляр Visio оценивает функцию RUNMACRO в формуле, не должен закрывать документ, содержащий ячейку, с помощью функции, так как ошибка приложения приводит к завершению Visio.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="ed2b7-126">Если необходимо закрыть документ, содержащий ячейку, которая использует функцию RUNMACRO, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="ed2b7-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="ed2b7-127">Закроем документ из кода, который не является VBA.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="ed2b7-128">Закроем документ из проекта, который не закрывается.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="ed2b7-129">Публикация сообщений в окне, чтобы закрыть окна в документе, а не закрывать документ.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="ed2b7-130">Дополнительные сведения о запуске кода в Visio см. в этой справке по таблицам фигур и сведениям о параметрах безопасности и запуске кода в [Visio.](about-security-settings-and-running-code-in-visio-shapesheet.md)</span><span class="sxs-lookup"><span data-stu-id="ed2b7-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ed2b7-131">Пример</span><span class="sxs-lookup"><span data-stu-id="ed2b7-131">Example</span></span>

<span data-ttu-id="ed2b7-132">В следующем примере вызывается макрос MyTest в модуле класса ThisDocument проекта VBA, содержащего формулу RUNMACRO.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="ed2b7-133">RUNMACRO ("ThisDocument.MyTest")</span><span class="sxs-lookup"><span data-stu-id="ed2b7-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

