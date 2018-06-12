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
description: Выполняет строку и передает аргументы командной строки программы как строку.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814716"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="483f6-103">Функция RUNADDONWARGS</span><span class="sxs-lookup"><span data-stu-id="483f6-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="483f6-104">Выполняет _строку_ и передает _аргументы_ командной строки программы как строку.</span><span class="sxs-lookup"><span data-stu-id="483f6-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="483f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="483f6-105">Syntax</span></span>

<span data-ttu-id="483f6-106">RUNADDONWARGS ("** *строки* **","** *аргументы* **")</span><span class="sxs-lookup"><span data-stu-id="483f6-106">RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="483f6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="483f6-107">Parameters</span></span>

|<span data-ttu-id="483f6-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="483f6-108">**Name**</span></span>|<span data-ttu-id="483f6-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="483f6-109">**Required/Optional**</span></span>|<span data-ttu-id="483f6-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="483f6-110">**Data Type**</span></span>|<span data-ttu-id="483f6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="483f6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="483f6-112">_string_</span><span class="sxs-lookup"><span data-stu-id="483f6-112">_string_</span></span> <br/> |<span data-ttu-id="483f6-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="483f6-113">Required</span></span>  <br/> |<span data-ttu-id="483f6-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="483f6-114">**String**</span></span> <br/> | <span data-ttu-id="483f6-115">Имя дополнительного компонента.</span><span class="sxs-lookup"><span data-stu-id="483f6-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="483f6-116">_аргументы_</span><span class="sxs-lookup"><span data-stu-id="483f6-116">_arguments_</span></span> <br/> |<span data-ttu-id="483f6-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="483f6-117">Required</span></span>  <br/> |<span data-ttu-id="483f6-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="483f6-118">**String**</span></span> <br/> |<span data-ttu-id="483f6-119">Аргументы для передачи в программу.</span><span class="sxs-lookup"><span data-stu-id="483f6-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="483f6-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="483f6-120">Remarks</span></span>

<span data-ttu-id="483f6-121">На практике _аргументы_ должны быть не более 50 знаков.</span><span class="sxs-lookup"><span data-stu-id="483f6-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="483f6-122">Используйте функцию RUNADDONWARGS для привязки программы, например дополнительного компонента для ячейки, например, действия или события ячейки.</span><span class="sxs-lookup"><span data-stu-id="483f6-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="483f6-123">Функция RUNADDONWARGS можно выполнить только надстройки, которые являются участниками семейства **надстроек** приложения.</span><span class="sxs-lookup"><span data-stu-id="483f6-123">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection.</span></span> <span data-ttu-id="483f6-124">Должны присутствовать в этой коллекции, дополнительный компонент должен быть EXE-файл или (VSL) для файла, который является:</span><span class="sxs-lookup"><span data-stu-id="483f6-124">To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="483f6-125">Установлен в пути приложения **при запуске** или **надстройки** .</span><span class="sxs-lookup"><span data-stu-id="483f6-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="483f6-126">Добавлен программными средствами с помощью метода **Add** коллекции **надстроек** .</span><span class="sxs-lookup"><span data-stu-id="483f6-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="483f6-127">Дополнительные сведения о запуске кода в Visio содержатся в разделе [о параметров безопасности и выполнить код в Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) этот справочник по таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="483f6-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="483f6-128">В более ранних версиях Visio эта функция отображается в виде _RUNADDONWARGS.</span><span class="sxs-lookup"><span data-stu-id="483f6-128">In earlier versions of Visio, this function appears as _RUNADDONWARGS.</span></span> <span data-ttu-id="483f6-129">Версии приложения Visio 4.0 и более поздних версий принимать любого из стилей.</span><span class="sxs-lookup"><span data-stu-id="483f6-129">Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="483f6-130">Пример</span><span class="sxs-lookup"><span data-stu-id="483f6-130">Example</span></span>

<span data-ttu-id="483f6-131">RUNADDONWARGS ("GRAPHMKR. Exe-ФАЙЛ», "/ GraphMaker = стек»)</span><span class="sxs-lookup"><span data-stu-id="483f6-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="483f6-132">Запускает Graphmkr.exe дополнительный компонент и передает его /GraphMaker аргумент = стека.</span><span class="sxs-lookup"><span data-stu-id="483f6-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

