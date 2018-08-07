---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809221"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="7a223-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="7a223-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="7a223-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a223-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a223-105">Возвращает список столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a223-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="7a223-106">���������</span><span class="sxs-lookup"><span data-stu-id="7a223-106">Parameters</span></span>

 <span data-ttu-id="7a223-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a223-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7a223-108">[in] Битовая маска флаги, которое указывает, какой столбец значение должны быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="7a223-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="7a223-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7a223-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7a223-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="7a223-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="7a223-111">В таблице должен возвращать все доступные столбцы.</span><span class="sxs-lookup"><span data-stu-id="7a223-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="7a223-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="7a223-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="7a223-113">[out] Установите указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий свойства тегов для столбца.</span><span class="sxs-lookup"><span data-stu-id="7a223-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7a223-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="7a223-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7a223-115">S_OK</span></span> 
  
> <span data-ttu-id="7a223-116">Набор столбцов успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="7a223-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="7a223-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7a223-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7a223-118">Другой операции в процессе выполнения, не позволяющей столбце устанавливается операции извлечения запуск.</span><span class="sxs-lookup"><span data-stu-id="7a223-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="7a223-119">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="7a223-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a223-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a223-120">Remarks</span></span>

<span data-ttu-id="7a223-121">Метод **IMAPITable::QueryColumns** может вызываться для извлечения:</span><span class="sxs-lookup"><span data-stu-id="7a223-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="7a223-122">По умолчанию набор столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a223-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="7a223-123">Текущий набор столбцов для таблицы, в соответствии с параметром вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="7a223-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="7a223-124">Полный набор столбцов для таблицы, столбцы, которые доступны, но не обязательно частью текущего набора.</span><span class="sxs-lookup"><span data-stu-id="7a223-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="7a223-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7a223-125">Notes to callers</span></span>

<span data-ttu-id="7a223-126">Если флаг TBL_ALL_COLUMNS не задано, **IMAPITable::QueryColumns** возвращает таблицы по умолчанию либо текущий набор столбцов, в зависимости от того, является ли изменяет таблицы с помощью вызова **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="7a223-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="7a223-127">**Метода SetColumns** изменяет порядок и выбор столбцов в набор столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a223-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="7a223-128">Если установлен флаг TBL_ALL_COLUMNS, **QueryColumns** возвращает все столбцы, которые могут находиться в набор столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="7a223-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="7a223-129">Освободите память для массива свойства tag указывает параметр _lpPropTagArray_ путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7a223-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7a223-130">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7a223-130">MFCMAPI reference</span></span>

<span data-ttu-id="7a223-131">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7a223-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7a223-132">**����**</span><span class="sxs-lookup"><span data-stu-id="7a223-132">**File**</span></span>|<span data-ttu-id="7a223-133">**�������**</span><span class="sxs-lookup"><span data-stu-id="7a223-133">**Function**</span></span>|<span data-ttu-id="7a223-134">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7a223-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a223-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="7a223-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7a223-136">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="7a223-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="7a223-137">Mfcmapi (en) используется метод **IMAPITable::QueryColumns** для получения текущего набор столбцов для таблицы, пользователь может изменять его.</span><span class="sxs-lookup"><span data-stu-id="7a223-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a223-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7a223-138">See also</span></span>



[<span data-ttu-id="7a223-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7a223-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="7a223-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7a223-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7a223-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="7a223-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="7a223-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a223-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="7a223-143">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7a223-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

