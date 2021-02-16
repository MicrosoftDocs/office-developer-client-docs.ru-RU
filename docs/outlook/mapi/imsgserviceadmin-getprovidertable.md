---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428769"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="38960-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="38960-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="38960-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38960-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38960-105">Предоставляет доступ к таблице поставщиков, перечислению поставщиков услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="38960-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="38960-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38960-106">Parameters</span></span>

 <span data-ttu-id="38960-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38960-107">_ulFlags_</span></span>
  
> <span data-ttu-id="38960-108">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="38960-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="38960-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="38960-109">_lppTable_</span></span>
  
> <span data-ttu-id="38960-110">[out] Указатель на указатель на таблицу поставщика.</span><span class="sxs-lookup"><span data-stu-id="38960-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38960-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38960-111">Return value</span></span>

<span data-ttu-id="38960-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="38960-112">S_OK</span></span> 
  
> <span data-ttu-id="38960-113">Таблица поставщика успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="38960-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38960-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="38960-114">Remarks</span></span>

<span data-ttu-id="38960-115">Метод **IMsgServiceAdmin::GetProviderTable** предоставляет доступ к таблице поставщиков MAPI, которая содержит список всех поставщиков адресной книги, хранилище сообщений и поставщиков транспорта, установленных в данный момент в профиле.</span><span class="sxs-lookup"><span data-stu-id="38960-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="38960-116">В отличие от таблицы поставщика, возвращаемой методом [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) таблица поставщиков, возвращаемая с помощью **IMsgServiceAdmin::GetProviderTable,** не может включать дополнительные строки, которые представляют сведения, связанные с одним или более поставщиками служб в профиле.</span><span class="sxs-lookup"><span data-stu-id="38960-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="38960-117">Поставщики, которые были удалены или используются, но помечены для удаления, не включаются в таблицу поставщиков.</span><span class="sxs-lookup"><span data-stu-id="38960-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="38960-118">Таблицы поставщиков являются статическими, то есть последующие добавления или удаления из профиля не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="38960-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="38960-119">Если в профиле нет поставщиков, **GetProviderTable** возвращает таблицу с нулевыми строками, а значение S_OK значение.</span><span class="sxs-lookup"><span data-stu-id="38960-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="38960-120">Полный список столбцов в таблице поставщиков см. в [таблице поставщиков.](provider-tables.md)</span><span class="sxs-lookup"><span data-stu-id="38960-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="38960-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="38960-121">Notes to callers</span></span>

<span data-ttu-id="38960-122">Чтобы получить строки таблицы поставщика в порядке транспорта, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="38960-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="38960-123">Вызовите метод [IMAPITable::Restrict,](imapitable-restrict.md) чтобы наложить ограничение свойства, которое соответствует свойству **PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)с MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="38960-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="38960-124">Вызовите метод [IMAPITable::SortTable](imapitable-sorttable.md) для сортировки таблицы по столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal).](pidtagproviderordinal-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="38960-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="38960-125">Вызовите [метод IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы получить строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="38960-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="38960-126">Альтернативой этим вызовам является один вызов функции [HrQueryAllRows](hrqueryallrows.md) со всеми соответствующими структурами данных.</span><span class="sxs-lookup"><span data-stu-id="38960-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="38960-127">При извлечении столбцов **PR_SERVICE_UID** ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)в каждой строке можно использовать этот массив структур **MAPIUID,** чтобы настроить порядок транспорта в вызове [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span><span class="sxs-lookup"><span data-stu-id="38960-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="38960-128">Установка флага MAPI_UNICODE в  _параметре ulFlags_ делает следующее:</span><span class="sxs-lookup"><span data-stu-id="38960-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="38960-129">Задает тип строки Юникод для данных, возвращаемых для начальных активных столбцов таблицы поставщиков методом [IMAPITable::QueryColumns.](imapitable-querycolumns.md)</span><span class="sxs-lookup"><span data-stu-id="38960-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="38960-130">Начальные активные столбцы для таблицы поставщиков — это те столбцы, которые метод **QueryColumns** возвращает перед тем, как поставщик, содержащий таблицу, вызывает метод [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="38960-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="38960-131">Задает тип строки Юникод для данных, возвращаемого для начальных активных строк таблицы поставщика **queryRows.**</span><span class="sxs-lookup"><span data-stu-id="38960-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="38960-132">Начальные активные строки для таблицы поставщиков — это строки, которые **QueryRows** возвращает перед тем, как поставщик, содержащий таблицу, вызывает **SetColumns.**</span><span class="sxs-lookup"><span data-stu-id="38960-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="38960-133">Управляет типами свойств порядка сортировки, возвращаемого методом [IMAPITable::QuerySortOrder,](imapitable-querysortorder.md) перед тем как клиент, содержащий таблицу поставщика, вызывает метод [IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="38960-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="38960-134">См. также</span><span class="sxs-lookup"><span data-stu-id="38960-134">See also</span></span>



[<span data-ttu-id="38960-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="38960-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="38960-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="38960-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="38960-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="38960-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="38960-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38960-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

