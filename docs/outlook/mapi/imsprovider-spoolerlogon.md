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
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="ee4dd-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="ee4dd-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="ee4dd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee4dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee4dd-105">Регистрирую пульпер MAPI в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ee4dd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ee4dd-106">Parameters</span></span>

 <span data-ttu-id="ee4dd-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="ee4dd-108">[in] Указатель на объект поддержки MAPI для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="ee4dd-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="ee4dd-110">[in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="ee4dd-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ee4dd-112">[in] Указатель на строку, содержаную имя профиля, используемого для логотипа пульпера MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="ee4dd-113">Эта строка может отображаться в диалоговом окне, записана в файл журнала или просто игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="ee4dd-114">Он должен быть в формате Unicode, если MAPI_UNICODE в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ee4dd-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ee4dd-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="ee4dd-116">[in] Размер в bytes идентификатора записи, на который указывает _параметр lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ee4dd-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ee4dd-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="ee4dd-118">[in] Указатель на идентификатор записи для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="ee4dd-119">Передача NULL в  _параметре lpEntryID_ указывает на то, что хранилище сообщений еще не выбрано и что диалоговые окна, позволяющие пользователю выбрать хранилище сообщений, могут быть представлены.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="ee4dd-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-120">_ulFlags_</span></span>
  
> <span data-ttu-id="ee4dd-121">[in] Битмаска флагов, которые контролируют выполнение логотипа.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="ee4dd-122">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ee4dd-122">The following flags can be set:</span></span>
    
<span data-ttu-id="ee4dd-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ee4dd-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ee4dd-124">Вызов может быть успешным, даже если его объект недопустим для реализации вызова.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="ee4dd-125">Если объект не доступен, последующий вызов объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="ee4dd-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee4dd-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ee4dd-127">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ee4dd-128">Если MAPI_UNICODE не установлено, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="ee4dd-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ee4dd-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="ee4dd-130">Предотвращает отображение диалогов с логотипом.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="ee4dd-131">Если этот флаг заданной, значение MAPI_E_LOGON_FAILED возвращается, если логотип неуспешен.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="ee4dd-132">Если этот флаг не установлен, поставщик магазина сообщений может побудить пользователя исправить имя или пароль, вставить диск или выполнить другие действия, необходимые для установления подключения к магазину.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="ee4dd-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="ee4dd-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="ee4dd-134">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="ee4dd-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-135">_lpInterface_</span></span>
  
> <span data-ttu-id="ee4dd-136">[in] Указатель на идентификатор интерфейса (IID) для входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="ee4dd-137">Передача NULL указывает, что возвращается интерфейс MAPI для магазина сообщений[(IMsgStore).](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="ee4dd-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="ee4dd-138">Параметр  _lpInterface_ также может быть задан идентификатору для соответствующего интерфейса для магазина сообщений (например, IID_IUnknown или IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="ee4dd-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="ee4dd-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="ee4dd-140">[in] Указатель на размер в bytes данных проверки в _параметре lppbSpoolSecurity._</span><span class="sxs-lookup"><span data-stu-id="ee4dd-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="ee4dd-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="ee4dd-142">[in] Указатель на указатель на данные проверки.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="ee4dd-143">Метод **SpoolerLogon** использует эти данные для входа шпалерОВ MAPI в тот же магазин, в который ранее входил поставщик магазина сообщений с помощью метода [IMSProvider::Logon.](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="ee4dd-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="ee4dd-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ee4dd-145">[вышел] Указатель на указатель на возвращаемую структуру [MAPIERROR,](mapierror.md) если таковые есть, содержит сведения о версии, компоненте и контексте для ошибки.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="ee4dd-146">Параметр  _lppMAPIError может_ быть задан в NULL, если нет структуры **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="ee4dd-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="ee4dd-148">[вышел] Указатель на указатель на объект логотипа магазина сообщений для входа в MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="ee4dd-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="ee4dd-149">_lppMDB_</span></span>
  
> <span data-ttu-id="ee4dd-150">[вышел] Указатель на указатель на объект хранения сообщений для пульпера MAPI и клиентских приложений для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee4dd-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee4dd-151">Return value</span></span>

<span data-ttu-id="ee4dd-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee4dd-152">S_OK</span></span> 
  
> <span data-ttu-id="ee4dd-153">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ee4dd-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="ee4dd-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="ee4dd-155">Профиль не содержит достаточно сведений для завершения логотипа.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="ee4dd-156">Когда это значение возвращается, MAPI вызывает функцию точки входа в службу входа поставщика сообщений поставщика сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="ee4dd-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="ee4dd-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="ee4dd-158">Вызов удался, но у поставщика магазина сообщений есть сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="ee4dd-159">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ee4dd-160">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ee4dd-161">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="ee4dd-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="ee4dd-162">Чтобы получить сведения об ошибках от поставщика, позвоните по [методу IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="ee4dd-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ee4dd-163">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee4dd-163">Remarks</span></span>

<span data-ttu-id="ee4dd-164">Spooler MAPI вызывает **метод IMSProvider::SpoolerLogon** для входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="ee4dd-165">Пульпер MAPI должен использовать объект хранения сообщений, возвращенный поставщиком магазина сообщений в  _параметре lppMDB_ во время и после логотипа.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="ee4dd-166">Для согласованности с методом [IMSProvider::Logon](imsprovider-logon.md) поставщик также возвращает объект logon магазина сообщений в _параметре lppMSLogon._</span><span class="sxs-lookup"><span data-stu-id="ee4dd-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="ee4dd-167">Использование объекта магазина и объекта logon идентично обычному логотипу магазина; между объектом logon и объектом магазина должна быть одна к одной, чтобы объекты действовали так, как если бы они были одним объектом, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="ee4dd-168">Эти два объекта создаются вместе и освобождены вместе.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="ee4dd-169">Поставщик магазина должен внутренне отметить объект возвращенного магазина сообщений, чтобы указать, что хранилище используется spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="ee4dd-170">Некоторые методы для этого объекта магазина ведут себя иначе, чем для объекта хранения сообщений, предоставляемого для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="ee4dd-171">Сохранение этой внутренней метки является наиболее распространенным способом запуска поведения, определенного для пулера MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee4dd-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee4dd-172">См. также</span><span class="sxs-lookup"><span data-stu-id="ee4dd-172">See also</span></span>



[<span data-ttu-id="ee4dd-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="ee4dd-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="ee4dd-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ee4dd-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ee4dd-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee4dd-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

