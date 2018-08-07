---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7de404f421a405d80dd7f98beba5168969222fc9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809068"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="f81e6-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="f81e6-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="f81e6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f81e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f81e6-105">Предоставляет доступ к таблице состояния, таблицу, содержащую сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="f81e6-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f81e6-106">���������</span><span class="sxs-lookup"><span data-stu-id="f81e6-106">Parameters</span></span>

 <span data-ttu-id="f81e6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f81e6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f81e6-108">[in] Битовая маска флаги, который определяет формат для столбцов, которые являются строками символов.</span><span class="sxs-lookup"><span data-stu-id="f81e6-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="f81e6-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f81e6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f81e6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f81e6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f81e6-111">Столбцы строку, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f81e6-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="f81e6-112">Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f81e6-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="f81e6-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f81e6-113">_lppTable_</span></span>
  
> <span data-ttu-id="f81e6-114">[out] Указатель на указатель в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="f81e6-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f81e6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="f81e6-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f81e6-116">S_OK</span></span> 
  
> <span data-ttu-id="f81e6-117">Таблица успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="f81e6-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f81e6-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="f81e6-118">Remarks</span></span>

<span data-ttu-id="f81e6-119">Метод **IMAPISession::GetStatusTable** предоставляет доступ к таблице состояния, который содержит сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="f81e6-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="f81e6-120">Существует одна строка в таблице сведения о подсистемы MAPI, одна строка для очереди MAPI, одна строка для встроенной адресной книги и одной строке для каждого поставщика служб в профиле.</span><span class="sxs-lookup"><span data-stu-id="f81e6-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="f81e6-121">Полный список обязательные и дополнительные столбцы в таблице состояния видеть [Состояние таблицы](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f81e6-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="f81e6-122">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="f81e6-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="f81e6-123">Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="f81e6-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f81e6-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f81e6-124">MFCMAPI reference</span></span>

<span data-ttu-id="f81e6-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f81e6-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f81e6-126">**����**</span><span class="sxs-lookup"><span data-stu-id="f81e6-126">**File**</span></span>|<span data-ttu-id="f81e6-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="f81e6-127">**Function**</span></span>|<span data-ttu-id="f81e6-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f81e6-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f81e6-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f81e6-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f81e6-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="f81e6-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="f81e6-131">Mfcmapi (en) использует метод **IMAPISession::GetStatusTable** для получения состояния таблицы для отображения.</span><span class="sxs-lookup"><span data-stu-id="f81e6-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f81e6-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f81e6-132">See also</span></span>



[<span data-ttu-id="f81e6-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f81e6-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="f81e6-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="f81e6-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="f81e6-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="f81e6-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="f81e6-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="f81e6-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="f81e6-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="f81e6-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="f81e6-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="f81e6-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="f81e6-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f81e6-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f81e6-140">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f81e6-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f81e6-141">Таблицы состояния</span><span class="sxs-lookup"><span data-stu-id="f81e6-141">Status Tables</span></span>](status-tables.md)

