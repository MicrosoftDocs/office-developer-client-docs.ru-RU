---
title: Функция FORMAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Возвращает результат выражения в виде строки, отформатированной в соответствии с formatpicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404654"
---
# <a name="format-function"></a><span data-ttu-id="886a7-103">Функция FORMAT</span><span class="sxs-lookup"><span data-stu-id="886a7-103">FORMAT Function</span></span>

<span data-ttu-id="886a7-104">Возвращает результат выражения  _в_ виде строки, отформатированной в соответствии  _с formatpicture_.</span><span class="sxs-lookup"><span data-stu-id="886a7-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="886a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="886a7-105">Syntax</span></span>

<span data-ttu-id="886a7-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="886a7-106">FORMAT(\*\* *expression* \*\*," \*\* *formatpicture* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="886a7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="886a7-107">Parameters</span></span>

|<span data-ttu-id="886a7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="886a7-108">**Name**</span></span>|<span data-ttu-id="886a7-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="886a7-109">**Required/Optional**</span></span>|<span data-ttu-id="886a7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="886a7-110">**Data Type**</span></span>|<span data-ttu-id="886a7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="886a7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="886a7-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="886a7-112">_expression_</span></span> <br/> |<span data-ttu-id="886a7-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="886a7-113">Required</span></span>  <br/> |<span data-ttu-id="886a7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="886a7-114">**String**</span></span> <br/> |<span data-ttu-id="886a7-115">Сочетание констант, операторов, функций и ссылок на ячейки ShapeSheet, что приводит к значению.</span><span class="sxs-lookup"><span data-stu-id="886a7-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="886a7-116">_formatpicture_</span><span class="sxs-lookup"><span data-stu-id="886a7-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="886a7-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="886a7-117">Required</span></span>  <br/> |<span data-ttu-id="886a7-118">**String**</span><span class="sxs-lookup"><span data-stu-id="886a7-118">**String**</span></span> <br/> |<span data-ttu-id="886a7-119">Изображение формата, используемая для фоматации строки.</span><span class="sxs-lookup"><span data-stu-id="886a7-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="886a7-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="886a7-120">Return value</span></span>

<span data-ttu-id="886a7-121">String</span><span class="sxs-lookup"><span data-stu-id="886a7-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="886a7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="886a7-122">Remarks</span></span>

<span data-ttu-id="886a7-123">Тип выражения и тип, указанный в изображении формата, регулируют поведение возвращенной строки.</span><span class="sxs-lookup"><span data-stu-id="886a7-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="886a7-124">Формат  _должен_ быть соответствующим типу выражения.</span><span class="sxs-lookup"><span data-stu-id="886a7-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="886a7-125">Дополнительные сведения о том, как указать изображения формата, см. в [рисунках формата.](about-format-pictures.md)</span><span class="sxs-lookup"><span data-stu-id="886a7-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="886a7-126">Возвращает ошибку, если  результат выражения и тип, ожидаемый в _formatpicture,_ имеют другой вид или если в _formatpicture_ имеются ошибки синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="886a7-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="886a7-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="886a7-127">Example 1</span></span>

<span data-ttu-id="886a7-128">FORMAT (1cm/4, "0.000 u")</span><span class="sxs-lookup"><span data-stu-id="886a7-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="886a7-129">Возвращает "0,250 см".</span><span class="sxs-lookup"><span data-stu-id="886a7-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="886a7-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="886a7-130">Example 2</span></span>

<span data-ttu-id="886a7-131">FORMAT (1cm/4, "0.00 U")</span><span class="sxs-lookup"><span data-stu-id="886a7-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="886a7-132">Возвращает "0.25 CM".</span><span class="sxs-lookup"><span data-stu-id="886a7-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="886a7-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="886a7-133">Example 3</span></span>

<span data-ttu-id="886a7-134">FORMAT (1cm/4, "0.0 u")</span><span class="sxs-lookup"><span data-stu-id="886a7-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="886a7-135">Возвращает "0,3 см".</span><span class="sxs-lookup"><span data-stu-id="886a7-135">Returns "0.3 cm."</span></span>
  

