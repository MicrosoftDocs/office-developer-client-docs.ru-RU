---
title: Функция GOTOPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Отображает страницу с именем страницы в активном окне.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302970"
---
# <a name="gotopage-function"></a><span data-ttu-id="a7a46-103">Функция GOTOPAGE</span><span class="sxs-lookup"><span data-stu-id="a7a46-103">GOTOPAGE Function</span></span>

<span data-ttu-id="a7a46-104">Отображает страницу с именем  *страницы*  в активном окне.</span><span class="sxs-lookup"><span data-stu-id="a7a46-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a7a46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7a46-105">Syntax</span></span>

<span data-ttu-id="a7a46-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="a7a46-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a7a46-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7a46-107">Parameters</span></span>

|<span data-ttu-id="a7a46-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a7a46-108">**Name**</span></span>|<span data-ttu-id="a7a46-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a7a46-109">**Required/Optional**</span></span>|<span data-ttu-id="a7a46-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a7a46-110">**Data Type**</span></span>|<span data-ttu-id="a7a46-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7a46-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7a46-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="a7a46-112">_pagename_</span></span> <br/> |<span data-ttu-id="a7a46-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a7a46-113">Required</span></span>  <br/> |<span data-ttu-id="a7a46-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a7a46-114">**String**</span></span> <br/> |<span data-ttu-id="a7a46-115">Имя страницы, на которое нужно перейти.</span><span class="sxs-lookup"><span data-stu-id="a7a46-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7a46-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7a46-116">Remarks</span></span>

<span data-ttu-id="a7a46-117">Если окно уже отображает страницу, это окно становится активным.</span><span class="sxs-lookup"><span data-stu-id="a7a46-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="a7a46-118">Если  *имени страницы*  не существует, приложение пытается перейти к https://  *pagename*  /.</span><span class="sxs-lookup"><span data-stu-id="a7a46-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="a7a46-119">Если Visio работает как сервер на месте, функция GOTOPAGE не влияет.</span><span class="sxs-lookup"><span data-stu-id="a7a46-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="a7a46-120">Вы можете использовать функцию HYPERLINK для перемещения по любому пути DOS, UNC или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a7a46-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="a7a46-121">В более ранних версиях Visio эта функция отображается как _GOTOPAGE.</span><span class="sxs-lookup"><span data-stu-id="a7a46-121">In earlier versions of Visio products, this function appears as _GOTOPAGE.</span></span> <span data-ttu-id="a7a46-122">Visio версии 4.0 и более поздние версии принимают любой стиль.</span><span class="sxs-lookup"><span data-stu-id="a7a46-122">Visio versions 4.0 and later accept either style.</span></span> 
  

