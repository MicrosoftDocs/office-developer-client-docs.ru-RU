---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418024"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="ea9b7-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ea9b7-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="ea9b7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea9b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea9b7-105">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="ea9b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea9b7-106">Parameters</span></span>

<span data-ttu-id="ea9b7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ea9b7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ea9b7-108">[in] Handle to the parent window of the common address dialog box and other related displays.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="ea9b7-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ea9b7-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="ea9b7-110">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ea9b7-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="ea9b7-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ea9b7-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="ea9b7-112">[in] Указатель на идентификатор записи для открываемого хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="ea9b7-113">Параметр  _lpEntryID_ не должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="ea9b7-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ea9b7-114">_lpInterface_</span></span>
  
> <span data-ttu-id="ea9b7-115">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="ea9b7-116">При передаче NULL параметр _lppMDB_ возвращает указатель на стандартный интерфейс для хранения сообщений (**IMsgStore).**</span><span class="sxs-lookup"><span data-stu-id="ea9b7-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="ea9b7-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ea9b7-117">_ulFlags_</span></span>
  
> <span data-ttu-id="ea9b7-118">[in] Битоваяmas флагов, которая управляет открытием объекта.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="ea9b7-119">Можно использовать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ea9b7-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="ea9b7-120">MAPI_BEST_ACCESS: запрашивает, чтобы хранилище сообщений было открыто с максимальным разрешенным для пользователя сетевым разрешением и максимальным разрешением клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="ea9b7-121">Например, если у клиента есть разрешение на чтение и записи, хранилище сообщений должно быть открыто с разрешением на чтение и записи; Если у клиента есть разрешение только на чтение, хранилище сообщений должно быть открыто с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="ea9b7-122">MAPI_DEFERRED_ERRORS: позволяет **OpenMsgStore** успешно возвращаться, возможно, до того, как хранилище сообщений будет полностью доступно вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="ea9b7-123">Если хранилище сообщений не доступно, последующий вызов объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="ea9b7-124">MDB NO_DIALOG: предотвращает отображение диалогов для \_ логотипа.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="ea9b7-125">Если этот флаг установлен, а **в OpenMsgStore** недостаточно сведений о конфигурации, чтобы открыть хранилище сообщений без помощи пользователя, он возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="ea9b7-126">Если этот флажок не установлен, поставщик store сообщений может отправить пользователю запрос на исправление имени или пароля, а также выполнить другие действия, необходимые для установления подключения к хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="ea9b7-127">MDB NO_MAIL: хранилище сообщений не должно использоваться для отправки \_ или получения почты.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="ea9b7-128">Если этот флаг установлен, MAPI не уведомляет пул mapI о том, что это хранилище сообщений открыто.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="ea9b7-129">MDB ONLINE: в режиме кэшации Exchange клиент или поставщик услуг может вызвать этот метод с помощью MDB_ONLINE переопределять подключение к локальному хранилище сообщений и открывать хранилище на удаленном \_ сервере.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="ea9b7-130">Невозможно открыть хранилище Exchange в режиме кэшации и в режиме без кэшации одновременно в одном сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="ea9b7-131">Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="ea9b7-132">MDB_TEMPORARY: сообщает MAPI, что хранилище сообщений не является постоянным и не должно быть добавлено в таблицу хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="ea9b7-133">Этот флаг используется для входа в хранилище сообщений, чтобы получить сведения из раздела профиля программным путем.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="ea9b7-134">MDB_WRITE: запрашивает разрешение на чтение и записи в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="ea9b7-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="ea9b7-135">_lppMDB_</span></span>
  
> <span data-ttu-id="ea9b7-136">[out] Указатель на указатель на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea9b7-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea9b7-137">Return value</span></span>

<span data-ttu-id="ea9b7-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea9b7-138">S_OK</span></span> 
  
> <span data-ttu-id="ea9b7-139">Хранилище сообщений успешно открыто.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="ea9b7-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ea9b7-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ea9b7-141">Предпринята попытка доступа к хранилище сообщений, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="ea9b7-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ea9b7-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ea9b7-143">Хранилище сообщений, обозначенное  _lpEntryID,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="ea9b7-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="ea9b7-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="ea9b7-145">Сервер не настроен для поддержки кодовой страницы клиента.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="ea9b7-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="ea9b7-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="ea9b7-147">Сервер не настроен для поддержки сведений о региональных настройках клиента.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="ea9b7-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="ea9b7-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="ea9b7-149">Вызов был успешным, но у поставщика хранения сообщений есть сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="ea9b7-150">При возврате этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ea9b7-151">Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="ea9b7-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="ea9b7-152">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="ea9b7-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ea9b7-153">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="ea9b7-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea9b7-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea9b7-154">Remarks</span></span>

<span data-ttu-id="ea9b7-155">Метод **IMAPISession::OpenMsgStore** открывает определенное хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ea9b7-156">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ea9b7-156">Notes to callers</span></span>

<span data-ttu-id="ea9b7-157">Уровень разрешений по умолчанию для хранилищ сообщений — только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="ea9b7-158">Если вы установите флаг MDB_WRITE, возможно, вам все равно не будет предоставлено разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="ea9b7-159">Окончательный уровень доступа, назначаемого MAPI хранилищем сообщений, зависит от вашего уровня разрешений, самого магазина сообщений и поставщика.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="ea9b7-160">Если вызвать **OpenMsgStore,** чтобы открыть хранилище сообщений с разрешением только на чтение, произойдет следующее:</span><span class="sxs-lookup"><span data-stu-id="ea9b7-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="ea9b7-161">В свойстве **PR \_ STORE_SUPPORT_MASK** Store [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)MODIFY_OK и \_ CREATE_OK \_ store.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="ea9b7-162">Вызовы для открытия одного из сообщений или папок в хранилище сообщений с помощью [IMAPISession::OpenEntry](imapisession-openentry.md) с установленным MAPI_MODIFY не удастся.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="ea9b7-163">Вызовы для открытия одного из свойств сообщений или папок в хранилище сообщений с помощью [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с флагом MAPI_MODIFY не удастся.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="ea9b7-164">Вызовы любого из следующих методов не удастся:</span><span class="sxs-lookup"><span data-stu-id="ea9b7-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="ea9b7-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="ea9b7-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="ea9b7-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="ea9b7-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="ea9b7-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ea9b7-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="ea9b7-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ea9b7-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="ea9b7-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ea9b7-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="ea9b7-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="ea9b7-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="ea9b7-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="ea9b7-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="ea9b7-172">Вызовы следующих методов не удастся, если место назначения для скопированного сообщения предназначено только для чтения, независимо от того, является ли назначение таким же, как хранилище исходных сообщений или другое хранилище, предназначенное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="ea9b7-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ea9b7-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="ea9b7-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ea9b7-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="ea9b7-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="ea9b7-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ea9b7-176">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ea9b7-176">MFCMAPI reference</span></span>

<span data-ttu-id="ea9b7-177">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ea9b7-178">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ea9b7-178">**File**</span></span>|<span data-ttu-id="ea9b7-179">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ea9b7-179">**Function**</span></span>|<span data-ttu-id="ea9b7-180">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ea9b7-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea9b7-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ea9b7-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ea9b7-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ea9b7-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="ea9b7-183">MFCMAPI использует метод **IMAPISession::OpenMsgStore** для открытия хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea9b7-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea9b7-184">См. также</span><span class="sxs-lookup"><span data-stu-id="ea9b7-184">See also</span></span>

- [<span data-ttu-id="ea9b7-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ea9b7-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="ea9b7-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ea9b7-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="ea9b7-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ea9b7-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="ea9b7-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="ea9b7-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="ea9b7-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea9b7-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="ea9b7-190">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="ea9b7-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="ea9b7-191">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="ea9b7-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

