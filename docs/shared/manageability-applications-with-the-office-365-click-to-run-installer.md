---
title: Интеграция приложений управляемости с установщиком click-to-run Office 365
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Узнайте, как можно интегрировать программу установки Office 365 Click-to-Run с помощью решения для управления программного обеспечения.
ms.openlocfilehash: 0e9e82fbf86b81ad35928277ff11fe9b86d91964
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401750"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="67154-103">Интеграция приложений управляемости с установщиком click-to-run Office 365</span><span class="sxs-lookup"><span data-stu-id="67154-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="67154-104">Узнайте, как можно интегрировать программу установки Office 365 Click-to-Run с помощью решения для управления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="67154-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="67154-105">Установщик Office 365 Click-to-Run предоставляет COM-интерфейс, обеспечивающий программный контроль за управление обновлениями ИТ-специалистов и решений по управлению программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="67154-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="67154-106">Этот интерфейс предоставляет дополнительные возможности управления рамками средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="67154-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="67154-107">Эта статья относится к Office 2016 и более поздних версий, Office 365.</span><span class="sxs-lookup"><span data-stu-id="67154-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="67154-108">Интеграция с Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="67154-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="67154-109">Чтобы использовать этот интерфейс, управляемость приложения вызывает интерфейс COM и вызовы предоставляемые API, которые напрямую связываются с служба установки Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="67154-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="67154-110">Установщик Office Click-to-Run может выполняться из командной строки с параметрами, которые можно управлять поведением, как описано в [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="67154-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="67154-111">**Ниже приведен концептуальная диаграмма интерфейса COM**</span><span class="sxs-lookup"><span data-stu-id="67154-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="67154-112">![Схема с помощью интерфейса COM программу установки Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема с использованием интерфейса COM программу установки Office Click-To-Run")</span><span class="sxs-lookup"><span data-stu-id="67154-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="67154-113">Интерфейс на основе COM реализует установщик Office 365 Click-to-Run, **IUpdateNotify** , зарегистрированных для CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="67154-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="67154-114">Этот интерфейс может быть вызван следующим образом:</span><span class="sxs-lookup"><span data-stu-id="67154-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="67154-115">Вызов будет только успешным Если запущен вызывающего абонента с повышенными привилегиями, как необходимо запустить программу установки Click-to-Run с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="67154-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="67154-116">Интерфейс **IUpdateNotify** COM предоставляет три асинхронные функции, ответственный за Проверка команды и параметры и расписание выполнения со службой установки Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="67154-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="67154-117">A Далее метод, **состояние**, можно использовать для получения сведений о состоянии последнего выполняемая команда или состояния в настоящее время выполнения команды (успех, ошибка, коды ошибок подробные).</span><span class="sxs-lookup"><span data-stu-id="67154-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="67154-118">Существует четыре состояния, служба установки Click-to-Run в во время его жизненного цикла, во время которого могут быть вызваны методы **IUpdateNotify** ; Перезагрузка, простоя, загрузки и применение.</span><span class="sxs-lookup"><span data-stu-id="67154-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="67154-119">**Ниже приведен на схеме COM интерфейс конечного компьютера**</span><span class="sxs-lookup"><span data-stu-id="67154-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="67154-120">![Диаграмму состояний для интерфейса COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Схема состояний для интерфейса COM")</span><span class="sxs-lookup"><span data-stu-id="67154-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="67154-121">**Rebooting**: при загрузке компьютер находится за период времени, когда служба установщика Click-to-Run недоступен.</span><span class="sxs-lookup"><span data-stu-id="67154-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="67154-122">Возвращает eUPDATE_UNKNOWN успешного вызова метода состояние после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="67154-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="67154-123">**Простоя:** Когда установщик Click-to-Run находится в состоянии простоя, можно вызвать:</span><span class="sxs-lookup"><span data-stu-id="67154-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="67154-124">**Применить**: Install ранее загруженного содержимого.</span><span class="sxs-lookup"><span data-stu-id="67154-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="67154-125">**Отмена**: возвращает `0x800000e`, «был вызван метод в непредвиденное время.»</span><span class="sxs-lookup"><span data-stu-id="67154-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="67154-126">**Загрузка**: файлы для загрузки нового контента на клиенте для установки более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="67154-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="67154-127">**Состояние**: возвращает результат последнего завершенного действия или сообщение об ошибке, если завершение действия в сбоя.</span><span class="sxs-lookup"><span data-stu-id="67154-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="67154-128">Если нет предыдущих действий, возвращает **состояние** `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="67154-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="67154-129">**Загрузка:** Когда установщик Click-to-Run находится в состоянии загрузки, можно вызвать:</span><span class="sxs-lookup"><span data-stu-id="67154-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="67154-130">**Применить**: возвращает значение **HRESULT** со значением `0x800000e`, «был вызван метод в непредвиденное время.»</span><span class="sxs-lookup"><span data-stu-id="67154-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="67154-131">**Отмена**: останавливает загрузку и удаляет частично загруженного содержимого.</span><span class="sxs-lookup"><span data-stu-id="67154-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="67154-132">**Загрузка**: возвращает значение **HRESULT** со значением `0x800000e`, «был вызван метод в непредвиденное время.»</span><span class="sxs-lookup"><span data-stu-id="67154-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="67154-133">**Состояние**: возвращает **DOWNLOAD_WIP** для указания, что файл для загрузки рабочих находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="67154-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="67154-134">**Применение:** Когда программа установки Click-to-Run находится в процессе установки ранее Загрузите содержимое:</span><span class="sxs-lookup"><span data-stu-id="67154-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="67154-135">**Применить**: возвращает значение **HRESULT** со значением `0x800000e`, «был вызван метод в непредвиденное время.»</span><span class="sxs-lookup"><span data-stu-id="67154-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="67154-136">**Отмена**: возвращает `0x800000e`, применить действие невозможно отменить.</span><span class="sxs-lookup"><span data-stu-id="67154-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="67154-137">**Загрузка**: возвращает значение **HRESULT** со значением `0x800000e`, «был вызван метод в непредвиденное время.»</span><span class="sxs-lookup"><span data-stu-id="67154-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="67154-138">**Состояние**: возвращает **APPLY_WIP** для указания, которые применяются рабочих находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="67154-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="67154-139">Поскольку OfficeC2RCOM — это служба COM + и динамически загружается, необходимо вызвать **CoCreateInstance** каждый раз при вызове метода на этот класс, чтобы убедиться, что вы получаете ожидаемый результат.</span><span class="sxs-lookup"><span data-stu-id="67154-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="67154-140">Служба COM + будет обрабатывать создания экземпляра, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="67154-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="67154-141">Когда один из методов вызывается в первый раз, COM + будет загрузить объект **IUpdateNotify** и запустите его в пределах одного из экземпляров dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="67154-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="67154-142">Новый объект будет находиться в активном для около 3 минут бездействия.</span><span class="sxs-lookup"><span data-stu-id="67154-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="67154-143">Если последующие вызов выполняется в три минуты последнего вызова, объект **IUpdateNotify** загружаются и не создается новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="67154-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="67154-144">Если вызов не происходит в течение трех минут, объект IUpdateNotify будет выгрузки и будет создан новый объект **IUpdateNotify** , при следующем вызове.</span><span class="sxs-lookup"><span data-stu-id="67154-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="67154-145">Справочник по COM API установщика Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="67154-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="67154-146">В следующей документации Справочник по API:</span><span class="sxs-lookup"><span data-stu-id="67154-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="67154-147">Параметры используются в виде пары ключ значение, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="67154-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="67154-148">Параметры не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="67154-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="67154-149">[Список параметров](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) с помощью документации доступен.</span><span class="sxs-lookup"><span data-stu-id="67154-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="67154-150">Обзор интерфейса IUpdateNotify2 — теперь включены.</span><span class="sxs-lookup"><span data-stu-id="67154-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="67154-151">Apply</span><span class="sxs-lookup"><span data-stu-id="67154-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="67154-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="67154-152">Parameters</span></span>

-  <span data-ttu-id="67154-153">_displaylevel_: **true** для отображения состояния установки, включая ошибки, во время процесса обновления; **значение false,** Чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="67154-154">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="67154-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="67154-155">_forceappshutdown_: **значение true,** Чтобы принудительно завершить работу сразу же если **Применить** действие инициируется; приложения Office **значение false** с ошибкой, если запущены любого приложения Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="67154-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="67154-156">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="67154-156">The default is **false**.</span></span> <span data-ttu-id="67154-157">[Для получения дополнительных сведений см.](#bk_ApplyRemark)</span><span class="sxs-lookup"><span data-stu-id="67154-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="67154-158">Если при запуске **Применить** действие выполняется любое приложение Office, **Применить** действие обычно завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="67154-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="67154-159">Передача `forceappshutdown=true` **Применить** метод будет отображено **OfficeClickToRun** службы сразу же завершите работу приложения и применения обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="67154-160">Пользователь может в этом случае привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="67154-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="67154-161">Возвращать результаты</span><span class="sxs-lookup"><span data-stu-id="67154-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67154-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="67154-162">**S_OK**</span></span> <br/> |<span data-ttu-id="67154-163">Действие было успешно отправлено в службу Click-To-Run для выполнения.</span><span class="sxs-lookup"><span data-stu-id="67154-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="67154-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="67154-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="67154-165">Вызывающий не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="67154-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="67154-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="67154-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="67154-167">Были переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="67154-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="67154-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="67154-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="67154-169">Действие не допускается в данный момент.</span><span class="sxs-lookup"><span data-stu-id="67154-169">Action is not allowed at this time.</span></span> <span data-ttu-id="67154-170">[Для получения дополнительных сведений см.](#bk_ApplyRemark)</span><span class="sxs-lookup"><span data-stu-id="67154-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="67154-171">Замечания</span><span class="sxs-lookup"><span data-stu-id="67154-171">Remarks</span></span>

- <span data-ttu-id="67154-172">Если при запуске **Применить** действие выполняется любое приложение Office, **Применить** действие завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="67154-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="67154-173">Передача `forceappshutdown=true` **Применить** метод будет отображено службы **OfficeClickToRun** немедленно завершить работу любого приложения Office, которые работают и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="67154-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="67154-174">Могут возникать данных как они не запрос на сохранение изменений для открытия документов.</span><span class="sxs-lookup"><span data-stu-id="67154-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="67154-175">Это действие может быть запущено, только если состояние COM одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="67154-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="67154-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="67154-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="67154-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="67154-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="67154-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="67154-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="67154-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="67154-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="67154-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="67154-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="67154-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="67154-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="67154-182">Если вызывается метод **Apply** без ранее загрузки содержимого, методу **Apply** сообщает **Succeeded** обнаружено значение nothing для применения и успешного завершения процесса **Применить** .</span><span class="sxs-lookup"><span data-stu-id="67154-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="67154-183">Cancel</span><span class="sxs-lookup"><span data-stu-id="67154-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="67154-184">Возвращать результаты</span><span class="sxs-lookup"><span data-stu-id="67154-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67154-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="67154-185">S_OK</span></span>  <br/> |<span data-ttu-id="67154-186">Действие было успешно отправлено в службу Click-to-Run для выполнения.</span><span class="sxs-lookup"><span data-stu-id="67154-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="67154-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="67154-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="67154-188">Действие не допускается в данный момент.</span><span class="sxs-lookup"><span data-stu-id="67154-188">Action is not allowed at this time.</span></span> <span data-ttu-id="67154-189">[Для получения дополнительных сведений см](#bk_CancelRemarks)</span><span class="sxs-lookup"><span data-stu-id="67154-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="67154-190">Замечания</span><span class="sxs-lookup"><span data-stu-id="67154-190">Remarks</span></span>

- <span data-ttu-id="67154-191">Этот метод может быть только инициируется при код состояния COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="67154-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="67154-192">Попытка отменить текущий файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="67154-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="67154-193">Состояние COM изменит **eDOWNLOAD_CANCELLING** и перейдите в конечном счете **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="67154-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="67154-194">Состояние COM возвращает **E_ILLEGAL_METHOD_CALL** , если запускаются в любое время.</span><span class="sxs-lookup"><span data-stu-id="67154-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="67154-195">Загрузка</span><span class="sxs-lookup"><span data-stu-id="67154-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="67154-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="67154-196">Parameters</span></span>

-  <span data-ttu-id="67154-197">_displaylevel_: **true** для отображения состояния установки, включая ошибки, во время процесса обновления; **значение false,** Чтобы скрыть состояние установки, включая ошибки, во время процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="67154-198">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="67154-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="67154-199">_updatebaseurl_: URL-адрес источника альтернативного файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="67154-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="67154-200">_updatetoversion_: версии для обновления Office.</span><span class="sxs-lookup"><span data-stu-id="67154-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="67154-201">Определите этот параметр, если вы хотите обновить старой версии, чем версия, которая устанавливается в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="67154-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="67154-202">_downloadsource_: CLSID пользовательские реализации **IBackgroundCopyManager** (диспетчер бит).</span><span class="sxs-lookup"><span data-stu-id="67154-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="67154-203">_contentid_: Определяет содержимое для загрузки с сервера через настраиваемый диспетчер бит.</span><span class="sxs-lookup"><span data-stu-id="67154-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="67154-204">Это значение передается через интерфейс БИТОВ для интерпретации.</span><span class="sxs-lookup"><span data-stu-id="67154-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="67154-205">Возвращать результаты</span><span class="sxs-lookup"><span data-stu-id="67154-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67154-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="67154-206">**S_OK**</span></span> <br/> |<span data-ttu-id="67154-207">Действие было успешно отправлено в службу Click-To-Run для выполнения.</span><span class="sxs-lookup"><span data-stu-id="67154-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="67154-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="67154-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="67154-209">Вызывающий не работает с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="67154-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="67154-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="67154-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="67154-211">Были переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="67154-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="67154-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="67154-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="67154-213">Действие не допускается в данный момент.</span><span class="sxs-lookup"><span data-stu-id="67154-213">Action is not allowed at this time.</span></span> <span data-ttu-id="67154-214">[Для получения дополнительных сведений см.](#bk_DownloadRemark)</span><span class="sxs-lookup"><span data-stu-id="67154-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="67154-215">Замечания</span><span class="sxs-lookup"><span data-stu-id="67154-215">Remarks</span></span>

- <span data-ttu-id="67154-216">Необходимо указать _downloadsource_ и _contentid_ парой.</span><span class="sxs-lookup"><span data-stu-id="67154-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="67154-217">В противном случае возвращает ошибку **E_INVALIDARG** метод **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="67154-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="67154-218">Если этот параметр указан _downloadsource_, _contentid_и _updatebaseurl_ _updatebaseurl_ будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="67154-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="67154-219">Это действие может быть запущено, только если состояние COM одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="67154-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="67154-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="67154-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="67154-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="67154-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="67154-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="67154-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="67154-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="67154-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="67154-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="67154-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="67154-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="67154-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="67154-226">При вызове метода **Применить** без ранее загруженного содержимого методу **Apply** сообщает **Succeeded** обнаружено значение nothing для применения и успешного завершения процесса **Применить** .</span><span class="sxs-lookup"><span data-stu-id="67154-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="67154-227">Примеры</span><span class="sxs-lookup"><span data-stu-id="67154-227">Examples</span></span>

- <span data-ttu-id="67154-228">Для загрузки содержимого из настраиваемый диспетчер БИТЫ: вызовите функцию **download()** , передав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="67154-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="67154-229">Для загрузки содержимого из сети Microsoft CDN: вызовите функцию **download()** без указания параметров _downloadsource_, _contentid_или _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="67154-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="67154-230">Для загрузки содержимого из настроенного расположения: вызовите функцию **download()** , передавая следующий параметр:</span><span class="sxs-lookup"><span data-stu-id="67154-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="67154-231">Status</span><span class="sxs-lookup"><span data-stu-id="67154-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="67154-232">Параметры</span><span class="sxs-lookup"><span data-stu-id="67154-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="67154-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="67154-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="67154-234">Указатель на структуру UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="67154-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="67154-235">Возвращать результаты</span><span class="sxs-lookup"><span data-stu-id="67154-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67154-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="67154-236">**S_OK**</span></span> <br/> |<span data-ttu-id="67154-237">Метод **состояние** всегда возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="67154-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="67154-238">Изучение `UPDATE_STATUS_RESULT` структуры для состояния текущего действия.</span><span class="sxs-lookup"><span data-stu-id="67154-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="67154-239">Замечания</span><span class="sxs-lookup"><span data-stu-id="67154-239">Remarks</span></span>

- <span data-ttu-id="67154-240">Поле состояния `UPDATE_STATUS_REPORT` содержит состояния текущего действия.</span><span class="sxs-lookup"><span data-stu-id="67154-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="67154-241">Возвращается одно из следующих значений состояния:</span><span class="sxs-lookup"><span data-stu-id="67154-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="67154-242">Если команда возникла ошибка, поле ошибки `UPDATE_STATUS_REPORT` содержит подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="67154-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="67154-243">Два типа коды ошибок возвращаются методом **состояние** .</span><span class="sxs-lookup"><span data-stu-id="67154-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="67154-244">Если ошибка меньше, чем `UDPATE_ERROR_CODE::eUNKNOWN`, ошибки — это один из следующих кодов ошибки предварительно заданные:</span><span class="sxs-lookup"><span data-stu-id="67154-244">If the error less than  `UDPATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="67154-245">Если этот код ошибки больше, чем `UDPATE_ERROR_CODE::eUNKNOWN` является **HRESULT** вызова неудачных функции.</span><span class="sxs-lookup"><span data-stu-id="67154-245">If the return error code is larger than  `UDPATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="67154-246">Чтобы извлечь вычитание HRESULT `UDPATE_ERROR_CODE::eUNKNOWN` по значению, возвращенному в поле ошибки `UPDATE_STATUS_REPORT`.</span><span class="sxs-lookup"><span data-stu-id="67154-246">To extract the HRESULT subtract  `UDPATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="67154-247">Полный список значений status и error можно просмотреть, изучив **IUpdateNotify** библиотеки типов, внедренные в OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="67154-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="67154-248">Поле contentid используется для вызовов, **состояние** после **загрузки** инициировал и возвращает contentid, переданный в вызов **загрузить** .</span><span class="sxs-lookup"><span data-stu-id="67154-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="67154-249">Рекомендуется инициализировать в этом поле **значения NULL** до вызова метода **состояние** и проверьте значение после возвращения **состояния** .</span><span class="sxs-lookup"><span data-stu-id="67154-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="67154-250">Если значение равно **null**, это означает, что нет не contentid для возврата.</span><span class="sxs-lookup"><span data-stu-id="67154-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="67154-251">Если значение не равно **null**, нужно освободить с помощью вызова **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="67154-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="67154-252">Ниже приведен фрагмент кода вызов **состояния** после **загрузки**.</span><span class="sxs-lookup"><span data-stu-id="67154-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="67154-253">Сводка по IUpdateNotify2 интерфейс</span><span class="sxs-lookup"><span data-stu-id="67154-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="67154-254">Этой сводки предоставляется информация дополнение [интегрирование управляемости приложений с помощью установщика нажми и работай Office 365](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx).</span><span class="sxs-lookup"><span data-stu-id="67154-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx).</span></span> <span data-ttu-id="67154-255">После обновления открытого документа, этот документ можно оценить как как устаревшие.</span><span class="sxs-lookup"><span data-stu-id="67154-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="67154-256">От C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (первый общедоступным построения должны быть построения разветвления июня--8326.\*) мы добавили новый интерфейс **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="67154-256">From C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="67154-257">Вот некоторые основные сведения о этот интерфейс:</span><span class="sxs-lookup"><span data-stu-id="67154-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="67154-258">CLSID_UpdateNotifyObject2 {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="67154-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="67154-259">Этот интерфейс также размещенная исходный интерфейс IUpdateNotify для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="67154-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="67154-260">Что означает, если вы используете этот интерфейс, у вас есть доступ ко всем методам, представленные в интерфейс **UpdateNotifyObject** .</span><span class="sxs-lookup"><span data-stu-id="67154-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="67154-261">Новые методы, добавленные к IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="67154-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="67154-262">**HRESULT** GetBlockingApps ([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="67154-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="67154-263">Получение обновлений блокировки список приложений.</span><span class="sxs-lookup"><span data-stu-id="67154-263">Get updates blocking apps list.</span></span> <span data-ttu-id="67154-264">Этот вызов будет возвращать работающих приложений Office, которые будет блокировать процесс обновления с переходом.</span><span class="sxs-lookup"><span data-stu-id="67154-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="67154-265">**HRESULT** GetOfficeDeploymentData (тип данных int, pcwszName **значение LPCWSTR** , [out] BSTR [in] [in] \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="67154-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="67154-266">Получите развертывания Office данных.</span><span class="sxs-lookup"><span data-stu-id="67154-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="67154-267">Если вы хотите использовать новые методы, необходимо убедитесь, что:</span><span class="sxs-lookup"><span data-stu-id="67154-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="67154-268">Новее выше построения вашей версии C2R (\>= построения разветвления июня).</span><span class="sxs-lookup"><span data-stu-id="67154-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="67154-269">Используйте UpdateNotifyObject2, а не **UpdateNotifyObject** для вызова **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="67154-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="67154-270">Если не используется один из новых методов, не нужно изменять что-либо.</span><span class="sxs-lookup"><span data-stu-id="67154-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="67154-271">Все существующие методы будут работать как точно так же, как перед.</span><span class="sxs-lookup"><span data-stu-id="67154-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="67154-272">Реализация интерфейса БИТОВ</span><span class="sxs-lookup"><span data-stu-id="67154-272">Implementing the BITS interface</span></span>

<span data-ttu-id="67154-273">[Фоновая интеллектуальная служба передачи](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (BITS) — это служба, предоставляемым корпорацией Майкрософт для передачи файлов между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="67154-273">The [Background Intelligent Transfer Service](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="67154-274">БИТ — это один из каналов, установщик Office Click-To-Run можно использовать для загрузки содержимого.</span><span class="sxs-lookup"><span data-stu-id="67154-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="67154-275">По умолчанию в Office Click-To-Run установщика используются Windows на основе в реализации BITS для загрузки содержимого из сети CDN.</span><span class="sxs-lookup"><span data-stu-id="67154-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="67154-276">С указанием специализированной реализации бит в метод **download()** интерфейса **IUpdateNotify** , программного обеспечения управляемости можно управлять, где и как клиент загружает содержимое.</span><span class="sxs-lookup"><span data-stu-id="67154-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="67154-277">Настроенный интерфейс бит полезен при предоставлении канал настраиваемого контента распространения отличных от каналы встроенных Click-to-Run, например CDN Office, серверов служб IIS или общие файловые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="67154-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="67154-278">Минимальные требования для настраиваемого интерфейса БИТОВ для работы со службой Office C2R — это:</span><span class="sxs-lookup"><span data-stu-id="67154-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="67154-279">Для **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="67154-279">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="67154-280">Для **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="67154-280">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="67154-281">Для **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="67154-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="67154-282">Для `Addfile` и `AddFileWithRanges` — это URL-адрес удаленной функции, в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="67154-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="67154-283">cmbits жестко закодированные и означает настраиваемого бит.</span><span class="sxs-lookup"><span data-stu-id="67154-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="67154-284">_ \<contentid\> _ — это _contentid_ параметра для метода **Download()** .</span><span class="sxs-lookup"><span data-stu-id="67154-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="67154-285">_ \<относительный путь к файлу целевой\> _ предоставляет расположение и имя файла для загрузки.</span><span class="sxs-lookup"><span data-stu-id="67154-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="67154-286">Например, если вы предоставили _contentid_ из `f732af58-5d86-4299-abe9-7595c35136ef` для **Download()** метод и Office C2R требуется загрузить версию CAB-файлу, таких как `v32.cab` файл, он вызовет **AddFile()** со следующими `RemoteUrl`:</span><span class="sxs-lookup"><span data-stu-id="67154-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="67154-287">Для **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="67154-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="67154-288">Для **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="67154-288">For **IBackgroundCopyFile**:</span></span>
    
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

## <a name="automating-content-staging"></a><span data-ttu-id="67154-289">Автоматизация промежуточного хранения содержимого</span><span class="sxs-lookup"><span data-stu-id="67154-289">Automating content staging</span></span>

<span data-ttu-id="67154-290">ИТ-администраторов можно включить, чтобы автоматически получать обновления при их можно использовать непосредственно из Microsoft доставки содержимого сети (CDN) или они могут выбрать для управления развертыванием обновлений, доступные из обновления настольных клиентов каналы, с помощью средства развертывания Office или System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="67154-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="67154-291">Служба поддерживает возможность средства управления для распознавания и автоматизации загрузку содержимого при обновления становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="67154-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="67154-292">**На следующем рисунке приведено Общие сведения о загрузке образа**</span><span class="sxs-lookup"><span data-stu-id="67154-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="67154-293">![Схема с помощью интерфейса COM программу установки Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема с использованием интерфейса COM программу установки Office Click-To-Run")</span><span class="sxs-lookup"><span data-stu-id="67154-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="67154-294">Общие сведения о загрузке образа</span><span class="sxs-lookup"><span data-stu-id="67154-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="67154-295">На предыдущем рисунке видеть, что Office 365 ProPlus изображения доступен на Office рассылки сети содержимого (CDN).</span><span class="sxs-lookup"><span data-stu-id="67154-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="67154-296">Вместе с Office 365 ProPlus изображение список XML-файлу доступна также которого содержит сведения, необходимые для включения программного обеспечения управляемости непосредственно Создание настраиваемых рисунков, нет необходимости в с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="67154-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="67154-297">Предприятия настраивает их WSUS для синхронизации обновления клиента Office 365.</span><span class="sxs-lookup"><span data-stu-id="67154-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="67154-298">Эти обновления не содержат полезных данных самого изображения, но разрешить программного обеспечения управляемости будет распознавать при доступности нового контента.</span><span class="sxs-lookup"><span data-stu-id="67154-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="67154-299">Программное обеспечение управляемости затем могут читать клиентское обновление метаданных понять, какие версии Office, обновление применяется.</span><span class="sxs-lookup"><span data-stu-id="67154-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="67154-300">Если требуется обновление программного обеспечения управляемости можно использовать CDN контента и список файлов для создания настраиваемого образа и сохраните ее на расположение общей папки, настроенной на использование.</span><span class="sxs-lookup"><span data-stu-id="67154-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="67154-301">Формат XML-файла списка</span><span class="sxs-lookup"><span data-stu-id="67154-301">Format of the XML file list</span></span>

<span data-ttu-id="67154-302">Существует два списка файлов в CAB-файле на CDN.</span><span class="sxs-lookup"><span data-stu-id="67154-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="67154-303">Один список файлов для 32-разрядной версии Office, а другая — для 64-разрядной версии Office.</span><span class="sxs-lookup"><span data-stu-id="67154-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="67154-304">URL-адрес из списка файлов Office (OFL. Файл CAB) является [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span><span class="sxs-lookup"><span data-stu-id="67154-304">The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="67154-305">Два файла списки называются:</span><span class="sxs-lookup"><span data-stu-id="67154-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="67154-306">O365Client_32bit.XML</span><span class="sxs-lookup"><span data-stu-id="67154-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="67154-307">O365Client_64bit.XML</span><span class="sxs-lookup"><span data-stu-id="67154-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="67154-308">В XML-код для каждого файла — это списки <UpdateFiles> узел, который содержит атрибут version.</span><span class="sxs-lookup"><span data-stu-id="67154-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="67154-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="67154-309"></span></span> <span data-ttu-id="67154-310">Эта версия увеличивается при внесении изменений в файл списки.</span><span class="sxs-lookup"><span data-stu-id="67154-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="67154-311">Существует два параметра, которые должны использоваться в сочетании с XML-код настраиваемого образа.</span><span class="sxs-lookup"><span data-stu-id="67154-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="67154-312">Замените *% версии* построения версии Office.</span><span class="sxs-lookup"><span data-stu-id="67154-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="67154-313">Могут быть получены из клиентское обновление метаданных (описано в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="67154-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="67154-314">Определение *baseURL* с помощью значение URL-адреса, связанные с филиала, изображение создается для.</span><span class="sxs-lookup"><span data-stu-id="67154-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="67154-315">Это является производным от клиентское обновление метаданных, описаны в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="67154-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="67154-316">Инструкции по созданию изображения являются:</span><span class="sxs-lookup"><span data-stu-id="67154-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="67154-317">Откройте список файлов XML.</span><span class="sxs-lookup"><span data-stu-id="67154-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="67154-318">Замените вхождения *% версии* применимых построения версии Office.</span><span class="sxs-lookup"><span data-stu-id="67154-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="67154-319">Версия сборки можно получить из releasehistory.xml, как описано далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="67154-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="67154-320">Прочитайте атрибут URL-адрес для конечной ветви.</span><span class="sxs-lookup"><span data-stu-id="67154-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="67154-321">Удалите узлы языка для любых языков в настраиваемых изображение не требуется.</span><span class="sxs-lookup"><span data-stu-id="67154-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="67154-322">Узлы с языком = "0", независимое от языка и должны быть включены в изображения.</span><span class="sxs-lookup"><span data-stu-id="67154-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="67154-323">Создайте образ локальной сети CDN, перебирая список файлов XML и копирования файлов CDN, при создании структуру папок при необходимости.</span><span class="sxs-lookup"><span data-stu-id="67154-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="67154-324">Если этот параметр указан атрибут *Переименование* затем *Переименуйте* скопированный файл значение, предоставляемые в атрибуте переименовать.</span><span class="sxs-lookup"><span data-stu-id="67154-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="67154-325">Используется для создания файлов v64.cab и v32.cab верхнего уровня по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67154-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="67154-326">Это переименованной версий CAB-файле построения верхнего уровня и используются в качестве версии установки по умолчанию, если версия не указан.</span><span class="sxs-lookup"><span data-stu-id="67154-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="67154-327">Используйте URL-адрес + relativePath + имя файла для построения CDN расположения.</span><span class="sxs-lookup"><span data-stu-id="67154-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="67154-328">Ниже приведены примеры использования ежемесячный канала (в соответствии с определением `<baseURL>` узел) и версия 16.0.4229.1004 из releasehistory.xml сборки.</span><span class="sxs-lookup"><span data-stu-id="67154-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="67154-329">Ниже приведен нейтральный файл языка, необходимые для всех языков.</span><span class="sxs-lookup"><span data-stu-id="67154-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="67154-330">V64_16.0.4229.1004.cab — это имя файла и его нужно скопировать из `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` и переименованные для `…/office/data/v64.cab`.</span><span class="sxs-lookup"><span data-stu-id="67154-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="67154-331">Ниже приведен файл должны быть включены в изображение en US, как описано в языке LCID = 1033.</span><span class="sxs-lookup"><span data-stu-id="67154-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="67154-332">S641033.cab — это имя файла и его нужно скопировать из `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` и не переименован.</span><span class="sxs-lookup"><span data-stu-id="67154-332">The name of the file is s641033.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="67154-333">Файлы с расширением DAT проверки хэш-функции</span><span class="sxs-lookup"><span data-stu-id="67154-333">Hash verification of .dat files</span></span>

<span data-ttu-id="67154-334">Средства создания образа может проверить целостность файлы с расширением DAT загруженного путем сравнения с заданным значения хэш-функции, связанные с каждым файлы с расширением DAT вычисленного значения хэш-функции.</span><span class="sxs-lookup"><span data-stu-id="67154-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="67154-335">Ниже приведен пример DAT-файл из ежемесячный канала с версией построения 16.0.4229.1004 и задайте для болгарского языка:</span><span class="sxs-lookup"><span data-stu-id="67154-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="67154-336">Атрибут **hashLocation** указывает расположение относительный путь bg.hash stream.x64.bg stream.x64.bg bg.dat файла.</span><span class="sxs-lookup"><span data-stu-id="67154-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="67154-337">Создайте расположение файла хэш-функции, объединив URL-адрес + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="67154-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="67154-338">В следующем примере будет stream.x64.bg bg.hash расположение:</span><span class="sxs-lookup"><span data-stu-id="67154-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="67154-339">Атрибут **hashAlgo** определяет, какой алгоритм хэширования использовалась.</span><span class="sxs-lookup"><span data-stu-id="67154-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="67154-340">В этом случае Sha256 использовалась.</span><span class="sxs-lookup"><span data-stu-id="67154-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="67154-341">Для проверки целостности файлов stream.x64.bg bg.dat, откройте stream.x64.bg-bg.hash и читать значения хэш-функции, который является первой строки текста в файле хэш-функции.</span><span class="sxs-lookup"><span data-stu-id="67154-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="67154-342">Сравните это вычисляемые значения хэш-функции (с использованием указанного алгоритм хэширования) для проверки целостности загруженного DAT-файл.</span><span class="sxs-lookup"><span data-stu-id="67154-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="67154-343">Пример кода C# для считывания хеш.</span><span class="sxs-lookup"><span data-stu-id="67154-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="67154-344">Обновления клиента Office 365</span><span class="sxs-lookup"><span data-stu-id="67154-344">Office 365 Client Updates</span></span>

<span data-ttu-id="67154-345">Все обновления клиента Office 365 публикуются [Каталога Центра обновления Майкрософт](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="67154-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="67154-346">Обновления клиента Office 365 Включение управляемость программному обеспечению обрабатывать обновления клиента Office 365 в виде очень похож на другие обновления ву одно исключение; обновление клиентов, не содержащих фактический полезных данных.</span><span class="sxs-lookup"><span data-stu-id="67154-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="67154-347">Обновления клиента Office 365 не должен быть установлен на всех клиентов, но вместо используется для запуска рабочих процессов с помощью программного обеспечения управляемости, заменив команду установки с помощью COM на основе отображается над механизм установки.</span><span class="sxs-lookup"><span data-stu-id="67154-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="67154-348">**На следующем рисунке показана схема рабочего процесса обновления клиента Office 365.**</span><span class="sxs-lookup"><span data-stu-id="67154-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="67154-349">![Схема рабочего процесса для обновления клиента O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Схема рабочего процесса для обновления клиента O365PP")</span><span class="sxs-lookup"><span data-stu-id="67154-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="67154-350">Каждый Office 365 обновление клиента, который был опубликован включает в себя метаданные об обновлении.</span><span class="sxs-lookup"><span data-stu-id="67154-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="67154-351">Метаданные включают в себя параметра с именем *MoreInfoUrl* , которую можно использовать для оценки со следующими сведениями:</span><span class="sxs-lookup"><span data-stu-id="67154-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="67154-352">*Версия*: Определяет версию Office, связанные с этим обновлением.</span><span class="sxs-lookup"><span data-stu-id="67154-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="67154-353">*Филиала*: канал обновления для обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="67154-354">Значения включают InsiderFast, сотрудники компании, ежемесячно, требуемой, Broad.</span><span class="sxs-lookup"><span data-stu-id="67154-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="67154-355">Дополнительные значения могут быть добавлены в будущем.</span><span class="sxs-lookup"><span data-stu-id="67154-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="67154-356">*Архитектура*: определяет архитектуру процессора, связанные с этим обновлением.</span><span class="sxs-lookup"><span data-stu-id="67154-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="67154-357">*xmlVer*: версия списки файлов XML, которые должны использоваться для создания базового изображения для обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="67154-358">*xmlPath*: путь к OFL. Список CAB-файл, который содержит XML-файл.</span><span class="sxs-lookup"><span data-stu-id="67154-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="67154-359">*mlFile*: имя списка файлов, который должен использоваться для этого обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="67154-360">Значение будет O365Client_32bit или O365Client_64bit и будет соответствовать архитектуры.</span><span class="sxs-lookup"><span data-stu-id="67154-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="67154-361">Следующий URL-адрес является примером параметр *MoreInfoURL* , который ссылается на выпуски обновления клиента Office 365 для 32-разрядной версии Office с версии построения 16.0.2342.2343 к текущему каналу.</span><span class="sxs-lookup"><span data-stu-id="67154-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="67154-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab— Это расположение списки файлов XML для обновления, в частности O365Client_32bit.xml из внутри OFL. CAB-ФАЙЛА.</span><span class="sxs-lookup"><span data-stu-id="67154-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="67154-363">Выпуски канала обновления клиента Office 365</span><span class="sxs-lookup"><span data-stu-id="67154-363">Office 365 client update channel releases</span></span>](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="67154-364">Дополнительные метаданные для автоматизации промежуточного хранения содержимого</span><span class="sxs-lookup"><span data-stu-id="67154-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="67154-365">В дополнение к метаданных, который был опубликован которого определяется существует также дополнительные XML-файлы публикуются в сети доставки Содержимого, могут получить дополнительные сведения о клиентах Office 365, которые доступны из сети CDN Office.</span><span class="sxs-lookup"><span data-stu-id="67154-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="67154-366">**НОМЕРА SKU. XML**</span><span class="sxs-lookup"><span data-stu-id="67154-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="67154-367">XML-файле содержится в подписанных CAB-ФАЙЛ и опубликовано CDN Office по следующему URL-АДРЕСУ: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span><span class="sxs-lookup"><span data-stu-id="67154-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="67154-368">Метаданные, опубликованной в XML-файл можно использовать для определение продуктов, которые доступны для развертывания и обслуживания из сети CDN Office, а также различные возможности для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="67154-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
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

<span data-ttu-id="67154-369">\*\* \<ReleaseInfo\> \*\* корневого узла содержит атрибут PublishedDate, который определяет дату, которая была опубликована в этом файле.</span><span class="sxs-lookup"><span data-stu-id="67154-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="67154-370">\*\* \<SKU\> \*\* узел определяет отдельные SKU.</span><span class="sxs-lookup"><span data-stu-id="67154-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="67154-371">Атрибут *ProductID* определяет идентификатор, который передается в качестве атрибута ID в configuration.xml при использовании ODT.</span><span class="sxs-lookup"><span data-stu-id="67154-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="67154-372">Например, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="67154-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="67154-373">*Значение по умолчанию* атрибута, если присвоено значение True, идентифицирующее рекомендуемая Конфигурация.</span><span class="sxs-lookup"><span data-stu-id="67154-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="67154-374">\*\* \<Приложения\> \*\* узлов используются для определения отдельных приложений Office, поддерживаемых каждой SKU.</span><span class="sxs-lookup"><span data-stu-id="67154-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="67154-375">Атрибут *Name* — это имя отображаемой приложения.</span><span class="sxs-lookup"><span data-stu-id="67154-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="67154-376">Атрибут *AppID* является в атрибуте ID, переданного файла configuration.xml для \*\* \<ExcludeApp\> \*\* узел при использовании ODT.</span><span class="sxs-lookup"><span data-stu-id="67154-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="67154-377">Например, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="67154-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="67154-378">**RELEASEHISTORY. XML**</span><span class="sxs-lookup"><span data-stu-id="67154-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="67154-379">Этот XML-файл содержится в подписанных CAB-ФАЙЛ и публикации в CDN Office в следующем расположении: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span><span class="sxs-lookup"><span data-stu-id="67154-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="67154-380">Метаданные, опубликованной в XML-файл полезен при определении, какие каналы поддерживаются для обслуживания обновления из сети CDN Office, а также сведения о журнале построения для каждого из поддерживаемых каналов.</span><span class="sxs-lookup"><span data-stu-id="67154-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
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

<span data-ttu-id="67154-381">\*\* \<ReleaseHistory\> \*\* корневого узла содержит атрибут PublishedDate, который определяет дату, которая была опубликована в этом файле.</span><span class="sxs-lookup"><span data-stu-id="67154-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="67154-382">\*\* \<UpdateChannel\> \*\* узел определяет поддерживаемые канала.</span><span class="sxs-lookup"><span data-stu-id="67154-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="67154-383">Атрибут *Name* определяет идентификатор канала, который используется для передачи ODT в configuration.xml как атрибут канала.</span><span class="sxs-lookup"><span data-stu-id="67154-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="67154-384">Пример: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="67154-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="67154-385">Этот атрибут является устаревшим и используется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="67154-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="67154-386">Использование атрибута ID вместо атрибута Name.</span><span class="sxs-lookup"><span data-stu-id="67154-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="67154-387">В атрибуте *ID* определяет идентификатор канала, который используется для передачи ODT в configuration.xml как атрибут канала.</span><span class="sxs-lookup"><span data-stu-id="67154-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="67154-388">Пример: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="67154-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="67154-389">Атрибут **DisplayName** используется в качестве отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="67154-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="67154-390">\*\* \<Обновление\> \*\* узел используется для определения каждого обновления, который был опубликован для конкретного канала.</span><span class="sxs-lookup"><span data-stu-id="67154-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="67154-391">**Новейшие** атрибут, если значение True, определяет выпуска, который является последнего выпуска для этого канала.</span><span class="sxs-lookup"><span data-stu-id="67154-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="67154-392">Атрибут **Version** определяет номер версии для этого конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="67154-393">Атрибут **LegacyVersion** определяет полный номер версии для этого конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="67154-394">Атрибут **построения** определяет номер сборки для данного конкретного обновления.</span><span class="sxs-lookup"><span data-stu-id="67154-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="67154-395">Атрибут **PubTime** определяет дату и время публикации это обновление Office CDN.</span><span class="sxs-lookup"><span data-stu-id="67154-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

