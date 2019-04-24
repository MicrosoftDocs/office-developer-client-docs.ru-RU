---
title: Имапитаблежетстатус
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328898"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="454d9-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="454d9-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="454d9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="454d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="454d9-105">Возвращает состояние и тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="454d9-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="454d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="454d9-106">Parameters</span></span>

 <span data-ttu-id="454d9-107">_Лпултаблестатус_</span><span class="sxs-lookup"><span data-stu-id="454d9-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="454d9-108">вышли Указатель на значение, указывающее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="454d9-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="454d9-109">Можно возвратить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="454d9-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="454d9-110">ТБЛСТАТ_КОМПЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="454d9-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="454d9-111">Ни одна операция не выполняется.</span><span class="sxs-lookup"><span data-stu-id="454d9-111">No operations are in progress.</span></span>
    
<span data-ttu-id="454d9-112">ТБЛСТАТ_КЧАНЖЕД</span><span class="sxs-lookup"><span data-stu-id="454d9-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="454d9-113">Содержимое таблицы изменилось с експектантли.</span><span class="sxs-lookup"><span data-stu-id="454d9-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="454d9-114">Это значение состояния не возвращается для изменений, вызванных операциями сортировки или ограничения.</span><span class="sxs-lookup"><span data-stu-id="454d9-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="454d9-115">ТБЛСТАТ_РЕСТРИКТ_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="454d9-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="454d9-116">Произошла ошибка при выполнении операции [IMAPITable:: restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="454d9-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="454d9-117">ТБЛСТАТ_РЕСТРИКТИНГ</span><span class="sxs-lookup"><span data-stu-id="454d9-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="454d9-118">В процессе **IMAPITable::** выполняется операция Restrict.</span><span class="sxs-lookup"><span data-stu-id="454d9-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="454d9-119">ТБЛСТАТ_СЕТКОЛ_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="454d9-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="454d9-120">Произошла ошибка при выполнении операции [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="454d9-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="454d9-121">ТБЛСТАТ_СЕТТИНГ_КОЛС</span><span class="sxs-lookup"><span data-stu-id="454d9-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="454d9-122">Выполняется операция **IMAPITable:: метода SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="454d9-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="454d9-123">ТБЛСТАТ_СОРТ_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="454d9-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="454d9-124">Произошла ошибка при выполнении операции [IMAPITable:: сорттабле](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="454d9-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="454d9-125">ТБЛСТАТ_СОРТИНГ</span><span class="sxs-lookup"><span data-stu-id="454d9-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="454d9-126">Выполняется операция **IMAPITable:: сорттабле** .</span><span class="sxs-lookup"><span data-stu-id="454d9-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="454d9-127">_Лпултаблетипе_</span><span class="sxs-lookup"><span data-stu-id="454d9-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="454d9-128">вышли Указатель на значение, указывающее тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="454d9-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="454d9-129">Можно вернуть один из следующих трех типов таблицы:</span><span class="sxs-lookup"><span data-stu-id="454d9-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="454d9-130">ТБЛТИПЕ_ДИНАМИК</span><span class="sxs-lookup"><span data-stu-id="454d9-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="454d9-131">Содержимое таблицы является динамическим; значения строк и столбцов могут изменяться при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="454d9-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="454d9-132">ТБЛТИПЕ_КЭЙСЕТ</span><span class="sxs-lookup"><span data-stu-id="454d9-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="454d9-133">Строки в таблице фиксированы, но значения столбцов в этих строках являются динамическими и могут изменяться при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="454d9-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="454d9-134">ТБЛТИПЕ_СНАПШОТ</span><span class="sxs-lookup"><span data-stu-id="454d9-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="454d9-135">Таблица является статической, и ее содержимое не изменяется при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="454d9-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="454d9-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="454d9-136">Return value</span></span>

<span data-ttu-id="454d9-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="454d9-137">S_OK</span></span> 
  
> <span data-ttu-id="454d9-138">Состояние таблицы было успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="454d9-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="454d9-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="454d9-139">Remarks</span></span>

<span data-ttu-id="454d9-140">Метод **имаптабле::** не получает сведений о типе таблицы и текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="454d9-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="454d9-141">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="454d9-141">Notes to callers</span></span>

<span data-ttu-id="454d9-142">Вы можете использовать методического **состояния** в сочетании с тремя другими методами **IMAPITable** для отслеживания состояния этих операций и определения их применения к таблице.</span><span class="sxs-lookup"><span data-stu-id="454d9-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="454d9-143">Call с параметром "/ **состояние** " после выполнения одного из следующих вызовов **IMAPITable** :</span><span class="sxs-lookup"><span data-stu-id="454d9-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="454d9-144">[IMAPITable:: restrict](imapitable-restrict.md) to set Restriction.</span><span class="sxs-lookup"><span data-stu-id="454d9-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="454d9-145">[IMAPITable:: сорттабле](imapitable-sorttable.md) для установки порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="454d9-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="454d9-146">[IMAPITable:: метода SetColumns](imapitable-setcolumns.md) для определения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="454d9-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="454d9-147">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="454d9-147">MFCMAPI reference</span></span>

<span data-ttu-id="454d9-148">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="454d9-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="454d9-149">**Файл**</span><span class="sxs-lookup"><span data-stu-id="454d9-149">**File**</span></span>|<span data-ttu-id="454d9-150">**Функция**</span><span class="sxs-lookup"><span data-stu-id="454d9-150">**Function**</span></span>|<span data-ttu-id="454d9-151">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="454d9-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="454d9-152">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="454d9-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="454d9-153">Кконтентстаблелистктрл::/Status</span><span class="sxs-lookup"><span data-stu-id="454d9-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="454d9-154">MFCMAPI использует метод **IMAPITable::** , чтобы сообщить о состоянии таблицы.</span><span class="sxs-lookup"><span data-stu-id="454d9-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="454d9-155">См. также</span><span class="sxs-lookup"><span data-stu-id="454d9-155">See also</span></span>



[<span data-ttu-id="454d9-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="454d9-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="454d9-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="454d9-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="454d9-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="454d9-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="454d9-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="454d9-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="454d9-160">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="454d9-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

