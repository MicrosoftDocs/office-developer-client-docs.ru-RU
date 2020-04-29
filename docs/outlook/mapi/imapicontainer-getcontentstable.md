---
title: имапиконтаинержетконтентстабле
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
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="2b921-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="2b921-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="2b921-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b921-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b921-105">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="2b921-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="2b921-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b921-106">Parameters</span></span>

 <span data-ttu-id="2b921-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b921-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2b921-108">возврата Битовая маска флагов, которые управляют способом возвращения таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="2b921-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="2b921-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="2b921-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2b921-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="2b921-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="2b921-111">Вместо стандартной таблицы содержимого следует возвратить связанную таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="2b921-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="2b921-112">Этот флаг используется только для папок.</span><span class="sxs-lookup"><span data-stu-id="2b921-112">This flag is used only with folders.</span></span> <span data-ttu-id="2b921-113">Сообщения, включенные в связанную таблицу содержимого, были созданы с помощью флага MAPI_ASSOCIATED, установленного в вызове метода [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="2b921-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="2b921-114">Клиенты обычно используют связанную таблицу содержимого для получения форм, представлений и других скрытых сообщений.</span><span class="sxs-lookup"><span data-stu-id="2b921-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="2b921-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="2b921-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="2b921-116">Разрешает доступ к правам Фригхтсфрибусисимпле и Фригхтсфрибусидетаилед в **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="2b921-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="2b921-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2b921-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2b921-118">**Жетконтентстабле** может успешно вернуть, возможно, перед тем, как таблица стала доступна вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="2b921-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="2b921-119">Если таблица недоступна, выполнение последующих вызовов таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="2b921-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="2b921-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b921-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2b921-121">Запрашивает возврат столбцов, содержащих строковые данные, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="2b921-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="2b921-122">Если флаг MAPI_UNICODE не установлен, строки должны быть возвращены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="2b921-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="2b921-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="2b921-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="2b921-124">Показывает элементы, которые в настоящее время помечены как обратимо удаленные — то есть они находятся на стадии хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="2b921-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="2b921-125">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="2b921-125">_lppTable_</span></span>
  
> <span data-ttu-id="2b921-126">вышли Указатель на указатель на таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="2b921-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2b921-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b921-127">Return value</span></span>

<span data-ttu-id="2b921-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b921-128">S_OK</span></span> 
  
> <span data-ttu-id="2b921-129">Таблица содержимого успешно получена.</span><span class="sxs-lookup"><span data-stu-id="2b921-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="2b921-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2b921-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2b921-131">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="2b921-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="2b921-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2b921-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2b921-133">Контейнер не имеет содержимого и не может предоставить таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="2b921-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b921-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b921-134">Remarks</span></span>

<span data-ttu-id="2b921-135">Метод **IMAPIContainer:: жетконтентстабле** возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="2b921-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="2b921-136">Таблица содержимого содержит сводную информацию об объектах в контейнере.</span><span class="sxs-lookup"><span data-stu-id="2b921-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="2b921-137">Таблицы содержимого содержат продолжительные наборы столбцов.</span><span class="sxs-lookup"><span data-stu-id="2b921-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="2b921-138">Полный список обязательных и необязательных столбцов в таблицах содержимого представлен в статье [оглавления](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2b921-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="2b921-139">Некоторые контейнеры могут не иметь содержимого.</span><span class="sxs-lookup"><span data-stu-id="2b921-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="2b921-140">Эти контейнеры возвращают MAPI_E_NO_SUPPORT из реализации **жетконтентстабле**.</span><span class="sxs-lookup"><span data-stu-id="2b921-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2b921-141">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2b921-141">Notes to implementers</span></span>

<span data-ttu-id="2b921-142">Если вы поддерживаете таблицу содержимого для контейнера, необходимо также выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2b921-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="2b921-143">Поддерживает вызовы метода контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для открытия свойства **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2b921-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2b921-144">Возвращает **PR_CONTAINER_CONTENTS** в ответ на вызов элемента контейнера</span><span class="sxs-lookup"><span data-stu-id="2b921-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="2b921-145">[IMAPIProp:: PROPS](imapiprop-getprops.md) и [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) методы.</span><span class="sxs-lookup"><span data-stu-id="2b921-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="2b921-146">Реализация этого метода в удаленном поставщике транспорта должна возвращать указатель на метод [IMAPITable: IUnknown](imapitableiunknown.md) в параметре _пптабле_ , переданном в метод **жетконтентстабле** .</span><span class="sxs-lookup"><span data-stu-id="2b921-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="2b921-147">Если у поставщика транспорта есть существующая таблица содержимого, достаточно возвратить указатель на него.</span><span class="sxs-lookup"><span data-stu-id="2b921-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="2b921-148">В противном случае этот метод должен создать новый объект [IMAPITable: IUnknown](imapitableiunknown.md) , заполнить таблицу заголовками сообщений (если они доступны) и возвратить указатель на новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="2b921-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="2b921-149">Метод [итабледата:: хржетвиев](itabledata-hrgetview.md) полезен для создания возвращаемого значения и сохранения указателя таблицы в параметре _пптабле_ .</span><span class="sxs-lookup"><span data-stu-id="2b921-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="2b921-150">Таблица Contents должна поддерживать по крайней мере следующие столбцы свойств:</span><span class="sxs-lookup"><span data-stu-id="2b921-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="2b921-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b921-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b921-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="2b921-169">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2b921-169">Notes to callers</span></span>

<span data-ttu-id="2b921-170">Столбцы таблицы строковых и двоичных содержимого можно усечь.</span><span class="sxs-lookup"><span data-stu-id="2b921-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="2b921-171">Как правило, поставщики возвращают 255 символов.</span><span class="sxs-lookup"><span data-stu-id="2b921-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="2b921-172">Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усекается, если длина столбца составляет 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="2b921-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="2b921-173">Вы всегда можете получить полное значение сокращенного столбца (при необходимости) непосредственно из объекта, используя его идентификатор записи, чтобы открыть его, а затем вызвать метод **IMAPIProp::/PROPS** .</span><span class="sxs-lookup"><span data-stu-id="2b921-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="2b921-174">В зависимости от реализации поставщика, ограничения и операции сортировки могут применяться ко всей строке или к усеченной версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="2b921-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2b921-175">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2b921-175">MFCMAPI reference</span></span>

<span data-ttu-id="2b921-176">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2b921-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2b921-177">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2b921-177">**File**</span></span>|<span data-ttu-id="2b921-178">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2b921-178">**Function**</span></span>|<span data-ttu-id="2b921-179">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2b921-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b921-180">Контентстабледиалог. cpp</span><span class="sxs-lookup"><span data-stu-id="2b921-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="2b921-181">Кконтентстабледлг:: Кконтентстабледлг</span><span class="sxs-lookup"><span data-stu-id="2b921-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="2b921-182">Класс **кконтентстабледлг** использует **жетконтентстабле** для получения записей в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="2b921-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b921-183">См. также</span><span class="sxs-lookup"><span data-stu-id="2b921-183">See also</span></span>



[<span data-ttu-id="2b921-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="2b921-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="2b921-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2b921-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="2b921-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="2b921-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="2b921-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b921-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="2b921-188">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="2b921-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="2b921-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2b921-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="2b921-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2b921-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

