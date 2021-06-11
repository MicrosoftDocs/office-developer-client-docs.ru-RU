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
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="78b6b-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="78b6b-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="78b6b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78b6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78b6b-105">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="78b6b-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="78b6b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="78b6b-106">Parameters</span></span>

<span data-ttu-id="78b6b-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="78b6b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="78b6b-108">[in] Ручка родительского окна общего диалогового окна адресов и других связанных дисплеев.</span><span class="sxs-lookup"><span data-stu-id="78b6b-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="78b6b-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="78b6b-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="78b6b-110">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="78b6b-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="78b6b-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="78b6b-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="78b6b-112">[in] Указатель на идентификатор входа открываемого магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="78b6b-113">Параметр  _lpEntryID_ не должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="78b6b-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="78b6b-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="78b6b-114">_lpInterface_</span></span>
  
> <span data-ttu-id="78b6b-115">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="78b6b-116">Передача NULL заставляет _параметр lppMDB_ возвращать указатель в стандартный интерфейс для магазина **сообщений (IMsgStore).**</span><span class="sxs-lookup"><span data-stu-id="78b6b-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="78b6b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78b6b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="78b6b-118">[in] Битмашка флагов, контролируемая тем, как открывается объект.</span><span class="sxs-lookup"><span data-stu-id="78b6b-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="78b6b-119">Можно использовать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="78b6b-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="78b6b-120">MAPI_BEST_ACCESS. Запрашивает, чтобы хранилище сообщений было открыто с максимальным разрешением сети, разрешенным для пользователя, и с максимальным разрешением клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="78b6b-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="78b6b-121">Например, если у клиента есть разрешение на чтение и написание, магазин сообщений должен быть открыт с разрешения на чтение и написание; если у клиента есть разрешение только для чтения, магазин сообщений должен быть открыт с разрешения только для чтения.</span><span class="sxs-lookup"><span data-stu-id="78b6b-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="78b6b-122">MAPI_DEFERRED_ERRORS: Позволяет **OpenMsgStore** успешно возвращаться, возможно, до того, как хранилище сообщений будет полностью доступно для вызываемого клиента.</span><span class="sxs-lookup"><span data-stu-id="78b6b-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="78b6b-123">Если хранилище сообщений не доступно, последующий вызов объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="78b6b-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="78b6b-124">MDB \_ NO_DIALOG: предотвращает отображение диалогов с логотипом.</span><span class="sxs-lookup"><span data-stu-id="78b6b-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="78b6b-125">Если этот флаг установлен, а **у OpenMsgStore** недостаточно сведений о конфигурации, чтобы открыть хранилище сообщений без помощи пользователя, он возвращается MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="78b6b-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="78b6b-126">Если этот флаг не установлен, поставщик магазина сообщений может побудить пользователя исправить имя или пароль или выполнить другие действия, необходимые для установления подключения к хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="78b6b-127">MDB NO_MAIL: хранилище сообщений не должно использоваться для \_ отправки или получения почты.</span><span class="sxs-lookup"><span data-stu-id="78b6b-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="78b6b-128">Когда этот флаг установлен, MAPI не уведомляет шпалер MAPI о том, что этот хранилище сообщений открывается.</span><span class="sxs-lookup"><span data-stu-id="78b6b-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="78b6b-129">MDB ONLINE. В режиме кэшировать Exchange клиент или поставщик услуг может вызвать этот метод с помощью MDB_ONLINE переопределения подключения к локальному хранилище сообщений и открытия магазина на удаленном \_ сервере.</span><span class="sxs-lookup"><span data-stu-id="78b6b-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="78b6b-130">Нельзя открыть хранилище Exchange в кэшном режиме и в режиме без кэшации одновременно в том же сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="78b6b-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="78b6b-131">Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.</span><span class="sxs-lookup"><span data-stu-id="78b6b-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="78b6b-132">MDB_TEMPORARY: предписывает MAPI, что хранилище сообщений не является постоянным и не должно быть добавлено в таблицу хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="78b6b-133">Этот флаг используется для входа в хранилище сообщений, чтобы получить сведения программным образом из раздела профилей.</span><span class="sxs-lookup"><span data-stu-id="78b6b-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="78b6b-134">MDB_WRITE: запрашивает разрешение на чтение и записи в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="78b6b-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="78b6b-135">_lppMDB_</span></span>
  
> <span data-ttu-id="78b6b-136">[вышел] Указатель на указатель магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78b6b-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78b6b-137">Return value</span></span>

<span data-ttu-id="78b6b-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="78b6b-138">S_OK</span></span> 
  
> <span data-ttu-id="78b6b-139">Хранилище сообщений было успешно открыто.</span><span class="sxs-lookup"><span data-stu-id="78b6b-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="78b6b-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="78b6b-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="78b6b-141">Была предпринята попытка доступа к хранилище сообщений, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="78b6b-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="78b6b-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="78b6b-143">Хранилище сообщений, указанный  _lpEntryID,_ не существует.</span><span class="sxs-lookup"><span data-stu-id="78b6b-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="78b6b-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="78b6b-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="78b6b-145">Сервер не настроен для поддержки страницы кода клиента.</span><span class="sxs-lookup"><span data-stu-id="78b6b-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="78b6b-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="78b6b-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="78b6b-147">Сервер не настроен для поддержки сведений о локальном уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="78b6b-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="78b6b-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="78b6b-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="78b6b-149">Вызов удался, но у поставщика магазина сообщений есть сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="78b6b-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="78b6b-150">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="78b6b-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="78b6b-151">Чтобы получить сведения об ошибках от поставщика, позвоните по [методу IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="78b6b-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="78b6b-152">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="78b6b-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="78b6b-153">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="78b6b-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78b6b-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="78b6b-154">Remarks</span></span>

<span data-ttu-id="78b6b-155">Метод **IMAPISession::OpenMsgStore** открывает определенный магазин сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="78b6b-156">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="78b6b-156">Notes to callers</span></span>

<span data-ttu-id="78b6b-157">Уровень разрешений по умолчанию для магазинов сообщений является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="78b6b-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="78b6b-158">Если вы установите флаг MDB_WRITE, вам все равно может не быть предоставлено разрешение на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="78b6b-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="78b6b-159">Конечный уровень доступа, который MAPI назначает в хранилище сообщений, зависит от уровня разрешений, самого магазина сообщений и поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="78b6b-160">Если вы **позвоните в OpenMsgStore,** чтобы открыть хранилище сообщений с разрешения только для чтения, произойдет следующее:</span><span class="sxs-lookup"><span data-stu-id="78b6b-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="78b6b-161">Pr-STORE_SUPPORT_MASK **магазина \_** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)не будет иметь набор MODIFY_OK store \_ \_ CREATE_OK.</span><span class="sxs-lookup"><span data-stu-id="78b6b-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="78b6b-162">Вызовы для открытия одного из сообщений или папок магазина сообщений с помощью [IMAPISession::OpenEntry](imapisession-openentry.md) с набором флага MAPI_MODIFY не удастся.</span><span class="sxs-lookup"><span data-stu-id="78b6b-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="78b6b-163">Вызовы для открытия одного из свойств сообщений или папок магазина сообщений с помощью [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с флагом MAPI_MODIFY не удастся.</span><span class="sxs-lookup"><span data-stu-id="78b6b-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="78b6b-164">Вызовы к любому из следующих методов сбой:</span><span class="sxs-lookup"><span data-stu-id="78b6b-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="78b6b-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="78b6b-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="78b6b-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="78b6b-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="78b6b-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="78b6b-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="78b6b-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="78b6b-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="78b6b-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="78b6b-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="78b6b-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="78b6b-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="78b6b-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="78b6b-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="78b6b-172">Вызовы к следующим методам не будут работать, если предназначение для скопированного сообщения только для чтения, является ли пункт назначения таким же, как хранилище исходных сообщений или другой магазин только для чтения.</span><span class="sxs-lookup"><span data-stu-id="78b6b-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="78b6b-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="78b6b-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="78b6b-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="78b6b-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="78b6b-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="78b6b-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="78b6b-176">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="78b6b-176">MFCMAPI reference</span></span>

<span data-ttu-id="78b6b-177">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="78b6b-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78b6b-178">**Файл**</span><span class="sxs-lookup"><span data-stu-id="78b6b-178">**File**</span></span>|<span data-ttu-id="78b6b-179">**Функция**</span><span class="sxs-lookup"><span data-stu-id="78b6b-179">**Function**</span></span>|<span data-ttu-id="78b6b-180">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="78b6b-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78b6b-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="78b6b-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="78b6b-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="78b6b-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="78b6b-183">MFCMAPI использует **метод IMAPISession::OpenMsgStore** для открытия магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="78b6b-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78b6b-184">См. также</span><span class="sxs-lookup"><span data-stu-id="78b6b-184">See also</span></span>

- [<span data-ttu-id="78b6b-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="78b6b-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="78b6b-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="78b6b-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="78b6b-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="78b6b-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="78b6b-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="78b6b-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="78b6b-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="78b6b-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="78b6b-190">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="78b6b-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="78b6b-191">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="78b6b-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

