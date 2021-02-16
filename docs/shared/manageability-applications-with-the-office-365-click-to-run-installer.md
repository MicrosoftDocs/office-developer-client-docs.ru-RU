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
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Интеграция приложений для управления с установщиком приложений Microsoft 365 "нажми и запускай"

Узнайте, как интегрировать установщик приложений Microsoft 365 "нажми и запускай" с решением для управления программным обеспечением.
  
Установщик приложений Microsoft 365 "нажми и запускай" предоставляет интерфейс COM, который позволяет ИТ-специалистам и решениям для управления программным обеспечением управлять управлением обновлениями. Этот интерфейс предоставляет дополнительные возможности управления помимо возможностей, предоставляемых средством развертывания Office.
  
> [!NOTE]
> Эта статья относится к приложениям Office, которые используют установщик "нажми и нажми и выйми". 
  
## <a name="integrating-with-the-click-to-run"></a>Интеграция с технологией "нажми и запускай"

Чтобы использовать этот интерфейс, приложение управляемости вызывает интерфейс COM и вызывает открытые API, которые взаимодействуют непосредственно со службой установки "нажми ижми и запускай". 
  
> [!NOTE]
> Установщик Office "нажми и запускай" можно запустить из командной строки с параметрами, которые могут управлять поведением, как описано в средстве развертывания Office для "нажми и нажми [и запускай".](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool) 
  
**Ниже приведена концептуальная схема интерфейса COM**

![Схема использования интерфейса COM в установщике Office нажми и работай.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования com-интерфейса в установщике office "нажми и нажми"")
  
Установщик приложений Microsoft 365 "нажми и запускай" реализует интерфейс на основе **COM, IUpdateNotify,** зарегистрированный в CLSID **CLSID_UpdateNotifyObject.**
  
Этот интерфейс можно вызвать следующим образом:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

Вызов будет успешным только в том случае, если вызываемая программа работает с повышенными привилегиями, так как программа установки "нажми ижми и нажми ий" должна быть запущена с повышенными привилегиями.
  
Com-интерфейс **IUpdateNotify** предоставляет три асинхронные функции, отвечающие за проверку команд и параметров и планирование выполнения с помощью службы установки "нажми и выполнив". 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

С помощью метода **Status** можно получить сведения о состоянии последней выполненной команды или состоянии исполняемой команды (например, об успешном выполнении, сбое, подробных кодах ошибок).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

В течение жизненного цикла службы установки "нажми и выполнив" может быть четыре состояния, во время которых могут быть вызваны методы **IUpdateNotify;** Перезагрузка, бездействие, загрузка и применение. 
  
**Ниже приведена схема автомата интерфейса COM**

![Схема состояний для интерфейса COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Схема состояния для интерфейса COM")
  
> [!NOTE]
> **Перезагрузка:** когда компьютер загружается, в течение некоторого времени служба установщика "нажми и запускай" недоступна. Успешный вызов метода Status после перезагрузки возвращает eUPDATE_UNKNOWN. 
  
**Бездействие:** Когда установщик "нажми и запускай" находится в состоянии простоя, можно вызвать: 
  
- **Apply**: Install previously downloaded content.
    
- **Cancel**: returns  `0x800000e` , "A method was called at an unexpected time".
    
- **Download**: Downloads new content to the client for later installation.
    
- **Status**: возвращает результат последнего выполненного действия или сообщение об ошибке, если действие завершилось сбоем. Если предыдущее действие не было, **возвращается**  `eUPDATE_UNKNOWN` состояние.
    
**Загрузка:** Когда установщик "нажми и запускай" находится в состоянии скачивания, вы можете вызвать: 
  
- **Apply**: возвращает **HRESULT** со значением  `0x800000e` "Метод был вызван в непредвиденное время".
    
- **Отмена:** останавливает скачивание и удаляет частично загруженное содержимое.
    
- **Download**: Returns an **HRESULT** with the value  `0x800000e` , "A method was called at an unexpected time". 
    
- **Состояние:** возвращает **DOWNLOAD_WIP,** чтобы указать, что загрузка уже идет. 
    
**Применение:** Когда установщик "нажми ижми и запускай" устанавливает ранее скачиваемые материалы: 
  
- **Apply**: возвращает **HRESULT** со значением  `0x800000e` "Метод был вызван в непредвиденное время".
    
- **Cancel**: Returns  `0x800000e` , the Apply action cannot be canceled.
    
- **Download**: Returns an **HRESULT** with the value  `0x800000e` , "A method was called at an unexpected time". 
    
- **Status**: возвращает **APPLY_WIP,** чтобы указать, что идет применение работы. 
    
> [!NOTE]
> Так как OfficeC2RCOM — это служба COM+ и динамически загружается, необходимо вызывать **CoCreateInstance** каждый раз при вызове метода для этого класса, чтобы получить ожидаемый результат. При необходимости служба COM+ будет обрабатывать создание нового экземпляра. Когда один из методов будет вызван в первый раз, COM+ загрузит объект **IUpdateNotify** и запустит его в одном из dllhost.exe экземпляров. Новый объект будет оставаться активным около 3 минут в бездействии. Если последующий вызов будет выполнен в течение трех минут после последнего вызова, объект **IUpdateNotify** останется загруженным, а новый экземпляр не будет создан. Если вызов не будет выполнен в течение трех минут, объект IUpdateNotify будет выгружен, и при следующем вызове будет создан новый объект **IUpdateNotify.** 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Справочник по API COM установщика "нажми ижми и запускай"

В следующей справочной документации по API:
  
- Параметры имеют формат пары "ключ-значение", разделенный пробелом.
    
- Параметры не чувствительны к делу.
    
- Существует список [параметров с](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) доступной документацией. 
    
- Теперь включается сводка интерфейса IUpdateNotify2.
    
### <a name="apply"></a>Применить

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Параметры

-  _displaylevel_: **true,** чтобы показать состояние установки, включая ошибки, во время процесса обновления; **false,** чтобы скрыть состояние установки, включая ошибки, во время процесса обновления. Значение по умолчанию: **false**.
    
-  _forceappshutdown_: **true,** чтобы принудительно отключить приложения Office сразу после запуска действия **Apply;** **false** для сбой, если запущены какие-либо приложения Office. Значение по умолчанию: **false**. Дополнительные [сведения см.](#bk_ApplyRemark) в примечаиях. 
    
  Если при запуске действия **Apply** запущено любое приложение Office, действие **Apply** обычно не будет работать. При передаче в метод Apply служба `forceappshutdown=true` **OfficeClickToRun** немедленно закрывает приложения и применяет обновление.  В этом случае у пользователя может возникнуть потеря данных. 
    
#### <a name="return-results"></a>Возврат результатов

|||
|:-----|:-----|
|**S_OK** <br/> |Действие успешно отправлено в службу "Нажми и запускай" для выполнения.  <br/> |
|**E_ACCESSDENIED** <br/> |Вызываемая не работает с повышенными привилегиями.  <br/> |
|**E_INVALIDARG** <br/> |Переданы недопустимые параметры.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Действие в настоящее время запрещено. Дополнительные [сведения см.](#bk_ApplyRemark) в примечаиях.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Примечания

- Если при запуске действия **Apply** запущено любое приложение Office, действие **Apply** не будет работать. При передаче в метод Apply служба `forceappshutdown=true` **OfficeClickToRun** немедленно отключает все запущенные приложения Office и применяет обновление.  У пользователя могут возникнуть данные, так как им не будет предложено сохранить изменения для открытия документов. 
    
- Это действие может быть инициировано только в том случае, если состояние COM имеет одно из следующих действий: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Если вызвать метод **Apply** без предварительной загрузки содержимого, метод **Apply** будет сообщать об успешном результате, так как он не обнаружил ничего для применения и успешно завершил процесс **применения.**  
    
### <a name="cancel"></a>"Отмена"

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Возврат результатов

|||
|:-----|:-----|
|S_OK  <br/> |Действие успешно отправлено в службу "нажми и запускай" для выполнения.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Действие в настоящее время запрещено. Дополнительные [сведения см.](#bk_CancelRemarks) в разделе "Замечания"  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Примечания

- Этот метод может запускаться только при eDOWNLOAD_WIP **состояния** COM. Он попытается отменить текущее действие загрузки. Состояние COM изменится на **eDOWNLOAD_CANCELLING** и в конечном итоге изменится на **eDOWNLOAD_CANCELED.** Состояние COM возвращает **E_ILLEGAL_METHOD_CALL,** если он активируется в любое другое время. 
    
### <a name="download"></a>Скачать

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Параметры

-  _displaylevel_: **true,** чтобы показать состояние установки, включая ошибки, во время процесса обновления; **false,** чтобы скрыть состояние установки, включая ошибки, во время процесса обновления. Значение по умолчанию: **false**.
    
-  _updatebaseurl_: URL-адрес альтернативного источника загрузки.
    
-  _updatetoversion_: версия для обновления Office. Определите этот параметр, если вы хотите обновить более старую версию, чем установленная в данный момент версия.
    
-  _downloadsource_: CLSID настраиваемой реализации **IBackgroundCopyManager** (диспетчер BITS). 
    
-  _contentid_: определяет содержимое, которое необходимо скачать с сервера контента с помощью настроенного диспетчера BITS. Это значение передается через интерфейс BITS для интерпретации.
    
#### <a name="return-results"></a>Возврат результатов

|||
|:-----|:-----|
|**S_OK** <br/> |Действие успешно отправлено в службу "Нажми и запускай" для выполнения.  <br/> |
|**E_ACCESSDENIED** <br/> |Вызываемая не работает с повышенными привилегиями.  <br/> |
|**E_INVALIDARG** <br/> |Переданы недопустимые параметры.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Действие в настоящее время запрещено. Дополнительные [сведения см.](#bk_DownloadRemark) в примечаиях.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Примечания

- В качестве пары необходимо указать _downloadsource_ и _contentid._ В этом случае метод **download** возвращает ошибку E_INVALIDARG **ошибке.** 
    
- Если  _предоставлены downloadsource,_  _contentid_ и  _updatebaseurl,_  _updatebaseurl_ будет игнорироваться. 
    
- Это действие может быть инициировано только в том случае, если состояние COM имеет одно из следующих действий: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Если вызвать метод **Apply** без ранее загруженного содержимого, метод **Apply** будет сообщать об успешном результате, так как он не обнаружил ничего для применения и успешно завершил процесс **применения.**  
    
#### <a name="examples"></a>Примеры

- Чтобы скачать содержимое из настроенного диспетчера BITS, вызовите функцию **download(),** передав следующие параметры: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Чтобы скачать содержимое из сети доставки содержимого Office (CDN): вызовите функцию **download()** без указания параметров _downloadsource,_ _contentid_ или _updatebaseurl._ 
    
- Чтобы скачать содержимое из настраиваемой области, вызовите функцию **download(),** передав следующий параметр: 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>Состояние

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>Параметры

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Указатель на UPDATE_STATUS_REPORT структуру.  <br/> |
   
#### <a name="return-results"></a>Возврат результатов

|||
|:-----|:-----|
|**S_OK** <br/> |Метод **Status** всегда возвращает этот результат. Проверьте  `UPDATE_STATUS_RESULT` структуру на состояние текущего действия.  <br/> |
   
#### <a name="remarks"></a>Примечания

- Поле состояния содержит  `UPDATE_STATUS_REPORT` состояние текущего действия. Возвращается одно из следующих значений состояния: 
    
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

- Если последняя команда приводит к ошибке, поле ошибки содержит  `UPDATE_STATUS_REPORT` подробные сведения об ошибке. Из метода Status возвращаются два типа кодов **ошибок.** 
    
- Если ошибка меньше, ошибка является одним из следующих  `UPDATE_ERROR_CODE::eUNKNOWN` предопределеных кодов ошибок:
    
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

  Если код возвращаемой ошибки превышает  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT** неудачного вызова функции. Извлечение вычитания HRESULT из значения, возвращаемого в поле  `UPDATE_ERROR_CODE::eUNKNOWN` ошибки  `UPDATE_STATUS_REPORT` .
    
  Полный список значений состояния и ошибок можно просмотреть, проверив библиотеку типов **IUpdateNotify,** внедренную в OfficeC2RCom.dll. 
    
- Поле contentid используется для  вызовов  состояния после инициалов загрузки и возвращает contentid, переданный в вызов **загрузки.** Перед вызовом метода **Status** лучше всего инициализировать это поле в  значение **NULL,** а затем проверить значение после возврата состояния. Если значение по-прежнему равно **null,** это означает, что не возвращается contentid. Если значение не **null,** необходимо освободить его с помощью вызова **SysFreeString()**. Вот фрагмент кода о вызове **состояния** после **скачивания.**
    
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

### <a name="summary-of-iupdatenotify2-interface"></a>Сводка интерфейса IUpdateNotify2

В версии [16.0.8208.6352] мы добавили новый **интерфейс IUpdateNotify2.** 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- В этом интерфейсе также был исходного интерфейса IUpdateNotify для обеспечения обратной совместимости. Это означает, что при использовании этого интерфейса у вас есть доступ ко всем методам, предоставляемым в **интерфейсе UpdateNotifyObject.** 
    
- Новые методы, добавленные в IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Получать обновления, блокирующие список приложений. Этот вызов возвратит запущенные приложения Office, которые заблокируют процесс обновления. 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Получите данные о развертывании Office. 
    
- Если вы хотите использовать новые методы, убедитесь, что:
    
  - Ваша версия C2R новее, чем сборка выше ( \> = июньская сборка ветвей).
    
  - Используйте UpdateNotifyObject2 вместо **UpdateNotifyObject** для вызова **CoCreateInstance.**
    
Если вы не используете ни один из новых методов, вам не нужно ничего менять. Все существующие методы будут работать точно так же, как и раньше.
  
## <a name="implementing-the-bits-interface"></a>Реализация интерфейса BITS

Служба [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) — это служба, предоставляемая корпорацией Майкрософт для передачи файлов между клиентом и сервером. BITS — это один из каналов, которые установщик office "нажми и запуск" может использовать для скачивания содержимого. По умолчанию установщик приложений Microsoft 365 "нажми и запускай" использует встроенную в Windows реализацию BITS для скачивания содержимого из CDN. 
  
Предоставляя настраиваемую реализацию BITS методу **загрузки ()** интерфейса **IUpdateNotify,** ваше программное обеспечение управляемости может контролировать, где и как клиент загружает содержимое. Настраиваемый интерфейс BITS полезен при предоставлении настраиваемого канала распространения содержимого, кроме встроенных каналов "нажми и запускай", таких как СЕТЬ CDN, серверы IIS или файловые папки. 
  
Минимальное требование к пользовательскому интерфейсу BITS для работы со службой Office C2R:
  
- Для **IBackgroundCopyManager:**
    
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

- Для **IBackgroundCopyJob:**
    
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

- Для **IBackgroundCopyJob3:**
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Для  `Addfile`  `AddFileWithRanges` функций удаленный URL-адрес имеет следующий формат: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits жестко закодировать и означает настраиваемые BITS.
    
  -  _\<contentid\>_ является _параметром contentid_ для метода **Download().** 
    
  -  _\<relative path to target file\>_ предоставляет расположение и имя файла для скачивания. 
    
    Например, если вы предоставили _contentid_ метода Download(), а Office C2R хочет скачать CAB-файл версии, например файл, он будет вызывать `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** со следующими данными: `RemoteUrl`
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Для **IBackgroundCopyError:**
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Для **IBackgroundCopyFile:**
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a>Автоматизация промежуточного содержимого

ИТ-администраторы могут включить для классических клиентов автоматическое получение обновлений, когда они доступны непосредственно из СЕТИ CDN, или управлять развертыванием обновлений, доступных из каналов обновления, с помощью средства развертывания Office или Microsoft Endpoint Configuration Manager.
  
Служба поддерживает возможность средств управления распознавать и автоматизировать загрузку содержимого при наличии доступных обновлений.
  
**На следующем изображении представлен обзор загрузки пользовательского образа**

![Схема использования интерфейса COM в установщике Office нажми и работай.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования com-интерфейса в установщике office "нажми и нажми"")
  
### <a name="overview-of-downloading-a-custom-image"></a>Обзор загрузки пользовательского образа
  
На предыдущей схеме видно, что в CDN доступен новый образ приложений Microsoft 365. Наряду с изображением приложений Microsoft 365 доступен API, который включает сведения, необходимые для обеспечения управляемости программного обеспечения для непосредственного создания настраиваемых образов, заменяющих необходимость использования средства развертывания Office.

Предприятие настраивает службы WSUS для синхронизации обновлений приложений Microsoft 365. Эти обновления не содержат фактических полезной нагрузки изображения, но позволяют программному обеспечению управляемости распознавать доступность нового содержимого. Затем программное обеспечение для управления может прочитать метаданные Обновления приложений Microsoft 365, чтобы понять, к какой версии Office применяется обновление.

Если обновление применимо, программное обеспечение для управления может использовать содержимое CDN и список файлов для создания пользовательского образа и его хранения в расположении файлового папки, которое оно настроено для использования.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Использование API списка файлов приложений Microsoft 365

API списка файлов приложений Microsoft 365 используется для получения имен файлов, необходимых для конкретного обновления приложений Microsoft 365.

HTTP-запрос

GET https://config.office.com/api/filelist

Не указывайте текст запроса для этого метода.

Для вызова этого API не требуются разрешения.

Необязательные параметры запросов

|**Название**|**Описание**|
|:-----|:-----|
| channel <br/>| Указывает имя канала  <br/> Необязательный — значение по умолчанию " SemiAnnual" <br/> Поддерживаемые значения https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| version <br/>| Указывает версию обновления <br/> Необязательный — по умолчанию установлена последняя версия, доступная для указанного канала |
| arch <br/>| Указывает архитектуру клиента <br/> Необязательный — значение по умолчанию — "x64" <br/> Поддерживаемые значения: x64, x86 |
| крышка <br/>| Указывает языковые файлы, которые необходимо включить <br/> Необязательный — значение по умолчанию — нет <br/> Чтобы указать несколько языков, включите параметр запроса крышки для каждого языка <br/> Используйте формат идентификатора языка, ex. "en-us", "fr-fr" |
| alllanguages <br/>| Указывает, что необходимо включить все языковые файлы <br/> Необязательный — значение по умолчанию — false |

HTTP-ответ

В случае успеха этот метод возвращает код отклика 200 OK и коллекцию объектов файла в тексте отклика.

Чтобы создать образ, выполните следующие действия:
1.  Вызовите API, предоставив соответствующие параметры запроса для канала, версии и архитектуры интересующих вас обновлений.
Примечание. Объекты-файлы с атрибутом "lcid": "0" являются нейтральными для языка файлами и должны быть включены в изображение.
2.  Создадим локальное изображение CDN, протерируя объекты файлов и копируя файлы CDN, создавая структуру папок в зависимости от атрибута relativePath, определенного для каждого объекта файла.

В следующем примере извлекается список файлов для Current Channel и версии 16.0.4229.1004 для 64-битных и включаются файлы французского и английского языков:

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Hash verification of .dat files

Средства создания изображений могут проверять целостность загруженных DAT-файлов, сравнивая вычисленное значение hash с предоставленным значением hash, связанным с каждым DAT-файлом. Ниже приводится пример объекта файла, который указывает значения hashLocation и hashAlgorithm:
  
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

- Атрибут **hashLocation** указывает относительный путь CAB-файла, который содержит значение hash. Сконструировать расположение файла hash, совметив URL-адрес + relativePath + hashLocation. В следующем примере расположение stream.x64.bg-bg.hash будет следующим: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- Атрибут **hashAlgorithm** указывает, какой алгоритм был использован. 
    
  Чтобы проверить целостность файла stream.x64.bg-bg.dat, откройте файл stream.x64.bg-bg.hash и прочитайте значение HASH, которое является первой строкой текста в hash-файле. Сравните это с вычисленным значением hash (с использованием указанного алгоритма hashing), чтобы проверить целостность загруженного DAT-файла.
    
  В следующем примере показан код C# для чтения хэш-кода.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Обновления приложений Microsoft 365

Все обновления приложений Microsoft 365 публикуются в [каталоге обновлений Майкрософт.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)
  
Обновления приложений Microsoft 365 позволяют управляемому программному обеспечению обрабатывать обновления приложений Microsoft 365 так, как любое другое обновление WU за одним исключением; обновления клиента не содержат фактических полезной нагрузки. Обновления приложений Microsoft 365 не следует устанавливать ни на каких клиентах, а использовать для запуска рабочего процесса с помощью программного обеспечения для управления, заменив команду установки механизмом установки на основе COM, показанным выше.

**На следующем рисунке показана схема рабочего процесса обновления клиента Office 365.**

![Схема рабочего процесса для обновлений клиента O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Схема рабочего процесса для обновлений клиента O365PP")
  
Каждое опубликованное обновление приложений Microsoft 365 включает метаданные об обновлении. Эти метаданные включают параметр MoreInfoUrl, который можно использовать для получения вызова API для API списка файлов для конкретного обновления.

В следующем примере API списка файлов внедрен в MoreInfoURL и начинается с "ServicePath="

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Дополнительные метаданные для автоматизации промежуточного содержимого

**API истории выпусков**
  
API истории выпусков приложений Microsoft 365 используется для получения сведений о каждом из обновлений, опубликованных в CDN, а также имен каналов и других атрибутов канала.

HTTP-запрос

```http
GET https://config.office.com/api/filelist/channels 
```

Не указывайте текст запроса для этого метода.

Для вызова этого API не требуются разрешения.

HTTP-ответ

В случае успеха этот метод возвращает код отклика 200 OK и коллекцию объектов файла в тексте отклика.

**API-API для skus**
  
API skus возвращает сведения, которые полезны для определения продуктов, доступных для развертывания и обслуживания из CDN Office, а также различные параметры для каждого из них.

HTTP-запрос

```http
GET https://config.office.com/api/filelist/skus 
```

Не указывайте текст запроса для этого метода.

Для вызова этого API не требуются разрешения.

HTTP-ответ

В случае успеха этот метод возвращает код отклика 200 OK и коллекцию объектов файла в тексте отклика.
