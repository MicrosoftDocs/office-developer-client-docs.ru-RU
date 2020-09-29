---
title: Интеграция приложений управления с установщиком Microsoft 365 приложений с помощью командлетов "нажми и работай"
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Сведения о том, как интегрировать установщик приложений Microsoft 365 с помощью решения для управления программным обеспечением.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297316"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="213f3-103">Интеграция приложений управления с установщиком Microsoft 365 приложений с помощью командлетов "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="213f3-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="213f3-104">Сведения о том, как интегрировать установщик приложений Microsoft 365 с помощью решения для управления программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="213f3-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="213f3-105">Установщик приложений Microsoft 365 нажми и работай предоставляет интерфейс COM, который позволяет ИТ-специалистам и решениям управления программным способом управлять управлением обновлениями.</span><span class="sxs-lookup"><span data-stu-id="213f3-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="213f3-106">Этот интерфейс предоставляет дополнительные возможности управления помимо того, что предоставляется средством развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="213f3-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="213f3-107">Эта статья относится к приложениям Office, использующим установщик "нажми и работай".</span><span class="sxs-lookup"><span data-stu-id="213f3-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="213f3-108">Интеграция с "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="213f3-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="213f3-109">Чтобы использовать этот интерфейс, приложение управляемости вызывает COM-интерфейс и вызывает интерфейсы API, напрямую взаимодействующие с службой установки "нажми и работай".</span><span class="sxs-lookup"><span data-stu-id="213f3-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="213f3-110">Установщик Office нажми и работай можно запустить из командной строки с параметрами, которые могут управлять поведением, как описано в разделе [средство развертывания Office для "нажми и работай](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)".</span><span class="sxs-lookup"><span data-stu-id="213f3-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="213f3-111">**Ниже приведена концептуальная схема COM-интерфейса**</span><span class="sxs-lookup"><span data-stu-id="213f3-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="213f3-112">![Схема использования интерфейса COM в установщике Office нажми и работай.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования интерфейса COM в установщике Office "нажми и работай"")</span><span class="sxs-lookup"><span data-stu-id="213f3-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="213f3-113">Установщик приложений Microsoft 365 с поддержкой технологии "нажми и работай" реализует интерфейс на основе COM, **иупдатенотифи** зарегистрированный в CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="213f3-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="213f3-114">Этот интерфейс можно вызвать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="213f3-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="213f3-115">Вызов будет успешным только в том случае, если вызывающий абонент работает с повышенными привилегиями, так как программа установки "нажми и работай" должна выполняться с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="213f3-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="213f3-116">COM-интерфейс **иупдатенотифи** предоставляет три асинхронные функции, ответственные за проверку команд и параметров и выполнение планирования с помощью службы установки "нажми и работай".</span><span class="sxs-lookup"><span data-stu-id="213f3-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="213f3-117">Метод, **Status**, может использоваться для получения сведений о состоянии последней выполненной команды или о состоянии выполняемой в данный момент команды (например, успех, сбой, подробные коды ошибок).</span><span class="sxs-lookup"><span data-stu-id="213f3-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="213f3-118">Во время жизненного цикла служба установки "нажми и работай" может находиться в четырех состояниях, в которых могут вызываться методы **иупдатенотифи** ; Перезагрузка, бездействие, Загрузка и применение.</span><span class="sxs-lookup"><span data-stu-id="213f3-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="213f3-119">**Ниже показана схема конечного автомата COM-интерфейса**</span><span class="sxs-lookup"><span data-stu-id="213f3-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="213f3-120">![Схема состояний для интерфейса COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Схема состояний для интерфейса COM")</span><span class="sxs-lookup"><span data-stu-id="213f3-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="213f3-121">**Перезагрузка**: при загрузке компьютера в случае недоступности службы установки "нажми и работай" происходит определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="213f3-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="213f3-122">Успешный вызов метода status после перезагрузки приведет к возвращению eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="213f3-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="213f3-123">**Бездействие:** Когда установщик "нажми и работай" находится в состоянии простоя, вы можете вызвать:</span><span class="sxs-lookup"><span data-stu-id="213f3-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="213f3-124">**Apply**: установка ранее загруженного контента.</span><span class="sxs-lookup"><span data-stu-id="213f3-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="213f3-125">**Cancel**: возвращает  `0x800000e` , "метод был вызван в непредвиденное время."</span><span class="sxs-lookup"><span data-stu-id="213f3-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="213f3-126">**Download**: Загрузка нового контента в клиент для последующей установки.</span><span class="sxs-lookup"><span data-stu-id="213f3-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="213f3-127">**Status**: возвращает результат последнего выполненного действия или сообщение об ошибке, если действие завершилось с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="213f3-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="213f3-128">Если предыдущее действие отсутствует, возвращается **состояние**  `eUPDATE_UNKNOWN` .</span><span class="sxs-lookup"><span data-stu-id="213f3-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="213f3-129">**Скачивание:** Когда установщик "нажми и работай" находится в состоянии загрузки, вы можете вызвать:</span><span class="sxs-lookup"><span data-stu-id="213f3-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="213f3-130">**Apply**: возвращает **HRESULT** со значением  `0x800000e` "метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="213f3-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="213f3-131">**Отмена**: остановка скачивания и удаление частично загруженного контента.</span><span class="sxs-lookup"><span data-stu-id="213f3-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="213f3-132">**Download**: возвращает **HRESULT** со значением  `0x800000e` "метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="213f3-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="213f3-133">**Status**: возвращает **DOWNLOAD_WIP** , чтобы указать, что выполняется загрузка.</span><span class="sxs-lookup"><span data-stu-id="213f3-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="213f3-134">**Применение:** Когда установщик "нажми и работай" находится в процессе установки ранее загружаемого содержимого:</span><span class="sxs-lookup"><span data-stu-id="213f3-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="213f3-135">**Apply**: возвращает **HRESULT** со значением  `0x800000e` "метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="213f3-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="213f3-136">**Cancel**: возвращает  `0x800000e` , действие Apply не может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="213f3-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="213f3-137">**Download**: возвращает **HRESULT** со значением  `0x800000e` "метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="213f3-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="213f3-138">**Status**: возвращает **APPLY_WIP** , указывающие на то, что выполняется работа.</span><span class="sxs-lookup"><span data-stu-id="213f3-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="213f3-139">Так как OfficeC2RCOM является службой COM+ и динамически загружается, вам необходимо вызвать функцию **CoCreateInstance** при каждом вызове метода для этого класса, чтобы убедиться, что вы получаете ожидаемый результат.</span><span class="sxs-lookup"><span data-stu-id="213f3-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="213f3-140">При необходимости служба COM+ будет обрабатывать создание нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="213f3-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="213f3-141">Когда один из методов вызывается в первый раз, COM+ загрузит объект **иупдатенотифи** и запустит его в одном из экземпляров dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="213f3-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="213f3-142">Новый объект остается активным в течение приблизительно 3 минут.</span><span class="sxs-lookup"><span data-stu-id="213f3-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="213f3-143">Если последующий вызов выполняется через три минуты последнего вызова, объект **иупдатенотифи** останется загруженным, а новый экземпляр не будет создан.</span><span class="sxs-lookup"><span data-stu-id="213f3-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="213f3-144">Если в течение трех минут ничего не происходит, объект Иупдатенотифи будет выгружен, а при следующем вызове будет создан новый объект **иупдатенотифи** .</span><span class="sxs-lookup"><span data-stu-id="213f3-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="213f3-145">Справочное руководство по API-интерфейсу API для установщика "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="213f3-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="213f3-146">В следующей справочной документации по API:</span><span class="sxs-lookup"><span data-stu-id="213f3-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="213f3-147">Параметры представлены в формате "ключ-значение", разделенном пробелом.</span><span class="sxs-lookup"><span data-stu-id="213f3-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="213f3-148">В параметрах регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="213f3-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="213f3-149">Существует [список параметров](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) , доступных в документации.</span><span class="sxs-lookup"><span data-stu-id="213f3-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="213f3-150">Сводка интерфейса IUpdateNotify2 теперь включена.</span><span class="sxs-lookup"><span data-stu-id="213f3-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="213f3-151">Применить</span><span class="sxs-lookup"><span data-stu-id="213f3-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="213f3-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="213f3-152">Parameters</span></span>

-  <span data-ttu-id="213f3-153">_displaylevel_: **true** , чтобы показать состояние установки, включая ошибки, во время процесса обновления; **значение false** , чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="213f3-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="213f3-154">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="213f3-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="213f3-155">_forceappshutdown_: **true** для принудительного завершения работы приложений Office при запуске действия **Apply** ; в противном случае — **false** .</span><span class="sxs-lookup"><span data-stu-id="213f3-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="213f3-156">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="213f3-156">The default is **false**.</span></span> <span data-ttu-id="213f3-157">Дополнительные [сведения см.](#bk_ApplyRemark)</span><span class="sxs-lookup"><span data-stu-id="213f3-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="213f3-158">Если какое-либо приложение Office запускается при запуске действия **Apply** , действие **Применить** обычно завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="213f3-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="213f3-159">Передача  `forceappshutdown=true` в метод **Apply** приведет к тому, что служба **оффицекликкторун** сразу же завершит работу приложений и применит обновление.</span><span class="sxs-lookup"><span data-stu-id="213f3-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="213f3-160">В этом случае в работе пользователя могут возникать потери данных.</span><span class="sxs-lookup"><span data-stu-id="213f3-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="213f3-161">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="213f3-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="213f3-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="213f3-162">**S_OK**</span></span> <br/> |<span data-ttu-id="213f3-163">Действие успешно отправлено службе "нажми и работай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="213f3-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="213f3-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="213f3-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="213f3-165">Вызывающий абонент не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="213f3-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="213f3-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="213f3-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="213f3-167">Переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="213f3-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="213f3-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="213f3-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="213f3-169">В настоящее время действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="213f3-169">Action is not allowed at this time.</span></span> <span data-ttu-id="213f3-170">Дополнительные [сведения см.](#bk_ApplyRemark)</span><span class="sxs-lookup"><span data-stu-id="213f3-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="213f3-171">Примечания</span><span class="sxs-lookup"><span data-stu-id="213f3-171">Remarks</span></span>

- <span data-ttu-id="213f3-172">Если какое-либо приложение Office запускается при запуске действия **Apply** , действие **Apply** завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="213f3-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="213f3-173">`forceappshutdown=true`При передаче в метод **Apply** служба **оффицекликкторун** немедленно завершит работу всех запущенных приложений Office и применить обновление.</span><span class="sxs-lookup"><span data-stu-id="213f3-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="213f3-174">Пользователь может столкнуться с данными, так как они не получают запроса на сохранение изменений в открытых документах...</span><span class="sxs-lookup"><span data-stu-id="213f3-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="213f3-175">Это действие может быть вызвано только в том случае, если состоянием COM является один из следующих:</span><span class="sxs-lookup"><span data-stu-id="213f3-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="213f3-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="213f3-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="213f3-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="213f3-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="213f3-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="213f3-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="213f3-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="213f3-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="213f3-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="213f3-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="213f3-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="213f3-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="213f3-182">При вызове метода **Apply** без предварительной загрузки содержимого метод **Apply** будет сообщать об **успешном** завершении, так как он не обнаружил, что успешно применялся и завершил процесс **применения** .</span><span class="sxs-lookup"><span data-stu-id="213f3-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="213f3-183">Отменить</span><span class="sxs-lookup"><span data-stu-id="213f3-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="213f3-184">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="213f3-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="213f3-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="213f3-185">S_OK</span></span>  <br/> |<span data-ttu-id="213f3-186">Действие успешно отправлено службе "нажми и работай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="213f3-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="213f3-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="213f3-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="213f3-188">В настоящее время действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="213f3-188">Action is not allowed at this time.</span></span> <span data-ttu-id="213f3-189">Для получения дополнительных сведений см раздел ["Примечания](#bk_CancelRemarks) ".</span><span class="sxs-lookup"><span data-stu-id="213f3-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="213f3-190">Примечания</span><span class="sxs-lookup"><span data-stu-id="213f3-190">Remarks</span></span>

- <span data-ttu-id="213f3-191">Этот метод можно запускать только при **eDOWNLOAD_WIP**идентификатора состояния com.</span><span class="sxs-lookup"><span data-stu-id="213f3-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="213f3-192">Будет предпринята попытка отменить текущее действие скачивания.</span><span class="sxs-lookup"><span data-stu-id="213f3-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="213f3-193">Состояние COM изменится на **eDOWNLOAD_CANCELLING** и в конечном итоге изменится на **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="213f3-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="213f3-194">Состояние COM возвращает **E_ILLEGAL_METHOD_CALL** , если триггер запускается в любое другое время.</span><span class="sxs-lookup"><span data-stu-id="213f3-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="213f3-195">Скачать</span><span class="sxs-lookup"><span data-stu-id="213f3-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="213f3-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="213f3-196">Parameters</span></span>

-  <span data-ttu-id="213f3-197">_displaylevel_: **true** , чтобы показать состояние установки, включая ошибки, во время процесса обновления; **значение false** , чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="213f3-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="213f3-198">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="213f3-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="213f3-199">_упдатебасеурл_: URL-адрес альтернативного источника скачивания.</span><span class="sxs-lookup"><span data-stu-id="213f3-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="213f3-200">_упдатетоверсион_: версия для обновления Office.</span><span class="sxs-lookup"><span data-stu-id="213f3-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="213f3-201">Определите этот параметр, если необходимо обновить более старую версию, чем версия, установленная в данный момент.</span><span class="sxs-lookup"><span data-stu-id="213f3-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="213f3-202">_довнлоадсаурце_: CLSID настраиваемой реализации **ИБАККГРАУНДКОПИМАНАЖЕР** (диспетчер BITS).</span><span class="sxs-lookup"><span data-stu-id="213f3-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="213f3-203">Идентификатор _ContentId_: определяет содержимое для загрузки с сервера контента через настраиваемый диспетчер BITS.</span><span class="sxs-lookup"><span data-stu-id="213f3-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="213f3-204">Это значение передается через интерфейс BITS для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="213f3-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="213f3-205">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="213f3-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="213f3-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="213f3-206">**S_OK**</span></span> <br/> |<span data-ttu-id="213f3-207">Действие успешно отправлено службе "нажми и работай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="213f3-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="213f3-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="213f3-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="213f3-209">Вызывающий абонент не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="213f3-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="213f3-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="213f3-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="213f3-211">Переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="213f3-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="213f3-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="213f3-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="213f3-213">В настоящее время действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="213f3-213">Action is not allowed at this time.</span></span> <span data-ttu-id="213f3-214">Дополнительные [сведения см.](#bk_DownloadRemark)</span><span class="sxs-lookup"><span data-stu-id="213f3-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="213f3-215">Примечания</span><span class="sxs-lookup"><span data-stu-id="213f3-215">Remarks</span></span>

- <span data-ttu-id="213f3-216">Необходимо указать  _довнлоадсаурце_ и идентификатор  _ContentId_ в виде связывания.</span><span class="sxs-lookup"><span data-stu-id="213f3-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="213f3-217">В противном случае метод **download** возвратит ошибку **E_INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="213f3-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="213f3-218">Если указаны  _довнлоадсаурце_,  _ContentId_и  _упдатебасеурл_ ,  _упдатебасеурл_ будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="213f3-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="213f3-219">Это действие может быть вызвано только в том случае, если состоянием COM является один из следующих:</span><span class="sxs-lookup"><span data-stu-id="213f3-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="213f3-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="213f3-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="213f3-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="213f3-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="213f3-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="213f3-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="213f3-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="213f3-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="213f3-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="213f3-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="213f3-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="213f3-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="213f3-226">При вызове метода **Apply** без ранее скачанного содержимого метод **Apply** будет сообщать об **успешном** завершении, так как он не обнаружил, что успешно применялся и завершил процесс **применения** .</span><span class="sxs-lookup"><span data-stu-id="213f3-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="213f3-227">Примеры</span><span class="sxs-lookup"><span data-stu-id="213f3-227">Examples</span></span>

- <span data-ttu-id="213f3-228">Чтобы скачать содержимое из настраиваемого диспетчера BITS: вызовите функцию **скачать ()** , передав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="213f3-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="213f3-229">Чтобы скачать содержимое из сети доставки содержимого Office (CDN): вызовите функцию **скачать ()** , не указывая параметры  _довнлоадсаурце_,  _ContentId_или  _упдатебасеурл_ .</span><span class="sxs-lookup"><span data-stu-id="213f3-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="213f3-230">Чтобы скачать содержимое из настраиваемого расположения: вызовите функцию **скачать ()** , передав следующий параметр:</span><span class="sxs-lookup"><span data-stu-id="213f3-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="213f3-231">Статус</span><span class="sxs-lookup"><span data-stu-id="213f3-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="213f3-232">Параметры</span><span class="sxs-lookup"><span data-stu-id="213f3-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="213f3-233">_пупдатестатусрепорт_</span><span class="sxs-lookup"><span data-stu-id="213f3-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="213f3-234">Указатель на структуру UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="213f3-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="213f3-235">Возвращаемые результаты</span><span class="sxs-lookup"><span data-stu-id="213f3-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="213f3-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="213f3-236">**S_OK**</span></span> <br/> |<span data-ttu-id="213f3-237">Метод **Status** всегда возвращает этот результат.</span><span class="sxs-lookup"><span data-stu-id="213f3-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="213f3-238">Проверка  `UPDATE_STATUS_RESULT` структуры на состояние текущего действия.</span><span class="sxs-lookup"><span data-stu-id="213f3-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="213f3-239">Примечания</span><span class="sxs-lookup"><span data-stu-id="213f3-239">Remarks</span></span>

- <span data-ttu-id="213f3-240">В поле Status (состояние)  `UPDATE_STATUS_REPORT` содержится состояние текущего действия.</span><span class="sxs-lookup"><span data-stu-id="213f3-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="213f3-241">Возвращается одно из следующих значений состояния:</span><span class="sxs-lookup"><span data-stu-id="213f3-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="213f3-242">Если последняя команда привела к ошибке, в поле ошибка  `UPDATE_STATUS_REPORT` содержится подробная информация об ошибке.</span><span class="sxs-lookup"><span data-stu-id="213f3-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="213f3-243">В методе **Status** возвращается два типа кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="213f3-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="213f3-244">Если ошибка меньше  `UPDATE_ERROR_CODE::eUNKNOWN` , то ошибка является одним из следующих предварительно определенных кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="213f3-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="213f3-245">Если код ошибки возврата превышает значение  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT** неудачного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="213f3-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="213f3-246">Чтобы извлечь значение HRESULT, вычитаемое  `UPDATE_ERROR_CODE::eUNKNOWN` из значения, которое возвращается в поле "ошибка"  `UPDATE_STATUS_REPORT` .</span><span class="sxs-lookup"><span data-stu-id="213f3-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="213f3-247">Полный список значений состояния и ошибок можно просмотреть, изучив библиотеку типов **иупдатенотифи** , встроенную в OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="213f3-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="213f3-248">Поле ContentId используется для вызовов с **состоянием** после **загрузки** и возвращает идентификатор ContentId, переданный в вызов **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="213f3-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="213f3-249">Рекомендуется инициализировать это поле до **значения NULL** перед вызовом метода **Status** , а затем проверить значение после того, как было возвращено значение **Status** .</span><span class="sxs-lookup"><span data-stu-id="213f3-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="213f3-250">Если значение по-прежнему равно **null**, это означает, что идентификатор ContentId не возвращается.</span><span class="sxs-lookup"><span data-stu-id="213f3-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="213f3-251">Если значение отлично от **null**, его необходимо освободить с помощью вызова **SysFreeString ()**.</span><span class="sxs-lookup"><span data-stu-id="213f3-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="213f3-252">Ниже приведен фрагмент кода, посвященный вызову **состояния** после **загрузки**.</span><span class="sxs-lookup"><span data-stu-id="213f3-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="213f3-253">Сводка по интерфейсу IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="213f3-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="213f3-254">Из версии [16.0.8208.6352] мы добавили новый интерфейс **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="213f3-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="213f3-255">CLSID_UpdateNotifyObject2 {52C2F9C2 — F1AC – 4021 – BF50.756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="213f3-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="213f3-256">Этот интерфейс также размещает исходный интерфейс Иупдатенотифи для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="213f3-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="213f3-257">Это означает, что при использовании этого интерфейса вы можете получить доступ ко всем методам, предоставляемым в интерфейсе **упдатенотифйобжект** .</span><span class="sxs-lookup"><span data-stu-id="213f3-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="213f3-258">Новые методы, добавленные в IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="213f3-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="213f3-259">**HRESULT** Жетблоккингаппс ([выходной] BSTR \* аппслист).</span><span class="sxs-lookup"><span data-stu-id="213f3-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="213f3-260">Получение списка заблокированных приложений для обновления.</span><span class="sxs-lookup"><span data-stu-id="213f3-260">Get updates blocking apps list.</span></span> <span data-ttu-id="213f3-261">Этот вызов возвратит запуск приложений Office, которые будут блокировать процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="213f3-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="213f3-262">**HRESULT** Жетоффицедеплойментдата ([in] int dataType, [in] **значение LPCWSTR** пквсзнаме, [out] BSTR \* оффицедата).</span><span class="sxs-lookup"><span data-stu-id="213f3-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="213f3-263">Получение данных развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="213f3-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="213f3-264">Если вы хотите использовать новые методы, необходимо убедиться в том, что:</span><span class="sxs-lookup"><span data-stu-id="213f3-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="213f3-265">Ваша версия C2R более новая, чем приведенная выше сборка (= с помощью \> построения разветвления за июнь).</span><span class="sxs-lookup"><span data-stu-id="213f3-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="213f3-266">Используйте UpdateNotifyObject2, а не **упдатенотифйобжект** , чтобы вызвать функцию **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="213f3-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="213f3-267">Если вы не используете ни один из новых методов, вам не нужно ничего менять.</span><span class="sxs-lookup"><span data-stu-id="213f3-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="213f3-268">Все существующие методы будут работать точно так же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="213f3-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="213f3-269">Реализация интерфейса BITS</span><span class="sxs-lookup"><span data-stu-id="213f3-269">Implementing the BITS interface</span></span>

<span data-ttu-id="213f3-270">[Фоновая интеллектуальная служба передачи](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) — это служба, предоставляемая корпорацией Майкрософт для передачи файлов между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="213f3-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="213f3-271">BITS это один из каналов, которые может использовать установщик Office нажми и работай для загрузки контента.</span><span class="sxs-lookup"><span data-stu-id="213f3-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="213f3-272">По умолчанию установщик Office 365 Apps нажми и работай использует встроенную в Windows реализацию BITS для загрузки содержимого из сети CDN.</span><span class="sxs-lookup"><span data-stu-id="213f3-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="213f3-273">Предоставляя настраиваемую реализацию BITS методу **Download ()** интерфейса **иупдатенотифи** , программное обеспечение управления может управлять тем, где и как клиент загружает контент.</span><span class="sxs-lookup"><span data-stu-id="213f3-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="213f3-274">Настраиваемый интерфейс BITS полезен при предоставлении настраиваемого канала распространения содержимого, отличного от встроенных каналов "нажми и работай", таких как CDN, серверы IIS или файловые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="213f3-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="213f3-275">Минимальное требование для настраиваемого интерфейса BITS для работы со службой Office C2R:</span><span class="sxs-lookup"><span data-stu-id="213f3-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="213f3-276">Для **ибаккграундкопиманажер**:</span><span class="sxs-lookup"><span data-stu-id="213f3-276">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="213f3-277">Для **ибаккграундкопижоб**:</span><span class="sxs-lookup"><span data-stu-id="213f3-277">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="213f3-278">Для **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="213f3-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="213f3-279">Для  `Addfile` функций и  `AddFileWithRanges` функции and удаленный URL-адрес имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="213f3-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="213f3-280">кмбитс жестко запрограммирована, а обозначает настроенные биты.</span><span class="sxs-lookup"><span data-stu-id="213f3-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="213f3-281">_\<contentid\>_ — Это параметр  _ContentId_ для метода **Download ()** .</span><span class="sxs-lookup"><span data-stu-id="213f3-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="213f3-282">_\<relative path to target file\>_ Указывает расположение и имя файла, который требуется скачать.</span><span class="sxs-lookup"><span data-stu-id="213f3-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="213f3-283">Например, если вы указали объект  _ContentId_  `f732af58-5d86-4299-abe9-7595c35136ef` для метода **Download ()** , и Office C2R хочет скачать CAB-файл версии, например  `v32.cab` File, он вызовите **аддфиле ()** , выполнив следующие  `RemoteUrl` действия:</span><span class="sxs-lookup"><span data-stu-id="213f3-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="213f3-284">Для **ибаккграундкоперрор**:</span><span class="sxs-lookup"><span data-stu-id="213f3-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="213f3-285">Для **ибаккграундкопифиле**:</span><span class="sxs-lookup"><span data-stu-id="213f3-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="213f3-286">Автоматизация промежуточного хранения контента</span><span class="sxs-lookup"><span data-stu-id="213f3-286">Automating content staging</span></span>

<span data-ttu-id="213f3-287">ИТ — администраторы могут разрешить клиентам для настольных ПК автоматически получать обновления, когда они доступны непосредственно из сети CDN, или управлять развертыванием обновлений, доступных в каналах обновления с помощью средства развертывания Office или диспетчера конфигураций конечных точек Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="213f3-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="213f3-288">Служба поддерживает возможность средств управления определять и автоматизировать загрузку контента при наличии обновлений.</span><span class="sxs-lookup"><span data-stu-id="213f3-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="213f3-289">**На следующем рисунке представлен обзор загрузки настраиваемого изображения.**</span><span class="sxs-lookup"><span data-stu-id="213f3-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="213f3-290">![Схема использования интерфейса COM в установщике Office нажми и работай.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования интерфейса COM в установщике Office "нажми и работай"")</span><span class="sxs-lookup"><span data-stu-id="213f3-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="213f3-291">Обзор загрузки настраиваемого изображения</span><span class="sxs-lookup"><span data-stu-id="213f3-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="213f3-292">На предыдущей схеме вы увидите, что новый образ приложений Microsoft 365 доступен в сети CDN.</span><span class="sxs-lookup"><span data-stu-id="213f3-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="213f3-293">Вместе с изображением приложений Microsoft 365 доступен API, который содержит сведения, необходимые для включения программного обеспечения управления для непосредственного создания настраиваемых образов, которые заменяют необходимость использования средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="213f3-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="213f3-294">Предприятие настраивает свои WSUS для синхронизации обновлений приложений Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="213f3-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="213f3-295">Эти обновления не содержат полезных данных изображения, но позволяют программному обеспечению для управления распознать, когда будет доступен новый контент.</span><span class="sxs-lookup"><span data-stu-id="213f3-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="213f3-296">Программное обеспечение для управления может прочитать метаданные обновления приложений Microsoft 365, чтобы узнать, к какой версии Office относится обновление.</span><span class="sxs-lookup"><span data-stu-id="213f3-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="213f3-297">Если обновление возможно, программное обеспечение для управления может использовать содержимое CDN и список файлов для создания настраиваемого образа и сохранения его в расположении общего файлового ресурса, который он использует.</span><span class="sxs-lookup"><span data-stu-id="213f3-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="213f3-298">Использование API списка файлов приложений Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="213f3-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="213f3-299">API списка файлов приложений Microsoft 365 используется для получения имен файлов, необходимых для конкретного обновления приложений Майкрософт 365.</span><span class="sxs-lookup"><span data-stu-id="213f3-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="213f3-300">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="213f3-300">HTTP Request</span></span>

<span data-ttu-id="213f3-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="213f3-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="213f3-302">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="213f3-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="213f3-303">Для вызова этого API не требуется никаких разрешений.</span><span class="sxs-lookup"><span data-stu-id="213f3-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="213f3-304">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="213f3-304">Optional query parameters</span></span>

|<span data-ttu-id="213f3-305">**Имя**</span><span class="sxs-lookup"><span data-stu-id="213f3-305">**Name**</span></span>|<span data-ttu-id="213f3-306">**Описание**</span><span class="sxs-lookup"><span data-stu-id="213f3-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="213f3-307">channel</span><span class="sxs-lookup"><span data-stu-id="213f3-307">channel</span></span> <br/>| <span data-ttu-id="213f3-308">Указывает имя канала</span><span class="sxs-lookup"><span data-stu-id="213f3-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="213f3-309">Необязательный — по умолчанию "полугодовые"</span><span class="sxs-lookup"><span data-stu-id="213f3-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="213f3-310">Поддерживаемые значения https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="213f3-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="213f3-311">version</span><span class="sxs-lookup"><span data-stu-id="213f3-311">version</span></span> <br/>| <span data-ttu-id="213f3-312">Указывает версию обновления</span><span class="sxs-lookup"><span data-stu-id="213f3-312">Specifies the update version</span></span> <br/> <span data-ttu-id="213f3-313">Необязательный параметр — значение по умолчанию для последней версии, доступной для указанного канала</span><span class="sxs-lookup"><span data-stu-id="213f3-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="213f3-314">зубц</span><span class="sxs-lookup"><span data-stu-id="213f3-314">arch</span></span> <br/>| <span data-ttu-id="213f3-315">Определяет архитектуру клиента</span><span class="sxs-lookup"><span data-stu-id="213f3-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="213f3-316">Необязательный параметр — значение по умолчанию: "x64"</span><span class="sxs-lookup"><span data-stu-id="213f3-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="213f3-317">Поддерживаемые значения: x64, x86</span><span class="sxs-lookup"><span data-stu-id="213f3-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="213f3-318">действие</span><span class="sxs-lookup"><span data-stu-id="213f3-318">lid</span></span> <br/>| <span data-ttu-id="213f3-319">Указывает языковые файлы, которые необходимо включить</span><span class="sxs-lookup"><span data-stu-id="213f3-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="213f3-320">Необязательный параметр — значение по умолчанию — None</span><span class="sxs-lookup"><span data-stu-id="213f3-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="213f3-321">Чтобы указать несколько языков, включите параметр запроса на закрышку для каждого языка</span><span class="sxs-lookup"><span data-stu-id="213f3-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="213f3-322">Используйте формат идентификатора языка, например,</span><span class="sxs-lookup"><span data-stu-id="213f3-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="213f3-323">"en $ US", "fr – FR"</span><span class="sxs-lookup"><span data-stu-id="213f3-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="213f3-324">алллангуажес</span><span class="sxs-lookup"><span data-stu-id="213f3-324">alllanguages</span></span> <br/>| <span data-ttu-id="213f3-325">Включение всех языковых файлов</span><span class="sxs-lookup"><span data-stu-id="213f3-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="213f3-326">Необязательный параметр — значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="213f3-326">Optional – defaults to false</span></span> |

<span data-ttu-id="213f3-327">HTTP-ответ</span><span class="sxs-lookup"><span data-stu-id="213f3-327">HTTP Response</span></span>

<span data-ttu-id="213f3-328">В случае успешного выполнения этот метод возвращает код отклика 200 ОК и коллекцию объектов File в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="213f3-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="213f3-329">Чтобы создать изображение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="213f3-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="213f3-330">Вызовите API, предоставив соответствующие параметры запроса для канала, версии и архитектуры интересующего обновления.</span><span class="sxs-lookup"><span data-stu-id="213f3-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="213f3-331">Note: объекты File с атрибутом "LCID": "0" — это независимые от языка файлы, которые должны быть включены в образ.</span><span class="sxs-lookup"><span data-stu-id="213f3-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="213f3-332">Создайте локальное изображение сети CDN, переполнив все объекты File и скопировав файлы CDN, создавая структуру папок в соответствии с атрибутом "Релативепас", определенным для каждого объекта File.</span><span class="sxs-lookup"><span data-stu-id="213f3-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="213f3-333">В следующем примере извлекается список файлов для текущего канала и версия 16.0.4229.1004 для 64 64, а также файлы на французском и английском языках:</span><span class="sxs-lookup"><span data-stu-id="213f3-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="213f3-334">Проверка хэша файлов DAT</span><span class="sxs-lookup"><span data-stu-id="213f3-334">Hash verification of .dat files</span></span>

<span data-ttu-id="213f3-335">Средства создания изображений могут проверить целостность скачанных файлов DAT, сравнив вычисленное значение хэша с заданным хэшем со значением, сопоставленным с каждым из DAT-файлов.</span><span class="sxs-lookup"><span data-stu-id="213f3-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="213f3-336">Ниже приведен пример объекта File, который определяет значения Хашлокатион и Хашалгорисм:</span><span class="sxs-lookup"><span data-stu-id="213f3-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- <span data-ttu-id="213f3-337">Атрибут **хашлокатион** указывает расположение относительного пути CAB-файла, который содержит хэш-значение.</span><span class="sxs-lookup"><span data-stu-id="213f3-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="213f3-338">Создайте расположение хэш-файла с помощью сцепления URL + Релативепас + Хашлокатион.</span><span class="sxs-lookup"><span data-stu-id="213f3-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="213f3-339">В следующем примере расположение stream.x64.bg-bg. hash будет следующим:</span><span class="sxs-lookup"><span data-stu-id="213f3-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="213f3-340">Атрибут **хашалгорисм** указывает, какой алгоритм хеширования использовался.</span><span class="sxs-lookup"><span data-stu-id="213f3-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="213f3-341">Чтобы проверить целостность файла stream.x64.bg-БГ. dat, откройте stream.x64.bg-bg. hash и прочтите хэш-значение, которое является первой строкой текста в хэш-файле.</span><span class="sxs-lookup"><span data-stu-id="213f3-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="213f3-342">Сравните это с вычисленным значением хэша (с использованием указанного алгоритма хеширования), чтобы проверить целостность загруженного файла. dat.</span><span class="sxs-lookup"><span data-stu-id="213f3-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="213f3-343">В следующем примере показан код C# для считывания хеша.</span><span class="sxs-lookup"><span data-stu-id="213f3-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="213f3-344">Обновления для приложений Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="213f3-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="213f3-345">Все обновления для приложений Microsoft 365 опубликованы в [каталоге обновлений Майкрософт](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="213f3-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="213f3-346">Обновления для приложений Microsoft 365 позволяют программному обеспечению программного обеспечения обрабатывать обновления для приложений Microsoft 365 аналогично любому другому обновлению WU с одним исключением; обновления клиента не содержат реальных полезных данных.</span><span class="sxs-lookup"><span data-stu-id="213f3-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="213f3-347">Обновления для приложений Microsoft 365 не должны устанавливаться на всех клиентах, а использовать для запуска рабочих процессов с программным обеспечением с программным обеспечением, заменив команду установки на механизм установки на основе COM, показанный выше.</span><span class="sxs-lookup"><span data-stu-id="213f3-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="213f3-348">**На следующем рисунке показана схема рабочего процесса обновления клиента Office 365.**</span><span class="sxs-lookup"><span data-stu-id="213f3-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="213f3-349">![Схема рабочего процесса для обновлений клиента O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Схема рабочего процесса для обновлений клиента O365PP")</span><span class="sxs-lookup"><span data-stu-id="213f3-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="213f3-350">Каждое публикуемое обновление приложений Microsoft 365 содержит метаданные об обновлении.</span><span class="sxs-lookup"><span data-stu-id="213f3-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="213f3-351">Эти метаданные содержат параметр с именем Мореинфаурл, который можно использовать для получения вызова API списка файлов для этого конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="213f3-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="213f3-352">В следующем примере API списка файлов внедряется в Мореинфаурл и начинается с "Сервицепас ="</span><span class="sxs-lookup"><span data-stu-id="213f3-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="213f3-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& Сервицепас =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="213f3-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="213f3-354">Дополнительные метаданные для автоматизации промежуточного хранения контента</span><span class="sxs-lookup"><span data-stu-id="213f3-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="213f3-355">**API истории выпуска**</span><span class="sxs-lookup"><span data-stu-id="213f3-355">**Release History API**</span></span>
  
<span data-ttu-id="213f3-356">API истории выпуска приложений Microsoft 365 используется для получения сведений о каждом обновлении, опубликованном в сети CDN, вместе с именами каналов и другими атрибутами канала.</span><span class="sxs-lookup"><span data-stu-id="213f3-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="213f3-357">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="213f3-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="213f3-358">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="213f3-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="213f3-359">Для вызова этого API не требуется никаких разрешений.</span><span class="sxs-lookup"><span data-stu-id="213f3-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="213f3-360">HTTP-ответ</span><span class="sxs-lookup"><span data-stu-id="213f3-360">HTTP Response</span></span>

<span data-ttu-id="213f3-361">В случае успешного выполнения этот метод возвращает код отклика 200 ОК и коллекцию объектов File в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="213f3-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="213f3-362">**API SKU**</span><span class="sxs-lookup"><span data-stu-id="213f3-362">**SKUs API**</span></span>
  
<span data-ttu-id="213f3-363">API SKU возвращает сведения, которые помогут определить, какие продукты доступны для развертывания и обслуживания из сети CDN Office, а также различные варианты для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="213f3-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="213f3-364">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="213f3-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="213f3-365">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="213f3-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="213f3-366">Для вызова этого API не требуется никаких разрешений.</span><span class="sxs-lookup"><span data-stu-id="213f3-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="213f3-367">HTTP-ответ</span><span class="sxs-lookup"><span data-stu-id="213f3-367">HTTP Response</span></span>

<span data-ttu-id="213f3-368">В случае успешного выполнения этот метод возвращает код отклика 200 ОК и коллекцию объектов File в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="213f3-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
