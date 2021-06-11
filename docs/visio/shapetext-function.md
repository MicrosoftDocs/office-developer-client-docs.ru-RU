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
# <a name="shapetext-function"></a><span data-ttu-id="5d7a5-103">Функция SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="5d7a5-103">SHAPETEXT Function</span></span>

<span data-ttu-id="5d7a5-104">Получает текст из фигуры.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5d7a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d7a5-105">Syntax</span></span>

<span data-ttu-id="5d7a5-106">SHAPETEXT (\*\* *shapename! TheText* \*\* \*\* *[,flag]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5d7a5-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d7a5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d7a5-107">Parameters</span></span>

|<span data-ttu-id="5d7a5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-108">**Name**</span></span>|<span data-ttu-id="5d7a5-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-109">**Required/Optional**</span></span>|<span data-ttu-id="5d7a5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-110">**Data Type**</span></span>|<span data-ttu-id="5d7a5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d7a5-112">_shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="5d7a5-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="5d7a5-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5d7a5-113">Required</span></span>  <br/> ||<span data-ttu-id="5d7a5-114">Ссылка на ячейку с именем TheText в целевой форме.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="5d7a5-115">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="5d7a5-115">_Shapename!_</span></span> <span data-ttu-id="5d7a5-116">это имя фигуры, из которой нужно получить текст.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="5d7a5-117">_flag_</span><span class="sxs-lookup"><span data-stu-id="5d7a5-117">_flag_</span></span> <br/> |<span data-ttu-id="5d7a5-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="5d7a5-118">Optional</span></span>  <br/> |<span data-ttu-id="5d7a5-119">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-119">**Numeric**</span></span> <br/> |<span data-ttu-id="5d7a5-120">Немного, который указывает формат текста.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="5d7a5-121">Флаг по умолчанию (0) показывает текст точно так, как он показан в форме.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5d7a5-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d7a5-122">Return value</span></span>

<span data-ttu-id="5d7a5-123">String</span><span class="sxs-lookup"><span data-stu-id="5d7a5-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d7a5-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d7a5-124">Remarks</span></span>

<span data-ttu-id="5d7a5-125">Вы можете использовать любое сочетание следующих флагов с функцией SHAPETEXT.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="5d7a5-126">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-126">**Flag**</span></span>|<span data-ttu-id="5d7a5-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d7a5-128">0</span><span class="sxs-lookup"><span data-stu-id="5d7a5-128">0</span></span>  <br/> |<span data-ttu-id="5d7a5-129">Показать текст точно так, как показано в форме.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-130">1</span><span class="sxs-lookup"><span data-stu-id="5d7a5-130">1</span></span>  <br/> |<span data-ttu-id="5d7a5-131">Включай дискреционные дефисы.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-132">2</span><span class="sxs-lookup"><span data-stu-id="5d7a5-132">2</span></span>  <br/> |<span data-ttu-id="5d7a5-133">Не включайте расширенный текст в поля.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-134">4 </span><span class="sxs-lookup"><span data-stu-id="5d7a5-134">4</span></span>  <br/> |<span data-ttu-id="5d7a5-135">Преобразование вкладок в одно пространство.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-136">8 </span><span class="sxs-lookup"><span data-stu-id="5d7a5-136">8</span></span>  <br/> |<span data-ttu-id="5d7a5-137">Преобразование вкладок в набор пробелов.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-138">16 </span><span class="sxs-lookup"><span data-stu-id="5d7a5-138">16</span></span>  <br/> |<span data-ttu-id="5d7a5-139">Преобразование возвращаемой кареты и каналов строки в пробелы.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-140">32</span><span class="sxs-lookup"><span data-stu-id="5d7a5-140">32</span></span>  <br/> |<span data-ttu-id="5d7a5-141">Преобразование кавычка опечатщика в обычные кавычка.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="5d7a5-142">64</span><span class="sxs-lookup"><span data-stu-id="5d7a5-142">64</span></span>  <br/> |<span data-ttu-id="5d7a5-143">Преобразование прилегающего белого пространства в одно пространство.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="5d7a5-144">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d7a5-144">Example 1</span></span>

<span data-ttu-id="5d7a5-145">SHAPETEXT(sheetN!theText)</span><span class="sxs-lookup"><span data-stu-id="5d7a5-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="5d7a5-146">Возвращает текст фигуры с именем sheetN, точно так же, как показано в фигуре.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5d7a5-147">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d7a5-147">Example 2</span></span>

<span data-ttu-id="5d7a5-148">SHAPETEXT (theText)</span><span class="sxs-lookup"><span data-stu-id="5d7a5-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="5d7a5-149">Возвращает текст текущей фигуры точно так, как показано в фигуре.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5d7a5-150">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5d7a5-150">Example 3</span></span>

<span data-ttu-id="5d7a5-151">SHAPETEXT (theText, 84)</span><span class="sxs-lookup"><span data-stu-id="5d7a5-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="5d7a5-152">Возвращает текст текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-152">Returns the text of the current shape.</span></span> <span data-ttu-id="5d7a5-153">Кроме того, он преобразует прилегающее белое пространство в одно пространство (64), преобразует возвраты вагона и каналы строки в пробелы (16) и преобразует вкладки в одно пространство (4).</span><span class="sxs-lookup"><span data-stu-id="5d7a5-153">It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4).</span></span> <span data-ttu-id="5d7a5-154">Сумма этих флагов — 84.</span><span class="sxs-lookup"><span data-stu-id="5d7a5-154">The sum of these flags is 84.</span></span>
  

