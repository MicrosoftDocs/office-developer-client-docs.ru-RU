---
title: имаписессионжетстатустабле
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
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407139"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="8a1a4-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="8a1a4-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="8a1a4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a1a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a1a4-105">Предоставляет доступ к таблице Status (таблица), в которой содержатся сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8a1a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a1a4-106">Parameters</span></span>

 <span data-ttu-id="8a1a4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a1a4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8a1a4-108">возврата Битовая маска флагов, определяющих формат столбцов, которые являются символьными строками.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="8a1a4-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8a1a4-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8a1a4-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8a1a4-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8a1a4-111">Строковые столбцы представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="8a1a4-112">Если флаг MAPI_UNICODE не установлен, строковые столбцы имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="8a1a4-113">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="8a1a4-113">_lppTable_</span></span>
  
> <span data-ttu-id="8a1a4-114">вышли Указатель на указатель на таблицу состояния.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a1a4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a1a4-115">Return value</span></span>

<span data-ttu-id="8a1a4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a1a4-116">S_OK</span></span> 
  
> <span data-ttu-id="8a1a4-117">Таблица была успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a1a4-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a1a4-118">Remarks</span></span>

<span data-ttu-id="8a1a4-119">Метод **IMAPISession:: жетстатустабле** предоставляет доступ к таблице состояния, которая содержит сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="8a1a4-120">В таблице есть одна строка для сведений о подсистеме MAPI, одна строка для диспетчера очереди MAPI, одна строка для встроенной адресной книги и одна строка для каждого поставщика услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="8a1a4-121">Полный список обязательных и необязательных столбцов в таблице состояние представлен в статье [Status Tables](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a4-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="8a1a4-122">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="8a1a4-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="8a1a4-123">Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="8a1a4-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8a1a4-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8a1a4-124">MFCMAPI reference</span></span>

<span data-ttu-id="8a1a4-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8a1a4-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8a1a4-126">**File**</span></span>|<span data-ttu-id="8a1a4-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8a1a4-127">**Function**</span></span>|<span data-ttu-id="8a1a4-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8a1a4-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a1a4-129">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="8a1a4-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="8a1a4-130">Кмаиндлг:: Онстатустабле</span><span class="sxs-lookup"><span data-stu-id="8a1a4-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="8a1a4-131">MFCMAPI использует метод **IMAPISession:: жетстатустабле** , чтобы получить таблицу состояния для отображения.</span><span class="sxs-lookup"><span data-stu-id="8a1a4-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a1a4-132">См. также</span><span class="sxs-lookup"><span data-stu-id="8a1a4-132">See also</span></span>



[<span data-ttu-id="8a1a4-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a1a4-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="8a1a4-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="8a1a4-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="8a1a4-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="8a1a4-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="8a1a4-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="8a1a4-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="8a1a4-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8a1a4-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="8a1a4-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8a1a4-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="8a1a4-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a1a4-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="8a1a4-140">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="8a1a4-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8a1a4-141">Таблицы состояния</span><span class="sxs-lookup"><span data-stu-id="8a1a4-141">Status Tables</span></span>](status-tables.md)

