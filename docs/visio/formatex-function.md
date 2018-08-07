---
title: Функция FORMATEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Возвращает результат выражения, вычисленное в srcUnit как строку отформатированное в соответствии с формату в dstUnit.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813823"
---
# <a name="formatex-function"></a><span data-ttu-id="d0a08-103">Функция FORMATEX</span><span class="sxs-lookup"><span data-stu-id="d0a08-103">FORMATEX Function</span></span>

<span data-ttu-id="d0a08-104">Возвращает результат выражения, вычисленное в srcUnit как строку отформатированное в соответствии с формату в dstUnit.</span><span class="sxs-lookup"><span data-stu-id="d0a08-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d0a08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0a08-105">Syntax</span></span>

<span data-ttu-id="d0a08-106">FORMATEX (** *выражение* **, "** *Формат* **", [** *srcUnit* **], [** *dstUnit* **], [** *langID* **] [, ** *calID* **])</span><span class="sxs-lookup"><span data-stu-id="d0a08-106">FORMATEX(** *expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0a08-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0a08-107">Parameters</span></span>

|<span data-ttu-id="d0a08-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d0a08-108">**Name**</span></span>|<span data-ttu-id="d0a08-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="d0a08-109">**Required/Optional**</span></span>|<span data-ttu-id="d0a08-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d0a08-110">**Data Type**</span></span>|<span data-ttu-id="d0a08-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d0a08-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0a08-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="d0a08-112">_expression_</span></span> <br/> |<span data-ttu-id="d0a08-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d0a08-113">Required</span></span>  <br/> |<span data-ttu-id="d0a08-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d0a08-114">**String**</span></span> <br/> |<span data-ttu-id="d0a08-115">Комбинация константы, операторы, функции и ссылки на ячейки таблицы свойств фигуры, которая приводит к значение.</span><span class="sxs-lookup"><span data-stu-id="d0a08-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="d0a08-116">_format_</span><span class="sxs-lookup"><span data-stu-id="d0a08-116">_format_</span></span> <br/> |<span data-ttu-id="d0a08-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d0a08-117">Required</span></span>  <br/> |<span data-ttu-id="d0a08-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d0a08-118">**String**</span></span> <br/> |<span data-ttu-id="d0a08-119">Формат рисунка, который используется для форматирования строки.</span><span class="sxs-lookup"><span data-stu-id="d0a08-119">The format picture used to format the string.</span></span> <span data-ttu-id="d0a08-120">Дополнительные сведения о формате изображения содержатся в разделе [О формате изображения](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="d0a08-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="d0a08-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="d0a08-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="d0a08-122">Optional</span><span class="sxs-lookup"><span data-stu-id="d0a08-122">Optional</span></span>  <br/> |<span data-ttu-id="d0a08-123">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d0a08-123">**String**</span></span> <br/> | <span data-ttu-id="d0a08-124">Единицы, используемые для оценки выражения (в, cm и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d0a08-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="d0a08-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="d0a08-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="d0a08-126">Optional</span><span class="sxs-lookup"><span data-stu-id="d0a08-126">Optional</span></span>  <br/> |<span data-ttu-id="d0a08-127">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d0a08-127">**String**</span></span> <br/> |<span data-ttu-id="d0a08-128">Единицы измерения для результата выражения (в, cm и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d0a08-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="d0a08-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="d0a08-129">_langID_</span></span> <br/> |<span data-ttu-id="d0a08-130">Optional</span><span class="sxs-lookup"><span data-stu-id="d0a08-130">Optional</span></span>  <br/> |<span data-ttu-id="d0a08-131">**Число**</span><span class="sxs-lookup"><span data-stu-id="d0a08-131">**Number**</span></span> <br/> |<span data-ttu-id="d0a08-132">Язык, используемый при форматировании изображений даты и времени системы Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d0a08-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="d0a08-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="d0a08-133">_calID_</span></span> <br/> |<span data-ttu-id="d0a08-134">Optional</span><span class="sxs-lookup"><span data-stu-id="d0a08-134">Optional</span></span>  <br/> |<span data-ttu-id="d0a08-135">**Число**</span><span class="sxs-lookup"><span data-stu-id="d0a08-135">**Number**</span></span> <br/> |<span data-ttu-id="d0a08-136">Календарь, используемый при форматировании изображений даты и времени системы Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d0a08-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d0a08-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="d0a08-138">Строка</span><span class="sxs-lookup"><span data-stu-id="d0a08-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0a08-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0a08-139">Remarks</span></span>

<span data-ttu-id="d0a08-140">Тип выражения и тип которых указан формат рисунка управляют поведением Возвращенная строка.</span><span class="sxs-lookup"><span data-stu-id="d0a08-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="d0a08-141">Формат значения соответствуют типу выражения.</span><span class="sxs-lookup"><span data-stu-id="d0a08-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="d0a08-142">Аргумент srcUnit используется для масштабирования результатов нетипизированного выражения, такие как 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="d0a08-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="d0a08-143">Если результат выражения явного типа, например 3 ft + 8 ft, то srcUnit игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d0a08-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="d0a08-144">Аргумент dstUnit используется для указания единицы измерения, используемые для форматированного результата.</span><span class="sxs-lookup"><span data-stu-id="d0a08-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="d0a08-145">Если dstUnit не указан, будут использоваться единиц измерения для результата выражения.</span><span class="sxs-lookup"><span data-stu-id="d0a08-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="d0a08-146">Возвращает ошибку, если результат выражения и типа в формате разного рода при наличии синтаксических ошибок в формате или не распознает единицы передается как srcUnit или dstUnit.</span><span class="sxs-lookup"><span data-stu-id="d0a08-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="d0a08-147">Пример</span><span class="sxs-lookup"><span data-stu-id="d0a08-147">Example</span></span>

<span data-ttu-id="d0a08-148">FORMATEX (5.5, "0,00 u», «cm», «ft")</span><span class="sxs-lookup"><span data-stu-id="d0a08-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="d0a08-149">Возвращает 0,18 футов.</span><span class="sxs-lookup"><span data-stu-id="d0a08-149">Returns 0.18 feet.</span></span> 
  

