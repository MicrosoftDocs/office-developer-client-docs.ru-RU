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
description: Возвращает время, представленные в час, минуты и секунды.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815044"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="b4145-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b4145-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b4145-104">Возвращает время, представленное _часа_, _минуты_и _второй_.</span><span class="sxs-lookup"><span data-stu-id="b4145-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b4145-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4145-105">Syntax</span></span>

<span data-ttu-id="b4145-106">ВРЕМЯ (** *час* **, ** *минуту* **, ** *второй* **)</span><span class="sxs-lookup"><span data-stu-id="b4145-106">TIME(** *hour* **, ** *minute* **, ** *second* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b4145-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4145-107">Parameters</span></span>

|<span data-ttu-id="b4145-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b4145-108">**Name**</span></span>|<span data-ttu-id="b4145-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="b4145-109">**Required/Optional**</span></span>|<span data-ttu-id="b4145-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b4145-110">**Data Type**</span></span>|<span data-ttu-id="b4145-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b4145-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b4145-112">_час_</span><span class="sxs-lookup"><span data-stu-id="b4145-112">_hour_</span></span> <br/> |<span data-ttu-id="b4145-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b4145-113">Required</span></span>  <br/> |<span data-ttu-id="b4145-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="b4145-114">**Numeric**</span></span> <br/> |<span data-ttu-id="b4145-115">Компонент часов.</span><span class="sxs-lookup"><span data-stu-id="b4145-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="b4145-116">_минуты_</span><span class="sxs-lookup"><span data-stu-id="b4145-116">_minute_</span></span> <br/> |<span data-ttu-id="b4145-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b4145-117">Required</span></span>  <br/> |<span data-ttu-id="b4145-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="b4145-118">**Numeric**</span></span> <br/> |<span data-ttu-id="b4145-119">Comonent минут.</span><span class="sxs-lookup"><span data-stu-id="b4145-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="b4145-120">_секунды_</span><span class="sxs-lookup"><span data-stu-id="b4145-120">_second_</span></span> <br/> |<span data-ttu-id="b4145-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b4145-121">Required</span></span>  <br/> |<span data-ttu-id="b4145-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="b4145-122">**Numeric**</span></span> <br/> |<span data-ttu-id="b4145-123">Второй компонент.</span><span class="sxs-lookup"><span data-stu-id="b4145-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b4145-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b4145-124">Return value</span></span>

<span data-ttu-id="b4145-125">Числовой</span><span class="sxs-lookup"><span data-stu-id="b4145-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="b4145-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4145-126">Example 1</span></span>

<span data-ttu-id="b4145-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="b4145-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="b4145-128">Возвращает значение, представляющее 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="b4145-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b4145-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b4145-129">Example 2</span></span>

<span data-ttu-id="b4145-130">Format(Time(15,30,30),"hh:mm")</span><span class="sxs-lookup"><span data-stu-id="b4145-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="b4145-131">Возвращает значение, представляющее 15:30.</span><span class="sxs-lookup"><span data-stu-id="b4145-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b4145-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b4145-132">Example 3</span></span>

<span data-ttu-id="b4145-133">Time(15,30,30) + 8 а.</span><span class="sxs-lookup"><span data-stu-id="b4145-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="b4145-134">Возвращает значение, представляющее 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="b4145-134">Returns the value representing 23:30:30.</span></span>
  

