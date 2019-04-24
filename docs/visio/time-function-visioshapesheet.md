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
description: Возвращает время, представленное в виде часа, минуты и секунды.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280999"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="e01aa-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e01aa-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e01aa-104">Возвращает время, представленное в виде _часа_, _минуты_и _секунды_.</span><span class="sxs-lookup"><span data-stu-id="e01aa-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e01aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e01aa-105">Syntax</span></span>

<span data-ttu-id="e01aa-106">TIME (\* \* *час* \* \*, \* \* *минут* \* \*, \* \* *секунд* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e01aa-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e01aa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e01aa-107">Parameters</span></span>

|<span data-ttu-id="e01aa-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e01aa-108">**Name**</span></span>|<span data-ttu-id="e01aa-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e01aa-109">**Required/Optional**</span></span>|<span data-ttu-id="e01aa-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e01aa-110">**Data Type**</span></span>|<span data-ttu-id="e01aa-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e01aa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e01aa-112">_час_</span><span class="sxs-lookup"><span data-stu-id="e01aa-112">_hour_</span></span> <br/> |<span data-ttu-id="e01aa-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e01aa-113">Required</span></span>  <br/> |<span data-ttu-id="e01aa-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e01aa-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e01aa-115">Компонент часа.</span><span class="sxs-lookup"><span data-stu-id="e01aa-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="e01aa-116">_за_</span><span class="sxs-lookup"><span data-stu-id="e01aa-116">_minute_</span></span> <br/> |<span data-ttu-id="e01aa-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e01aa-117">Required</span></span>  <br/> |<span data-ttu-id="e01aa-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e01aa-118">**Numeric**</span></span> <br/> |<span data-ttu-id="e01aa-119">Минута комонент.</span><span class="sxs-lookup"><span data-stu-id="e01aa-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="e01aa-120">_Втор_</span><span class="sxs-lookup"><span data-stu-id="e01aa-120">_second_</span></span> <br/> |<span data-ttu-id="e01aa-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e01aa-121">Required</span></span>  <br/> |<span data-ttu-id="e01aa-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e01aa-122">**Numeric**</span></span> <br/> |<span data-ttu-id="e01aa-123">Второй компонент.</span><span class="sxs-lookup"><span data-stu-id="e01aa-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e01aa-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e01aa-124">Return value</span></span>

<span data-ttu-id="e01aa-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="e01aa-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="e01aa-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e01aa-126">Example 1</span></span>

<span data-ttu-id="e01aa-127">ВРЕМЯ (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="e01aa-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="e01aa-128">Возвращает значение, представляющее 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="e01aa-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e01aa-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e01aa-129">Example 2</span></span>

<span data-ttu-id="e01aa-130">FORMAT (время (15, 30, 30), "чч: мм")</span><span class="sxs-lookup"><span data-stu-id="e01aa-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="e01aa-131">Возвращает значение, представляющее 15:30.</span><span class="sxs-lookup"><span data-stu-id="e01aa-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e01aa-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e01aa-132">Example 3</span></span>

<span data-ttu-id="e01aa-133">ВРЕМЯ (15, 30, 30) + 8 EH.</span><span class="sxs-lookup"><span data-stu-id="e01aa-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="e01aa-134">Возвращает значение, представляющее 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="e01aa-134">Returns the value representing 23:30:30.</span></span>
  

