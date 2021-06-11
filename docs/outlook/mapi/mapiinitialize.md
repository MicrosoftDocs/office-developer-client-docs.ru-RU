---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411178"
---
# <a name="mapiinitialize"></a><span data-ttu-id="7e300-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="7e300-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="7e300-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e300-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e300-105">Прибавка к эталону подсистемы MAPI и инициализация глобальных данных для DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e300-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e300-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7e300-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e300-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="7e300-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="7e300-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7e300-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e300-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7e300-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7e300-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7e300-110">Called by:</span></span>  <br/> |<span data-ttu-id="7e300-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="7e300-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="7e300-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="7e300-112">Parameters</span></span>

 <span data-ttu-id="7e300-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="7e300-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="7e300-114">[in] Указатель на [MAPIINIT_0](mapiinit_0.md) структуру.</span><span class="sxs-lookup"><span data-stu-id="7e300-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="7e300-115">Параметр  _lpMapiInit_ можно установить в NULL.</span><span class="sxs-lookup"><span data-stu-id="7e300-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7e300-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e300-116">Return value</span></span>

<span data-ttu-id="7e300-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e300-117">S_OK</span></span> 
  
> <span data-ttu-id="7e300-118">Подсистема MAPI была успешно инициализирована.</span><span class="sxs-lookup"><span data-stu-id="7e300-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e300-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e300-119">Remarks</span></span>

<span data-ttu-id="7e300-120">Функция **MAPIInitialize** приумножит количество ссылок MAPI для подсистемы MAPI, а функция [MAPIUninitialize](mapiuninitialize.md) отнимет внутреннее количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="7e300-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="7e300-121">Таким образом, количество вызовов одной функции должно равняться количеству вызовов другой.</span><span class="sxs-lookup"><span data-stu-id="7e300-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="7e300-122">**MAPIInitialize** возвращает S_OK, если MAPI не была ранее инициализирована.</span><span class="sxs-lookup"><span data-stu-id="7e300-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="7e300-123">Перед другим вызовом MAPI клиент или поставщик услуг должен вызвать **MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="7e300-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="7e300-124">Если этого не сделать, клиент или поставщик услуг вызовы возвращают MAPI_E_NOT_INITIALIZED значение.</span><span class="sxs-lookup"><span data-stu-id="7e300-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="7e300-125">При вызове **MAPIInitialize** из многоуровневого приложения установите параметр _lpMapiInit_ в структуру MAPIINIT_0, которая объявляется следующим образом: [](mapiinit_0.md)</span><span class="sxs-lookup"><span data-stu-id="7e300-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="7e300-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="7e300-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="7e300-127">и вызов:</span><span class="sxs-lookup"><span data-stu-id="7e300-127">and call:</span></span> 
  
 <span data-ttu-id="7e300-128">**MAPIInitialize** &amp; (MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="7e300-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="7e300-129">Когда эта структура объявляется, MAPI создает отдельный поток для обработки окна уведомлений, который продолжается до тех пор, пока инициализация отсчета ссылок не опускается до нуля.</span><span class="sxs-lookup"><span data-stu-id="7e300-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="7e300-130">Служба Windows должна задать **члену ulflags** структуры MAPIINIT_0, на который указывает _lpMapiInit,_ MAPI_NT_SERVICE. </span><span class="sxs-lookup"><span data-stu-id="7e300-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7e300-131">Вы не можете вызвать **MAPIInitialize** или **MAPIUninitialize** из функции **Win32 DllMain** или любой другой функции, которая создает или прекращает потоки.</span><span class="sxs-lookup"><span data-stu-id="7e300-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="7e300-132">Дополнительные сведения см. в [Thread-Safe".](using-thread-safe-objects.md)</span><span class="sxs-lookup"><span data-stu-id="7e300-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="7e300-133">**MAPIInitialize** не возвращает расширенные сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7e300-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="7e300-134">В отличие от большинства других вызовов MAPI значения возвращаемого значения строго определяются в соответствии с определенным этапом неудачной инициализации:</span><span class="sxs-lookup"><span data-stu-id="7e300-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="7e300-135">Проверяет параметры и флаги.</span><span class="sxs-lookup"><span data-stu-id="7e300-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="7e300-136">MAPI_E_INVALID_PARAMETER или MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="7e300-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="7e300-137">Вызываемая передала недействительный параметр или флаг.</span><span class="sxs-lookup"><span data-stu-id="7e300-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="7e300-138">Инициализирует ключи реестра, необходимые MAPI, и подтверждает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7e300-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="7e300-139">Этот шаг происходит только в том случае, если клиентский процесс запущен в качестве службы Windows и задает флаг службы MAPI_NT службы в **структуре** MAPIINIT_0.</span><span class="sxs-lookup"><span data-stu-id="7e300-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="7e300-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="7e300-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="7e300-141">Процесс вызова — это Windows и не может быть инициализирована служба и ключи реестра, необходимые MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e300-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="7e300-142">Дополнительные сведения могут быть доступны в журнале событий приложения.</span><span class="sxs-lookup"><span data-stu-id="7e300-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="7e300-143">Проверьте совместимость MAPI с OLE, а затем инициализировать OLE.</span><span class="sxs-lookup"><span data-stu-id="7e300-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="7e300-144">Проверка совместимости между текущими версиями OLE и MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e300-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="7e300-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="7e300-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="7e300-146">Версия OLE, установленная на рабочей станции, не совместима с этой версией MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e300-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="7e300-147">Инициализирует OLE.</span><span class="sxs-lookup"><span data-stu-id="7e300-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="7e300-148">Только на этом этапе эта функция может возвращать код ошибки, не указанный здесь.</span><span class="sxs-lookup"><span data-stu-id="7e300-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="7e300-149">Любая  _ошибка,_ не указанная здесь, должна быть допущена из функции **CoInitialize** OLE.</span><span class="sxs-lookup"><span data-stu-id="7e300-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="7e300-150">Инициализирует глобальные переменные для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="7e300-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="7e300-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="7e300-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="7e300-152">MAPI настраивает контекст, специфический для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="7e300-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="7e300-153">В Win16 могут возникать сбои, если количество процессов превышает определенное число, или в любой системе, если доступная память исчерпана.</span><span class="sxs-lookup"><span data-stu-id="7e300-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="7e300-154">Инициализирует общие глобальные переменные всех процессов.</span><span class="sxs-lookup"><span data-stu-id="7e300-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="7e300-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="7e300-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="7e300-156">Для завершения операции было недостаточно ресурсов системы.</span><span class="sxs-lookup"><span data-stu-id="7e300-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="7e300-157">Инициализирует движок уведомлений, создает его окно и его поток по запросу MAPI_MULTITHREAD_NOTIFICATIONS флага.</span><span class="sxs-lookup"><span data-stu-id="7e300-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="7e300-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="7e300-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="7e300-159">Может привести к сбой, если ресурсы системы исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="7e300-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="7e300-160">Загружает и инициализирует поставщика профилей.</span><span class="sxs-lookup"><span data-stu-id="7e300-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="7e300-161">Проверяет, что **MAPIInitialize** может получить доступ к ключу реестра, в котором хранятся данные профиля.</span><span class="sxs-lookup"><span data-stu-id="7e300-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="7e300-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="7e300-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="7e300-163">Поставщик профилей столкнулся с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7e300-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7e300-164">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7e300-164">MFCMAPI reference</span></span>

<span data-ttu-id="7e300-165">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7e300-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7e300-166">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7e300-166">**File**</span></span>|<span data-ttu-id="7e300-167">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7e300-167">**Function**</span></span>|<span data-ttu-id="7e300-168">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7e300-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7e300-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="7e300-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="7e300-170">MFCMAPI использует **метод MAPIInitialize** для инициализации MAPI на фоновом потоке для обработки таблиц.</span><span class="sxs-lookup"><span data-stu-id="7e300-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e300-171">См. также</span><span class="sxs-lookup"><span data-stu-id="7e300-171">See also</span></span>



[<span data-ttu-id="7e300-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7e300-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

