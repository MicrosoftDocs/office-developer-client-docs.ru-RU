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
description: Возвращает результат выражения, оцениваемого в srcUnit как строка, отформатированная в соответствии с форматом, выраженным в dstUnit.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430968"
---
# <a name="formatex-function"></a><span data-ttu-id="8abba-103">Функция FORMATEX</span><span class="sxs-lookup"><span data-stu-id="8abba-103">FORMATEX Function</span></span>

<span data-ttu-id="8abba-104">Возвращает результат выражения, оцениваемого в srcUnit как строка, отформатированная в соответствии с форматом, выраженным в dstUnit.</span><span class="sxs-lookup"><span data-stu-id="8abba-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8abba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8abba-105">Syntax</span></span>

<span data-ttu-id="8abba-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="8abba-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8abba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8abba-107">Parameters</span></span>

|<span data-ttu-id="8abba-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8abba-108">**Name**</span></span>|<span data-ttu-id="8abba-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8abba-109">**Required/Optional**</span></span>|<span data-ttu-id="8abba-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8abba-110">**Data Type**</span></span>|<span data-ttu-id="8abba-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8abba-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8abba-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="8abba-112">_expression_</span></span> <br/> |<span data-ttu-id="8abba-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="8abba-113">Required</span></span>  <br/> |<span data-ttu-id="8abba-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="8abba-114">**String**</span></span> <br/> |<span data-ttu-id="8abba-115">Сочетание констант, операторов, функций и ссылок на ячейки ShapeSheet, которое приводит к значению.</span><span class="sxs-lookup"><span data-stu-id="8abba-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="8abba-116">_format_</span><span class="sxs-lookup"><span data-stu-id="8abba-116">_format_</span></span> <br/> |<span data-ttu-id="8abba-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="8abba-117">Required</span></span>  <br/> |<span data-ttu-id="8abba-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="8abba-118">**String**</span></span> <br/> |<span data-ttu-id="8abba-119">Изображение формата, используемая для формата строки.</span><span class="sxs-lookup"><span data-stu-id="8abba-119">The format picture used to format the string.</span></span> <span data-ttu-id="8abba-120">Дополнительные сведения о формате изображений см. в [сведениях о формате изображений.](about-format-pictures.md)</span><span class="sxs-lookup"><span data-stu-id="8abba-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="8abba-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="8abba-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="8abba-122">Необязательна</span><span class="sxs-lookup"><span data-stu-id="8abba-122">Optional</span></span>  <br/> |<span data-ttu-id="8abba-123">**Строка**</span><span class="sxs-lookup"><span data-stu-id="8abba-123">**String**</span></span> <br/> | <span data-ttu-id="8abba-124">Единицы, используемые для оценки выражения (в, cm и так далее).</span><span class="sxs-lookup"><span data-stu-id="8abba-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="8abba-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="8abba-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="8abba-126">Необязательна</span><span class="sxs-lookup"><span data-stu-id="8abba-126">Optional</span></span>  <br/> |<span data-ttu-id="8abba-127">**Строка**</span><span class="sxs-lookup"><span data-stu-id="8abba-127">**String**</span></span> <br/> |<span data-ttu-id="8abba-128">Единицы, которые будут использовать для результата выражения (в, cm и так далее).</span><span class="sxs-lookup"><span data-stu-id="8abba-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="8abba-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="8abba-129">_langID_</span></span> <br/> |<span data-ttu-id="8abba-130">Необязательна</span><span class="sxs-lookup"><span data-stu-id="8abba-130">Optional</span></span>  <br/> |<span data-ttu-id="8abba-131">**Number**</span><span class="sxs-lookup"><span data-stu-id="8abba-131">**Number**</span></span> <br/> |<span data-ttu-id="8abba-132">Язык, используемый при Microsoft Office системных рисунков даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8abba-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="8abba-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="8abba-133">_calID_</span></span> <br/> |<span data-ttu-id="8abba-134">Необязательна</span><span class="sxs-lookup"><span data-stu-id="8abba-134">Optional</span></span>  <br/> |<span data-ttu-id="8abba-135">**Number**</span><span class="sxs-lookup"><span data-stu-id="8abba-135">**Number**</span></span> <br/> |<span data-ttu-id="8abba-136">Календарь, используемый при Microsoft Office системных рисунков даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8abba-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8abba-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8abba-137">Return value</span></span>

<span data-ttu-id="8abba-138">String</span><span class="sxs-lookup"><span data-stu-id="8abba-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8abba-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="8abba-139">Remarks</span></span>

<span data-ttu-id="8abba-140">Тип выражения и тип, указанные в изображении формата, управляют поведением возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="8abba-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="8abba-141">Формат должен быть соответствующим типу выражения.</span><span class="sxs-lookup"><span data-stu-id="8abba-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="8abba-142">Аргумент srcUnit используется для масштабирования результатов нетипизированных выражений, например 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="8abba-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="8abba-143">Если результат выражения имеет явный тип, например 3 ft + 8 ft, srcUnit игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8abba-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="8abba-144">Аргумент dstUnit используется для указания единиц, используемых для отформатированный результат.</span><span class="sxs-lookup"><span data-stu-id="8abba-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="8abba-145">Если dstUnit не указан, используются единицы для результата выражения.</span><span class="sxs-lookup"><span data-stu-id="8abba-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="8abba-146">Возвращает ошибку, если результат выражения и тип, ожидаемый в формате, имеют другой вид, существуют ошибки синтаксиса в формате или если он не распознает единицы, переданные как srcUnit или dstUnit.</span><span class="sxs-lookup"><span data-stu-id="8abba-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="8abba-147">Пример</span><span class="sxs-lookup"><span data-stu-id="8abba-147">Example</span></span>

<span data-ttu-id="8abba-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="8abba-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="8abba-149">Возвращает 0,18 метров.</span><span class="sxs-lookup"><span data-stu-id="8abba-149">Returns 0.18 feet.</span></span> 
  

