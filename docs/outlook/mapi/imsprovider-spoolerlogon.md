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
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430576"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="57825-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="57825-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="57825-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57825-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57825-105">Занося в журнал пул MAPI в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="57825-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57825-106">Parameters</span></span>

 <span data-ttu-id="57825-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="57825-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="57825-108">[in] Указатель на объект поддержки MAPI для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="57825-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="57825-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="57825-110">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span><span class="sxs-lookup"><span data-stu-id="57825-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="57825-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="57825-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="57825-112">[in] Указатель на строку, содержаную имя профиля, используемого для имени пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="57825-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="57825-113">Эта строка может отображаться в диалоговом окне, записана в файл журнала или просто игнорируется.</span><span class="sxs-lookup"><span data-stu-id="57825-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="57825-114">Он должен быть в формате Юникод, MAPI_UNICODE флага в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="57825-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="57825-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="57825-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="57825-116">[in] Размер идентификатора записи в вайтах, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="57825-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="57825-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="57825-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="57825-118">[in] Указатель на идентификатор записи для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="57825-119">Передача NULL в  _параметре lpEntryID_ означает, что хранилище сообщений еще не выбрано и могут быть представлены диалоговые окна, позволяющие пользователю выбрать хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="57825-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57825-120">_ulFlags_</span></span>
  
> <span data-ttu-id="57825-121">[in] Битоваяmas флагов, которая управляет выполнением выполнения для этого.</span><span class="sxs-lookup"><span data-stu-id="57825-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="57825-122">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="57825-122">The following flags can be set:</span></span>
    
<span data-ttu-id="57825-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="57825-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="57825-124">Вызов может быть успешным даже в том случае, если его объект недопустим для реализации вызова.</span><span class="sxs-lookup"><span data-stu-id="57825-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="57825-125">Если объект не доступен, последующий вызов объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="57825-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="57825-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="57825-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="57825-127">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="57825-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="57825-128">Если MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="57825-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="57825-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="57825-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="57825-130">Предотвращает отображение диалогов для логотипа.</span><span class="sxs-lookup"><span data-stu-id="57825-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="57825-131">Если этот флаг установлен, значение ошибки MAPI_E_LOGON_FAILED возвращается в случае ошибки при запуске.</span><span class="sxs-lookup"><span data-stu-id="57825-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="57825-132">Если этот флаг не установлен, поставщик store сообщений может отправить пользователю запрос на исправление имени или пароля, вставить диск или выполнить другие действия, необходимые для установления подключения к магазину.</span><span class="sxs-lookup"><span data-stu-id="57825-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="57825-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="57825-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="57825-134">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="57825-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="57825-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="57825-135">_lpInterface_</span></span>
  
> <span data-ttu-id="57825-136">[in] Указатель на идентификатор интерфейса для входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="57825-137">Передача NULL означает, что возвращается интерфейс MAPI для хранения сообщений[(IMsgStore).](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="57825-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="57825-138">Параметру  _lpInterface_ также можно присвоить идентификатор для соответствующего интерфейса для хранения сообщений (например, IID_IUnknown или IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="57825-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="57825-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="57825-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="57825-140">[in] Указатель на размер данных проверки в параметре  _lppbSpoolSecurity_ (в bytes).</span><span class="sxs-lookup"><span data-stu-id="57825-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="57825-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="57825-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="57825-142">[in] Указатель на указатель на данные проверки.</span><span class="sxs-lookup"><span data-stu-id="57825-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="57825-143">Метод **SpoolerLogon** использует эти данные для входа пула MAPI в то же хранилище, в которое ранее входил поставщик store сообщений с помощью метода [IMSProvider::Logon.](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="57825-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="57825-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="57825-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="57825-145">[out] Указатель на указатель на возвращенную структуру [MAPIERROR](mapierror.md) (если таковые есть), которая содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="57825-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="57825-146">Для _параметра lppMAPIError_ можно установить NULL, если не существует возвращаемой структуры **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="57825-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="57825-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="57825-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="57825-148">[out] Указатель на указатель на объект входа в хранилище сообщений для входа в MAPI.</span><span class="sxs-lookup"><span data-stu-id="57825-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="57825-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="57825-149">_lppMDB_</span></span>
  
> <span data-ttu-id="57825-150">[out] Указатель на указатель на объект хранения сообщений для входа в пул MAPI и клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="57825-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57825-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57825-151">Return value</span></span>

<span data-ttu-id="57825-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="57825-152">S_OK</span></span> 
  
> <span data-ttu-id="57825-153">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="57825-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="57825-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="57825-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="57825-155">Профиль не содержит достаточно сведений для завершения работы с данными.</span><span class="sxs-lookup"><span data-stu-id="57825-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="57825-156">При возврате этого значения MAPI вызывает функцию точки входа службы сообщений поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="57825-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="57825-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="57825-158">Вызов был успешным, но у поставщика хранения сообщений есть сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="57825-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="57825-159">При возврате этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="57825-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="57825-160">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="57825-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="57825-161">Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="57825-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="57825-162">Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="57825-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="57825-163">Примечания</span><span class="sxs-lookup"><span data-stu-id="57825-163">Remarks</span></span>

<span data-ttu-id="57825-164">Пулер MAPI вызывает метод **IMSProvider::SpoolerLogon** для входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="57825-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="57825-165">Пулер MAPI должен использовать объект банка сообщений, возвращенный поставщиком банка сообщений в параметре  _lppMDB_ во время и после этого.</span><span class="sxs-lookup"><span data-stu-id="57825-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="57825-166">Для согласованности с методом [IMSProvider::Logon](imsprovider-logon.md) поставщик также возвращает объект для логотипа для хранения сообщений в _параметре lppMSLogon._</span><span class="sxs-lookup"><span data-stu-id="57825-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="57825-167">Использование объекта store и объекта для логотипа идентично обычному окну для логотипа магазина; между объектом для логотипа и объектом хранения должно быть соответствие "один к одному", чтобы объекты действовали так, будто они являются одним объектом, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="57825-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="57825-168">Эти два объекта создаются вместе и вместе освобождены.</span><span class="sxs-lookup"><span data-stu-id="57825-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="57825-169">Поставщик магазина должен внутренне пометить возвращенный объект, чтобы указать, что хранилище используется пулером MAPI.</span><span class="sxs-lookup"><span data-stu-id="57825-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="57825-170">Некоторые методы для этого объекта store ведут себя иначе, чем для объекта хранения сообщений, предоставляемого клиентские приложения.</span><span class="sxs-lookup"><span data-stu-id="57825-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="57825-171">Сохранение этой внутренней метки является наиболее распространенным способом запуска поведения, характерного для пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="57825-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57825-172">См. также</span><span class="sxs-lookup"><span data-stu-id="57825-172">See also</span></span>



[<span data-ttu-id="57825-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="57825-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="57825-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="57825-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="57825-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57825-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

