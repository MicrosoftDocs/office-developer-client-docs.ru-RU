---
title: Имапиконтаинержетконтентстабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349289"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="acfff-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="acfff-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="acfff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acfff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acfff-105">Возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="acfff-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="acfff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="acfff-106">Parameters</span></span>

 <span data-ttu-id="acfff-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="acfff-107">_ulFlags_</span></span>
  
> <span data-ttu-id="acfff-108">возврата Битовая маска флагов, которые управляют способом возвращения таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="acfff-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="acfff-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="acfff-109">The following flags can be set:</span></span>
    
<span data-ttu-id="acfff-110">МАПИ_АССОЦИАТЕД</span><span class="sxs-lookup"><span data-stu-id="acfff-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="acfff-111">Вместо стандартной таблицы содержимого следует возвратить связанную таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="acfff-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="acfff-112">Этот флаг используется только для папок.</span><span class="sxs-lookup"><span data-stu-id="acfff-112">This flag is used only with folders.</span></span> <span data-ttu-id="acfff-113">Сообщения, включенные в связанную таблицу содержимого, были созданы с помощью флага МАПИ_АССОЦИАТЕД, установленного в вызове метода [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="acfff-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="acfff-114">Клиенты обычно используют связанную таблицу содержимого для получения форм, представлений и других скрытых сообщений.</span><span class="sxs-lookup"><span data-stu-id="acfff-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="acfff-115">АКЛТАБЛЕ_ФРИБУСИ</span><span class="sxs-lookup"><span data-stu-id="acfff-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="acfff-116">Предоставляет доступ к правам Фригхтсфрибусисимпле и Фригхтсфрибусидетаилед в **пр_мембер_ригхтс**.</span><span class="sxs-lookup"><span data-stu-id="acfff-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="acfff-117">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="acfff-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="acfff-118">**Жетконтентстабле** может успешно вернуть, возможно, перед тем, как таблица стала доступна вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="acfff-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="acfff-119">Если таблица недоступна, выполнение последующих вызовов таблицы может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="acfff-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="acfff-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="acfff-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="acfff-121">ЗаПрашивает возврат столбцов, содержащих строковые данные, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="acfff-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="acfff-122">Если флаг МАПИ_УНИКОДЕ не установлен, строки должны быть возвращены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="acfff-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="acfff-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="acfff-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="acfff-124">Показывает элементы, которые в настоящее время помечены как обратимо удаленные — то есть они находятся на стадии хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="acfff-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="acfff-125">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="acfff-125">_lppTable_</span></span>
  
> <span data-ttu-id="acfff-126">вышли Указатель на указатель на таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="acfff-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="acfff-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acfff-127">Return value</span></span>

<span data-ttu-id="acfff-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="acfff-128">S_OK</span></span> 
  
> <span data-ttu-id="acfff-129">Таблица содержимого успешно получена.</span><span class="sxs-lookup"><span data-stu-id="acfff-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="acfff-130">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="acfff-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="acfff-131">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="acfff-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="acfff-132">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="acfff-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="acfff-133">Контейнер не имеет содержимого и не может предоставить таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="acfff-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="acfff-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="acfff-134">Remarks</span></span>

<span data-ttu-id="acfff-135">Метод **IMAPIContainer:: жетконтентстабле** возвращает указатель на таблицу содержимого контейнера.</span><span class="sxs-lookup"><span data-stu-id="acfff-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="acfff-136">Таблица содержимого содержит сводную информацию об объектах в контейнере.</span><span class="sxs-lookup"><span data-stu-id="acfff-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="acfff-137">Таблицы содержимого содержат продолжительные наборы столбцов.</span><span class="sxs-lookup"><span data-stu-id="acfff-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="acfff-138">Полный список обязательных и необязательных столбцов в таблицах содержимого представлен в [](contents-tables.md)статье оглавления.</span><span class="sxs-lookup"><span data-stu-id="acfff-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="acfff-139">Некоторые контейнеры могут не иметь содержимого.</span><span class="sxs-lookup"><span data-stu-id="acfff-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="acfff-140">Эти контейнеры возвращают МАПИ_Е_НО_СУППОРТ из реализации **жетконтентстабле**.</span><span class="sxs-lookup"><span data-stu-id="acfff-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="acfff-141">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="acfff-141">Notes to implementers</span></span>

<span data-ttu-id="acfff-142">Если вы поддерживаете таблицу содержимого для контейнера, необходимо также выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="acfff-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="acfff-143">Поддерживает вызовы метода контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для открытия свойства **пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="acfff-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="acfff-144">Возвращает **пр_контаинер_контентс** в ответ на вызов объекта контейнера</span><span class="sxs-lookup"><span data-stu-id="acfff-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="acfff-145">[IMAPIProp:: PROPS](imapiprop-getprops.md) и [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) методы.</span><span class="sxs-lookup"><span data-stu-id="acfff-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="acfff-146">Реализация этого метода В удаленном поставщике транспорта должна возвращать указатель на метод [IMAPITable: IUnknown](imapitableiunknown.md) в параметре _пптабле_ , переданном в метод **жетконтентстабле** .</span><span class="sxs-lookup"><span data-stu-id="acfff-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="acfff-147">Если у поставщика транспорта есть существующая таблица содержимого, достаточно возвратить указатель на него.</span><span class="sxs-lookup"><span data-stu-id="acfff-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="acfff-148">В противном случае этот метод должен создать новый объект [IMAPITable: IUnknown](imapitableiunknown.md) , заполнить таблицу заголовками сообщений (если они доступны) и возвратить указатель на новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="acfff-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="acfff-149">Метод [итабледата:: хржетвиев](itabledata-hrgetview.md) полезен для создания возвращаемого значения и сохранения указателя таблицы в параметре _пптабле_ .</span><span class="sxs-lookup"><span data-stu-id="acfff-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="acfff-150">Таблица Contents должна поддерживать по крайней мере следующие столбцы свойств:</span><span class="sxs-lookup"><span data-stu-id="acfff-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="acfff-151">**Пр_ентрид** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-152">**Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-153">**Пр_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-154">**Пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-155">**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-156">**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-157">**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-158">**Пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-159">**Пр_приорити** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-160">**Пр_импортанце** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-161">**Пр_сенситивити** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-162">**Пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-163">**Пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-164">**Пр_мессаже_довнлоад_тиме** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-165">**Пр_хасаттач** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-166">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-167">**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="acfff-168">**Пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acfff-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="acfff-169">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="acfff-169">Notes to callers</span></span>

<span data-ttu-id="acfff-170">Столбцы таблицы строковых и двоичных содержимого можно усечь.</span><span class="sxs-lookup"><span data-stu-id="acfff-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="acfff-171">Как правило, поставщики возвращают 255 символов.</span><span class="sxs-lookup"><span data-stu-id="acfff-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="acfff-172">Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усекается, если длина столбца составляет 255 или 510 байт.</span><span class="sxs-lookup"><span data-stu-id="acfff-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="acfff-173">Вы всегда можете получить полное значение сокращенного столбца (при необходимости) непосредственно из объекта, используя его идентификатор записи, чтобы открыть его, а затем вызвать метод **IMAPIProp::** /PROPS.</span><span class="sxs-lookup"><span data-stu-id="acfff-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="acfff-174">В зависимости от реализации поставщика, ограничения и операции сортировки могут применяться ко всей строке или к усеченной версии этой строки.</span><span class="sxs-lookup"><span data-stu-id="acfff-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="acfff-175">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="acfff-175">MFCMAPI reference</span></span>

<span data-ttu-id="acfff-176">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="acfff-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="acfff-177">**Файл**</span><span class="sxs-lookup"><span data-stu-id="acfff-177">**File**</span></span>|<span data-ttu-id="acfff-178">**Функция**</span><span class="sxs-lookup"><span data-stu-id="acfff-178">**Function**</span></span>|<span data-ttu-id="acfff-179">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="acfff-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="acfff-180">Контентстабледиалог. cpp</span><span class="sxs-lookup"><span data-stu-id="acfff-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="acfff-181">Кконтентстабледлг:: Кконтентстабледлг</span><span class="sxs-lookup"><span data-stu-id="acfff-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="acfff-182">Класс **кконтентстабледлг** использует **жетконтентстабле** для получения записей в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="acfff-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="acfff-183">См. также</span><span class="sxs-lookup"><span data-stu-id="acfff-183">See also</span></span>



[<span data-ttu-id="acfff-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="acfff-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="acfff-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="acfff-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="acfff-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="acfff-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="acfff-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="acfff-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="acfff-188">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="acfff-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="acfff-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="acfff-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="acfff-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="acfff-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

