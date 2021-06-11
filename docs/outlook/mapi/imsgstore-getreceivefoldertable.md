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
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421356"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="c41c0-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="c41c0-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="c41c0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c41c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c41c0-105">Предоставляет доступ к таблице приемных папок, которая содержит сведения обо всех папках получения для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="c41c0-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="c41c0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c41c0-106">Parameters</span></span>

 <span data-ttu-id="c41c0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c41c0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c41c0-108">[in] Битмаска флагов, которые контролируют доступ к таблице.</span><span class="sxs-lookup"><span data-stu-id="c41c0-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="c41c0-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c41c0-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c41c0-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c41c0-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c41c0-111">Позволяет **GetReceiveFolderTable** успешно вернуться, возможно, до того, как таблица будет полностью доступна вызываемой.</span><span class="sxs-lookup"><span data-stu-id="c41c0-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="c41c0-112">Если таблица недоступна полностью, последующий вызов таблицы может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="c41c0-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="c41c0-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c41c0-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c41c0-114">Возвращенные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="c41c0-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="c41c0-115">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c41c0-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c41c0-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c41c0-116">_lppTable_</span></span>
  
> <span data-ttu-id="c41c0-117">[вышел] Указатель на указатель на таблицу папки получения.</span><span class="sxs-lookup"><span data-stu-id="c41c0-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c41c0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c41c0-118">Return value</span></span>

<span data-ttu-id="c41c0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c41c0-119">S_OK</span></span> 
  
> <span data-ttu-id="c41c0-120">Таблица папки получения успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="c41c0-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c41c0-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="c41c0-121">Remarks</span></span>

<span data-ttu-id="c41c0-122">Метод **IMsgStore::GetReceiveFolderTable** предоставляет доступ к таблице, в которую показаны параметры свойств для всех папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c41c0-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c41c0-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c41c0-123">Notes to implementers</span></span>

<span data-ttu-id="c41c0-124">Список необходимых столбцов в таблице папки получения см. в [статье Получение таблиц папок.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="c41c0-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="c41c0-125">Реализуйте таблицы папки получения для поддержки установки ограничений свойств **для свойства PR_RECORD_KEY** [(PidTagRecordKey).](pidtagrecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c41c0-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="c41c0-126">Это позволяет легко получить доступ к определенным папкам получения.</span><span class="sxs-lookup"><span data-stu-id="c41c0-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c41c0-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c41c0-127">Notes to callers</span></span>

<span data-ttu-id="c41c0-128">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="c41c0-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="c41c0-129">Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="c41c0-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c41c0-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c41c0-130">MFCMAPI reference</span></span>

<span data-ttu-id="c41c0-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c41c0-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c41c0-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c41c0-132">**File**</span></span>|<span data-ttu-id="c41c0-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c41c0-133">**Function**</span></span>|<span data-ttu-id="c41c0-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c41c0-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c41c0-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c41c0-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="c41c0-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="c41c0-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="c41c0-137">MFCMAPI использует **метод IMsgStore::GetReceiveFolderTable** для отображения таблицы папки получения.</span><span class="sxs-lookup"><span data-stu-id="c41c0-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c41c0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c41c0-138">See also</span></span>



[<span data-ttu-id="c41c0-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c41c0-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="c41c0-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c41c0-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c41c0-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="c41c0-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="c41c0-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c41c0-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="c41c0-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c41c0-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="c41c0-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c41c0-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

