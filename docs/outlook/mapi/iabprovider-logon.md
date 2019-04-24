---
title: Иабпровидерлогон
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
# <a name="iabproviderlogon"></a><span data-ttu-id="551d0-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="551d0-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="551d0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="551d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="551d0-105">Устанавливает подключение к активному сеансу.</span><span class="sxs-lookup"><span data-stu-id="551d0-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="551d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="551d0-106">Parameters</span></span>

 <span data-ttu-id="551d0-107">_Лпмаписуп_</span><span class="sxs-lookup"><span data-stu-id="551d0-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="551d0-108">возврата Указатель на объект поддержки поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="551d0-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="551d0-109">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="551d0-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="551d0-110">возврата Дескриптор родительского окна для диалогового окна входа, который отображается в методе **logon** , если это разрешено.</span><span class="sxs-lookup"><span data-stu-id="551d0-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="551d0-111">Параметр _улуипарам_ содержит значение параметра с таким же именем, переДАННОЕ в MAPI при предыдущем вызове функции [мапилогонекс](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="551d0-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="551d0-112">_Лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="551d0-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="551d0-113">возврата Указатель на имя профиля сеанса.</span><span class="sxs-lookup"><span data-stu-id="551d0-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="551d0-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="551d0-114">_ulFlags_</span></span>
  
> <span data-ttu-id="551d0-115">возврата Битовая маска флагов, определяющая способ выполнения входа.</span><span class="sxs-lookup"><span data-stu-id="551d0-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="551d0-116">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="551d0-116">The following flags can be set:</span></span>
    
<span data-ttu-id="551d0-117">АБ_НО_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="551d0-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="551d0-118">Поставщик не должен отображать диалоговое окно во время входа.</span><span class="sxs-lookup"><span data-stu-id="551d0-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="551d0-119">Если этот флаг не установлен, поставщик может отобразить диалоговое окно, предлагающее пользователю указать отсутствующие сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="551d0-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="551d0-120">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="551d0-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="551d0-121">Обеспечивает успешный **Вход в систему** , возможно, до завершения процесса входа.</span><span class="sxs-lookup"><span data-stu-id="551d0-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="551d0-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="551d0-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="551d0-123">Все строки должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="551d0-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="551d0-124">Если флаг МАПИ_УНИКОДЕ не установлен, строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="551d0-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="551d0-125">_Лпулкбсекурити_</span><span class="sxs-lookup"><span data-stu-id="551d0-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="551d0-126">[вход, выход] Указатель на размер структуры учетных данных безопасности (в байтах), на которую указывает параметр _лппбсекурити_ .</span><span class="sxs-lookup"><span data-stu-id="551d0-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="551d0-127">На входе значение должно быть ненулевым; в выходных данных значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="551d0-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="551d0-128">В обоих случаях указатели должны быть допустимыми.</span><span class="sxs-lookup"><span data-stu-id="551d0-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="551d0-129">_Лппбсекурити_</span><span class="sxs-lookup"><span data-stu-id="551d0-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="551d0-130">[вход, выход] Указатель на указатель учетных данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="551d0-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="551d0-131">На входе значение должно быть ненулевым; в выходных данных значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="551d0-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="551d0-132">В обоих случаях указатель должен быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="551d0-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="551d0-133">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="551d0-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="551d0-134">вышли Указатель на указатель на структуру [мапиеррор](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="551d0-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="551d0-135">Параметр _лппмапиеррор_ может иметь значение null, если структура **мапиеррор** для возврата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="551d0-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="551d0-136">_Лппаблогон_</span><span class="sxs-lookup"><span data-stu-id="551d0-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="551d0-137">вышли Указатель на указатель на объект входа поставщика.</span><span class="sxs-lookup"><span data-stu-id="551d0-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="551d0-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="551d0-138">Return value</span></span>

<span data-ttu-id="551d0-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="551d0-139">S_OK</span></span> 
  
> <span data-ttu-id="551d0-140">Успешно установлено подключение к активному сеансу.</span><span class="sxs-lookup"><span data-stu-id="551d0-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="551d0-141">МАПИ_Е_ФАИЛОНЕПРОВИДЕР</span><span class="sxs-lookup"><span data-stu-id="551d0-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="551d0-142">Поставщик не может войти в систему, но MAPI может продолжать выполнять вход других поставщиков в службе сообщений, к которой принадлежит поставщик.</span><span class="sxs-lookup"><span data-stu-id="551d0-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="551d0-143">МАПИ_Е_УНКОНФИГУРЕД</span><span class="sxs-lookup"><span data-stu-id="551d0-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="551d0-144">У поставщика недостаточно сведений для завершения входа.</span><span class="sxs-lookup"><span data-stu-id="551d0-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="551d0-145">MAPI вызывает функцию ввода службы сообщений поставщика.</span><span class="sxs-lookup"><span data-stu-id="551d0-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="551d0-146">МАПИ_Е_УНКНОВН_КПИД</span><span class="sxs-lookup"><span data-stu-id="551d0-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="551d0-147">Сервер не настроен для поддержки кодовой страницы клиента.</span><span class="sxs-lookup"><span data-stu-id="551d0-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="551d0-148">МАПИ_Е_УНКНОВН_ЛЦИД</span><span class="sxs-lookup"><span data-stu-id="551d0-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="551d0-149">Сервер не настроен для поддержки информации о языковых стандартах клиента.</span><span class="sxs-lookup"><span data-stu-id="551d0-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="551d0-150">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="551d0-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="551d0-151">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне входа в систему.</span><span class="sxs-lookup"><span data-stu-id="551d0-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="551d0-152">Примечания</span><span class="sxs-lookup"><span data-stu-id="551d0-152">Remarks</span></span>

<span data-ttu-id="551d0-153">Подключения устанавливаются с каждым поставщиком адресных книг в профиле сеанса, когда клиент вызывает метод [IMAPISession:: опенаддрессбук](imapisession-openaddressbook.md) .</span><span class="sxs-lookup"><span data-stu-id="551d0-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="551d0-154">Затем **опенаддрессбук** вызывает метод **входа** каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="551d0-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="551d0-155">Имя профиля, на которое указывает параметр _лпсзпрофиленаме_ , отображается в наборе символов клиента пользователя, как указано в параметре присутствия или отсутствия флага мапи_уникоде в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="551d0-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="551d0-156">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="551d0-156">Notes to implementers</span></span>

<span data-ttu-id="551d0-157">В реализации метода **logon** вызовите метод [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) для регистрации уникального идентификатора или структуры [мапиуид](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="551d0-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="551d0-158">Каждый из объектов будет иметь идентификатор записи, включающий этот **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="551d0-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="551d0-159">MAPI использует **мапиуид** для согласования объекта со своим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="551d0-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="551d0-160">Например, когда клиент вызывает метод [IMAPISession:: OpenEntry](imapisession-openentry.md) для открытия пользователя обмена сообщениями, **OpenEntry** проверяет часть **мапиуид** переданного идентификатора записи и сопоставляет ее с **мапиуид** , зарегистрированным Поставщик адресных книг.</span><span class="sxs-lookup"><span data-stu-id="551d0-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="551d0-161">Если клиент входит в систему поставщика несколько раз, можно зарегистрировать другой **мапиуид** для каждого входа в систему.</span><span class="sxs-lookup"><span data-stu-id="551d0-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="551d0-162">Регистрация уникальных структур **мапиуид** позволяет MAPI правильно маршрутизировать запросы к соответствующему экземпляру поставщика.</span><span class="sxs-lookup"><span data-stu-id="551d0-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="551d0-163">Однако может потребоваться, чтобы каждый объект logon совместно использовать один **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="551d0-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="551d0-164">В этом случае необходимо иметь возможность самостоятельно обрабатывать маршрутизацию, а не полагаться на MAPI.</span><span class="sxs-lookup"><span data-stu-id="551d0-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="551d0-165">Дополнительные сведения о том, как создать **мапиуид**, приведены в статье [Регистрация уникальных идентификаторов поставщиков служб](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="551d0-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="551d0-166">Объект поддержки, который MAPI передает методу **logon** , в параметре _лпмаписуп_ предоставляет доступ ко многим методам, включенным в интерфейс [имаписуппорт: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="551d0-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="551d0-167">MAPI создает объект поддержки, настроенный на тип поставщика.</span><span class="sxs-lookup"><span data-stu-id="551d0-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="551d0-168">Например, если необходимо выполнить вход в базовую систему обмена сообщениями или службу каталогов при установлении подключения, можно вызвать метод [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) для получения учетных данных безопасности для этого конкретного сеанса входа.</span><span class="sxs-lookup"><span data-stu-id="551d0-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="551d0-169">Если **Вход** выполнен успешно, убедитесь, что вы вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) объекта support, чтобы увеличить значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="551d0-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="551d0-170">Это позволяет поставщику хранить указатель на объект поддержки для оставшейся части сеанса.</span><span class="sxs-lookup"><span data-stu-id="551d0-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="551d0-171">Если не вызывать этот метод **AddRef** , то MAPI выгружает поставщика.</span><span class="sxs-lookup"><span data-stu-id="551d0-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="551d0-172">Вы можете включить имя профиля, переданное в параметре _лпсзпрофиленаме_ в диалоговых окнах ошибок, диалоговых окнах входа или других пользовательских интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="551d0-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="551d0-173">Чтобы использовать имя профиля, скопируйте его в выделенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="551d0-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="551d0-174">Создайте объект logon и возвратите ему указатель на него в параметре _лппаблогон_ .</span><span class="sxs-lookup"><span data-stu-id="551d0-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="551d0-175">MAPI использует этот объект для входа, чтобы вызывать методы в реализации [иаблогон](iablogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="551d0-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="551d0-176">Если вы запрашиваете пароль при входе в систему, отображать диалоговое окно входа в систему, только если не установлен флаг АБ_НО_ДИАЛОГ.</span><span class="sxs-lookup"><span data-stu-id="551d0-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="551d0-177">Если пользователь отменяет вход в систему, то, как правило, при нажатии кнопки **Отмена** в диалоговом окне возвращается значение мапи_е_усер_канцел из поля **Вход**.</span><span class="sxs-lookup"><span data-stu-id="551d0-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="551d0-178">Как правило, когда поставщик адресной книги не может войти в систему, MAPI отключает службу сообщений, к которой принадлежит неисправность поставщика, то есть MAPI не пытается установить подключения для других поставщиков, принадлежащих службе, для оставшейся части сеанса. время жизни.</span><span class="sxs-lookup"><span data-stu-id="551d0-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="551d0-179">Тем не менее, если поставщик не может установить подключение и вы не хотите отключать всю службу, возвращается значение МАПИ_Е_ФАИЛОНЕПРОВИДЕР или МАПИ_Е_УНКОНФИГУРЕД.</span><span class="sxs-lookup"><span data-stu-id="551d0-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="551d0-180">MAPI не отключит службу сообщений, к которой относится поставщик.</span><span class="sxs-lookup"><span data-stu-id="551d0-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="551d0-181">Возвращает МАПИ_Е_ФАИЛОНЕПРОВИДЕР, если возникла ошибка, которая не является достаточно серьезной для предотвращения установки подключений другими поставщиками в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="551d0-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="551d0-182">Возвращает МАПИ_Е_УНКОНФИГУРЕД, если в профиле отсутствуют необходимые сведения о конфигурации, и не удается отобразить диалоговое окно для приглашения пользователя.</span><span class="sxs-lookup"><span data-stu-id="551d0-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="551d0-183">MAPI ответит, вызвав функцию точки входа службы сообщений поставщика с МСГ_СЕРВИЦЕ_КОНФИГУРЕ, установленным в качестве параметра _улконтекст_ , чтобы предоставить службе возможность настроить себя либо программно, либо с помощью таблицы свойств.</span><span class="sxs-lookup"><span data-stu-id="551d0-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="551d0-184">После завершения функции точки входа службы сообщений MAPI повторяет попытку входа.</span><span class="sxs-lookup"><span data-stu-id="551d0-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="551d0-185">См. также</span><span class="sxs-lookup"><span data-stu-id="551d0-185">See also</span></span>



[<span data-ttu-id="551d0-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="551d0-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="551d0-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="551d0-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="551d0-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="551d0-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="551d0-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="551d0-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="551d0-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="551d0-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="551d0-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="551d0-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

