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
description: Вызывает макроса в Microsoft Visual Basic для приложений (VBA) проект.
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814717"
---
# <a name="runmacro-function"></a><span data-ttu-id="c9cd8-103">Функция RUNMACRO</span><span class="sxs-lookup"><span data-stu-id="c9cd8-103">RUNMACRO Function</span></span>

<span data-ttu-id="c9cd8-104">Вызывает макроса в Microsoft Visual Basic для приложений (VBA) проект.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c9cd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9cd8-105">Syntax</span></span>

<span data-ttu-id="c9cd8-106">ЗАПУСКМАКРОСА (** *имяМакроса* ** [, ** *projname_opt* **])</span><span class="sxs-lookup"><span data-stu-id="c9cd8-106">RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c9cd8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9cd8-107">Parameters</span></span>

|<span data-ttu-id="c9cd8-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c9cd8-108">**Name**</span></span>|<span data-ttu-id="c9cd8-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c9cd8-109">**Required/Optional**</span></span>|<span data-ttu-id="c9cd8-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c9cd8-110">**Data Type**</span></span>|<span data-ttu-id="c9cd8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c9cd8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c9cd8-112">_имяМакроса_</span><span class="sxs-lookup"><span data-stu-id="c9cd8-112">_macroname_</span></span> <br/> |<span data-ttu-id="c9cd8-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c9cd8-113">Required</span></span>  <br/> |<span data-ttu-id="c9cd8-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c9cd8-114">**String**</span></span> <br/> |<span data-ttu-id="c9cd8-115">Имя макроса для вызова.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="c9cd8-116">_projname_opt_</span><span class="sxs-lookup"><span data-stu-id="c9cd8-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="c9cd8-117">Optional</span><span class="sxs-lookup"><span data-stu-id="c9cd8-117">Optional</span></span>  <br/> |<span data-ttu-id="c9cd8-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c9cd8-118">**String**</span></span> <br/> | <span data-ttu-id="c9cd8-119">Проект, содержащий макрос.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9cd8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9cd8-120">Remarks</span></span>

<span data-ttu-id="c9cd8-121">Если проект указан, Microsoft Visio сканирование всех открытых документов для одного содержащего _projname_opt_ и вызовы _имяМакроса_ в проекте.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="c9cd8-122">Если _projname_opt_ неправильных или значение null ("»), _имяМакроса_ предполагается, что в проекте VBA документа, которая содержит формулу ЗАПУСКМАКРОСА вычислением.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="c9cd8-123">Функция ЗАПУСКМАКРОСА отличается от функции CALLTHIS, то есть не передает ссылку на фигуры, которому принадлежит вычислением _имяМакроса_формулу.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="c9cd8-124">Как CALLTHIS функция ЗАПУСКМАКРОСА не требуется ссылка на _projname_opt_ для его вызова.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="c9cd8-125">Код VBA, которая вызывается при экземпляр Visio оценивает ЗАПУСКМАКРОСА функции в формуле не следует закрыть документ, содержащий ячейки, с помощью функции, так как возникает ошибка приложения и завершает Visio.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="c9cd8-126">Если необходимо закрыть документ, содержащий ячейки, которая использует функцию ЗАПУСКМАКРОСА, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="c9cd8-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="c9cd8-127">Закройте документ, из кода, который не является VBA.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="c9cd8-128">Закройте документ из проекта не закрывается.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="c9cd8-129">Публиковать сообщения окна для закрытия окна в документе, а не закрытия документа.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="c9cd8-130">Дополнительные сведения о запуске кода в Visio можно [о настройках безопасности и выполнение кода в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этом по таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c9cd8-131">Пример</span><span class="sxs-lookup"><span data-stu-id="c9cd8-131">Example</span></span>

<span data-ttu-id="c9cd8-132">В следующем примере вызывается вызывает MyTest в модуле класса ThisDocument проекта VBA, содержащий формулу ЗАПУСКМАКРОСА макроса.</span><span class="sxs-lookup"><span data-stu-id="c9cd8-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="c9cd8-133">ЗАПУСКМАКРОСА («ThisDocument.MyTest»)</span><span class="sxs-lookup"><span data-stu-id="c9cd8-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

