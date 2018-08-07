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
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809076"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="5a89f-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="5a89f-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="5a89f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a89f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a89f-105">Открывает хранилища сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="5a89f-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="5a89f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a89f-106">Parameters</span></span>

<span data-ttu-id="5a89f-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5a89f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5a89f-108">[in] Дескриптор родительского окна стандартным диалоговым окном адрес и других, связанных с отображает.</span><span class="sxs-lookup"><span data-stu-id="5a89f-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="5a89f-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5a89f-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="5a89f-110">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5a89f-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="5a89f-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5a89f-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="5a89f-112">[in] Указатель на идентификатор записи хранилища сообщение, которое требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="5a89f-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="5a89f-113">Параметр _lpEntryID_ не должна быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5a89f-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="5a89f-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5a89f-114">_lpInterface_</span></span>
  
> <span data-ttu-id="5a89f-115">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к хранилищу данных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="5a89f-116">Значение NULL вызывает параметр _lppMDB_ возвращает указатель на стандартный интерфейс для хранилища сообщений (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="5a89f-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="5a89f-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a89f-117">_ulFlags_</span></span>
  
> <span data-ttu-id="5a89f-118">[in] Битовая маска флаги, который определяет способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="5a89f-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="5a89f-119">Можно использовать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="5a89f-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="5a89f-120">MAPI_BEST_ACCESS: Запросы открыть хранилище сообщений с разрешениями максимальное сетевое разрешено для пользователя и максимальное число клиентов разрешения приложения.</span><span class="sxs-lookup"><span data-stu-id="5a89f-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="5a89f-121">Например если клиент имеет разрешение на чтение и запись, хранилища сообщений должен быть открыт с разрешением на чтение и запись; Если клиент имеет разрешение на чтение, хранилище сообщений должен быть открыт с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5a89f-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="5a89f-122">MAPI_DEFERRED_ERRORS: Разрешает **OpenMsgStore** для возврата успешно, возможно перед сообщением хранилища доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="5a89f-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="5a89f-123">Если хранилище сообщений недоступен, вызов последующих объектов может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="5a89f-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="5a89f-124">MDB\_NO_DIALOG: не отображать диалоговые окна входа в систему.</span><span class="sxs-lookup"><span data-stu-id="5a89f-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="5a89f-125">Если этот флаг установлен, и **OpenMsgStore** содержит сведения о конфигурации недостаточно для открытия хранилища сообщений без помощи пользователя, он возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="5a89f-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="5a89f-126">Если этот флаг не установлен, поставщик хранения сообщений можно запрашивать у пользователя в нужное имя или пароль или для выполнения других действий, необходимых для установки подключения к хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="5a89f-127">MDB\_NO_MAIL: хранилище сообщений не должна использоваться для отправки или получения почты.</span><span class="sxs-lookup"><span data-stu-id="5a89f-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="5a89f-128">Если этот флаг, MAPI не уведомляет диспетчер очереди MAPI открыта, что хранилища.</span><span class="sxs-lookup"><span data-stu-id="5a89f-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="5a89f-129">MDB\_ONLINE: В режиме кэширования данных Exchange, клиента или поставщика можно вызвать этот метод с MDB_ONLINE переопределение подключения к хранилищу локального сообщения и откройте хранилище на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="5a89f-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="5a89f-130">Не удается открыть хранилища Exchange в режиме кэширования и в режиме без кэширования в то же время, в том же сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a89f-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="5a89f-131">При открытии уже хранилище кэшированных сообщений, либо необходимо закрыть хранилище перед откройте этот флаг или откройте новый сеанс MAPI, где можно открыть в хранилище Exchange на удаленном сервере с помощью этот флаг.</span><span class="sxs-lookup"><span data-stu-id="5a89f-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="5a89f-132">MDB_TEMPORARY: Указывает, что MAPI, что хранилище сообщений не является постоянным и не следует добавлять к таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="5a89f-133">Этот флаг используется для входа в хранилище сообщений, сведения могут быть получены из раздела профиля программными средствами.</span><span class="sxs-lookup"><span data-stu-id="5a89f-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="5a89f-134">MDB_WRITE: Запросы на чтение и запись разрешений для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="5a89f-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="5a89f-135">_lppMDB_</span></span>
  
> <span data-ttu-id="5a89f-136">[out] Указатель на указатель хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a89f-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="5a89f-138">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5a89f-138">S_OK</span></span> 
  
> <span data-ttu-id="5a89f-139">Хранилище сообщений был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="5a89f-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="5a89f-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5a89f-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5a89f-141">Предпринята попытка получить доступ к хранилища сообщений, для которого пользователь имеет недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="5a89f-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5a89f-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5a89f-143">Хранилище сообщений, указанный в параметре _lpEntryID_ не существует.</span><span class="sxs-lookup"><span data-stu-id="5a89f-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="5a89f-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="5a89f-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="5a89f-145">Сервер не настроен для поддержки кодовой страницы клиента.</span><span class="sxs-lookup"><span data-stu-id="5a89f-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="5a89f-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="5a89f-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="5a89f-147">Сервер не настроен для поддержки сведения о языковом стандарте клиента.</span><span class="sxs-lookup"><span data-stu-id="5a89f-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="5a89f-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="5a89f-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="5a89f-149">Вызов завершился успешно, но поставщика хранилища сообщений имеет доступные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5a89f-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="5a89f-150">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="5a89f-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5a89f-151">Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5a89f-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="5a89f-152">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="5a89f-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5a89f-153">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5a89f-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a89f-154">Замечания</span><span class="sxs-lookup"><span data-stu-id="5a89f-154">Remarks</span></span>

<span data-ttu-id="5a89f-155">Метод **IMAPISession::OpenMsgStore** открывает хранилища конкретное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5a89f-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5a89f-156">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5a89f-156">Notes to callers</span></span>

<span data-ttu-id="5a89f-157">Уровень разрешений по умолчанию для хранилищ сообщений доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5a89f-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="5a89f-158">Если значение флага MDB_WRITE, вы по-прежнему может не иметь разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5a89f-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="5a89f-159">Последний уровень доступа, который назначает MAPI для хранилища сообщений, зависит от уровней разрешений, сообщение хранилища себя и поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="5a89f-160">При вызове **OpenMsgStore** , чтобы открыть хранилище сообщений с разрешением только для чтения, произойдет следующее:</span><span class="sxs-lookup"><span data-stu-id="5a89f-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="5a89f-161">Хранилище **связей с Общественностью\_STORE_SUPPORT_MASK** свойство ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), не будут иметь его ХРАНИЛИЩЕ\_MODIFY_OK и ХРАНИЛИЩЕ\_CREATE_OK бит set.</span><span class="sxs-lookup"><span data-stu-id="5a89f-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="5a89f-162">Откройте одну из сообщения или папки хранилища сообщений с помощью [IMAPISession::OpenEntry](imapisession-openentry.md) с установленным флагом MAPI_MODIFY вызовы завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5a89f-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="5a89f-163">Откройте одну из свойств сообщения или папки хранилища сообщений с помощью [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с флагом MAPI_MODIFY вызовы завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5a89f-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="5a89f-164">Вызовы любого из следующих методов произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="5a89f-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="5a89f-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="5a89f-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="5a89f-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="5a89f-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="5a89f-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="5a89f-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="5a89f-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="5a89f-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="5a89f-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="5a89f-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="5a89f-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="5a89f-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="5a89f-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="5a89f-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="5a89f-172">Вызовы следующих методов завершится ошибкой, если назначения для скопированного сообщения доступен только для чтения, ли назначение — то же, что хранилище сообщений источника или другого хранилища только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5a89f-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="5a89f-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="5a89f-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="5a89f-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="5a89f-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="5a89f-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="5a89f-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5a89f-176">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="5a89f-176">MFCMAPI reference</span></span>

<span data-ttu-id="5a89f-177">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="5a89f-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5a89f-178">**����**</span><span class="sxs-lookup"><span data-stu-id="5a89f-178">**File**</span></span>|<span data-ttu-id="5a89f-179">**�������**</span><span class="sxs-lookup"><span data-stu-id="5a89f-179">**Function**</span></span>|<span data-ttu-id="5a89f-180">**�����������**</span><span class="sxs-lookup"><span data-stu-id="5a89f-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a89f-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5a89f-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5a89f-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="5a89f-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="5a89f-183">Mfcmapi (en) использует метод **IMAPISession::OpenMsgStore** для открытия хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a89f-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a89f-184">См. также</span><span class="sxs-lookup"><span data-stu-id="5a89f-184">See also</span></span>

- [<span data-ttu-id="5a89f-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5a89f-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="5a89f-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5a89f-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="5a89f-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5a89f-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="5a89f-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="5a89f-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="5a89f-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a89f-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="5a89f-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5a89f-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="5a89f-191">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="5a89f-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

