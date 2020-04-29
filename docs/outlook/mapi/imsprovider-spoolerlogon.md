---
title: имспровидерспулерлогон
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
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="222a3-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="222a3-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="222a3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="222a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="222a3-105">Заносит в журнал Диспетчер очереди MAPI в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="222a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="222a3-106">Parameters</span></span>

 <span data-ttu-id="222a3-107">_лпмаписуп_</span><span class="sxs-lookup"><span data-stu-id="222a3-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="222a3-108">возврата Указатель на объект поддержки MAPI для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="222a3-109">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="222a3-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="222a3-110">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="222a3-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="222a3-111">_лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="222a3-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="222a3-112">возврата Указатель на строку, содержащую имя профиля, используемого для входа в систему диспетчера очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="222a3-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="222a3-113">Эта строка может отображаться в диалоговых окнах, записанных в файл журнала или просто игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="222a3-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="222a3-114">Он должен быть в формате Юникод, если установлен флаг MAPI_UNICODE в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="222a3-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="222a3-115">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="222a3-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="222a3-116">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="222a3-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="222a3-117">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="222a3-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="222a3-118">возврата Указатель на идентификатор записи для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="222a3-119">При передаче значения NULL в параметре _лпентрид_ показывается, что хранилище сообщений еще не выбрано, а также отображаются диалоговые окна, позволяющие пользователю выбрать хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="222a3-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="222a3-120">_ulFlags_</span></span>
  
> <span data-ttu-id="222a3-121">возврата Битовая маска флагов, определяющая способ выполнения входа.</span><span class="sxs-lookup"><span data-stu-id="222a3-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="222a3-122">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="222a3-122">The following flags can be set:</span></span>
    
<span data-ttu-id="222a3-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="222a3-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="222a3-124">Вызов может быть выполнен, даже если базовый объект недоступен для вызывающей реализации.</span><span class="sxs-lookup"><span data-stu-id="222a3-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="222a3-125">Если объект недоступен, последующий вызов объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="222a3-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="222a3-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="222a3-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="222a3-127">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="222a3-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="222a3-128">Если MAPI_UNICODE не заданы, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="222a3-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="222a3-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="222a3-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="222a3-130">Запрещает отображение диалоговых окон входа в систему.</span><span class="sxs-lookup"><span data-stu-id="222a3-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="222a3-131">Если этот флаг установлен, значение ошибки MAPI_E_LOGON_FAILED возвращается в случае неудачного входа.</span><span class="sxs-lookup"><span data-stu-id="222a3-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="222a3-132">Если этот флаг не установлен, поставщик хранилища сообщений может предложить пользователю исправить имя или пароль, вставить диск или выполнить другие действия, необходимые для установки подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="222a3-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="222a3-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="222a3-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="222a3-134">Запрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="222a3-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="222a3-135">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="222a3-135">_lpInterface_</span></span>
  
> <span data-ttu-id="222a3-136">возврата Указатель на идентификатор интерфейса (IID) для подключения к хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="222a3-137">Передача значения NULL указывает, что возвращается интерфейс MAPI для хранилища сообщений ([IMsgStore](imsgstoreimapiprop.md)).</span><span class="sxs-lookup"><span data-stu-id="222a3-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="222a3-138">Для параметра _лпинтерфаце_ также можно задать идентификатор соответствующего интерфейса для хранилища сообщений (например, IID_IUnknown или IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="222a3-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="222a3-139">_кбспулсекурити_</span><span class="sxs-lookup"><span data-stu-id="222a3-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="222a3-140">возврата Указатель на размер проверочных данных (в байтах) в параметре _лппбспулсекурити_ .</span><span class="sxs-lookup"><span data-stu-id="222a3-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="222a3-141">_лпбспулсекурити_</span><span class="sxs-lookup"><span data-stu-id="222a3-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="222a3-142">возврата Указатель на указатель на проверочные данные.</span><span class="sxs-lookup"><span data-stu-id="222a3-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="222a3-143">Метод **спулерлогон** использует эти данные для входа в систему БУФЕРИЗАЦИи MAPI в то же хранилище, что и поставщик хранилища сообщений, ранее вошедшего в систему, с помощью метода [Функцииimsprovider:: logon](imsprovider-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="222a3-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="222a3-144">_лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="222a3-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="222a3-145">вышли Указатель на указатель на возвращенную структуру [мапиеррор](mapierror.md) (при наличии), содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="222a3-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="222a3-146">Параметр _лппмапиеррор_ может иметь значение null, если структура **мапиеррор** для возврата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="222a3-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="222a3-147">_лппмслогон_</span><span class="sxs-lookup"><span data-stu-id="222a3-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="222a3-148">вышли Указатель на указатель на объект входа хранилища сообщений для входа MAPI.</span><span class="sxs-lookup"><span data-stu-id="222a3-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="222a3-149">_лппмдб_</span><span class="sxs-lookup"><span data-stu-id="222a3-149">_lppMDB_</span></span>
  
> <span data-ttu-id="222a3-150">вышли Указатель на указатель на объект хранилища сообщений для системы буферизации MAPI и клиентских приложений для входа в.</span><span class="sxs-lookup"><span data-stu-id="222a3-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="222a3-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="222a3-151">Return value</span></span>

<span data-ttu-id="222a3-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="222a3-152">S_OK</span></span> 
  
> <span data-ttu-id="222a3-153">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="222a3-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="222a3-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="222a3-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="222a3-155">Профиль не содержит достаточно сведений для завершения входа.</span><span class="sxs-lookup"><span data-stu-id="222a3-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="222a3-156">Когда возвращается это значение, MAPI вызывает функцию точки входа службы сообщений поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="222a3-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="222a3-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="222a3-158">Вызов выполнен успешно, но у поставщика хранилища сообщений есть доступные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="222a3-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="222a3-159">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="222a3-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="222a3-160">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="222a3-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="222a3-161">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="222a3-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="222a3-162">Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession:: GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="222a3-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="222a3-163">Примечания</span><span class="sxs-lookup"><span data-stu-id="222a3-163">Remarks</span></span>

<span data-ttu-id="222a3-164">Диспетчер очереди MAPI вызывает метод **функцииimsprovider:: спулерлогон** для входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="222a3-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="222a3-165">Диспетчер очереди MAPI должен использовать объект хранилища сообщений, возвращенный поставщиком хранилища сообщений, в параметре _лппмдб_ во время и после входа.</span><span class="sxs-lookup"><span data-stu-id="222a3-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="222a3-166">Для обеспечения совместимости с методом [функцииimsprovider:: logon](imsprovider-logon.md) поставщик также возвращает объект входа в хранилище сообщений в параметре _лппмслогон_ .</span><span class="sxs-lookup"><span data-stu-id="222a3-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="222a3-167">Использование объекта Store и объекта logon одинаково для обычного входа в систему хранения; между объектом logon и объектом Store должно быть отношение "один к одному", чтобы объекты действовали так, как если бы они были одним объектом, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="222a3-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="222a3-168">Два объекта создаются вместе и освобождаются вместе.</span><span class="sxs-lookup"><span data-stu-id="222a3-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="222a3-169">Поставщик магазина должен внутренним образом пометить возвращенный объект хранилища сообщений, чтобы указать, что хранилище используется диспетчером MAPI.</span><span class="sxs-lookup"><span data-stu-id="222a3-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="222a3-170">Некоторые методы для этого объекта хранилища ведут себя иначе, чем для объекта хранилища сообщений, предоставленного клиентским приложениям.</span><span class="sxs-lookup"><span data-stu-id="222a3-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="222a3-171">Хранение этой внутренней метки является самым распространенным способом запуска поведения, характерного для диспетчера очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="222a3-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="222a3-172">См. также</span><span class="sxs-lookup"><span data-stu-id="222a3-172">See also</span></span>



[<span data-ttu-id="222a3-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="222a3-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="222a3-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="222a3-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="222a3-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="222a3-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

