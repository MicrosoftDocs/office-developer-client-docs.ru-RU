---
title: Имсгсервицеадминжетпровидертабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317383"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="81ede-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="81ede-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="81ede-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81ede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81ede-105">Предоставляет доступ к таблице поставщика, в которой перечислены поставщики служб в профиле.</span><span class="sxs-lookup"><span data-stu-id="81ede-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="81ede-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81ede-106">Parameters</span></span>

 <span data-ttu-id="81ede-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81ede-107">_ulFlags_</span></span>
  
> <span data-ttu-id="81ede-108">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="81ede-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="81ede-109">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="81ede-109">_lppTable_</span></span>
  
> <span data-ttu-id="81ede-110">вышли Указатель на указатель на таблицу поставщика.</span><span class="sxs-lookup"><span data-stu-id="81ede-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81ede-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81ede-111">Return value</span></span>

<span data-ttu-id="81ede-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="81ede-112">S_OK</span></span> 
  
> <span data-ttu-id="81ede-113">Таблица поставщика успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="81ede-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81ede-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="81ede-114">Remarks</span></span>

<span data-ttu-id="81ede-115">Метод **имсгсервицеадмин:: жетпровидертабле** предоставляет доступ к таблице поставщика MAPI, таблице, в которой перечислены все адресные книги, хранилища сообщений и поставщики транспорта, установленные в профиле.</span><span class="sxs-lookup"><span data-stu-id="81ede-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="81ede-116">В отличие от таблицы поставщика, возвращаемой с помощью метода [ипровидерадмин:: жетпровидертабле](iprovideradmin-getprovidertable.md) , таблица поставщика, возвращенная с помощью **Имсгсервицеадмин:: жетпровидертабле** не может включать дополнительные строки, представляющие информацию, связанную с одним или несколькими поставщиками услуг в профиле.</span><span class="sxs-lookup"><span data-stu-id="81ede-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="81ede-117">Поставщики, которые были удалены или используются, но помечены для удаления, не включаются в таблицу поставщика.</span><span class="sxs-lookup"><span data-stu-id="81ede-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="81ede-118">Таблицы поставщика являются статическими, что означает, что последующие добавления или удаления из профиля не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="81ede-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="81ede-119">Если у профиля нет поставщиков, **жетпровидертабле** возвращает таблицу с нулевыми строками и возвращаемым значением S_OK.</span><span class="sxs-lookup"><span data-stu-id="81ede-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="81ede-120">Полный список столбцов таблицы поставщик представлен в разделе [таблица поставщиков](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="81ede-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="81ede-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="81ede-121">Notes to callers</span></span>

<span data-ttu-id="81ede-122">Чтобы получить строки таблицы поставщика в порядке транспорта, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="81ede-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="81ede-123">ВыЗовите метод [IMAPITable:: restrict](imapitable-restrict.md) , чтобы применить ограничение свойства, которое соответствует свойству **пр_ресаурце_типе** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) с мапи_транспорт_провидер.</span><span class="sxs-lookup"><span data-stu-id="81ede-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="81ede-124">ВыЗовите метод [IMAPITable:: сорттабле](imapitable-sorttable.md) , чтобы отсортировать таблицу по столбцу **пр_провидер_ординал** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81ede-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="81ede-125">ВыЗовите метод [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="81ede-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="81ede-126">В качестве альтернативы этим вызовам можно выполнить один вызов функции [хркуеряллровс](hrqueryallrows.md) со всеми соответствующими структурами данных.</span><span class="sxs-lookup"><span data-stu-id="81ede-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="81ede-127">При получении столбцов **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) в каждой строке можно использовать этот массив структуры **мапиуид** , чтобы задать порядок транспорта в вызове [имсгсервицеадмин:: мсгсервицетранспортордер](imsgserviceadmin-msgservicetransportorder.md).</span><span class="sxs-lookup"><span data-stu-id="81ede-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="81ede-128">Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="81ede-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="81ede-129">Задает тип строки Юникод для данных, возвращаемых для начальных активных столбцов таблицы поставщика, с помощью метода [IMAPITable:: куериколумнс](imapitable-querycolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="81ede-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="81ede-130">Исходные активные столбцы для таблицы поставщика — это столбцы, возвращаемые методом **куериколумнс** , прежде чем поставщик, содержащий таблицу, вызывает метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="81ede-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="81ede-131">Задает тип строки Юникод для данных, возвращаемых для начальных активных строк таблицы поставщика, с помощью **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="81ede-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="81ede-132">Исходные активные строки для таблицы поставщика — это строки, возвращаемые **QueryRows** до того, как поставщик, содержащий таблицу, вызывает **метода SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="81ede-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="81ede-133">Управляет типами свойств порядка сортировки, возвращаемого методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) перед тем, как клиент, содержащий таблицу поставщика, вызывает метод [IMAPITable:: сорттабле](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="81ede-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="81ede-134">См. также</span><span class="sxs-lookup"><span data-stu-id="81ede-134">See also</span></span>



[<span data-ttu-id="81ede-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="81ede-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="81ede-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="81ede-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="81ede-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="81ede-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="81ede-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81ede-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

