---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ddfcdd95f0423ba92c37c434f18078eadf90d82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594022"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="b91fd-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="b91fd-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="b91fd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b91fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b91fd-105">Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b91fd-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="b91fd-106">���������</span><span class="sxs-lookup"><span data-stu-id="b91fd-106">Parameters</span></span>

 <span data-ttu-id="b91fd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b91fd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b91fd-108">[in] Битовая маска флаги, определяющее тип строк, возвращаемых в столбцов таблицы поставщика.</span><span class="sxs-lookup"><span data-stu-id="b91fd-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="b91fd-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b91fd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="b91fd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b91fd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b91fd-111">Столбцы строку, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b91fd-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="b91fd-112">Если флаг MAPI_UNICODE не установлен, столбцы представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b91fd-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="b91fd-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="b91fd-113">_lppTable_</span></span>
  
> <span data-ttu-id="b91fd-114">[out] Указатель на указатель в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="b91fd-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b91fd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b91fd-115">Return value</span></span>

<span data-ttu-id="b91fd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b91fd-116">S_OK</span></span> 
  
> <span data-ttu-id="b91fd-117">В таблице поставщика успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="b91fd-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b91fd-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="b91fd-118">Remarks</span></span>

<span data-ttu-id="b91fd-119">Метод **IProviderAdmin::GetProviderTable** получает указатель на таблице поставщика службы сообщений, таблицы, которая поддерживает MAPI, содержащий сведения о каждой поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b91fd-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="b91fd-120">В отличие от поставщика таблицы, возвращенный методом [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) в таблице поставщика, возвращаемые **IProviderAdmin::GetProviderTable** может включать дополнительные строки, которые представляют сведения, связанные с одним или несколькими из Поставщики услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b91fd-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="b91fd-121">Эти дополнительные данные добавляется к профилю ключевое слово «Раздела» файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="b91fd-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="b91fd-122">Поставщик имеет разделах дополнительных профилей, сохраняется структур **MAPIUID** для этих разделов в свойстве **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b91fd-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="b91fd-123">**PR_SERVICE_EXTRA_UIDS** сохраняется в разделе сообщения службы профилей.</span><span class="sxs-lookup"><span data-stu-id="b91fd-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="b91fd-124">Поставщики, которые были удалены, или используется, но помечены для удаления, не включаются в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="b91fd-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="b91fd-125">Поставщик таблиц являются статическими, что означает, что последующие дополнения или удалений из службы сообщений, не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="b91fd-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="b91fd-126">Если у службы сообщение нет поставщиков, **IProviderAdmin::GetProviderTable** возвращает таблицу с нуля строк и возвращаемое значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b91fd-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="b91fd-127">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="b91fd-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="b91fd-128">Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="b91fd-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="b91fd-129">Полный список столбцов в таблице поставщика в разделе [Поставщик в таблице](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b91fd-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b91fd-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b91fd-130">Notes to callers</span></span>

<span data-ttu-id="b91fd-131">Для получения строк таблицы поставщика в порядке транспорта, сортировку таблицы в столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b91fd-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="b91fd-132">Чтобы получить только те строки, представляющие поставщиков услуг (не включая любые дополнительные строки), ограничение на извлечение строк со значением PT_ERROR в столбце **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b91fd-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b91fd-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b91fd-133">MFCMAPI reference</span></span>

<span data-ttu-id="b91fd-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b91fd-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b91fd-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b91fd-135">**File**</span></span>|<span data-ttu-id="b91fd-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b91fd-136">**Function**</span></span>|<span data-ttu-id="b91fd-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b91fd-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b91fd-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b91fd-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="b91fd-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="b91fd-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="b91fd-140">Mfcmapi (en) использует метод **IProviderAdmin::GetProviderTable** для получения таблицы поставщиков для отображения в диалоговом окне новый.</span><span class="sxs-lookup"><span data-stu-id="b91fd-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b91fd-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b91fd-141">See also</span></span>



[<span data-ttu-id="b91fd-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="b91fd-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="b91fd-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b91fd-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="b91fd-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="b91fd-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="b91fd-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b91fd-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="b91fd-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="b91fd-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="b91fd-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b91fd-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="b91fd-148">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b91fd-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

