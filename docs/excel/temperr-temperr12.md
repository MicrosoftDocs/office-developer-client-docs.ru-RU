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
- Функция темперр [Excel 2007], функция TempErr12 [Excel 2007]
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
# <a name="temperrtemperr12"></a><span data-ttu-id="b8b34-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="b8b34-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="b8b34-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8b34-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b8b34-106">Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ \*\*\*\* , содержащую ошибку листа Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b8b34-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="b8b34-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8b34-107">Parameters</span></span>

 <span data-ttu-id="b8b34-108">_err_</span><span class="sxs-lookup"><span data-stu-id="b8b34-108">_err_</span></span>
  
<span data-ttu-id="b8b34-109">Необходимый код ошибки или его литеральный числовой эквивалент, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b8b34-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="b8b34-110">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="b8b34-110">**Error**</span></span>|<span data-ttu-id="b8b34-111">**Код ошибки, определенный в XLCALL. Высоты**</span><span class="sxs-lookup"><span data-stu-id="b8b34-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="b8b34-112">**Эквивалент десятичного разделителя**</span><span class="sxs-lookup"><span data-stu-id="b8b34-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8b34-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="b8b34-113">#NULL</span></span>  <br/> |<span data-ttu-id="b8b34-114">**Кслеррнулл**</span><span class="sxs-lookup"><span data-stu-id="b8b34-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="b8b34-115">нуль</span><span class="sxs-lookup"><span data-stu-id="b8b34-115">0</span></span>  <br/> |
|<span data-ttu-id="b8b34-116">#ДЕЛ/0!</span><span class="sxs-lookup"><span data-stu-id="b8b34-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="b8b34-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="b8b34-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="b8b34-118">см</span><span class="sxs-lookup"><span data-stu-id="b8b34-118">7</span></span>  <br/> |
|<span data-ttu-id="b8b34-119">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="b8b34-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="b8b34-120">**Кслеррвалуе**</span><span class="sxs-lookup"><span data-stu-id="b8b34-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="b8b34-121">15 </span><span class="sxs-lookup"><span data-stu-id="b8b34-121">15</span></span>  <br/> |
|<span data-ttu-id="b8b34-122">#ССЫЛКА!</span><span class="sxs-lookup"><span data-stu-id="b8b34-122">#REF!</span></span>  <br/> |<span data-ttu-id="b8b34-123">**Кслеррреф**</span><span class="sxs-lookup"><span data-stu-id="b8b34-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="b8b34-124">23</span><span class="sxs-lookup"><span data-stu-id="b8b34-124">23</span></span>  <br/> |
|<span data-ttu-id="b8b34-125">#ИМЯ?</span><span class="sxs-lookup"><span data-stu-id="b8b34-125">#NAME?</span></span>  <br/> |<span data-ttu-id="b8b34-126">**Кслеррнаме**</span><span class="sxs-lookup"><span data-stu-id="b8b34-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="b8b34-127">суммируемых</span><span class="sxs-lookup"><span data-stu-id="b8b34-127">29</span></span>  <br/> |
|<span data-ttu-id="b8b34-128">#ЧИСЛО!</span><span class="sxs-lookup"><span data-stu-id="b8b34-128">#NUM!</span></span>  <br/> |<span data-ttu-id="b8b34-129">**Кслеррнум**</span><span class="sxs-lookup"><span data-stu-id="b8b34-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="b8b34-130">36</span><span class="sxs-lookup"><span data-stu-id="b8b34-130">36</span></span>  <br/> |
|<span data-ttu-id="b8b34-131">#Н/Д</span><span class="sxs-lookup"><span data-stu-id="b8b34-131">#N/A</span></span>  <br/> |<span data-ttu-id="b8b34-132">**Кслеррна**</span><span class="sxs-lookup"><span data-stu-id="b8b34-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="b8b34-133">42</span><span class="sxs-lookup"><span data-stu-id="b8b34-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="b8b34-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8b34-134">Return value</span></span>

<span data-ttu-id="b8b34-135">Возвращает объект **кслтипебул** , содержащий код ошибки, который был передан.</span><span class="sxs-lookup"><span data-stu-id="b8b34-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b8b34-136">Пример</span><span class="sxs-lookup"><span data-stu-id="b8b34-136">Example</span></span>

<span data-ttu-id="b8b34-137">В этом примере функция **TempErr12** используется для возврата #VALUE!</span><span class="sxs-lookup"><span data-stu-id="b8b34-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="b8b34-138">Ошибка в Excel.</span><span class="sxs-lookup"><span data-stu-id="b8b34-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b8b34-139">Функция библиотеки Framework **TempErr12** выделяет память из внутреннего буфера, который обычно освобождается при вызове функции **Excel12f** платформы.</span><span class="sxs-lookup"><span data-stu-id="b8b34-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="b8b34-140">Если этот пример функции вызывается повторно без вызова **Excel12f** , происходит утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="b8b34-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="b8b34-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b8b34-141">See also</span></span>



[<span data-ttu-id="b8b34-142">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="b8b34-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

