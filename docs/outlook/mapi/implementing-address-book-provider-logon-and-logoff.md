---
title: Реализация входа и выхода для поставщика адресных книг
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438738"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="efa52-103">Реализация входа и выхода для поставщика адресных книг</span><span class="sxs-lookup"><span data-stu-id="efa52-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="efa52-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efa52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efa52-105">Поставщики адресных книг поддерживают вход в сеанс и выход из нее путем реализации методов интерфейса [иабпровидер: IUnknown](iabprovideriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="efa52-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="efa52-106">Интерфейс \* \* Иабпровидер \* \* наследуется напрямую от **IUnknown** и добавляет только два других метода: **Вход** и **Завершение**.</span><span class="sxs-lookup"><span data-stu-id="efa52-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="efa52-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="efa52-107">Logoff</span></span>

<span data-ttu-id="efa52-108">MAPI вызывает метод [иабпровидер:: logon](iabprovider-logon.md) поставщика в начале каждого сеанса и каждый раз, когда поставщик добавляется в текущий профиль, и клиент поддерживает динамическую перенастройку.</span><span class="sxs-lookup"><span data-stu-id="efa52-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="efa52-109">Когда MAPI вызывает метод **иабпровидер:: logon** , поставщик адресных книг начинает процесс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="efa52-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="efa52-110">**Реализация Иабпровидер:: log**</span><span class="sxs-lookup"><span data-stu-id="efa52-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="efa52-111">Инициализируйте все указатели выходных параметров, переданные с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="efa52-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="efa52-112">Вызовите метод **IUnknown:: AddRef** объекта support, чтобы увеличить счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="efa52-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="efa52-113">Вызовите метод [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) объекта support, чтобы открыть раздел профиля, содержащий сведения о конфигурации поставщика.</span><span class="sxs-lookup"><span data-stu-id="efa52-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="efa52-114">Передайте значение NULL для параметра _лпуид_ и флага MAPI_MODIFY, если вы собираетесь вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="efa52-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="efa52-115">Вызовите метод [IMAPIProp::/PROPS](imapiprop-getprops.md) раздела profile, чтобы получить свойства, необходимые поставщику для входа в систему, например имя файла данных или таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="efa52-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="efa52-116">Убедитесь, что свойства доступны и действительны.</span><span class="sxs-lookup"><span data-stu-id="efa52-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="efa52-117">Если необходимо, отобразите диалоговое окно, предлагающее пользователю внести исправления или добавления в недопустимые или отсутствующие сведения, и вызвать метод [IMAPIProp:: SetProps](imapiprop-setprops.md) для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="efa52-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="efa52-118">Ниже приведены некоторые из стандартных свойств, которые должны быть доступны.</span><span class="sxs-lookup"><span data-stu-id="efa52-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="efa52-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efa52-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="efa52-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efa52-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="efa52-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efa52-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="efa52-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="efa52-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="efa52-123">Не задавайте **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) или **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="efa52-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="efa52-124">Во время входа эти свойства доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="efa52-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="efa52-125">Если одно или несколько свойств конфигурации недоступны, произошел отказ и возвратите значение MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="efa52-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="efa52-126">Call [имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) для регистрации [мапиуид](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="efa52-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="efa52-127">Поставщик может создать **мапиуид** , выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="efa52-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="efa52-128">Вызов метода [имаписуппорт:: невуид](imapisupport-newuid.md) .</span><span class="sxs-lookup"><span data-stu-id="efa52-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="efa52-129">Вызов УУИДЖЕН. EXE, чтобы определить GUID, который использует поставщик для включения в один из файлов заголовков.</span><span class="sxs-lookup"><span data-stu-id="efa52-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="efa52-130">При необходимости сохраните недавно созданный **мапиуид** в текущем профиле, вызвав метод \* \* IMAPIProp:: SetProps \* \*.</span><span class="sxs-lookup"><span data-stu-id="efa52-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="efa52-131">Отпустите раздел профиля, вызвав его метод **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="efa52-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="efa52-132">Создайте экземпляр нового объекта logon и задайте для параметра _лппаблогон_ значение Address этого нового объекта.</span><span class="sxs-lookup"><span data-stu-id="efa52-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="efa52-133">Так как MAPI может вызывать метод \* \* logon \* \* несколько раз во время сеанса, рекомендуется обеспечить возможность создания нескольких объектов входа и отслеживания каждого созданного объекта в вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="efa52-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="efa52-134">Поддержка нескольких вызовов **входа** позволяет пользователю клиентского приложения, например, выполнить вход в сеанс с другими удостоверениями или использовать другие назначения доставки.</span><span class="sxs-lookup"><span data-stu-id="efa52-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="efa52-135">**Завершение работы** вызывается при завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="efa52-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="efa52-136">MAPI вызывает метод [иабпровидер:: Shutdown](iabprovider-shutdown.md) в качестве одной из последних задач, связанных с завершением сеанса.</span><span class="sxs-lookup"><span data-stu-id="efa52-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="efa52-137">MAPI освободил все объекты входа поставщика и, когда поставщик получает этот вызов, он может предположить, что этот вызов будет получен последним.</span><span class="sxs-lookup"><span data-stu-id="efa52-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="efa52-138">В реализации **иабпровидер:: Shutdown**, выполните последнюю очистку, которая вам нужна.</span><span class="sxs-lookup"><span data-stu-id="efa52-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="efa52-139">Например, поставщик может вызвать **мапидеинитидле** , если он вызывал **мапиинитидле** , чтобы использовать антивирусное ядро во время сеанса или метод **IUnknown:: Release** всех объектов, которые еще не были выпущены.</span><span class="sxs-lookup"><span data-stu-id="efa52-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="efa52-140">Если у поставщика нет завершающей очистки, его реализация может состоять из одной строки кода:</span><span class="sxs-lookup"><span data-stu-id="efa52-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


