---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Возвращает время, относяное к часам, минутам и секундам.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414475"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="8b8b8-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8b8b8-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8b8b8-104">Возвращает время, относяное к _часам,_ _минутам_ и _секундам._</span><span class="sxs-lookup"><span data-stu-id="8b8b8-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8b8b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b8b8-105">Syntax</span></span>

<span data-ttu-id="8b8b8-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8b8b8-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8b8b8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b8b8-107">Parameters</span></span>

|<span data-ttu-id="8b8b8-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-108">**Name**</span></span>|<span data-ttu-id="8b8b8-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-109">**Required/Optional**</span></span>|<span data-ttu-id="8b8b8-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-110">**Data Type**</span></span>|<span data-ttu-id="8b8b8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8b8b8-112">_час_</span><span class="sxs-lookup"><span data-stu-id="8b8b8-112">_hour_</span></span> <br/> |<span data-ttu-id="8b8b8-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8b8b8-113">Required</span></span>  <br/> |<span data-ttu-id="8b8b8-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8b8b8-115">Компонент часов.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="8b8b8-116">_минута_</span><span class="sxs-lookup"><span data-stu-id="8b8b8-116">_minute_</span></span> <br/> |<span data-ttu-id="8b8b8-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8b8b8-117">Required</span></span>  <br/> |<span data-ttu-id="8b8b8-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8b8b8-119">Минутный comonent.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="8b8b8-120">_во-вторых_</span><span class="sxs-lookup"><span data-stu-id="8b8b8-120">_second_</span></span> <br/> |<span data-ttu-id="8b8b8-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8b8b8-121">Required</span></span>  <br/> |<span data-ttu-id="8b8b8-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="8b8b8-122">**Numeric**</span></span> <br/> |<span data-ttu-id="8b8b8-123">Второй компонент.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8b8b8-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b8b8-124">Return value</span></span>

<span data-ttu-id="8b8b8-125">Числовой</span><span class="sxs-lookup"><span data-stu-id="8b8b8-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="8b8b8-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b8b8-126">Example 1</span></span>

<span data-ttu-id="8b8b8-127">TIME (15 30,30)</span><span class="sxs-lookup"><span data-stu-id="8b8b8-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="8b8b8-128">Возвращает значение, представляющее 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8b8b8-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b8b8-129">Example 2</span></span>

<span data-ttu-id="8b8b8-130">FORMAT (TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="8b8b8-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="8b8b8-131">Возвращает значение 15:30.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8b8b8-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8b8b8-132">Example 3</span></span>

<span data-ttu-id="8b8b8-133">TIME (15 30,30) + 8 да.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="8b8b8-134">Возвращает значение, представляющее 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-134">Returns the value representing 23:30:30.</span></span>
  

