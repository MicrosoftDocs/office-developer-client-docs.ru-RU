---
title: Файл конфигурации формы [платформы] Раздел
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419130"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="f55a8-103">Файл конфигурации формы [платформы] Раздел</span><span class="sxs-lookup"><span data-stu-id="f55a8-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="f55a8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f55a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f55a8-105">В **разделе [Платформы]** перечислены все платформы, поддерживаемые этой формой.</span><span class="sxs-lookup"><span data-stu-id="f55a8-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="f55a8-106">Каждая запись платформы состоит из префикса **Platform.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="f55a8-107">_строка,_  _где строка_ является произвольным строковым кодом для платформы.</span><span class="sxs-lookup"><span data-stu-id="f55a8-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="f55a8-108">Каждая строка соответствует записи **ЦП** отдельных **разделов [Платформы].**</span><span class="sxs-lookup"><span data-stu-id="f55a8-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="f55a8-109">Каждая запись в **разделе [Платформы]** определяет строку платформы, которая ссылается на **следующий [Platform).** </span><span class="sxs-lookup"><span data-stu-id="f55a8-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="f55a8-110">_раздел "строка_ **платформы]** как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="f55a8-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="f55a8-111">В **разделе [Платформы]** перечислены все платформы, поддерживаемые этой формой.</span><span class="sxs-lookup"><span data-stu-id="f55a8-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="f55a8-112">Каждая запись платформы состоит из префикса **Platform.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="f55a8-113">_строка,_  _где строка_ является произвольным строковым кодом для платформы.</span><span class="sxs-lookup"><span data-stu-id="f55a8-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="f55a8-114">Каждая строка соответствует записи **ЦП** отдельных **разделов [Платформы].**</span><span class="sxs-lookup"><span data-stu-id="f55a8-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="f55a8-115">Каждая запись в **разделе [Платформы]** определяет строку платформы, которая ссылается на **следующий [Platform).** </span><span class="sxs-lookup"><span data-stu-id="f55a8-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="f55a8-116">_раздел "строка_ **платформы]** как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="f55a8-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="f55a8-117">**[Платформы]**</span><span class="sxs-lookup"><span data-stu-id="f55a8-117">**[Platforms]**</span></span>
  
<span data-ttu-id="f55a8-118">**Платформа.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-118">**Platform**.</span></span> <span data-ttu-id="f55a8-119">_string_  =   _строка платформы_</span><span class="sxs-lookup"><span data-stu-id="f55a8-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="f55a8-120">Ниже приводится пример раздела **[Платформы].**</span><span class="sxs-lookup"><span data-stu-id="f55a8-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="f55a8-121">Каждая **[платформа.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-121">Each **[Platform.**</span></span> <span data-ttu-id="f55a8-122">_Раздел строки_ **платформы ]** содержит две необходимые записи: **ЦП** и **OSVersion.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="f55a8-123">Запись **ЦП** указывает процессор, а **запись OSVersion** — операционную систему.</span><span class="sxs-lookup"><span data-stu-id="f55a8-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="f55a8-124">**Допустимые значения** ЦП описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f55a8-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="f55a8-125">**Запись ЦП**</span><span class="sxs-lookup"><span data-stu-id="f55a8-125">**CPU Entry**</span></span>|<span data-ttu-id="f55a8-126">**Процессор**</span><span class="sxs-lookup"><span data-stu-id="f55a8-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f55a8-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="f55a8-127">Ix86</span></span>  <br/> |<span data-ttu-id="f55a8-128">Процессоры Intel 80x86 и серии Pentium, а также эквивалентные процессоры amD, Cyrix, NextGen и других производителей.</span><span class="sxs-lookup"><span data-stu-id="f55a8-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="f55a8-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="f55a8-129">MIPS</span></span>  <br/> |<span data-ttu-id="f55a8-130">Процессоры серии MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="f55a8-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="f55a8-131">AXP</span><span class="sxs-lookup"><span data-stu-id="f55a8-131">AXP</span></span>  <br/> |<span data-ttu-id="f55a8-132">Процессор Alpha AXP компании Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="f55a8-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="f55a8-133">PPC</span><span class="sxs-lookup"><span data-stu-id="f55a8-133">PPC</span></span>  <br/> |<span data-ttu-id="f55a8-134">Процессоры серии Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="f55a8-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="f55a8-135">M68</span><span class="sxs-lookup"><span data-stu-id="f55a8-135">M68</span></span>  <br/> |<span data-ttu-id="f55a8-136">Процессоры серии Mororola 68x00.</span><span class="sxs-lookup"><span data-stu-id="f55a8-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="f55a8-137">Допустимые значения **OSVersion** описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f55a8-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="f55a8-138">**Запись OSVersion**</span><span class="sxs-lookup"><span data-stu-id="f55a8-138">**OSVersion Entry**</span></span>|<span data-ttu-id="f55a8-139">**Операционная система**</span><span class="sxs-lookup"><span data-stu-id="f55a8-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f55a8-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="f55a8-140">Win3.1</span></span>  <br/> |<span data-ttu-id="f55a8-141">Windows 3.1 и Windows для workgroups 3.11.</span><span class="sxs-lookup"><span data-stu-id="f55a8-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="f55a8-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="f55a8-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="f55a8-143">Windows NT 3,5 или ниже.</span><span class="sxs-lookup"><span data-stu-id="f55a8-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="f55a8-144">Win95</span><span class="sxs-lookup"><span data-stu-id="f55a8-144">Win95</span></span>  <br/> |<span data-ttu-id="f55a8-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f55a8-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="f55a8-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="f55a8-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="f55a8-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="f55a8-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="f55a8-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="f55a8-148">Mac7</span></span>  <br/> |<span data-ttu-id="f55a8-149">Система Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="f55a8-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="f55a8-150">Кроме того, **[Платформа.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="f55a8-151">_раздел строки_ **платформы ]** должен содержать запись **File** или **LinkTo.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="f55a8-152">Запись **"Файл"** содержит исполняемый файл приложения сервера форм, который библиотека форм поддерживает и загружает в новый подпапок в дисковом кэше при запуске формы.</span><span class="sxs-lookup"><span data-stu-id="f55a8-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="f55a8-153">Если вместо этого используется запись **LinkTo,** она содержит имя другой строки платформы, из которой взяты **сведения** о файле.</span><span class="sxs-lookup"><span data-stu-id="f55a8-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="f55a8-154">Это полезно, если одна версия формы поддерживает несколько платформ.</span><span class="sxs-lookup"><span data-stu-id="f55a8-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="f55a8-155">Запись **реестра** используется всякий раз, когда используется запись файла, она определяет ключ реестра для библиотеки форм, в которой хранится исполняемый файл для приложения сервера форм. </span><span class="sxs-lookup"><span data-stu-id="f55a8-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="f55a8-156">Строки, предшествующие backslash ( \ ) размещаются в корне реестра.</span><span class="sxs-lookup"><span data-stu-id="f55a8-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="f55a8-157">Строки, не предшествующие косой строке, помещаются в HKEY_CLASSES_ROOT\CLSID\ GUID \ ключ реестра, где _GUID_— **это GUID** формы. </span><span class="sxs-lookup"><span data-stu-id="f55a8-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="f55a8-158">С символами "%d" можно указать путь к каталогу, из которого был считаен файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="f55a8-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="f55a8-159">Это полезно для указания других файлов с именами путей относительно файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="f55a8-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="f55a8-160">**Несколько записей** **в** файле или реестре могут быть заданы с помощью префикса "Файл" или "Реестр", за которым следует любой другой текст.</span><span class="sxs-lookup"><span data-stu-id="f55a8-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="f55a8-161">Формат для **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-161">The format for the **[Platform.**</span></span> <span data-ttu-id="f55a8-162">_Раздел "строка_ **платформы]** " является:</span><span class="sxs-lookup"><span data-stu-id="f55a8-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="f55a8-163">**[Платформа.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-163">**[Platform.**</span></span> <span data-ttu-id="f55a8-164">_строка платформы_ **]**</span><span class="sxs-lookup"><span data-stu-id="f55a8-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="f55a8-165">**ЦП**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f55a8-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="f55a8-166">**OSVersion**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f55a8-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="f55a8-167">**Файл**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="f55a8-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="f55a8-168">**LinkTo**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f55a8-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="f55a8-169">**Реестр**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f55a8-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="f55a8-170">Ниже приводится два примера **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="f55a8-171">_строка_ **платформы ]** разделы, один с использованием записи **файла,** а другой с использованием **записи LinkTo.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

<span data-ttu-id="f55a8-172">**[Платформа.**</span><span class="sxs-lookup"><span data-stu-id="f55a8-172">The **[Platform.**</span></span> <span data-ttu-id="f55a8-173"> Раздел строки платформы **]** игнорируется при добавлении формы в локонную библиотеку форм, когда предполагается, что установщик поместил файлы, оформив обработщик класса сообщений, в доступное локальное хранилище, как по имени в разделе обработщика в реестре OLE, и зарегистрировал OLE в реестре системы.</span><span class="sxs-lookup"><span data-stu-id="f55a8-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

