---
title: 'Файл конфигурации формы: раздел [Платформы]'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808476"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="eaf11-103">Файл конфигурации формы: раздел [Платформы]</span><span class="sxs-lookup"><span data-stu-id="eaf11-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="eaf11-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eaf11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eaf11-105">В разделе **[платформ]** представлен полный набор платформ, поддерживаются в эту форму.</span><span class="sxs-lookup"><span data-stu-id="eaf11-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="eaf11-106">Каждая запись платформы состоит из префикса **платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="eaf11-107">_строка_, где _строка_ — код произвольную строку для платформы.</span><span class="sxs-lookup"><span data-stu-id="eaf11-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="eaf11-108">Каждая строка соответствует записи **ЦП** отдельных разделов **[платформ]** .</span><span class="sxs-lookup"><span data-stu-id="eaf11-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="eaf11-109">Каждая запись в раздел **[платформ]** задает _строки платформы_ , которая ссылается на последующих **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="eaf11-110">_строка платформы_ раздел **]** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="eaf11-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="eaf11-111">В разделе **[платформ]** представлен полный набор платформ, поддерживаются в эту форму.</span><span class="sxs-lookup"><span data-stu-id="eaf11-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="eaf11-112">Каждая запись платформы состоит из префикса **платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="eaf11-113">_строка_, где _строка_ — код произвольную строку для платформы.</span><span class="sxs-lookup"><span data-stu-id="eaf11-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="eaf11-114">Каждая строка соответствует записи **ЦП** отдельных разделов **[платформ]** .</span><span class="sxs-lookup"><span data-stu-id="eaf11-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="eaf11-115">Каждая запись в раздел **[платформ]** задает _строки платформы_ , которая ссылается на последующих **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="eaf11-116">_строка платформы_ раздел **]** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="eaf11-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="eaf11-117">**[Платформ]**</span><span class="sxs-lookup"><span data-stu-id="eaf11-117">**[Platforms]**</span></span>
  
<span data-ttu-id="eaf11-118">**Платформа**.</span><span class="sxs-lookup"><span data-stu-id="eaf11-118">**Platform**.</span></span> <span data-ttu-id="eaf11-119">_Строка_ =  _строки платформы_</span><span class="sxs-lookup"><span data-stu-id="eaf11-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="eaf11-120">Ниже приведен пример раздела **[платформ]** .</span><span class="sxs-lookup"><span data-stu-id="eaf11-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="eaf11-121">Каждый **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-121">Each **[Platform.**</span></span> <span data-ttu-id="eaf11-122">_строка платформы_ раздел **]** содержит два необходимые записи, **ЦП** и **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="eaf11-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="eaf11-123">**Загрузка ЦП** указывается процессора и **OSVersion** указывается в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="eaf11-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="eaf11-124">Допустимые значения **ЦП** описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="eaf11-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="eaf11-125">**Запись ЦП**</span><span class="sxs-lookup"><span data-stu-id="eaf11-125">**CPU Entry**</span></span>|<span data-ttu-id="eaf11-126">**Процессор**</span><span class="sxs-lookup"><span data-stu-id="eaf11-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eaf11-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="eaf11-127">Ix86</span></span>  <br/> |<span data-ttu-id="eaf11-128">Intel 80 x 86 и процессора Pentium серии, а также эквивалентный процессоры AMD, Cyrix, NextGen и других производителей.</span><span class="sxs-lookup"><span data-stu-id="eaf11-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="eaf11-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="eaf11-129">MIPS</span></span>  <br/> |<span data-ttu-id="eaf11-130">Процессоры серии MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="eaf11-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="eaf11-131">AXP</span><span class="sxs-lookup"><span data-stu-id="eaf11-131">AXP</span></span>  <br/> |<span data-ttu-id="eaf11-132">Процессор цифровой AXP буква корпорация оборудования.</span><span class="sxs-lookup"><span data-stu-id="eaf11-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="eaf11-133">PPC</span><span class="sxs-lookup"><span data-stu-id="eaf11-133">PPC</span></span>  <br/> |<span data-ttu-id="eaf11-134">Процессоры серии Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="eaf11-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="eaf11-135">M68</span><span class="sxs-lookup"><span data-stu-id="eaf11-135">M68</span></span>  <br/> |<span data-ttu-id="eaf11-136">Процессоры серии Mororola 68 x 00.</span><span class="sxs-lookup"><span data-stu-id="eaf11-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="eaf11-137">Допустимые значения **OSVersion** описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="eaf11-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="eaf11-138">**Запись OSVersion**</span><span class="sxs-lookup"><span data-stu-id="eaf11-138">**OSVersion Entry**</span></span>|<span data-ttu-id="eaf11-139">**Операционная система**</span><span class="sxs-lookup"><span data-stu-id="eaf11-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eaf11-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="eaf11-140">Win3.1</span></span>  <br/> |<span data-ttu-id="eaf11-141">Windows 3.1 и Windows для рабочих групп 3.11.</span><span class="sxs-lookup"><span data-stu-id="eaf11-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="eaf11-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="eaf11-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="eaf11-143">Windows NT 3.5 или меньше.</span><span class="sxs-lookup"><span data-stu-id="eaf11-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="eaf11-144">Win95</span><span class="sxs-lookup"><span data-stu-id="eaf11-144">Win95</span></span>  <br/> |<span data-ttu-id="eaf11-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="eaf11-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="eaf11-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="eaf11-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="eaf11-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="eaf11-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="eaf11-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="eaf11-148">Mac7</span></span>  <br/> |<span data-ttu-id="eaf11-149">Система Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="eaf11-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="eaf11-150">Кроме того **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="eaf11-151">_строка платформы_ раздел **]** должен содержать запись **файла** или **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="eaf11-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="eaf11-152">Запись **файла** перечислены формы server исполняемый файл приложения, который поддерживает и загружает в новый подкаталог в дисковый кэш при запуске формы библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="eaf11-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="eaf11-153">Если вместо этого используется **LinkTo** запись, содержит имя строки другой платформы, из которого взят сведения о **файле** .</span><span class="sxs-lookup"><span data-stu-id="eaf11-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="eaf11-154">Это полезно, если одной версии формы поддерживает несколько платформ.</span><span class="sxs-lookup"><span data-stu-id="eaf11-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="eaf11-155">Запись **реестра** используется при каждом использовании запись **файла** , определяет раздел реестра для библиотеки форм, где хранится исполняемый файл для серверного приложения формы.</span><span class="sxs-lookup"><span data-stu-id="eaf11-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="eaf11-156">Строки стоять обратной косой черты (\) помещаются в корне реестра.</span><span class="sxs-lookup"><span data-stu-id="eaf11-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="eaf11-157">Строки не предшествует обратную косую черту помещаются в HKEY_CLASSES_ROOT\CLSID\ _GUID_\ раздел реестра, где _GUID_ — это **GUID** формы.</span><span class="sxs-lookup"><span data-stu-id="eaf11-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="eaf11-158">Чтобы указать путь к каталогу, из которого чтение файла конфигурации формы можно использовать символы «%d».</span><span class="sxs-lookup"><span data-stu-id="eaf11-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="eaf11-159">Этот метод подходит для указания других файлов с помощью путей относительно файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="eaf11-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="eaf11-160">Записи **реестра** или **Нескольких файлов** можно указать, используя файл или реестра в качестве префикса, а затем другой текст.</span><span class="sxs-lookup"><span data-stu-id="eaf11-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="eaf11-161">Формат для **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-161">The format for the **[Platform.**</span></span> <span data-ttu-id="eaf11-162">_строка платформы_ раздел **]** :</span><span class="sxs-lookup"><span data-stu-id="eaf11-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="eaf11-163">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-163">**[Platform.**</span></span> <span data-ttu-id="eaf11-164">_строка платформы_ **]**</span><span class="sxs-lookup"><span data-stu-id="eaf11-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="eaf11-165">**Загрузка ЦП** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="eaf11-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="eaf11-166">**OSVersion** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="eaf11-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="eaf11-167">**Файл** =  _путь_</span><span class="sxs-lookup"><span data-stu-id="eaf11-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="eaf11-168">**LinkTo** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="eaf11-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="eaf11-169">**Реестр** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="eaf11-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="eaf11-170">Далее представлены два примера **[платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="eaf11-171">_строка платформы_ разделы **]** с помощью запись **файла** и с помощью **LinkTo** запись.</span><span class="sxs-lookup"><span data-stu-id="eaf11-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="eaf11-172">**[Платформы.**</span><span class="sxs-lookup"><span data-stu-id="eaf11-172">The **[Platform.**</span></span> <span data-ttu-id="eaf11-173">_строка платформы_ раздел **]** игнорируется при добавлении формы в библиотеку локальной форме, если предполагается, что программа установки для размещения файлов, определить обработчик класса сообщений в локальное хранилище доступно как с именем обработчика раздела в реестре OLE и выполненная Регистрация OLE в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="eaf11-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

