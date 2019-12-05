---
title: Совместимость 32- и 64-разрядных версий Office
ms.date: 12/03/2019
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Узнайте о совместимости 32- и 64-разрядных версий Office.
localization_priority: Priority
ms.openlocfilehash: a0accc9c4b0198ab18b999353762a016d52f6b39
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819255"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="d6d89-103">Совместимость 32- и 64-разрядных версий Office</span><span class="sxs-lookup"><span data-stu-id="d6d89-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="d6d89-104">Узнайте о совместимости 32- и 64-разрядных версий Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="d6d89-105">Доступны 32-разрядные и 64-разрядные версии приложений Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="d6d89-106">64-разрядные версии Office позволяют перемещать более крупные объемы данных и обеспечивают дополнительные возможности (например, при работе с большими числами в Microsoft Excel 2010).</span><span class="sxs-lookup"><span data-stu-id="d6d89-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="d6d89-107">Если создаете 32-разрядный код, вы можете использовать 64-разрядную версию Office, не внося какие-либо изменения.</span><span class="sxs-lookup"><span data-stu-id="d6d89-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="d6d89-108">Если же вы создаете 64-разрядный код, в коде должны использоваться определенные ключевые слова и константы условной компиляции для обратной совместимости кода с более ранней версией Office, а при смешении 32- и 64-разрядного должен выполняться правильный код.</span><span class="sxs-lookup"><span data-stu-id="d6d89-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="d6d89-109">Visual Basic для приложений 7.0 (VBA 7) выпущен в виде 64-разрядных версий для Office и работает как с 32-, так и с 64-разрядными приложениями.</span><span class="sxs-lookup"><span data-stu-id="d6d89-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="d6d89-110">Изменения, приведенные в этой статье, применимы только к 64-разрядным версиям Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="d6d89-111">32-разрядные версии Microsoft Office позволяют использовать решения, встроенные в предыдущие версии Office, без дальнейших изменений.</span><span class="sxs-lookup"><span data-stu-id="d6d89-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d6d89-112">По умолчанию при установке 64-разрядной версии Office также устанавливается 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="d6d89-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="d6d89-113">Во время установки выберите непосредственно 64-разрядную версию Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="d6d89-114">Для работы с 64-разрядной версией в VBA 7 необходимо обновить существующие операторы Windows API (операторы **Declare**).</span><span class="sxs-lookup"><span data-stu-id="d6d89-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="d6d89-115">Кроме того, необходимо обновить адресные указатели и отобразить дескрипторы окон в пользовательских типах, которые используются этими операторами.</span><span class="sxs-lookup"><span data-stu-id="d6d89-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="d6d89-116">Эти вопросы, а также проблемы совместимости между 32-разрядной и 64-разрядной версиями и предлагаемые решения обсуждаются более подробно далее.</span><span class="sxs-lookup"><span data-stu-id="d6d89-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="d6d89-117">Сравнение 32- и 64-разрядных систем</span><span class="sxs-lookup"><span data-stu-id="d6d89-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="d6d89-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span></span>

<span data-ttu-id="d6d89-119">Приложения, созданные с использованием 64-разрядных версий Office, могут ссылаться на адресные пространства большего объема, чем приложения, созданные в 32-разрядных версиях.</span><span class="sxs-lookup"><span data-stu-id="d6d89-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="d6d89-120">Это значит, что вы можете использовать для данных больший объем физической памяти, чем раньше, и в результате снизить потребление ресурсов на перемещение данных в физическую память и из нее.</span><span class="sxs-lookup"><span data-stu-id="d6d89-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="d6d89-121">Помимо ссылок на определенные места (известных как указатели) в физической памяти, вы также можете использовать адреса для обращения к идентификаторам окна отображения (известным как дескрипторы).</span><span class="sxs-lookup"><span data-stu-id="d6d89-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="d6d89-122">Размер (в байтах) указателя или дескриптора зависит от того, какая система используется (32- или 64-разрядная).</span><span class="sxs-lookup"><span data-stu-id="d6d89-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="d6d89-123">Чтобы запустить существующие решения вместе с 64-разрядными версиями Office, учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="d6d89-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="d6d89-124">Собственные 64-разрядные процессы в Office не могут загружать 32-разрядные двоичные файлы.</span><span class="sxs-lookup"><span data-stu-id="d6d89-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="d6d89-125">Это происходит при использовании существующих элементов Microsoft ActiveX и надстроек.</span><span class="sxs-lookup"><span data-stu-id="d6d89-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="d6d89-126">Ранее в VBA не было типа данных указателя, поэтому для хранения указателей и дескрипторов приходилось использовать 32-разрядные переменные.</span><span class="sxs-lookup"><span data-stu-id="d6d89-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="d6d89-127">Теперь при использовании операторов **Declare** эти переменные усекают 64-разрядные значения, возвращаемые при вызовах API.</span><span class="sxs-lookup"><span data-stu-id="d6d89-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="d6d89-128">База кода VBA 7</span><span class="sxs-lookup"><span data-stu-id="d6d89-128">VBA 7 code base</span></span>
<span data-ttu-id="d6d89-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span></span>

<span data-ttu-id="d6d89-130">VBA 7 заменяет базу кода VBA в Office 2007 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="d6d89-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="d6d89-131">VBA 7 доступен в 32- и 64-разрядных версиях Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="d6d89-132">Он предоставляет две константы условной компиляции:</span><span class="sxs-lookup"><span data-stu-id="d6d89-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="d6d89-133">**VBA7** помогает обеспечить обратную совместимость вашего кода, проверяя, какую версию VBA использует ваше приложение — VBA 7 или более раннюю.</span><span class="sxs-lookup"><span data-stu-id="d6d89-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="d6d89-134">**Win64** проверяет разрядность кода (32- или 64-разрядный код).</span><span class="sxs-lookup"><span data-stu-id="d6d89-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="d6d89-135">За некоторыми исключениями макросы, которые работают в документе в 32-разрядной версии приложения, также будут работать в 64-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="d6d89-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="d6d89-136">Совместимость элементов ActiveX и надстроек COM</span><span class="sxs-lookup"><span data-stu-id="d6d89-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="d6d89-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span></span>

<span data-ttu-id="d6d89-138">Существующие 32-разрядные элементы ActiveX несовместимы с 64-разрядными версиями Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="d6d89-139">Для элементов ActiveX и объектов COM:</span><span class="sxs-lookup"><span data-stu-id="d6d89-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="d6d89-140">Если есть исходный код, создайте 64-разрядную версию самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="d6d89-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="d6d89-141">Если исходного кода нет, обратитесь к поставщику за обновленной версией.</span><span class="sxs-lookup"><span data-stu-id="d6d89-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="d6d89-142">Собственные 64-разрядные процессы в Office не могут загружать 32-разрядные двоичные файлы.</span><span class="sxs-lookup"><span data-stu-id="d6d89-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="d6d89-143">Сюда входят общие элементы управления **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) и элементы управления **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="d6d89-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="d6d89-144">Эти элементы управления были установлены 32-разрядными версиями Office, выпущенными до Office 2010.</span><span class="sxs-lookup"><span data-stu-id="d6d89-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="d6d89-145">При переносе кода в 64-разрядные версии Office вам потребуется найти альтернативные варианты для существующих решений VBA, использующих эти элементы управления.</span><span class="sxs-lookup"><span data-stu-id="d6d89-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="d6d89-146">Совместимость API</span><span class="sxs-lookup"><span data-stu-id="d6d89-146">API compatibility</span></span>
<span data-ttu-id="d6d89-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span></span>

<span data-ttu-id="d6d89-148">Сочетая VBA и библиотеки типов, вы получаете множество функций для создания приложений Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="d6d89-149">Однако иногда бывает необходимо взаимодействовать с операционной системой компьютера и другими компонентами напрямую (например, при управлении памятью или процессами, при работе с элементами пользовательского интерфейса, такими как окна и элементы управления, или при внесении изменений в реестр Windows).</span><span class="sxs-lookup"><span data-stu-id="d6d89-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="d6d89-150">В этих ситуациях лучше всего использовать одну из внешних функций, встроенных в DLL-файлы.</span><span class="sxs-lookup"><span data-stu-id="d6d89-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="d6d89-151">Это можно сделать в VBA, вызвав API с помощью операторов **Declare**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6d89-152">Корпорация Майкрософт предоставляет файл Win32API.txt, содержащий 1500 операторов Declare, и инструмент для копирования требуемого оператора **Declare** в ваш код.</span><span class="sxs-lookup"><span data-stu-id="d6d89-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="d6d89-153">Однако эти операторы предназначены для 32-разрядных систем и должны быть преобразованы в 64-разрядные. Это можно сделать, используя информацию, приведенную далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="d6d89-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="d6d89-154">Существующие операторы **Declare** не будут компилироваться в 64-разрядной версии VBA до тех пор, пока они не будут помечены с помощью атрибута **PtrSafe** как безопасные для 64-разрядных систем.</span><span class="sxs-lookup"><span data-stu-id="d6d89-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="d6d89-155">Вы можете найти примеры этого типа конверсии на веб-сайте Яна Карела Питерса, являющегося MVP по продуктам Excel, по адресу [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="d6d89-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="d6d89-156">[Руководство пользователя для инспектора совместимости кода Office](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) — полезный инструмент для проверки синтаксиса API оператора **Declare** на наличие атрибута **PtrSafe**, если это необходимо, и соответствующего возвращаемого типа.</span><span class="sxs-lookup"><span data-stu-id="d6d89-156">The [Office Code Compatibility Inspector user's guide](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="d6d89-157">Операторы **Declare** похожи на один из приведенных ниже примеров в зависимости от того, вызывается ли подпрограмма (без возвращаемого значения) или функция (с возвращаемым значением).</span><span class="sxs-lookup"><span data-stu-id="d6d89-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="d6d89-158">Функция **SubName** или **FunctionName** заменяется фактическим именем процедуры в файле DLL и представляет собой имя, которое используется при вызове этой процедуры из кода VBA.</span><span class="sxs-lookup"><span data-stu-id="d6d89-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="d6d89-159">Для имени процедуры можно также указать аргумент **AliasName**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="d6d89-160">Имя DLL-файла, содержащего вызываемую процедуру, следует за ключевым словом **Lib**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="d6d89-161">И, наконец, список аргументов содержит параметры и типы данных, которые должны быть переданы в процедуру.</span><span class="sxs-lookup"><span data-stu-id="d6d89-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="d6d89-162">Приведенный ниже оператор **Declare** открывает *подраздел* реестра Windows и заменяет его значение.</span><span class="sxs-lookup"><span data-stu-id="d6d89-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="d6d89-163">Запись Windows.h (дескриптор окна) для функции **RegOpenKeyA** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6d89-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="d6d89-164">В Visual C и Microsoft Visual C++ предыдущий пример правильно компилируется как для 32-разрядных, так и для 64-разрядных версий.</span><span class="sxs-lookup"><span data-stu-id="d6d89-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="d6d89-165">Это объясняется тем, что HKEY определен как указатель, размер которого показывает размер памяти платформы, на которой компилируется код.</span><span class="sxs-lookup"><span data-stu-id="d6d89-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="d6d89-166">В предыдущих версиях VBA не было определенного типа данных указателя, поэтому использовался тип **Long**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="d6d89-167">А поскольку тип данных **Long** всегда является 32-разрядным, код прерывается при работе в системе с 64-разрядной памятью, так как 32-разрядные данные могут быть усечены или перезаписаны поверх других адресов памяти.</span><span class="sxs-lookup"><span data-stu-id="d6d89-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="d6d89-168">Любая из этих ситуаций может привести к непредсказуемому поведению или сбою системы.</span><span class="sxs-lookup"><span data-stu-id="d6d89-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="d6d89-169">Для решения этой проблемы VBA содержит истинный тип данных *указателя*: **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="d6d89-170">Новый тип данных позволяет написать исходный оператор **Declare** правильно:</span><span class="sxs-lookup"><span data-stu-id="d6d89-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="d6d89-171">Этот тип данных и новый атрибут **PtrSafe** позволяют использовать этот оператор **Declare** как в 32-разрядных, так и в 64-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="d6d89-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="d6d89-172">Атрибут **PtrSafe** указывает компилятору VBA, что оператор **Declare** предусмотрен для 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="d6d89-173">При использовании оператора **Declare** в 64-разрядной системе без этого атрибута возникнет ошибка компиляции.</span><span class="sxs-lookup"><span data-stu-id="d6d89-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="d6d89-174">Атрибут **PtrSafe** необязателен в 32-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="d6d89-175">Это позволяет существующим операторам **Declare** работать так, как и обычно.</span><span class="sxs-lookup"><span data-stu-id="d6d89-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="d6d89-176">В приведенной ниже таблице описаны новые квалификатор и тип данных, а также другой тип данных, два оператора преобразования и три функции.</span><span class="sxs-lookup"><span data-stu-id="d6d89-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="d6d89-177">Тип</span><span class="sxs-lookup"><span data-stu-id="d6d89-177">Type</span></span>|<span data-ttu-id="d6d89-178">Item</span><span class="sxs-lookup"><span data-stu-id="d6d89-178">Item</span></span>|<span data-ttu-id="d6d89-179">Описание</span><span class="sxs-lookup"><span data-stu-id="d6d89-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6d89-180">Квалификатор</span><span class="sxs-lookup"><span data-stu-id="d6d89-180">Qualifier</span></span>  <br/> |<span data-ttu-id="d6d89-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="d6d89-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="d6d89-p119">Указывает, что оператор **Declare** совместим с 64-разрядными версиями. Этот атрибут обязателен в 64-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="d6d89-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="d6d89-184">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6d89-184">Data Type</span></span>  <br/> |<span data-ttu-id="d6d89-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="d6d89-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="d6d89-186">Переменный тип данных, равный 4 байтам в 32-разрядных версиях и 8 байтам в 64-разрядных версиях Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="d6d89-187">Это рекомендуемый способ объявления указателя или дескриптора в новом, а также устаревшем коде, который должен работать в 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="d6d89-188">Он поддерживается только в 32- и 64-разрядной среде выполнения VBA 7.</span><span class="sxs-lookup"><span data-stu-id="d6d89-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="d6d89-189">Обратите внимание, что вы можете назначать ему числовые значения, но не числовые типы.</span><span class="sxs-lookup"><span data-stu-id="d6d89-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="d6d89-190">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6d89-190">Data Type</span></span>  <br/> |<span data-ttu-id="d6d89-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="d6d89-191">**LongLong**</span></span> <br/> |<span data-ttu-id="d6d89-192">Это 8-байтовый тип данных, который доступен только в 64-разрядных версиях Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="d6d89-193">Вы можете назначать числовые значения, но не числовые типы (чтобы избежать усечения).</span><span class="sxs-lookup"><span data-stu-id="d6d89-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="d6d89-194">Оператор преобразования</span><span class="sxs-lookup"><span data-stu-id="d6d89-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="d6d89-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="d6d89-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="d6d89-196">Преобразует простое выражение в тип данных **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="d6d89-197">Оператор преобразования</span><span class="sxs-lookup"><span data-stu-id="d6d89-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="d6d89-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="d6d89-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="d6d89-199">Преобразует простое выражение в тип данных **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="d6d89-200">Функция</span><span class="sxs-lookup"><span data-stu-id="d6d89-200">Function</span></span>  <br/> |<span data-ttu-id="d6d89-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="d6d89-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="d6d89-p122">Преобразователь переменной. Возвращает тип данных **LongPtr** в 64-разрядных версиях и тип данных **Long** в 32-разрядных версиях (4 байта).</span><span class="sxs-lookup"><span data-stu-id="d6d89-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="d6d89-204">Функция</span><span class="sxs-lookup"><span data-stu-id="d6d89-204">Function</span></span>  <br/> |<span data-ttu-id="d6d89-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="d6d89-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="d6d89-p123">Преобразователь объекта. Возвращает тип данных **LongPtr** в 64-разрядных версиях и тип данных **Long** в 32-разрядных версиях (4 байта).</span><span class="sxs-lookup"><span data-stu-id="d6d89-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="d6d89-208">Функция</span><span class="sxs-lookup"><span data-stu-id="d6d89-208">Function</span></span>  <br/> |<span data-ttu-id="d6d89-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="d6d89-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="d6d89-p124">Преобразователь строки. Возвращает тип данных **LongPtr** в 64-разрядных версиях и тип данных **Long** в 32-разрядных версиях (4 байта).</span><span class="sxs-lookup"><span data-stu-id="d6d89-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="d6d89-212">В приведенном ниже примере показано, как использовать некоторые из этих элементов в операторе **Declare**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="d6d89-213">Обратите внимание, что операторы **Declare** без атрибута **PtrSafe** не совместимы с 64-разрядной версией Office.</span><span class="sxs-lookup"><span data-stu-id="d6d89-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="d6d89-214">Существует две константы условной компиляции: **VBA7** и **Win64**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="d6d89-215">Чтобы предотвратить использование 64-разрядного кода в более ранней версии Office и тем самым обеспечить обратную совместимость с предыдущими версиями Microsoft Office, используйте константу **VBA7** (наиболее распространенный случай).</span><span class="sxs-lookup"><span data-stu-id="d6d89-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="d6d89-216">Для кода с отличающимися друг от друга 32- и 64-разрядными версиями (например, для вызова математического API, который применяет тип данных **LongLong** в 64-разрядной версии и тип данных **Long** в 32-разрядной версии) используйте константу **Win64**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="d6d89-217">В следующем коде показан пример использования этих двух констант.</span><span class="sxs-lookup"><span data-stu-id="d6d89-217">The following code shows the use of these two constants.</span></span> 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

<span data-ttu-id="d6d89-218">Подводя итог, если вы пишете 64-разрядный код и планируете использовать его в предыдущих версиях Office, рекомендуется использовать константу условной компиляции **VBA7**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="d6d89-219">Но если вы пишете в Office 32-разрядный код, он будет работать так же, как и в предыдущих версиях Office (без использования константы компиляции).</span><span class="sxs-lookup"><span data-stu-id="d6d89-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="d6d89-220">Чтобы гарантировать использование 32-разрядных операторов для 32-разрядных версий и 64-разрядных операторов для 64-разрядных версий, лучше всего применять константу условной компиляции **Win64**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="d6d89-221">Использование атрибутов условной компиляции</span><span class="sxs-lookup"><span data-stu-id="d6d89-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="d6d89-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span></span>

<span data-ttu-id="d6d89-223">В следующем примере показан требующий обновления код на языке VBA, написанный для 32-разрядных версий.</span><span class="sxs-lookup"><span data-stu-id="d6d89-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="d6d89-224">В устаревшем коде обратите внимание на типы данных, которые обновлены для использования \*\* LongPtr \*\*, так как ссылаются на дескрипторы или указатели.</span><span class="sxs-lookup"><span data-stu-id="d6d89-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="d6d89-225">Код на языке VBA, написанный для 32-разрядных версий</span><span class="sxs-lookup"><span data-stu-id="d6d89-225">VBA code written for 32-bit versions</span></span>
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="d6d89-226">Код на языке VBA, написанный для 64-разрядных версий</span><span class="sxs-lookup"><span data-stu-id="d6d89-226">VBA code rewritten for 64-bit versions</span></span>
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<span data-ttu-id="d6d89-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="d6d89-228">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="d6d89-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="d6d89-229">В каком случае мне следует использовать 64-разрядную версию Office?</span><span class="sxs-lookup"><span data-stu-id="d6d89-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="d6d89-230">Это зависит в большей степени от того, какое ведущее приложение (Excel, Word и т. д.) вы используете.</span><span class="sxs-lookup"><span data-stu-id="d6d89-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="d6d89-231">Например, Excel в 64-разрядной версии Microsoft Office может обрабатывать листы большего размера.</span><span class="sxs-lookup"><span data-stu-id="d6d89-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="d6d89-232">Могу ли я установить параллельно 64- и 32-разрядную версии Office?</span><span class="sxs-lookup"><span data-stu-id="d6d89-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="d6d89-233">Нет.</span><span class="sxs-lookup"><span data-stu-id="d6d89-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="d6d89-234">В каком случае необходимо преобразовывать параметры типа Long в тип LongPtr?</span><span class="sxs-lookup"><span data-stu-id="d6d89-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="d6d89-235">Вам необходимо заглянуть в документацию по Windows API на сайте Microsoft Developers Network и найти функцию, которую вы хотите вызвать.</span><span class="sxs-lookup"><span data-stu-id="d6d89-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="d6d89-236">Дескрипторы и указатели должны быть преобразованы в **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="d6d89-237">Например, в документации для функции [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) есть такая сигнатура:</span><span class="sxs-lookup"><span data-stu-id="d6d89-237">As an example, the documentation for [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="d6d89-238">Ниже приведено определение параметров.</span><span class="sxs-lookup"><span data-stu-id="d6d89-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="d6d89-239">Параметр</span><span class="sxs-lookup"><span data-stu-id="d6d89-239">Parameter</span></span>|<span data-ttu-id="d6d89-240">Описание</span><span class="sxs-lookup"><span data-stu-id="d6d89-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6d89-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="d6d89-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="d6d89-242">*Дескриптор* для открытого раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="d6d89-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="d6d89-243">lpSubKey [in, необязательный]</span><span class="sxs-lookup"><span data-stu-id="d6d89-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="d6d89-244">Имя открытого подраздела реестра.</span><span class="sxs-lookup"><span data-stu-id="d6d89-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="d6d89-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="d6d89-245">ulOptions</span></span>  <br/> |<span data-ttu-id="d6d89-246">Этот параметр зарезервирован и должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d6d89-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="d6d89-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="d6d89-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="d6d89-248">Маска, указывающая желаемые права для доступа к разделу.</span><span class="sxs-lookup"><span data-stu-id="d6d89-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="d6d89-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="d6d89-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="d6d89-250">*Указатель* на переменную, которая получает дескриптор для открытого раздела.</span><span class="sxs-lookup"><span data-stu-id="d6d89-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="d6d89-251">В [Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support) оператор **Declare** определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6d89-251">In [Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="d6d89-252">Нужно ли мне преобразовывать указатели и дескрипторы в структурах?</span><span class="sxs-lookup"><span data-stu-id="d6d89-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="d6d89-253">Да.</span><span class="sxs-lookup"><span data-stu-id="d6d89-253">Yes.</span></span> <span data-ttu-id="d6d89-254">См. тип **MSG** в Win32API_PtrSafe.txt:</span><span class="sxs-lookup"><span data-stu-id="d6d89-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="d6d89-255">В каких случая необходимо использовать функции strptr, varpt и objptr?</span><span class="sxs-lookup"><span data-stu-id="d6d89-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="d6d89-256">Эти функции необходимо использовать для извлечения указателей на строки, переменные и объекты соответственно.</span><span class="sxs-lookup"><span data-stu-id="d6d89-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="d6d89-257">В 64-разрядной версии Office эти функции будут возвращать 64-разрядный тип данных **LongPtr**, который может быть передан в операторы **Declare**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="d6d89-258">Использование этих функций осталось таким же, как в предыдущих версиях VBA.</span><span class="sxs-lookup"><span data-stu-id="d6d89-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="d6d89-259">Разница лишь в том, что теперь они возвращают тип данных **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="d6d89-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6d89-260">См. также</span><span class="sxs-lookup"><span data-stu-id="d6d89-260">See also</span></span>
<span data-ttu-id="d6d89-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d89-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span></span>

- <span data-ttu-id="d6d89-262">[Структура оператора Declare](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="d6d89-262">[Anatomy of a Declare Statement](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))</span></span>
