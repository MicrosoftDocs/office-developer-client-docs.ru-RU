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
ms.openlocfilehash: c3c66b9e54f0776a8afd6b4638d36dec3393dda8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809218"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="221ae-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="221ae-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="221ae-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="221ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="221ae-105">Получает текущую позицию строки в таблице курсора на основании дробное значение.</span><span class="sxs-lookup"><span data-stu-id="221ae-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="221ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="221ae-106">Parameters</span></span>

 <span data-ttu-id="221ae-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="221ae-107">_lpulRow_</span></span>
  
> <span data-ttu-id="221ae-108">[out] Указатель на номер текущей строки.</span><span class="sxs-lookup"><span data-stu-id="221ae-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="221ae-109">Номер строки с отсчетом от нуля; первой строки в таблице равно нулю.</span><span class="sxs-lookup"><span data-stu-id="221ae-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="221ae-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="221ae-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="221ae-111">[out] Указатель на числитель дроби, определяющее позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="221ae-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="221ae-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="221ae-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="221ae-113">[out] Указатель на делителя дроби, определяющее позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="221ae-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="221ae-114">Параметр _lpulDenominator_ не может быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="221ae-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="221ae-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="221ae-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="221ae-116">S_OK</span></span> 
  
> <span data-ttu-id="221ae-117">Метод допустимого значения, возвращаемые в _lpulRow_, _lpulNumerator_и _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="221ae-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="221ae-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="221ae-118">Remarks</span></span>

<span data-ttu-id="221ae-119">Метод **IMAPITable::QueryPosition** определяет положение текущей строки и возвращает номер текущей строки и дробное значение, указывающее, относительное в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="221ae-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="221ae-120">MAPI определяет текущую строку, следующую строку для чтения.</span><span class="sxs-lookup"><span data-stu-id="221ae-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="221ae-121">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="221ae-121">Notes to implementers</span></span>

<span data-ttu-id="221ae-122">Необходимо получить точное количество строк в таблице для параметра _lpulDenominator_ ; она может быть приблизительным.</span><span class="sxs-lookup"><span data-stu-id="221ae-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="221ae-123">Если не удается определить текущей строки, возвращать значение 0xFFFFFFFF в _lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="221ae-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="221ae-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="221ae-124">Notes to callers</span></span>

<span data-ttu-id="221ae-125">**QueryPosition** можно использовать для размещения ползунка полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="221ae-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="221ae-126">Например, в таблице, содержащей 100 строк Если **QueryPosition** возвращает значение 75 в параметре _lpulNumerator_ 100 с помощью параметра _lpulDenominator_ и 75 в параметре _lpulRow_ можно расположить 3 и 4 поля прокрутки из способ через полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="221ae-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="221ae-127">Не полагайтесь на значение в _lpulDenominator_ число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="221ae-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="221ae-128">**QueryPosition** не может определить всегда точной строку, в которой находится курсор на.</span><span class="sxs-lookup"><span data-stu-id="221ae-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="221ae-129">Вызов **QueryPosition** может потребоваться большой объем памяти, особенно для больших таблиц по категориям.</span><span class="sxs-lookup"><span data-stu-id="221ae-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="221ae-130">Если параметр _lpulRow_ имеет значение 0xFFFFFFFF, слишком много памяти не требуется для **QueryPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="221ae-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="221ae-131">Вызовите метод [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) для размещения в таблице, чтобы строки, параметры _lpulNumerator_ и _lpulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="221ae-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="221ae-132">Тем не менее не следует ожидать **SeekRowApprox** для установки в качестве текущей позиции той же строке, если памяти не был фактор бы **QueryPosition** .</span><span class="sxs-lookup"><span data-stu-id="221ae-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="221ae-133">См. также</span><span class="sxs-lookup"><span data-stu-id="221ae-133">See also</span></span>



[<span data-ttu-id="221ae-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="221ae-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="221ae-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="221ae-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

