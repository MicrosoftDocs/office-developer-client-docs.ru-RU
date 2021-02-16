---
title: Ссылки на функции MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346887"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="8eafb-103">Ссылки на функции MAPI</span><span class="sxs-lookup"><span data-stu-id="8eafb-103">Link to MAPI functions</span></span>

<span data-ttu-id="8eafb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8eafb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8eafb-105">Существует три способа связывания: неявное связывание, явное связывание и новая гибридная модель с помощью библиотеки заголовок MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="8eafb-106">Неявное связывание</span><span class="sxs-lookup"><span data-stu-id="8eafb-106">Implicit linking</span></span>

<span data-ttu-id="8eafb-107">Традиционно вызов функций MAPI в приложении для обмена сообщениями всегда связывался с библиотекой Mapi32.lib.</span><span class="sxs-lookup"><span data-stu-id="8eafb-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="8eafb-108">Это включало вызовы MAPI маршрутов в библиотеку загонов Windows MAPI, Mapi32.dll, которая затем перенаададовыла вызовы в клиентскую реализацию MAPI по умолчанию во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="8eafb-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="8eafb-109">Этот процесс вызова называется неявной связью.</span><span class="sxs-lookup"><span data-stu-id="8eafb-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="8eafb-110">В левой части рисунка ниже показан пример неявной связи, используемой в процессе вызова функции MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="8eafb-111">Этот процесс инициализировался приложением MAPI и включает библиотеку MAPI (Mapi32.lib) и загую Windows MAPI (Mapi32.dll) и его можно завершить с помощью клиентской реализации MAPI Outlook в загладке MAPI (Msmapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="8eafb-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="8eafb-112">**Сравнение неявных и явных ссылок.**</span><span class="sxs-lookup"><span data-stu-id="8eafb-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="8eafb-113">![Сравнение неявного и явного связывания](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Сравнения неявных и явных ссылок")</span><span class="sxs-lookup"><span data-stu-id="8eafb-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="8eafb-114">Явное связывание</span><span class="sxs-lookup"><span data-stu-id="8eafb-114">Explicit linking</span></span>

<span data-ttu-id="8eafb-115">Так как клиент MAPI по умолчанию поддерживает установку по требованию с помощью установщика Windows (MSI), можно разрабатывать приложения для обмена сообщениями непосредственно на загоне MAPI Outlook, а не с помощью библиотеки MAPI и загона Windows MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="8eafb-116">В правой части предыдущего рисунка показан пример процесса вызова функции MAPI, начиная с приложения MAPI, которое ищет путь и имя DLL для загладки MAPI Outlook (шаг 2 в следующем разделе) и делает вызов функции в загрезке Outlook MAPI (шаг 3 в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="8eafb-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="8eafb-117">В следующей процедуре показано, как вызывать функции MAPI с использованием явных ссылок.</span><span class="sxs-lookup"><span data-stu-id="8eafb-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8eafb-118">Эти сведения об явных связываниях могут быть лишними в соответствии с вашими потребностями с появлением MAPIStubLibrary.lib, рассмотренного в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="8eafb-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="8eafb-119">Как и неявная модель, новая библиотека управляет всем и реализует явную логику связывания, которая загружает MAPI Outlook напрямую.</span><span class="sxs-lookup"><span data-stu-id="8eafb-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="8eafb-120">Дополнительные сведения об явных ссылках см. в явной ссылке.</span><span class="sxs-lookup"><span data-stu-id="8eafb-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="8eafb-121">Вызов элементов API MAPI без библиотеки MAPI и заголовки Windows MAPI</span><span class="sxs-lookup"><span data-stu-id="8eafb-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="8eafb-122">В файле программы создайте глобальный список указателей функций для каждого используемого элемента API MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="8eafb-123">В следующем примере показан этот шаг.</span><span class="sxs-lookup"><span data-stu-id="8eafb-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="8eafb-124">Создайте функцию, которая инициализирует функции MAPI для ссылки на DLL MAPI клиента MAPI по умолчанию (например, Msmapi32.dll Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="8eafb-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="8eafb-125">В этой функции сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="8eafb-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="8eafb-126">Загруз mapi32.dll из соответствующего системного каталога.</span><span class="sxs-lookup"><span data-stu-id="8eafb-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="8eafb-127">X64 или x86 в основном</span><span class="sxs-lookup"><span data-stu-id="8eafb-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="8eafb-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="8eafb-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="8eafb-129">x86 в режиме WoW</span><span class="sxs-lookup"><span data-stu-id="8eafb-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="8eafb-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="8eafb-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="8eafb-131">Вызовите [функцию FGetComponentPath,](fgetcomponentpath.md) чтобы получить путь и имя DLL, реализуя подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="8eafb-132">Дополнительные сведения см. в [поддоме "Выбор конкретной версии MAPI для загрузки".](how-to-choose-a-specific-version-of-mapi-to-load.md)</span><span class="sxs-lookup"><span data-stu-id="8eafb-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="8eafb-133">Загрузив DLL, выполняв вызов функции LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="8eafb-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="8eafb-134">Инициализировать массив указателей функции MAPI с помощью вызова функции GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="8eafb-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="8eafb-135">В следующем примере показаны предыдущие шаги:</span><span class="sxs-lookup"><span data-stu-id="8eafb-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="8eafb-136">Наконец, вызовите функцию, созданную на шаге 2 в приложении для обмена сообщениями, прежде чем вызывать элементы API MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="8eafb-137">Перед закрытием приложения необходимо инициализировать подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="8eafb-138">В следующем примере показан этот шаг:</span><span class="sxs-lookup"><span data-stu-id="8eafb-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="8eafb-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="8eafb-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="8eafb-140">Для полной реализации Microsoft Outlook 2010, русская версия 64-битного MAPI, который теперь распространяется на Microsoft Outlook 2013, требуется больше, чем традиционный 32-битный API.</span><span class="sxs-lookup"><span data-stu-id="8eafb-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="8eafb-141">Новый проект, библиотека ЗАГТ MAPI, опубликованная на веб-сайте CodePlex, представляет собой замену для Mapi32.lib, которая поддерживает создание как 32-, так и 64-битных приложений MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="8eafb-142">MAPIStubLibrary.lib устраняет необходимость явного связывания с MAPI, и после его создания можно удалить Mapi32.lib из параметров linker, заменив его на MAPIStubLibrary.lib; Никаких дальнейших изменений в коде не требуется.</span><span class="sxs-lookup"><span data-stu-id="8eafb-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="8eafb-143">Он также устраняет необходимость в написании **кода LoadLibrary,** **GetProcAddress** и **FreeLibrary** для обработки новых экспортов, включенных в этот файл библиотеки, но не в Файл Mapi32.lib, что потребуется при явном связывание.</span><span class="sxs-lookup"><span data-stu-id="8eafb-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="8eafb-144">Некоторые из новых функций, связанных с этой библиотекой, недоступны в Mapi32.lib, включают следующие:</span><span class="sxs-lookup"><span data-stu-id="8eafb-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="8eafb-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="8eafb-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="8eafb-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="8eafb-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="8eafb-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="8eafb-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="8eafb-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="8eafb-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="8eafb-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="8eafb-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="8eafb-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="8eafb-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="8eafb-151">Альтернативным способом включения библиотеки затуха MAPI является копирование исходных файлов MapiStubLibrary.cpp и StubUtils.cpp непосредственно в проект и удаление ссылок на Mapi32.lib и любой код, явным образом ссылающийся на MAPI.</span><span class="sxs-lookup"><span data-stu-id="8eafb-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="8eafb-152">Сведения о том, как создать и интегрировать библиотеку в свой проект, а также вопросы об этой библиотеке, например о том, когда и зачем ее использовать, см. в библиотеке [ЗАТМ MAPI](https://mapistublibrary.codeplex.com/documentation) на сайте CodePlex.</span><span class="sxs-lookup"><span data-stu-id="8eafb-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8eafb-153">См. также</span><span class="sxs-lookup"><span data-stu-id="8eafb-153">See also</span></span>

- [<span data-ttu-id="8eafb-154">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="8eafb-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="8eafb-155">Установка подсистемы MAPI</span><span class="sxs-lookup"><span data-stu-id="8eafb-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="8eafb-156">Установка файлов заголовок MAPI</span><span class="sxs-lookup"><span data-stu-id="8eafb-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="8eafb-157">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="8eafb-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="8eafb-158">Определение используемого метода связывания</span><span class="sxs-lookup"><span data-stu-id="8eafb-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="8eafb-159">Связывание исполняемого исполняемого с DLL-данными</span><span class="sxs-lookup"><span data-stu-id="8eafb-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="8eafb-160">Настройка ключей MSI для DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="8eafb-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

