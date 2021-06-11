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
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431108"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="a49af-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="a49af-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="a49af-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a49af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a49af-105">Возвращает указатель в таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="a49af-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="a49af-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a49af-106">Parameters</span></span>

 <span data-ttu-id="a49af-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a49af-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a49af-108">[in] Битмаска флагов, которая управляет тем, как возвращается таблица контента.</span><span class="sxs-lookup"><span data-stu-id="a49af-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="a49af-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a49af-109">The following flags can be set:</span></span>
    
<span data-ttu-id="a49af-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="a49af-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="a49af-111">Связанная таблица содержимого контейнера должна быть возвращена вместо стандартной таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="a49af-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="a49af-112">Этот флаг используется только в папках.</span><span class="sxs-lookup"><span data-stu-id="a49af-112">This flag is used only with folders.</span></span> <span data-ttu-id="a49af-113">Сообщения, включенные в связанную таблицу содержимого, были созданы с флагом MAPI_ASSOCIATED в вызове метода [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="a49af-114">Обычно клиенты используют связанную таблицу контента для получения форм, представлений и других скрытых сообщений.</span><span class="sxs-lookup"><span data-stu-id="a49af-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="a49af-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="a49af-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="a49af-116">Включает доступ к правам frightsFreeBusySimple и frightsFreeBusyDetailed **в PR_MEMBER_RIGHTS.**</span><span class="sxs-lookup"><span data-stu-id="a49af-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="a49af-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a49af-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a49af-118">**GetContentsTable** может успешно вернуться, возможно, до того, как таблица будет доступна вызываемой.</span><span class="sxs-lookup"><span data-stu-id="a49af-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="a49af-119">Если таблица недоступна, при последующем вызове таблицы может быть допущена ошибка.</span><span class="sxs-lookup"><span data-stu-id="a49af-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="a49af-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a49af-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a49af-121">Запрашивает, чтобы столбцы, содержащие данные строки, возвращались в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="a49af-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="a49af-122">Если флаг MAPI_UNICODE не установлен, строки должны быть возвращены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a49af-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="a49af-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="a49af-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="a49af-124">Показывает элементы, которые в настоящее время помечены как мягкие удаленные, то есть они находятся на этапе времени хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="a49af-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="a49af-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a49af-125">_lppTable_</span></span>
  
> <span data-ttu-id="a49af-126">[вышел] Указатель на указатель на таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="a49af-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a49af-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a49af-127">Return value</span></span>

<span data-ttu-id="a49af-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="a49af-128">S_OK</span></span> 
  
> <span data-ttu-id="a49af-129">Таблица содержимого была успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="a49af-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="a49af-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a49af-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a49af-131">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="a49af-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="a49af-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a49af-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a49af-133">Контейнер не имеет содержимого и не может предоставить таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="a49af-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a49af-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="a49af-134">Remarks</span></span>

<span data-ttu-id="a49af-135">Метод **IMAPIContainer::GetContentsTable** возвращает указатель в таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="a49af-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="a49af-136">В таблице содержимого содержатся сводные сведения о объектах в контейнере.</span><span class="sxs-lookup"><span data-stu-id="a49af-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="a49af-137">Таблицы контента имеют длительные наборы столбцов.</span><span class="sxs-lookup"><span data-stu-id="a49af-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="a49af-138">Полный список необходимых и необязательных столбцов в таблицах контента см. в [статье Contents Tables.](contents-tables.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="a49af-139">Некоторые контейнеры могут не иметь содержимого.</span><span class="sxs-lookup"><span data-stu-id="a49af-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="a49af-140">Эти контейнеры возвращают MAPI_E_NO_SUPPORT из реализации **GetContentsTable.**</span><span class="sxs-lookup"><span data-stu-id="a49af-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a49af-141">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a49af-141">Notes to implementers</span></span>

<span data-ttu-id="a49af-142">Если вы поддерживаете таблицу контента для контейнера, необходимо также сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="a49af-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="a49af-143">Поддержка вызовов для метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия **свойства** [PR_CONTAINER_CONTENTS (PidTagContainerContents).](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="a49af-144">Возвращение **PR_CONTAINER_CONTENTS** в ответ на вызов контейнера</span><span class="sxs-lookup"><span data-stu-id="a49af-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="a49af-145">[Методы IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="a49af-146">Реализация этого метода удаленным поставщиком транспорта должна вернуть указатель в [интерфейс IMAPITable : IUnknown](imapitableiunknown.md) в параметре _ppTable,_ переданном в **метод GetContentsTable.**</span><span class="sxs-lookup"><span data-stu-id="a49af-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="a49af-147">Если у поставщика транспорта есть существующая таблица содержимого, достаточно вернуть указатель к ней.</span><span class="sxs-lookup"><span data-stu-id="a49af-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="a49af-148">Если нет, этот метод должен создать новый [объект IMAPITable : IUnknown,](imapitableiunknown.md) заполнить таблицу заголовщиками сообщений (если таковые имеются) и вернуть указатель в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a49af-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="a49af-149">Метод [ITableData::HrGetView](itabledata-hrgetview.md) полезен для создания возвращаемого значения и хранения указателя таблицы в параметре _ppTable._</span><span class="sxs-lookup"><span data-stu-id="a49af-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="a49af-150">Таблица контента должна поддерживать по крайней мере следующие столбцы свойств:</span><span class="sxs-lookup"><span data-stu-id="a49af-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="a49af-151">**PR_ENTRYID** [(PidTagEntryID)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-152">**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-153">**PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-154">**PR_DISPLAY_TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-155">**PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-156">**PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-157">**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-158">**PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-159">**PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-160">**PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-161">**PR_SENSITIVITY** [(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-162">**PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-163">**PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-164">**PR_MESSAGE_DOWNLOAD_TIME** [(PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-165">**PR_HASATTACH** [(PidTagHasAttachments)](pidtaghasattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-166">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-167">**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="a49af-168">**PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a49af-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="a49af-169">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a49af-169">Notes to callers</span></span>

<span data-ttu-id="a49af-170">Столбцы таблицы строк и двоичного содержимого можно усечено.</span><span class="sxs-lookup"><span data-stu-id="a49af-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="a49af-171">Обычно поставщики возвращают 255 символов.</span><span class="sxs-lookup"><span data-stu-id="a49af-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="a49af-172">Поскольку вы не можете заранее узнать, включает ли таблица усеченные столбцы, предположим, что столбец усечен, если длина столбца составляет 255 или 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="a49af-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="a49af-173">При необходимости вы всегда можете получить полное значение усеченного столбца непосредственно с объекта с помощью его идентификатора входа, чтобы открыть его, а затем позвонить по методу **IMAPIProp::GetProps.**</span><span class="sxs-lookup"><span data-stu-id="a49af-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="a49af-174">В зависимости от реализации поставщика ограничения и операции сортировки могут применяться к всем строкам или к усеченной версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="a49af-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a49af-175">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a49af-175">MFCMAPI reference</span></span>

<span data-ttu-id="a49af-176">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a49af-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a49af-177">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a49af-177">**File**</span></span>|<span data-ttu-id="a49af-178">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a49af-178">**Function**</span></span>|<span data-ttu-id="a49af-179">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a49af-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a49af-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="a49af-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="a49af-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="a49af-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="a49af-182">Класс **CContentsTableDlg** использует **GetContentsTable** для получения записей в таблице контента.</span><span class="sxs-lookup"><span data-stu-id="a49af-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a49af-183">См. также</span><span class="sxs-lookup"><span data-stu-id="a49af-183">See also</span></span>



[<span data-ttu-id="a49af-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="a49af-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="a49af-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a49af-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="a49af-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="a49af-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="a49af-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a49af-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="a49af-188">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="a49af-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="a49af-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a49af-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="a49af-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a49af-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

