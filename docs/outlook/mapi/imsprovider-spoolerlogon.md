---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586419"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="07dc5-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="07dc5-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="07dc5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07dc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07dc5-105">Журналы очереди MAPI вход в систему хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="07dc5-105">Logs the MAPI spooler on to a message store.</span></span>
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a><span data-ttu-id="07dc5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07dc5-106">Parameters</span></span>

 <span data-ttu-id="07dc5-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="07dc5-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="07dc5-108">[in] Указатель на MAPI поддержку объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="07dc5-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="07dc5-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="07dc5-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="07dc5-110">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="07dc5-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="07dc5-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="07dc5-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="07dc5-112">[in] Указатель на строку, содержащую имя профиля, используется для входа очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="07dc5-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="07dc5-113">Эта строка может отображаются в диалоговых окнах, записывается в файл журнала или просто игнорируются.</span><span class="sxs-lookup"><span data-stu-id="07dc5-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="07dc5-114">Он должен быть в формате Юникод, если флаг MAPI_UNICODE установлен в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="07dc5-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="07dc5-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="07dc5-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="07dc5-116">[in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="07dc5-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="07dc5-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="07dc5-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="07dc5-118">[in] Указатель на идентификатор записи для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="07dc5-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="07dc5-119">Указать значение NULL для параметра _lpEntryID_ указывает, что хранилище сообщений еще не был выбран и диалоговых окон, которые позволяют пользователю выбрать хранилище сообщений могут быть представлены.</span><span class="sxs-lookup"><span data-stu-id="07dc5-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="07dc5-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="07dc5-120">_ulFlags_</span></span>
  
> <span data-ttu-id="07dc5-121">[in] Битовая маска флаги, который определяет, как выполняется вход в систему.</span><span class="sxs-lookup"><span data-stu-id="07dc5-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="07dc5-122">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="07dc5-122">The following flags can be set:</span></span>
    
<span data-ttu-id="07dc5-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="07dc5-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="07dc5-124">Разрешено для успешного выполнения даже в том случае, если базовый объект недоступен для вызова реализации.</span><span class="sxs-lookup"><span data-stu-id="07dc5-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="07dc5-125">Если объект недоступен, следующий вызов объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="07dc5-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="07dc5-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07dc5-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="07dc5-127">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="07dc5-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="07dc5-128">Если MAPI_UNICODE не задано, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="07dc5-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="07dc5-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="07dc5-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="07dc5-130">Не отображать диалоговые окна входа в систему.</span><span class="sxs-lookup"><span data-stu-id="07dc5-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="07dc5-131">Если этот флаг установлен, возвращается значение ошибка MAPI_E_LOGON_FAILED, если вход в систему не удалось.</span><span class="sxs-lookup"><span data-stu-id="07dc5-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="07dc5-132">Если этот флаг не установлен, поставщик хранения сообщений можно запрашивать пользователя в нужное имя или пароль, вставьте диск или выполнить другие действия, необходимые для установления подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="07dc5-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="07dc5-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="07dc5-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="07dc5-134">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="07dc5-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="07dc5-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="07dc5-135">_lpInterface_</span></span>
  
> <span data-ttu-id="07dc5-136">[in] Указатель на интерфейс идентификатор (ИД интерфейса) для хранилища сообщений для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="07dc5-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="07dc5-137">Значение NULL указывает, что возвращается интерфейс MAPI для хранилища сообщений ([IMsgStore](imsgstoreimapiprop.md)).</span><span class="sxs-lookup"><span data-stu-id="07dc5-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="07dc5-138">Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для хранилища сообщений (например, IID_IUnknown или IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="07dc5-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="07dc5-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="07dc5-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="07dc5-140">[in] Указатель на размер в байтах, проверки данных с помощью параметра _lppbSpoolSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="07dc5-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="07dc5-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="07dc5-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="07dc5-142">[in] Указатель на указатель на данные проверки.</span><span class="sxs-lookup"><span data-stu-id="07dc5-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="07dc5-143">Метод **SpoolerLogon** использует эти данные для входа в качестве поставщика хранилища сообщений, ранее вход в систему с помощью метода [IMSProvider::Logon](imsprovider-logon.md) диспетчер очереди MAPI на том же хранилище.</span><span class="sxs-lookup"><span data-stu-id="07dc5-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="07dc5-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="07dc5-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="07dc5-145">[out] Указатель на указатель на возвращенный [MAPIERROR](mapierror.md) структуры, если они существуют, который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="07dc5-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="07dc5-146">Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="07dc5-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="07dc5-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="07dc5-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="07dc5-148">[out] Указатель на указатель на сообщение хранить объект входа в систему для MAPI для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="07dc5-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="07dc5-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="07dc5-149">_lppMDB_</span></span>
  
> <span data-ttu-id="07dc5-150">[out] Указатель на указатель на сообщение хранилища объект для очереди MAPI и клиентскими приложениями для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="07dc5-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07dc5-151">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="07dc5-151">Return value</span></span>

<span data-ttu-id="07dc5-152">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="07dc5-152">S_OK</span></span> 
  
> <span data-ttu-id="07dc5-153">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="07dc5-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="07dc5-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="07dc5-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="07dc5-155">Профиль не содержит достаточно сведений для входа в систему для выполнения.</span><span class="sxs-lookup"><span data-stu-id="07dc5-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="07dc5-156">При возвращении это значение MAPI вызывает функцию точки входа службы сообщений поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="07dc5-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="07dc5-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="07dc5-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="07dc5-158">Вызов завершился успешно, но поставщика хранилища сообщений имеет доступные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="07dc5-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="07dc5-159">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="07dc5-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="07dc5-160">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="07dc5-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="07dc5-161">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="07dc5-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="07dc5-162">Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="07dc5-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="07dc5-163">Замечания</span><span class="sxs-lookup"><span data-stu-id="07dc5-163">Remarks</span></span>

<span data-ttu-id="07dc5-164">Диспетчер очереди MAPI вызывает метод **IMSProvider::SpoolerLogon** войти в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="07dc5-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="07dc5-165">Диспетчер очереди MAPI следует использовать объект хранилища сообщений, возвращенный поставщиком хранилища сообщений с помощью параметра _lppMDB_ во время и после входа в систему.</span><span class="sxs-lookup"><span data-stu-id="07dc5-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="07dc5-166">Для обеспечения согласованности с помощью метода [IMSProvider::Logon](imsprovider-logon.md) поставщик возвращает объект входа хранилища сообщений с помощью параметра _lppMSLogon_ .</span><span class="sxs-lookup"><span data-stu-id="07dc5-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="07dc5-167">Использование объекта хранилища и объект вход в систему идентичны для входа в систему обычным хранения; Таким образом, что объекты действовать как если бы они были одного объекта, который предоставляет два из них следует однозначного соответствия между объект вход в систему и объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="07dc5-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="07dc5-168">Создаются два объекта вместе и освобожденное друг с другом.</span><span class="sxs-lookup"><span data-stu-id="07dc5-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="07dc5-169">Поставщик хранения во внутренней сети следует пометить объект хранилища возвращенных сообщений для указания, что хранилище используется диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="07dc5-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="07dc5-170">Некоторые методы для данного объекта хранилища ведут себя иначе, не в сообщении хранилища, который на клиентские приложения.</span><span class="sxs-lookup"><span data-stu-id="07dc5-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="07dc5-171">Поддержание внутренних Марка — это чаще всего инициирования поведения, характерные для очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="07dc5-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="07dc5-172">См. также</span><span class="sxs-lookup"><span data-stu-id="07dc5-172">See also</span></span>



[<span data-ttu-id="07dc5-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="07dc5-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="07dc5-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="07dc5-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="07dc5-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07dc5-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

