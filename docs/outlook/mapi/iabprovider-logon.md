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
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348785"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="1945d-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1945d-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="1945d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1945d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1945d-105">Устанавливает подключение к активному сеансу.</span><span class="sxs-lookup"><span data-stu-id="1945d-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1945d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1945d-106">Parameters</span></span>

 <span data-ttu-id="1945d-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="1945d-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="1945d-108">[in] Указатель на объект поддержки поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1945d-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="1945d-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1945d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="1945d-110">[in] Ручка родительского окна для диалогового окна logon, отображаемого методом **Logon,** если разрешено.</span><span class="sxs-lookup"><span data-stu-id="1945d-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="1945d-111">Параметр _ulUIParam_ содержит значение параметра с таким же именем, переданного MAPI в предыдущем вызове на функцию [MAPILogonEx.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="1945d-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1945d-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1945d-113">[in] Указатель на имя профиля сеанса.</span><span class="sxs-lookup"><span data-stu-id="1945d-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="1945d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1945d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="1945d-115">[in] Битмаска флагов, которые контролируют выполнение логотипа.</span><span class="sxs-lookup"><span data-stu-id="1945d-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="1945d-116">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1945d-116">The following flags can be set:</span></span>
    
<span data-ttu-id="1945d-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1945d-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="1945d-118">Поставщик не должен отображать диалоговое окно во время logon.</span><span class="sxs-lookup"><span data-stu-id="1945d-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="1945d-119">Если этот флаг не установлен, поставщик может отобразить диалоговое окно, чтобы подсказыть пользователю отсутствующие сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1945d-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="1945d-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1945d-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1945d-121">Позволяет **logon** успешно возвращаться, возможно, до завершения процесса логона.</span><span class="sxs-lookup"><span data-stu-id="1945d-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="1945d-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1945d-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1945d-123">Все строки должны быть в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="1945d-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="1945d-124">Если флаг MAPI_UNICODE не установлен, строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1945d-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="1945d-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="1945d-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="1945d-126">[in, out] Указатель на размер в bytes структуры учетных данных безопасности, на который указывает параметр _lppbSecurity._</span><span class="sxs-lookup"><span data-stu-id="1945d-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="1945d-127">При входе значение должно быть незеро; на выходе значение должно быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="1945d-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="1945d-128">В обоих случаях указатели должны быть действительными.</span><span class="sxs-lookup"><span data-stu-id="1945d-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="1945d-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="1945d-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="1945d-130">[in, out] Указатель на указатель на учетные данные безопасности.</span><span class="sxs-lookup"><span data-stu-id="1945d-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="1945d-131">При входе значение должно быть незеро; на выходе значение должно быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="1945d-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="1945d-132">В обоих случаях указатель должен быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="1945d-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="1945d-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1945d-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1945d-134">[вышел] Указатель на указатель на [структуру MAPIERROR.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="1945d-135">Параметр  _lppMAPIError может_ быть задан в NULL, если нет структуры **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="1945d-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="1945d-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="1945d-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="1945d-137">[вышел] Указатель на указатель на объект logon поставщика.</span><span class="sxs-lookup"><span data-stu-id="1945d-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1945d-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1945d-138">Return value</span></span>

<span data-ttu-id="1945d-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="1945d-139">S_OK</span></span> 
  
> <span data-ttu-id="1945d-140">Успешно установлено подключение к активному сеансу.</span><span class="sxs-lookup"><span data-stu-id="1945d-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="1945d-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="1945d-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="1945d-142">Поставщик не может войти в систему, но MAPI может продолжать входить в систему других поставщиков в службе сообщений, к которой принадлежит поставщик.</span><span class="sxs-lookup"><span data-stu-id="1945d-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="1945d-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="1945d-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="1945d-144">У поставщика недостаточно сведений для завершения логотипа.</span><span class="sxs-lookup"><span data-stu-id="1945d-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="1945d-145">MAPI вызывает функцию входа в службу сообщений поставщика.</span><span class="sxs-lookup"><span data-stu-id="1945d-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="1945d-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="1945d-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="1945d-147">Сервер не настроен для поддержки страницы кода клиента.</span><span class="sxs-lookup"><span data-stu-id="1945d-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="1945d-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="1945d-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="1945d-149">Сервер не настроен для поддержки сведений о локальном уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="1945d-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="1945d-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1945d-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1945d-151">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне logon.</span><span class="sxs-lookup"><span data-stu-id="1945d-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1945d-152">Примечания</span><span class="sxs-lookup"><span data-stu-id="1945d-152">Remarks</span></span>

<span data-ttu-id="1945d-153">Подключения устанавливаются с каждым поставщиком адресной книги в профиле сеанса, когда клиент вызывает [метод IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="1945d-154">**Затем OpenAddressBook** вызывает метод **Logon каждого** поставщика.</span><span class="sxs-lookup"><span data-stu-id="1945d-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="1945d-155">Имя профиля, на которое указывает параметр _lpszProfileName,_ отображается в наборе символов клиента пользователя, как указывается наличием или отсутствием флага MAPI_UNICODE в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="1945d-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1945d-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1945d-156">Notes to implementers</span></span>

<span data-ttu-id="1945d-157">В реализации метода **Logon** вызывайте [метод IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникального идентификатора или [структуры MAPIUID.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="1945d-158">Каждый из ваших объектов будет иметь идентификатор записи, который включает этот **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="1945d-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="1945d-159">MAPI использует **MAPIUID** для совпадения объекта со своим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1945d-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="1945d-160">Например, когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия пользователя обмена сообщениями, **OpenEntry** проверяет часть **MAPIUID** идентификатора записи, которая была передана, и соотнося ее с **MAPIUID,** зарегистрированным поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1945d-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="1945d-161">Если клиент входит в систему поставщика несколько раз, вам может потребоваться зарегистрировать другой **MAPIUID** для каждого логотипа.</span><span class="sxs-lookup"><span data-stu-id="1945d-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="1945d-162">Регистрация уникальных **структур MAPIUID** позволяет MAPI правильно маршрутировать запросы в соответствующий экземпляр поставщика.</span><span class="sxs-lookup"><span data-stu-id="1945d-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="1945d-163">Однако может потребоваться, чтобы каждый объект с логотипом делил **по одному MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="1945d-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="1945d-164">В этом случае вы должны иметь возможность самостоятельно обрабатывать маршрутику, а не полагаться на MAPI.</span><span class="sxs-lookup"><span data-stu-id="1945d-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="1945d-165">Дополнительные сведения о создании **MAPIUID** см. в документе [Registering Service Provider Unique Identifiers.](registering-service-provider-unique-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="1945d-166">Объект поддержки, который MAPI передает методу **Logon** в _параметре lpMAPISup,_ предоставляет доступ ко многим методам, включенным в [интерфейс IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="1945d-167">MAPI создает объект поддержки, настраиваемый под ваш тип поставщика.</span><span class="sxs-lookup"><span data-stu-id="1945d-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="1945d-168">Например, если при создании подключения необходимо войти в систему или службу каталогов, можно вызвать [метод IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md) чтобы получить учетные данные безопасности для этого конкретного сеанса логотипа.</span><span class="sxs-lookup"><span data-stu-id="1945d-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="1945d-169">Если **logon** успешно, убедитесь, что вы вызываете метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы приумновить его количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="1945d-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="1945d-170">Это позволяет поставщику держаться за указатель объекта поддержки до конца сеанса.</span><span class="sxs-lookup"><span data-stu-id="1945d-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="1945d-171">Если этот метод **AddRef** не называется, MAPI разгрузит поставщика.</span><span class="sxs-lookup"><span data-stu-id="1945d-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="1945d-172">Имя профиля, переданное в  _параметре lpszProfileName,_ можно включить в диалоговые окна ошибок, экраны логотипов или другие пользовательские интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1945d-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="1945d-173">Чтобы использовать имя профиля, скопируйте его в выделенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="1945d-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="1945d-174">Создайте объект logon и верни ему указатель в _параметре lppABLogon._</span><span class="sxs-lookup"><span data-stu-id="1945d-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="1945d-175">MAPI использует этот объект logon для звонков к методам реализации [IABLogon.](iablogoniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1945d-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="1945d-176">Если во время логотипа требуется пароль, отобразите диалоговое окно с логотипом только в том случае, если AB_NO_DIALOG флаг не установлен.</span><span class="sxs-lookup"><span data-stu-id="1945d-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="1945d-177">Если пользователь отменяет процесс логотипа, как правило, нажав кнопку Отмена в диалоговом окне, MAPI_E_USER_CANCEL **из Logon**. </span><span class="sxs-lookup"><span data-stu-id="1945d-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="1945d-178">Как правило, если поставщик адресной книги не может войти в систему, MAPI отключает службу сообщений, к которой принадлежит поставщик сбоя, то есть MAPI не будет пытаться установить подключения для других поставщиков, которые относятся к службе до конца срока службы сеанса.</span><span class="sxs-lookup"><span data-stu-id="1945d-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="1945d-179">Однако, если поставщик не может установить подключение и вы не хотите отключить всю службу, возвращайте MAPI_E_FAILONEPROVIDER или MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="1945d-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="1945d-180">MAPI не отключит службу сообщений, к которой принадлежит поставщик.</span><span class="sxs-lookup"><span data-stu-id="1945d-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="1945d-181">Возврат MAPI_E_FAILONEPROVIDER, если возникает ошибка, которая не является достаточно серьезной, чтобы предотвратить установление подключений другими поставщиками в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="1945d-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="1945d-182">Возвращайте MAPI_E_UNCONFIGURED, если из профиля отсутствуют необходимые сведения о конфигурации, и вы не можете отобразить диалоговое окно для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="1945d-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="1945d-183">MAPI будет отвечать, вызывая функцию точки входа службы сообщений поставщика с помощью MSG_SERVICE_CONFIGURE  _параметра ulContext,_ чтобы предоставить службе возможность настроить себя, программным образом или с помощью листа свойств.</span><span class="sxs-lookup"><span data-stu-id="1945d-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="1945d-184">По завершению функции точки входа службы сообщений MAPI повторно вырисовывает логотип.</span><span class="sxs-lookup"><span data-stu-id="1945d-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1945d-185">См. также</span><span class="sxs-lookup"><span data-stu-id="1945d-185">See also</span></span>



[<span data-ttu-id="1945d-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="1945d-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="1945d-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1945d-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="1945d-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1945d-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="1945d-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="1945d-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="1945d-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="1945d-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="1945d-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1945d-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

