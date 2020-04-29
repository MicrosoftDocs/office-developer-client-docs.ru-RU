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
description: Возвращает результат выражения, вычисленный в Сркунит в виде строки, отформатированной в соответствии с форматом, выраженным в Дстунит.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430968"
---
# <a name="formatex-function"></a><span data-ttu-id="15f90-103">Функция FORMATEX</span><span class="sxs-lookup"><span data-stu-id="15f90-103">FORMATEX Function</span></span>

<span data-ttu-id="15f90-104">Возвращает результат выражения, вычисленный в Сркунит в виде строки, отформатированной в соответствии с форматом, выраженным в Дстунит.</span><span class="sxs-lookup"><span data-stu-id="15f90-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="15f90-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15f90-105">Syntax</span></span>

<span data-ttu-id="15f90-106">FORMATEX (\* \* *Expression* \* *, "* \* *Format* \* *", [* \* *сркунит* \* *], [* \* *дстунит* \* *], [* \* *langID* \* \*] [, \* \* *Калид* \* \*])</span><span class="sxs-lookup"><span data-stu-id="15f90-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="15f90-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="15f90-107">Parameters</span></span>

|<span data-ttu-id="15f90-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="15f90-108">**Name**</span></span>|<span data-ttu-id="15f90-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="15f90-109">**Required/Optional**</span></span>|<span data-ttu-id="15f90-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="15f90-110">**Data Type**</span></span>|<span data-ttu-id="15f90-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="15f90-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="15f90-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="15f90-112">_expression_</span></span> <br/> |<span data-ttu-id="15f90-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="15f90-113">Required</span></span>  <br/> |<span data-ttu-id="15f90-114">**String**</span><span class="sxs-lookup"><span data-stu-id="15f90-114">**String**</span></span> <br/> |<span data-ttu-id="15f90-115">Сочетание констант, операторов, функций и ссылок на ячейки таблицы свойств фигуры, в результате чего получается значение.</span><span class="sxs-lookup"><span data-stu-id="15f90-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="15f90-116">_format_</span><span class="sxs-lookup"><span data-stu-id="15f90-116">_format_</span></span> <br/> |<span data-ttu-id="15f90-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="15f90-117">Required</span></span>  <br/> |<span data-ttu-id="15f90-118">**String**</span><span class="sxs-lookup"><span data-stu-id="15f90-118">**String**</span></span> <br/> |<span data-ttu-id="15f90-119">Формат рисунка, используемый для форматирования строки.</span><span class="sxs-lookup"><span data-stu-id="15f90-119">The format picture used to format the string.</span></span> <span data-ttu-id="15f90-120">Дополнительные сведения о форматах [рисунков см.](about-format-pictures.md)</span><span class="sxs-lookup"><span data-stu-id="15f90-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="15f90-121">_сркунит_</span><span class="sxs-lookup"><span data-stu-id="15f90-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="15f90-122">Необязательна</span><span class="sxs-lookup"><span data-stu-id="15f90-122">Optional</span></span>  <br/> |<span data-ttu-id="15f90-123">**String**</span><span class="sxs-lookup"><span data-stu-id="15f90-123">**String**</span></span> <br/> | <span data-ttu-id="15f90-124">Единицы измерения, используемые для вычисления выражения (в, cm и т. д.).</span><span class="sxs-lookup"><span data-stu-id="15f90-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="15f90-125">_дстунит_</span><span class="sxs-lookup"><span data-stu-id="15f90-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="15f90-126">Необязательна</span><span class="sxs-lookup"><span data-stu-id="15f90-126">Optional</span></span>  <br/> |<span data-ttu-id="15f90-127">**String**</span><span class="sxs-lookup"><span data-stu-id="15f90-127">**String**</span></span> <br/> |<span data-ttu-id="15f90-128">Единица, используемая для результата выражения (in, cm и т. д.).</span><span class="sxs-lookup"><span data-stu-id="15f90-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="15f90-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="15f90-129">_langID_</span></span> <br/> |<span data-ttu-id="15f90-130">Необязательна</span><span class="sxs-lookup"><span data-stu-id="15f90-130">Optional</span></span>  <br/> |<span data-ttu-id="15f90-131">**Number**</span><span class="sxs-lookup"><span data-stu-id="15f90-131">**Number**</span></span> <br/> |<span data-ttu-id="15f90-132">Язык, используемый при форматировании изображений даты и времени в системе Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="15f90-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="15f90-133">_калид_</span><span class="sxs-lookup"><span data-stu-id="15f90-133">_calID_</span></span> <br/> |<span data-ttu-id="15f90-134">Необязательна</span><span class="sxs-lookup"><span data-stu-id="15f90-134">Optional</span></span>  <br/> |<span data-ttu-id="15f90-135">**Number**</span><span class="sxs-lookup"><span data-stu-id="15f90-135">**Number**</span></span> <br/> |<span data-ttu-id="15f90-136">Календарь, используемый при форматировании изображений даты и времени в системе Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="15f90-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="15f90-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15f90-137">Return value</span></span>

<span data-ttu-id="15f90-138">String</span><span class="sxs-lookup"><span data-stu-id="15f90-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15f90-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="15f90-139">Remarks</span></span>

<span data-ttu-id="15f90-140">Тип выражения и тип, указанный в формате рисунок, управляют поведением возвращенной строки.</span><span class="sxs-lookup"><span data-stu-id="15f90-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="15f90-141">Формат должен соответствовать типу выражения.</span><span class="sxs-lookup"><span data-stu-id="15f90-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="15f90-142">Аргумент Сркунит используется для масштабирования нетипизированных результатов выражения, например 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="15f90-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="15f90-143">Если результат выражения имеет явный тип, например 3 фт + 8 ФТ, то Сркунит игнорируется.</span><span class="sxs-lookup"><span data-stu-id="15f90-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="15f90-144">Аргумент Дстунит используется для указания единиц измерения, используемых для отформатированного результата.</span><span class="sxs-lookup"><span data-stu-id="15f90-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="15f90-145">Если Дстунит не указан, используются единицы измерения результата в выражении.</span><span class="sxs-lookup"><span data-stu-id="15f90-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="15f90-146">Возвращает ошибку, если результат выражения и тип, ожидаемый в формате, имеют другой тип, если в формате есть синтаксические ошибки, или если он не распознает единицы, переданные как Сркунит или Дстунит.</span><span class="sxs-lookup"><span data-stu-id="15f90-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="15f90-147">Пример</span><span class="sxs-lookup"><span data-stu-id="15f90-147">Example</span></span>

<span data-ttu-id="15f90-148">FORMATEX (5,5, "0,00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="15f90-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="15f90-149">Возвращает 0,18 метров.</span><span class="sxs-lookup"><span data-stu-id="15f90-149">Returns 0.18 feet.</span></span> 
  

