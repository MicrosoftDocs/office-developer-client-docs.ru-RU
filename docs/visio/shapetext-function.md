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
# <a name="shapetext-function"></a><span data-ttu-id="3ab79-103">Функция SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="3ab79-103">SHAPETEXT Function</span></span>

<span data-ttu-id="3ab79-104">Получает текст из фигуры.</span><span class="sxs-lookup"><span data-stu-id="3ab79-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3ab79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ab79-105">Syntax</span></span>

<span data-ttu-id="3ab79-106">SHAPETEXT (\* \* *шапенаме! TheText* \* \* \* \* *[, флаг]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3ab79-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3ab79-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ab79-107">Parameters</span></span>

|<span data-ttu-id="3ab79-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3ab79-108">**Name**</span></span>|<span data-ttu-id="3ab79-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3ab79-109">**Required/Optional**</span></span>|<span data-ttu-id="3ab79-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3ab79-110">**Data Type**</span></span>|<span data-ttu-id="3ab79-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ab79-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3ab79-112">_шапенаме! TheText_</span><span class="sxs-lookup"><span data-stu-id="3ab79-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="3ab79-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3ab79-113">Required</span></span>  <br/> ||<span data-ttu-id="3ab79-114">Ссылка на ячейку с именем TheText в целевой фигуре.</span><span class="sxs-lookup"><span data-stu-id="3ab79-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="3ab79-115">_Шапенаме!_</span><span class="sxs-lookup"><span data-stu-id="3ab79-115">_Shapename!_</span></span> <span data-ttu-id="3ab79-116">— имя фигуры, из которой требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="3ab79-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="3ab79-117">_flag_</span><span class="sxs-lookup"><span data-stu-id="3ab79-117">_flag_</span></span> <br/> |<span data-ttu-id="3ab79-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="3ab79-118">Optional</span></span>  <br/> |<span data-ttu-id="3ab79-119">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3ab79-119">**Numeric**</span></span> <br/> |<span data-ttu-id="3ab79-120">Бит, указывающий формат текста.</span><span class="sxs-lookup"><span data-stu-id="3ab79-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="3ab79-121">По умолчанию в качестве значения флага (0) текст отображается точно так же, как и в фигуре.</span><span class="sxs-lookup"><span data-stu-id="3ab79-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3ab79-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ab79-122">Return value</span></span>

<span data-ttu-id="3ab79-123">String</span><span class="sxs-lookup"><span data-stu-id="3ab79-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ab79-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ab79-124">Remarks</span></span>

<span data-ttu-id="3ab79-125">С помощью функции SHAPETEXT можно использовать любое сочетание следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="3ab79-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="3ab79-126">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="3ab79-126">**Flag**</span></span>|<span data-ttu-id="3ab79-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ab79-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ab79-128">нуль</span><span class="sxs-lookup"><span data-stu-id="3ab79-128">0</span></span>  <br/> |<span data-ttu-id="3ab79-129">Отображение текста в точности так, как показано в фигуре.</span><span class="sxs-lookup"><span data-stu-id="3ab79-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="3ab79-130">1,1</span><span class="sxs-lookup"><span data-stu-id="3ab79-130">1</span></span>  <br/> |<span data-ttu-id="3ab79-131">Включение дискреционных переносов.</span><span class="sxs-lookup"><span data-stu-id="3ab79-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="3ab79-132">2</span><span class="sxs-lookup"><span data-stu-id="3ab79-132">2</span></span>  <br/> |<span data-ttu-id="3ab79-133">Не включайте развернутый текст в поля.</span><span class="sxs-lookup"><span data-stu-id="3ab79-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="3ab79-134">SP4</span><span class="sxs-lookup"><span data-stu-id="3ab79-134">4</span></span>  <br/> |<span data-ttu-id="3ab79-135">Преобразование вкладок в один пробел.</span><span class="sxs-lookup"><span data-stu-id="3ab79-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="3ab79-136">8,5</span><span class="sxs-lookup"><span data-stu-id="3ab79-136">8</span></span>  <br/> |<span data-ttu-id="3ab79-137">Преобразование вкладок в набор пробелов.</span><span class="sxs-lookup"><span data-stu-id="3ab79-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="3ab79-138">16 </span><span class="sxs-lookup"><span data-stu-id="3ab79-138">16</span></span>  <br/> |<span data-ttu-id="3ab79-139">Преобразование символов возврата каретки и перевода строки в пробелы.</span><span class="sxs-lookup"><span data-stu-id="3ab79-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="3ab79-140">32</span><span class="sxs-lookup"><span data-stu-id="3ab79-140">32</span></span>  <br/> |<span data-ttu-id="3ab79-141">ПреОбразуйте типографские кавычки в обычные кавычки.</span><span class="sxs-lookup"><span data-stu-id="3ab79-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="3ab79-142">64</span><span class="sxs-lookup"><span data-stu-id="3ab79-142">64</span></span>  <br/> |<span data-ttu-id="3ab79-143">ПреОбразуйте соседние пробелы в один пробел.</span><span class="sxs-lookup"><span data-stu-id="3ab79-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="3ab79-144">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ab79-144">Example 1</span></span>

<span data-ttu-id="3ab79-145">SHAPETEXT (Шитн! theText)</span><span class="sxs-lookup"><span data-stu-id="3ab79-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="3ab79-146">Возвращает текст фигуры с именем Шитн, точно так же, как показано в фигуре.</span><span class="sxs-lookup"><span data-stu-id="3ab79-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3ab79-147">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3ab79-147">Example 2</span></span>

<span data-ttu-id="3ab79-148">SHAPETEXT (theText)</span><span class="sxs-lookup"><span data-stu-id="3ab79-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="3ab79-149">Возвращает текст текущей фигуры точно так же, как показано в фигуре.</span><span class="sxs-lookup"><span data-stu-id="3ab79-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3ab79-150">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3ab79-150">Example 3</span></span>

<span data-ttu-id="3ab79-151">SHAPETEXT (theText, 84)</span><span class="sxs-lookup"><span data-stu-id="3ab79-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="3ab79-152">Возвращает текст текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="3ab79-152">Returns the text of the current shape.</span></span> <span data-ttu-id="3ab79-153">Кроме того, он преобразует соседние пробелы в один пробел (64), преобразует символы возврата каретки и перевода строки в пробелы (16) и преобразует знаки табуляции в один пробел (4).</span><span class="sxs-lookup"><span data-stu-id="3ab79-153">It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4).</span></span> <span data-ttu-id="3ab79-154">Сумма этих флагов равна 84.</span><span class="sxs-lookup"><span data-stu-id="3ab79-154">The sum of these flags is 84.</span></span>
  

