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
description: Возвращает результат выражения в виде строки, отформатированное в соответствии с formatpicture.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813821"
---
# <a name="format-function"></a><span data-ttu-id="3890d-103">Функция FORMAT</span><span class="sxs-lookup"><span data-stu-id="3890d-103">FORMAT Function</span></span>

<span data-ttu-id="3890d-104">Возвращает результат _выражения_ в виде строки, отформатированное в соответствии с _formatpicture_.</span><span class="sxs-lookup"><span data-stu-id="3890d-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3890d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3890d-105">Syntax</span></span>

<span data-ttu-id="3890d-106">ФОРМАТ (** *выражение* **, "** *formatpicture* **")</span><span class="sxs-lookup"><span data-stu-id="3890d-106">FORMAT(** *expression* **," ** *formatpicture* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3890d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3890d-107">Parameters</span></span>

|<span data-ttu-id="3890d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3890d-108">**Name**</span></span>|<span data-ttu-id="3890d-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="3890d-109">**Required/Optional**</span></span>|<span data-ttu-id="3890d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3890d-110">**Data Type**</span></span>|<span data-ttu-id="3890d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3890d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3890d-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="3890d-112">_expression_</span></span> <br/> |<span data-ttu-id="3890d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3890d-113">Required</span></span>  <br/> |<span data-ttu-id="3890d-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3890d-114">**String**</span></span> <br/> |<span data-ttu-id="3890d-115">Комбинация константы, операторы, функции и ссылки на ячейки таблицы свойств фигуры, которая приводит к значение.</span><span class="sxs-lookup"><span data-stu-id="3890d-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="3890d-116">_formatpicture_</span><span class="sxs-lookup"><span data-stu-id="3890d-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="3890d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3890d-117">Required</span></span>  <br/> |<span data-ttu-id="3890d-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3890d-118">**String**</span></span> <br/> |<span data-ttu-id="3890d-119">Формат рисунка используется для fomat строки.</span><span class="sxs-lookup"><span data-stu-id="3890d-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3890d-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3890d-120">Return value</span></span>

<span data-ttu-id="3890d-121">Строка</span><span class="sxs-lookup"><span data-stu-id="3890d-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3890d-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="3890d-122">Remarks</span></span>

<span data-ttu-id="3890d-123">Тип выражения и тип которых указан формат рисунка управляют поведением Возвращенная строка.</span><span class="sxs-lookup"><span data-stu-id="3890d-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="3890d-124">_Formatpicture_ должен применяться в тип выражения.</span><span class="sxs-lookup"><span data-stu-id="3890d-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="3890d-125">Дополнительные сведения о задании форматирование рисунков можно [о формате изображений](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="3890d-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="3890d-126">Возвращает ошибку, если результат _выражения_ и типа в _formatpicture_ разного рода или при наличии синтаксических ошибок в _formatpicture_.</span><span class="sxs-lookup"><span data-stu-id="3890d-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="3890d-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3890d-127">Example 1</span></span>

<span data-ttu-id="3890d-128">ФОРМАТ (1cm/4 "0.000 u")</span><span class="sxs-lookup"><span data-stu-id="3890d-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="3890d-129">Возвращает «0,250 см.»</span><span class="sxs-lookup"><span data-stu-id="3890d-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3890d-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3890d-130">Example 2</span></span>

<span data-ttu-id="3890d-131">ФОРМАТ (1cm/4 "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="3890d-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="3890d-132">Возвращает «0,25 см.»</span><span class="sxs-lookup"><span data-stu-id="3890d-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3890d-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3890d-133">Example 3</span></span>

<span data-ttu-id="3890d-134">ФОРМАТ (1cm/4 "0.0 u")</span><span class="sxs-lookup"><span data-stu-id="3890d-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="3890d-135">Возвращает «0,3 см.»</span><span class="sxs-lookup"><span data-stu-id="3890d-135">Returns "0.3 cm."</span></span>
  

