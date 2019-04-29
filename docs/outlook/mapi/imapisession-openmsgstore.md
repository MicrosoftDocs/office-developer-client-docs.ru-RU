---
title: Имаписессионопенмсгсторе
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
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="53d30-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="53d30-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="53d30-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53d30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53d30-105">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для получения доступа.</span><span class="sxs-lookup"><span data-stu-id="53d30-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="53d30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53d30-106">Parameters</span></span>

<span data-ttu-id="53d30-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="53d30-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="53d30-108">возврата Дескриптор родительского окна для диалогового окна общего адреса и других связанных дисплеев.</span><span class="sxs-lookup"><span data-stu-id="53d30-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="53d30-109">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="53d30-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="53d30-110">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="53d30-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="53d30-111">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="53d30-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="53d30-112">возврата Указатель на идентификатор записи хранилища сообщений, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="53d30-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="53d30-113">Параметр _лпентрид_ не должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="53d30-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="53d30-114">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="53d30-114">_lpInterface_</span></span>
  
> <span data-ttu-id="53d30-115">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="53d30-116">При передаче значения NULL параметр _лппмдб_ возвращает указатель на стандартный интерфейс для хранилища сообщений (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="53d30-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="53d30-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53d30-117">_ulFlags_</span></span>
  
> <span data-ttu-id="53d30-118">возврата Битовая маска флагов, определяющих способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="53d30-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="53d30-119">Можно использовать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="53d30-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="53d30-120">МАПИ_БЕСТ_АКЦЕСС: запросы, которые должны быть открыты для хранения сообщений с максимальными разрешениями в сети, разрешенными для пользователя и максимальными разрешениями клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="53d30-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="53d30-121">Например, если у клиента есть разрешение на чтение и запись, необходимо открыть хранилище сообщений с разрешением на чтение и запись; Если клиент имеет разрешение только на чтение, оно должно быть открыто с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="53d30-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="53d30-122">МАПИ_ДЕФЕРРЕД_ЕРРОРС: разрешает успешное возвращение **опенмсгсторе** , возможно, перед тем, как хранилище сообщений будет полностью доступно для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="53d30-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="53d30-123">Если хранилище сообщений недоступно, то выполнение следующего вызова объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="53d30-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="53d30-124">MDB\_Но_диалог: запрещает отображение диалоговых окон входа в систему.</span><span class="sxs-lookup"><span data-stu-id="53d30-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="53d30-125">Если этот флаг установлен, а **опенмсгсторе** не хватает сведений о конфигурации, чтобы открыть хранилище сообщений без справки пользователя, возвращается мапи_е_логон_фаилед.</span><span class="sxs-lookup"><span data-stu-id="53d30-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="53d30-126">Если этот флаг не установлен, поставщик хранилища сообщений может предложить пользователю исправить имя или пароль или выполнить другие действия, необходимые для установки подключения к хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="53d30-127">MDB\_но_маил: хранилище сообщений не должно использоваться для отправки и получения почты.</span><span class="sxs-lookup"><span data-stu-id="53d30-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="53d30-128">Если этот флаг установлен, MAPI не уведомляет Диспетчер очереди MAPI о том, что это хранилище сообщений открыто.</span><span class="sxs-lookup"><span data-stu-id="53d30-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="53d30-129">MDB\_Online: в режиме кэширования Exchange клиент или поставщик услуг может вызывать этот метод с мдб_онлине для переопределения подключения к локальному хранилищу сообщений и открытия хранилища на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="53d30-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="53d30-130">Вы не можете открыть хранилище Exchange в режиме кэширования и в некэшированном режиме одновременно в том же сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="53d30-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="53d30-131">Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.</span><span class="sxs-lookup"><span data-stu-id="53d30-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="53d30-132">МДБ_ТЕМПОРАРИ: предПисывает MAPI, что хранилище сообщений не является постоянным и не должно добавляться в таблицу хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="53d30-133">Этот флаг используется для входа в хранилище сообщений, что позволяет программно получать данные из раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="53d30-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="53d30-134">МДБ_ВРИТЕ: заПрашивает разрешение на чтение и запись в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="53d30-135">_Лппмдб_</span><span class="sxs-lookup"><span data-stu-id="53d30-135">_lppMDB_</span></span>
  
> <span data-ttu-id="53d30-136">вышли Указатель на указатель хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53d30-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53d30-137">Return value</span></span>

<span data-ttu-id="53d30-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="53d30-138">S_OK</span></span> 
  
> <span data-ttu-id="53d30-139">Хранилище сообщений успешно открыто.</span><span class="sxs-lookup"><span data-stu-id="53d30-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="53d30-140">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="53d30-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="53d30-141">Предпринята попытка получить доступ к хранилищу сообщений, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="53d30-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="53d30-142">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="53d30-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="53d30-143">Хранилище сообщений, указанное в _лпентрид_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="53d30-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="53d30-144">МАПИ_Е_УНКНОВН_КПИД</span><span class="sxs-lookup"><span data-stu-id="53d30-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="53d30-145">Сервер не настроен для поддержки кодовой страницы клиента.</span><span class="sxs-lookup"><span data-stu-id="53d30-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="53d30-146">МАПИ_Е_УНКНОВН_ЛЦИД</span><span class="sxs-lookup"><span data-stu-id="53d30-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="53d30-147">Сервер не настроен для поддержки информации о языковых стандартах клиента.</span><span class="sxs-lookup"><span data-stu-id="53d30-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="53d30-148">МАПИ_В_ЕРРОРС_РЕТУРНЕД</span><span class="sxs-lookup"><span data-stu-id="53d30-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="53d30-149">Вызов выполнен успешно, но у поставщика хранилища сообщений есть доступные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53d30-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="53d30-150">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="53d30-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="53d30-151">Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession:: GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="53d30-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="53d30-152">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="53d30-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="53d30-153">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="53d30-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53d30-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="53d30-154">Remarks</span></span>

<span data-ttu-id="53d30-155">Метод **IMAPISession:: опенмсгсторе** открывает определенное хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53d30-156">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="53d30-156">Notes to callers</span></span>

<span data-ttu-id="53d30-157">Уровень разрешений по умолчанию для хранилищ сообщений доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="53d30-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="53d30-158">Если вы установили флаг МДБ_ВРИТЕ, вы по-прежнему можете получить разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="53d30-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="53d30-159">Конечный уровень доступа, который MAPI назначает хранилищу сообщений, зависит от вашего уровня разрешений, самого хранилища сообщений и поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="53d30-160">Если вы вызовите **опенмсгсторе** , чтобы открыть хранилище сообщений с разрешением только для чтения, произойдет следующее:</span><span class="sxs-lookup"><span data-stu-id="53d30-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="53d30-161">В свойстве **\_сторе_суппорт_маск** магазина ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) не будет задано хранилище\_модифи_ок и хранилище\_креате_ок.</span><span class="sxs-lookup"><span data-stu-id="53d30-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="53d30-162">Вызовы для открытия одного из сообщений или папок хранилища сообщений с помощью [IMAPISession:: OpenEntry](imapisession-openentry.md) с установленным ФЛАГом мапи_модифи завершатся с ошибками.</span><span class="sxs-lookup"><span data-stu-id="53d30-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="53d30-163">Вызовы для открытия одного из свойств сообщений или папок хранилища сообщений с помощью [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с ФЛАГом мапи_модифи завершатся с ошибками.</span><span class="sxs-lookup"><span data-stu-id="53d30-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="53d30-164">При вызове любого из следующих методов произойдет ошибка:</span><span class="sxs-lookup"><span data-stu-id="53d30-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="53d30-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="53d30-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="53d30-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="53d30-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="53d30-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="53d30-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="53d30-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="53d30-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="53d30-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="53d30-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="53d30-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="53d30-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="53d30-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="53d30-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="53d30-172">Вызовы следующих методов завершатся с ошибками, если целевой объект для скопированного сообщения доступен только для чтения, независимо от того, совпадает ли целевой объект с исходным хранилищем сообщений или другое хранилище, доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="53d30-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="53d30-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="53d30-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="53d30-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="53d30-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="53d30-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="53d30-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="53d30-176">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="53d30-176">MFCMAPI reference</span></span>

<span data-ttu-id="53d30-177">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="53d30-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53d30-178">**Файл**</span><span class="sxs-lookup"><span data-stu-id="53d30-178">**File**</span></span>|<span data-ttu-id="53d30-179">**Функция**</span><span class="sxs-lookup"><span data-stu-id="53d30-179">**Function**</span></span>|<span data-ttu-id="53d30-180">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="53d30-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53d30-181">Маписторефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="53d30-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="53d30-182">Каллопенмсгсторе</span><span class="sxs-lookup"><span data-stu-id="53d30-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="53d30-183">MFCMAPI использует метод **IMAPISession:: опенмсгсторе** , чтобы открыть хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="53d30-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53d30-184">См. также</span><span class="sxs-lookup"><span data-stu-id="53d30-184">See also</span></span>

- [<span data-ttu-id="53d30-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53d30-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="53d30-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="53d30-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="53d30-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="53d30-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="53d30-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="53d30-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="53d30-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="53d30-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="53d30-190">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="53d30-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="53d30-191">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="53d30-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

