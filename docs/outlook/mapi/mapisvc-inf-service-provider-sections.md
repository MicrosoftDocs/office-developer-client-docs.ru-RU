---
title: Разделы поставщика служб MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405564"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="e7510-103">Разделы поставщика служб MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="e7510-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="e7510-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7510-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7510-105">Mapisvc.inf содержит один раздел поставщика услуг для каждой записи, перечисленной в записи **Поставщики** в предыдущем разделе служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="e7510-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="e7510-106">**Разделы** поставщика услуг похожи на разделы службы сообщений, так как оба типа разделов содержат записи в этом формате:</span><span class="sxs-lookup"><span data-stu-id="e7510-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="e7510-107">**тег свойства** = значение свойства</span><span class="sxs-lookup"><span data-stu-id="e7510-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="e7510-108">Однако разделы поставщика услуг и разделы службы сообщений отличаются тем, что такие записи свойств являются единственным типом записи, включенной в разделы поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e7510-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="e7510-109">Для поставщиков услуг не может быть дополнительных или связанных разделов; Все сведения о поставщике услуг должны содержаться в одном разделе.</span><span class="sxs-lookup"><span data-stu-id="e7510-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="e7510-110">Некоторые свойства, установленные в разделах службы сообщений, также замещение в разделах поставщика услуг, так как эти свойства имеют смысл для обоих.</span><span class="sxs-lookup"><span data-stu-id="e7510-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="e7510-111">Примером **PR_DISPLAY_NAME** является свойство PR_DISPLAY_NAME.</span><span class="sxs-lookup"><span data-stu-id="e7510-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="e7510-112">Как поставщики услуг, так и службы сообщений имеют имя, которое используется для отображения в пользовательском интерфейсе конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e7510-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="e7510-113">В зависимости от поставщика услуг это имя может быть или не быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="e7510-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="e7510-114">Другие свойства являются специфическими для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e7510-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="e7510-115">Типичные разделы поставщиков услуг включают следующие записи, все из которых являются обязательной:</span><span class="sxs-lookup"><span data-stu-id="e7510-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="e7510-116">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="e7510-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="e7510-117">**PR_PROVIDER_DISPLAY**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="e7510-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="e7510-118">**PR_PROVIDER_DLL_NAME**  =   _имя DLL-файла_</span><span class="sxs-lookup"><span data-stu-id="e7510-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="e7510-119">**PR_RESOURCE_TYPE**  =   _long_</span><span class="sxs-lookup"><span data-stu-id="e7510-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="e7510-120">**PR_RESOURCE_FLAGS**  =   _битоваяmask_</span><span class="sxs-lookup"><span data-stu-id="e7510-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="e7510-121">Запись **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)аналогична **PR_SERVICE_DLL_NAME;** он указывает имя файла для DLL, которая содержит поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e7510-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="e7510-122">Код службы сообщений может храниться у одного из поставщиков услуг в том же DLL-файле или существовать как отдельная DLL.</span><span class="sxs-lookup"><span data-stu-id="e7510-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="e7510-123">Обратите внимание, что суффикс не включен в запись независимо от целевой платформы; MAPI при необходимости добавляет суффикс.</span><span class="sxs-lookup"><span data-stu-id="e7510-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="e7510-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) представляет тип поставщика услуг; поставщики услуг присваивают ему соответствующую предопределеную константу.</span><span class="sxs-lookup"><span data-stu-id="e7510-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="e7510-125">Допустимые значения: MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER и MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="e7510-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="e7510-126">Другая запись свойства, которая применяется как к службам сообщений, так и к поставщикам служб, PR_RESOURCE_FLAGS **(** [PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)указывает параметры.</span><span class="sxs-lookup"><span data-stu-id="e7510-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="e7510-127">Параметры для этой записи свойства могут отличаться в зависимости от поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e7510-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="e7510-128">Например, некоторые поставщики  store сообщений могут PR_RESOURCE_FLAGS значение STATUS_NO_DEFAULT_STORE, если они никогда не смогут работать как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7510-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="e7510-129">В этом примере следуют три примера разделов поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e7510-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="e7510-130">Раздел **[Поставщик ab]** — это раздел поставщика услуг для службы адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7510-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="e7510-131">Разделы **[MsgService Prov1]** и **[MsgService Prov2]** относятся к моей собственной службе; Первый раздел является разделом поставщика адресной книги, а второй — разделом поставщика службы хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e7510-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


