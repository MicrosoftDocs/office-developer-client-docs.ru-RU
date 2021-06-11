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
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412151"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="32e72-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="32e72-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="32e72-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32e72-105">Перемещает курсор в приблизительное дробное положение в таблице.</span><span class="sxs-lookup"><span data-stu-id="32e72-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="32e72-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="32e72-106">Parameters</span></span>

 <span data-ttu-id="32e72-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="32e72-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="32e72-108">[in] Указатель на числитель фракции, представляющей положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="32e72-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="32e72-109">Если  _параметр ulNumerator_ ноль, курсор находится в начале таблицы независимо от значения знаменателя.</span><span class="sxs-lookup"><span data-stu-id="32e72-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="32e72-110">Если  _параметр ulNumerator_ равен параметру  _ulDenominator,_ курсор находится после последней строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="32e72-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="32e72-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="32e72-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="32e72-112">[in] Указатель на знаменатель фракции, представляющей положение таблицы.</span><span class="sxs-lookup"><span data-stu-id="32e72-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="32e72-113">Параметр  _ulDenominator не_ может быть нулем.</span><span class="sxs-lookup"><span data-stu-id="32e72-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="32e72-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32e72-114">Return value</span></span>

<span data-ttu-id="32e72-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="32e72-115">S_OK</span></span> 
  
> <span data-ttu-id="32e72-116">Операция поиска прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="32e72-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="32e72-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="32e72-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="32e72-118">В настоящее время продолжается еще одна операция, которая не позволяет начать операцию поиска строки.</span><span class="sxs-lookup"><span data-stu-id="32e72-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="32e72-119">Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="32e72-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32e72-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="32e72-120">Remarks</span></span>

<span data-ttu-id="32e72-121">Положение курсора в таблице после вызова к методу **IMAPITable::SeekRowApprox** является выурохом фракции и может быть не точным.</span><span class="sxs-lookup"><span data-stu-id="32e72-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="32e72-122">Например, некоторые поставщики могут реализовать таблицу поверх двоичного дерева, обрабатывая полпути таблицы как верх дерева по соображениям производительности.</span><span class="sxs-lookup"><span data-stu-id="32e72-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="32e72-123">Если дерево не сбалансировано, используемая на полпути точка может не быть ровно на полпути через таблицу.</span><span class="sxs-lookup"><span data-stu-id="32e72-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="32e72-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="32e72-124">Notes to callers</span></span>

<span data-ttu-id="32e72-125">Вызов **SeekRowApprox,** чтобы предоставить данные для реализации панели прокрутки.</span><span class="sxs-lookup"><span data-stu-id="32e72-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="32e72-126">Например, если пользователь расположил поле прокрутки 2/3 вниз по панели прокрутки, можно смоделировать это действие, позвонив **SeekRowApprox** и передав эквивалентное дробное значение с помощью  _ulNumerator_ и  _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="32e72-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="32e72-127">Поиск **SeekRowApprox** всегда является абсолютным с начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="32e72-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="32e72-128">Чтобы переместиться в конец таблицы, значения  _в ulNumerator_ и  _ulDenominator_ должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="32e72-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="32e72-129">Используйте любую соответствующую схему номеров.</span><span class="sxs-lookup"><span data-stu-id="32e72-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="32e72-130">То есть для поиска позиции на полпути через таблицу можно указать 1/2, 10/20 или 50/100.</span><span class="sxs-lookup"><span data-stu-id="32e72-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32e72-131">См. также</span><span class="sxs-lookup"><span data-stu-id="32e72-131">See also</span></span>



[<span data-ttu-id="32e72-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32e72-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

