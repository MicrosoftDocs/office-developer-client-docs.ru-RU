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
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="bcd4c-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="bcd4c-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="bcd4c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcd4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcd4c-105">Возвращает идентификатор входа объекта, который предоставляет основное удостоверение сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="bcd4c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bcd4c-106">Parameters</span></span>

 <span data-ttu-id="bcd4c-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bcd4c-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="bcd4c-108">[вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="bcd4c-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bcd4c-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="bcd4c-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="bcd4c-110">[вышел] Указатель на указатель на идентификатор входа объекта, который предоставляет основное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcd4c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcd4c-111">Return value</span></span>

<span data-ttu-id="bcd4c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcd4c-112">S_OK</span></span> 
  
> <span data-ttu-id="bcd4c-113">Первичный идентификатор был успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="bcd4c-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="bcd4c-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="bcd4c-115">Вызов удался, но основного удостоверения для сеанса не существует.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="bcd4c-116">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bcd4c-117">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bcd4c-118">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcd4c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="bcd4c-119">Remarks</span></span>

<span data-ttu-id="bcd4c-120">Метод **IMAPISession::QueryIdentity** извлекает основное удостоверение для текущего сеанса и возвращает значение через параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="bcd4c-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="bcd4c-121">Основной идентификатор — это объект, как правило, пользователь обмена сообщениями, который представляет пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="bcd4c-122">_lppEntryID_ возвращает основное удостоверение объекта [IMailUser,](imailuserimapiprop.md) который также хранится в качестве свойства [PidTagEntryID.](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="bcd4c-123">Значение, возвращенное в _lppEntryID,_ можно использовать для открытия объекта **IMailUser** с помощью [IMAPISession::OpenEntry.](imapisession-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="bcd4c-124">Хотя многие поставщики услуг в нескольких службах сообщений могут предоставлять основные удостоверения для сеанса, MAPI назначает одного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="bcd4c-125">Поставщик услуг, который поставляет основные удостоверения, задает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="bcd4c-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="bcd4c-126">Флаг STATUS_PRIMARY_IDENTITY в **свойстве PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="bcd4c-127">Свойство **PR_IDENTITY_DISPLAY** [(PidTagIdentityDisplay).](pidtagidentitydisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="bcd4c-128">Свойство **PR_IDENTITY_ENTRYID** [(PidTagIdentityEntryId).](pidtagidentityentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="bcd4c-129">Свойство **PR_IDENTITY_SEARCH_KEY** [(PidTagIdentitySearchKey).](pidtagidentitysearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="bcd4c-130">Если поставщик услуг, который поставляет основные удостоверения, принадлежит службе сообщений, другие поставщики услуг в службе сообщений также PR_IDENTITY свойства.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="bcd4c-131">Эти свойства публикуются в таблице состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="bcd4c-132">По возможности **объект QueryId возвращает** значение для **свойства** PR_IDENTITY_ENTRYID из строки состояния, помеченной STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="bcd4c-133">Если свойство **PR_IDENTITY_ENTRYID** отсутствует в основной строке удостоверений, **объект QueryIdentity** возвращает идентификатор одноавтной записи, построенный с другими сведениями из этой строки.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="bcd4c-134">Если флаг STATUS_PRIMARY_IDENTITY отсутствует во всех  столбцах PR_RESOURCE_FLAG в таблице состояния, **queryIdentity** возвращает первый идентификатор записи, который он находит.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="bcd4c-135">Когда нет подходящего идентификатора записи для возврата, **queryIdentity** успешно с предупреждением MAPI_W_NO_SERVICE и указывает  _lppEntryID_ на жесткий кодовый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bcd4c-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bcd4c-136">Notes to callers</span></span>

<span data-ttu-id="bcd4c-137">Вы можете вызвать [метод IMsgServiceAdmin::SetPrimaryIdentity,](imsgserviceadmin-setprimaryidentity.md) чтобы назначить службе сообщений задачу поставки основного удостоверения сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="bcd4c-138">Еще один способ получения основного удостоверения — поиск  таблицы состояния строки с PR_RESOURCE_FLAGS столбцов, STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="bcd4c-139">Дополнительные сведения об этом альтернативном способе получения сведений о удостоверениях см. в таблице [status Table и Status Objects.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="bcd4c-140">После завершения использования идентификатора записи для основного удостоверения, возвращенного **объектом QueryIdentity,** освободите его память, позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="bcd4c-141">Дополнительные сведения о удостоверении в целом см. в [главной идентификации MAPI.](mapi-primary-identity.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="bcd4c-142">Дополнительные сведения о том, как получить удостоверение сеанса MAPI, см. в дополнительных сведениях о том, как получить удостоверение основного поставщика и удостоверение [поставщика.](retrieving-primary-and-provider-identity.md)</span><span class="sxs-lookup"><span data-stu-id="bcd4c-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bcd4c-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bcd4c-143">MFCMAPI reference</span></span>

<span data-ttu-id="bcd4c-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bcd4c-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bcd4c-145">**File**</span></span>|<span data-ttu-id="bcd4c-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bcd4c-146">**Function**</span></span>|<span data-ttu-id="bcd4c-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bcd4c-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcd4c-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="bcd4c-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="bcd4c-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="bcd4c-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="bcd4c-150">MFCMAPI использует **метод IMAPISession::QueryIdentity** для открытия записи адресной книги для основного удостоверения сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcd4c-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcd4c-151">См. также</span><span class="sxs-lookup"><span data-stu-id="bcd4c-151">See also</span></span>



[<span data-ttu-id="bcd4c-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="bcd4c-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="bcd4c-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="bcd4c-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="bcd4c-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bcd4c-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bcd4c-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcd4c-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="bcd4c-156">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="bcd4c-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bcd4c-157">Основной идентификатор MAPI</span><span class="sxs-lookup"><span data-stu-id="bcd4c-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="bcd4c-158">Повторное иждивение удостоверения основного поставщика и поставщика</span><span class="sxs-lookup"><span data-stu-id="bcd4c-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="bcd4c-159">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="bcd4c-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="bcd4c-160">Объекты таблицы состояния и состояния</span><span class="sxs-lookup"><span data-stu-id="bcd4c-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

