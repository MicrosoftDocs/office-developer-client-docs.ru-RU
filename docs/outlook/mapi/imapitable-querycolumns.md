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
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410107"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="d4d63-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="d4d63-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="d4d63-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4d63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4d63-105">Возвращает список столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4d63-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="d4d63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4d63-106">Parameters</span></span>

 <span data-ttu-id="d4d63-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4d63-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d4d63-108">[in] Битоваяmas флагов, которая указывает, какой набор столбцов должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="d4d63-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="d4d63-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d4d63-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d4d63-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="d4d63-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="d4d63-111">Таблица должна возвращать все доступные столбцы.</span><span class="sxs-lookup"><span data-stu-id="d4d63-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="d4d63-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d4d63-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="d4d63-113">[out] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащую теги свойств для набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="d4d63-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d4d63-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4d63-114">Return value</span></span>

<span data-ttu-id="d4d63-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4d63-115">S_OK</span></span> 
  
> <span data-ttu-id="d4d63-116">Набор столбцов был успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="d4d63-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="d4d63-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d4d63-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d4d63-118">В настоящее время идет другая операция, которая не позволяет начать операцию иниации набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="d4d63-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="d4d63-119">Либо операция должна быть разрешена для завершения, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="d4d63-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4d63-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4d63-120">Remarks</span></span>

<span data-ttu-id="d4d63-121">Метод **IMAPITable::QueryColumns** можно использовать для получения:</span><span class="sxs-lookup"><span data-stu-id="d4d63-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="d4d63-122">Набор столбцов по умолчанию для таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4d63-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="d4d63-123">Текущий столбец, задаемый для таблицы, как установлен вызовом метода [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="d4d63-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="d4d63-124">Полный набор столбцов для таблицы, столбцов, которые доступны, но не обязательно являются частью текущего набора.</span><span class="sxs-lookup"><span data-stu-id="d4d63-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d4d63-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d4d63-125">Notes to callers</span></span>

<span data-ttu-id="d4d63-126">Если флаг TBL_ALL_COLUMNS не установлен, **IMAPITable::QueryColumns** возвращает набор столбцов по умолчанию или текущий набор столбцов таблицы в зависимости от того, был ли затронут вызов **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="d4d63-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="d4d63-127">**SetColumns** изменяет порядок и выбор столбцов в наборе столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4d63-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="d4d63-128">Если установлен флаг TBL_ALL_COLUMNS, **QueryColumns** возвращает все столбцы, которые могут быть в наборе столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="d4d63-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="d4d63-129">Освободите память для массива тегов свойств, на который указывает параметр _lpPropTagArray,_ путем вызова функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d4d63-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4d63-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d4d63-130">MFCMAPI reference</span></span>

<span data-ttu-id="d4d63-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d4d63-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4d63-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d4d63-132">**File**</span></span>|<span data-ttu-id="d4d63-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d4d63-133">**Function**</span></span>|<span data-ttu-id="d4d63-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d4d63-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4d63-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d4d63-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d4d63-136">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="d4d63-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="d4d63-137">MFCMAPI использует метод **IMAPITable::QueryColumns** для получения текущего набора столбцов для таблицы, чтобы пользователь может изменить его.</span><span class="sxs-lookup"><span data-stu-id="d4d63-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4d63-138">См. также</span><span class="sxs-lookup"><span data-stu-id="d4d63-138">See also</span></span>



[<span data-ttu-id="d4d63-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d4d63-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="d4d63-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d4d63-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d4d63-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d4d63-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="d4d63-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4d63-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d4d63-143">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d4d63-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

