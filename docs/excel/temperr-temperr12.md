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
- функция temperr [excel 2007], функция TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807320"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="0c2fc-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="0c2fc-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="0c2fc-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c2fc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0c2fc-106">Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащий ошибку лист Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0c2fc-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="0c2fc-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c2fc-107">Parameters</span></span>

 <span data-ttu-id="0c2fc-108">_Ошибка_</span><span class="sxs-lookup"><span data-stu-id="0c2fc-108">_err_</span></span>
  
<span data-ttu-id="0c2fc-109">Код ошибки желаемую или его литерала числовой эквивалент, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0c2fc-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="0c2fc-110">**Error**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-110">**Error**</span></span>|<span data-ttu-id="0c2fc-111">**Код ошибки, определенных в XLCALL. H**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="0c2fc-112">**Десятичный эквивалент**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c2fc-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="0c2fc-113">#NULL</span></span>  <br/> |<span data-ttu-id="0c2fc-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="0c2fc-115">0</span><span class="sxs-lookup"><span data-stu-id="0c2fc-115">0</span></span>  <br/> |
|<span data-ttu-id="0c2fc-116">#���/0!</span><span class="sxs-lookup"><span data-stu-id="0c2fc-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="0c2fc-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="0c2fc-118">7</span><span class="sxs-lookup"><span data-stu-id="0c2fc-118">7</span></span>  <br/> |
|<span data-ttu-id="0c2fc-119">#����!</span><span class="sxs-lookup"><span data-stu-id="0c2fc-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="0c2fc-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="0c2fc-121">15</span><span class="sxs-lookup"><span data-stu-id="0c2fc-121">15</span></span>  <br/> |
|<span data-ttu-id="0c2fc-122">#������!</span><span class="sxs-lookup"><span data-stu-id="0c2fc-122">#REF!</span></span>  <br/> |<span data-ttu-id="0c2fc-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="0c2fc-124">23</span><span class="sxs-lookup"><span data-stu-id="0c2fc-124">23</span></span>  <br/> |
|<span data-ttu-id="0c2fc-125">#���?</span><span class="sxs-lookup"><span data-stu-id="0c2fc-125">#NAME?</span></span>  <br/> |<span data-ttu-id="0c2fc-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="0c2fc-127">29</span><span class="sxs-lookup"><span data-stu-id="0c2fc-127">29</span></span>  <br/> |
|<span data-ttu-id="0c2fc-128">#�����!</span><span class="sxs-lookup"><span data-stu-id="0c2fc-128">#NUM!</span></span>  <br/> |<span data-ttu-id="0c2fc-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="0c2fc-130">36</span><span class="sxs-lookup"><span data-stu-id="0c2fc-130">36</span></span>  <br/> |
|<span data-ttu-id="0c2fc-131">#�/�</span><span class="sxs-lookup"><span data-stu-id="0c2fc-131">#N/A</span></span>  <br/> |<span data-ttu-id="0c2fc-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="0c2fc-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="0c2fc-133">42</span><span class="sxs-lookup"><span data-stu-id="0c2fc-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="0c2fc-134">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0c2fc-134">Return value</span></span>

<span data-ttu-id="0c2fc-135">Возвращает значение **xltypeBool** , содержащий код ошибки переданную.</span><span class="sxs-lookup"><span data-stu-id="0c2fc-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0c2fc-136">Пример</span><span class="sxs-lookup"><span data-stu-id="0c2fc-136">Example</span></span>

<span data-ttu-id="0c2fc-137">В этом примере используется функция **TempErr12** возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="0c2fc-137">This example uses the **TempErr12** function to return a #VALUE!</span></span> <span data-ttu-id="0c2fc-138">Ошибка в Excel.</span><span class="sxs-lookup"><span data-stu-id="0c2fc-138">error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0c2fc-139">Функция библиотеки Framework **TempErr12** выделение памяти из внутреннего буфера, который обычно освобождается при вызове функции Framework **Excel12f** .</span><span class="sxs-lookup"><span data-stu-id="0c2fc-139">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called.</span></span> <span data-ttu-id="0c2fc-140">Если в этом примере функция вызывается несколько раз без **Excel12f** вызов, утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="0c2fc-140">If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="0c2fc-141">См. также</span><span class="sxs-lookup"><span data-stu-id="0c2fc-141">See also</span></span>



[<span data-ttu-id="0c2fc-142">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="0c2fc-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

