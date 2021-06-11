---
title: Записи свойств в разделах Службы сообщений MapiSvc.inf
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
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="2c859-103">Записи свойств в разделах Службы сообщений MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="2c859-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="2c859-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c859-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c859-105">Записи, заданной свойствами, используют этот формат:</span><span class="sxs-lookup"><span data-stu-id="2c859-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="2c859-106">**тег свойства** **=** значение свойства</span><span class="sxs-lookup"><span data-stu-id="2c859-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="2c859-107">Тег свойства может быть стандартным тегом свойства MAPI, если данные конфигурации представляют одно из свойств, предопределенных MAPI, или нестандартный тег, если данные не представляют свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c859-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="2c859-108">Нестандартный тег выполнен путем объединения значения идентификатора свойства с типом свойства.</span><span class="sxs-lookup"><span data-stu-id="2c859-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="2c859-109">В результате будет 8-значное гексадецимальное число.</span><span class="sxs-lookup"><span data-stu-id="2c859-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="2c859-110">Значение свойства может быть любым, что имеет смысл для тега свойства.</span><span class="sxs-lookup"><span data-stu-id="2c859-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="2c859-111">Разделы службы сообщений могут содержать различные записи в зависимости от настраиваемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c859-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="2c859-112">Следующие свойства MAPI обычно включаются в раздел служб сообщений в перечисленном формате:</span><span class="sxs-lookup"><span data-stu-id="2c859-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="2c859-113">**PR_DISPLAY_NAME**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="2c859-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="2c859-114">**PR_SERVICE_DLL_NAME**  =   _имя файла DLL_</span><span class="sxs-lookup"><span data-stu-id="2c859-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="2c859-115">**PR_SERVICE_ENTRY_NAME**  =   _имя функции точки входа_</span><span class="sxs-lookup"><span data-stu-id="2c859-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="2c859-116">**PR_SERVICE_SUPPORT_FILES**  =   _список файлов_</span><span class="sxs-lookup"><span data-stu-id="2c859-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="2c859-117">**PR_SERVICE_DELETE_FILES**  =   _список файлов_</span><span class="sxs-lookup"><span data-stu-id="2c859-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="2c859-118">**PR_RESOURCE_FLAGS**  =   _bitmask_</span><span class="sxs-lookup"><span data-stu-id="2c859-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="2c859-119">Строка **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)— это имя службы сообщений, которая отображается в пользовательском интерфейсе, имя, которое пользователь связывает со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c859-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="2c859-120">Имя отображения — необязательная запись в mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="2c859-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="2c859-121">Иногда имя отображения состоит из двух частей; часть, назначенная службой сообщений, и часть, назначенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="2c859-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="2c859-122">Если пользователь отвечает за назначение одной из частей, это обычно обрабатывается с помощью специального диалогового окна, известного как лист свойств, предоставленный службой сообщений под управлением клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="2c859-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="2c859-123">Сведения, предоставленные для **PR_SERVICE_DLL_NAME** [(PidTagServiceDllName)](pidtagservicedllname-canonical-property.md)— это имя службы сообщений DLL.</span><span class="sxs-lookup"><span data-stu-id="2c859-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="2c859-124">Сведения, предоставленные для **записи PR_SERVICE_ENTRY_NAME** [(PidTagServiceEntryName)](pidtagserviceentryname-canonical-property.md)— это имя функции точки входа в этой DLL, которую MAPI вызывает для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c859-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="2c859-125">Файлы, перечисленные в **записи PR_SERVICE_SUPPORT_FILES** [(PidTagServiceSupportFiles),](pidtagservicesupportfiles-canonical-property.md)— это файлы, которые необходимо установить в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c859-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="2c859-126">Кроме того, файлы в записи **PR_SERVICE_DELETE_FILES** [(PidTagServiceDeleteFiles)](pidtagservicedeletefiles-canonical-property.md)должны быть удалены при удалении службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c859-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="2c859-127">Запись **PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)— это набор параметров, определенных для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c859-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="2c859-128">Например, SERVICE_SINGLE_COPY устанавливается, когда служба сообщений может отображаться только один раз в заданном профиле.</span><span class="sxs-lookup"><span data-stu-id="2c859-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="2c859-129">Набор SERVICE_NO_PRIMARY_IDENTITY, если служба сообщений не предоставляет сведений о удостоверениях.</span><span class="sxs-lookup"><span data-stu-id="2c859-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="2c859-130">Следуют два примера нестандартных записей свойств.</span><span class="sxs-lookup"><span data-stu-id="2c859-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="2c859-131">Первая запись указывает путь к файлу, используемму адресной книгой по умолчанию в качестве значения свойства; вторая запись указывает числовую ценность свойства.</span><span class="sxs-lookup"><span data-stu-id="2c859-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="2c859-132">Обе записи имеют значение, определенное для службы сообщений AB.</span><span class="sxs-lookup"><span data-stu-id="2c859-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


