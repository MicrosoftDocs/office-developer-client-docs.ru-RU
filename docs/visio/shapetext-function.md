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
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814816"
---
# <a name="shapetext-function"></a><span data-ttu-id="cdb82-103">Функция SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="cdb82-103">SHAPETEXT Function</span></span>

<span data-ttu-id="cdb82-104">Получает текст из фигуры.</span><span class="sxs-lookup"><span data-stu-id="cdb82-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cdb82-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdb82-105">Syntax</span></span>

<span data-ttu-id="cdb82-106">SHAPETEXT (** указанной фигуре *! TheText* ** ** *[, флаг]* **)</span><span class="sxs-lookup"><span data-stu-id="cdb82-106">SHAPETEXT (** *shapename!TheText* ** ** *[,flag]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cdb82-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdb82-107">Parameters</span></span>

|<span data-ttu-id="cdb82-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="cdb82-108">**Name**</span></span>|<span data-ttu-id="cdb82-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="cdb82-109">**Required/Optional**</span></span>|<span data-ttu-id="cdb82-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="cdb82-110">**Data Type**</span></span>|<span data-ttu-id="cdb82-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cdb82-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cdb82-112">_указанной фигуре! TheText_</span><span class="sxs-lookup"><span data-stu-id="cdb82-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="cdb82-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cdb82-113">Required</span></span>  <br/> ||<span data-ttu-id="cdb82-114">Ссылка на ячейку с именем TheText в конечную фигуру.</span><span class="sxs-lookup"><span data-stu-id="cdb82-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="cdb82-115">_Указанной фигуре!_</span><span class="sxs-lookup"><span data-stu-id="cdb82-115">_Shapename!_</span></span> <span data-ttu-id="cdb82-116">— Это имя фигуры, из которого требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="cdb82-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="cdb82-117">_флаг_</span><span class="sxs-lookup"><span data-stu-id="cdb82-117">_flag_</span></span> <br/> |<span data-ttu-id="cdb82-118">Optional</span><span class="sxs-lookup"><span data-stu-id="cdb82-118">Optional</span></span>  <br/> |<span data-ttu-id="cdb82-119">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="cdb82-119">**Numeric**</span></span> <br/> |<span data-ttu-id="cdb82-120">Бит, который определяет формат текста.</span><span class="sxs-lookup"><span data-stu-id="cdb82-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="cdb82-121">Флаг по умолчанию (0) отображается текст точно так, как он отображается в форме.</span><span class="sxs-lookup"><span data-stu-id="cdb82-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cdb82-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cdb82-122">Return value</span></span>

<span data-ttu-id="cdb82-123">Строка</span><span class="sxs-lookup"><span data-stu-id="cdb82-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdb82-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="cdb82-124">Remarks</span></span>

<span data-ttu-id="cdb82-125">Можно использовать любое сочетание следующих флагов с помощью функции SHAPETEXT.</span><span class="sxs-lookup"><span data-stu-id="cdb82-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="cdb82-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="cdb82-126">**Flag**</span></span>|<span data-ttu-id="cdb82-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cdb82-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdb82-128">0</span><span class="sxs-lookup"><span data-stu-id="cdb82-128">0</span></span>  <br/> |<span data-ttu-id="cdb82-129">Отображение текста так же, как показано в форму.</span><span class="sxs-lookup"><span data-stu-id="cdb82-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="cdb82-130">1</span><span class="sxs-lookup"><span data-stu-id="cdb82-130">1</span></span>  <br/> |<span data-ttu-id="cdb82-131">Включите дефисы на уровне пользователей.</span><span class="sxs-lookup"><span data-stu-id="cdb82-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="cdb82-132">2</span><span class="sxs-lookup"><span data-stu-id="cdb82-132">2</span></span>  <br/> |<span data-ttu-id="cdb82-133">Не включать расширенное текст в полях.</span><span class="sxs-lookup"><span data-stu-id="cdb82-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="cdb82-134">4</span><span class="sxs-lookup"><span data-stu-id="cdb82-134">4</span></span>  <br/> |<span data-ttu-id="cdb82-135">Преобразование в один пробел.</span><span class="sxs-lookup"><span data-stu-id="cdb82-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="cdb82-136">8</span><span class="sxs-lookup"><span data-stu-id="cdb82-136">8</span></span>  <br/> |<span data-ttu-id="cdb82-137">Преобразование в набор пробелов.</span><span class="sxs-lookup"><span data-stu-id="cdb82-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="cdb82-138">16</span><span class="sxs-lookup"><span data-stu-id="cdb82-138">16</span></span>  <br/> |<span data-ttu-id="cdb82-139">Преобразование возврат каретки и перевода строки в пробелы.</span><span class="sxs-lookup"><span data-stu-id="cdb82-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="cdb82-140">32</span><span class="sxs-lookup"><span data-stu-id="cdb82-140">32</span></span>  <br/> |<span data-ttu-id="cdb82-141">Преобразования typographer квот для регулярного кавычки.</span><span class="sxs-lookup"><span data-stu-id="cdb82-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="cdb82-142">64</span><span class="sxs-lookup"><span data-stu-id="cdb82-142">64</span></span>  <br/> |<span data-ttu-id="cdb82-143">Преобразование рядом с пробелов в пробел.</span><span class="sxs-lookup"><span data-stu-id="cdb82-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="cdb82-144">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdb82-144">Example 1</span></span>

<span data-ttu-id="cdb82-145">SHAPETEXT(sheetN!theText)</span><span class="sxs-lookup"><span data-stu-id="cdb82-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="cdb82-146">Возвращает текст фигуры, с именем sheetN, точно так, как он отображается в форме.</span><span class="sxs-lookup"><span data-stu-id="cdb82-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cdb82-147">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cdb82-147">Example 2</span></span>

<span data-ttu-id="cdb82-148">SHAPETEXT(theText)</span><span class="sxs-lookup"><span data-stu-id="cdb82-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="cdb82-149">Возвращает текст текущего фигуры точно так, как он отображается в форме.</span><span class="sxs-lookup"><span data-stu-id="cdb82-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="cdb82-150">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cdb82-150">Example 3</span></span>

<span data-ttu-id="cdb82-151">SHAPETEXT (theText, 84)</span><span class="sxs-lookup"><span data-stu-id="cdb82-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="cdb82-152">Возвращает текст текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="cdb82-152">Returns the text of the current shape.</span></span> <span data-ttu-id="cdb82-153">Также преобразует рядом с пробелы пробелом (64), возврат каретки преобразует и в строке каналов пробелов (16) и преобразует знаки табуляции в пробелом (4).</span><span class="sxs-lookup"><span data-stu-id="cdb82-153">It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4).</span></span> <span data-ttu-id="cdb82-154">Сумма эти флаги — 84.</span><span class="sxs-lookup"><span data-stu-id="cdb82-154">The sum of these flags is 84.</span></span>
  

