---
title: Реализация службы для логоса
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310089"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="ce5ed-103">Реализация службы для логоса</span><span class="sxs-lookup"><span data-stu-id="ce5ed-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="ce5ed-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce5ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce5ed-105">MAPI вызывает метод в объекте поставщика, чтобы начать процесс входа с помощью указателя, возвращаемого функцией точки входа.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="ce5ed-106">Этот метод зависит от типа поставщика услуг:</span><span class="sxs-lookup"><span data-stu-id="ce5ed-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="ce5ed-107">[IABProvider::Logon](iabprovider-logon.md) для поставщиков адресных книг</span><span class="sxs-lookup"><span data-stu-id="ce5ed-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="ce5ed-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span><span class="sxs-lookup"><span data-stu-id="ce5ed-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="ce5ed-109">[IXPProvider::TransportLogon для](ixpprovider-transportlogon.md) поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="ce5ed-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="ce5ed-110">Выполните следующие задачи в любом методе для логоса, который вы реализуете:</span><span class="sxs-lookup"><span data-stu-id="ce5ed-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="ce5ed-111">Приращение отсчета ссылки на объект поддержки, который передается в качестве входного параметра, путем вызова метода [IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="ce5ed-112">Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы получить доступ к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="ce5ed-113">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля, чтобы установить следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ce5ed-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="ce5ed-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ce5ed-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="ce5ed-115">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="ce5ed-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="ce5ed-117">**PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="ce5ed-118">Не пытайтесь установить свойства PR_RESOURCE_FLAGS **или** **PR_PROVIDER_DLL_NAME** профиля.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="ce5ed-119">Во время logon эти свойства являются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="ce5ed-120">Убедитесь, что свойства, необходимые для настройки, хранятся в профиле или доступны пользователю.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="ce5ed-121">Дополнительные сведения о проверке конфигурации см. в под [вопросе "Проверка конфигурации поставщика услуг".](verifying-service-provider-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="ce5ed-122">Вызовите метод [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) объекта поддержки, чтобы зарегистрировать уникальный идентификатор или [MAPIUID,](mapiuid.md)если ваш поставщик является адресной книгой или поставщиком store сообщений.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="ce5ed-123">Поставщики транспорта регистрируют структуры **MAPIUID,** когда MAPI вызывает метод [IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="ce5ed-124">Дополнительные сведения о регистрации **MAPIUID** см. в документе [Registering Service Provider Unique Identifiers.](registering-service-provider-unique-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="ce5ed-125">С помощью одного из следующих значений обновите объект для логотипа и вернетесь:</span><span class="sxs-lookup"><span data-stu-id="ce5ed-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="ce5ed-126">S_OK, чтобы указать успешное в logon.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="ce5ed-127">MAPI_E_UNCONFIGURED, что одно или несколько свойств конфигурации недоступны.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="ce5ed-128">MAPI_E_USER_CANCEL, что пользователь отменил диалоговое окно конфигурации, из-за чего свойства конфигурации недоступны.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="ce5ed-129">MAPI_E_FAILONEPROVIDER, что поставщик не может быть настроен, но mapI должен разрешить его использовать независимо от того.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="ce5ed-130">Методы для доступа к данным должны возвращать это значение, чтобы сообщить о некритальной ошибке, например о том, что поставщику требуется пароль и он не может завести его у пользователя, так как пользовательский интерфейс отключен.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="ce5ed-131">В предыдущем списке задач описана минимальная реализация метода для работы с поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="ce5ed-132">При необходимости можно включить дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="ce5ed-133">Например, некоторые поставщики звонят по методу [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы обновить таблицу состояния.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ce5ed-134">Чтобы добиться максимальной производительности при во время работы при logon, избегайте вызова [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) или [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md)</span><span class="sxs-lookup"><span data-stu-id="ce5ed-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="ce5ed-135">Прежде чем эти вызовы завершались и возвратит управление методу для логотипа, необходимо начать работу пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce5ed-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ce5ed-136">See also</span></span>

- [<span data-ttu-id="ce5ed-137">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="ce5ed-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

