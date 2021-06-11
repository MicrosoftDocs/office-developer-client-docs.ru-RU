---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- функция темпера [Excel 2007], функция TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410611"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="355d8-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="355d8-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="355d8-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="355d8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="355d8-106">Функция библиотеки framework, которая создает временную **XLOPER** /  **XLOPER12,** содержащую ошибку Microsoft Excel таблицы.</span><span class="sxs-lookup"><span data-stu-id="355d8-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="355d8-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="355d8-107">Parameters</span></span>

 <span data-ttu-id="355d8-108">_err_</span><span class="sxs-lookup"><span data-stu-id="355d8-108">_err_</span></span>
  
<span data-ttu-id="355d8-109">Желаемый код ошибки или его литеральный числовый эквивалент, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="355d8-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="355d8-110">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="355d8-110">**Error**</span></span>|<span data-ttu-id="355d8-111">**Код ошибки, определенный в XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="355d8-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="355d8-112">**Десятичной эквивалент**</span><span class="sxs-lookup"><span data-stu-id="355d8-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="355d8-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="355d8-113">#NULL</span></span>  <br/> |<span data-ttu-id="355d8-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="355d8-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="355d8-115">0</span><span class="sxs-lookup"><span data-stu-id="355d8-115">0</span></span>  <br/> |
|<span data-ttu-id="355d8-116">#ДЕЛ/0!</span><span class="sxs-lookup"><span data-stu-id="355d8-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="355d8-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="355d8-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="355d8-118">7 </span><span class="sxs-lookup"><span data-stu-id="355d8-118">7</span></span>  <br/> |
|<span data-ttu-id="355d8-119">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="355d8-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="355d8-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="355d8-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="355d8-121">15</span><span class="sxs-lookup"><span data-stu-id="355d8-121">15</span></span>  <br/> |
|<span data-ttu-id="355d8-122">#ССЫЛКА!</span><span class="sxs-lookup"><span data-stu-id="355d8-122">#REF!</span></span>  <br/> |<span data-ttu-id="355d8-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="355d8-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="355d8-124">23</span><span class="sxs-lookup"><span data-stu-id="355d8-124">23</span></span>  <br/> |
|<span data-ttu-id="355d8-125">#ИМЯ?</span><span class="sxs-lookup"><span data-stu-id="355d8-125">#NAME?</span></span>  <br/> |<span data-ttu-id="355d8-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="355d8-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="355d8-127">29</span><span class="sxs-lookup"><span data-stu-id="355d8-127">29</span></span>  <br/> |
|<span data-ttu-id="355d8-128">#ЧИСЛО!</span><span class="sxs-lookup"><span data-stu-id="355d8-128">#NUM!</span></span>  <br/> |<span data-ttu-id="355d8-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="355d8-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="355d8-130">36</span><span class="sxs-lookup"><span data-stu-id="355d8-130">36</span></span>  <br/> |
|<span data-ttu-id="355d8-131">#Н/Д</span><span class="sxs-lookup"><span data-stu-id="355d8-131">#N/A</span></span>  <br/> |<span data-ttu-id="355d8-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="355d8-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="355d8-133">42</span><span class="sxs-lookup"><span data-stu-id="355d8-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="355d8-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="355d8-134">Return value</span></span>

<span data-ttu-id="355d8-135">Возвращает **xltypeBool,** содержащий переданный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="355d8-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="355d8-136">Пример</span><span class="sxs-lookup"><span data-stu-id="355d8-136">Example</span></span>

<span data-ttu-id="355d8-137">В этом примере **используется функция TempErr12** для возврата #VALUE!</span><span class="sxs-lookup"><span data-stu-id="355d8-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="355d8-138">ошибка Excel.</span><span class="sxs-lookup"><span data-stu-id="355d8-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="355d8-139">Функция библиотеки Framework **TempErr12** выделяет память из внутреннего буфера, который обычно освобожден при назвав функцию **Framework Excel12f.**</span><span class="sxs-lookup"><span data-stu-id="355d8-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="355d8-140">Если эта функция в примере называется несколько раз без призыва **Excel12f,** происходит утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="355d8-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="355d8-141">См. также</span><span class="sxs-lookup"><span data-stu-id="355d8-141">See also</span></span>



[<span data-ttu-id="355d8-142">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="355d8-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

