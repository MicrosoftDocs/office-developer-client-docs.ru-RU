---
title: Функция IF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Возвращает valueiftrue, если logicalexpression имеет значение TRUE. В противном случае возвращает valueiffalse.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813941"
---
# <a name="if-function"></a><span data-ttu-id="5f40b-104">Функция IF</span><span class="sxs-lookup"><span data-stu-id="5f40b-104">IF Function</span></span>

<span data-ttu-id="5f40b-105">Возвращает _valueiftrue_ , если _logicalexpression_ имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5f40b-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="5f40b-106">В противном случае возвращает _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="5f40b-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5f40b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f40b-107">Syntax</span></span>

<span data-ttu-id="5f40b-108">Если (** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* **)</span><span class="sxs-lookup"><span data-stu-id="5f40b-108">IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f40b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f40b-109">Parameters</span></span>

|<span data-ttu-id="5f40b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5f40b-110">**Name**</span></span>|<span data-ttu-id="5f40b-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="5f40b-111">**Required/Optional**</span></span>|<span data-ttu-id="5f40b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5f40b-112">**Data Type**</span></span>|<span data-ttu-id="5f40b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5f40b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f40b-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="5f40b-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="5f40b-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5f40b-115">Required</span></span>  <br/> |<span data-ttu-id="5f40b-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="5f40b-116">**String**</span></span> <br/> |<span data-ttu-id="5f40b-117">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="5f40b-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="5f40b-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="5f40b-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="5f40b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5f40b-119">Required</span></span>  <br/> |<span data-ttu-id="5f40b-120">**Разные**</span><span class="sxs-lookup"><span data-stu-id="5f40b-120">**Varies**</span></span> <br/> |<span data-ttu-id="5f40b-121">Значение, возвращаемое, если _logicalexpression_ имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="5f40b-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="5f40b-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="5f40b-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="5f40b-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5f40b-123">Required</span></span>  <br/> |<span data-ttu-id="5f40b-124">**Разные**</span><span class="sxs-lookup"><span data-stu-id="5f40b-124">**Varies**</span></span> <br/> | <span data-ttu-id="5f40b-125">Значение, возвращаемое, если _logicalexpression_ имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="5f40b-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5f40b-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5f40b-126">Return value</span></span>

<span data-ttu-id="5f40b-127">Разные</span><span class="sxs-lookup"><span data-stu-id="5f40b-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="5f40b-128">Пример</span><span class="sxs-lookup"><span data-stu-id="5f40b-128">Example</span></span>

<span data-ttu-id="5f40b-129">Если (высота \> 1,25 в, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="5f40b-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="5f40b-130">Возвращает 5, если высота фигуры больше, чем 1,25 дюйма.</span><span class="sxs-lookup"><span data-stu-id="5f40b-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="5f40b-131">Возвращает 7, если высота фигуры — меньше или равно 1,25 дюйма.</span><span class="sxs-lookup"><span data-stu-id="5f40b-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

