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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414475"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="c8648-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c8648-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c8648-104">Возвращает время, представленное в виде _часа_, _минуты_и _секунды_.</span><span class="sxs-lookup"><span data-stu-id="c8648-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c8648-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8648-105">Syntax</span></span>

<span data-ttu-id="c8648-106">TIME (\* \* *час* \* \*, \* \* *минут* \* \*, \* \* *секунд* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c8648-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c8648-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8648-107">Parameters</span></span>

|<span data-ttu-id="c8648-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c8648-108">**Name**</span></span>|<span data-ttu-id="c8648-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c8648-109">**Required/Optional**</span></span>|<span data-ttu-id="c8648-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c8648-110">**Data Type**</span></span>|<span data-ttu-id="c8648-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8648-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c8648-112">_час_</span><span class="sxs-lookup"><span data-stu-id="c8648-112">_hour_</span></span> <br/> |<span data-ttu-id="c8648-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c8648-113">Required</span></span>  <br/> |<span data-ttu-id="c8648-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="c8648-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c8648-115">Компонент часа.</span><span class="sxs-lookup"><span data-stu-id="c8648-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="c8648-116">_за_</span><span class="sxs-lookup"><span data-stu-id="c8648-116">_minute_</span></span> <br/> |<span data-ttu-id="c8648-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c8648-117">Required</span></span>  <br/> |<span data-ttu-id="c8648-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="c8648-118">**Numeric**</span></span> <br/> |<span data-ttu-id="c8648-119">Минута комонент.</span><span class="sxs-lookup"><span data-stu-id="c8648-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="c8648-120">_Втор_</span><span class="sxs-lookup"><span data-stu-id="c8648-120">_second_</span></span> <br/> |<span data-ttu-id="c8648-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c8648-121">Required</span></span>  <br/> |<span data-ttu-id="c8648-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="c8648-122">**Numeric**</span></span> <br/> |<span data-ttu-id="c8648-123">Второй компонент.</span><span class="sxs-lookup"><span data-stu-id="c8648-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c8648-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8648-124">Return value</span></span>

<span data-ttu-id="c8648-125">Числовой</span><span class="sxs-lookup"><span data-stu-id="c8648-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="c8648-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8648-126">Example 1</span></span>

<span data-ttu-id="c8648-127">ВРЕМЯ (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="c8648-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="c8648-128">Возвращает значение, представляющее 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="c8648-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c8648-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c8648-129">Example 2</span></span>

<span data-ttu-id="c8648-130">FORMAT (время (15, 30, 30), "чч: мм")</span><span class="sxs-lookup"><span data-stu-id="c8648-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="c8648-131">Возвращает значение, представляющее 15:30.</span><span class="sxs-lookup"><span data-stu-id="c8648-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c8648-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c8648-132">Example 3</span></span>

<span data-ttu-id="c8648-133">ВРЕМЯ (15, 30, 30) + 8 EH.</span><span class="sxs-lookup"><span data-stu-id="c8648-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="c8648-134">Возвращает значение, представляющее 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="c8648-134">Returns the value representing 23:30:30.</span></span>
  

