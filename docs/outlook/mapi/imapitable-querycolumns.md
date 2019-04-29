---
title: Имапитаблекуериколумнс
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
# <a name="imapitablequerycolumns"></a><span data-ttu-id="a6f50-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a6f50-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="a6f50-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6f50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6f50-105">Возвращает список столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="a6f50-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="a6f50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6f50-106">Parameters</span></span>

 <span data-ttu-id="a6f50-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6f50-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a6f50-108">возврата Битовая маска флагов, указывающих, какой набор столбцов должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="a6f50-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="a6f50-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a6f50-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a6f50-110">ТБЛ_АЛЛ_КОЛУМНС</span><span class="sxs-lookup"><span data-stu-id="a6f50-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="a6f50-111">Таблица должна возвращать все доступные столбцы.</span><span class="sxs-lookup"><span data-stu-id="a6f50-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="a6f50-112">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="a6f50-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="a6f50-113">вышли Указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую теги свойств для набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="a6f50-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6f50-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6f50-114">Return value</span></span>

<span data-ttu-id="a6f50-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6f50-115">S_OK</span></span> 
  
> <span data-ttu-id="a6f50-116">Набор столбцов успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="a6f50-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="a6f50-117">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="a6f50-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a6f50-118">Выполняется другая операция, которая не позволяет запустить операцию извлечения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="a6f50-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="a6f50-119">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="a6f50-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6f50-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6f50-120">Remarks</span></span>

<span data-ttu-id="a6f50-121">Метод **IMAPITable:: куериколумнс** можно вызвать для получения следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="a6f50-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="a6f50-122">Набор столбцов по умолчанию для таблицы.</span><span class="sxs-lookup"><span data-stu-id="a6f50-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="a6f50-123">Текущий набор столбцов для таблицы, установленный при вызове метода [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="a6f50-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="a6f50-124">Полный набор столбцов для таблицы, доступные столбцы, но не обязательно входящие в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="a6f50-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="a6f50-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a6f50-125">Notes to callers</span></span>

<span data-ttu-id="a6f50-126">Если не установить флаг ТБЛ_АЛЛ_КОЛУМНС, **IMAPITable:: куериколумнс** возвращает либо набор столбцов по умолчанию, либо текущий набор столбцов в зависимости от того, затронула ли таблица вызов **IMAPITable:: метода SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="a6f50-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="a6f50-127">**Метода SetColumns** изменяет порядок и выбор столбцов в наборе столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="a6f50-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="a6f50-128">Если установлен флаг ТБЛ_АЛЛ_КОЛУМНС, **куериколумнс** возвращает все столбцы, которые могут быть включены в набор столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="a6f50-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="a6f50-129">Освободите память для массива тегов свойств, на который указывает параметр _лппроптагаррай_ , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a6f50-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a6f50-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a6f50-130">MFCMAPI reference</span></span>

<span data-ttu-id="a6f50-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a6f50-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a6f50-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a6f50-132">**File**</span></span>|<span data-ttu-id="a6f50-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a6f50-133">**Function**</span></span>|<span data-ttu-id="a6f50-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a6f50-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6f50-135">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="a6f50-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="a6f50-136">Кконтентстаблелистктрл::D Осетколумнс</span><span class="sxs-lookup"><span data-stu-id="a6f50-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="a6f50-137">MFCMAPI использует метод **IMAPITable:: куериколумнс** , чтобы получить текущий набор столбцов для таблицы, чтобы пользователь мог ее редактировать.</span><span class="sxs-lookup"><span data-stu-id="a6f50-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6f50-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a6f50-138">See also</span></span>



[<span data-ttu-id="a6f50-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a6f50-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a6f50-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a6f50-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a6f50-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a6f50-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a6f50-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6f50-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="a6f50-143">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a6f50-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

