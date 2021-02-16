---
title: Реализация входа и входа поставщика адресной книги
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
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="45cf2-103">Реализация входа и входа поставщика адресной книги</span><span class="sxs-lookup"><span data-stu-id="45cf2-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="45cf2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45cf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45cf2-105">Поставщики адресных книг поддерживают вход и вход в сеанс, реализуя методы интерфейса [IABProvider : IUnknown.](iabprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="45cf2-106">Интерфейс \*\* IABProvider \*\* наследуется непосредственно от **IUnknown** и добавляет только два других метода: **Logon** и **Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="45cf2-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="45cf2-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="45cf2-107">Logoff</span></span>

<span data-ttu-id="45cf2-108">MAPI будет вызывать метод [IABProvider::Logon](iabprovider-logon.md) поставщика в начале каждого сеанса и каждый раз, когда поставщик добавляется в текущий профиль и клиент поддерживает динамическую перенастройку.</span><span class="sxs-lookup"><span data-stu-id="45cf2-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="45cf2-109">Когда MAPI вызывает метод **IABProvider::Logon,** поставщик адресной книги начинает процесс его работы.</span><span class="sxs-lookup"><span data-stu-id="45cf2-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="45cf2-110">**Реализация IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="45cf2-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="45cf2-111">Инициализировать все указатели выходных параметров, переданные MAPI.</span><span class="sxs-lookup"><span data-stu-id="45cf2-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="45cf2-112">Вызовите метод **IUnknown::AddRef** объекта поддержки, чтобы добавить его количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="45cf2-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="45cf2-113">Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы открыть раздел профиля, содержащий сведения о конфигурации поставщика.</span><span class="sxs-lookup"><span data-stu-id="45cf2-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="45cf2-114">Передав NULL для  _параметра lpUID_ и MAPI_MODIFY флага, если вы собираетесь внести изменения.</span><span class="sxs-lookup"><span data-stu-id="45cf2-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="45cf2-115">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) раздела профиля, чтобы получить свойства, необходимые поставщику для работы с данными, например имя файла данных или таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="45cf2-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="45cf2-116">Убедитесь, что все свойства доступны и действительны.</span><span class="sxs-lookup"><span data-stu-id="45cf2-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="45cf2-117">Если необходимо и разрешено, вы можете отобразить диалоговое окно с запросом на внесение исправлений или дополнений в недопустимые или отсутствующие сведения, а также вызвать метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="45cf2-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="45cf2-118">Некоторые из общих свойств, которые должны быть доступны:</span><span class="sxs-lookup"><span data-stu-id="45cf2-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="45cf2-119">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="45cf2-120">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="45cf2-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="45cf2-122">**PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="45cf2-123">Не **задав PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md) **или PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName).](pidtagproviderdllname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="45cf2-124">Во время logon эти свойства являются только для чтения.</span><span class="sxs-lookup"><span data-stu-id="45cf2-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="45cf2-125">Если одно или несколько свойств конфигурации недоступны, сбой и возврат значения MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="45cf2-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="45cf2-126">Вызов [IMAPISupport::SetProviderUID для](imapisupport-setprovideruid.md) регистрации [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="45cf2-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="45cf2-127">Поставщик может создать **MAPIUID** с помощью:</span><span class="sxs-lookup"><span data-stu-id="45cf2-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="45cf2-128">Вызов метода [IMAPISupport::NewUID.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="45cf2-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="45cf2-129">Вызов средства UUIDGEN.EXE для определения GUID, который поставщик использует для включаемого в один из файлов его заголовок.</span><span class="sxs-lookup"><span data-stu-id="45cf2-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="45cf2-130">При желании сохраните только что созданный **MAPIUID** в текущем профиле, вызывая метод \*\* IMAPIProp::SetProps \*\* раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="45cf2-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="45cf2-131">Освободите раздел профиля, вызывая его метод **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="45cf2-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="45cf2-132">Создать новый объект для логотипа и установить для содержимого параметра  _lppABLogon_ адрес этого нового объекта.</span><span class="sxs-lookup"><span data-stu-id="45cf2-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="45cf2-133">Так как MAPI может вызвать метод \*\* Logon \*\* несколько раз во время сеанса, целесообразно поддерживать эту возможность в реализации, создав несколько объектов для логотипа и отслеживая каждый созданный объект.</span><span class="sxs-lookup"><span data-stu-id="45cf2-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="45cf2-134">Поддержка **нескольких вызовов** входа позволяет пользователю клиентского приложения, например, войти в сеанс с разными удостоверениями или использовать разные места доставки.</span><span class="sxs-lookup"><span data-stu-id="45cf2-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="45cf2-135">**Завершение работы** происходит после завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="45cf2-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="45cf2-136">MAPI вызывает метод [IABProvider::Shutdown](iabprovider-shutdown.md) как одну из последних задач, которые связаны с завершением сеанса.</span><span class="sxs-lookup"><span data-stu-id="45cf2-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="45cf2-137">MAPI выпустила все объекты для работы с вашим поставщиком и, когда поставщик получает этот вызов, он может предположить, что это последний вызов, который он получит.</span><span class="sxs-lookup"><span data-stu-id="45cf2-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="45cf2-138">В реализации **IABProvider::Shutdown** выполните окончательную очистку, которую вы считаете необходимой.</span><span class="sxs-lookup"><span data-stu-id="45cf2-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="45cf2-139">Например, поставщик может вызвать **MAPIDeinitIdle,** если он вызвал **MAPIInitIdle,** чтобы использовать обработчик бездействия во время сеанса, или метод **IUnknown::Release** любых объектов, которые еще не были отпущены.</span><span class="sxs-lookup"><span data-stu-id="45cf2-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="45cf2-140">Если у поставщика нет окончательной очистки, его реализация может быть состоит из одной строки кода:</span><span class="sxs-lookup"><span data-stu-id="45cf2-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


