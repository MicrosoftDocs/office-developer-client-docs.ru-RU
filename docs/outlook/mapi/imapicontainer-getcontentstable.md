---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9fb8919287420038b5c9165bb14b7d33d1ad2fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578866"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="021a2-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="021a2-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="021a2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="021a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="021a2-105">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="021a2-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="021a2-106">���������</span><span class="sxs-lookup"><span data-stu-id="021a2-106">Parameters</span></span>

 <span data-ttu-id="021a2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="021a2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="021a2-108">[in] Битовая маска флаги, который определяет, как возвращается в таблице содержимое.</span><span class="sxs-lookup"><span data-stu-id="021a2-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="021a2-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="021a2-109">The following flags can be set:</span></span>
    
<span data-ttu-id="021a2-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="021a2-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="021a2-111">Таблица связанного содержимого контейнера должны быть возвращены вместо стандартного содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="021a2-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="021a2-112">Этот флаг используется только для папок.</span><span class="sxs-lookup"><span data-stu-id="021a2-112">This flag is used only with folders.</span></span> <span data-ttu-id="021a2-113">Сообщения, которые включены в таблицу связанного содержимого были созданы с флагом MAPI_ASSOCIATED, задайте в вызове метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="021a2-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="021a2-114">Клиенты обычно используется в таблице связанное содержимое для получения форм, представлений и другие скрытые сообщения.</span><span class="sxs-lookup"><span data-stu-id="021a2-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="021a2-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="021a2-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="021a2-116">Обеспечивает доступ к frightsFreeBusySimple и frightsFreeBusyDetailed правами в **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="021a2-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="021a2-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="021a2-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="021a2-118">**GetContentsTable** может вернуть успешно, возможно перед таблице можно сделать доступной для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="021a2-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="021a2-119">Если в таблице не поддерживается, вызов последующие таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="021a2-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="021a2-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="021a2-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="021a2-121">Запросы, которые столбцы, которые содержат строковые данные возвращаются в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="021a2-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="021a2-122">Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="021a2-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="021a2-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="021a2-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="021a2-124">Отображает элементы, которые в настоящее время помечены как программных удалены, то есть, они находятся в хранения удаленных элементов этап времени.</span><span class="sxs-lookup"><span data-stu-id="021a2-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="021a2-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="021a2-125">_lppTable_</span></span>
  
> <span data-ttu-id="021a2-126">[out] Указатель на указатель на таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="021a2-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="021a2-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="021a2-127">Return value</span></span>

<span data-ttu-id="021a2-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="021a2-128">S_OK</span></span> 
  
> <span data-ttu-id="021a2-129">В таблице содержимое был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="021a2-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="021a2-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="021a2-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="021a2-131">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="021a2-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="021a2-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="021a2-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="021a2-133">Контейнер не имеет содержимого и не могут предоставить таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="021a2-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="021a2-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="021a2-134">Remarks</span></span>

<span data-ttu-id="021a2-135">Метод **IMAPIContainer::GetContentsTable** возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="021a2-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="021a2-136">Содержимое таблицы содержит сводную информацию о объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="021a2-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="021a2-137">Содержимое таблицы имеют наборов длительным столбца.</span><span class="sxs-lookup"><span data-stu-id="021a2-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="021a2-138">Полный список обязательные и дополнительные столбцы в таблицах содержимое [Содержимое](contents-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="021a2-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="021a2-139">Существует возможность для некоторых контейнеров для без содержимого.</span><span class="sxs-lookup"><span data-stu-id="021a2-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="021a2-140">Эти контейнеры возврата MAPI_E_NO_SUPPORT из их реализации **GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="021a2-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="021a2-141">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="021a2-141">Notes to implementers</span></span>

<span data-ttu-id="021a2-142">Если вы поддерживаете таблицу содержимого для контейнера, необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="021a2-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="021a2-143">Поддерживает вызовы метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия свойство **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="021a2-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="021a2-144">Возвращает **PR_CONTAINER_CONTENTS** в ответ на звонок в контейнер</span><span class="sxs-lookup"><span data-stu-id="021a2-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="021a2-145">Методы [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="021a2-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="021a2-146">Реализация поставщика транспорта удаленного этот метод должен возвращать указатель [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса с помощью параметра _ppTable_ , передаваемый в метод **GetContentsTable** .</span><span class="sxs-lookup"><span data-stu-id="021a2-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="021a2-147">Если ваш поставщик транспорта существующей таблицы содержимое, достаточно возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="021a2-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="021a2-148">Если не, этот метод должен создать новый [IMAPITable: IUnknown](imapitableiunknown.md) объекта, заполните таблицу с заголовками сообщения (если они доступны) и возвращает указатель для новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="021a2-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="021a2-149">Метод [ITableData::HrGetView](itabledata-hrgetview.md) может использоваться для создания возвращаемого значения и хранения указатель таблицы с помощью параметра _ppTable_ .</span><span class="sxs-lookup"><span data-stu-id="021a2-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="021a2-150">В таблице содержимого должна поддерживать по крайней мере следующие столбцы свойств:</span><span class="sxs-lookup"><span data-stu-id="021a2-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="021a2-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="021a2-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="021a2-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="021a2-169">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="021a2-169">Notes to callers</span></span>

<span data-ttu-id="021a2-170">Строка и двоичный столбцов таблицы содержимое может быть усечен.</span><span class="sxs-lookup"><span data-stu-id="021a2-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="021a2-171">Как правило поставщики возвращать 255 символов.</span><span class="sxs-lookup"><span data-stu-id="021a2-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="021a2-172">Так как не известно, заранее ли таблицы включает в себя усеченных столбцы, предполагается, что столбец усекается, если длина столбца — 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="021a2-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="021a2-173">Всегда можно будет извлечь полное значение усеченных столбца, при необходимости непосредственно из объекта с помощью его идентификатор записи чтобы его открыть, затем вызвать метод **IMAPIProp::GetProps** .</span><span class="sxs-lookup"><span data-stu-id="021a2-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="021a2-174">В зависимости от реализации поставщика, ограничения и операции сортировки можно применять ко всем строки или усеченных версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="021a2-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="021a2-175">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="021a2-175">MFCMAPI reference</span></span>

<span data-ttu-id="021a2-176">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="021a2-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="021a2-177">**Файл**</span><span class="sxs-lookup"><span data-stu-id="021a2-177">**File**</span></span>|<span data-ttu-id="021a2-178">**Функция**</span><span class="sxs-lookup"><span data-stu-id="021a2-178">**Function**</span></span>|<span data-ttu-id="021a2-179">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="021a2-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="021a2-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="021a2-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="021a2-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="021a2-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="021a2-182">Класс **CContentsTableDlg** **GetContentsTable** используется для получения записей в таблицу.</span><span class="sxs-lookup"><span data-stu-id="021a2-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="021a2-183">См. также</span><span class="sxs-lookup"><span data-stu-id="021a2-183">See also</span></span>



[<span data-ttu-id="021a2-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="021a2-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="021a2-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="021a2-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="021a2-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="021a2-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="021a2-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="021a2-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="021a2-188">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="021a2-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="021a2-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="021a2-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="021a2-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="021a2-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

