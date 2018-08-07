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
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809082"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="e2a5a-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e2a5a-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="e2a5a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2a5a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2a5a-105">Возвращает идентификатор записи объекта, который содержит основной идентификатор для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e2a5a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2a5a-106">Parameters</span></span>

 <span data-ttu-id="e2a5a-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2a5a-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="e2a5a-108">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e2a5a-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e2a5a-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2a5a-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="e2a5a-110">[out] Указатель на указатель на идентификатор записи объекта, который содержит основной идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2a5a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="e2a5a-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e2a5a-112">S_OK</span></span> 
  
> <span data-ttu-id="e2a5a-113">Основной идентификатор успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="e2a5a-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e2a5a-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="e2a5a-115">Вызов завершился успешно, однако это не имеет не основного удостоверения для сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="e2a5a-116">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e2a5a-117">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e2a5a-118">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2a5a-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="e2a5a-119">Remarks</span></span>

<span data-ttu-id="e2a5a-120">Метод **IMAPISession::QueryIdentity** получает основной идентификатор для текущего сеанса и возвращает значение, используя параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e2a5a-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="e2a5a-121">Основной идентификатор является объектом, обычно обмена сообщениями пользователя, представляющий пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="e2a5a-122">_lppEntryID_ возвращает первичный идентификатор объекта [IMailUser](imailuserimapiprop.md) , которые также хранятся как свойство [PidTagEntryID](pidtagentryid-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a5a-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="e2a5a-123">Значение, возвращаемое в _lppEntryID_ можно использовать для открытия объекта **IMailUser** с помощью [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="e2a5a-124">Несмотря на то, что многие поставщики услуг в нескольких служб сообщения можно обеспечить основной идентификатор сеанса, MAPI назначает отдельный поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="e2a5a-125">Поставщик услуг, который предоставляет основной идентификатор задает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="e2a5a-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="e2a5a-126">Флаг STATUS_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e2a5a-127">Свойство **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e2a5a-128">Свойство **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e2a5a-129">Свойство **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="e2a5a-130">Если поставщик услуг, который предоставляет основной идентификатор принадлежит службы сообщений, других поставщиков услуг службы сообщений также необходимо задать свойства PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="e2a5a-131">Эти свойства публикуются в таблице состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="e2a5a-132">Если это возможно **QueryIdentity** возвращает значение для свойства **PR_IDENTITY_ENTRYID** из строки состояния, с STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="e2a5a-133">Если свойство **PR_IDENTITY_ENTRYID** отсутствует в строке основного удостоверения, **QueryIdentity** возвращает идентификатора единичных записей, созданных с помощью прочие сведения из этой строки.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="e2a5a-134">В случае отсутствия из всех **PR_RESOURCE_FLAG** столбцов в таблице состояния флага STATUS_PRIMARY_IDENTITY **QueryIdentity** возвращает первый идентификатор записи, которая будет обнаружен.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="e2a5a-135">Если идентификатор не соответствующие записи для возврата, **QueryIdentity** успешно с предупреждением MAPI_W_NO_SERVICE и _lppEntryID_ , указывает идентификатор жестко записи.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2a5a-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e2a5a-136">Notes to callers</span></span>

<span data-ttu-id="e2a5a-137">Можно вызвать метод [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) для назначения задач предоставления основной идентификатор сеанса службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="e2a5a-138">Другой способ получить основной идентификатор — поиск по ключевым словам в таблице состояния для строки со столбцами **PR_RESOURCE_FLAGS** , задайте значение STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="e2a5a-139">Дополнительные сведения об этой альтернативный способ получения сведений об удостоверениях см в [таблице состояния и состояния объектов](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="e2a5a-140">По окончании с помощью идентификатора записи для основного удостоверения, возвращаемые **QueryIdentity**освободите память путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a5a-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="e2a5a-141">Дополнительные сведения сведения об удостоверениях, как правило, можно [Основного удостоверения MAPI](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="e2a5a-142">Дополнительные сведения о получении идентификатор сеанса MAPI разделе [Извлечение основной и поставщика удостоверений](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="e2a5a-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2a5a-143">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="e2a5a-143">MFCMAPI reference</span></span>

<span data-ttu-id="e2a5a-144">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2a5a-145">**����**</span><span class="sxs-lookup"><span data-stu-id="e2a5a-145">**File**</span></span>|<span data-ttu-id="e2a5a-146">**�������**</span><span class="sxs-lookup"><span data-stu-id="e2a5a-146">**Function**</span></span>|<span data-ttu-id="e2a5a-147">**�����������**</span><span class="sxs-lookup"><span data-stu-id="e2a5a-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2a5a-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e2a5a-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e2a5a-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e2a5a-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="e2a5a-150">Mfcmapi (en) использует метод **IMAPISession::QueryIdentity** для открытия записи адресной книги для основной идентификатор сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2a5a-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2a5a-151">См. также</span><span class="sxs-lookup"><span data-stu-id="e2a5a-151">See also</span></span>



[<span data-ttu-id="e2a5a-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e2a5a-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="e2a5a-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="e2a5a-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="e2a5a-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e2a5a-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e2a5a-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2a5a-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e2a5a-156">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e2a5a-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e2a5a-157">Основной идентификатор MAPI</span><span class="sxs-lookup"><span data-stu-id="e2a5a-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="e2a5a-158">Получение удостоверения поставщика и основного удостоверения</span><span class="sxs-lookup"><span data-stu-id="e2a5a-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="e2a5a-159">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="e2a5a-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="e2a5a-160">Таблица и объекты состояний</span><span class="sxs-lookup"><span data-stu-id="e2a5a-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

