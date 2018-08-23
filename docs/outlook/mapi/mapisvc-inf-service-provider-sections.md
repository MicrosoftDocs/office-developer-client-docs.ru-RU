---
title: Разделы поставщика службы MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586783"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="2109b-103">Разделы поставщика службы MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="2109b-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="2109b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2109b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2109b-105">Mapisvc.inf включает в себя один раздел поставщика службы для каждой записи, указанные в запись **поставщиков** в предыдущем разделе служб сообщения.</span><span class="sxs-lookup"><span data-stu-id="2109b-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="2109b-106">Разделы поставщика **службы** аналогичны разделах службы сообщений в обоих типов разделы содержат записи в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="2109b-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="2109b-107">**свойство tag** = значение свойства</span><span class="sxs-lookup"><span data-stu-id="2109b-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="2109b-108">Тем не менее разделах службы сообщений и разделах поставщика службы отличаются, такие свойства операции — это единственный тип операции, содержатся в разделах поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="2109b-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="2109b-109">Может быть без дополнительных или связанные разделы для поставщиков услуг; все сведения о поставщике услуг должен содержаться в один раздел.</span><span class="sxs-lookup"><span data-stu-id="2109b-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="2109b-110">Некоторые свойства, в разделах службы сообщений также задан в разделах поставщика службы, так как эти свойства смысла для них.</span><span class="sxs-lookup"><span data-stu-id="2109b-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="2109b-111">Свойство **PR_DISPLAY_NAME** приведен пример.</span><span class="sxs-lookup"><span data-stu-id="2109b-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="2109b-112">Поставщиков услуг и службы сообщений иметь имя, которое используется для отображения в пользовательском интерфейсе конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2109b-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="2109b-113">В зависимости от поставщика услуг это имя может или не может быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="2109b-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="2109b-114">Другие свойства специфичны для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="2109b-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="2109b-115">Разделы поставщика обычной службы включают следующие записи, каждый из которых являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="2109b-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="2109b-116">**PR_DISPLAY_NAME** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="2109b-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="2109b-117">**PR_PROVIDER_DISPLAY** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="2109b-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="2109b-118">**PR_PROVIDER_DLL_NAME** =  _имя DLL-файла_</span><span class="sxs-lookup"><span data-stu-id="2109b-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="2109b-119">**PR_RESOURCE_TYPE** =  _времени_</span><span class="sxs-lookup"><span data-stu-id="2109b-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="2109b-120">**PR_RESOURCE_FLAGS** =  _битовой маски_</span><span class="sxs-lookup"><span data-stu-id="2109b-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="2109b-121">Запись **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) похож на **PR_SERVICE_DLL_NAME**; Указывает имя файла для библиотеки DLL, которая содержит поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2109b-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="2109b-122">Код сообщения службы могут храниться в одном из его поставщиков услуг в один и тот же файл DLL или существовать в качестве отдельной библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="2109b-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="2109b-123">Обратите внимание на то, что не суффикс включается в запись вне зависимости от целевой платформы; Отвечает за MAPI добавляется суффикс, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="2109b-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="2109b-124">**PR_RESOURCE_TYPE** Запись ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) представляет тип поставщика услуг; Поставщики услуг установить соответствующий предварительно определенная константа.</span><span class="sxs-lookup"><span data-stu-id="2109b-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="2109b-125">Допустимые значения включают MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER и MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="2109b-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="2109b-126">Другой записи свойства, которое применяется к службы сообщений и поставщиков услуг, запись **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) указывает параметры.</span><span class="sxs-lookup"><span data-stu-id="2109b-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="2109b-127">Параметры для этой записи свойство может отличаться в зависимости от поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2109b-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="2109b-128">Например некоторые поставщики хранилища сообщений может значение **PR_RESOURCE_FLAGS** STATUS_NO_DEFAULT_STORE если они никогда не могут работать как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2109b-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="2109b-129">Выполните три примера разделах поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="2109b-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="2109b-130">В разделе **[AB поставщика]** — раздел поставщика службы для службы адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2109b-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="2109b-131">В разделах **[MsgService Prov1]** и **[MsgService Prov2]** принадлежат мои собственные службы; раздел поставщик адресной книги — это первый и второй — раздел поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2109b-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
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


