---
title: Функция SHAPETEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Получает текст из фигуры.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419347"
---
# <a name="shapetext-function"></a><span data-ttu-id="bf3f7-103">Функция SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="bf3f7-103">SHAPETEXT Function</span></span>

<span data-ttu-id="bf3f7-104">Получает текст из фигуры.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bf3f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf3f7-105">Syntax</span></span>

<span data-ttu-id="bf3f7-106">SHAPETEXT (\*\* *shapename! TheText* \*\* \*\* *[,flag]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="bf3f7-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bf3f7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf3f7-107">Parameters</span></span>

|<span data-ttu-id="bf3f7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-108">**Name**</span></span>|<span data-ttu-id="bf3f7-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-109">**Required/Optional**</span></span>|<span data-ttu-id="bf3f7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-110">**Data Type**</span></span>|<span data-ttu-id="bf3f7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bf3f7-112">_shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="bf3f7-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="bf3f7-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="bf3f7-113">Required</span></span>  <br/> ||<span data-ttu-id="bf3f7-114">Ссылка на ячейку с именем TheText в целевой фигуре.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="bf3f7-115">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="bf3f7-115">_Shapename!_</span></span> <span data-ttu-id="bf3f7-116">— имя фигуры, из которой вы хотите получить текст.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="bf3f7-117">_flag_</span><span class="sxs-lookup"><span data-stu-id="bf3f7-117">_flag_</span></span> <br/> |<span data-ttu-id="bf3f7-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="bf3f7-118">Optional</span></span>  <br/> |<span data-ttu-id="bf3f7-119">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-119">**Numeric**</span></span> <br/> |<span data-ttu-id="bf3f7-120">Бит, который определяет формат текста.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="bf3f7-121">Флаг по умолчанию (0) показывает текст точно так, как он отображается в фигуре.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bf3f7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf3f7-122">Return value</span></span>

<span data-ttu-id="bf3f7-123">String</span><span class="sxs-lookup"><span data-stu-id="bf3f7-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf3f7-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf3f7-124">Remarks</span></span>

<span data-ttu-id="bf3f7-125">С функцией SHAPETEXT можно использовать любое сочетание следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="bf3f7-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-126">**Flag**</span></span>|<span data-ttu-id="bf3f7-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf3f7-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf3f7-128">0</span><span class="sxs-lookup"><span data-stu-id="bf3f7-128">0</span></span>  <br/> |<span data-ttu-id="bf3f7-129">Отобразить текст точно так, как показано в фигуре.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-130">1 </span><span class="sxs-lookup"><span data-stu-id="bf3f7-130">1</span></span>  <br/> |<span data-ttu-id="bf3f7-131">Включаем дискреционные дефисы.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-132">2 </span><span class="sxs-lookup"><span data-stu-id="bf3f7-132">2</span></span>  <br/> |<span data-ttu-id="bf3f7-133">Не включайте расширенный текст в поля.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-134">4 </span><span class="sxs-lookup"><span data-stu-id="bf3f7-134">4</span></span>  <br/> |<span data-ttu-id="bf3f7-135">Преобразование вкладок в одно пространство.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-136">8 </span><span class="sxs-lookup"><span data-stu-id="bf3f7-136">8</span></span>  <br/> |<span data-ttu-id="bf3f7-137">Преобразование вкладок в набор пробелов.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-138">16 </span><span class="sxs-lookup"><span data-stu-id="bf3f7-138">16</span></span>  <br/> |<span data-ttu-id="bf3f7-139">Преобразуем возвраты каретки и переводимые строки в пробелы.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-140">32</span><span class="sxs-lookup"><span data-stu-id="bf3f7-140">32</span></span>  <br/> |<span data-ttu-id="bf3f7-141">Преобразуйте кавычка опечатки в обычные кавычка.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="bf3f7-142">64</span><span class="sxs-lookup"><span data-stu-id="bf3f7-142">64</span></span>  <br/> |<span data-ttu-id="bf3f7-143">Преобразуем смежный пробел в одно пространство.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="bf3f7-144">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf3f7-144">Example 1</span></span>

<span data-ttu-id="bf3f7-145">SHAPETEXT(sheetN!theText)</span><span class="sxs-lookup"><span data-stu-id="bf3f7-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="bf3f7-146">Возвращает текст фигуры с именем sheetN точно так же, как он показан в фигуре.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bf3f7-147">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bf3f7-147">Example 2</span></span>

<span data-ttu-id="bf3f7-148">SHAPETEXT(theText)</span><span class="sxs-lookup"><span data-stu-id="bf3f7-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="bf3f7-149">Возвращает текст текущей фигуры точно так же, как он показан в фигуре.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bf3f7-150">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bf3f7-150">Example 3</span></span>

<span data-ttu-id="bf3f7-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="bf3f7-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="bf3f7-152">Возвращает текст текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-152">Returns the text of the current shape.</span></span> <span data-ttu-id="bf3f7-153">Он также преобразует смежное пробел в одно пространство (64), преобразует возврат каретки и каналы строк в пробелы (16) и преобразует вкладки в одно пространство (4).</span><span class="sxs-lookup"><span data-stu-id="bf3f7-153">It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4).</span></span> <span data-ttu-id="bf3f7-154">Сумма этих флагов составляет 84.</span><span class="sxs-lookup"><span data-stu-id="bf3f7-154">The sum of these flags is 84.</span></span>
  

