---
title: Имсгсторежетрецеивефолдертабле
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
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="69bc3-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="69bc3-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="69bc3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69bc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69bc3-105">Предоставляет доступ к таблице получения папки, в которой содержатся сведения обо всех папках получения для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="69bc3-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="69bc3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69bc3-106">Parameters</span></span>

 <span data-ttu-id="69bc3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69bc3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="69bc3-108">возврата Битовая маска флагов, определяющих доступ к таблицам.</span><span class="sxs-lookup"><span data-stu-id="69bc3-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="69bc3-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="69bc3-109">The following flags can be set:</span></span>
    
<span data-ttu-id="69bc3-110">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="69bc3-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="69bc3-111">Позволяет **жетрецеивефолдертабле** успешно возвращать результат, возможно, прежде чем таблица будет полностью доступна вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="69bc3-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="69bc3-112">Если таблица недоступна, то выполнение последующих вызовов таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="69bc3-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="69bc3-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69bc3-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="69bc3-114">Возвращаемые строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="69bc3-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="69bc3-115">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="69bc3-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="69bc3-116">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="69bc3-116">_lppTable_</span></span>
  
> <span data-ttu-id="69bc3-117">вышли Указатель на указатель на таблицу "Получение папки".</span><span class="sxs-lookup"><span data-stu-id="69bc3-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69bc3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69bc3-118">Return value</span></span>

<span data-ttu-id="69bc3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="69bc3-119">S_OK</span></span> 
  
> <span data-ttu-id="69bc3-120">Таблица получения папки успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="69bc3-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69bc3-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="69bc3-121">Remarks</span></span>

<span data-ttu-id="69bc3-122">Метод **IMsgStore:: жетрецеивефолдертабле** предоставляет доступ к таблице, в которой показаны параметры свойств для всех папок получения хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="69bc3-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="69bc3-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="69bc3-123">Notes to implementers</span></span>

<span data-ttu-id="69bc3-124">Список обязательных столбцов в таблице получения папок представлен в статье [получение таблиц](receive-folder-tables.md)с папками.</span><span class="sxs-lookup"><span data-stu-id="69bc3-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="69bc3-125">Реализуйте таблицы приема-передачи для поддержки настройки ограничений свойств для свойства **пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="69bc3-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="69bc3-126">Это позволяет легко получить доступ к определенным папкам получения.</span><span class="sxs-lookup"><span data-stu-id="69bc3-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="69bc3-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="69bc3-127">Notes to callers</span></span>

<span data-ttu-id="69bc3-128">Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="69bc3-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="69bc3-129">Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="69bc3-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="69bc3-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69bc3-130">MFCMAPI reference</span></span>

<span data-ttu-id="69bc3-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="69bc3-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69bc3-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="69bc3-132">**File**</span></span>|<span data-ttu-id="69bc3-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="69bc3-133">**Function**</span></span>|<span data-ttu-id="69bc3-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="69bc3-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69bc3-135">Мсгсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="69bc3-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="69bc3-136">Кмсгсторедлг:: Ондисплайрецеивефолдертабле</span><span class="sxs-lookup"><span data-stu-id="69bc3-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="69bc3-137">MFCMAPI использует метод **IMsgStore:: жетрецеивефолдертабле** , чтобы получить отображаемую таблицу с папкой получения.</span><span class="sxs-lookup"><span data-stu-id="69bc3-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69bc3-138">См. также</span><span class="sxs-lookup"><span data-stu-id="69bc3-138">See also</span></span>



[<span data-ttu-id="69bc3-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="69bc3-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="69bc3-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="69bc3-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="69bc3-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="69bc3-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="69bc3-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="69bc3-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="69bc3-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="69bc3-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="69bc3-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="69bc3-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

