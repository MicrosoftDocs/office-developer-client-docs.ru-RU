---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8cb7934919722139622b6caf3aac741c9b2e54c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582464"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="94695-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="94695-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="94695-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94695-105">Устанавливает подключение к активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="94695-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="94695-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94695-106">Parameters</span></span>

 <span data-ttu-id="94695-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="94695-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="94695-108">[in] Указатель на объект поддержки поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="94695-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="94695-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="94695-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="94695-110">[in] Дескриптор родительского окна для диалогового окна входа в систему, которая отображает метод **входа в систему** , если это разрешено.</span><span class="sxs-lookup"><span data-stu-id="94695-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="94695-111">Параметр _ulUIParam_ содержит значение параметра с таким же именем, переданной в MAPI в предыдущем вызове функции [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="94695-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="94695-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="94695-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="94695-113">[in] Указатель на имя профиля сеанса.</span><span class="sxs-lookup"><span data-stu-id="94695-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="94695-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94695-114">_ulFlags_</span></span>
  
> <span data-ttu-id="94695-115">[in] Битовая маска флаги, который определяет, как выполняется вход в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="94695-116">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="94695-116">The following flags can be set:</span></span>
    
<span data-ttu-id="94695-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="94695-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="94695-118">Поставщик не отображать диалоговое окно во время входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="94695-119">Если этот флаг не установлен, поставщик может отображать диалоговое окно запрашивать у пользователя отсутствуют сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="94695-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="94695-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="94695-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="94695-121">Включение **входа в систему** для возврата успешно, возможно до завершения процесса входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="94695-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94695-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="94695-123">Все строки должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="94695-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="94695-124">Если флаг MAPI_UNICODE не установлен, строки должен быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="94695-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="94695-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="94695-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="94695-126">[in, out] Указатель на размер в байтах, структуры учетные данные безопасности, на который указывает параметр _lppbSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="94695-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="94695-127">На выходе — значение должно быть от нуля; в выходных данных значение должно быть нулю.</span><span class="sxs-lookup"><span data-stu-id="94695-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="94695-128">В обоих случаях указатели должно быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="94695-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="94695-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="94695-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="94695-130">[in, out] Указатель на указатель на учетные данные безопасности.</span><span class="sxs-lookup"><span data-stu-id="94695-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="94695-131">На выходе — значение должно быть от нуля; в выходных данных значение должно быть нулю.</span><span class="sxs-lookup"><span data-stu-id="94695-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="94695-132">В обоих случаях указатель должен быть допустимый.</span><span class="sxs-lookup"><span data-stu-id="94695-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="94695-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="94695-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="94695-134">[out] Указатель на указатель на структуру [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="94695-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="94695-135">Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="94695-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="94695-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="94695-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="94695-137">[out] Указатель на указатель на объект поставщика входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94695-138">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="94695-138">Return value</span></span>

<span data-ttu-id="94695-139">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="94695-139">S_OK</span></span> 
  
> <span data-ttu-id="94695-140">Подключение к активного сеанса успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="94695-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="94695-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="94695-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="94695-142">Поставщик не может войти, но можно продолжить MAPI, войдите в систему других поставщиков службы сообщений, к которой принадлежит поставщик.</span><span class="sxs-lookup"><span data-stu-id="94695-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="94695-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="94695-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="94695-144">Поставщик имеет недостаточно сведений для выполнения входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="94695-145">MAPI вызывает функцию запись службы поставщика сообщения.</span><span class="sxs-lookup"><span data-stu-id="94695-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="94695-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="94695-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="94695-147">Сервер не настроен для поддержки кодовой страницы клиента.</span><span class="sxs-lookup"><span data-stu-id="94695-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="94695-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="94695-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="94695-149">Сервер не настроен для поддержки сведения о языковом стандарте клиента.</span><span class="sxs-lookup"><span data-stu-id="94695-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="94695-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="94695-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="94695-151">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="94695-152">Замечания</span><span class="sxs-lookup"><span data-stu-id="94695-152">Remarks</span></span>

<span data-ttu-id="94695-153">Подключений с каждой поставщик адресной книги в профиле сеанса при вызове метода [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) клиентом.</span><span class="sxs-lookup"><span data-stu-id="94695-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="94695-154">**OpenAddressBook** вызывает метод **входа в систему** для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="94695-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="94695-155">Имя профиля, на который указывает параметр _lpszProfileName_ отображается в набор знаков клиента пользователя, как указано в наличие или отсутствие флага MAPI_UNICODE с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="94695-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="94695-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="94695-156">Notes to implementers</span></span>

<span data-ttu-id="94695-157">В реализации метода **входа в систему** вызовите метод [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникального идентификатора или [MAPIUID](mapiuid.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="94695-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="94695-158">Каждый объект будет иметь запись идентификатор, который включает в себя этот **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="94695-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="94695-159">MAPI использует **MAPIUID** объекта с его поставщиком.</span><span class="sxs-lookup"><span data-stu-id="94695-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="94695-160">Например, когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) , чтобы открыть обмена сообщениями пользователя, **OpenEntry** проверяет **MAPIUID** часть идентификатор записи, который был передан и сопоставляет его с **MAPIUID** , зарегистрированные, поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="94695-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="94695-161">Если клиент входит в систему с поставщиком более одного раза, можно зарегистрировать различных **MAPIUID** для каждого входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="94695-162">Регистрация уникальных структур **MAPIUID** позволяет MAPI для правильной маршрутизации запросов к экземпляру соответствующего поставщика.</span><span class="sxs-lookup"><span data-stu-id="94695-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="94695-163">Тем не менее может потребоваться каждый объект входа совместно использовать один **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="94695-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="94695-164">В этом случае требуется обрабатывать маршрута самостоятельно вместо использования MAPI.</span><span class="sxs-lookup"><span data-stu-id="94695-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="94695-165">Дополнительные сведения о создании **MAPIUID**можно [Регистрации уникальных идентификаторов поставщика службы](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="94695-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="94695-166">Поддержка объект, который передает MAPI в метод **входа в систему** с помощью параметра _lpMAPISup_ предоставляет доступ к многие из методов, включенных в [IMAPISupport: IUnknown](imapisupportiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="94695-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="94695-167">MAPI создает объект поддержки, настроенный для соответствующего типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="94695-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="94695-168">К примеру Если необходимо войти в базовом системы обмена сообщениями или служба каталогов при создании подключения к можно вызвать метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) для получения учетных данных для этого конкретного сеанса.</span><span class="sxs-lookup"><span data-stu-id="94695-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="94695-169">Если **Вход в систему** прошла успешно, убедитесь, что метод объектов поддержки [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) увеличить счетчик ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="94695-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="94695-170">Благодаря этому поставщику к удержанию указателя на объект поддержки для остальных сеанса.</span><span class="sxs-lookup"><span data-stu-id="94695-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="94695-171">Если этот метод **AddRef** не вызван, MAPI будет выгрузить ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="94695-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="94695-172">Может включать имя профиля, переданной в параметре _lpszProfileName_ ошибка диалоговых окон, экрана входа или других пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="94695-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="94695-173">Чтобы использовать имя профиля, скопируйте его в хранилище, которое выделено.</span><span class="sxs-lookup"><span data-stu-id="94695-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="94695-174">Создайте объект входа в систему и возвращает указатель на него с помощью параметра _lppABLogon_ .</span><span class="sxs-lookup"><span data-stu-id="94695-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="94695-175">MAPI выполнять вызовы методов в реализации [IABLogon](iablogoniunknown.md) использует этот объект входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="94695-176">Если требуется пароль при входе в систему, только в том случае, если не установлен флаг AB_NO_DIALOG отображения диалогового окна входа в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="94695-177">Если пользователь отменил процесс входа в систему, как правило, нажмите кнопку **Отмена** в диалоговом окне возврата MAPI_E_USER_CANCEL из **входа в систему**.</span><span class="sxs-lookup"><span data-stu-id="94695-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="94695-178">Как правило, если поставщика адресных книг не может войти, MAPI отключает службы сообщений, к которой принадлежит поставщик со сбоями, то есть MAPI не пытается устанавливать подключения для каких-либо других поставщиков, относящихся к службе для остальных сеанса время жизни.</span><span class="sxs-lookup"><span data-stu-id="94695-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="94695-179">Тем не менее если ваш поставщик не удается установить подключение и вы не хотите отключить всей службы, возвращает MAPI_E_FAILONEPROVIDER или MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="94695-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="94695-180">MAPI не отключает службы сообщений, к которой принадлежит поставщик.</span><span class="sxs-lookup"><span data-stu-id="94695-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="94695-181">Возврат MAPI_E_FAILONEPROVIDER при возникновении ошибки, которая не является серьезные, чтобы предотвратить установления подключения других поставщиков службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="94695-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="94695-182">Возвращает MAPI_E_UNCONFIGURED, если отсутствуют необходимые сведения о конфигурации из профиля и не может отобразить диалоговое окно с запросом.</span><span class="sxs-lookup"><span data-stu-id="94695-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="94695-183">MAPI ответит путем вызова функции точки входа службы сообщения ваш поставщик с набором MSG_SERVICE_CONFIGURE как параметр _ulContext_ для предоставления службы возможности для настройки, либо программными средствами или с помощью свойств.</span><span class="sxs-lookup"><span data-stu-id="94695-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="94695-184">Точка входа в службу сообщение завершения работы функции, MAPI, как повторить вход в систему.</span><span class="sxs-lookup"><span data-stu-id="94695-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94695-185">См. также</span><span class="sxs-lookup"><span data-stu-id="94695-185">See also</span></span>



[<span data-ttu-id="94695-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="94695-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="94695-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="94695-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="94695-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="94695-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="94695-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="94695-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="94695-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="94695-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="94695-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94695-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

