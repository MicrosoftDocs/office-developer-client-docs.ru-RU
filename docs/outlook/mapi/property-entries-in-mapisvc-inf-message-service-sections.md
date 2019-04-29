---
title: Записи свойств в разделах службы сообщений MapiSvc. INF
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
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="5a335-103">Записи свойств в разделах службы сообщений MapiSvc. INF</span><span class="sxs-lookup"><span data-stu-id="5a335-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="5a335-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a335-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a335-105">Записи, которые задают свойства, используют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="5a335-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="5a335-106">**тег Property** **=** значение свойства</span><span class="sxs-lookup"><span data-stu-id="5a335-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="5a335-107">Тег Property может быть стандартным тегом свойства MAPI, если данные конфигурации представляют одно из свойств, предопределенных MAPI, или нестандартный тег, если данные не представляют собой свойство MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a335-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="5a335-108">Нестандартный тег состоит из сочетания значения идентификатора свойства с типом свойства.</span><span class="sxs-lookup"><span data-stu-id="5a335-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="5a335-109">Результатом является 8-значное шестнадцатеричное число.</span><span class="sxs-lookup"><span data-stu-id="5a335-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="5a335-110">Значение свойства может иметь любой смысл для тега Property.</span><span class="sxs-lookup"><span data-stu-id="5a335-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="5a335-111">Разделы службы сообщений могут содержать различные записи в зависимости от настроенной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a335-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="5a335-112">Следующие свойства MAPI обычно включаются в раздел "службы сообщений" в указанном формате:</span><span class="sxs-lookup"><span data-stu-id="5a335-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="5a335-113">\*\*\*\* =  _Строка_ пр_дисплай_наме</span><span class="sxs-lookup"><span data-stu-id="5a335-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="5a335-114">**Пр_сервице_длл_наме** =  _имя файла DLL_</span><span class="sxs-lookup"><span data-stu-id="5a335-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="5a335-115">**Пр_сервице_ентри_наме** =  _имя функции точки входа_</span><span class="sxs-lookup"><span data-stu-id="5a335-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="5a335-116">**Пр_сервице_суппорт_филес** =  _список файлов_</span><span class="sxs-lookup"><span data-stu-id="5a335-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="5a335-117">**Пр_сервице_делете_филес** =  _список файлов_</span><span class="sxs-lookup"><span data-stu-id="5a335-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="5a335-118">\*\*\*\* =  _Битовая маска_ пр_ресаурце_флагс</span><span class="sxs-lookup"><span data-stu-id="5a335-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="5a335-119">Строка **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — это имя службы сообщений, отображаемое в пользовательском интерфейсе, имя, которое пользователь свяжет со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a335-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="5a335-120">Отображаемое имя является необязательной записью в Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="5a335-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="5a335-121">Иногда отображаемое имя будет состоять из двух частей; часть, назначенная службой сообщений, и часть, назначенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="5a335-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="5a335-122">Если пользователь несет ответственность за назначение одной из частей, обычно это правило обрабатывается специальным диалоговым окном, которое называется листом свойств, предоставленным службой сообщений в элементе управления клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="5a335-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="5a335-123">Сведения, предоставленные для записи **пр_сервице_длл_наме** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)), это имя библиотеки DLL, содержащей службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a335-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="5a335-124">Сведения, предоставляемые для записи **пр_сервице_ентри_наме** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), это имя функции точки входа в этой библиотеке DLL, с помощью которой вызовы MAPI настраивают службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a335-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="5a335-125">Файлы, перечисленные в записи **пр_сервице_суппорт_филес** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)), — это файлы, которые необходимо установить вместе со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a335-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="5a335-126">Аналогично, при удалении службы сообщений необходимо удалить файлы из записи **пр_сервице_делете_филес** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5a335-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="5a335-127">Запись **пр_ресаурце_флагс** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) представляет собой коллекцию параметров, определенных для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5a335-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="5a335-128">Например, бит СЕРВИЦЕ_СИНГЛЕ_КОПИ задается, когда служба сообщений может появиться только один раз в заданном профиле.</span><span class="sxs-lookup"><span data-stu-id="5a335-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="5a335-129">Бит СЕРВИЦЕ_НО_ПРИМАРИ_ИДЕНТИТИ задается, если служба сообщений не предоставляет сведения об удостоверениях.</span><span class="sxs-lookup"><span data-stu-id="5a335-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="5a335-130">Ниже приведены два примера нестандартных записей свойств.</span><span class="sxs-lookup"><span data-stu-id="5a335-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="5a335-131">Первая запись указывает путь к файлу, используемому адресной книгой по умолчанию в качестве значения свойства; Вторая запись указывает значение числового свойства.</span><span class="sxs-lookup"><span data-stu-id="5a335-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="5a335-132">Обе записи имеют значение, характерное для службы сообщений АДРЕСНОЙ книги.</span><span class="sxs-lookup"><span data-stu-id="5a335-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


