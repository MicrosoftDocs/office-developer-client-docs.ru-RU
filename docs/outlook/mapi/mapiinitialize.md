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
# <a name="mapiinitialize"></a><span data-ttu-id="98e1a-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="98e1a-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="98e1a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98e1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98e1a-105">Увеличивает значение счетчика ссылок подсистемы MAPI и инициализирует глобальные данные для библиотеки MAPI.</span><span class="sxs-lookup"><span data-stu-id="98e1a-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98e1a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="98e1a-106">Header file:</span></span>  <br/> |<span data-ttu-id="98e1a-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="98e1a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="98e1a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="98e1a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98e1a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98e1a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98e1a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="98e1a-110">Called by:</span></span>  <br/> |<span data-ttu-id="98e1a-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="98e1a-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="98e1a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="98e1a-112">Parameters</span></span>

 <span data-ttu-id="98e1a-113">_Лпмапиинит_</span><span class="sxs-lookup"><span data-stu-id="98e1a-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="98e1a-114">возврата Указатель на структуру [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="98e1a-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="98e1a-115">Параметру _лпмапиинит_ можно приСВОИТЬ значение null.</span><span class="sxs-lookup"><span data-stu-id="98e1a-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98e1a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98e1a-116">Return value</span></span>

<span data-ttu-id="98e1a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="98e1a-117">S_OK</span></span> 
  
> <span data-ttu-id="98e1a-118">Подсистема MAPI инициализирована успешно.</span><span class="sxs-lookup"><span data-stu-id="98e1a-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98e1a-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="98e1a-119">Remarks</span></span>

<span data-ttu-id="98e1a-120">Функция **мапиинитиализе** увеличивает счетчик ссылок MAPI для подсистемы MAPI, а функция [мапиунинитиализе](mapiuninitialize.md) уменьшает внутренний счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="98e1a-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="98e1a-121">Таким образом, число вызовов одной функции должно равняться числу вызовов другой.</span><span class="sxs-lookup"><span data-stu-id="98e1a-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="98e1a-122">**Мапиинитиализе** ВОЗВРАЩАЕТ значение S_OK, если перед инициализацией MAPI еще не выполнялась инициализация.</span><span class="sxs-lookup"><span data-stu-id="98e1a-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="98e1a-123">Клиент или поставщик услуг должен вызвать **мапиинитиализе** перед выполнением любого другого вызова MAPI.</span><span class="sxs-lookup"><span data-stu-id="98e1a-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="98e1a-124">В противном случае вызовы клиента или поставщика услуг приводят к возврату значения МАПИ_Е_НОТ_ИНИТИАЛИЗЕД.</span><span class="sxs-lookup"><span data-stu-id="98e1a-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="98e1a-125">При вызове **мапиинитиализе** из многопоточного приложения задайте для параметра _лпмапиинит_ структуру [MAPIINIT_0](mapiinit_0.md) , которая объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="98e1a-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="98e1a-126">**MAPIINIT_0** МАПИИНИТ = {0, МАПИ_МУЛТИСРЕАД_НОТИФИКАТИОНС}</span><span class="sxs-lookup"><span data-stu-id="98e1a-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="98e1a-127">и звоните:</span><span class="sxs-lookup"><span data-stu-id="98e1a-127">and call:</span></span> 
  
 <span data-ttu-id="98e1a-128">**Мапиинитиализе** (&amp;Мапиинит);</span><span class="sxs-lookup"><span data-stu-id="98e1a-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="98e1a-129">Если эта структура объявлена, MAPI создает отдельный поток для обработки окна уведомления, который продолжается до тех пор, пока значение счетчика ссылок инициализации не станет равно нулю.</span><span class="sxs-lookup"><span data-stu-id="98e1a-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="98e1a-130">Служба Windows должна задать элемент **ulflags** структуры **MAPIINIT_0** , на который указывает _лпмапиинит_ , мапи_нт_сервице.</span><span class="sxs-lookup"><span data-stu-id="98e1a-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="98e1a-131">Вы не можете вызывать **мапиинитиализе** или **Мапиунинитиализе** из функции Win32 **DllMain** или любой другой функции, создающей или завершающей потоки.</span><span class="sxs-lookup"><span data-stu-id="98e1a-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="98e1a-132">Более подробную информацию можно узнать [в статье Использование потокобезопасных объектов](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="98e1a-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="98e1a-133">**Мапиинитиализе** не возвращает расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="98e1a-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="98e1a-134">В отличие от большинства других вызовов MAPI, значения возвращаемых значений строго определяются в соответствии с определенным шагом инициализации, для которого произошел сбой:</span><span class="sxs-lookup"><span data-stu-id="98e1a-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="98e1a-135">Проверяет параметры и флаги.</span><span class="sxs-lookup"><span data-stu-id="98e1a-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="98e1a-136">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР или МАПИ_Е_УНКНОВН_ФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="98e1a-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="98e1a-137">Вызывающий объект передал недопустимый параметр или флаг.</span><span class="sxs-lookup"><span data-stu-id="98e1a-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="98e1a-138">Инициализирует ключи реестра, необходимые для MAPI, и подтверждает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="98e1a-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="98e1a-139">Это действие происходит только в том случае, если клиентский процесс выполняется как служба в Windows и устанавливает флаг службы МАПИ_НТ в структуре **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="98e1a-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="98e1a-140">МАПИ_Е_ТУ_КОМПЛЕКС.</span><span class="sxs-lookup"><span data-stu-id="98e1a-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="98e1a-141">Процесс вызова — это служба Windows и разделы реестра, необходимые для MAPI, которые не удалось инициализировать.</span><span class="sxs-lookup"><span data-stu-id="98e1a-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="98e1a-142">Дополнительные сведения можно найти в журнале событий приложений.</span><span class="sxs-lookup"><span data-stu-id="98e1a-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="98e1a-143">Проверьте совместимость MAPI с OLE, а затем инициализируйте OLE.</span><span class="sxs-lookup"><span data-stu-id="98e1a-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="98e1a-144">Проверяет совместимость текущих версий OLE и MAPI.</span><span class="sxs-lookup"><span data-stu-id="98e1a-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="98e1a-145">МАПИ_Е_ВЕРСИОН.</span><span class="sxs-lookup"><span data-stu-id="98e1a-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="98e1a-146">Версия OLE, установленная на рабочей станции, несовместима с этой версией MAPI.</span><span class="sxs-lookup"><span data-stu-id="98e1a-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="98e1a-147">Инициализирует OLE.</span><span class="sxs-lookup"><span data-stu-id="98e1a-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="98e1a-148">На этом этапе эта функция может возвращать код ошибки, не указанный здесь.</span><span class="sxs-lookup"><span data-stu-id="98e1a-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="98e1a-149">Любая ошибка, _не_ указанная в этом разделе, предполагается поступать из функции **CoInitialize**функции OLE.</span><span class="sxs-lookup"><span data-stu-id="98e1a-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="98e1a-150">Инициализирует глобальные переменные для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="98e1a-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="98e1a-151">МАПИ_Е_СЕССИОН_ЛИМИТ.</span><span class="sxs-lookup"><span data-stu-id="98e1a-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="98e1a-152">MAPI настраивает контекст, характерный для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="98e1a-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="98e1a-153">Ошибки могут возникать на платформе Win16, если количество процессов превышает определенное число или в любой системе, если объем доступной памяти исчерпан.</span><span class="sxs-lookup"><span data-stu-id="98e1a-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="98e1a-154">Инициализирует общие глобальные переменные для всех процессов.</span><span class="sxs-lookup"><span data-stu-id="98e1a-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="98e1a-155">МАПИ_Е_НОТ_ЕНАУГХ_РЕСАУРЦЕС.</span><span class="sxs-lookup"><span data-stu-id="98e1a-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="98e1a-156">Недостаточно системных ресурсов для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="98e1a-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="98e1a-157">Инициализирует обработчик уведомлений, создает окно и его поток, если это запрошено флагом МАПИ_МУЛТИСРЕАД_НОТИФИКАТИОНС.</span><span class="sxs-lookup"><span data-stu-id="98e1a-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="98e1a-158">МАПИ_Е_ИНВАЛИД_ОБЖЕКТ.</span><span class="sxs-lookup"><span data-stu-id="98e1a-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="98e1a-159">Может привести к сбою, если ресурсы системы исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="98e1a-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="98e1a-160">ЗаГружает и Инициализирует поставщика профилей.</span><span class="sxs-lookup"><span data-stu-id="98e1a-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="98e1a-161">Проверяет, имеет ли **мапиинитиализе** доступ к разделу реестра, в котором хранятся данные профиля.</span><span class="sxs-lookup"><span data-stu-id="98e1a-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="98e1a-162">МАПИ_Е_НОТ_ИНИТИАЛИЗЕД.</span><span class="sxs-lookup"><span data-stu-id="98e1a-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="98e1a-163">Поставщик профилей обнаружил ошибку.</span><span class="sxs-lookup"><span data-stu-id="98e1a-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="98e1a-164">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="98e1a-164">MFCMAPI reference</span></span>

<span data-ttu-id="98e1a-165">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="98e1a-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="98e1a-166">**Файл**</span><span class="sxs-lookup"><span data-stu-id="98e1a-166">**File**</span></span>|<span data-ttu-id="98e1a-167">**Функция**</span><span class="sxs-lookup"><span data-stu-id="98e1a-167">**Function**</span></span>|<span data-ttu-id="98e1a-168">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="98e1a-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="98e1a-169">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="98e1a-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="98e1a-170">MFCMAPI использует метод **мапиинитиализе** для инициализации MAPI в фоновом потоке для выполнения некоторой обработки таблицы.</span><span class="sxs-lookup"><span data-stu-id="98e1a-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98e1a-171">См. также</span><span class="sxs-lookup"><span data-stu-id="98e1a-171">See also</span></span>



[<span data-ttu-id="98e1a-172">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="98e1a-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

