---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809395"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="e370f-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="e370f-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="e370f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e370f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e370f-105">Предоставляет доступ к таблице папок получения таблицу, содержащую сведения обо всех получения папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e370f-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="e370f-106">���������</span><span class="sxs-lookup"><span data-stu-id="e370f-106">Parameters</span></span>

 <span data-ttu-id="e370f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e370f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e370f-108">[in] Битовая маска флаги, таблицы, что элементы управления доступом.</span><span class="sxs-lookup"><span data-stu-id="e370f-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="e370f-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="e370f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="e370f-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e370f-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e370f-111">Позволяет **GetReceiveFolderTable** для возврата успешно, возможно перед таблице доступными для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="e370f-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="e370f-112">Если в таблице полностью недоступен, вызов последующие таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="e370f-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="e370f-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e370f-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e370f-114">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="e370f-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="e370f-115">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e370f-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e370f-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e370f-116">_lppTable_</span></span>
  
> <span data-ttu-id="e370f-117">[out] Указатель на указатель в таблице папку получения.</span><span class="sxs-lookup"><span data-stu-id="e370f-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e370f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="e370f-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e370f-119">S_OK</span></span> 
  
> <span data-ttu-id="e370f-120">В таблице папку получения успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="e370f-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e370f-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="e370f-121">Remarks</span></span>

<span data-ttu-id="e370f-122">Метод **IMsgStore::GetReceiveFolderTable** предоставляет доступ к таблице, которая отображает значения свойств для всех хранилища сообщений получают папок.</span><span class="sxs-lookup"><span data-stu-id="e370f-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e370f-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="e370f-123">Notes to implementers</span></span>

<span data-ttu-id="e370f-124">Список обязательные столбцы в таблице папку получения см [получают папки](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e370f-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="e370f-125">Реализация вашей получать таблиц папки для поддержки задание ограничений свойств на свойство **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e370f-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="e370f-126">В этом позволяет легко получить доступ к конкретным получают папок.</span><span class="sxs-lookup"><span data-stu-id="e370f-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e370f-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e370f-127">Notes to callers</span></span>

<span data-ttu-id="e370f-128">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="e370f-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="e370f-129">Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="e370f-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e370f-130">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="e370f-130">MFCMAPI reference</span></span>

<span data-ttu-id="e370f-131">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="e370f-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e370f-132">**����**</span><span class="sxs-lookup"><span data-stu-id="e370f-132">**File**</span></span>|<span data-ttu-id="e370f-133">**�������**</span><span class="sxs-lookup"><span data-stu-id="e370f-133">**Function**</span></span>|<span data-ttu-id="e370f-134">**�����������**</span><span class="sxs-lookup"><span data-stu-id="e370f-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e370f-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e370f-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="e370f-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="e370f-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="e370f-137">Mfcmapi (en) использует метод **IMsgStore::GetReceiveFolderTable** для получения таблицы получения папки для отображения.</span><span class="sxs-lookup"><span data-stu-id="e370f-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e370f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="e370f-138">See also</span></span>



[<span data-ttu-id="e370f-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e370f-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="e370f-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e370f-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e370f-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e370f-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="e370f-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e370f-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="e370f-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e370f-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="e370f-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e370f-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

