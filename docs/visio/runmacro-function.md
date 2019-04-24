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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355715"
---
# <a name="runmacro-function"></a><span data-ttu-id="31cc6-103">Функция RUNMACRO</span><span class="sxs-lookup"><span data-stu-id="31cc6-103">RUNMACRO Function</span></span>

<span data-ttu-id="31cc6-104">Вызывает макрос в проекте Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="31cc6-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="31cc6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31cc6-105">Syntax</span></span>

<span data-ttu-id="31cc6-106">ЗапускМакроса (\* \* *имяМакроса* \* \* [, \* \* *прожнаме_опт* \* \*])</span><span class="sxs-lookup"><span data-stu-id="31cc6-106">RUNMACRO (\*\* *macroname* \*\* [, \*\* *projname_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="31cc6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31cc6-107">Parameters</span></span>

|<span data-ttu-id="31cc6-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="31cc6-108">**Name**</span></span>|<span data-ttu-id="31cc6-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="31cc6-109">**Required/Optional**</span></span>|<span data-ttu-id="31cc6-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="31cc6-110">**Data Type**</span></span>|<span data-ttu-id="31cc6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="31cc6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="31cc6-112">_макрос_</span><span class="sxs-lookup"><span data-stu-id="31cc6-112">_macroname_</span></span> <br/> |<span data-ttu-id="31cc6-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31cc6-113">Required</span></span>  <br/> |<span data-ttu-id="31cc6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="31cc6-114">**String**</span></span> <br/> |<span data-ttu-id="31cc6-115">Имя вызываемого макроса.</span><span class="sxs-lookup"><span data-stu-id="31cc6-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="31cc6-116">_прожнаме_опт_</span><span class="sxs-lookup"><span data-stu-id="31cc6-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="31cc6-117">Необязательно</span><span class="sxs-lookup"><span data-stu-id="31cc6-117">Optional</span></span>  <br/> |<span data-ttu-id="31cc6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="31cc6-118">**String**</span></span> <br/> | <span data-ttu-id="31cc6-119">Проект, содержащий макрос.</span><span class="sxs-lookup"><span data-stu-id="31cc6-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31cc6-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="31cc6-120">Remarks</span></span>

<span data-ttu-id="31cc6-121">Если указан проект, Microsoft Visio сканирует все открытые документы для элемента, содержащего _прожнаме_опт_ , и вызывает _макрос имяМакроса_ в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="31cc6-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="31cc6-122">Если _прожнаме_опт_ опущен или имеет значение null (""), предполагается, что _имяМакроса_ находится в проекте VBA документа, содержащего оцениваемую формулу ЗапускМакроса.</span><span class="sxs-lookup"><span data-stu-id="31cc6-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="31cc6-123">Функция RUNMACRO отличается от функции CALLTHIS в том, что она не передает ссылку на фигуру, которой принадлежит формула, оцениваемую до _имяМакроса_.</span><span class="sxs-lookup"><span data-stu-id="31cc6-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="31cc6-124">Как и в CALLTHIS, для вызова функции ЗАПУСКМАКРОСА не требуется ссылаться на _прожнаме_опт_ .</span><span class="sxs-lookup"><span data-stu-id="31cc6-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="31cc6-125">Код VBA, вызываемый, когда экземпляр Visio оценивает функцию ЗАПУСКМАКРОСА в формуле, не должно закрывать документ, содержащий ячейку, с помощью функции, так как результаты ошибки приложения и Visio завершает работу.</span><span class="sxs-lookup"><span data-stu-id="31cc6-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="31cc6-126">Если вам нужно закрыть документ с ячейкой, использующей функцию ЗАПУСКМАКРОСА, используйте один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="31cc6-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="31cc6-127">Закройте документ из кода, который не является VBA.</span><span class="sxs-lookup"><span data-stu-id="31cc6-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="31cc6-128">Закройте документ из проекта, отличного от закрывающего.</span><span class="sxs-lookup"><span data-stu-id="31cc6-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="31cc6-129">ПоМещать сообщения окна, чтобы закрыть окна в документе, а не закрывать документ.</span><span class="sxs-lookup"><span data-stu-id="31cc6-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="31cc6-130">Дополнительные сведения о запуске кода в Visio можно найти в статье [о параметрах безопасности и выполнении кода в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой ссылке на таблицу свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="31cc6-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="31cc6-131">Пример</span><span class="sxs-lookup"><span data-stu-id="31cc6-131">Example</span></span>

<span data-ttu-id="31cc6-132">В приведенном ниже примере вызывается макрос MyTest в модуле класса ThisDocument проекта VBA, содержащего формулу ЗАПУСКМАКРОСА.</span><span class="sxs-lookup"><span data-stu-id="31cc6-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="31cc6-133">ЗАПУСКМАКРОСА ("ThisDocument. MyTest")</span><span class="sxs-lookup"><span data-stu-id="31cc6-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

