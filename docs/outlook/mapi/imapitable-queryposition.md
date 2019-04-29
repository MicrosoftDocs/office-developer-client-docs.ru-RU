---
title: Имапитаблекуерипоситион
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
# <a name="imapitablequeryposition"></a><span data-ttu-id="3ea60-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="3ea60-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="3ea60-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ea60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ea60-105">Возвращает текущую позицию строки таблицы курсора на основе дробного значения.</span><span class="sxs-lookup"><span data-stu-id="3ea60-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="3ea60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ea60-106">Parameters</span></span>

 <span data-ttu-id="3ea60-107">_Лпулров_</span><span class="sxs-lookup"><span data-stu-id="3ea60-107">_lpulRow_</span></span>
  
> <span data-ttu-id="3ea60-108">вышли Указатель на номер текущей строки.</span><span class="sxs-lookup"><span data-stu-id="3ea60-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="3ea60-109">Номер строки отсчитывается от нуля; Первая строка в таблице равна нулю.</span><span class="sxs-lookup"><span data-stu-id="3ea60-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="3ea60-110">_Лпулнумератор_</span><span class="sxs-lookup"><span data-stu-id="3ea60-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="3ea60-111">вышли Указатель на числитель для дробной части, определяющей положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="3ea60-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="3ea60-112">_Лпулденоминатор_</span><span class="sxs-lookup"><span data-stu-id="3ea60-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="3ea60-113">вышли Указатель на знаменатель для дробной части, определяющей положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="3ea60-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="3ea60-114">Параметр _лпулденоминатор_ не может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="3ea60-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ea60-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ea60-115">Return value</span></span>

<span data-ttu-id="3ea60-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ea60-116">S_OK</span></span> 
  
> <span data-ttu-id="3ea60-117">Метод возвращает допустимые значения в _лпулров_, _лпулнумератор_и _лпулденоминатор_.</span><span class="sxs-lookup"><span data-stu-id="3ea60-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ea60-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ea60-118">Remarks</span></span>

<span data-ttu-id="3ea60-119">Метод **IMAPITable:: куерипоситион** определяет положение текущей строки и возвращает номер текущей строки и дробное значение, обозначающее его относительное положение до конца таблицы.</span><span class="sxs-lookup"><span data-stu-id="3ea60-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="3ea60-120">MAPI определяет текущую строку в качестве следующей строки для считывания.</span><span class="sxs-lookup"><span data-stu-id="3ea60-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ea60-121">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3ea60-121">Notes to implementers</span></span>

<span data-ttu-id="3ea60-122">Нет необходимости возвращать точное количество строк в таблице для параметра _лпулденоминатор_ ; Это может быть приближением.</span><span class="sxs-lookup"><span data-stu-id="3ea60-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="3ea60-123">Если вы не можете определить текущую строку, возвращайте значение 0xFFFFFFFF в _лпулров_.</span><span class="sxs-lookup"><span data-stu-id="3ea60-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ea60-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3ea60-124">Notes to callers</span></span>

<span data-ttu-id="3ea60-125">Вы можете использовать **куерипоситион** , чтобы разместить ползунок в полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3ea60-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="3ea60-126">Например, в таблице, содержащей 100 строк, если **куерипоситион** возвращает значение 75 в параметре _лпулнумератор_ , 100 в параметре _лпулденоминатор_ и 75 в параметре _лпулров_ , можно разместить поле прокрутки 3/4 способ на полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3ea60-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="3ea60-127">Не полагайтесь на то, что значение в _лпулденоминатор_ является количеством строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="3ea60-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="3ea60-128">**Куерипоситион** не всегда определяет точную строку, на которой размещен курсор.</span><span class="sxs-lookup"><span data-stu-id="3ea60-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="3ea60-129">При вызове **куерипоситион** может потребоваться большой объем памяти, особенно для таблиц с большими категориями.</span><span class="sxs-lookup"><span data-stu-id="3ea60-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="3ea60-130">Если для параметра _лпулров_ задано значение 0xFFFFFFFF, для определения текущей строки в **куерипоситион** требовалось слишком много памяти.</span><span class="sxs-lookup"><span data-stu-id="3ea60-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="3ea60-131">ВыЗовите метод [IMAPITable:: сикроваппрокс](imapitable-seekrowapprox.md) , чтобы поместить таблицу в строку, определенную параметрами _лпулнумератор_ и _лпулденоминатор_ .</span><span class="sxs-lookup"><span data-stu-id="3ea60-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="3ea60-132">Однако не всегда следует ожидать, что **сикроваппрокс** устанавливается в качестве текущей позиции, но в \*\*\*\* случае недостаточного коэффициента памяти.</span><span class="sxs-lookup"><span data-stu-id="3ea60-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ea60-133">См. также</span><span class="sxs-lookup"><span data-stu-id="3ea60-133">See also</span></span>



[<span data-ttu-id="3ea60-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="3ea60-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="3ea60-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ea60-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

