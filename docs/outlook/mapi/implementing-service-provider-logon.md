---
title: Реализация входа для поставщика службы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401645"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="118be-103">Реализация входа для поставщика службы</span><span class="sxs-lookup"><span data-stu-id="118be-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="118be-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="118be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="118be-105">MAPI вызывает метод в объект поставщика для начала процесса входа в систему с помощью указателя, который возвращает из вашей функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="118be-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="118be-106">Метод следующим образом может отличаться в зависимости от типа поставщика услуг:</span><span class="sxs-lookup"><span data-stu-id="118be-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="118be-107">[IABProvider::Logon](iabprovider-logon.md) для поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="118be-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="118be-108">[IMSProvider::Logon](imsprovider-logon.md) для поставщиков хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="118be-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="118be-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) для поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="118be-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="118be-110">Выполните следующие задачи в любой реализации метода входа в систему.</span><span class="sxs-lookup"><span data-stu-id="118be-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="118be-111">Увеличивает счетчик ссылок на объекте поддержки, который передается в качестве входного параметра путем вызова метода [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="118be-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="118be-112">Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки для доступа к вашей раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="118be-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="118be-113">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля для настройки следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="118be-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="118be-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="118be-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="118be-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="118be-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="118be-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="118be-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="118be-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="118be-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="118be-118">Не следует задать свойства **PR_RESOURCE_FLAGS** или **PR_PROVIDER_DLL_NAME** раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="118be-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="118be-119">Во время входа в систему эти свойства доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="118be-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="118be-120">Проверьте, что свойства, которые необходимы для настройки хранятся в профиле или от пользователя.</span><span class="sxs-lookup"><span data-stu-id="118be-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="118be-121">Дополнительные сведения о проверке конфигурации можно [Проверка конфигурации поставщика службы](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="118be-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="118be-122">Вызов метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) объекта поддержки для регистрации уникального идентификатора или [MAPIUID](mapiuid.md), если ваш поставщик является поставщик адресной книги или сообщения хранилища.</span><span class="sxs-lookup"><span data-stu-id="118be-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="118be-123">Поставщики транспорта зарегистрировать структур **MAPIUID** при MAPI вызывает метод их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="118be-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="118be-124">Дополнительные сведения о регистрации **MAPIUID**можно [Регистрации уникальных идентификаторов поставщика службы](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="118be-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="118be-125">Создайте экземпляр объекта входа в систему и возврата с одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="118be-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="118be-126">Значение S_OK для указания успешного входа в систему.</span><span class="sxs-lookup"><span data-stu-id="118be-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="118be-127">MAPI_E_UNCONFIGURED, чтобы указать, что один или несколько свойств конфигурации будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="118be-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="118be-128">MAPI_E_USER_CANCEL, чтобы указать, что пользователь отменил окно настройки вызывает ошибку свойства конфигурации, которые будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="118be-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="118be-129">MAPI_E_FAILONEPROVIDER, чтобы указать, что ваш поставщик может не настроен, но, что MAPI, должна поддерживать его для использования в любом случае.</span><span class="sxs-lookup"><span data-stu-id="118be-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="118be-130">Методы входа в систему должна вернуть это значение, чтобы сообщить о Исправимая ошибка, например, когда поставщика требуется пароль и не могут запрашивать у пользователя его так, как отключить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="118be-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="118be-131">Предыдущая список задач описываются минимальные реализации метода входа в систему поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="118be-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="118be-132">При необходимости можно включить дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="118be-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="118be-133">Например некоторые поставщики вызов [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для обновления таблицы состояния в их способ входа в систему.</span><span class="sxs-lookup"><span data-stu-id="118be-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="118be-134">Для достижения наилучшей производительности во время входа в систему, избегайте вызова [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) или [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="118be-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="118be-135">Перед эти вызовы можно выполнить и вернуть управление в метод входа в систему, необходимо запустить диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="118be-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="118be-136">См. также</span><span class="sxs-lookup"><span data-stu-id="118be-136">See also</span></span>

- [<span data-ttu-id="118be-137">Запуск поставщика службы</span><span class="sxs-lookup"><span data-stu-id="118be-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

