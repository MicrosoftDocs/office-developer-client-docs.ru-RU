---
title: имаписессионкуеридентити
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
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="b4d77-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d77-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="b4d77-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4d77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4d77-105">Возвращает идентификатор записи объекта, который предоставляет основной идентификатор для сеанса.</span><span class="sxs-lookup"><span data-stu-id="b4d77-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="b4d77-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4d77-106">Parameters</span></span>

 <span data-ttu-id="b4d77-107">_лпкбентрид_</span><span class="sxs-lookup"><span data-stu-id="b4d77-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="b4d77-108">вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ .</span><span class="sxs-lookup"><span data-stu-id="b4d77-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b4d77-109">_лппентрид_</span><span class="sxs-lookup"><span data-stu-id="b4d77-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="b4d77-110">вышли Указатель на указатель на идентификатор записи объекта, который предоставляет основное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="b4d77-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4d77-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4d77-111">Return value</span></span>

<span data-ttu-id="b4d77-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4d77-112">S_OK</span></span> 
  
> <span data-ttu-id="b4d77-113">Основное удостоверение успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="b4d77-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="b4d77-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b4d77-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="b4d77-115">Вызов выполнен успешно, но основной идентификатор для этого сеанса отсутствует.</span><span class="sxs-lookup"><span data-stu-id="b4d77-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="b4d77-116">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="b4d77-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b4d77-117">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b4d77-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b4d77-118">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b4d77-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4d77-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4d77-119">Remarks</span></span>

<span data-ttu-id="b4d77-120">Метод **IMAPISession:: куеридентити** получает основное удостоверение для текущего сеанса и возвращает значение с помощью параметра _лппентрид_ .</span><span class="sxs-lookup"><span data-stu-id="b4d77-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="b4d77-121">Основной идентификатор — это объект, обычно пользователь обмена сообщениями, представляющий пользователя сеанса.</span><span class="sxs-lookup"><span data-stu-id="b4d77-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="b4d77-122">_лппентрид_ Возвращает основной идентификатор объекта [имаилусер](imailuserimapiprop.md) , который также хранится в свойстве [PidTagEntryID](pidtagentryid-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b4d77-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="b4d77-123">Значение, возвращаемое в _лппентрид_ , можно использовать для открытия объекта **Имаилусер** с помощью [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b4d77-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="b4d77-124">Несмотря на то, что многие поставщики служб в нескольких службах сообщений могут предоставлять основной идентификатор сеанса, MAPI определяет одного поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="b4d77-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="b4d77-125">Поставщик услуг, который предоставляет первичный идентификатор, задает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="b4d77-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="b4d77-126">Флаг STATUS_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d77-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b4d77-127">Свойство **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d77-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b4d77-128">Свойство **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d77-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="b4d77-129">Свойство **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d77-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="b4d77-130">Если поставщик услуг, предоставляющий основной идентификатор, принадлежит службе сообщений, другие поставщики услуг в службе сообщений также устанавливают свойства PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b4d77-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="b4d77-131">Эти свойства публикуются в таблице состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="b4d77-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="b4d77-132">Если это возможно, **куеридентити** возвращает значение свойства **PR_IDENTITY_ENTRYID** из строки состояния с тегом STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="b4d77-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b4d77-133">Если в строке основного удостоверения отсутствует свойство **PR_IDENTITY_ENTRYID** , **куеридентити** возвращает идентификатор одноразовой записи, построенный с другими сведениями из этой строки.</span><span class="sxs-lookup"><span data-stu-id="b4d77-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="b4d77-134">Если флаг STATUS_PRIMARY_IDENTITY отсутствует во всех столбцах **PR_RESOURCE_FLAG** в таблице status, **куеридентити** возвращает первый найденный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b4d77-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="b4d77-135">Если нет подходящего идентификатора записи, **куеридентити** завершается с предупреждением MAPI_W_NO_SERVICE и указывает _лппентрид_ на жестко заданный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="b4d77-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b4d77-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b4d77-136">Notes to callers</span></span>

<span data-ttu-id="b4d77-137">Вы можете вызвать метод [имсгсервицеадмин:: сетпримаридентити](imsgserviceadmin-setprimaryidentity.md) , чтобы назначить службе сообщений задачу предоставления основного удостоверения сеанса.</span><span class="sxs-lookup"><span data-stu-id="b4d77-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="b4d77-138">Другой способ получения основного идентификатора — Поиск строки со столбцами **PR_RESOURCE_FLAGS** , для которых задано значение STATUS_PRIMARY_IDENTITY, в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="b4d77-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="b4d77-139">Дополнительные сведения об этом альтернативном способе получения сведений об удостоверении можно узнать в статье [Status Table and Status Objects](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b4d77-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="b4d77-140">По завершении использования идентификатора записи для основного удостоверения, возвращенного функцией **куеридентити**, освободите его память, вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b4d77-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b4d77-141">Для получения дополнительных сведений об удостоверении в разделе General ( [основной идентификатор MAPI](mapi-primary-identity.md)).</span><span class="sxs-lookup"><span data-stu-id="b4d77-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="b4d77-142">Дополнительные сведения о получении удостоверения сеанса MAPI приведены в статье [Получение основного удостоверения и идентификатора поставщика](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="b4d77-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b4d77-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b4d77-143">MFCMAPI reference</span></span>

<span data-ttu-id="b4d77-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b4d77-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b4d77-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b4d77-145">**File**</span></span>|<span data-ttu-id="b4d77-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b4d77-146">**Function**</span></span>|<span data-ttu-id="b4d77-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b4d77-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4d77-148">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="b4d77-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b4d77-149">Кмаиндлг:: Онкуеридентити</span><span class="sxs-lookup"><span data-stu-id="b4d77-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="b4d77-150">MFCMAPI использует метод **IMAPISession:: куеридентити** , чтобы открыть запись адресной книги для основного удостоверения сеанса.</span><span class="sxs-lookup"><span data-stu-id="b4d77-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4d77-151">См. также</span><span class="sxs-lookup"><span data-stu-id="b4d77-151">See also</span></span>



[<span data-ttu-id="b4d77-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b4d77-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="b4d77-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="b4d77-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="b4d77-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b4d77-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b4d77-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4d77-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b4d77-156">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="b4d77-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b4d77-157">Основной идентификатор MAPI</span><span class="sxs-lookup"><span data-stu-id="b4d77-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="b4d77-158">Получение основного удостоверения и удостоверения поставщика</span><span class="sxs-lookup"><span data-stu-id="b4d77-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="b4d77-159">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="b4d77-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="b4d77-160">Объекты "таблица состояния" и "состояние"</span><span class="sxs-lookup"><span data-stu-id="b4d77-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

