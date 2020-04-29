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
description: Возвращает валуеифтруе, если логикалекспрессион имеет значение TRUE. В противном случае возвращается валуеиффалсе.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405473"
---
# <a name="if-function"></a><span data-ttu-id="3796f-104">Функция IF</span><span class="sxs-lookup"><span data-stu-id="3796f-104">IF Function</span></span>

<span data-ttu-id="3796f-105">Возвращает _валуеифтруе_ , если _логикалекспрессион_ имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3796f-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="3796f-106">В противном случае возвращается _валуеиффалсе_.</span><span class="sxs-lookup"><span data-stu-id="3796f-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3796f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3796f-107">Syntax</span></span>

<span data-ttu-id="3796f-108">IF (\* \* *логикалекспрессион* \* \*, \* \* *валуеифтруе* \* \*, \* \* *валуеиффалсе* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3796f-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3796f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3796f-109">Parameters</span></span>

|<span data-ttu-id="3796f-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3796f-110">**Name**</span></span>|<span data-ttu-id="3796f-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3796f-111">**Required/Optional**</span></span>|<span data-ttu-id="3796f-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3796f-112">**Data Type**</span></span>|<span data-ttu-id="3796f-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3796f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3796f-114">_логикалекспрессион_</span><span class="sxs-lookup"><span data-stu-id="3796f-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="3796f-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3796f-115">Required</span></span>  <br/> |<span data-ttu-id="3796f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3796f-116">**String**</span></span> <br/> |<span data-ttu-id="3796f-117">Вычисляемое выражение.</span><span class="sxs-lookup"><span data-stu-id="3796f-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="3796f-118">_валуеифтруе_</span><span class="sxs-lookup"><span data-stu-id="3796f-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="3796f-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3796f-119">Required</span></span>  <br/> |<span data-ttu-id="3796f-120">**Разные**</span><span class="sxs-lookup"><span data-stu-id="3796f-120">**Varies**</span></span> <br/> |<span data-ttu-id="3796f-121">Значение, возвращаемое, если _логикалекспрессион_ имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3796f-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="3796f-122">_валуеиффалсе_</span><span class="sxs-lookup"><span data-stu-id="3796f-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="3796f-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3796f-123">Required</span></span>  <br/> |<span data-ttu-id="3796f-124">**Разные**</span><span class="sxs-lookup"><span data-stu-id="3796f-124">**Varies**</span></span> <br/> | <span data-ttu-id="3796f-125">Значение, возвращаемое, если _логикалекспрессион_ имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="3796f-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3796f-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3796f-126">Return value</span></span>

<span data-ttu-id="3796f-127">Разные</span><span class="sxs-lookup"><span data-stu-id="3796f-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="3796f-128">Пример</span><span class="sxs-lookup"><span data-stu-id="3796f-128">Example</span></span>

<span data-ttu-id="3796f-129">Если (высота \> 1,25 в, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="3796f-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="3796f-130">Возвращает 5, если высота фигуры больше 1,25 дюйма.</span><span class="sxs-lookup"><span data-stu-id="3796f-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="3796f-131">Возвращает значение 7, если высота фигуры меньше или равна 1,25 сантиметра.</span><span class="sxs-lookup"><span data-stu-id="3796f-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

