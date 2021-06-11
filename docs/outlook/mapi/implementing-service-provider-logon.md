---
title: Реализация logon поставщика услуг
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
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="23ae6-103">Реализация logon поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="23ae6-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="23ae6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23ae6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23ae6-105">MAPI вызывает метод в объекте поставщика для начала процесса логона с помощью указателя, возвращаемого с функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="23ae6-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="23ae6-106">Метод изменяется следующим образом, в зависимости от типа поставщика услуг:</span><span class="sxs-lookup"><span data-stu-id="23ae6-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="23ae6-107">[IABProvider::Logon](iabprovider-logon.md) для поставщиков адресных книг</span><span class="sxs-lookup"><span data-stu-id="23ae6-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="23ae6-108">[IMSProvider::Logon](imsprovider-logon.md) для поставщиков магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="23ae6-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="23ae6-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="23ae6-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="23ae6-110">Выполните следующие задачи в любом методе logon, который вы реализуете:</span><span class="sxs-lookup"><span data-stu-id="23ae6-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="23ae6-111">Прибавка отсчета ссылок на объект поддержки, передаваемого в качестве параметра ввода, вызывает его [метод IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23ae6-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="23ae6-112">Чтобы получить доступ к разделу профилей, позвоните в [метод IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="23ae6-113">Чтобы установить следующие свойства, позвоните по методу [IMAPIProp::SetProps в разделе IMAPIProp.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="23ae6-114">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="23ae6-115">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="23ae6-116">**PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="23ae6-117">**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="23ae6-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="23ae6-118">Не пытайтесь установить свойства PR_RESOURCE_FLAGS  **или PR_PROVIDER_DLL_NAME** профиля.</span><span class="sxs-lookup"><span data-stu-id="23ae6-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="23ae6-119">Во время логоса эти свойства являются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="23ae6-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="23ae6-120">Убедитесь, что свойства, необходимые для настройки, хранятся в профиле или доступны пользователю.</span><span class="sxs-lookup"><span data-stu-id="23ae6-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="23ae6-121">Дополнительные сведения о проверке конфигурации см. в дополнительных сведениях [о проверке конфигурации поставщика услуг.](verifying-service-provider-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="23ae6-122">Вызов метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникального идентификатора или [MAPIUID,](mapiuid.md)если поставщик является поставщиком адресной книги или магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="23ae6-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="23ae6-123">Поставщики транспорта регистрируют **структуры MAPIUID,** когда MAPI вызывает их [метод IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="23ae6-124">Дополнительные сведения о регистрации **MAPIUID** см. в документе [Registering Service Provider Unique Identifiers.](registering-service-provider-unique-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="23ae6-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="23ae6-125">Мгновенно укачив объект logon и вернись с одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="23ae6-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="23ae6-126">S_OK указать успешный логотип.</span><span class="sxs-lookup"><span data-stu-id="23ae6-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="23ae6-127">MAPI_E_UNCONFIGURED указывает, что одно или несколько свойств конфигурации недоступны.</span><span class="sxs-lookup"><span data-stu-id="23ae6-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="23ae6-128">MAPI_E_USER_CANCEL, что пользователь отменил диалоговое окно конфигурации, из-за чего свойства конфигурации были недоступны.</span><span class="sxs-lookup"><span data-stu-id="23ae6-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="23ae6-129">MAPI_E_FAILONEPROVIDER, чтобы указать, что поставщик не может быть настроен, но что MAPI следует разрешить его использовать независимо.</span><span class="sxs-lookup"><span data-stu-id="23ae6-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="23ae6-130">Методы Logon должны вернуть это значение, чтобы сообщить о нефатальной ошибке, например, когда поставщику требуется пароль и он не может подсказать пользователю его, так как пользовательский интерфейс отключен.</span><span class="sxs-lookup"><span data-stu-id="23ae6-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="23ae6-131">В предыдущем списке задач описывается минимальная реализация метода логотипа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="23ae6-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="23ae6-132">При необходимости можно включить дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="23ae6-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="23ae6-133">Например, некоторые поставщики называют [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы обновить таблицу состояния в методе logon.</span><span class="sxs-lookup"><span data-stu-id="23ae6-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="23ae6-134">Чтобы достичь максимальной производительности во время логотипа, не вызывайтесь в [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) или [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="23ae6-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="23ae6-135">Прежде чем эти вызовы смогут завершить и вернуть управление методу logon, необходимо начать использовать пуллер MAPI.</span><span class="sxs-lookup"><span data-stu-id="23ae6-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23ae6-136">См. также</span><span class="sxs-lookup"><span data-stu-id="23ae6-136">See also</span></span>

- [<span data-ttu-id="23ae6-137">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="23ae6-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

