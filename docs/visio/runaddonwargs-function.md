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
description: Выполняет строку и передает аргументы командной строки в программу в виде строки.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408707"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="f150e-103">Функция RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="f150e-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="f150e-104">Выполняет _строку_ и передает _аргументы_ командной строки в программу в виде строки.</span><span class="sxs-lookup"><span data-stu-id="f150e-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f150e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f150e-105">Syntax</span></span>

<span data-ttu-id="f150e-106">RUNADDONWARGS ("\* \* *String* \* *", "* \* *аргументы* \* \*")</span><span class="sxs-lookup"><span data-stu-id="f150e-106">RUNADDONWARGS(" \*\* *string* \*\* "," \*\* *arguments* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f150e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f150e-107">Parameters</span></span>

|<span data-ttu-id="f150e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f150e-108">**Name**</span></span>|<span data-ttu-id="f150e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f150e-109">**Required/Optional**</span></span>|<span data-ttu-id="f150e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f150e-110">**Data Type**</span></span>|<span data-ttu-id="f150e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f150e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f150e-112">_string_</span><span class="sxs-lookup"><span data-stu-id="f150e-112">_string_</span></span> <br/> |<span data-ttu-id="f150e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f150e-113">Required</span></span>  <br/> |<span data-ttu-id="f150e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f150e-114">**String**</span></span> <br/> | <span data-ttu-id="f150e-115">Имя надстройки.</span><span class="sxs-lookup"><span data-stu-id="f150e-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="f150e-116">_указаны_</span><span class="sxs-lookup"><span data-stu-id="f150e-116">_arguments_</span></span> <br/> |<span data-ttu-id="f150e-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f150e-117">Required</span></span>  <br/> |<span data-ttu-id="f150e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f150e-118">**String**</span></span> <br/> |<span data-ttu-id="f150e-119">Аргументы для передачи в программу.</span><span class="sxs-lookup"><span data-stu-id="f150e-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f150e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="f150e-120">Remarks</span></span>

<span data-ttu-id="f150e-121">На практике _аргументы_ должны иметь длину не более 50 символов.</span><span class="sxs-lookup"><span data-stu-id="f150e-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="f150e-122">Используйте функцию RUNADDONWARGS для привязывания программы, например надстройки, к ячейке, например, к ячейке Action или Events.</span><span class="sxs-lookup"><span data-stu-id="f150e-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="f150e-123">Функция RUNADDONWARGS может запускать только те надстройки, которые являются членами коллекции **надстроек** приложения.</span><span class="sxs-lookup"><span data-stu-id="f150e-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="f150e-124">В этой коллекции должна присутствовать надстройка, представляющая собой EXE-файл или VSL-файл:</span><span class="sxs-lookup"><span data-stu-id="f150e-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="f150e-125">Устанавливается в пути **загрузки** приложения или **надстройки** .</span><span class="sxs-lookup"><span data-stu-id="f150e-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="f150e-126">Добавляется программным способом с помощью метода **Add** коллекции **надстроек** .</span><span class="sxs-lookup"><span data-stu-id="f150e-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="f150e-127">Дополнительные сведения о запуске кода в Visio можно найти в статье [о параметрАх безопасности и выполнении кода в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) в этой ссылке на таблицу свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="f150e-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="f150e-128">В более ранних версиях Visio Эта функция отображается как _РУНАДДОНВАРГС.</span><span class="sxs-lookup"><span data-stu-id="f150e-128">In earlier versions of Visio, this function appears as _RUNADDONWARGS.</span></span> <span data-ttu-id="f150e-129">Приложения Visio версии 4,0 и более поздние принимают любой из этих стилей.</span><span class="sxs-lookup"><span data-stu-id="f150e-129">Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="f150e-130">Пример</span><span class="sxs-lookup"><span data-stu-id="f150e-130">Example</span></span>

<span data-ttu-id="f150e-131">RUNADDONWARGS ("ГРАФМКР. EXE ","/Графмакер = стек ")</span><span class="sxs-lookup"><span data-stu-id="f150e-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="f150e-132">Запускает надстройку Графмкр. exe и передает ей аргумент/Графмакер = Stack.</span><span class="sxs-lookup"><span data-stu-id="f150e-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

