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
ms.openlocfilehash: 30f5e0b59bacfab91a3a6c77c0b345d6299df9e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812065"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="0f258-103">Записи свойств в разделах службы сообщений MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="0f258-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="0f258-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f258-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f258-105">Записи, которые задать свойства используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0f258-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="0f258-106">**свойство tag** **=** значение свойства</span><span class="sxs-lookup"><span data-stu-id="0f258-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="0f258-107">Свойство tag может быть стандартных свойство tag MAPI Если данные конфигурации представляет одно из свойств предопределенную MAPI или нестандартного тег, если данные не представляет свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f258-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="0f258-108">Нестандартные тег выполняется путем объединения значение для свойства идентификатора с типом свойства.</span><span class="sxs-lookup"><span data-stu-id="0f258-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="0f258-109">Результатом будет на 8-разрядный шестнадцатеричный номер.</span><span class="sxs-lookup"><span data-stu-id="0f258-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="0f258-110">Значение свойства может быть все, что имеет смысл для тега свойства.</span><span class="sxs-lookup"><span data-stu-id="0f258-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="0f258-111">Разделы службы сообщение может содержать множество записей в зависимости от настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="0f258-112">Следующие свойства MAPI обычно включается в разделе службы сообщений в списке формат:</span><span class="sxs-lookup"><span data-stu-id="0f258-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="0f258-113">**PR_DISPLAY_NAME** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="0f258-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="0f258-114">**PR_SERVICE_DLL_NAME** =  _имя DLL-файла_</span><span class="sxs-lookup"><span data-stu-id="0f258-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="0f258-115">**PR_SERVICE_ENTRY_NAME** =  _имя функции точки входа_</span><span class="sxs-lookup"><span data-stu-id="0f258-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="0f258-116">**PR_SERVICE_SUPPORT_FILES** =  _список файлов_</span><span class="sxs-lookup"><span data-stu-id="0f258-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="0f258-117">**PR_SERVICE_DELETE_FILES** =  _список файлов_</span><span class="sxs-lookup"><span data-stu-id="0f258-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="0f258-118">**PR_RESOURCE_FLAGS** =  _битовой маски_</span><span class="sxs-lookup"><span data-stu-id="0f258-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="0f258-119">Строка **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — это имя службы сообщений, которая отображается в пользовательском интерфейсе, имя, которое пользователь связывается со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="0f258-120">Отображаемое имя — это необязательный запись в mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="0f258-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="0f258-121">В некоторых случаях отображаемое имя будет состоять из двух частей; часть, назначаемая по службе сообщений и часть, назначенных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f258-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="0f258-122">Если пользователь несет ответственность за назначение одну из частей, обычно это делается с специальные диалоговое окно, известных как на листе свойств, предоставляемую службой сообщения в области Управление клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="0f258-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="0f258-123">Сведения, приведенные для записи **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) — это имя библиотеки DLL, которая содержит службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="0f258-124">Сведения, приведенные для записи **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) — это имя функции точки входа в рамках этой библиотеки DLL, которая вызывает MAPI для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="0f258-125">Файлы, перечисленные в запись **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)), файлы, которые должны быть установлены с помощью службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="0f258-126">Аналогичным образом необходимо удалить файлы в запись **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) при удалении службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="0f258-127">Запись **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) — это набор параметров, определенных для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f258-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="0f258-128">Например SERVICE_SINGLE_COPY бита при службы сообщений может использоваться только один раз для заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="0f258-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="0f258-129">Если служба сообщений не предоставляет сведения об удостоверениях, устанавливается бит SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="0f258-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="0f258-130">Следуйте два примера записи нестандартные свойства.</span><span class="sxs-lookup"><span data-stu-id="0f258-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="0f258-131">Первой записи указывает путь к файлу, используемой с адресной книги по умолчанию в качестве значения свойства; Второй параметр задает числовое значение.</span><span class="sxs-lookup"><span data-stu-id="0f258-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="0f258-132">Обе операции имеют значения, относящиеся к службе сообщений AB.</span><span class="sxs-lookup"><span data-stu-id="0f258-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


