---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428139"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="e80ce-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="e80ce-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="e80ce-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e80ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e80ce-105">Предоставляет доступ к таблице хранилища сообщений, которая содержит сведения обо всех хранилищах сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="e80ce-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e80ce-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e80ce-106">Parameters</span></span>

 <span data-ttu-id="e80ce-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e80ce-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e80ce-108">[in] Битмаска флагов, определяемая форматом столбцов, которые являются строками символов.</span><span class="sxs-lookup"><span data-stu-id="e80ce-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="e80ce-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e80ce-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e80ce-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e80ce-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e80ce-111">Столбцы строк находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="e80ce-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="e80ce-112">Если флаг MAPI_UNICODE не установлен, столбцы строк находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e80ce-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="e80ce-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e80ce-113">_lppTable_</span></span>
  
> <span data-ttu-id="e80ce-114">[вышел] Указатель на указатель на таблице хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e80ce-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e80ce-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e80ce-115">Return value</span></span>

<span data-ttu-id="e80ce-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e80ce-116">S_OK</span></span> 
  
> <span data-ttu-id="e80ce-117">Таблица успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="e80ce-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="e80ce-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e80ce-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e80ce-119">Флаг MAPI_UNICODE и сеанс не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="e80ce-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e80ce-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e80ce-120">Remarks</span></span>

<span data-ttu-id="e80ce-121">Метод **IMAPISession::GetMsgStoresTable** извлекает указатель на таблицу хранения сообщений, таблицу, поддерживаемую MAPI, которая содержит сведения о каждом хранилище открытых сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="e80ce-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="e80ce-122">Полный список необходимых и необязательных столбцов в таблице хранения сообщений см. в статье [Таблицы хранения сообщений.](message-store-tables.md)</span><span class="sxs-lookup"><span data-stu-id="e80ce-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e80ce-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e80ce-123">Notes to callers</span></span>

<span data-ttu-id="e80ce-124">Поскольку MAPI обновляет таблицу хранения сообщений во время  сеанса при всех изменениях, вызывайте метод Advise таблицы хранения сообщений для регистрации, чтобы получить уведомление об этих изменениях.</span><span class="sxs-lookup"><span data-stu-id="e80ce-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="e80ce-125">Возможные изменения включают добавление новых магазинов сообщений, удаление существующих магазинов и изменения в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e80ce-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="e80ce-126">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="e80ce-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="e80ce-127">Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="e80ce-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e80ce-128">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e80ce-128">MFCMAPI reference</span></span>

<span data-ttu-id="e80ce-129">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e80ce-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e80ce-130">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e80ce-130">**File**</span></span>|<span data-ttu-id="e80ce-131">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e80ce-131">**Function**</span></span>|<span data-ttu-id="e80ce-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e80ce-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e80ce-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e80ce-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e80ce-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="e80ce-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="e80ce-135">MFCMAPI использует метод **IMAPISession::GetMsgStoresTable** для получения таблицы хранения сообщений, чтобы она была отрисовка в главном диалоговом окне MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="e80ce-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e80ce-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e80ce-136">See also</span></span>



[<span data-ttu-id="e80ce-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="e80ce-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="e80ce-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e80ce-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="e80ce-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e80ce-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="e80ce-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e80ce-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e80ce-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e80ce-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="e80ce-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e80ce-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="e80ce-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e80ce-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e80ce-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e80ce-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e80ce-145">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="e80ce-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e80ce-146">Таблицы магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="e80ce-146">Message Store Tables</span></span>](message-store-tables.md)

