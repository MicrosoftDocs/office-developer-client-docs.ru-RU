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
# <a name="mapiinitialize"></a><span data-ttu-id="155ec-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="155ec-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="155ec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="155ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="155ec-105">Добавит количество ссылок подсистем MAPI и инициализирует глобальные данные для DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="155ec-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="155ec-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="155ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="155ec-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="155ec-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="155ec-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="155ec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="155ec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="155ec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="155ec-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="155ec-110">Called by:</span></span>  <br/> |<span data-ttu-id="155ec-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="155ec-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="155ec-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="155ec-112">Parameters</span></span>

 <span data-ttu-id="155ec-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="155ec-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="155ec-114">[in] Указатель на [MAPIINIT_0](mapiinit_0.md) структуру.</span><span class="sxs-lookup"><span data-stu-id="155ec-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="155ec-115">Для  _параметра lpMapiInit_ можно установить NULL.</span><span class="sxs-lookup"><span data-stu-id="155ec-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="155ec-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="155ec-116">Return value</span></span>

<span data-ttu-id="155ec-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="155ec-117">S_OK</span></span> 
  
> <span data-ttu-id="155ec-118">Подсистема MAPI успешно инициализирована.</span><span class="sxs-lookup"><span data-stu-id="155ec-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="155ec-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="155ec-119">Remarks</span></span>

<span data-ttu-id="155ec-120">Функция **MAPIInitialize** добавит количество ссылок MAPI для подсистемы MAPI, а функция [MAPIUninitialize](mapiuninitialize.md) понижит внутреннее количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="155ec-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="155ec-121">Таким образом, число вызовов одной функции должно быть равно числу вызовов другой.</span><span class="sxs-lookup"><span data-stu-id="155ec-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="155ec-122">**MAPIInitialize** возвращает S_OK, если MAPI не был ранее инициализирован.</span><span class="sxs-lookup"><span data-stu-id="155ec-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="155ec-123">Клиент или поставщик услуг должен вызвать **MAPIInitialize** перед любым другим вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="155ec-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="155ec-124">Если этого не сделать, вызовы клиента или поставщика услуг возвращают MAPI_E_NOT_INITIALIZED значение.</span><span class="sxs-lookup"><span data-stu-id="155ec-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="155ec-125">При вызове **MAPIInitialize** из многоуровневого приложения установите для параметра [](mapiinit_0.md) _lpMapiInit_ MAPIINIT_0 структуру, которая объявлена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="155ec-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="155ec-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="155ec-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="155ec-127">и вызовите:</span><span class="sxs-lookup"><span data-stu-id="155ec-127">and call:</span></span> 
  
 <span data-ttu-id="155ec-128">**MAPIInitialize** ( &amp; MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="155ec-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="155ec-129">Когда эта структура объявлена, MAPI создает отдельный поток для обработки окна уведомлений, который продолжается до тех пор, пока количество ссылок инициализации не упадет до нуля.</span><span class="sxs-lookup"><span data-stu-id="155ec-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="155ec-130">Служба Windows должна установить для члена **ulflags** MAPIINIT_0, на который указывает _lpMapiInit,_ MAPI_NT_SERVICE. </span><span class="sxs-lookup"><span data-stu-id="155ec-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="155ec-131">Невозможно вызвать **MAPIInitialize** или **MAPIUninitialize** из функции **Win32 DllMain** или любой другой функции, которая создает или завершает потоки.</span><span class="sxs-lookup"><span data-stu-id="155ec-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="155ec-132">Дополнительные сведения см. в [Thread-Safe".](using-thread-safe-objects.md)</span><span class="sxs-lookup"><span data-stu-id="155ec-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="155ec-133">**MAPIInitialize** не возвращает расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="155ec-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="155ec-134">В отличие от большинства других вызовов MAPI значения возвращаемого значения строго определяются в соответствии с конкретным этапом инициализации, который не удалось инициализации:</span><span class="sxs-lookup"><span data-stu-id="155ec-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="155ec-135">Проверяет параметры и флаги.</span><span class="sxs-lookup"><span data-stu-id="155ec-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="155ec-136">MAPI_E_INVALID_PARAMETER или MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="155ec-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="155ec-137">Звоняке передан недопустимый параметр или флаг.</span><span class="sxs-lookup"><span data-stu-id="155ec-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="155ec-138">Инициализирует ключи реестра, необходимые mapI, и подтверждает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="155ec-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="155ec-139">Этот шаг происходит только в том случае, если клиентский процесс работает как служба в Windows и устанавливает флаг MAPI_NT service в **MAPIINIT_0** структуре.</span><span class="sxs-lookup"><span data-stu-id="155ec-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="155ec-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="155ec-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="155ec-141">Процесс вызова — это служба Windows, и не удалось инициализировать ключи реестра, необходимые MAPI.</span><span class="sxs-lookup"><span data-stu-id="155ec-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="155ec-142">Дополнительные сведения могут быть доступны в журнале событий приложения.</span><span class="sxs-lookup"><span data-stu-id="155ec-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="155ec-143">Проверьте совместимость MAPI с OLE, а затем инициализируют OLE.</span><span class="sxs-lookup"><span data-stu-id="155ec-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="155ec-144">Проверяет совместимость между текущими версиями OLE и MAPI.</span><span class="sxs-lookup"><span data-stu-id="155ec-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="155ec-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="155ec-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="155ec-146">Версия OLE, установленная на рабочей станции, несовместима с этой версией MAPI.</span><span class="sxs-lookup"><span data-stu-id="155ec-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="155ec-147">Инициализирует OLE.</span><span class="sxs-lookup"><span data-stu-id="155ec-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="155ec-148">Только на этом этапе эта функция может возвращать код ошибки, не указанный здесь.</span><span class="sxs-lookup"><span data-stu-id="155ec-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="155ec-149">Любая _ошибка, не_ указанная в этом списке, должна происходить из функции OLE **CoInitialize.**</span><span class="sxs-lookup"><span data-stu-id="155ec-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="155ec-150">Инициализирует глобальные переменные для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="155ec-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="155ec-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="155ec-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="155ec-152">MAPI настраивает контекст, специфический для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="155ec-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="155ec-153">Сбои могут возникать в Win16, если число процессов превышает определенное число, или в любой системе, если объем доступной памяти исчерпан.</span><span class="sxs-lookup"><span data-stu-id="155ec-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="155ec-154">Инициализирует общие глобальные переменные всех процессов.</span><span class="sxs-lookup"><span data-stu-id="155ec-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="155ec-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="155ec-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="155ec-156">Недостаточно системных ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="155ec-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="155ec-157">Инициализирует обдвижку уведомлений, создает его окно и его поток, если его запрашивает флаг MAPI_MULTITHREAD_NOTIFICATIONS уведомления.</span><span class="sxs-lookup"><span data-stu-id="155ec-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="155ec-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="155ec-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="155ec-159">Может привести к сбойу, если системные ресурсы исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="155ec-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="155ec-160">Загружает и инициализирует поставщика профилей.</span><span class="sxs-lookup"><span data-stu-id="155ec-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="155ec-161">Проверяет, может **ли MAPIInitialize** получить доступ к ключу реестра, в котором хранятся данные профиля.</span><span class="sxs-lookup"><span data-stu-id="155ec-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="155ec-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="155ec-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="155ec-163">Поставщик профилей столкнулся с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="155ec-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="155ec-164">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="155ec-164">MFCMAPI reference</span></span>

<span data-ttu-id="155ec-165">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="155ec-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="155ec-166">**Файл**</span><span class="sxs-lookup"><span data-stu-id="155ec-166">**File**</span></span>|<span data-ttu-id="155ec-167">**Функция**</span><span class="sxs-lookup"><span data-stu-id="155ec-167">**Function**</span></span>|<span data-ttu-id="155ec-168">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="155ec-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="155ec-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="155ec-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="155ec-170">MFCMAPI использует метод **MAPIInitialize** для инициализации MAPI в фоновом потоке для обработки таблиц.</span><span class="sxs-lookup"><span data-stu-id="155ec-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="155ec-171">См. также</span><span class="sxs-lookup"><span data-stu-id="155ec-171">See also</span></span>



[<span data-ttu-id="155ec-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="155ec-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

