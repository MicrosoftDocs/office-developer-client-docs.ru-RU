---
title: Файл конфигурации формы раздел [платформы]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327512"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="92e34-103">Файл конфигурации формы раздел [платформы]</span><span class="sxs-lookup"><span data-stu-id="92e34-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="92e34-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92e34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92e34-105">Раздел **[Platforms]** содержит полный набор платформ, поддерживаемых этой формой.</span><span class="sxs-lookup"><span data-stu-id="92e34-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="92e34-106">Каждая запись платформы состоит из префиксной **платформы.**</span><span class="sxs-lookup"><span data-stu-id="92e34-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="92e34-107">_строка_, где _String_ — это произвольный строковый код для платформы.</span><span class="sxs-lookup"><span data-stu-id="92e34-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="92e34-108">Каждая строка соответствует записи **ЦП** отдельных разделов **[Platforms]** .</span><span class="sxs-lookup"><span data-stu-id="92e34-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="92e34-109">Каждая запись в разделе **[Platforms]** определяет _строку платформы_ , которая ссылается на последующий **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="92e34-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="92e34-110">_строка платформы_ **]** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="92e34-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="92e34-111">Раздел **[Platforms]** содержит полный набор платформ, поддерживаемых этой формой.</span><span class="sxs-lookup"><span data-stu-id="92e34-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="92e34-112">Каждая запись платформы состоит из префиксной **платформы.**</span><span class="sxs-lookup"><span data-stu-id="92e34-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="92e34-113">_строка_, где _String_ — это произвольный строковый код для платформы.</span><span class="sxs-lookup"><span data-stu-id="92e34-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="92e34-114">Каждая строка соответствует записи **ЦП** отдельных разделов **[Platforms]** .</span><span class="sxs-lookup"><span data-stu-id="92e34-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="92e34-115">Каждая запись в разделе **[Platforms]** определяет _строку платформы_ , которая ссылается на последующий **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="92e34-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="92e34-116">_строка платформы_ **]** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="92e34-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="92e34-117">**Embedded**</span><span class="sxs-lookup"><span data-stu-id="92e34-117">**[Platforms]**</span></span>
  
<span data-ttu-id="92e34-118">**Платформа**.</span><span class="sxs-lookup"><span data-stu-id="92e34-118">**Platform**.</span></span> <span data-ttu-id="92e34-119">__ =  строка_платформы_ строк</span><span class="sxs-lookup"><span data-stu-id="92e34-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="92e34-120">Ниже приведен пример раздела **[Platforms]** .</span><span class="sxs-lookup"><span data-stu-id="92e34-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="92e34-121">Каждая **[платформа.**</span><span class="sxs-lookup"><span data-stu-id="92e34-121">Each **[Platform.**</span></span> <span data-ttu-id="92e34-122">_строка платформы_ **]** раздел содержит два обязательных элемента: **CPU** и **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="92e34-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="92e34-123">Запись **CPU** указывает процессор, а запись **OSVersion** указывает операционную систему.</span><span class="sxs-lookup"><span data-stu-id="92e34-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="92e34-124">Допустимые значения **ЦП** описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="92e34-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="92e34-125">**Запись ЦП**</span><span class="sxs-lookup"><span data-stu-id="92e34-125">**CPU Entry**</span></span>|<span data-ttu-id="92e34-126">**Процессор**</span><span class="sxs-lookup"><span data-stu-id="92e34-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92e34-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="92e34-127">Ix86</span></span>  <br/> |<span data-ttu-id="92e34-128">Процессоры Intel 80x86 и Pentium Series, а также эквивалентные процессоры с AMD, Cyrix, Некстжен и другие производители.</span><span class="sxs-lookup"><span data-stu-id="92e34-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="92e34-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="92e34-129">MIPS</span></span>  <br/> |<span data-ttu-id="92e34-130">Процессоры серии MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="92e34-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="92e34-131">AXP</span><span class="sxs-lookup"><span data-stu-id="92e34-131">AXP</span></span>  <br/> |<span data-ttu-id="92e34-132">Процессор Digital Digital Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="92e34-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="92e34-133">ППК</span><span class="sxs-lookup"><span data-stu-id="92e34-133">PPC</span></span>  <br/> |<span data-ttu-id="92e34-134">Процессоры серии Power PC серии Motorola.</span><span class="sxs-lookup"><span data-stu-id="92e34-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="92e34-135">M68</span><span class="sxs-lookup"><span data-stu-id="92e34-135">M68</span></span>  <br/> |<span data-ttu-id="92e34-136">Процессоры серии Моророла 68x00.</span><span class="sxs-lookup"><span data-stu-id="92e34-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="92e34-137">Допустимые значения **OSVersion** описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="92e34-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="92e34-138">**Запись OSVersion**</span><span class="sxs-lookup"><span data-stu-id="92e34-138">**OSVersion Entry**</span></span>|<span data-ttu-id="92e34-139">**Операционная система**</span><span class="sxs-lookup"><span data-stu-id="92e34-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92e34-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="92e34-140">Win3.1</span></span>  <br/> |<span data-ttu-id="92e34-141">Windows 3,1 и Windows для рабочих групп 3,11.</span><span class="sxs-lookup"><span data-stu-id="92e34-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="92e34-142">WinNT 3.5</span><span class="sxs-lookup"><span data-stu-id="92e34-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="92e34-143">Windows NT 3,5 или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="92e34-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="92e34-144">Win95</span><span class="sxs-lookup"><span data-stu-id="92e34-144">Win95</span></span>  <br/> |<span data-ttu-id="92e34-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="92e34-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="92e34-146">WinNT 4.0</span><span class="sxs-lookup"><span data-stu-id="92e34-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="92e34-147">Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="92e34-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="92e34-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="92e34-148">Mac7</span></span>  <br/> |<span data-ttu-id="92e34-149">Система Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="92e34-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="92e34-150">Кроме того, **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="92e34-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="92e34-151">_строка платформы_ **]** раздел должен содержать либо **файл** , либо запись **линкто** .</span><span class="sxs-lookup"><span data-stu-id="92e34-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="92e34-152">В записи **файла** перечислены исполняемые файлы приложения-сервера форм, которые библиотека форм обслуживает и загружает в новый подкаталог кэша на диске при запуске формы.</span><span class="sxs-lookup"><span data-stu-id="92e34-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="92e34-153">Если вместо этого используется запись **линкто** , она содержит имя другой строки платформы, из которой берутся сведения о **файле** .</span><span class="sxs-lookup"><span data-stu-id="92e34-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="92e34-154">Это полезно, если одна версия формы поддерживает несколько платформ.</span><span class="sxs-lookup"><span data-stu-id="92e34-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="92e34-155">Запись **реестра** используется при каждом использовании записи **файла** , она определяет раздел реестра для библиотеки форм, в которой хранится исполняемый файл приложения-сервера форм.</span><span class="sxs-lookup"><span data-stu-id="92e34-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="92e34-156">Строки, которым предшествует обратная косая черта (\), размещаются в корне реестра.</span><span class="sxs-lookup"><span data-stu-id="92e34-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="92e34-157">Строки, не предшествующие обратной косой черте, помещаются в раздел ХКЭЙ_КЛАССЕС_РУТ\КЛСИД\ _GUID_\ реестра, где _GUID_ — это **GUID** формы.</span><span class="sxs-lookup"><span data-stu-id="92e34-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="92e34-158">Символы "% d" можно использовать для указания пути к каталогу, из которого был прочитан файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="92e34-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="92e34-159">Это полезно для указания других файлов с использованием путей относительно файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="92e34-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="92e34-160">**Несколько** записей **реестра** можно указать с помощью файла или реестра в качестве префикса, за которым следует любой другой текст.</span><span class="sxs-lookup"><span data-stu-id="92e34-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="92e34-161">Формат для параметра **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="92e34-161">The format for the **[Platform.**</span></span> <span data-ttu-id="92e34-162">_строка платформы_ **]** раздел:</span><span class="sxs-lookup"><span data-stu-id="92e34-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="92e34-163">**Управляем.**</span><span class="sxs-lookup"><span data-stu-id="92e34-163">**[Platform.**</span></span> <span data-ttu-id="92e34-164">_строка платформы_ **]**</span><span class="sxs-lookup"><span data-stu-id="92e34-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="92e34-165">\*\*\*\* =  _Строка_ ЦП</span><span class="sxs-lookup"><span data-stu-id="92e34-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="92e34-166">\*\*\*\* =  _Строка_ OSVersion</span><span class="sxs-lookup"><span data-stu-id="92e34-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="92e34-167">\*\*\*\* =  _Путь к_ файлу</span><span class="sxs-lookup"><span data-stu-id="92e34-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="92e34-168">\*\*\*\* =  _Строка_ линкто</span><span class="sxs-lookup"><span data-stu-id="92e34-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="92e34-169">\*\*\*\* =  _Строка_ реестра</span><span class="sxs-lookup"><span data-stu-id="92e34-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="92e34-170">Ниже приведено два примера **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="92e34-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="92e34-171">_строка платформы_ **]** , один из которых использует запись **файла** и один с помощью записи **линкто**</span><span class="sxs-lookup"><span data-stu-id="92e34-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="92e34-172">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="92e34-172">The **[Platform.**</span></span> <span data-ttu-id="92e34-173">_строка платформы_ **]** раздел игнорируется при добавлении формы в локальную библиотеку форм, когда предполагается, что установщик поместил файлы конститутинг в доступное локальное хранилище, как указано в разделе обработчика в реестре OLE и выполнил Регистрация OLE в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="92e34-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

