---
title: Реализация входа у поставщика услуг
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
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="b0671-103">Реализация входа у поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="b0671-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="b0671-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0671-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0671-105">MAPI вызывает метод в объекте поставщика, чтобы начать процесс входа с помощью указателя, возвращенного из функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="b0671-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="b0671-106">Метод изменяется следующим образом в зависимости от типа поставщика услуг:</span><span class="sxs-lookup"><span data-stu-id="b0671-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="b0671-107">[Иабпровидер:: вход](iabprovider-logon.md) для поставщиков адресных книг</span><span class="sxs-lookup"><span data-stu-id="b0671-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="b0671-108">[Функцииimsprovider:: вход в систему](imsprovider-logon.md) для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="b0671-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="b0671-109">[Иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="b0671-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="b0671-110">Выполните следующие действия в любом методе входа, который вы реализуете:</span><span class="sxs-lookup"><span data-stu-id="b0671-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="b0671-111">Увеличьте значение счетчика ссылок для объекта support, который передается в качестве входного параметра, вызвав его метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0671-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="b0671-112">Вызовите метод [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) объекта support для доступа к разделу профиля.</span><span class="sxs-lookup"><span data-stu-id="b0671-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="b0671-113">Вызовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) раздела profile, чтобы задать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="b0671-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="b0671-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0671-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="b0671-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0671-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="b0671-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0671-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="b0671-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0671-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="b0671-118">Не пытайтесь задать свойства **PR_RESOURCE_FLAGS** и **PR_PROVIDER_DLL_NAME** раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="b0671-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="b0671-119">Во время входа эти свойства доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b0671-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="b0671-120">Убедитесь, что свойства, необходимые для настройки, хранятся в профиле или доступны от пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0671-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="b0671-121">Для получения дополнительных сведений о проверке конфигурации ознакомьтесь со статьей [Проверка конфигурации поставщика услуг](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="b0671-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="b0671-122">Вызовите метод [имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) объекта support, чтобы зарегистрировать уникальный идентификатор, или [мапиуид](mapiuid.md), если поставщик является адресной книгой или поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0671-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="b0671-123">Поставщики транспорта регистрируют структуры **мапиуид** при вызове MAPI метода [Иксплогон:: аддресстипес](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="b0671-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="b0671-124">Дополнительные сведения о регистрации **мапиуид**можно найти в статье [Регистрация уникальных идентификаторов поставщиков служб](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b0671-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="b0671-125">Создайте экземпляр объекта logon и возвратите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b0671-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="b0671-126">S_OK, чтобы обозначить успешный вход в систему.</span><span class="sxs-lookup"><span data-stu-id="b0671-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="b0671-127">MAPI_E_UNCONFIGURED, чтобы указать, что одно или несколько свойств конфигурации были недоступны.</span><span class="sxs-lookup"><span data-stu-id="b0671-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="b0671-128">MAPI_E_USER_CANCEL, чтобы указать, что пользователь отменил диалоговое окно Configuration, что привело к недоступности свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b0671-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="b0671-129">MAPI_E_FAILONEPROVIDER, чтобы указать, что поставщик не может быть настроен, но MAPI должен разрешить его использование независимо.</span><span class="sxs-lookup"><span data-stu-id="b0671-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="b0671-130">Методы входа должны возвращать это значение, чтобы сообщить о неустранимой ошибке, например, когда поставщик требует пароль и не может запросить пользователя, так как интерфейс пользователя отключен.</span><span class="sxs-lookup"><span data-stu-id="b0671-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="b0671-131">В предыдущем списке задач описывается минимальная реализация метода входа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="b0671-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="b0671-132">При необходимости можно включить дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="b0671-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="b0671-133">Например, некоторые поставщики вызывают [имаписуппорт:: модифистатусров](imapisupport-modifystatusrow.md) для обновления таблицы состояний в методе logon.</span><span class="sxs-lookup"><span data-stu-id="b0671-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b0671-134">Чтобы обеспечить наилучшую производительность при входе в систему, не выполняйте вызов [имаписуппорт::P репаресубмит](imapisupport-preparesubmit.md) или [Имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="b0671-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="b0671-135">Перед выполнением этих вызовов и возвратом управления методу входа в систему необходимо запустить диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0671-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0671-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b0671-136">See also</span></span>

- [<span data-ttu-id="b0671-137">Запуск поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="b0671-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

