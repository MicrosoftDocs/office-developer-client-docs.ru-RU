---
title: Совместимость 32- и 64-разрядных версий Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Узнайте, как 32-разрядной версии Office совместим с 64-разрядной версии Office.
ms.openlocfilehash: 924f7a1aa891addc5841e6cdefc5226dcb056096
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813067"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="f803c-103">Совместимость 32- и 64-разрядных версий Office</span><span class="sxs-lookup"><span data-stu-id="f803c-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="f803c-104">Узнайте, как 32-разрядной версии Office совместим с 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="f803c-105">Приложения Office доступны в 32-разрядной и 64-разрядных версиях.</span><span class="sxs-lookup"><span data-stu-id="f803c-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="f803c-106">64-разрядных версиях Office позволяют перемещать больше данных для повышения возможности, например, при работе с большим количеством в Microsoft Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="f803c-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="f803c-107">При создании кода 32-разрядная версия, можно использовать 64-разрядной версии Office без изменений.</span><span class="sxs-lookup"><span data-stu-id="f803c-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="f803c-108">Тем не менее, при написании кода 64-разрядная версия, необходимо убедиться, что код содержит определенные ключевые слова и констант условной компиляции, чтобы убедиться, что код входит обратную совместимость с более ранней версии Office, и что правильный код выполняется, если вы Использование 32-разрядных и 64-разрядная версия кода.</span><span class="sxs-lookup"><span data-stu-id="f803c-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="f803c-109">Visual Basic для приложений 7.0 (VBA 7) выпущена в 64-разрядных версиях для Office и работает с 32-разрядной и 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="f803c-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="f803c-110">Изменения, описанные в этой статье применимы только для 64-разрядных версиях Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="f803c-111">Использование 32-разрядных версиях enable Microsoft Office для использования решений созданных в предыдущих версиях Office без дальнейших изменений.</span><span class="sxs-lookup"><span data-stu-id="f803c-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f803c-112">По умолчанию при установке 64-разрядной версии Office, вам также установить 32-разрядная версия устанавливается вместе с 64-разрядной системе.</span><span class="sxs-lookup"><span data-stu-id="f803c-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="f803c-113">Необходимо явно задать параметр установки Microsoft Office 64-разрядные версии.</span><span class="sxs-lookup"><span data-stu-id="f803c-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="f803c-114">В VBA 7 необходимо обновить существующие операторов Windows API (инструкции**Declare** ) для работы с 64-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="f803c-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="f803c-115">Кроме того необходимо обновить указатели адрес и отображение дескрипторы окон в пользовательских типов, которые использует эти инструкции.</span><span class="sxs-lookup"><span data-stu-id="f803c-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="f803c-116">Эта процедура рассматривается более подробно в этой статье также проблемы совместимости между 32-разрядной и 64-разрядных версий и рекомендуемые решения.</span><span class="sxs-lookup"><span data-stu-id="f803c-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="f803c-117">Сравнение 32-разрядной и 64-разрядных систем</span><span class="sxs-lookup"><span data-stu-id="f803c-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="f803c-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-118"></span></span>

<span data-ttu-id="f803c-119">Приложения, созданные с помощью 64-разрядных версиях Office можно ссылаться на большего адресного пространства, чем 32-разрядные версии.</span><span class="sxs-lookup"><span data-stu-id="f803c-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="f803c-120">Это означает, которые можно использовать для данных, чем прежде чем физическую память, потенциально уменьшая нагрузку, затраченное на перенос данных и выходить из нее физической памяти</span><span class="sxs-lookup"><span data-stu-id="f803c-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="f803c-121">В дополнение к ссылке (известную как указатели) определенного расположения в физической памяти, можно также использовать адреса для отображения окна идентификаторы (известную как значками) ссылки.</span><span class="sxs-lookup"><span data-stu-id="f803c-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="f803c-122">Размер (в байтах) указателя или дескриптора зависит от того, используется ли в 32-разрядная или 64-разрядная версия системы.</span><span class="sxs-lookup"><span data-stu-id="f803c-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="f803c-123">Если вы хотите запустить существующих решений с 64-разрядных версий Office, необходимо учитывать следующее:</span><span class="sxs-lookup"><span data-stu-id="f803c-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="f803c-124">Собственные 64-разрядные процессы в Office не удается загрузить 32-разрядных двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="f803c-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="f803c-125">Это должен быть распространенные проблемы при наличии существующих элементов управления Microsoft ActiveX и существующих надстроек.</span><span class="sxs-lookup"><span data-stu-id="f803c-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="f803c-126">VBA ранее не имеют тип данных указатель, поэтому было необходимо использовать 32-разрядная версия переменных для хранения указателей и дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="f803c-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="f803c-127">Теперь эти переменные усекать 64-разрядная версия значения, возвращаемые вызовов API при использовании инструкции **Declare** .</span><span class="sxs-lookup"><span data-stu-id="f803c-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="f803c-128">Базу кода VBA 7</span><span class="sxs-lookup"><span data-stu-id="f803c-128">VBA 7 code base</span></span>
<span data-ttu-id="f803c-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-129"></span></span>

<span data-ttu-id="f803c-130">VBA 7 заменяет кода VBA в Office 2007 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="f803c-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="f803c-131">VBA 7 доступна в 32-разрядной и 64-разрядных версиях Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="f803c-132">Она предоставляет два константы условной компиляции:</span><span class="sxs-lookup"><span data-stu-id="f803c-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="f803c-133">**VBA7** - помогает обеспечить обратной совместимости кода путем тестирования ли ваше приложение использует VBA 7 или предыдущей версии VBA.</span><span class="sxs-lookup"><span data-stu-id="f803c-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="f803c-134">**Win64** Проверяет, является ли код выполняется как 32-разрядная или 64-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="f803c-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="f803c-135">С определенными исключениями макросов в документе, которые работают в 32-разрядная версия приложения также работать в 64-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="f803c-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="f803c-136">Элемент управления ActiveX и надстройки COM и совместимость</span><span class="sxs-lookup"><span data-stu-id="f803c-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="f803c-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-137"></span></span>

<span data-ttu-id="f803c-138">Существующие элементы управления ActiveX 32-разрядная версия, не совместимы с 64-разрядных версиях Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="f803c-139">Для элементов управления ActiveX и COM-объектов:</span><span class="sxs-lookup"><span data-stu-id="f803c-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="f803c-140">Если у вас есть исходный код, создайте 64-разрядная версия самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="f803c-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="f803c-141">Если у вас нет исходного кода, обратитесь к производителю за обновленной версией.</span><span class="sxs-lookup"><span data-stu-id="f803c-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="f803c-142">Собственные 64-разрядные процессы в Office не удается загрузить 32-разрядных двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="f803c-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="f803c-143">Сюда входят общие элементы управления **MSComCtl** (TabStrip, панель инструментов, строка состояния, ProgressBar, TreeView, ListViews, ImageList, ползунок, ImageComboBox) и элементы управления **MSComCt2** (анимации "Счетчик", управления MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="f803c-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="f803c-144">Эти элементы управления были установлены с 32-разрядных версиях Office до Office 2010.</span><span class="sxs-lookup"><span data-stu-id="f803c-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="f803c-145">Вам потребуется найти альтернативы для существующих решений VBA, использующие эти элементы управления при переходе код на 64-разрядных версиях Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="f803c-146">API совместимости</span><span class="sxs-lookup"><span data-stu-id="f803c-146">API compatibility</span></span>
<span data-ttu-id="f803c-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-147"></span></span>

<span data-ttu-id="f803c-148">Сочетание библиотек VBA и тип предоставляет многие функции для создания приложения на базе Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="f803c-149">Тем не менее в некоторых случаях вы должны напрямую связываются с операционной системы и других компонентов, таких как при управлении памяти или процессами, при работе с windows linke элементы пользовательского интерфейса и элементов управления, либо при изменении реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="f803c-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="f803c-150">В следующих ситуациях лучше использовать одну из внешних функций, внедренных в DLL-файлы.</span><span class="sxs-lookup"><span data-stu-id="f803c-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="f803c-151">Для этого в VBA путем вызова API, с помощью инструкции **Declare** .</span><span class="sxs-lookup"><span data-stu-id="f803c-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f803c-152">Корпорация Майкрософт предоставляет Win32API.txt файл, содержащий 1500 инструкции Declare и средства для копирования оператор **Declare** , который будет в коде.</span><span class="sxs-lookup"><span data-stu-id="f803c-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="f803c-153">Тем не менее, эти инструкции для 32-разрядных систем и должен быть преобразован в 64-разрядная версия с помощью сведений, представленных далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="f803c-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="f803c-154">Существующие инструкции **Declare** не компиляции в 64-разрядных версиях VBA, пока они помечены как безопасные для 64-разрядная версия с помощью атрибута **PtrSafe** .</span><span class="sxs-lookup"><span data-stu-id="f803c-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="f803c-155">Примеры этого типа преобразования можно найти на веб-сайте Jan Karel Excel со статусом MVP Pieterse по [http://www.jkp-ads.com/articles/apideclarations.asp](http://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="f803c-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [http://www.jkp-ads.com/articles/apideclarations.asp](http://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="f803c-156">[Руководство пользователя инспектор совместимости кода Office](http://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) полезно для проверки синтаксиса инструкции API **Declare** для атрибута **PtrSafe** при необходимости и соответствующий тип возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f803c-156">The [Office Code Compatibility Inspector user's guide](http://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="f803c-157">Операторы **Declare** похожи на один из следующих действий в зависимости от того, вызывается подпрограмма (без возвращаемого значения) или функция (имеют возвращаемое значение).</span><span class="sxs-lookup"><span data-stu-id="f803c-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="f803c-158">Функция **Дополнительное_имя** или функция **имяФункции** заменяется реальное имя процедуры в DLL-файла и представляет имя, которое используется при вызове процедуры из кода VBA.</span><span class="sxs-lookup"><span data-stu-id="f803c-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="f803c-159">Можно также указать аргумент **AliasName** для имени процедуры.</span><span class="sxs-lookup"><span data-stu-id="f803c-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="f803c-160">Имя DLL-файла, который содержит вызываемой процедуры следует ключевое слово **Lib** .</span><span class="sxs-lookup"><span data-stu-id="f803c-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="f803c-161">И наконец, список аргумент содержит параметры и типы данных, которые нужно передать в процедуру.</span><span class="sxs-lookup"><span data-stu-id="f803c-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="f803c-162">Следующий оператор **Declare** открывает *подраздел* реестра Windows и заменяет его значение.</span><span class="sxs-lookup"><span data-stu-id="f803c-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="f803c-163">Запись Windows.h (дескриптор окна) для функции **RegOpenKeyA** выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f803c-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="f803c-164">В Visual C и Microsoft Visual C++ предыдущий пример компилируется правильно для 32- и 64-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="f803c-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="f803c-165">Это HKEY определяется как указатель, размер которого отражает объем памяти платформы, код компилируется в.</span><span class="sxs-lookup"><span data-stu-id="f803c-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="f803c-166">В предыдущих версиях VBA возникла тип данных не определенный указатель, поэтому использовать тип данных **Long** .</span><span class="sxs-lookup"><span data-stu-id="f803c-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="f803c-167">И так как тип данных **Long** всегда используется 32-разрядной, этот разрывов при использовании в системе с 64-разрядных, так как верхнем 32 разряда может усекаться или перезаписать другие адреса памяти.</span><span class="sxs-lookup"><span data-stu-id="f803c-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="f803c-168">Любой из этих ситуаций можно привести непредсказуемое поведение и сбоям системы.</span><span class="sxs-lookup"><span data-stu-id="f803c-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="f803c-169">Чтобы решить эту проблему, VBA включает в себя тип данных true *указатель* : **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="f803c-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="f803c-170">Этот новый тип данных позволяет создавать исходный оператор **Declare** правильно как:</span><span class="sxs-lookup"><span data-stu-id="f803c-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="f803c-171">Этот тип данных и новый атрибут **PtrSafe** позволяют использовать этот оператор **Declare** в 32-разрядная или 64-разрядных системах.</span><span class="sxs-lookup"><span data-stu-id="f803c-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="f803c-172">Атрибут **PtrSafe** указывает компилятора VBA, что оператор **Declare** предназначен для 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="f803c-173">Если этот атрибут не с помощью оператора **Declare** в системе с 64-разрядная версия приведет к ошибке компиляции.</span><span class="sxs-lookup"><span data-stu-id="f803c-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="f803c-174">Атрибут **PtrSafe** является необязательным на 32-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="f803c-175">Это позволяет работать, как у существующего выражения **Declare** .</span><span class="sxs-lookup"><span data-stu-id="f803c-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="f803c-176">В следующей таблице представлены дополнительные сведения о новых квалификатор и typeas данных, а также другой тип данных, два операторы преобразования и три функции.</span><span class="sxs-lookup"><span data-stu-id="f803c-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="f803c-177">Тип</span><span class="sxs-lookup"><span data-stu-id="f803c-177">Type</span></span>|<span data-ttu-id="f803c-178">Элемент</span><span class="sxs-lookup"><span data-stu-id="f803c-178">Item</span></span>|<span data-ttu-id="f803c-179">Описание</span><span class="sxs-lookup"><span data-stu-id="f803c-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f803c-180">Квалификатор</span><span class="sxs-lookup"><span data-stu-id="f803c-180">Qualifier</span></span>  <br/> |<span data-ttu-id="f803c-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="f803c-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="f803c-p119">Обозначает, что оператор **Declare** совместим с 64-разрядными системами. Этот атрибут обязателен для 64-разрядных систем.</span><span class="sxs-lookup"><span data-stu-id="f803c-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="f803c-184">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f803c-184">Data Type</span></span>  <br/> |<span data-ttu-id="f803c-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="f803c-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="f803c-186">Тип данных переменной, которой имеет тип данных 4 байта в 32-разрядных версий и типа данных 8 байтов в 64-разрядных версиях системы Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="f803c-187">Это рекомендуемый способ объявления указатель или дескриптор для нового кода, но также для кода прежних версий, если оно должно работать в 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="f803c-188">Это только поддерживаемые в среде выполнения VBA 7 в 32-разрядной и 64-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="f803c-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="f803c-189">Обратите внимание на то, что можно назначить числовых значений его, но не числовые типы.</span><span class="sxs-lookup"><span data-stu-id="f803c-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="f803c-190">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f803c-190">Data Type</span></span>  <br/> |<span data-ttu-id="f803c-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="f803c-191">**LongLong**</span></span> <br/> |<span data-ttu-id="f803c-192">Это относится к типу данных 8 байтов, которое доступно только в 64-разрядных версиях системы Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="f803c-193">Можно назначить числовые значения, но не числовые типы (во избежание усечения).</span><span class="sxs-lookup"><span data-stu-id="f803c-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="f803c-194">Оператор преобразования</span><span class="sxs-lookup"><span data-stu-id="f803c-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="f803c-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="f803c-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="f803c-196">Преобразует простое выражение в тип данных **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="f803c-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="f803c-197">Оператор преобразования</span><span class="sxs-lookup"><span data-stu-id="f803c-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="f803c-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="f803c-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="f803c-199">Преобразует простое выражение в тип данных **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="f803c-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="f803c-200">Функция</span><span class="sxs-lookup"><span data-stu-id="f803c-200">Function</span></span>  <br/> |<span data-ttu-id="f803c-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="f803c-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="f803c-p122">Преобразователь вариантов. Возвращает тип **LongPtr** для 64-разрядных версий и тип **Long** для 32-разрядных версий (4 байта).</span><span class="sxs-lookup"><span data-stu-id="f803c-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="f803c-204">Функция</span><span class="sxs-lookup"><span data-stu-id="f803c-204">Function</span></span>  <br/> |<span data-ttu-id="f803c-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="f803c-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="f803c-p123">Преобразователь объектов. Возвращает тип **LongPtr** для 64-разрядных версий и тип **Long** для 32-разрядных версий (4 байта).</span><span class="sxs-lookup"><span data-stu-id="f803c-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="f803c-208">Функция</span><span class="sxs-lookup"><span data-stu-id="f803c-208">Function</span></span>  <br/> |<span data-ttu-id="f803c-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="f803c-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="f803c-p124">Преобразователь строк. Возвращает тип **LongPtr** для 64-разрядных версий и тип **Long** для 32-разрядных версий (4 байта).</span><span class="sxs-lookup"><span data-stu-id="f803c-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="f803c-212">В следующем примере показано, как использовать эти элементы в операторе **Declare**.</span><span class="sxs-lookup"><span data-stu-id="f803c-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="f803c-213">Обратите внимание, что операторы **Declare** без атрибута **PtrSafe** предполагается, что не совместимы с 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="f803c-214">Существует две константы условной компиляции: **VBA7** и **Win64**.</span><span class="sxs-lookup"><span data-stu-id="f803c-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="f803c-215">Для обеспечения обратной совместимости с предыдущими версиями Microsoft Office, используйте константу **VBA7** (это обычно case) для предотвращения использования в более ранней версии Office 64-разрядного кода.</span><span class="sxs-lookup"><span data-stu-id="f803c-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="f803c-216">Для кода, который различие между 32-разрядная и 64-разрядная версия, такие как вызова math API, которое использует **LongLong** для 64-разрядной версии и **времени** для его 32-разрядная версия используйте константу **Win64** .</span><span class="sxs-lookup"><span data-stu-id="f803c-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="f803c-217">Приведенный ниже код показывает использование этих двух констант.</span><span class="sxs-lookup"><span data-stu-id="f803c-217">The following code shows the use of these two constants.</span></span> 
  
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

<span data-ttu-id="f803c-218">В целом, если писать код 64-разрядная версия и планируется использовать его в предыдущих версиях Office, необходимо использовать **VBA7** константа условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="f803c-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="f803c-219">Тем не менее при написании кода 32-разрядная версия пакета Office этот код работает как в предыдущих версиях Office без необходимости константы компиляции.</span><span class="sxs-lookup"><span data-stu-id="f803c-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="f803c-220">Если вы хотите убедиться, что используется 32-разрядная версия операторов для 32-разрядных версий и 64-разрядная версия операторов для 64-разрядных версий, лучше использовать константа условной компиляции **Win64** .</span><span class="sxs-lookup"><span data-stu-id="f803c-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="f803c-221">Использование атрибутов условной компиляции</span><span class="sxs-lookup"><span data-stu-id="f803c-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="f803c-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-222"></span></span>

<span data-ttu-id="f803c-223">Пример кода VBA, написанные для 32-разрядная версия, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="f803c-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="f803c-224">Обратите внимание на то типы данных в прежних версий кода, которые обновляются для использования **LongPtr** , так как они ссылаются на обработчика или указателя.</span><span class="sxs-lookup"><span data-stu-id="f803c-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="f803c-225">Код VBA, написанные для 32-разрядные версии</span><span class="sxs-lookup"><span data-stu-id="f803c-225">VBA code written for 32-bit versions</span></span>
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="f803c-226">Код VBA, переопределяются для 64-разрядных версий</span><span class="sxs-lookup"><span data-stu-id="f803c-226">VBA code rewritten for 64-bit versions</span></span>
  
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

<span data-ttu-id="f803c-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f803c-228">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="f803c-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="f803c-229">Когда следует использовать 64-разрядной версии Office?</span><span class="sxs-lookup"><span data-stu-id="f803c-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="f803c-230">Эта функция больше используется независимо от того, какие приложения узла (Excel, Word и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f803c-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="f803c-231">Например Excel будет обрабатывать намного более листов с 64-разрядная версия Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f803c-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="f803c-232">Как установить 32-разрядной и 64-разрядных версий Office одновременно?</span><span class="sxs-lookup"><span data-stu-id="f803c-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="f803c-233">Нет.</span><span class="sxs-lookup"><span data-stu-id="f803c-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="f803c-234">Когда следует преобразовать длинные параметры в LongPtr</span><span class="sxs-lookup"><span data-stu-id="f803c-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="f803c-235">Следует проверить документация по Windows API в сети разработчиков Microsoft функции, которую нужно позвонить.</span><span class="sxs-lookup"><span data-stu-id="f803c-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="f803c-236">Маркеры и указатели нужно преобразовать в **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="f803c-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="f803c-237">Например документации по [RegOpenKeyA](http://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) предоставляет следующую подпись:</span><span class="sxs-lookup"><span data-stu-id="f803c-237">As an example, the documentation for [RegOpenKeyA](http://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="f803c-238">Параметры имеют следующее значение.</span><span class="sxs-lookup"><span data-stu-id="f803c-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="f803c-239">Параметр</span><span class="sxs-lookup"><span data-stu-id="f803c-239">Parameter</span></span>|<span data-ttu-id="f803c-240">Описание</span><span class="sxs-lookup"><span data-stu-id="f803c-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f803c-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="f803c-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="f803c-242">*Обработка* открыть раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="f803c-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="f803c-243">lpSubKey [в, необязательно]</span><span class="sxs-lookup"><span data-stu-id="f803c-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="f803c-244">Имя подраздела реестра, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="f803c-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="f803c-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="f803c-245">ulOptions</span></span>  <br/> |<span data-ttu-id="f803c-246">Этот параметр зарезервирован и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f803c-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="f803c-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="f803c-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="f803c-248">Маска, указывающая требуемые права доступа к ключу.</span><span class="sxs-lookup"><span data-stu-id="f803c-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="f803c-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="f803c-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="f803c-250">*Указатель* на переменную, которая получает маркер открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="f803c-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="f803c-251">В [Win32API_PtrSafe.txt](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b)оператор **Declare** определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f803c-251">In [Win32API_PtrSafe.txt](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="f803c-252">Преобразование указателей и дескрипторов в структуры?</span><span class="sxs-lookup"><span data-stu-id="f803c-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="f803c-253">Да.</span><span class="sxs-lookup"><span data-stu-id="f803c-253">Yes.</span></span> <span data-ttu-id="f803c-254">Просмотрите тип **сообщений** в Win32API_PtrSafe.txt:</span><span class="sxs-lookup"><span data-stu-id="f803c-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="f803c-255">Когда следует использовать strptr, varpt и objptr?</span><span class="sxs-lookup"><span data-stu-id="f803c-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="f803c-256">Эти функции следует использовать для получения указатели строк, переменных и объектов, соответственно.</span><span class="sxs-lookup"><span data-stu-id="f803c-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="f803c-257">64-разрядной версии Office эти функции возвращают в 64-разрядная версия **LongPtr**, который может быть передан инструкции **Declare** .</span><span class="sxs-lookup"><span data-stu-id="f803c-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="f803c-258">Использование этих функций не был изменен в предыдущих версиях VBA.</span><span class="sxs-lookup"><span data-stu-id="f803c-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="f803c-259">Единственное отличие — это теперь возвращают **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="f803c-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f803c-260">См. также</span><span class="sxs-lookup"><span data-stu-id="f803c-260">See also</span></span>
<span data-ttu-id="f803c-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="f803c-261"></span></span>

- [<span data-ttu-id="f803c-262">Анатомия оператор Declare</span><span class="sxs-lookup"><span data-stu-id="f803c-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/en-us/library/office/aa671659.aspx)
    

