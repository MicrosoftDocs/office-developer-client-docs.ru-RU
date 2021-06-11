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
# <a name="link-to-mapi-functions"></a><span data-ttu-id="7722c-103">Ссылки на функции MAPI</span><span class="sxs-lookup"><span data-stu-id="7722c-103">Link to MAPI functions</span></span>

<span data-ttu-id="7722c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7722c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7722c-105">Существует три способа связывания: неявная привязка, явные ссылки и новая гибридная модель с помощью библиотеки STUB MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="7722c-106">Неявная привязка</span><span class="sxs-lookup"><span data-stu-id="7722c-106">Implicit linking</span></span>

<span data-ttu-id="7722c-107">Исторически функции MAPI в приложении обмена сообщениями всегда связаны со ссылкой на библиотеку Mapi32.lib.</span><span class="sxs-lookup"><span data-stu-id="7722c-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="7722c-108">Это включало маршрутику вызовов MAPI в библиотеку Windows MAPI, Mapi32.dll, которая затем перенаадлила вызовы в клиентскую реализацию MAPI по умолчанию во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7722c-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="7722c-109">Этот процесс вызова называется неявной привязкой.</span><span class="sxs-lookup"><span data-stu-id="7722c-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="7722c-110">На левой стороне следующей фигуры показан пример неявной привязки, используемой в процессе вызова функции MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="7722c-111">Процесс инициировался приложением MAPI и включает библиотеку MAPI (Mapi32.lib) и загбаум Windows MAPI (Mapi32.dll) и завершится клиентской реализацией Outlook MAPI загмы MAPI (Msmapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="7722c-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="7722c-112">**Сравнение неявных и явных ссылок.**</span><span class="sxs-lookup"><span data-stu-id="7722c-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="7722c-113">![Сравнение неявного и явного сопоставления](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "сопоставления неявной и явной связи")</span><span class="sxs-lookup"><span data-stu-id="7722c-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="7722c-114">Явные ссылки</span><span class="sxs-lookup"><span data-stu-id="7722c-114">Explicit linking</span></span>

<span data-ttu-id="7722c-115">Поскольку клиент MAPI по умолчанию поддерживает установку по требованию с помощью установки Windows (MSI), приложения обмена сообщениями можно разрабатывать непосредственно на Outlook MAPI, а не с помощью библиотеки MAPI и Windows MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="7722c-116">На правой стороне предыдущего рисунка показан пример процесса вызова функции MAPI, начиная с приложения MAPI, которое ищет путь и имя DLL для загба Outlook MAPI (шаг 2 в следующем разделе) и делает вызовы функций в Outlook MAPI (шаг 3 в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="7722c-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="7722c-117">В следующей процедуре показано, как вызывать функции MAPI с помощью явных ссылок.</span><span class="sxs-lookup"><span data-stu-id="7722c-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7722c-118">Эти сведения о явной связи могут быть лишними для ваших потребностей с введением MAPIStubLibrary.lib, рассмотренного в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="7722c-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="7722c-119">Как и неявная модель, новая библиотека управляет всем и реализует явную логику связывания, которая загружает Outlook MAPI компании.</span><span class="sxs-lookup"><span data-stu-id="7722c-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="7722c-120">Дополнительные сведения о явной ссылке см. в ссылке Explicitly.</span><span class="sxs-lookup"><span data-stu-id="7722c-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="7722c-121">Вызов элементов API MAPI без библиотеки MAPI и Windows MAPI</span><span class="sxs-lookup"><span data-stu-id="7722c-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="7722c-122">В файле программы создайте глобальный список указателей функции для каждого используемого элемента API MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="7722c-123">В следующем примере показан этот шаг.</span><span class="sxs-lookup"><span data-stu-id="7722c-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="7722c-124">Создайте функцию, которая инициализирует функции MAPI для ссылки на DLL MAPI клиента MAPI по умолчанию (например, Msmapi32.dll Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="7722c-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="7722c-125">В этой функции сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="7722c-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="7722c-126">Загрузка mapi32.dll из соответствующего каталога системы.</span><span class="sxs-lookup"><span data-stu-id="7722c-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="7722c-127">x64 или x86</span><span class="sxs-lookup"><span data-stu-id="7722c-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="7722c-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="7722c-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="7722c-129">x86 в режиме WoW</span><span class="sxs-lookup"><span data-stu-id="7722c-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="7722c-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="7722c-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="7722c-131">Позвоните [в функцию FGetComponentPath,](fgetcomponentpath.md) чтобы получить путь и имя DLL, реализуемую подсистемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="7722c-132">Дополнительные сведения см. [в специальной версии MAPI для загрузки.](how-to-choose-a-specific-version-of-mapi-to-load.md)</span><span class="sxs-lookup"><span data-stu-id="7722c-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="7722c-133">Загрузив DLL, вызов функции LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="7722c-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="7722c-134">Инициализация массива указателей функции MAPI с помощью вызова функции GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="7722c-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="7722c-135">В следующем примере показаны предыдущие действия:</span><span class="sxs-lookup"><span data-stu-id="7722c-135">The following example shows the previous steps:</span></span>
        
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

3. <span data-ttu-id="7722c-136">Наконец, перед вызовом элементов API MAPI вызывайте функцию, созданную на шаге 2 в приложении обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7722c-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="7722c-137">Перед закрытием приложения необходимо униниализовать подсистему MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="7722c-138">В следующем примере показан следующий шаг:</span><span class="sxs-lookup"><span data-stu-id="7722c-138">The following example shows this step:</span></span> 
    
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

## <a name="mapistublibrarylib"></a><span data-ttu-id="7722c-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="7722c-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="7722c-140">Появление Microsoft Outlook 2010, русская версия и 64-битных MAPI, теперь расширяющихся до Microsoft Outlook 2013, требует большего, чем традиционный 32-битный API для полной реализации.</span><span class="sxs-lookup"><span data-stu-id="7722c-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="7722c-141">Новый проект , библиотека stub MAPI, размещенная на веб-сайте CodePlex, предоставляет замену для Mapi32.lib, которая поддерживает создание как 32-битных, так и 64-битных приложений MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="7722c-142">MAPIStubLibrary.lib устраняет необходимость прямой ссылки на MAPI, и, построив ее, можно удалить Mapi32.lib из параметров linker, заменив ее на MAPIStubLibrary.lib; никаких дальнейших изменений в коде не требуется.</span><span class="sxs-lookup"><span data-stu-id="7722c-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="7722c-143">Он также устраняет необходимость записи **Кода LoadLibrary,** **GetProcAddress** и **FreeLibrary** для обработки новых экспортов, включенных в этот файл библиотеки, но не в Mapi32.lib, которые будут необходимы, если вы использовали явные ссылки.</span><span class="sxs-lookup"><span data-stu-id="7722c-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="7722c-144">Некоторые из новых функций, связанных с этой библиотекой, недоступные в Mapi32.lib, включают следующие:</span><span class="sxs-lookup"><span data-stu-id="7722c-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="7722c-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="7722c-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="7722c-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="7722c-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="7722c-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="7722c-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="7722c-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="7722c-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="7722c-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="7722c-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="7722c-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="7722c-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="7722c-151">Альтернативным методом включения библиотеки stub MAPI является копирование исходных файлов MapiStubLibrary.cpp и StubUtils.cpp непосредственно в проект и удаление любых ссылок на Mapi32.lib и любого кода, явно ссылаясь на MAPI.</span><span class="sxs-lookup"><span data-stu-id="7722c-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="7722c-152">Сведения о создании и интеграции файлов библиотеки MAPI Stub, а также вопросы об этой библиотеке, например о том, когда и зачем ее использовать, см. в библиотеке [MAPI Stub на](https://mapistublibrary.codeplex.com/documentation) сайте CodePlex.</span><span class="sxs-lookup"><span data-stu-id="7722c-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7722c-153">См. также</span><span class="sxs-lookup"><span data-stu-id="7722c-153">See also</span></span>

- [<span data-ttu-id="7722c-154">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="7722c-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="7722c-155">Установка подсистемы MAPI</span><span class="sxs-lookup"><span data-stu-id="7722c-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="7722c-156">Установка файлов заголовки MAPI</span><span class="sxs-lookup"><span data-stu-id="7722c-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="7722c-157">Выберите определенную версию MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="7722c-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="7722c-158">Определение способа привязки к использованию</span><span class="sxs-lookup"><span data-stu-id="7722c-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="7722c-159">Привязка исполняемого к DLL</span><span class="sxs-lookup"><span data-stu-id="7722c-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="7722c-160">Настройка клавиш MSI для DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="7722c-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

