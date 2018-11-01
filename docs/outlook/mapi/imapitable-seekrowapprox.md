---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e6803c54ddd60c1bcebbe7a139c2edf2e7f4449d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572094"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="42e2a-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="42e2a-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="42e2a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42e2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42e2a-105">Перемещение курсора в приблизительно, например дробная позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="42e2a-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="42e2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42e2a-106">Parameters</span></span>

 <span data-ttu-id="42e2a-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="42e2a-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="42e2a-108">[in] Указатель на числитель дроби, представляющее позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="42e2a-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="42e2a-109">Если параметр _ulNumerator_ равно нулю, курсор расположен в начале таблицы независимо от значения делителя.</span><span class="sxs-lookup"><span data-stu-id="42e2a-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="42e2a-110">Если параметр _ulDenominator_ равен _ulNumerator_ , курсор расположен после последней строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="42e2a-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="42e2a-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="42e2a-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="42e2a-112">[in] Указатель на делителя дроби, представляющее позицию в таблице.</span><span class="sxs-lookup"><span data-stu-id="42e2a-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="42e2a-113">Параметр _ulDenominator_ не может быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="42e2a-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42e2a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42e2a-114">Return value</span></span>

<span data-ttu-id="42e2a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="42e2a-115">S_OK</span></span> 
  
> <span data-ttu-id="42e2a-116">Операции поиска выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="42e2a-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="42e2a-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="42e2a-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="42e2a-118">В, не позволяющей строку поиска операция запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="42e2a-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="42e2a-119">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="42e2a-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42e2a-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="42e2a-120">Remarks</span></span>

<span data-ttu-id="42e2a-121">Позиции курсора в таблице после вызова метода **IMAPITable::SeekRowApprox** был эвристически дроби и может быть точным.</span><span class="sxs-lookup"><span data-stu-id="42e2a-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="42e2a-122">Например определенных поставщиков реализовать таблице вверху двоичного дерева обработке середины таблицы как в верхней части дерева в целях повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="42e2a-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="42e2a-123">Если дерево не сбалансированной, затем середины используется может быть точно в середине таблицы.</span><span class="sxs-lookup"><span data-stu-id="42e2a-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="42e2a-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="42e2a-124">Notes to callers</span></span>

<span data-ttu-id="42e2a-125">Вызов **SeekRowApprox** для предоставления данных для реализации полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="42e2a-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="42e2a-126">Например при наведении пользователем 2 и 3 поле прокрутки вниз полосы прокрутки, чтобы смоделировать это действие путем вызова **SeekRowApprox** и передачи в эквивалентный дробное значение, с помощью _ulNumerator_ и _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="42e2a-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="42e2a-127">Поиск **SeekRowApprox** всегда является абсолютным с самого начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="42e2a-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="42e2a-128">Чтобы переместить в конец таблицы, значения в _ulNumerator_ и _ulDenominator_ должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="42e2a-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="42e2a-129">Используйте любой номер схема.</span><span class="sxs-lookup"><span data-stu-id="42e2a-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="42e2a-130">То есть выполнить поиск в таблице в середине позицию, можно указать 1/2, 10/20 или 50/100.</span><span class="sxs-lookup"><span data-stu-id="42e2a-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42e2a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="42e2a-131">See also</span></span>



[<span data-ttu-id="42e2a-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42e2a-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

