---
title: Функция RUNADDONWARGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Выполняет строку и передает аргументы строки команд в программу в качестве строки.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408707"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="9f170-103">Функция RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="9f170-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="9f170-104">Выполняет  _строку_ и передает аргументы строки  _команд_ в программу в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="9f170-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f170-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f170-105">Syntax</span></span>

<span data-ttu-id="9f170-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="9f170-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f170-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f170-107">Parameters</span></span>

|<span data-ttu-id="9f170-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9f170-108">**Name**</span></span>|<span data-ttu-id="9f170-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="9f170-109">**Required/Optional**</span></span>|<span data-ttu-id="9f170-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9f170-110">**Data Type**</span></span>|<span data-ttu-id="9f170-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f170-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f170-112">_string_</span><span class="sxs-lookup"><span data-stu-id="9f170-112">_string_</span></span> <br/> |<span data-ttu-id="9f170-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9f170-113">Required</span></span>  <br/> |<span data-ttu-id="9f170-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9f170-114">**String**</span></span> <br/> | <span data-ttu-id="9f170-115">Имя надстройки.</span><span class="sxs-lookup"><span data-stu-id="9f170-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="9f170-116">_аргументы_</span><span class="sxs-lookup"><span data-stu-id="9f170-116">_arguments_</span></span> <br/> |<span data-ttu-id="9f170-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9f170-117">Required</span></span>  <br/> |<span data-ttu-id="9f170-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9f170-118">**String**</span></span> <br/> |<span data-ttu-id="9f170-119">Аргументы для передачи в программу.</span><span class="sxs-lookup"><span data-stu-id="9f170-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f170-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="9f170-120">Remarks</span></span>

<span data-ttu-id="9f170-121">На практике  _аргументов_ должно быть 50 или меньше символов.</span><span class="sxs-lookup"><span data-stu-id="9f170-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="9f170-122">Используйте функцию RUNADDONWARGS, чтобы привязать программу, например надстройку, к ячейке, например, к ячейке Action или Events.</span><span class="sxs-lookup"><span data-stu-id="9f170-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="9f170-123">Функция RUNADDONWARGS может запускать только надстройки, которые являются членами коллекции **Addons** приложения.</span><span class="sxs-lookup"><span data-stu-id="9f170-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="9f170-124">Чтобы присутствовать в этой коллекции, надстройка должна быть файлом EXE или VSL-файлом, который:</span><span class="sxs-lookup"><span data-stu-id="9f170-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="9f170-125">Установлено на пути **запуска или** **надстройки** приложения.</span><span class="sxs-lookup"><span data-stu-id="9f170-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="9f170-126">Добавлено программным путем с помощью **метода Add** из коллекции **Addons.**</span><span class="sxs-lookup"><span data-stu-id="9f170-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="9f170-127">Дополнительные сведения о запуске кода в Visio см. в Параметры и [running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой справке ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="9f170-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="9f170-128">В более ранних версиях Visio эта функция отображается как _RUNADDONWARGS.</span><span class="sxs-lookup"><span data-stu-id="9f170-128">In earlier versions of Visio, this function appears as _RUNADDONWARGS.</span></span> <span data-ttu-id="9f170-129">Visio версии приложения 4.0 и позднее принимают любой стиль.</span><span class="sxs-lookup"><span data-stu-id="9f170-129">Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="9f170-130">Пример</span><span class="sxs-lookup"><span data-stu-id="9f170-130">Example</span></span>

<span data-ttu-id="9f170-131">RUNADDONWARGS ("GRAPHMKR.EXE","/GraphMaker=Stack")</span><span class="sxs-lookup"><span data-stu-id="9f170-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="9f170-132">Запускает надстройку Graphmkr.exe и передает ее аргумент /GraphMaker=Stack.</span><span class="sxs-lookup"><span data-stu-id="9f170-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

