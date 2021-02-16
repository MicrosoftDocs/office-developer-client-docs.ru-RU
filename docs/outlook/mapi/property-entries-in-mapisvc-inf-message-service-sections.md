---
title: Записи свойств в разделах службы сообщений MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427999"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="b2e31-103">Записи свойств в разделах службы сообщений MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="b2e31-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="b2e31-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2e31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2e31-105">Записи, которые устанавливают свойства, используют этот формат:</span><span class="sxs-lookup"><span data-stu-id="b2e31-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="b2e31-106">**тег свойства** **=** значение свойства</span><span class="sxs-lookup"><span data-stu-id="b2e31-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="b2e31-107">Тег свойства может быть стандартным тегом свойства MAPI, если данные конфигурации представляют одно из свойств, предопределенных MAPI, или нестандартным тегом, если данные не представляют свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2e31-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="b2e31-108">Нестандартный тег состоит из объединения значения идентификатора свойства с типом свойства.</span><span class="sxs-lookup"><span data-stu-id="b2e31-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="b2e31-109">В результате будет 8-значное 8-значное число.</span><span class="sxs-lookup"><span data-stu-id="b2e31-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="b2e31-110">Значение свойства может быть любым, что имеет смысл для тега свойства.</span><span class="sxs-lookup"><span data-stu-id="b2e31-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="b2e31-111">Разделы службы сообщений могут содержать различные записи в зависимости от настраиваемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="b2e31-112">Следующие свойства MAPI обычно включаются в раздел служб сообщений в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="b2e31-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="b2e31-113">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="b2e31-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="b2e31-114">**PR_SERVICE_DLL_NAME**  =   _имя DLL-файла_</span><span class="sxs-lookup"><span data-stu-id="b2e31-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="b2e31-115">**PR_SERVICE_ENTRY_NAME**  =   _имя функции точки входа_</span><span class="sxs-lookup"><span data-stu-id="b2e31-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="b2e31-116">**PR_SERVICE_SUPPORT_FILES**  =   _список файлов_</span><span class="sxs-lookup"><span data-stu-id="b2e31-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="b2e31-117">**PR_SERVICE_DELETE_FILES**  =   _список файлов_</span><span class="sxs-lookup"><span data-stu-id="b2e31-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="b2e31-118">**PR_RESOURCE_FLAGS**  =   _битоваяmask_</span><span class="sxs-lookup"><span data-stu-id="b2e31-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="b2e31-119">Строка **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)— это имя службы сообщений, которая отображается в пользовательском интерфейсе, имя, которое пользователь связывает со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="b2e31-120">Отображаемая запись — это необязательная запись в mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="b2e31-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="b2e31-121">Иногда отображаемого имени состоит из двух частей; часть, назначенная службой сообщений, и часть, назначенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="b2e31-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="b2e31-122">Если пользователь отвечает за назначение одной из частей, это обычно обрабатывается с помощью специального диалоговое окно, известное как лист свойств, предоставленный службой сообщений под управлением клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="b2e31-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="b2e31-123">Сведения, предоставленные для **записи PR_SERVICE_DLL_NAME** ([PidTagServiceDllName),](pidtagservicedllname-canonical-property.md)— это имя DLL-записи, которая содержит службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="b2e31-124">Сведения, предоставленные для записи **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName),](pidtagserviceentryname-canonical-property.md)— это имя функции точки входа в этой DLL, которую MAPI вызывает для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="b2e31-125">Файлы, перечисленные в **записи PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles),](pidtagservicesupportfiles-canonical-property.md)— это файлы, которые необходимо установить вместе со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="b2e31-126">Аналогично, файлы в записи **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles)](pidtagservicedeletefiles-canonical-property.md)необходимо удалить при удалении службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="b2e31-127">Запись **PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)— это коллекция параметров, определенных для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2e31-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="b2e31-128">Например, SERVICE_SINGLE_COPY задается, если служба сообщений может отображаться в заданном профиле только один раз.</span><span class="sxs-lookup"><span data-stu-id="b2e31-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="b2e31-129">Бит SERVICE_NO_PRIMARY_IDENTITY, если служба сообщений не предоставляет идентификацию.</span><span class="sxs-lookup"><span data-stu-id="b2e31-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="b2e31-130">Вот два примера записей нестандартных свойств.</span><span class="sxs-lookup"><span data-stu-id="b2e31-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="b2e31-131">Первая запись указывает путь к файлу, используемму адресной книгой по умолчанию в качестве значения свойства; Вторая запись указывает числовый значение свойства.</span><span class="sxs-lookup"><span data-stu-id="b2e31-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="b2e31-132">Обе записи имеют значение, определенное для службы сообщений ab.</span><span class="sxs-lookup"><span data-stu-id="b2e31-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


