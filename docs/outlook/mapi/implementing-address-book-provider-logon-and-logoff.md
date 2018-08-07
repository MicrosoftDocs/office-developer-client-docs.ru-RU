---
title: Реализация входа и выхода для поставщика адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ffde0814fe5024a3f89a93462c48136712f1013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809306"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="e654f-103">Реализация входа и выхода для поставщика адресной книги</span><span class="sxs-lookup"><span data-stu-id="e654f-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="e654f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e654f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e654f-105">Поставщиками адресных книг поддерживать сеанса входа в систему и выход из системы за счет реализации методов из [IABProvider: IUnknown](iabprovideriunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e654f-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="e654f-106">** IABProvider ** интерфейс наследует непосредственно из **IUnknown** и добавляет только два других метода: **Вход в систему** и **Завершение работы**.</span><span class="sxs-lookup"><span data-stu-id="e654f-106">The ** IABProvider ** interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="e654f-107">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="e654f-107">Logoff</span></span>

<span data-ttu-id="e654f-108">MAPI будет вызов метода [IABProvider::Logon](iabprovider-logon.md) ваш поставщик в начале каждого сеанса и каждый раз, когда у поставщика добавляется в текущий профиль клиента поддерживает динамической перенастройки.</span><span class="sxs-lookup"><span data-stu-id="e654f-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="e654f-109">Когда MAPI вызывает метод **IABProvider::Logon** , адресной книге начинается его процесс входа.</span><span class="sxs-lookup"><span data-stu-id="e654f-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="e654f-110">**Для реализации IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="e654f-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="e654f-111">Инициализируйте все указатели параметра выходные данные, переданного по MAPI.</span><span class="sxs-lookup"><span data-stu-id="e654f-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="e654f-112">Вызовите метод **IUnknown::AddRef** объекта поддержки увеличить счетчик ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="e654f-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="e654f-113">Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки откройте раздел профиль, который содержит сведения о конфигурации о ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="e654f-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="e654f-114">Передайте значение NULL для параметра _lpUID_ и флаг MAPI_MODIFY, если требуется внести изменения.</span><span class="sxs-lookup"><span data-stu-id="e654f-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="e654f-115">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) раздела профиля для извлечения свойств, поставщик должен для входа в систему, таких как имя таблицы данных, файл или базы данных.</span><span class="sxs-lookup"><span data-stu-id="e654f-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="e654f-116">Убедитесь, что установлен свойства всех доступных и допустимый.</span><span class="sxs-lookup"><span data-stu-id="e654f-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="e654f-117">Если необходимо, разрешенных отображения диалогового окна на запрос пользователю для исправлений или дополнении недопустимый или отсутствующий сведения и вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="e654f-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="e654f-118">Ниже перечислены некоторые общие свойства, которые должны быть доступны:</span><span class="sxs-lookup"><span data-stu-id="e654f-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="e654f-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e654f-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="e654f-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e654f-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="e654f-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e654f-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="e654f-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e654f-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="e654f-123">Не устанавливайте **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) или **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e654f-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="e654f-124">Во время входа в систему эти свойства доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e654f-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="e654f-125">При отсутствии одного или нескольких свойств конфигурации с ошибкой, а возвращаемое значение MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="e654f-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="e654f-126">Вызов [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="e654f-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="e654f-127">Ваш поставщик можно создать **MAPIUID** с:</span><span class="sxs-lookup"><span data-stu-id="e654f-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="e654f-128">Вызов метода [IMAPISupport::NewUID](imapisupport-newuid.md) .</span><span class="sxs-lookup"><span data-stu-id="e654f-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="e654f-129">Вызов UUIDGEN. Tool exe-ФАЙЛ, чтобы задать идентификатор GUID, который использует ваш поставщик, чтобы включить в один из файлов заголовка.</span><span class="sxs-lookup"><span data-stu-id="e654f-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="e654f-130">При желании сохранить только что созданный **MAPIUID** текущего профиля, вызвав раздела профиля ** IMAPIProp::SetProps ** метод.</span><span class="sxs-lookup"><span data-stu-id="e654f-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's ** IMAPIProp::SetProps ** method.</span></span> 
    
9. <span data-ttu-id="e654f-131">Освобождение раздела профиля путем вызова метода **функции IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="e654f-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="e654f-132">Создайте экземпляр объекта входа в систему и установите содержимое параметра _lppABLogon_ адрес этого нового объекта.</span><span class="sxs-lookup"><span data-stu-id="e654f-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="e654f-133">Поскольку существует возможность MAPI для вызова вашей ** входа ** метод несколько раз во время сеанса имеет смысл для поддержки этой возможности в реализации по возможность создать несколько объектов входа в систему и отслеживание каждого объекта, которая создается.</span><span class="sxs-lookup"><span data-stu-id="e654f-133">Because it is possible for MAPI to call your ** Logon ** method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="e654f-134">Поддержка нескольких звонков **входа** позволяет пользователю из клиентского приложения, например войти в сеанс с разными удостоверениями и использования различных доставки назначений.</span><span class="sxs-lookup"><span data-stu-id="e654f-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="e654f-135">**Завершение работы** вызывается при завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="e654f-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="e654f-136">MAPI вызывает метод [IABProvider::Shutdown](iabprovider-shutdown.md) как один из последней задачи в завершение работы сеанса.</span><span class="sxs-lookup"><span data-stu-id="e654f-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="e654f-137">MAPI выпущен все объекты ваш поставщик входа в систему и, если ваш поставщик получает этот вызов, его можно допустить, что это последний звонок, он будет получать.</span><span class="sxs-lookup"><span data-stu-id="e654f-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="e654f-138">В реализации **IABProvider::Shutdown**Очистка, если вам не требуется.</span><span class="sxs-lookup"><span data-stu-id="e654f-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="e654f-139">Например ваш поставщик может вызвать **MAPIDeinitIdle** , если называется **MAPIInitIdle** простоя модуль во время сеанса или метод **функции IUnknown::Release** любые объекты, которые еще не нужно освободить по.</span><span class="sxs-lookup"><span data-stu-id="e654f-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="e654f-140">Если ваш поставщик не окончательную, его реализация может состоять из одной строки кода:</span><span class="sxs-lookup"><span data-stu-id="e654f-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


