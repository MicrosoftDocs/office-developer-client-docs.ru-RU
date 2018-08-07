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
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809890"
---
# <a name="mapiinitialize"></a><span data-ttu-id="4e4b5-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="4e4b5-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="4e4b5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e4b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e4b5-105">Увеличивает счетчик ссылок подсистемы MAPI и инициализирует глобальных данных для библиотеки DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e4b5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4e4b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e4b5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="4e4b5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="4e4b5-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="4e4b5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4e4b5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4e4b5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4e4b5-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="4e4b5-110">Called by:</span></span>  <br/> |<span data-ttu-id="4e4b5-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="4e4b5-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="4e4b5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e4b5-112">Parameters</span></span>

 <span data-ttu-id="4e4b5-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="4e4b5-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="4e4b5-114">[in] Указатель на структуру [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4b5-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="4e4b5-115">Параметр _lpMapiInit_ может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e4b5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="4e4b5-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4e4b5-117">S_OK</span></span> 
  
> <span data-ttu-id="4e4b5-118">Подсистема MAPI инициализирован успешно.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e4b5-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e4b5-119">Remarks</span></span>

<span data-ttu-id="4e4b5-120">Увеличивает функции **MAPIInitialize** , счетчик ссылок MAPI для подсистемы MAPI и уменьшает функция [MAPIUninitialize](mapiuninitialize.md) счетчик внутренних ссылок.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="4e4b5-121">Таким образом количество вызовов на одной функции должно совпадать с количеством вызовов в другой.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="4e4b5-122">**MAPIInitialize** возвращает значение S_OK, если ранее не был инициализирован MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="4e4b5-123">Клиент или служба поставщика необходимо вызвать **MAPIInitialize** перед внесением другой вызов MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="4e4b5-124">В противном случае вызывает клиента или поставщика вызовы для возврата значения MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="4e4b5-125">При вызове **MAPIInitialize** из многопоточного приложения, установите для параметра _lpMapiInit_ значение структура [MAPIINIT_0](mapiinit_0.md) , объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e4b5-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="4e4b5-126">**MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="4e4b5-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="4e4b5-127">и звонка:</span><span class="sxs-lookup"><span data-stu-id="4e4b5-127">and call:</span></span> 
  
 <span data-ttu-id="4e4b5-128">**MAPIInitialize** (&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="4e4b5-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="4e4b5-129">При объявлении эту структуру MAPI создает отдельный поток обработки окно уведомления, которое продолжается, пока число ссылок initialize становится равным нулю.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="4e4b5-130">Службы Windows необходимо задать член **ulflags** структуры **MAPIINIT_0** , на который указывает _lpMapiInit_ для MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e4b5-131">В функции Win32 **DllMain** или любых других функций, который создает или завершение работы потоков не может вызывать **MAPIInitialize** или **MAPIUninitialize** из.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="4e4b5-132">Дополнительные сведения можно [С помощью объектов являющихся потокобезопасными](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b5-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="4e4b5-133">**MAPIInitialize** не возвращает все расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="4e4b5-134">В отличие от большинства вызовов MAPI значения его возвращаемые значения строго определяются в соответствии с конкретной шаг инициализации, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="4e4b5-135">Проверяет, параметры и флаги.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="4e4b5-136">MAPI_E_INVALID_PARAMETER или MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="4e4b5-137">Вызывающий объект передан недопустимый параметр или флаг.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="4e4b5-138">Инициализирует разделы реестра, необходимые для MAPI и подтверждает типа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="4e4b5-139">Это действие происходит только в том случае, если процесс клиента выполняется как служба под управлением Windows и устанавливает для флага службы MAPI_NT в структуре **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="4e4b5-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="4e4b5-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="4e4b5-141">Процесс вызова — это служба Windows и разделы реестра, необходимые для MAPI не удалось инициализировать.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="4e4b5-142">Дополнительные сведения можно получить в журнале событий приложений.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="4e4b5-143">Проверка совместимости MAPI с OLE, а затем инициализировать OLE.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="4e4b5-144">Проверяет совместимость текущей версии OLE и MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="4e4b5-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="4e4b5-146">Версия OLE, установленная на рабочей станции несовместима с этой версией MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="4e4b5-147">Инициализирует OLE.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="4e4b5-148">Во время только этот шаг эта функция может возвращать код ошибки, не перечисленных здесь.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="4e4b5-149">Любая ошибка _отсутствует_ в списке здесь должно быть предполагается, что поступают из функции OLE **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="4e4b5-150">Инициализирует каждого процесса глобальных переменных.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="4e4b5-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="4e4b5-152">MAPI устанавливает контекст для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="4e4b5-153">Ошибки Win16 превышения определенного числа процессов, либо на любой системе если исчерпано доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="4e4b5-154">Инициализирует общих глобальных переменных всеми процессами.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="4e4b5-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="4e4b5-156">Не хватает системных ресурсов, не были доступны для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="4e4b5-157">Инициализирует обработчик уведомлений, создает его окно и его потока по запросу флаг MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="4e4b5-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="4e4b5-159">Может отсутствовать, если исчерпано системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="4e4b5-160">Загружает и инициализирует поставщика профиля.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="4e4b5-161">Проверяет, что **MAPIInitialize** можно получить доступ к разделу реестра, где хранятся данные профиля.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="4e4b5-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="4e4b5-163">Поставщик профиля произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="4e4b5-164">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="4e4b5-164">MFCMAPI reference</span></span>

<span data-ttu-id="4e4b5-165">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4e4b5-166">**����**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-166">**File**</span></span>|<span data-ttu-id="4e4b5-167">**�������**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-167">**Function**</span></span>|<span data-ttu-id="4e4b5-168">**�����������**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e4b5-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="4e4b5-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="4e4b5-170">Mfcmapi (en) использует метод **MAPIInitialize** для инициализации MAPI в фоновом потоке обработки некоторые таблицы.</span><span class="sxs-lookup"><span data-stu-id="4e4b5-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e4b5-171">См. также</span><span class="sxs-lookup"><span data-stu-id="4e4b5-171">See also</span></span>



[<span data-ttu-id="4e4b5-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="4e4b5-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

