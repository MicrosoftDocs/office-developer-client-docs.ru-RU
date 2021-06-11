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
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="8a4db-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="8a4db-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="8a4db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a4db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a4db-105">Предоставляет доступ к таблице поставщиков сообщений, списку поставщиков услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a4db-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8a4db-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a4db-106">Parameters</span></span>

 <span data-ttu-id="8a4db-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a4db-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8a4db-108">[in] Немного флагов, которые контролируют тип строк, возвращаемых в столбцах таблицы поставщика.</span><span class="sxs-lookup"><span data-stu-id="8a4db-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="8a4db-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8a4db-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8a4db-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8a4db-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8a4db-111">Столбцы строк находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="8a4db-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="8a4db-112">Если флаг MAPI_UNICODE не установлен, столбцы находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="8a4db-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="8a4db-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="8a4db-113">_lppTable_</span></span>
  
> <span data-ttu-id="8a4db-114">[вышел] Указатель на указатель на таблицу поставщика.</span><span class="sxs-lookup"><span data-stu-id="8a4db-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a4db-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a4db-115">Return value</span></span>

<span data-ttu-id="8a4db-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a4db-116">S_OK</span></span> 
  
> <span data-ttu-id="8a4db-117">Таблица поставщика успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="8a4db-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a4db-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a4db-118">Remarks</span></span>

<span data-ttu-id="8a4db-119">Метод **IProviderAdmin::GetProviderTable** извлекает указатель в таблицу поставщика службы сообщений, таблицу, которую поддерживает MAPI, которая содержит сведения о каждом поставщике услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a4db-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="8a4db-120">В отличие от таблицы поставщиков, возвращаемой методом [IMsgServiceAdmin:::GetProviderTable,](imsgserviceadmin-getprovidertable.md) таблица поставщиков, возвращенная **IProviderAdmin::GetProviderTable,** может включать дополнительные строки, которые представляют сведения, связанные с одним или более поставщиками услуг в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a4db-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="8a4db-121">Эта дополнительная информация добавляется в профиль с помощью ключевого слова "Разделы" файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8a4db-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="8a4db-122">Если у поставщика есть дополнительные разделы профилей, он сохраняет структуры **MAPIUID** для этих разделов в **свойстве** [PR_SERVICE_EXTRA_UIDS (PidTagServiceExtraUids).](pidtagserviceextrauids-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8a4db-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="8a4db-123">**PR_SERVICE_EXTRA_UIDS** сохранена в разделе профиль службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a4db-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="8a4db-124">Поставщики, которые были удалены или используются, но помечены для удаления, не включены в таблицу поставщиков.</span><span class="sxs-lookup"><span data-stu-id="8a4db-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="8a4db-125">Таблицы поставщиков являются статичными, что означает, что последующие добавления или удаления из службы сообщений не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="8a4db-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="8a4db-126">Если служба сообщений не имеет поставщиков, **IProviderAdmin::GetProviderTable** возвращает таблицу с нулевыми строками и значением S_OK возвращается.</span><span class="sxs-lookup"><span data-stu-id="8a4db-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="8a4db-127">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="8a4db-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="8a4db-128">Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="8a4db-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="8a4db-129">Полный список столбцов в таблице поставщиков см. в [статье Provider Table.](provider-tables.md)</span><span class="sxs-lookup"><span data-stu-id="8a4db-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8a4db-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8a4db-130">Notes to callers</span></span>

<span data-ttu-id="8a4db-131">Чтобы получить строки таблицы поставщика в порядке транспорта, **сортировать таблицу** по столбце [PR_PROVIDER_ORDINAL (PidTagProviderOrdinal).](pidtagproviderordinal-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8a4db-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="8a4db-132">Чтобы получить только те строки, которые представляют поставщиков услуг (без дополнительных строк), ограничьте извлечение строками, которые имеют значение PT_ERROR в столбце **PR_RESOURCE_TYPE** [(PidTagResourceType).](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8a4db-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8a4db-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8a4db-133">MFCMAPI reference</span></span>

<span data-ttu-id="8a4db-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8a4db-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8a4db-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8a4db-135">**File**</span></span>|<span data-ttu-id="8a4db-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8a4db-136">**Function**</span></span>|<span data-ttu-id="8a4db-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8a4db-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8a4db-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8a4db-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="8a4db-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="8a4db-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="8a4db-140">MFCMAPI использует **метод IProviderAdmin::GetProviderTable** для получения таблицы поставщиков для отрисовки в новом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="8a4db-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a4db-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8a4db-141">See also</span></span>



[<span data-ttu-id="8a4db-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="8a4db-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="8a4db-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="8a4db-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="8a4db-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="8a4db-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="8a4db-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8a4db-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="8a4db-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="8a4db-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="8a4db-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a4db-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="8a4db-148">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8a4db-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

