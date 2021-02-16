---
title: Интеграция приложений управляемости с установщиком приложений Microsoft 365 "нажми и запускай"
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Узнайте, как интегрировать установщик приложений Microsoft 365 "нажми и запускай" с решением для управления программным обеспечением.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297316"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="1099c-103">Интеграция приложений для управления с установщиком приложений Microsoft 365 "нажми и запускай"</span><span class="sxs-lookup"><span data-stu-id="1099c-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="1099c-104">Узнайте, как интегрировать установщик приложений Microsoft 365 "нажми и запускай" с решением для управления программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="1099c-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="1099c-105">Установщик приложений Microsoft 365 "нажми и запускай" предоставляет интерфейс COM, который позволяет ИТ-специалистам и решениям для управления программным обеспечением управлять управлением обновлениями.</span><span class="sxs-lookup"><span data-stu-id="1099c-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="1099c-106">Этот интерфейс предоставляет дополнительные возможности управления помимо возможностей, предоставляемых средством развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="1099c-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1099c-107">Эта статья относится к приложениям Office, которые используют установщик "нажми и нажми и выйми".</span><span class="sxs-lookup"><span data-stu-id="1099c-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="1099c-108">Интеграция с технологией "нажми и запускай"</span><span class="sxs-lookup"><span data-stu-id="1099c-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="1099c-109">Чтобы использовать этот интерфейс, приложение управляемости вызывает интерфейс COM и вызывает открытые API, которые взаимодействуют непосредственно со службой установки "нажми ижми и запускай".</span><span class="sxs-lookup"><span data-stu-id="1099c-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1099c-110">Установщик Office "нажми и запускай" можно запустить из командной строки с параметрами, которые могут управлять поведением, как описано в средстве развертывания Office для "нажми и нажми [и запускай".](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)</span><span class="sxs-lookup"><span data-stu-id="1099c-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="1099c-111">**Ниже приведена концептуальная схема интерфейса COM**</span><span class="sxs-lookup"><span data-stu-id="1099c-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="1099c-112">![Схема использования интерфейса COM в установщике Office нажми и работай.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования com-интерфейса в установщике office "нажми и нажми"")</span><span class="sxs-lookup"><span data-stu-id="1099c-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="1099c-113">Установщик приложений Microsoft 365 "нажми и запускай" реализует интерфейс на основе **COM, IUpdateNotify,** зарегистрированный в CLSID **CLSID_UpdateNotifyObject.**</span><span class="sxs-lookup"><span data-stu-id="1099c-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="1099c-114">Этот интерфейс можно вызвать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1099c-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="1099c-115">Вызов будет успешным только в том случае, если вызываемая программа работает с повышенными привилегиями, так как программа установки "нажми ижми и нажми ий" должна быть запущена с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="1099c-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="1099c-116">Com-интерфейс **IUpdateNotify** предоставляет три асинхронные функции, отвечающие за проверку команд и параметров и планирование выполнения с помощью службы установки "нажми и выполнив".</span><span class="sxs-lookup"><span data-stu-id="1099c-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="1099c-117">С помощью метода **Status** можно получить сведения о состоянии последней выполненной команды или состоянии исполняемой команды (например, об успешном выполнении, сбое, подробных кодах ошибок).</span><span class="sxs-lookup"><span data-stu-id="1099c-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="1099c-118">В течение жизненного цикла службы установки "нажми и выполнив" может быть четыре состояния, во время которых могут быть вызваны методы **IUpdateNotify;** Перезагрузка, бездействие, загрузка и применение.</span><span class="sxs-lookup"><span data-stu-id="1099c-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="1099c-119">**Ниже приведена схема автомата интерфейса COM**</span><span class="sxs-lookup"><span data-stu-id="1099c-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="1099c-120">![Схема состояний для интерфейса COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Схема состояния для интерфейса COM")</span><span class="sxs-lookup"><span data-stu-id="1099c-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="1099c-121">**Перезагрузка:** когда компьютер загружается, в течение некоторого времени служба установщика "нажми и запускай" недоступна.</span><span class="sxs-lookup"><span data-stu-id="1099c-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="1099c-122">Успешный вызов метода Status после перезагрузки возвращает eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="1099c-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="1099c-123">**Бездействие:** Когда установщик "нажми и запускай" находится в состоянии простоя, можно вызвать:</span><span class="sxs-lookup"><span data-stu-id="1099c-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="1099c-124">**Apply**: Install previously downloaded content.</span><span class="sxs-lookup"><span data-stu-id="1099c-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="1099c-125">**Cancel**: returns  `0x800000e` , "A method was called at an unexpected time".</span><span class="sxs-lookup"><span data-stu-id="1099c-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="1099c-126">**Download**: Downloads new content to the client for later installation.</span><span class="sxs-lookup"><span data-stu-id="1099c-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="1099c-127">**Status**: возвращает результат последнего выполненного действия или сообщение об ошибке, если действие завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="1099c-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="1099c-128">Если предыдущее действие не было, **возвращается**  `eUPDATE_UNKNOWN` состояние.</span><span class="sxs-lookup"><span data-stu-id="1099c-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="1099c-129">**Загрузка:** Когда установщик "нажми и запускай" находится в состоянии скачивания, вы можете вызвать:</span><span class="sxs-lookup"><span data-stu-id="1099c-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="1099c-130">**Apply**: возвращает **HRESULT** со значением  `0x800000e` "Метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="1099c-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="1099c-131">**Отмена:** останавливает скачивание и удаляет частично загруженное содержимое.</span><span class="sxs-lookup"><span data-stu-id="1099c-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="1099c-132">**Download**: Returns an **HRESULT** with the value  `0x800000e` , "A method was called at an unexpected time".</span><span class="sxs-lookup"><span data-stu-id="1099c-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="1099c-133">**Состояние:** возвращает **DOWNLOAD_WIP,** чтобы указать, что загрузка уже идет.</span><span class="sxs-lookup"><span data-stu-id="1099c-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="1099c-134">**Применение:** Когда установщик "нажми ижми и запускай" устанавливает ранее скачиваемые материалы:</span><span class="sxs-lookup"><span data-stu-id="1099c-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="1099c-135">**Apply**: возвращает **HRESULT** со значением  `0x800000e` "Метод был вызван в непредвиденное время".</span><span class="sxs-lookup"><span data-stu-id="1099c-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="1099c-136">**Cancel**: Returns  `0x800000e` , the Apply action cannot be canceled.</span><span class="sxs-lookup"><span data-stu-id="1099c-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="1099c-137">**Download**: Returns an **HRESULT** with the value  `0x800000e` , "A method was called at an unexpected time".</span><span class="sxs-lookup"><span data-stu-id="1099c-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="1099c-138">**Status**: возвращает **APPLY_WIP,** чтобы указать, что идет применение работы.</span><span class="sxs-lookup"><span data-stu-id="1099c-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1099c-139">Так как OfficeC2RCOM — это служба COM+ и динамически загружается, необходимо вызывать **CoCreateInstance** каждый раз при вызове метода для этого класса, чтобы получить ожидаемый результат.</span><span class="sxs-lookup"><span data-stu-id="1099c-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="1099c-140">При необходимости служба COM+ будет обрабатывать создание нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1099c-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="1099c-141">Когда один из методов будет вызван в первый раз, COM+ загрузит объект **IUpdateNotify** и запустит его в одном из dllhost.exe экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1099c-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="1099c-142">Новый объект будет оставаться активным около 3 минут в бездействии.</span><span class="sxs-lookup"><span data-stu-id="1099c-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="1099c-143">Если последующий вызов будет выполнен в течение трех минут после последнего вызова, объект **IUpdateNotify** останется загруженным, а новый экземпляр не будет создан.</span><span class="sxs-lookup"><span data-stu-id="1099c-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="1099c-144">Если вызов не будет выполнен в течение трех минут, объект IUpdateNotify будет выгружен, и при следующем вызове будет создан новый объект **IUpdateNotify.**</span><span class="sxs-lookup"><span data-stu-id="1099c-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="1099c-145">Справочник по API COM установщика "нажми ижми и запускай"</span><span class="sxs-lookup"><span data-stu-id="1099c-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="1099c-146">В следующей справочной документации по API:</span><span class="sxs-lookup"><span data-stu-id="1099c-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="1099c-147">Параметры имеют формат пары "ключ-значение", разделенный пробелом.</span><span class="sxs-lookup"><span data-stu-id="1099c-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="1099c-148">Параметры не чувствительны к делу.</span><span class="sxs-lookup"><span data-stu-id="1099c-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="1099c-149">Существует список [параметров с](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) доступной документацией.</span><span class="sxs-lookup"><span data-stu-id="1099c-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="1099c-150">Теперь включается сводка интерфейса IUpdateNotify2.</span><span class="sxs-lookup"><span data-stu-id="1099c-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="1099c-151">Применить</span><span class="sxs-lookup"><span data-stu-id="1099c-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="1099c-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="1099c-152">Parameters</span></span>

-  <span data-ttu-id="1099c-153">_displaylevel_: **true,** чтобы показать состояние установки, включая ошибки, во время процесса обновления; **false,** чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="1099c-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="1099c-154">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="1099c-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="1099c-155">_forceappshutdown_: **true,** чтобы принудительно отключить приложения Office сразу после запуска действия **Apply;** **false** для сбой, если запущены какие-либо приложения Office.</span><span class="sxs-lookup"><span data-stu-id="1099c-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="1099c-156">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="1099c-156">The default is **false**.</span></span> <span data-ttu-id="1099c-157">Дополнительные [сведения см.](#bk_ApplyRemark) в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="1099c-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="1099c-158">Если при запуске действия **Apply** запущено любое приложение Office, действие **Apply** обычно не будет работать.</span><span class="sxs-lookup"><span data-stu-id="1099c-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="1099c-159">При передаче в метод Apply служба `forceappshutdown=true` **OfficeClickToRun** немедленно закрывает приложения и применяет обновление. </span><span class="sxs-lookup"><span data-stu-id="1099c-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="1099c-160">В этом случае у пользователя может возникнуть потеря данных.</span><span class="sxs-lookup"><span data-stu-id="1099c-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="1099c-161">Возврат результатов</span><span class="sxs-lookup"><span data-stu-id="1099c-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1099c-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="1099c-162">**S_OK**</span></span> <br/> |<span data-ttu-id="1099c-163">Действие успешно отправлено в службу "Нажми и запускай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="1099c-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="1099c-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="1099c-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="1099c-165">Вызываемая не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="1099c-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="1099c-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="1099c-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="1099c-167">Переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="1099c-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="1099c-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="1099c-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="1099c-169">Действие в настоящее время запрещено.</span><span class="sxs-lookup"><span data-stu-id="1099c-169">Action is not allowed at this time.</span></span> <span data-ttu-id="1099c-170">Дополнительные [сведения см.](#bk_ApplyRemark) в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="1099c-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="1099c-171">Примечания</span><span class="sxs-lookup"><span data-stu-id="1099c-171">Remarks</span></span>

- <span data-ttu-id="1099c-172">Если при запуске действия **Apply** запущено любое приложение Office, действие **Apply** не будет работать.</span><span class="sxs-lookup"><span data-stu-id="1099c-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="1099c-173">При передаче в метод Apply служба `forceappshutdown=true` **OfficeClickToRun** немедленно отключает все запущенные приложения Office и применяет обновление. </span><span class="sxs-lookup"><span data-stu-id="1099c-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="1099c-174">У пользователя могут возникнуть данные, так как им не будет предложено сохранить изменения для открытия документов.</span><span class="sxs-lookup"><span data-stu-id="1099c-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="1099c-175">Это действие может быть инициировано только в том случае, если состояние COM имеет одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1099c-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="1099c-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="1099c-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="1099c-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="1099c-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="1099c-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="1099c-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="1099c-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="1099c-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="1099c-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="1099c-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="1099c-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="1099c-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="1099c-182">Если вызвать метод **Apply** без предварительной загрузки содержимого, метод **Apply** будет сообщать об успешном результате, так как он не обнаружил ничего для применения и успешно завершил процесс **применения.** </span><span class="sxs-lookup"><span data-stu-id="1099c-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="1099c-183">"Отмена"</span><span class="sxs-lookup"><span data-stu-id="1099c-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="1099c-184">Возврат результатов</span><span class="sxs-lookup"><span data-stu-id="1099c-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1099c-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="1099c-185">S_OK</span></span>  <br/> |<span data-ttu-id="1099c-186">Действие успешно отправлено в службу "нажми и запускай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="1099c-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="1099c-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="1099c-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="1099c-188">Действие в настоящее время запрещено.</span><span class="sxs-lookup"><span data-stu-id="1099c-188">Action is not allowed at this time.</span></span> <span data-ttu-id="1099c-189">Дополнительные [сведения см.](#bk_CancelRemarks) в разделе "Замечания"</span><span class="sxs-lookup"><span data-stu-id="1099c-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="1099c-190">Примечания</span><span class="sxs-lookup"><span data-stu-id="1099c-190">Remarks</span></span>

- <span data-ttu-id="1099c-191">Этот метод может запускаться только при eDOWNLOAD_WIP **состояния** COM.</span><span class="sxs-lookup"><span data-stu-id="1099c-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="1099c-192">Он попытается отменить текущее действие загрузки.</span><span class="sxs-lookup"><span data-stu-id="1099c-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="1099c-193">Состояние COM изменится на **eDOWNLOAD_CANCELLING** и в конечном итоге изменится на **eDOWNLOAD_CANCELED.**</span><span class="sxs-lookup"><span data-stu-id="1099c-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="1099c-194">Состояние COM возвращает **E_ILLEGAL_METHOD_CALL,** если он активируется в любое другое время.</span><span class="sxs-lookup"><span data-stu-id="1099c-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="1099c-195">Скачать</span><span class="sxs-lookup"><span data-stu-id="1099c-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="1099c-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="1099c-196">Parameters</span></span>

-  <span data-ttu-id="1099c-197">_displaylevel_: **true,** чтобы показать состояние установки, включая ошибки, во время процесса обновления; **false,** чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="1099c-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="1099c-198">Значение по умолчанию: **false**.</span><span class="sxs-lookup"><span data-stu-id="1099c-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="1099c-199">_updatebaseurl_: URL-адрес альтернативного источника загрузки.</span><span class="sxs-lookup"><span data-stu-id="1099c-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="1099c-200">_updatetoversion_: версия для обновления Office.</span><span class="sxs-lookup"><span data-stu-id="1099c-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="1099c-201">Определите этот параметр, если вы хотите обновить более старую версию, чем установленная в данный момент версия.</span><span class="sxs-lookup"><span data-stu-id="1099c-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="1099c-202">_downloadsource_: CLSID настраиваемой реализации **IBackgroundCopyManager** (диспетчер BITS).</span><span class="sxs-lookup"><span data-stu-id="1099c-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="1099c-203">_contentid_: определяет содержимое, которое необходимо скачать с сервера контента с помощью настроенного диспетчера BITS.</span><span class="sxs-lookup"><span data-stu-id="1099c-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="1099c-204">Это значение передается через интерфейс BITS для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="1099c-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="1099c-205">Возврат результатов</span><span class="sxs-lookup"><span data-stu-id="1099c-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1099c-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="1099c-206">**S_OK**</span></span> <br/> |<span data-ttu-id="1099c-207">Действие успешно отправлено в службу "Нажми и запускай" для выполнения.</span><span class="sxs-lookup"><span data-stu-id="1099c-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="1099c-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="1099c-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="1099c-209">Вызываемая не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="1099c-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="1099c-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="1099c-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="1099c-211">Переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="1099c-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="1099c-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="1099c-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="1099c-213">Действие в настоящее время запрещено.</span><span class="sxs-lookup"><span data-stu-id="1099c-213">Action is not allowed at this time.</span></span> <span data-ttu-id="1099c-214">Дополнительные [сведения см.](#bk_DownloadRemark) в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="1099c-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="1099c-215">Примечания</span><span class="sxs-lookup"><span data-stu-id="1099c-215">Remarks</span></span>

- <span data-ttu-id="1099c-216">В качестве пары необходимо указать _downloadsource_ и _contentid._</span><span class="sxs-lookup"><span data-stu-id="1099c-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="1099c-217">В этом случае метод **download** возвращает ошибку E_INVALIDARG **ошибке.**</span><span class="sxs-lookup"><span data-stu-id="1099c-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="1099c-218">Если  _предоставлены downloadsource,_  _contentid_ и  _updatebaseurl,_  _updatebaseurl_ будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="1099c-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="1099c-219">Это действие может быть инициировано только в том случае, если состояние COM имеет одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1099c-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="1099c-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="1099c-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="1099c-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="1099c-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="1099c-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="1099c-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="1099c-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="1099c-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="1099c-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="1099c-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="1099c-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="1099c-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="1099c-226">Если вызвать метод **Apply** без ранее загруженного содержимого, метод **Apply** будет сообщать об успешном результате, так как он не обнаружил ничего для применения и успешно завершил процесс **применения.** </span><span class="sxs-lookup"><span data-stu-id="1099c-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="1099c-227">Примеры</span><span class="sxs-lookup"><span data-stu-id="1099c-227">Examples</span></span>

- <span data-ttu-id="1099c-228">Чтобы скачать содержимое из настроенного диспетчера BITS, вызовите функцию **download(),** передав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1099c-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="1099c-229">Чтобы скачать содержимое из сети доставки содержимого Office (CDN): вызовите функцию **download()** без указания параметров _downloadsource,_ _contentid_ или _updatebaseurl._</span><span class="sxs-lookup"><span data-stu-id="1099c-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="1099c-230">Чтобы скачать содержимое из настраиваемой области, вызовите функцию **download(),** передав следующий параметр:</span><span class="sxs-lookup"><span data-stu-id="1099c-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="1099c-231">Состояние</span><span class="sxs-lookup"><span data-stu-id="1099c-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="1099c-232">Параметры</span><span class="sxs-lookup"><span data-stu-id="1099c-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="1099c-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="1099c-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="1099c-234">Указатель на UPDATE_STATUS_REPORT структуру.</span><span class="sxs-lookup"><span data-stu-id="1099c-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="1099c-235">Возврат результатов</span><span class="sxs-lookup"><span data-stu-id="1099c-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1099c-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="1099c-236">**S_OK**</span></span> <br/> |<span data-ttu-id="1099c-237">Метод **Status** всегда возвращает этот результат.</span><span class="sxs-lookup"><span data-stu-id="1099c-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="1099c-238">Проверьте  `UPDATE_STATUS_RESULT` структуру на состояние текущего действия.</span><span class="sxs-lookup"><span data-stu-id="1099c-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="1099c-239">Примечания</span><span class="sxs-lookup"><span data-stu-id="1099c-239">Remarks</span></span>

- <span data-ttu-id="1099c-240">Поле состояния содержит  `UPDATE_STATUS_REPORT` состояние текущего действия.</span><span class="sxs-lookup"><span data-stu-id="1099c-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="1099c-241">Возвращается одно из следующих значений состояния:</span><span class="sxs-lookup"><span data-stu-id="1099c-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="1099c-242">Если последняя команда приводит к ошибке, поле ошибки содержит  `UPDATE_STATUS_REPORT` подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1099c-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="1099c-243">Из метода Status возвращаются два типа кодов **ошибок.**</span><span class="sxs-lookup"><span data-stu-id="1099c-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="1099c-244">Если ошибка меньше, ошибка является одним из следующих  `UPDATE_ERROR_CODE::eUNKNOWN` предопределеных кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="1099c-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="1099c-245">Если код возвращаемой ошибки превышает  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT** неудачного вызова функции.</span><span class="sxs-lookup"><span data-stu-id="1099c-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="1099c-246">Извлечение вычитания HRESULT из значения, возвращаемого в поле  `UPDATE_ERROR_CODE::eUNKNOWN` ошибки  `UPDATE_STATUS_REPORT` .</span><span class="sxs-lookup"><span data-stu-id="1099c-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="1099c-247">Полный список значений состояния и ошибок можно просмотреть, проверив библиотеку типов **IUpdateNotify,** внедренную в OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="1099c-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="1099c-248">Поле contentid используется для  вызовов  состояния после инициалов загрузки и возвращает contentid, переданный в вызов **загрузки.**</span><span class="sxs-lookup"><span data-stu-id="1099c-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="1099c-249">Перед вызовом метода **Status** лучше всего инициализировать это поле в  значение **NULL,** а затем проверить значение после возврата состояния.</span><span class="sxs-lookup"><span data-stu-id="1099c-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="1099c-250">Если значение по-прежнему равно **null,** это означает, что не возвращается contentid.</span><span class="sxs-lookup"><span data-stu-id="1099c-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="1099c-251">Если значение не **null,** необходимо освободить его с помощью вызова **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="1099c-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="1099c-252">Вот фрагмент кода о вызове **состояния** после **скачивания.**</span><span class="sxs-lookup"><span data-stu-id="1099c-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="1099c-253">Сводка интерфейса IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="1099c-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="1099c-254">В версии [16.0.8208.6352] мы добавили новый **интерфейс IUpdateNotify2.**</span><span class="sxs-lookup"><span data-stu-id="1099c-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="1099c-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="1099c-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="1099c-256">В этом интерфейсе также был исходного интерфейса IUpdateNotify для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="1099c-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="1099c-257">Это означает, что при использовании этого интерфейса у вас есть доступ ко всем методам, предоставляемым в **интерфейсе UpdateNotifyObject.**</span><span class="sxs-lookup"><span data-stu-id="1099c-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="1099c-258">Новые методы, добавленные в IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="1099c-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="1099c-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="1099c-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="1099c-260">Получать обновления, блокирующие список приложений.</span><span class="sxs-lookup"><span data-stu-id="1099c-260">Get updates blocking apps list.</span></span> <span data-ttu-id="1099c-261">Этот вызов возвратит запущенные приложения Office, которые заблокируют процесс обновления.</span><span class="sxs-lookup"><span data-stu-id="1099c-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="1099c-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="1099c-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="1099c-263">Получите данные о развертывании Office.</span><span class="sxs-lookup"><span data-stu-id="1099c-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="1099c-264">Если вы хотите использовать новые методы, убедитесь, что:</span><span class="sxs-lookup"><span data-stu-id="1099c-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="1099c-265">Ваша версия C2R новее, чем сборка выше ( \> = июньская сборка ветвей).</span><span class="sxs-lookup"><span data-stu-id="1099c-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="1099c-266">Используйте UpdateNotifyObject2 вместо **UpdateNotifyObject** для вызова **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="1099c-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="1099c-267">Если вы не используете ни один из новых методов, вам не нужно ничего менять.</span><span class="sxs-lookup"><span data-stu-id="1099c-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="1099c-268">Все существующие методы будут работать точно так же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="1099c-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="1099c-269">Реализация интерфейса BITS</span><span class="sxs-lookup"><span data-stu-id="1099c-269">Implementing the BITS interface</span></span>

<span data-ttu-id="1099c-270">Служба [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) — это служба, предоставляемая корпорацией Майкрософт для передачи файлов между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1099c-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="1099c-271">BITS — это один из каналов, которые установщик office "нажми и запуск" может использовать для скачивания содержимого.</span><span class="sxs-lookup"><span data-stu-id="1099c-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="1099c-272">По умолчанию установщик приложений Microsoft 365 "нажми и запускай" использует встроенную в Windows реализацию BITS для скачивания содержимого из CDN.</span><span class="sxs-lookup"><span data-stu-id="1099c-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="1099c-273">Предоставляя настраиваемую реализацию BITS методу **загрузки ()** интерфейса **IUpdateNotify,** ваше программное обеспечение управляемости может контролировать, где и как клиент загружает содержимое.</span><span class="sxs-lookup"><span data-stu-id="1099c-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="1099c-274">Настраиваемый интерфейс BITS полезен при предоставлении настраиваемого канала распространения содержимого, кроме встроенных каналов "нажми и запускай", таких как СЕТЬ CDN, серверы IIS или файловые папки.</span><span class="sxs-lookup"><span data-stu-id="1099c-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="1099c-275">Минимальное требование к пользовательскому интерфейсу BITS для работы со службой Office C2R:</span><span class="sxs-lookup"><span data-stu-id="1099c-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="1099c-276">Для **IBackgroundCopyManager:**</span><span class="sxs-lookup"><span data-stu-id="1099c-276">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="1099c-277">Для **IBackgroundCopyJob:**</span><span class="sxs-lookup"><span data-stu-id="1099c-277">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="1099c-278">Для **IBackgroundCopyJob3:**</span><span class="sxs-lookup"><span data-stu-id="1099c-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="1099c-279">Для  `Addfile`  `AddFileWithRanges` функций удаленный URL-адрес имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="1099c-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="1099c-280">cmbits жестко закодировать и означает настраиваемые BITS.</span><span class="sxs-lookup"><span data-stu-id="1099c-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="1099c-281">_\<contentid\>_ является _параметром contentid_ для метода **Download().**</span><span class="sxs-lookup"><span data-stu-id="1099c-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="1099c-282">_\<relative path to target file\>_ предоставляет расположение и имя файла для скачивания.</span><span class="sxs-lookup"><span data-stu-id="1099c-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="1099c-283">Например, если вы предоставили _contentid_ метода Download(), а Office C2R хочет скачать CAB-файл версии, например файл, он будет вызывать `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** со следующими данными: `RemoteUrl`</span><span class="sxs-lookup"><span data-stu-id="1099c-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="1099c-284">Для **IBackgroundCopyError:**</span><span class="sxs-lookup"><span data-stu-id="1099c-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="1099c-285">Для **IBackgroundCopyFile:**</span><span class="sxs-lookup"><span data-stu-id="1099c-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="1099c-286">Автоматизация промежуточного содержимого</span><span class="sxs-lookup"><span data-stu-id="1099c-286">Automating content staging</span></span>

<span data-ttu-id="1099c-287">ИТ-администраторы могут включить для классических клиентов автоматическое получение обновлений, когда они доступны непосредственно из СЕТИ CDN, или управлять развертыванием обновлений, доступных из каналов обновления, с помощью средства развертывания Office или Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1099c-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="1099c-288">Служба поддерживает возможность средств управления распознавать и автоматизировать загрузку содержимого при наличии доступных обновлений.</span><span class="sxs-lookup"><span data-stu-id="1099c-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="1099c-289">**На следующем изображении представлен обзор загрузки пользовательского образа**</span><span class="sxs-lookup"><span data-stu-id="1099c-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="1099c-290">![Схема использования интерфейса COM в установщике Office нажми и работай.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования com-интерфейса в установщике office "нажми и нажми"")</span><span class="sxs-lookup"><span data-stu-id="1099c-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="1099c-291">Обзор загрузки пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="1099c-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="1099c-292">На предыдущей схеме видно, что в CDN доступен новый образ приложений Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1099c-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="1099c-293">Наряду с изображением приложений Microsoft 365 доступен API, который включает сведения, необходимые для обеспечения управляемости программного обеспечения для непосредственного создания настраиваемых образов, заменяющих необходимость использования средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="1099c-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="1099c-294">Предприятие настраивает службы WSUS для синхронизации обновлений приложений Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1099c-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="1099c-295">Эти обновления не содержат фактических полезной нагрузки изображения, но позволяют программному обеспечению управляемости распознавать доступность нового содержимого.</span><span class="sxs-lookup"><span data-stu-id="1099c-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="1099c-296">Затем программное обеспечение для управления может прочитать метаданные Обновления приложений Microsoft 365, чтобы понять, к какой версии Office применяется обновление.</span><span class="sxs-lookup"><span data-stu-id="1099c-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="1099c-297">Если обновление применимо, программное обеспечение для управления может использовать содержимое CDN и список файлов для создания пользовательского образа и его хранения в расположении файлового папки, которое оно настроено для использования.</span><span class="sxs-lookup"><span data-stu-id="1099c-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="1099c-298">Использование API списка файлов приложений Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1099c-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="1099c-299">API списка файлов приложений Microsoft 365 используется для получения имен файлов, необходимых для конкретного обновления приложений Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1099c-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="1099c-300">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="1099c-300">HTTP Request</span></span>

<span data-ttu-id="1099c-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="1099c-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="1099c-302">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="1099c-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="1099c-303">Для вызова этого API не требуются разрешения.</span><span class="sxs-lookup"><span data-stu-id="1099c-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="1099c-304">Необязательные параметры запросов</span><span class="sxs-lookup"><span data-stu-id="1099c-304">Optional query parameters</span></span>

|<span data-ttu-id="1099c-305">**Название**</span><span class="sxs-lookup"><span data-stu-id="1099c-305">**Name**</span></span>|<span data-ttu-id="1099c-306">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1099c-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1099c-307">channel</span><span class="sxs-lookup"><span data-stu-id="1099c-307">channel</span></span> <br/>| <span data-ttu-id="1099c-308">Указывает имя канала</span><span class="sxs-lookup"><span data-stu-id="1099c-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="1099c-309">Необязательный — значение по умолчанию " SemiAnnual"</span><span class="sxs-lookup"><span data-stu-id="1099c-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="1099c-310">Поддерживаемые значения https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="1099c-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="1099c-311">version</span><span class="sxs-lookup"><span data-stu-id="1099c-311">version</span></span> <br/>| <span data-ttu-id="1099c-312">Указывает версию обновления</span><span class="sxs-lookup"><span data-stu-id="1099c-312">Specifies the update version</span></span> <br/> <span data-ttu-id="1099c-313">Необязательный — по умолчанию установлена последняя версия, доступная для указанного канала</span><span class="sxs-lookup"><span data-stu-id="1099c-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="1099c-314">arch</span><span class="sxs-lookup"><span data-stu-id="1099c-314">arch</span></span> <br/>| <span data-ttu-id="1099c-315">Указывает архитектуру клиента</span><span class="sxs-lookup"><span data-stu-id="1099c-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="1099c-316">Необязательный — значение по умолчанию — "x64"</span><span class="sxs-lookup"><span data-stu-id="1099c-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="1099c-317">Поддерживаемые значения: x64, x86</span><span class="sxs-lookup"><span data-stu-id="1099c-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="1099c-318">крышка</span><span class="sxs-lookup"><span data-stu-id="1099c-318">lid</span></span> <br/>| <span data-ttu-id="1099c-319">Указывает языковые файлы, которые необходимо включить</span><span class="sxs-lookup"><span data-stu-id="1099c-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="1099c-320">Необязательный — значение по умолчанию — нет</span><span class="sxs-lookup"><span data-stu-id="1099c-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="1099c-321">Чтобы указать несколько языков, включите параметр запроса крышки для каждого языка</span><span class="sxs-lookup"><span data-stu-id="1099c-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="1099c-322">Используйте формат идентификатора языка, ex.</span><span class="sxs-lookup"><span data-stu-id="1099c-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="1099c-323">"en-us", "fr-fr"</span><span class="sxs-lookup"><span data-stu-id="1099c-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="1099c-324">alllanguages</span><span class="sxs-lookup"><span data-stu-id="1099c-324">alllanguages</span></span> <br/>| <span data-ttu-id="1099c-325">Указывает, что необходимо включить все языковые файлы</span><span class="sxs-lookup"><span data-stu-id="1099c-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="1099c-326">Необязательный — значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="1099c-326">Optional – defaults to false</span></span> |

<span data-ttu-id="1099c-327">HTTP-ответ</span><span class="sxs-lookup"><span data-stu-id="1099c-327">HTTP Response</span></span>

<span data-ttu-id="1099c-328">В случае успеха этот метод возвращает код отклика 200 OK и коллекцию объектов файла в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="1099c-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="1099c-329">Чтобы создать образ, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1099c-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="1099c-330">Вызовите API, предоставив соответствующие параметры запроса для канала, версии и архитектуры интересующих вас обновлений.</span><span class="sxs-lookup"><span data-stu-id="1099c-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="1099c-331">Примечание. Объекты-файлы с атрибутом "lcid": "0" являются нейтральными для языка файлами и должны быть включены в изображение.</span><span class="sxs-lookup"><span data-stu-id="1099c-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="1099c-332">Создадим локальное изображение CDN, протерируя объекты файлов и копируя файлы CDN, создавая структуру папок в зависимости от атрибута relativePath, определенного для каждого объекта файла.</span><span class="sxs-lookup"><span data-stu-id="1099c-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="1099c-333">В следующем примере извлекается список файлов для Current Channel и версии 16.0.4229.1004 для 64-битных и включаются файлы французского и английского языков:</span><span class="sxs-lookup"><span data-stu-id="1099c-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="1099c-334">Hash verification of .dat files</span><span class="sxs-lookup"><span data-stu-id="1099c-334">Hash verification of .dat files</span></span>

<span data-ttu-id="1099c-335">Средства создания изображений могут проверять целостность загруженных DAT-файлов, сравнивая вычисленное значение hash с предоставленным значением hash, связанным с каждым DAT-файлом.</span><span class="sxs-lookup"><span data-stu-id="1099c-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="1099c-336">Ниже приводится пример объекта файла, который указывает значения hashLocation и hashAlgorithm:</span><span class="sxs-lookup"><span data-stu-id="1099c-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
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

- <span data-ttu-id="1099c-337">Атрибут **hashLocation** указывает относительный путь CAB-файла, который содержит значение hash.</span><span class="sxs-lookup"><span data-stu-id="1099c-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="1099c-338">Сконструировать расположение файла hash, совметив URL-адрес + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="1099c-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="1099c-339">В следующем примере расположение stream.x64.bg-bg.hash будет следующим:</span><span class="sxs-lookup"><span data-stu-id="1099c-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="1099c-340">Атрибут **hashAlgorithm** указывает, какой алгоритм был использован.</span><span class="sxs-lookup"><span data-stu-id="1099c-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="1099c-341">Чтобы проверить целостность файла stream.x64.bg-bg.dat, откройте файл stream.x64.bg-bg.hash и прочитайте значение HASH, которое является первой строкой текста в hash-файле.</span><span class="sxs-lookup"><span data-stu-id="1099c-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="1099c-342">Сравните это с вычисленным значением hash (с использованием указанного алгоритма hashing), чтобы проверить целостность загруженного DAT-файла.</span><span class="sxs-lookup"><span data-stu-id="1099c-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="1099c-343">В следующем примере показан код C# для чтения хэш-кода.</span><span class="sxs-lookup"><span data-stu-id="1099c-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="1099c-344">Обновления приложений Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1099c-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="1099c-345">Все обновления приложений Microsoft 365 публикуются в [каталоге обновлений Майкрософт.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)</span><span class="sxs-lookup"><span data-stu-id="1099c-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="1099c-346">Обновления приложений Microsoft 365 позволяют управляемому программному обеспечению обрабатывать обновления приложений Microsoft 365 так, как любое другое обновление WU за одним исключением; обновления клиента не содержат фактических полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1099c-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="1099c-347">Обновления приложений Microsoft 365 не следует устанавливать ни на каких клиентах, а использовать для запуска рабочего процесса с помощью программного обеспечения для управления, заменив команду установки механизмом установки на основе COM, показанным выше.</span><span class="sxs-lookup"><span data-stu-id="1099c-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="1099c-348">**На следующем рисунке показана схема рабочего процесса обновления клиента Office 365.**</span><span class="sxs-lookup"><span data-stu-id="1099c-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="1099c-349">![Схема рабочего процесса для обновлений клиента O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Схема рабочего процесса для обновлений клиента O365PP")</span><span class="sxs-lookup"><span data-stu-id="1099c-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="1099c-350">Каждое опубликованное обновление приложений Microsoft 365 включает метаданные об обновлении.</span><span class="sxs-lookup"><span data-stu-id="1099c-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="1099c-351">Эти метаданные включают параметр MoreInfoUrl, который можно использовать для получения вызова API для API списка файлов для конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="1099c-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="1099c-352">В следующем примере API списка файлов внедрен в MoreInfoURL и начинается с "ServicePath="</span><span class="sxs-lookup"><span data-stu-id="1099c-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="1099c-353"> http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="1099c-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="1099c-354">Дополнительные метаданные для автоматизации промежуточного содержимого</span><span class="sxs-lookup"><span data-stu-id="1099c-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="1099c-355">**API истории выпусков**</span><span class="sxs-lookup"><span data-stu-id="1099c-355">**Release History API**</span></span>
  
<span data-ttu-id="1099c-356">API истории выпусков приложений Microsoft 365 используется для получения сведений о каждом из обновлений, опубликованных в CDN, а также имен каналов и других атрибутов канала.</span><span class="sxs-lookup"><span data-stu-id="1099c-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="1099c-357">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="1099c-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="1099c-358">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="1099c-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="1099c-359">Для вызова этого API не требуются разрешения.</span><span class="sxs-lookup"><span data-stu-id="1099c-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="1099c-360">HTTP-ответ</span><span class="sxs-lookup"><span data-stu-id="1099c-360">HTTP Response</span></span>

<span data-ttu-id="1099c-361">В случае успеха этот метод возвращает код отклика 200 OK и коллекцию объектов файла в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="1099c-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="1099c-362">**API-API для skus**</span><span class="sxs-lookup"><span data-stu-id="1099c-362">**SKUs API**</span></span>
  
<span data-ttu-id="1099c-363">API skus возвращает сведения, которые полезны для определения продуктов, доступных для развертывания и обслуживания из CDN Office, а также различные параметры для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="1099c-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="1099c-364">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="1099c-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="1099c-365">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="1099c-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="1099c-366">Для вызова этого API не требуются разрешения.</span><span class="sxs-lookup"><span data-stu-id="1099c-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="1099c-367">HTTP-ответ</span><span class="sxs-lookup"><span data-stu-id="1099c-367">HTTP Response</span></span>

<span data-ttu-id="1099c-368">В случае успеха этот метод возвращает код отклика 200 OK и коллекцию объектов файла в тексте отклика.</span><span class="sxs-lookup"><span data-stu-id="1099c-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
