---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428223"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="e5a64-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e5a64-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="e5a64-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5a64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5a64-105">Возвращает идентификатор записи объекта, который предоставляет основное удостоверение для сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5a64-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e5a64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5a64-106">Parameters</span></span>

 <span data-ttu-id="e5a64-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e5a64-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="e5a64-108">[out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="e5a64-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e5a64-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="e5a64-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="e5a64-110">[out] Указатель на указатель на идентификатор записи объекта, который предоставляет основное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="e5a64-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5a64-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5a64-111">Return value</span></span>

<span data-ttu-id="e5a64-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5a64-112">S_OK</span></span> 
  
> <span data-ttu-id="e5a64-113">Основное удостоверение успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="e5a64-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="e5a64-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e5a64-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="e5a64-115">Вызов был успешным, но основного удостоверения для сеанса не существует.</span><span class="sxs-lookup"><span data-stu-id="e5a64-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="e5a64-116">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="e5a64-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e5a64-117">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="e5a64-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e5a64-118">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5a64-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5a64-119">Remarks</span></span>

<span data-ttu-id="e5a64-120">Метод **IMAPISession::QueryIdentity** извлекает основное удостоверение для текущего сеанса и возвращает значение с помощью параметра _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="e5a64-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="e5a64-121">Основное удостоверение — это объект, как правило, пользователь обмена сообщениями, который представляет пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5a64-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="e5a64-122">_lppEntryID_ возвращает основное удостоверение для объекта [IMailUser,](imailuserimapiprop.md) которое также хранится в качестве свойства [PidTagEntryID.](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="e5a64-123">Значение, возвращенное в _lppEntryID,_ можно использовать для открытия объекта **IMailUser** с помощью [IMAPISession::OpenEntry.](imapisession-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="e5a64-124">Хотя многие поставщики услуг в нескольких службах сообщений могут предоставлять основное удостоверение для сеанса, MAPI назначает одного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e5a64-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="e5a64-125">Поставщик услуг, который обеспечивает основное удостоверение, задает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="e5a64-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="e5a64-126">Флаг STATUS_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e5a64-127">Свойство **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay).](pidtagidentitydisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e5a64-128">Свойство **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId).](pidtagidentityentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e5a64-129">Свойство **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey).](pidtagidentitysearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="e5a64-130">Если поставщик услуг, который передает основное удостоверение, принадлежит службе сообщений, другие поставщики услуг в службе сообщений также PR_IDENTITY свойства.</span><span class="sxs-lookup"><span data-stu-id="e5a64-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="e5a64-131">Эти свойства публикуются в таблице состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5a64-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="e5a64-132">По возможности **QueryIdentity** возвращает значение  свойства PR_IDENTITY_ENTRYID из строки состояния, помеченной тегом STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e5a64-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="e5a64-133">Если свойство **PR_IDENTITY_ENTRYID** отсутствует в основной строке удостоверения, **QueryIdentity** возвращает идентификатор однорахной записи, построенный с другими сведениями из этой строки.</span><span class="sxs-lookup"><span data-stu-id="e5a64-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="e5a64-134">Если флаг STATUS_PRIMARY_IDENTITY отсутствует во всех  столбцах PR_RESOURCE_FLAG таблицы состояния, **QueryIdentity** возвращает идентификатор первой записи, которую он находит.</span><span class="sxs-lookup"><span data-stu-id="e5a64-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="e5a64-135">Если не существует соответствующего идентификатора записи для возврата, **QueryIdentity** успешно с предупреждением MAPI_W_NO_SERVICE и указывает  _lppEntryID_ жестко заданный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="e5a64-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e5a64-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e5a64-136">Notes to callers</span></span>

<span data-ttu-id="e5a64-137">Можно вызвать метод [IMsgServiceAdmin::SetPrimaryIdentity,](imsgserviceadmin-setprimaryidentity.md) чтобы назначить службе сообщений задачу по присвоению основного удостоверения сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5a64-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="e5a64-138">Еще один способ получить основное удостоверение — поиск  в таблице состояния строки с PR_RESOURCE_FLAGS столбцов, для STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e5a64-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="e5a64-139">Дополнительные сведения об этом альтернативном способе получения сведений об удостоверениях см. в таблице ["Состояние" и "Объекты состояния".](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="e5a64-140">После завершения использования идентификатора записи для основного удостоверения, возвращаемого **QueryIdentity,** освободите память, вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="e5a64-141">Дополнительные сведения об удостоверении в целом см. в основном удостоверении [MAPI.](mapi-primary-identity.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="e5a64-142">Дополнительные сведения о том, как получить удостоверение сеанса MAPI, см. в этой [теме.](retrieving-primary-and-provider-identity.md)</span><span class="sxs-lookup"><span data-stu-id="e5a64-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e5a64-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e5a64-143">MFCMAPI reference</span></span>

<span data-ttu-id="e5a64-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e5a64-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e5a64-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e5a64-145">**File**</span></span>|<span data-ttu-id="e5a64-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e5a64-146">**Function**</span></span>|<span data-ttu-id="e5a64-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e5a64-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5a64-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e5a64-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e5a64-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e5a64-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="e5a64-150">MFCMAPI использует метод **IMAPISession::QueryIdentity** для открытия записи адресной книги для основного удостоверения сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5a64-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5a64-151">См. также</span><span class="sxs-lookup"><span data-stu-id="e5a64-151">See also</span></span>



[<span data-ttu-id="e5a64-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e5a64-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="e5a64-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="e5a64-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="e5a64-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e5a64-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e5a64-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5a64-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e5a64-156">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="e5a64-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e5a64-157">Основное удостоверение MAPI</span><span class="sxs-lookup"><span data-stu-id="e5a64-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="e5a64-158">Искомые удостоверения основного и поставщика</span><span class="sxs-lookup"><span data-stu-id="e5a64-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="e5a64-159">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="e5a64-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="e5a64-160">Таблица состояния и объекты состояния</span><span class="sxs-lookup"><span data-stu-id="e5a64-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

