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
description: Отображает страницу с именем имя_страницы в активное окно.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397151"
---
# <a name="gotopage-function"></a><span data-ttu-id="3ef4e-103">Функция GOTOPAGE</span><span class="sxs-lookup"><span data-stu-id="3ef4e-103">GOTOPAGE Function</span></span>

<span data-ttu-id="3ef4e-104">Отображает страницу с именем *имя_страницы* в активное окно.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3ef4e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ef4e-105">Syntax</span></span>

<span data-ttu-id="3ef4e-106">НАСТРАНИЦУ ("\*\* *имя_страницы* \*\*")</span><span class="sxs-lookup"><span data-stu-id="3ef4e-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3ef4e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ef4e-107">Parameters</span></span>

|<span data-ttu-id="3ef4e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3ef4e-108">**Name**</span></span>|<span data-ttu-id="3ef4e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3ef4e-109">**Required/Optional**</span></span>|<span data-ttu-id="3ef4e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3ef4e-110">**Data Type**</span></span>|<span data-ttu-id="3ef4e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ef4e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3ef4e-112">_имя_страницы_</span><span class="sxs-lookup"><span data-stu-id="3ef4e-112">_pagename_</span></span> <br/> |<span data-ttu-id="3ef4e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3ef4e-113">Required</span></span>  <br/> |<span data-ttu-id="3ef4e-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3ef4e-114">**String**</span></span> <br/> |<span data-ttu-id="3ef4e-115">Имя страницы, чтобы перейти к.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ef4e-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="3ef4e-116">Remarks</span></span>

<span data-ttu-id="3ef4e-117">Если окно уже отображается страница, это окно становится активной.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="3ef4e-118">Если *имя_страницы* не существует, приложение пытается перейти к https:// *имя_страницы* /.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="3ef4e-119">Если Visio выступать в качестве сервера на месте, функция НАСТРАНИЦУ не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="3ef4e-120">Функция ГИПЕРССЫЛКИ для перехода к любой путь DOS, UNC или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="3ef4e-121">В более ранних версиях продуктов Visio эта функция отображается в виде _GOTOPAGE.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-121">In earlier versions of Visio products, this function appears as _GOTOPAGE.</span></span> <span data-ttu-id="3ef4e-122">Visio версии 4.0 и более поздних версий принимать любого из стилей.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-122">Visio versions 4.0 and later accept either style.</span></span> 
  

