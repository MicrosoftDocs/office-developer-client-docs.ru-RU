---
title: Интеграция приложений управления с помощью установщика Office 365 нажми и работай
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Узнайте, как интегрировать установщик Office 365 нажми и работай с решением управления программным обеспечением.
ms.openlocfilehash: cdcdde0618e2b96ce997ba5e263f75d85c21fd11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318353"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="26b3a-103">Интеграция приложений управления с помощью установщика Office 365 нажми и работай</span><span class="sxs-lookup"><span data-stu-id="26b3a-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="26b3a-104">Узнайте, как интегрировать установщик Office 365 нажми и работай с решением управления программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="26b3a-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="26b3a-105">Установщик Office 365 нажми и работай предоставляет COM-интерфейс, который позволяет ИТ-специалистам и решениям управления программным способом управлять управлением обновлениями.</span><span class="sxs-lookup"><span data-stu-id="26b3a-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="26b3a-106">Этот интерфейс предоставляет дополнительные возможности управления помимо того, что предоставляется средством развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="26b3a-107">Эта статья относится к Office 2016 и более поздних версий, Office 365.</span><span class="sxs-lookup"><span data-stu-id="26b3a-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="26b3a-108">Интеграция с "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="26b3a-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="26b3a-109">Чтобы использовать этот интерфейс, приложение управляемости вызывает COM-интерфейс и вызывает интерфейсы API, напрямую взаимодействующие с службой установки "нажми и работай".</span><span class="sxs-lookup"><span data-stu-id="26b3a-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26b3a-110">Установщик Office нажми и работай можно запустить из командной строки с параметрами, которые могут управлять поведением, как описано в разделе [средство развертывания Office для "нажми](https://www.microsoft.com/en-us/download/details.aspx?id=49117)и работай".</span><span class="sxs-lookup"><span data-stu-id="26b3a-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="26b3a-111">**Ниже приведена концептуальная схема COM-интерфейса**</span><span class="sxs-lookup"><span data-stu-id="26b3a-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="26b3a-112">![Схема использования интерфейса COM в установщике Office "нажми] и работай". (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования интерфейса COM в установщике Office \"нажми") и работай"</span><span class="sxs-lookup"><span data-stu-id="26b3a-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="26b3a-113">Установщик Office 365 Click-to-Run реализует интерфейс на основе COM, **иупдатенотифи** зарегистрированный в CLSID **клсид_упдатенотифйобжект**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="26b3a-114">Этот интерфейс можно вызвать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="26b3a-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="26b3a-115">Вызов будет успешным только в том случае, если вызывающий абонент работает с повышенными привилегиями, так как программа установки "нажми и работай" должна выполняться с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="26b3a-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="26b3a-116">COM-интерфейс **иупдатенотифи** предоставляет три асинхронные функции, ответственные за проверку команд и параметров и выполнение планирования с помощью службы установки "нажми и работай".</span><span class="sxs-lookup"><span data-stu-id="26b3a-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="26b3a-117">Метод, **Status**, может использоваться для получения сведений о состоянии последней выполненной команды или о состоянии выполняемой в данный момент команды (например, успех, сбой, подробные коды ошибок).</span><span class="sxs-lookup"><span data-stu-id="26b3a-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="26b3a-118">Во время жизненного цикла служба установки "нажми и работай" может находиться в четырех состояниях, в которых могут вызываться методы **иупдатенотифи** ; Перезагрузка, безДействие, Загрузка и применение.</span><span class="sxs-lookup"><span data-stu-id="26b3a-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="26b3a-119">**Ниже показана схема конечного автомата COM-интерфейса**</span><span class="sxs-lookup"><span data-stu-id="26b3a-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="26b3a-120">![Схема состояний для интерфейса COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Схема состояний для интерфейса COM")</span><span class="sxs-lookup"><span data-stu-id="26b3a-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="26b3a-121">**Перезагрузка**: при загрузке компьютера в случае недоступности службы установки "нажми и работай" происходит определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="26b3a-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="26b3a-122">Успешный вызов метода status после перезагрузки возвратит Еупдате_ункновн.</span><span class="sxs-lookup"><span data-stu-id="26b3a-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="26b3a-123">**Бездействие:** Когда установщик "нажми и работай" находится в состоянии простоя, вы можете вызвать:</span><span class="sxs-lookup"><span data-stu-id="26b3a-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="26b3a-124">**Apply**: установка ранее загруженного контента.</span><span class="sxs-lookup"><span data-stu-id="26b3a-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="26b3a-125">**Cancel**: возвращает `0x800000e`, "метод был вызван в непредвиденное время."</span><span class="sxs-lookup"><span data-stu-id="26b3a-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="26b3a-126">**Download**: Загрузка нового контента в клиент для последующей установки.</span><span class="sxs-lookup"><span data-stu-id="26b3a-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="26b3a-127">**Status**: возвращает результат последнего выполненного действия или сообщение об ошибке, если действие завершилось с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="26b3a-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="26b3a-128">Если предыдущее действие отсутствует, `eUPDATE_UNKNOWN`возвращается **состояние** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="26b3a-129">**Скачивание:** Когда установщик "нажми и работай" находится в состоянии загрузки, вы можете вызвать:</span><span class="sxs-lookup"><span data-stu-id="26b3a-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="26b3a-130">**Apply**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="26b3a-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="26b3a-131">**Отмена**: остановка скачивания и удаление частично загруженного контента.</span><span class="sxs-lookup"><span data-stu-id="26b3a-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="26b3a-132">**Download**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="26b3a-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="26b3a-133">**Status**: возвращает **довнлоад_вип** , чтобы указать, что выполняется загрузка.</span><span class="sxs-lookup"><span data-stu-id="26b3a-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="26b3a-134">**Применение:** Когда установщик "нажми и работай" находится в процессе установки ранее загружаемого содержимого:</span><span class="sxs-lookup"><span data-stu-id="26b3a-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="26b3a-135">**Apply**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="26b3a-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="26b3a-136">**Cancel**: возвращает `0x800000e`, действие Apply не может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="26b3a-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="26b3a-137">**Download**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="26b3a-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="26b3a-138">**Status**: возвращает **аппли_вип** , чтобы указать, что выполняется работа.</span><span class="sxs-lookup"><span data-stu-id="26b3a-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="26b3a-139">Так как OfficeC2RCOM является службой COM+ и динамически загружается, вам необходимо вызвать функцию **CoCreateInstance** при каждом вызове метода для этого класса, чтобы убедиться, что вы получаете ожидаемый результат.</span><span class="sxs-lookup"><span data-stu-id="26b3a-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="26b3a-140">При необходимости служба COM+ будет обрабатывать создание нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="26b3a-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="26b3a-141">Когда один из методов вызывается в первый раз, COM+ загрузит объект **иупдатенотифи** и запустите его в одном из экземпляров Dllhost. exe.</span><span class="sxs-lookup"><span data-stu-id="26b3a-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="26b3a-142">Новый объект остается активным в течение приблизительно 3 минут.</span><span class="sxs-lookup"><span data-stu-id="26b3a-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="26b3a-143">Если последующий вызов выполняется через три минуты последнего вызова, объект **иупдатенотифи** останется загруженным, а новый экземпляр не будет создан.</span><span class="sxs-lookup"><span data-stu-id="26b3a-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="26b3a-144">Если в течение трех минут ничего не происходит, объект Иупдатенотифи будет выгружен, а при следующем вызове будет создан новый объект **иупдатенотифи** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="26b3a-145">Справочное руководство по API-ИНТЕРФЕЙСу API для установщика "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="26b3a-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="26b3a-146">В следующей справочной документации по API:</span><span class="sxs-lookup"><span data-stu-id="26b3a-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="26b3a-147">Параметры представлены в формате "ключ-значение", разделенном пробелом.</span><span class="sxs-lookup"><span data-stu-id="26b3a-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="26b3a-148">В параметрах регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="26b3a-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="26b3a-149">Существует [список параметров](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) , доступных в документации.</span><span class="sxs-lookup"><span data-stu-id="26b3a-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="26b3a-150">Сводка интерфейса IUpdateNotify2 теперь включена.</span><span class="sxs-lookup"><span data-stu-id="26b3a-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="26b3a-151">Применить</span><span class="sxs-lookup"><span data-stu-id="26b3a-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="26b3a-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="26b3a-152">Parameters</span></span>

-  <span data-ttu-id="26b3a-153">_displaylevel_: **true** , чтобы показать состояние установки, включая ошибки, во время процесса обновления; **значение false** , чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="26b3a-154">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="26b3a-155">_forceappshutdown_: **true** для принудительного завершения работы приложений Office при запуске действия **Apply** ; в противном случае — **false** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="26b3a-156">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-156">The default is **false**.</span></span> <span data-ttu-id="26b3a-157">Дополнительные [](#bk_ApplyRemark) сведения см.</span><span class="sxs-lookup"><span data-stu-id="26b3a-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="26b3a-158">Если какое-либо приложение Office запускается при запуске действия **Apply** , действие **Применить** обычно завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="26b3a-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="26b3a-159">Передача `forceappshutdown=true` в метод **Apply** приведет к тому, что служба **оффицекликкторун** сразу же завершит работу приложений и применит обновление.</span><span class="sxs-lookup"><span data-stu-id="26b3a-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="26b3a-160">В этом случае в работе пользователя могут возникать потери данных.</span><span class="sxs-lookup"><span data-stu-id="26b3a-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="26b3a-161">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="26b3a-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26b3a-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="26b3a-162">**S_OK**</span></span> <br/> |<span data-ttu-id="26b3a-163">Действие успешно отправлено службе "нажми и работай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="26b3a-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="26b3a-164">**Е_АКЦЕССДЕНИЕД**</span><span class="sxs-lookup"><span data-stu-id="26b3a-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="26b3a-165">Вызывающий абонент не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="26b3a-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="26b3a-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="26b3a-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="26b3a-167">Переданы неДопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="26b3a-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="26b3a-168">**Е_ИЛЛЕГАЛ_МЕСОД_КАЛЛ**</span><span class="sxs-lookup"><span data-stu-id="26b3a-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="26b3a-169">В настоящее время действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="26b3a-169">Action is not allowed at this time.</span></span> <span data-ttu-id="26b3a-170">Дополнительные [](#bk_ApplyRemark) сведения см.</span><span class="sxs-lookup"><span data-stu-id="26b3a-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="26b3a-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26b3a-171">Remarks</span></span>

- <span data-ttu-id="26b3a-172">Если какое-либо приложение Office запускается при запуске действия **Apply** , действие **Apply** завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="26b3a-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="26b3a-173">При `forceappshutdown=true` передаче в метод **Apply** служба **оффицекликкторун** немедленно завершит работу всех запущенных приложений Office и применить обновление.</span><span class="sxs-lookup"><span data-stu-id="26b3a-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="26b3a-174">Пользователь может столкнуться с данными, так как они не получают запроса на сохранение изменений в открытых документах...</span><span class="sxs-lookup"><span data-stu-id="26b3a-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="26b3a-175">Это действие может быть вызвано только в том случае, если состоянием COM является один из следующих:</span><span class="sxs-lookup"><span data-stu-id="26b3a-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="26b3a-176">**Еупдате_ункновн**</span><span class="sxs-lookup"><span data-stu-id="26b3a-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="26b3a-177">**Едовнлоад_канцеллед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="26b3a-178">**Едовнлоад_фаилед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="26b3a-179">**Едовнлоад_сукцеедед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="26b3a-180">**Еаппли_сукцеедед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="26b3a-181">**Еаппли_фаилед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="26b3a-182">При вызове метода **Apply** без предварительной загрузки содержимого метод **Apply** будет сообщать об **успешном** завершении, так как он не обнаружил, что успешно применялся и завершил процесс **применения** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="26b3a-183">Отмена</span><span class="sxs-lookup"><span data-stu-id="26b3a-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="26b3a-184">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="26b3a-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26b3a-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="26b3a-185">S_OK</span></span>  <br/> |<span data-ttu-id="26b3a-186">Действие успешно отправлено службе "нажми и работай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="26b3a-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="26b3a-187">Е_ИЛЛЕГАЛ_МЕСОД_КАЛЛ</span><span class="sxs-lookup"><span data-stu-id="26b3a-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="26b3a-188">В настоящее время действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="26b3a-188">Action is not allowed at this time.</span></span> <span data-ttu-id="26b3a-189">Для получения дополнительных сведений см раздел ["Примечания](#bk_CancelRemarks) ".</span><span class="sxs-lookup"><span data-stu-id="26b3a-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="26b3a-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26b3a-190">Remarks</span></span>

- <span data-ttu-id="26b3a-191">Этот метод может быть вызван только в том случае, если идентификатор состояния COM **едовнлоад_вип**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="26b3a-192">Будет предпринята попытка отменить текущее действие скачивания.</span><span class="sxs-lookup"><span data-stu-id="26b3a-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="26b3a-193">Состояние COM изменится на **едовнлоад_канцеллинг** и в конечном итоге изменится на **едовнлоад_канцелед**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="26b3a-194">Состояние COM возвращает значение **е_иллегал_месод_калл** , если триггер запускается в любое другое время.</span><span class="sxs-lookup"><span data-stu-id="26b3a-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="26b3a-195">Скачать</span><span class="sxs-lookup"><span data-stu-id="26b3a-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="26b3a-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="26b3a-196">Parameters</span></span>

-  <span data-ttu-id="26b3a-197">_displaylevel_: **true** , чтобы показать состояние установки, включая ошибки, во время процесса обновления; **значение false** , чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="26b3a-198">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="26b3a-199">_упдатебасеурл_: URL-адрес альтернативного источника скачивания.</span><span class="sxs-lookup"><span data-stu-id="26b3a-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="26b3a-200">_упдатетоверсион_: версия для обновления Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="26b3a-201">Определите этот параметр, если необходимо обновить более старую версию, чем версия, установленная в данный момент.</span><span class="sxs-lookup"><span data-stu-id="26b3a-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="26b3a-202">_довнлоадсаурце_: CLSID настраиваемой реализации **ИБАККГРАУНДКОПИМАНАЖЕР** (диспетчер BITS).</span><span class="sxs-lookup"><span data-stu-id="26b3a-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="26b3a-203">Идентификатор _ContentId_: определяет содержимое для загрузки с сервера контента через настраиваемый диспетчер BITS.</span><span class="sxs-lookup"><span data-stu-id="26b3a-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="26b3a-204">Это значение передается через интерфейс BITS для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="26b3a-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="26b3a-205">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="26b3a-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26b3a-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="26b3a-206">**S_OK**</span></span> <br/> |<span data-ttu-id="26b3a-207">Действие успешно отправлено службе "нажми и работай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="26b3a-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="26b3a-208">**Е_АКЦЕССДЕНИЕД**</span><span class="sxs-lookup"><span data-stu-id="26b3a-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="26b3a-209">Вызывающий абонент не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="26b3a-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="26b3a-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="26b3a-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="26b3a-211">Переданы неДопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="26b3a-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="26b3a-212">**Е_ИЛЛЕГАЛ_МЕСОД_КАЛЛ**</span><span class="sxs-lookup"><span data-stu-id="26b3a-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="26b3a-213">В настоящее время действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="26b3a-213">Action is not allowed at this time.</span></span> <span data-ttu-id="26b3a-214">Дополнительные [](#bk_DownloadRemark) сведения см.</span><span class="sxs-lookup"><span data-stu-id="26b3a-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="26b3a-215">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26b3a-215">Remarks</span></span>

- <span data-ttu-id="26b3a-216">Необходимо указать _довнлоадсаурце_ и идентификатор _ContentId_ в виде связывания.</span><span class="sxs-lookup"><span data-stu-id="26b3a-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="26b3a-217">В противном случае метод **download** возвратит ошибку **е_инвалидарг** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="26b3a-218">Если указаны _довнлоадсаурце_, _ContentId_и _упдатебасеурл_ , _упдатебасеурл_ будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="26b3a-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="26b3a-219">Это действие может быть вызвано только в том случае, если состоянием COM является один из следующих:</span><span class="sxs-lookup"><span data-stu-id="26b3a-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="26b3a-220">**Еупдате_ункновн**</span><span class="sxs-lookup"><span data-stu-id="26b3a-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="26b3a-221">**Едовнлоад_канцеллед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="26b3a-222">**Едовнлоад_фаилед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="26b3a-223">**Едовнлоад_сукцеедед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="26b3a-224">**Еаппли_сукцеедед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="26b3a-225">**Еаппли_фаилед**</span><span class="sxs-lookup"><span data-stu-id="26b3a-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="26b3a-226">При вызове метода **Apply** без ранее скачанного содержимого метод **Apply** будет сообщать об **успешном** завершении, так как он не обнаружил, что успешно применялся и завершил процесс **применения** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="26b3a-227">Примеры</span><span class="sxs-lookup"><span data-stu-id="26b3a-227">Examples</span></span>

- <span data-ttu-id="26b3a-228">Чтобы скачать содержимое из настраиваемого диспетчера BITS: выЗовите функцию **скачать ()** , передав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="26b3a-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="26b3a-229">Чтобы скачать содержимое из сети CDN Microsoft CDN: выЗовите функцию **скачать ()** , не указывая параметры _довнлоадсаурце_, _ContentId_или _упдатебасеурл_ .</span><span class="sxs-lookup"><span data-stu-id="26b3a-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="26b3a-230">Чтобы скачать содержимое из настраиваемого расположения: выЗовите функцию **скачать ()** , передав следующий параметр:</span><span class="sxs-lookup"><span data-stu-id="26b3a-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="26b3a-231">Состояние</span><span class="sxs-lookup"><span data-stu-id="26b3a-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="26b3a-232">Параметры</span><span class="sxs-lookup"><span data-stu-id="26b3a-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="26b3a-233">_Пупдатестатусрепорт_</span><span class="sxs-lookup"><span data-stu-id="26b3a-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="26b3a-234">Указатель на структуру УПДАТЕ_СТАТУС_РЕПОРТ.</span><span class="sxs-lookup"><span data-stu-id="26b3a-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="26b3a-235">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="26b3a-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26b3a-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="26b3a-236">**S_OK**</span></span> <br/> |<span data-ttu-id="26b3a-237">Метод **Status** всегда возвращает этот результат.</span><span class="sxs-lookup"><span data-stu-id="26b3a-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="26b3a-238">Проверка `UPDATE_STATUS_RESULT` структуры на состояние текущего действия.</span><span class="sxs-lookup"><span data-stu-id="26b3a-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="26b3a-239">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26b3a-239">Remarks</span></span>

- <span data-ttu-id="26b3a-240">В поле Status ( `UPDATE_STATUS_REPORT` состояние) содержится состояние текущего действия.</span><span class="sxs-lookup"><span data-stu-id="26b3a-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="26b3a-241">Возвращается одно из следующих значений состояния:</span><span class="sxs-lookup"><span data-stu-id="26b3a-241">One of the following status values is returned:</span></span> 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- <span data-ttu-id="26b3a-242">Если последняя команда привела к ошибке, в поле ошибка `UPDATE_STATUS_REPORT` содержится подробная информация об ошибке.</span><span class="sxs-lookup"><span data-stu-id="26b3a-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="26b3a-243">В методе **Status** возвращается два типа кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="26b3a-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="26b3a-244">Если ошибка меньше `UPDATE_ERROR_CODE::eUNKNOWN`, то ошибка является одним из следующих предварительно определенных кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="26b3a-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  <span data-ttu-id="26b3a-245">Если код ошибки возврата превышает `UPDATE_ERROR_CODE::eUNKNOWN` значение **HRESULT** неудачного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="26b3a-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="26b3a-246">Чтобы извлечь значение HRESULT, `UPDATE_ERROR_CODE::eUNKNOWN` вычитаемое из значения, которое возвращается в поле `UPDATE_STATUS_REPORT`"ошибка".</span><span class="sxs-lookup"><span data-stu-id="26b3a-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="26b3a-247">Полный список значений состояния и ошибок можно просмотреть, изучив библиотеку типов **иупдатенотифи** , встроенную в OfficeC2RCom. dll.</span><span class="sxs-lookup"><span data-stu-id="26b3a-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="26b3a-248">Поле ContentId используется для вызовов с состоянием \*\*\*\* после **загрузки** и возвращает идентификатор ContentId, переданный в вызов **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="26b3a-249">Рекомендуется инициализировать это поле до **значения NULL** перед вызовом метода **Status** , а затем проверить значение после того, как было возвращено значение **Status** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="26b3a-250">Если значение по-прежнему равно **null**, это означает, что идентификатор ContentId не возвращается.</span><span class="sxs-lookup"><span data-stu-id="26b3a-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="26b3a-251">Если значение отлично от **null**, его необходимо освободить с помощью вызова **SysFreeString ()**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="26b3a-252">Ниже приведен фрагмент кода, посвященный вызову **состояния** после **загрузки**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="26b3a-253">Сводка по интерфейсу IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="26b3a-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="26b3a-254">Эта сводка предоставляется в качестве приветственной информации о [том, как интегрировать приложения управления с установщикОм Office 365 нажми](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx)и работай.</span><span class="sxs-lookup"><span data-stu-id="26b3a-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx).</span></span> <span data-ttu-id="26b3a-255">После обновления общедоступного документа этот документ можно считать устаревшим.</span><span class="sxs-lookup"><span data-stu-id="26b3a-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="26b3a-256">В C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (первая общедоступная сборка должна быть в июне сборка--8326. \*) мы добавили новый интерфейс **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-256">From C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="26b3a-257">Ниже представлено несколько основных сведений об этом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="26b3a-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="26b3a-258">CLSID_UpdateNotifyObject2, {52C2F9C2 — F1AC – 4021 – BF50 – 756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="26b3a-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="26b3a-259">Этот интерфейс также размещает исходный интерфейс Иупдатенотифи для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="26b3a-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="26b3a-260">Это означает, что при использовании этого интерфейса вы можете получить доступ ко всем методам, предоставляемым в интерфейсе **упдатенотифйобжект** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="26b3a-261">Новые методы, добавленные в IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="26b3a-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="26b3a-262">**HRESULT** Жетблоккингаппс ([выходной] BSTR \* аппслист).</span><span class="sxs-lookup"><span data-stu-id="26b3a-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="26b3a-263">Получение списка заблокированных приложений для обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-263">Get updates blocking apps list.</span></span> <span data-ttu-id="26b3a-264">Этот вызов возвратит запуск приложений Office, которые будут блокировать процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="26b3a-265">**HRESULT** Жетоффицедеплойментдата ([in] int dataType, [in] **значение LPCWSTR** пквсзнаме, [out] BSTR \* оффицедата).</span><span class="sxs-lookup"><span data-stu-id="26b3a-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="26b3a-266">Получение данных развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="26b3a-267">Если вы хотите использовать новые методы, необходимо убедиться в том, что:</span><span class="sxs-lookup"><span data-stu-id="26b3a-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="26b3a-268">Ваша версия C2R более новая, чем приведенная выше\>сборка (= с помощью построения разветвления за июнь).</span><span class="sxs-lookup"><span data-stu-id="26b3a-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="26b3a-269">Используйте UpdateNotifyObject2, а не **упдатенотифйобжект** , чтобы вызвать функцию **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="26b3a-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="26b3a-270">Если вы не используете ни один из новых методов, вам не нужно ничего менять.</span><span class="sxs-lookup"><span data-stu-id="26b3a-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="26b3a-271">Все существующие методы будут работать точно так же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="26b3a-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="26b3a-272">Реализация интерфейса BITS</span><span class="sxs-lookup"><span data-stu-id="26b3a-272">Implementing the BITS interface</span></span>

<span data-ttu-id="26b3a-273">[ФоновАя интеллектуальнАя служба передачи](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (BITS) — это служба, предоставляемая корпорацией Майкрософт для передачи файлов между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="26b3a-273">The [Background Intelligent Transfer Service](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="26b3a-274">BITS это один из каналов, которые может использовать установщик Office нажми и работай для загрузки контента.</span><span class="sxs-lookup"><span data-stu-id="26b3a-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="26b3a-275">По умолчанию установщик Office нажми и работай использует встроенную в Windows реализацию BITS для загрузки содержимого из сети CDN.</span><span class="sxs-lookup"><span data-stu-id="26b3a-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="26b3a-276">Предоставляя настраиваемую реализацию BITS методу **Download ()** интерфейса **иупдатенотифи** , программное обеспечение управления может управлять тем, где и как клиент загружает контент.</span><span class="sxs-lookup"><span data-stu-id="26b3a-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="26b3a-277">Настраиваемый интерфейс BITS полезен при предоставлении настраиваемого канала распространения содержимого, отличного от встроенных каналов "нажми и работай", таких как CDN CDN, серверы IIS или общие файловые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="26b3a-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="26b3a-278">Минимальное требование для настраиваемого интерфейса BITS для работы со службой Office C2R:</span><span class="sxs-lookup"><span data-stu-id="26b3a-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="26b3a-279">Для **ибаккграундкопиманажер**:</span><span class="sxs-lookup"><span data-stu-id="26b3a-279">For **IBackgroundCopyManager**:</span></span>
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- <span data-ttu-id="26b3a-280">Для **ибаккграундкопижоб**:</span><span class="sxs-lookup"><span data-stu-id="26b3a-280">For **IBackgroundCopyJob**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- <span data-ttu-id="26b3a-281">Для **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="26b3a-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="26b3a-282">Для функций `Addfile` и `AddFileWithRanges` функции and удаленный URL-адрес имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="26b3a-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="26b3a-283">кмбитс жестко запрограммирована, а обозначает настроенные биты.</span><span class="sxs-lookup"><span data-stu-id="26b3a-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="26b3a-284">Идентификатор ContentId __ _\> является параметром ContentId для метода \<_ **Download ()** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="26b3a-285">_относительный путь к\> целевому файлу указывает расположение и имя файла, который требуется скачать. \<_</span><span class="sxs-lookup"><span data-stu-id="26b3a-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="26b3a-286">Например, если вы указали объект _ContentId_ `f732af58-5d86-4299-abe9-7595c35136ef` для метода **Download ()** , и Office C2R хочет скачать CAB-файл версии, например `v32.cab` File, он вызовите **аддфиле ()** , выполнив следующие `RemoteUrl`действия:</span><span class="sxs-lookup"><span data-stu-id="26b3a-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="26b3a-287">Для **ибаккграундкоперрор**:</span><span class="sxs-lookup"><span data-stu-id="26b3a-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="26b3a-288">Для **ибаккграундкопифиле**:</span><span class="sxs-lookup"><span data-stu-id="26b3a-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/en-us/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/en-us/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="26b3a-289">Автоматизация промежуточного хранения контента</span><span class="sxs-lookup"><span data-stu-id="26b3a-289">Automating content staging</span></span>

<span data-ttu-id="26b3a-290">ИТ-администраторы могут разрешить клиентам для настольных ПК автоматически получать обновления, когда они доступны непосредственно из сети доставки содержимого (CDN) Microsoft (CDN), или могут управлять развертыванием обновлений, доступных в обновлении каналы с помощью средства развертывания Office или System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="26b3a-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="26b3a-291">Служба поддерживает возможность средств управления определять и автоматизировать загрузку контента при наличии обновлений.</span><span class="sxs-lookup"><span data-stu-id="26b3a-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="26b3a-292">**На следующем рисунке представлен обзор загрузки настраиваемого изображения.**</span><span class="sxs-lookup"><span data-stu-id="26b3a-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="26b3a-293">![Схема использования интерфейса COM в установщике Office "нажми] и работай". (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования интерфейса COM в установщике Office \"нажми") и работай"</span><span class="sxs-lookup"><span data-stu-id="26b3a-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="26b3a-294">Обзор загрузки настраиваемого изображения</span><span class="sxs-lookup"><span data-stu-id="26b3a-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="26b3a-295">На предыдущей схеме вы увидите, что новый образ Office 365 профессиональный плюс доступен в сети доставки содержимого Office (CDN).</span><span class="sxs-lookup"><span data-stu-id="26b3a-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="26b3a-296">Вместе с изображением Office 365 профессиональный плюс доступен список файлов в формате XML, в котором есть информация, необходимая для поддержки управляемого программного обеспечения для непосредственного создания настраиваемых образов, которые заменяют необходимость использования средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="26b3a-297">Предприятие настраивает свои WSUS для синхронизации обновлений клиента Office 365.</span><span class="sxs-lookup"><span data-stu-id="26b3a-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="26b3a-298">Эти обновления не содержат полезных данных изображения, но позволяют программному обеспечению для управления распознать, когда будет доступен новый контент.</span><span class="sxs-lookup"><span data-stu-id="26b3a-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="26b3a-299">Затем программное обеспечение для управления может прочитать метаданные обновления клиента, чтобы узнать, к какой версии Office относится обновление.</span><span class="sxs-lookup"><span data-stu-id="26b3a-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="26b3a-300">Если обновление возможно, программное обеспечение для управления может использовать содержимое CDN и список файлов для создания настраиваемого образа и сохранения его в расположении общего файлового ресурса, который он использует.</span><span class="sxs-lookup"><span data-stu-id="26b3a-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="26b3a-301">Формат списка XML-файлов</span><span class="sxs-lookup"><span data-stu-id="26b3a-301">Format of the XML file list</span></span>

<span data-ttu-id="26b3a-302">В CAB-файле сети CDN доступно два списка файлов.</span><span class="sxs-lookup"><span data-stu-id="26b3a-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="26b3a-303">Один список файлов для 32 разрядной версии Office и другой для 64 — разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="26b3a-304">URL-адрес списка файлов Office (ОФЛ. CAB- [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab)файл).</span><span class="sxs-lookup"><span data-stu-id="26b3a-304">The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="26b3a-305">Вызываются два списка файлов:</span><span class="sxs-lookup"><span data-stu-id="26b3a-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="26b3a-306">O365Client_32bit. XML</span><span class="sxs-lookup"><span data-stu-id="26b3a-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="26b3a-307">O365Client_64bit. XML</span><span class="sxs-lookup"><span data-stu-id="26b3a-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="26b3a-308">В XML-файле для каждого списка файлов указывается <UpdateFiles> узел, который содержит атрибут Version.</span><span class="sxs-lookup"><span data-stu-id="26b3a-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="26b3a-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="26b3a-309"></span></span> <span data-ttu-id="26b3a-310">Эта версия увеличивается при внесении изменений в списки файлов.</span><span class="sxs-lookup"><span data-stu-id="26b3a-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="26b3a-311">Существует два параметра, которые необходимо объединить с XML, чтобы создать настраиваемое изображение:</span><span class="sxs-lookup"><span data-stu-id="26b3a-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="26b3a-312">Замените *% Version%* на версию сборки Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="26b3a-313">Это может быть получено из метаданных обновления клиента (описывается в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="26b3a-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="26b3a-314">Определите *baseURL* с использованием значения URL-адреса, связанного с ветвью, для которой создается изображение.</span><span class="sxs-lookup"><span data-stu-id="26b3a-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="26b3a-315">Это является производным от метаданных обновления клиента, описанных в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="26b3a-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="26b3a-316">Для создания изображения можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="26b3a-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="26b3a-317">Откройте список XML-файлов.</span><span class="sxs-lookup"><span data-stu-id="26b3a-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="26b3a-318">Замените вхождения *% Version%* соответствующей версией сборки Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="26b3a-319">Версию сборки можно получить из релеасехистори. XML, как описано далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="26b3a-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="26b3a-320">Прочитайте атрибут URL для целевой ветви.</span><span class="sxs-lookup"><span data-stu-id="26b3a-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="26b3a-321">Удалить Языковые узлы для всех языков, не обязательных в настраиваемом образе.</span><span class="sxs-lookup"><span data-stu-id="26b3a-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="26b3a-322">Узлы с языком = "0" нейтральны к языку и должны быть включены в образ.</span><span class="sxs-lookup"><span data-stu-id="26b3a-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="26b3a-323">Создайте локальное изображение сети CDN, пересматривая список XML-файлов и скопировав файлы CDN, создавая структуру папок по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="26b3a-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="26b3a-324">Если указан \*\* атрибут Rename, переименуйте \*\* скопированный файл в значение, указанное в атрибуте Rename.</span><span class="sxs-lookup"><span data-stu-id="26b3a-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="26b3a-325">Используется для создания файлов верхнего уровня по умолчанию v64. cab и v32. cab.</span><span class="sxs-lookup"><span data-stu-id="26b3a-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="26b3a-326">Это переименованные версии CAB-файла верхнего уровня, которые используются в качестве версии установки по умолчанию, если версия не указана.</span><span class="sxs-lookup"><span data-stu-id="26b3a-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="26b3a-327">Для создания расположения CDN используйте URL-адрес + Релативепас + имя файла.</span><span class="sxs-lookup"><span data-stu-id="26b3a-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="26b3a-328">Ниже приведены примеры, в которых используется месячный канал (в соответствии с `<baseURL>` определением узла) и версия сборки 16.0.4229.1004 из релеасехистори. XML.</span><span class="sxs-lookup"><span data-stu-id="26b3a-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="26b3a-329">Ниже приведен независимый от языка файл, необходимый для всех языков.</span><span class="sxs-lookup"><span data-stu-id="26b3a-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="26b3a-330">Имя файла v64_ 16.0.4229.1004. cab и его следует скопировать из `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` и переименовать в. `…/office/data/v64.cab`</span><span class="sxs-lookup"><span data-stu-id="26b3a-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="26b3a-331">Ниже приведен файл, который должен быть включен в изображение en-US в соответствии с языком LCID = 1033.</span><span class="sxs-lookup"><span data-stu-id="26b3a-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="26b3a-332">Имя файла s641033. cab и его следует скопировать из `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` него и не переименовывать.</span><span class="sxs-lookup"><span data-stu-id="26b3a-332">The name of the file is s641033.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="26b3a-333">Проверка хэша файлов DAT</span><span class="sxs-lookup"><span data-stu-id="26b3a-333">Hash verification of .dat files</span></span>

<span data-ttu-id="26b3a-334">Средства создания изображений могут проверить целостность скачанных файлов DAT, сравнив вычисленное значение ХЭША с заданным ХЭШЕМ со значением, сопоставленным с каждым из DAT-файлов.</span><span class="sxs-lookup"><span data-stu-id="26b3a-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="26b3a-335">Ниже приведен пример файла DAT из ежемесячного канала с версией сборки 16.0.4229.1004 и языковым набором для болгарского языка:</span><span class="sxs-lookup"><span data-stu-id="26b3a-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="26b3a-336">Атрибут **хашлокатион** указывает расположение относительного пути Stream.x64.bg-bg. hash для файла Stream.x64.bg-БГ. dat.</span><span class="sxs-lookup"><span data-stu-id="26b3a-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="26b3a-337">Создайте расположение хэш-файла с помощью сцепления URL + Релативепас + Хашлокатион.</span><span class="sxs-lookup"><span data-stu-id="26b3a-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="26b3a-338">В следующем примере расположение stream.x64.bg-bg. hash будет следующим:</span><span class="sxs-lookup"><span data-stu-id="26b3a-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="26b3a-339">Атрибут **хашалго** указывает, какой алгоритм хеширования использовался.</span><span class="sxs-lookup"><span data-stu-id="26b3a-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="26b3a-340">В этом случае использовался SHA256.</span><span class="sxs-lookup"><span data-stu-id="26b3a-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="26b3a-341">Чтобы проверить целостность файла stream.x64.bg-БГ. dat, откройте stream.x64.bg-bg. hash и прочтите хэш-значение, которое является первой строкой текста в хэш-файле.</span><span class="sxs-lookup"><span data-stu-id="26b3a-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="26b3a-342">Сравните это с вычисленным значением хэша (с использованием указанного алгоритма хеширования), чтобы проверить целостность загруженного файла. dat.</span><span class="sxs-lookup"><span data-stu-id="26b3a-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="26b3a-343">В следующем примере показан код C# для считывания хеша.</span><span class="sxs-lookup"><span data-stu-id="26b3a-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="26b3a-344">Обновления для клиентов Office 365</span><span class="sxs-lookup"><span data-stu-id="26b3a-344">Office 365 Client Updates</span></span>

<span data-ttu-id="26b3a-345">Все обновления для клиентов Office 365 опубликованы в [каталоге обновлений Майкрософт](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="26b3a-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="26b3a-346">Обновления клиента Office 365 позволяют программному обеспечению программного обеспечения для программного обеспечения программного обеспечения обновления клиента Office 365 аналогично любому другому обновлению WU с одним исключением; обновления клиента не содержат реальных полезных данных.</span><span class="sxs-lookup"><span data-stu-id="26b3a-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="26b3a-347">Обновления клиента Office 365 не должны устанавливаться на всех клиентах, а использовать для запуска рабочих процессов с программным обеспечением с программным обеспечением, заменив команду установки на основе механизма установки на основе COM, показанного выше.</span><span class="sxs-lookup"><span data-stu-id="26b3a-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="26b3a-348">**На следующем рисунке показана схема рабочего процесса обновления клиента Office 365.**</span><span class="sxs-lookup"><span data-stu-id="26b3a-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="26b3a-349">![Схема рабочего процесса для обновлений клиента O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Схема рабочего процесса для обновлений клиента O365PP")</span><span class="sxs-lookup"><span data-stu-id="26b3a-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="26b3a-350">Каждое публикуемое обновление клиента Office 365 содержит метаданные об обновлении.</span><span class="sxs-lookup"><span data-stu-id="26b3a-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="26b3a-351">Эти метаданные содержат параметр с именем *мореинфаурл* , который можно использовать для получения следующих сведений:</span><span class="sxs-lookup"><span data-stu-id="26b3a-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="26b3a-352">*Ver*: идентифицирует версию Office, связанную с этим обновлением.</span><span class="sxs-lookup"><span data-stu-id="26b3a-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="26b3a-353">*Branch*: идентифицирует канал обновления для этого обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="26b3a-354">К значениям относятся Инсидерфаст, предварительные оценки, ежемесячные, целевые, общие.</span><span class="sxs-lookup"><span data-stu-id="26b3a-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="26b3a-355">В будущем можно добавить дополнительные значения.</span><span class="sxs-lookup"><span data-stu-id="26b3a-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="26b3a-356">*Arch*: идентифицирует архитектуру процессора, связанную с этим обновлением.</span><span class="sxs-lookup"><span data-stu-id="26b3a-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="26b3a-357">*ксмлвер*: версия списка XML-файлов, которая должна использоваться для создания основного образа для этого обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="26b3a-358">*ксмлпас*: путь к ОФЛ. CAB-файл, который содержит списки XML-файлов.</span><span class="sxs-lookup"><span data-stu-id="26b3a-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="26b3a-359">*млфиле*: имя списка файлов, который должен использоваться для этого обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="26b3a-360">Значение будет равно O365Client_32bit или O365Client_64bit и будет совпадать с Arch.</span><span class="sxs-lookup"><span data-stu-id="26b3a-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="26b3a-361">Следующий URL-адрес — это пример параметра *мореинфаурл* , который ссылается на выпуск обновления клиента Office 365 для 32-разрядной версии Office с версией сборки 16.0.2342.2343 на текущем канале.</span><span class="sxs-lookup"><span data-stu-id="26b3a-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="26b3a-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab— Это расположение списков XML-файлов для этого обновления, в частности, в файле O365Client_32bit. XML в ОФЛ. Архива.</span><span class="sxs-lookup"><span data-stu-id="26b3a-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="26b3a-363">Ветви обновлений для клиента Office 365</span><span class="sxs-lookup"><span data-stu-id="26b3a-363">Office 365 client update channel releases</span></span>](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="26b3a-364">Дополнительные метаданные для автоматизации промежуточного хранения контента</span><span class="sxs-lookup"><span data-stu-id="26b3a-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="26b3a-365">Кроме метаданных, которые публикуются, что определяет, есть ли дополнительные XML-файлы, опубликованные в сети CDN, которые могут помочь предоставить дополнительные сведения о клиентах Office 365, доступных из сети CDN Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="26b3a-366">**Инвентаризационные. ЯЗЫК**</span><span class="sxs-lookup"><span data-stu-id="26b3a-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="26b3a-367">Этот XML-файл находится в подписанном CAB-файле и опубликован в сети CDN Office по следующему URL [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab)-адресу:.</span><span class="sxs-lookup"><span data-stu-id="26b3a-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="26b3a-368">Метаданные, опубликованные в этом XML-файле, удобно использовать для определения того, какие продукты доступны для развертывания и обслуживания из сети CDN Office, а также различные варианты для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="26b3a-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

<span data-ttu-id="26b3a-369">Корневой узел **релеасеинфо\> содержит атрибут публишеддате, который определяет дату публикации этого файла. \<**</span><span class="sxs-lookup"><span data-stu-id="26b3a-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="26b3a-370">**Узел SKU\> определяет индивидуальные единицы \<** хранения.</span><span class="sxs-lookup"><span data-stu-id="26b3a-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="26b3a-371">Атрибут *ProductID* определяет идентификатор, который передается в качестве атрибута ID в файле Configuration. XML при использовании ODT.</span><span class="sxs-lookup"><span data-stu-id="26b3a-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="26b3a-372">Например, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="26b3a-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="26b3a-373">Атрибут *по умолчанию* , если он имеет значение true, определяет рекомендованную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="26b3a-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="26b3a-374">**Узлы приложений\> используются для определения отдельных приложений Office, поддерживаемых каждым \<** SKU.</span><span class="sxs-lookup"><span data-stu-id="26b3a-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="26b3a-375">Атрибут *Name* — это имя отображаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="26b3a-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="26b3a-376">Атрибут *AppID* — это атрибут ID, передаваемый в файле Configuration. XML для \*\* \<узла\> ExcludeApp\*\* при использовании ODT.</span><span class="sxs-lookup"><span data-stu-id="26b3a-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="26b3a-377">Например, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="26b3a-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="26b3a-378">**РЕЛЕАСЕХИСТОРИ. ЯЗЫК**</span><span class="sxs-lookup"><span data-stu-id="26b3a-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="26b3a-379">Этот XML-файл находится в подписанном CAB-файле и опубликован в сети CDN Office в следующем расположении: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span><span class="sxs-lookup"><span data-stu-id="26b3a-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="26b3a-380">Метаданные, опубликованные в этом XML-файле, помогают определить, какие каналы поддерживаются для обслуживания обновлений из сети CDN Office, а также сведения о журнале сборки для каждого поддерживаемого канала.</span><span class="sxs-lookup"><span data-stu-id="26b3a-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

<span data-ttu-id="26b3a-381">Корневой узел \*\* \<релеасехистори\> \*\* содержит атрибут публишеддате, который определяет дату публикации этого файла.</span><span class="sxs-lookup"><span data-stu-id="26b3a-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="26b3a-382">Узел \*\* \<UpdateChannel\> \*\* определяет поддерживаемый канал.</span><span class="sxs-lookup"><span data-stu-id="26b3a-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="26b3a-383">Атрибут *Name* определяет идентификатор канала, который используется для передачи в ODT из файла Configuration. XML в качестве атрибута Channel.</span><span class="sxs-lookup"><span data-stu-id="26b3a-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="26b3a-384">Пример: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="26b3a-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="26b3a-385">Этот атрибут устарел и используется только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="26b3a-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="26b3a-386">Используйте атрибут ID вместо атрибута Name.</span><span class="sxs-lookup"><span data-stu-id="26b3a-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="26b3a-387">Атрибут *ID* определяет идентификатор канала, который используется для передачи в ODT из файла Configuration. XML в качестве атрибута Channel.</span><span class="sxs-lookup"><span data-stu-id="26b3a-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="26b3a-388">Пример: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="26b3a-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="26b3a-389">В качестве отображаемого имени используется атрибут **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="26b3a-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="26b3a-390">Узел \*\* \<Update\> \*\* используется для определения каждого обновления, опубликованного для конкретного канала.</span><span class="sxs-lookup"><span data-stu-id="26b3a-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="26b3a-391">**Последний** атрибут, если он имеет значение true, определяет выпуск, который является последним выпуском для этого канала.</span><span class="sxs-lookup"><span data-stu-id="26b3a-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="26b3a-392">Атрибут **Version** определяет номер версии для этого конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="26b3a-393">Атрибут **легациверсион** определяет полный номер версии для этого конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="26b3a-394">Атрибут **Build** определяет номер сборки для этого конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="26b3a-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="26b3a-395">Атрибут **пубтиме** определяет дату и время публикации этого обновления в сети CDN Office.</span><span class="sxs-lookup"><span data-stu-id="26b3a-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

