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
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809352"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="2aa9f-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="2aa9f-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="2aa9f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2aa9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2aa9f-105">Предоставляет доступ к таблице поставщика список поставщиков услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="2aa9f-106">���������</span><span class="sxs-lookup"><span data-stu-id="2aa9f-106">Parameters</span></span>

 <span data-ttu-id="2aa9f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2aa9f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2aa9f-108">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="2aa9f-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="2aa9f-109">_lppTable_</span></span>
  
> <span data-ttu-id="2aa9f-110">[out] Указатель на указатель в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2aa9f-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2aa9f-111">Return value</span></span>

<span data-ttu-id="2aa9f-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2aa9f-112">S_OK</span></span> 
  
> <span data-ttu-id="2aa9f-113">В таблице поставщика успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2aa9f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2aa9f-114">Remarks</span></span>

<span data-ttu-id="2aa9f-115">Метод **IMsgServiceAdmin::GetProviderTable** предоставляет доступ к таблице поставщика MAPI, таблица, перечисляющая адресной книги, хранилища сообщений и поставщиками транспорта, установленным в профиле.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="2aa9f-116">В отличие от поставщика таблицы, возвращенные с помощью метода [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) в таблице поставщика, возвращаемых при **IMsgServiceAdmin::GetProviderTable** не может содержать дополнительные строки, которые представляют сведения, связанные с помощью одного или нескольких поставщиков услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="2aa9f-117">Поставщики, которые были удалены, или используется, но помечены для удаления, не включаются в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="2aa9f-118">Поставщик таблиц являются статическими, что означает, что последующего добавления или удаления из профиля, не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="2aa9f-119">Если профиль не поставщиков, **GetProviderTable** возвращает таблицу с нуля строк и возвращаемое значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="2aa9f-120">Полный список столбцов в таблице поставщика в разделе [Поставщик в таблице](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2aa9f-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2aa9f-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2aa9f-121">Notes to callers</span></span>

<span data-ttu-id="2aa9f-122">Для получения строк таблицы поставщика в порядке транспорта, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="2aa9f-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="2aa9f-123">Вызовите метод [IMAPITable::Restrict](imapitable-restrict.md) , чтобы наложить ограничение свойство, которое соответствует свойства **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) с MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="2aa9f-124">Вызовите метод [IMAPITable::SortTable](imapitable-sorttable.md) , используемый для сортировки в таблице в столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2aa9f-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="2aa9f-125">Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) для получения строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="2aa9f-126">Альтернативой эти вызовы является сделать одного вызова функции [HrQueryAllRows](hrqueryallrows.md) со всеми структуры, передаются в соответствующие данные.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="2aa9f-127">При извлечении **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) столбцов в каждой из строк, чтобы установить порядок транспорта в вызове [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)можно использовать этот массив структур **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="2aa9f-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="2aa9f-128">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2aa9f-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="2aa9f-129">Задает тип string в Юникод для данных, возвращенный методом [IMAPITable::QueryColumns](imapitable-querycolumns.md) для начальной active столбцов в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="2aa9f-130">Начальное active столбцы для таблицы поставщика — это столбцы, возвращаемый методом **QueryColumns** перед поставщика, который содержит метод [IMAPITable::SetColumns](imapitable-setcolumns.md) вызовов в таблице.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="2aa9f-131">Задает тип string в Юникод для данных, возвращаемых **QueryRows**для начальной активных строк в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="2aa9f-132">Начальное active строк для поставщика таблицы, строки, **QueryRows** возвращает перед поставщика, который содержит таблицы вызовы **метода SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="2aa9f-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="2aa9f-133">Элементы управления типы свойств порядок сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) перед клиента с таблицей поставщик вызывает метод [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="2aa9f-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2aa9f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2aa9f-134">See also</span></span>



[<span data-ttu-id="2aa9f-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="2aa9f-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="2aa9f-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="2aa9f-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="2aa9f-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="2aa9f-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="2aa9f-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2aa9f-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

