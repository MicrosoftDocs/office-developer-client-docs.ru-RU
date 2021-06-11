---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415665"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="65d5a-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="65d5a-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="65d5a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65d5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65d5a-105">Извлекает текущее положение строки таблицы курсора на основе дробного значения.</span><span class="sxs-lookup"><span data-stu-id="65d5a-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="65d5a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="65d5a-106">Parameters</span></span>

 <span data-ttu-id="65d5a-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="65d5a-107">_lpulRow_</span></span>
  
> <span data-ttu-id="65d5a-108">[вышел] Указатель на номер текущей строки.</span><span class="sxs-lookup"><span data-stu-id="65d5a-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="65d5a-109">Номер строки нулевой; первая строка в таблице — ноль.</span><span class="sxs-lookup"><span data-stu-id="65d5a-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="65d5a-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="65d5a-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="65d5a-111">[вышел] Указатель на числитель для фракции, определяющий положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="65d5a-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="65d5a-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="65d5a-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="65d5a-113">[вышел] Указатель на знаменатель для фракции, определяющий положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="65d5a-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="65d5a-114">Параметр  _lpulDenominator не_ может быть нулем.</span><span class="sxs-lookup"><span data-stu-id="65d5a-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="65d5a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65d5a-115">Return value</span></span>

<span data-ttu-id="65d5a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="65d5a-116">S_OK</span></span> 
  
> <span data-ttu-id="65d5a-117">Метод возвращал допустимые значения  _в lpulRow,_  _lpulNumerator_ и  _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="65d5a-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65d5a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="65d5a-118">Remarks</span></span>

<span data-ttu-id="65d5a-119">Метод **IMAPITable::QueryPosition** определяет текущую позицию строки и возвращает число текущей строки и дробное значение, указывающее ее относительное положение в конце таблицы.</span><span class="sxs-lookup"><span data-stu-id="65d5a-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="65d5a-120">MAPI определяет текущую строку как следующую строку, которая должна быть прочитана.</span><span class="sxs-lookup"><span data-stu-id="65d5a-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="65d5a-121">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="65d5a-121">Notes to implementers</span></span>

<span data-ttu-id="65d5a-122">Вам не нужно возвращать точное количество строк в таблице для  _параметра lpulDenominator;_ это может быть приближение.</span><span class="sxs-lookup"><span data-stu-id="65d5a-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="65d5a-123">Если вы не можете определить текущую строку, верни значение 0xFFFFFFFF  _в lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="65d5a-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="65d5a-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="65d5a-124">Notes to callers</span></span>

<span data-ttu-id="65d5a-125">Вы можете использовать **QueryPosition** для расположения окна прокрутки в панели прокрутки.</span><span class="sxs-lookup"><span data-stu-id="65d5a-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="65d5a-126">Например, в таблице, содержащей 100 строк, если **QueryPosition** возвращает значение 75 в параметре  _lpulNumerator,_ 100 в  _параметре lpulDenominator_ и 75 в параметре  _lpulRow,_ можно расположить поле прокрутки 3/4 поперек панели прокрутки.</span><span class="sxs-lookup"><span data-stu-id="65d5a-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="65d5a-127">Не полагаться на значение  _lpulDenominator,_ являемого числом строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="65d5a-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="65d5a-128">**QueryPosition** не всегда может определить точную строку, на которую находится курсор.</span><span class="sxs-lookup"><span data-stu-id="65d5a-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="65d5a-129">Вызов в **QueryPosition может** включать большое количество памяти, особенно для больших категорий таблиц.</span><span class="sxs-lookup"><span data-stu-id="65d5a-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="65d5a-130">Если  _параметр lpulRow_ задан для 0xFFFFFFFF, для определения текущей строки **в QueryPosition** требуется слишком много памяти.</span><span class="sxs-lookup"><span data-stu-id="65d5a-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="65d5a-131">Вызов [метода IMAPITable::SeekRowApprox,](imapitable-seekrowapprox.md) чтобы расположить таблицу к строке, определенной _параметрами lpulNumerator_ и _lpulDenominator._</span><span class="sxs-lookup"><span data-stu-id="65d5a-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="65d5a-132">Однако не всегда следует ожидать, что **SeekRowApprox** установит в качестве текущей позиции ту же строку **QueryPosition,** если бы память не была фактором.</span><span class="sxs-lookup"><span data-stu-id="65d5a-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65d5a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="65d5a-133">See also</span></span>



[<span data-ttu-id="65d5a-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="65d5a-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="65d5a-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65d5a-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

