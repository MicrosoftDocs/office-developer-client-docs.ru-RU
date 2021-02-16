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
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434475"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="6c01d-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="6c01d-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="6c01d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c01d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c01d-105">Предоставляет доступ к таблице поставщиков службы сообщений, списку поставщиков услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c01d-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6c01d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c01d-106">Parameters</span></span>

 <span data-ttu-id="6c01d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c01d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6c01d-108">[in] Битоваяmas флагов, которая управляет типом строк, возвращаемой в столбцах таблицы поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c01d-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="6c01d-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6c01d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6c01d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c01d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6c01d-111">Строки столбцов в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="6c01d-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6c01d-112">Если флаг MAPI_UNICODE не установлен, столбцы будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6c01d-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="6c01d-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6c01d-113">_lppTable_</span></span>
  
> <span data-ttu-id="6c01d-114">[out] Указатель на указатель на таблицу поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c01d-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c01d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c01d-115">Return value</span></span>

<span data-ttu-id="6c01d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c01d-116">S_OK</span></span> 
  
> <span data-ttu-id="6c01d-117">Таблица поставщика успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="6c01d-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c01d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c01d-118">Remarks</span></span>

<span data-ttu-id="6c01d-119">Метод **IProviderAdmin::GetProviderTable** извлекает указатель на таблицу поставщика службы сообщений , таблицу, которую поддерживает MAPI, которая содержит сведения о каждом поставщике службы в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c01d-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="6c01d-120">В отличие от таблицы поставщика, возвращаемой методом [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) таблица поставщиков, возвращенная **IProviderAdmin::GetProviderTable,** может включать дополнительные строки, которые представляют сведения, связанные с одним или более поставщиками служб в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c01d-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="6c01d-121">Эти дополнительные сведения добавляются в профиль с ключевым словом "Sections" файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="6c01d-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="6c01d-122">Если у поставщика есть дополнительные разделы профиля, он сохраняет структуры **MAPIUID** для этих разделов в свойстве **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids).](pidtagserviceextrauids-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6c01d-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="6c01d-123">**PR_SERVICE_EXTRA_UIDS** в разделе профиля службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c01d-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="6c01d-124">Поставщики, которые были удалены или используются, но помечены для удаления, не включаются в таблицу поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6c01d-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="6c01d-125">Таблицы поставщиков являются статическими, то есть последующие добавления или удаления из службы сообщений не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="6c01d-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="6c01d-126">Если служба сообщений не имеет поставщиков, **IProviderAdmin::GetProviderTable** возвращает таблицу с нулем строк и значением S_OK возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6c01d-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="6c01d-127">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="6c01d-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="6c01d-128">Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="6c01d-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="6c01d-129">Полный список столбцов в таблице поставщиков см. в [таблице поставщиков.](provider-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6c01d-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c01d-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6c01d-130">Notes to callers</span></span>

<span data-ttu-id="6c01d-131">Чтобы получить строки таблицы поставщика в порядке транспорта, отсортировать таблицу по столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal).](pidtagproviderordinal-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6c01d-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="6c01d-132">Чтобы получить только те строки, которые представляют поставщиков услуг (без использования дополнительных строк), ограничите извлечение строками со значением PT_ERROR в столбце **PR_RESOURCE_TYPE** ([PidTagResourceType).](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6c01d-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c01d-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6c01d-133">MFCMAPI reference</span></span>

<span data-ttu-id="6c01d-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6c01d-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c01d-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6c01d-135">**File**</span></span>|<span data-ttu-id="6c01d-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6c01d-136">**Function**</span></span>|<span data-ttu-id="6c01d-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6c01d-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6c01d-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6c01d-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="6c01d-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="6c01d-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="6c01d-140">MFCMAPI использует метод **IProviderAdmin::GetProviderTable** для получения таблицы поставщиков для отображения в новом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6c01d-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c01d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="6c01d-141">See also</span></span>



[<span data-ttu-id="6c01d-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="6c01d-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="6c01d-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="6c01d-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="6c01d-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="6c01d-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="6c01d-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6c01d-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6c01d-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="6c01d-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="6c01d-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c01d-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="6c01d-148">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6c01d-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

