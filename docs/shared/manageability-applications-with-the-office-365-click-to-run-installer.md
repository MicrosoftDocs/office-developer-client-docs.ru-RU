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
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a>Интеграция приложений управления с помощью установщика Office 365 нажми и работай

Узнайте, как интегрировать установщик Office 365 нажми и работай с решением управления программным обеспечением.
  
Установщик Office 365 нажми и работай предоставляет COM-интерфейс, который позволяет ИТ-специалистам и решениям управления программным способом управлять управлением обновлениями. Этот интерфейс предоставляет дополнительные возможности управления помимо того, что предоставляется средством развертывания Office.
  
> [!NOTE]
> Эта статья относится к Office 2016 и более поздних версий, Office 365. 
  
## <a name="integrating-with-the-click-to-run"></a>Интеграция с "нажми и работай"

Чтобы использовать этот интерфейс, приложение управляемости вызывает COM-интерфейс и вызывает интерфейсы API, напрямую взаимодействующие с службой установки "нажми и работай". 
  
> [!NOTE]
> Установщик Office нажми и работай можно запустить из командной строки с параметрами, которые могут управлять поведением, как описано в разделе [средство развертывания Office для "нажми](https://www.microsoft.com/en-us/download/details.aspx?id=49117)и работай". 
  
**Ниже приведена концептуальная схема COM-интерфейса**

![Схема использования интерфейса COM в установщике Office "нажми] и работай". (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования интерфейса COM в установщике Office \"нажми") и работай"
  
Установщик Office 365 Click-to-Run реализует интерфейс на основе COM, **иупдатенотифи** зарегистрированный в CLSID **клсид_упдатенотифйобжект**.
  
Этот интерфейс можно вызвать следующим образом:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

Вызов будет успешным только в том случае, если вызывающий абонент работает с повышенными привилегиями, так как программа установки "нажми и работай" должна выполняться с повышенными привилегиями.
  
COM-интерфейс **иупдатенотифи** предоставляет три асинхронные функции, ответственные за проверку команд и параметров и выполнение планирования с помощью службы установки "нажми и работай". 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Метод, **Status**, может использоваться для получения сведений о состоянии последней выполненной команды или о состоянии выполняемой в данный момент команды (например, успех, сбой, подробные коды ошибок).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Во время жизненного цикла служба установки "нажми и работай" может находиться в четырех состояниях, в которых могут вызываться методы **иупдатенотифи** ; Перезагрузка, безДействие, Загрузка и применение. 
  
**Ниже показана схема конечного автомата COM-интерфейса**

![Схема состояний для интерфейса COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Схема состояний для интерфейса COM")
  
> [!NOTE]
> **Перезагрузка**: при загрузке компьютера в случае недоступности службы установки "нажми и работай" происходит определенный период времени. Успешный вызов метода status после перезагрузки возвратит Еупдате_ункновн. 
  
**Бездействие:** Когда установщик "нажми и работай" находится в состоянии простоя, вы можете вызвать: 
  
- **Apply**: установка ранее загруженного контента.
    
- **Cancel**: возвращает `0x800000e`, "метод был вызван в непредвиденное время."
    
- **Download**: Загрузка нового контента в клиент для последующей установки.
    
- **Status**: возвращает результат последнего выполненного действия или сообщение об ошибке, если действие завершилось с ошибкой. Если предыдущее действие отсутствует, `eUPDATE_UNKNOWN`возвращается **состояние** .
    
**Скачивание:** Когда установщик "нажми и работай" находится в состоянии загрузки, вы можете вызвать: 
  
- **Apply**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время".
    
- **Отмена**: остановка скачивания и удаление частично загруженного контента.
    
- **Download**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время". 
    
- **Status**: возвращает **довнлоад_вип** , чтобы указать, что выполняется загрузка. 
    
**Применение:** Когда установщик "нажми и работай" находится в процессе установки ранее загружаемого содержимого: 
  
- **Apply**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время".
    
- **Cancel**: возвращает `0x800000e`, действие Apply не может быть отменено.
    
- **Download**: возвращает **HRESULT** со значением `0x800000e`"метод был вызван в непредвиденное время". 
    
- **Status**: возвращает **аппли_вип** , чтобы указать, что выполняется работа. 
    
> [!NOTE]
> Так как OfficeC2RCOM является службой COM+ и динамически загружается, вам необходимо вызвать функцию **CoCreateInstance** при каждом вызове метода для этого класса, чтобы убедиться, что вы получаете ожидаемый результат. При необходимости служба COM+ будет обрабатывать создание нового экземпляра. Когда один из методов вызывается в первый раз, COM+ загрузит объект **иупдатенотифи** и запустите его в одном из экземпляров Dllhost. exe. Новый объект остается активным в течение приблизительно 3 минут. Если последующий вызов выполняется через три минуты последнего вызова, объект **иупдатенотифи** останется загруженным, а новый экземпляр не будет создан. Если в течение трех минут ничего не происходит, объект Иупдатенотифи будет выгружен, а при следующем вызове будет создан новый объект **иупдатенотифи** . 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Справочное руководство по API-ИНТЕРФЕЙСу API для установщика "нажми и работай"

В следующей справочной документации по API:
  
- Параметры представлены в формате "ключ-значение", разделенном пробелом.
    
- В параметрах регистр не учитывается.
    
- Существует [список параметров](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) , доступных в документации. 
    
- Сводка интерфейса IUpdateNotify2 теперь включена.
    
### <a name="apply"></a>Применить

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Параметры

-  _displaylevel_: **true** , чтобы показать состояние установки, включая ошибки, во время процесса обновления; **значение false** , чтобы скрыть состояние установки, включая ошибки, во время процесса обновления. Значение по умолчанию: **false**.
    
-  _forceappshutdown_: **true** для принудительного завершения работы приложений Office при запуске действия **Apply** ; в противном случае — **false** . Значение по умолчанию: **false**. Дополнительные [](#bk_ApplyRemark) сведения см. 
    
  Если какое-либо приложение Office запускается при запуске действия **Apply** , действие **Применить** обычно завершится с ошибками. Передача `forceappshutdown=true` в метод **Apply** приведет к тому, что служба **оффицекликкторун** сразу же завершит работу приложений и применит обновление. В этом случае в работе пользователя могут возникать потери данных. 
    
#### <a name="return-results"></a>Возвращаемые результаты

|||
|:-----|:-----|
|**S_OK** <br/> |Действие успешно отправлено службе "нажми и работай" для выполнения.  <br/> |
|**Е_АКЦЕССДЕНИЕД** <br/> |Вызывающий абонент не работает с повышенными привилегиями.  <br/> |
|**E_INVALIDARG** <br/> |Переданы неДопустимые параметры.  <br/> |
|**Е_ИЛЛЕГАЛ_МЕСОД_КАЛЛ** <br/> |В настоящее время действие не разрешено. Дополнительные [](#bk_ApplyRemark) сведения см.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Комментарии

- Если какое-либо приложение Office запускается при запуске действия **Apply** , действие **Apply** завершится с ошибками. При `forceappshutdown=true` передаче в метод **Apply** служба **оффицекликкторун** немедленно завершит работу всех запущенных приложений Office и применить обновление. Пользователь может столкнуться с данными, так как они не получают запроса на сохранение изменений в открытых документах... 
    
- Это действие может быть вызвано только в том случае, если состоянием COM является один из следующих: 
    
  - **Еупдате_ункновн**
    
  - **Едовнлоад_канцеллед**
    
  - **Едовнлоад_фаилед**
    
  - **Едовнлоад_сукцеедед**
    
  - **Еаппли_сукцеедед**
    
  - **Еаппли_фаилед**
    
- При вызове метода **Apply** без предварительной загрузки содержимого метод **Apply** будет сообщать об **успешном** завершении, так как он не обнаружил, что успешно применялся и завершил процесс **применения** . 
    
### <a name="cancel"></a>Отмена

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Возвращаемые результаты

|||
|:-----|:-----|
|S_OK  <br/> |Действие успешно отправлено службе "нажми и работай" для выполнения.  <br/> |
|Е_ИЛЛЕГАЛ_МЕСОД_КАЛЛ  <br/> |В настоящее время действие не разрешено. Для получения дополнительных сведений см раздел ["Примечания](#bk_CancelRemarks) ".  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Комментарии

- Этот метод может быть вызван только в том случае, если идентификатор состояния COM **едовнлоад_вип**. Будет предпринята попытка отменить текущее действие скачивания. Состояние COM изменится на **едовнлоад_канцеллинг** и в конечном итоге изменится на **едовнлоад_канцелед**. Состояние COM возвращает значение **е_иллегал_месод_калл** , если триггер запускается в любое другое время. 
    
### <a name="download"></a>Скачать

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Параметры

-  _displaylevel_: **true** , чтобы показать состояние установки, включая ошибки, во время процесса обновления; **значение false** , чтобы скрыть состояние установки, включая ошибки, во время процесса обновления. Значение по умолчанию: **false**.
    
-  _упдатебасеурл_: URL-адрес альтернативного источника скачивания.
    
-  _упдатетоверсион_: версия для обновления Office. Определите этот параметр, если необходимо обновить более старую версию, чем версия, установленная в данный момент.
    
-  _довнлоадсаурце_: CLSID настраиваемой реализации **ИБАККГРАУНДКОПИМАНАЖЕР** (диспетчер BITS). 
    
-  Идентификатор _ContentId_: определяет содержимое для загрузки с сервера контента через настраиваемый диспетчер BITS. Это значение передается через интерфейс BITS для интерпретации.
    
#### <a name="return-results"></a>Возвращаемые результаты

|||
|:-----|:-----|
|**S_OK** <br/> |Действие успешно отправлено службе "нажми и работай" для выполнения.  <br/> |
|**Е_АКЦЕССДЕНИЕД** <br/> |Вызывающий абонент не работает с повышенными привилегиями.  <br/> |
|**E_INVALIDARG** <br/> |Переданы неДопустимые параметры.  <br/> |
|**Е_ИЛЛЕГАЛ_МЕСОД_КАЛЛ** <br/> |В настоящее время действие не разрешено. Дополнительные [](#bk_DownloadRemark) сведения см.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Комментарии

- Необходимо указать _довнлоадсаурце_ и идентификатор _ContentId_ в виде связывания. В противном случае метод **download** возвратит ошибку **е_инвалидарг** . 
    
- Если указаны _довнлоадсаурце_, _ContentId_и _упдатебасеурл_ , _упдатебасеурл_ будет игнорироваться. 
    
- Это действие может быть вызвано только в том случае, если состоянием COM является один из следующих: 
    
  - **Еупдате_ункновн**
    
  - **Едовнлоад_канцеллед**
    
  - **Едовнлоад_фаилед**
    
  - **Едовнлоад_сукцеедед**
    
  - **Еаппли_сукцеедед**
    
  - **Еаппли_фаилед**
    
- При вызове метода **Apply** без ранее скачанного содержимого метод **Apply** будет сообщать об **успешном** завершении, так как он не обнаружил, что успешно применялся и завершил процесс **применения** . 
    
#### <a name="examples"></a>Примеры

- Чтобы скачать содержимое из настраиваемого диспетчера BITS: выЗовите функцию **скачать ()** , передав следующие параметры: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Чтобы скачать содержимое из сети CDN Microsoft CDN: выЗовите функцию **скачать ()** , не указывая параметры _довнлоадсаурце_, _ContentId_или _упдатебасеурл_ . 
    
- Чтобы скачать содержимое из настраиваемого расположения: выЗовите функцию **скачать ()** , передав следующий параметр: 
    
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
| _Пупдатестатусрепорт_ <br/> |Указатель на структуру УПДАТЕ_СТАТУС_РЕПОРТ.  <br/> |
   
#### <a name="return-results"></a>Возвращаемые результаты

|||
|:-----|:-----|
|**S_OK** <br/> |Метод **Status** всегда возвращает этот результат. Проверка `UPDATE_STATUS_RESULT` структуры на состояние текущего действия.  <br/> |
   
#### <a name="remarks"></a>Комментарии

- В поле Status ( `UPDATE_STATUS_REPORT` состояние) содержится состояние текущего действия. Возвращается одно из следующих значений состояния: 
    
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

- Если последняя команда привела к ошибке, в поле ошибка `UPDATE_STATUS_REPORT` содержится подробная информация об ошибке. В методе **Status** возвращается два типа кодов ошибок. 
    
- Если ошибка меньше `UPDATE_ERROR_CODE::eUNKNOWN`, то ошибка является одним из следующих предварительно определенных кодов ошибок:
    
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

  Если код ошибки возврата превышает `UPDATE_ERROR_CODE::eUNKNOWN` значение **HRESULT** неудачного вызова функции. Чтобы извлечь значение HRESULT, `UPDATE_ERROR_CODE::eUNKNOWN` вычитаемое из значения, которое возвращается в поле `UPDATE_STATUS_REPORT`"ошибка".
    
  Полный список значений состояния и ошибок можно просмотреть, изучив библиотеку типов **иупдатенотифи** , встроенную в OfficeC2RCom. dll. 
    
- Поле ContentId используется для вызовов с состоянием **** после **загрузки** и возвращает идентификатор ContentId, переданный в вызов **загрузки** . Рекомендуется инициализировать это поле до **значения NULL** перед вызовом метода **Status** , а затем проверить значение после того, как было возвращено значение **Status** . Если значение по-прежнему равно **null**, это означает, что идентификатор ContentId не возвращается. Если значение отлично от **null**, его необходимо освободить с помощью вызова **SysFreeString ()**. Ниже приведен фрагмент кода, посвященный вызову **состояния** после **загрузки**.
    
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

### <a name="summary-of-iupdatenotify2-interface"></a>Сводка по интерфейсу IUpdateNotify2

> [!NOTE]
> Эта сводка предоставляется в качестве приветственной информации о [том, как интегрировать приложения управления с установщикОм Office 365 нажми](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx)и работай. После обновления общедоступного документа этот документ можно считать устаревшим. 
  
В C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (первая общедоступная сборка должна быть в июне сборка--8326. *) мы добавили новый интерфейс **IUpdateNotify2** . Ниже представлено несколько основных сведений об этом интерфейсе. 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2 — F1AC – 4021 – BF50 – 756A5FA8DDFE}
    
- Этот интерфейс также размещает исходный интерфейс Иупдатенотифи для обеспечения обратной совместимости. Это означает, что при использовании этого интерфейса вы можете получить доступ ко всем методам, предоставляемым в интерфейсе **упдатенотифйобжект** . 
    
- Новые методы, добавленные в IUpdateNotify2:
    
  - **HRESULT** Жетблоккингаппс ([выходной] BSTR \* аппслист). Получение списка заблокированных приложений для обновления. Этот вызов возвратит запуск приложений Office, которые будут блокировать процесс обновления. 
    
  - **HRESULT** Жетоффицедеплойментдата ([in] int dataType, [in] **значение LPCWSTR** пквсзнаме, [out] BSTR * оффицедата). Получение данных развертывания Office. 
    
- Если вы хотите использовать новые методы, необходимо убедиться в том, что:
    
  - Ваша версия C2R более новая, чем приведенная выше\>сборка (= с помощью построения разветвления за июнь).
    
  - Используйте UpdateNotifyObject2, а не **упдатенотифйобжект** , чтобы вызвать функцию **CoCreateInstance**.
    
Если вы не используете ни один из новых методов, вам не нужно ничего менять. Все существующие методы будут работать точно так же, как и раньше.
  
## <a name="implementing-the-bits-interface"></a>Реализация интерфейса BITS

[ФоновАя интеллектуальнАя служба передачи](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (BITS) — это служба, предоставляемая корпорацией Майкрософт для передачи файлов между клиентом и сервером. BITS это один из каналов, которые может использовать установщик Office нажми и работай для загрузки контента. По умолчанию установщик Office нажми и работай использует встроенную в Windows реализацию BITS для загрузки содержимого из сети CDN. 
  
Предоставляя настраиваемую реализацию BITS методу **Download ()** интерфейса **иупдатенотифи** , программное обеспечение управления может управлять тем, где и как клиент загружает контент. Настраиваемый интерфейс BITS полезен при предоставлении настраиваемого канала распространения содержимого, отличного от встроенных каналов "нажми и работай", таких как CDN CDN, серверы IIS или общие файловые ресурсы. 
  
Минимальное требование для настраиваемого интерфейса BITS для работы со службой Office C2R:
  
- Для **ибаккграундкопиманажер**:
    
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

- Для **ибаккграундкопижоб**:
    
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

- Для **IBackgroundCopyJob3**:
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Для функций `Addfile` и `AddFileWithRanges` функции and удаленный URL-адрес имеет следующий формат: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - кмбитс жестко запрограммирована, а обозначает настроенные биты.
    
  -  Идентификатор ContentId __ _\> является параметром ContentId для метода \<_ **Download ()** . 
    
  -  _относительный путь к\> целевому файлу указывает расположение и имя файла, который требуется скачать. \<_ 
    
    Например, если вы указали объект _ContentId_ `f732af58-5d86-4299-abe9-7595c35136ef` для метода **Download ()** , и Office C2R хочет скачать CAB-файл версии, например `v32.cab` File, он вызовите **аддфиле ()** , выполнив следующие `RemoteUrl`действия:
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Для **ибаккграундкоперрор**:
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Для **ибаккграундкопифиле**:
    
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

## <a name="automating-content-staging"></a>Автоматизация промежуточного хранения контента

ИТ-администраторы могут разрешить клиентам для настольных ПК автоматически получать обновления, когда они доступны непосредственно из сети доставки содержимого (CDN) Microsoft (CDN), или могут управлять развертыванием обновлений, доступных в обновлении каналы с помощью средства развертывания Office или System Center Configuration Manager.
  
Служба поддерживает возможность средств управления определять и автоматизировать загрузку контента при наличии обновлений.
  
**На следующем рисунке представлен обзор загрузки настраиваемого изображения.**

![Схема использования интерфейса COM в установщике Office "нажми] и работай". (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Схема использования интерфейса COM в установщике Office \"нажми") и работай"
  
### <a name="overview-of-downloading-a-custom-image"></a>Обзор загрузки настраиваемого изображения
  
На предыдущей схеме вы увидите, что новый образ Office 365 профессиональный плюс доступен в сети доставки содержимого Office (CDN). Вместе с изображением Office 365 профессиональный плюс доступен список файлов в формате XML, в котором есть информация, необходимая для поддержки управляемого программного обеспечения для непосредственного создания настраиваемых образов, которые заменяют необходимость использования средства развертывания Office.
  
Предприятие настраивает свои WSUS для синхронизации обновлений клиента Office 365. Эти обновления не содержат полезных данных изображения, но позволяют программному обеспечению для управления распознать, когда будет доступен новый контент. Затем программное обеспечение для управления может прочитать метаданные обновления клиента, чтобы узнать, к какой версии Office относится обновление.
  
Если обновление возможно, программное обеспечение для управления может использовать содержимое CDN и список файлов для создания настраиваемого образа и сохранения его в расположении общего файлового ресурса, который он использует.
  
### <a name="format-of-the-xml-file-list"></a>Формат списка XML-файлов

В CAB-файле сети CDN доступно два списка файлов. Один список файлов для 32 разрядной версии Office и другой для 64 — разрядной версии Office. URL-адрес списка файлов Office (ОФЛ. CAB- [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab)файл). Вызываются два списка файлов:
  
- O365Client_32bit. XML
    
- O365Client_64bit. XML
    
В XML-файле для каждого списка файлов указывается <UpdateFiles> узел, который содержит атрибут Version.  `<UpdateFiles version="1.4">`. Эта версия увеличивается при внесении изменений в списки файлов.
  
Существует два параметра, которые необходимо объединить с XML, чтобы создать настраиваемое изображение: 
  
- Замените *% Version%* на версию сборки Office. Это может быть получено из метаданных обновления клиента (описывается в следующем разделе). 
    
- Определите *baseURL* с использованием значения URL-адреса, связанного с ветвью, для которой создается изображение. Это является производным от метаданных обновления клиента, описанных в следующем разделе. 
    
Для создания изображения можно выполнить следующие действия:
  
1. Откройте список XML-файлов.
    
2. Замените вхождения *% Version%* соответствующей версией сборки Office. Версию сборки можно получить из релеасехистори. XML, как описано далее в этой статье. 
    
3. Прочитайте атрибут URL для целевой ветви.
    
4. Удалить Языковые узлы для всех языков, не обязательных в настраиваемом образе.
    
   > [!NOTE]
   > Узлы с языком = "0" нейтральны к языку и должны быть включены в образ. 
  
5. Создайте локальное изображение сети CDN, пересматривая список XML-файлов и скопировав файлы CDN, создавая структуру папок по мере необходимости. 
    
   - Если указан ** атрибут Rename, переименуйте ** скопированный файл в значение, указанное в атрибуте Rename. Используется для создания файлов верхнего уровня по умолчанию v64. cab и v32. cab. Это переименованные версии CAB-файла верхнего уровня, которые используются в качестве версии установки по умолчанию, если версия не указана. 
    
   - Для создания расположения CDN используйте URL-адрес + Релативепас + имя файла.
    
Ниже приведены примеры, в которых используется месячный канал (в соответствии с `<baseURL>` определением узла) и версия сборки 16.0.4229.1004 из релеасехистори. XML. 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- Ниже приведен независимый от языка файл, необходимый для всех языков. Имя файла v64_ 16.0.4229.1004. cab и его следует скопировать из `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` и переименовать в. `…/office/data/v64.cab` 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- Ниже приведен файл, который должен быть включен в изображение en-US в соответствии с языком LCID = 1033. Имя файла s641033. cab и его следует скопировать из `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` него и не переименовывать.
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a>Проверка хэша файлов DAT

Средства создания изображений могут проверить целостность скачанных файлов DAT, сравнив вычисленное значение ХЭША с заданным ХЭШЕМ со значением, сопоставленным с каждым из DAT-файлов. Ниже приведен пример файла DAT из ежемесячного канала с версией сборки 16.0.4229.1004 и языковым набором для болгарского языка:
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- Атрибут **хашлокатион** указывает расположение относительного пути Stream.x64.bg-bg. hash для файла Stream.x64.bg-БГ. dat. Создайте расположение хэш-файла с помощью сцепления URL + Релативепас + Хашлокатион. В следующем примере расположение stream.x64.bg-bg. hash будет следующим: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- Атрибут **хашалго** указывает, какой алгоритм хеширования использовался. В этом случае использовался SHA256. 
    
  Чтобы проверить целостность файла stream.x64.bg-БГ. dat, откройте stream.x64.bg-bg. hash и прочтите хэш-значение, которое является первой строкой текста в хэш-файле. Сравните это с вычисленным значением хэша (с использованием указанного алгоритма хеширования), чтобы проверить целостность загруженного файла. dat.
    
  В следующем примере показан код C# для считывания хеша.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a>Обновления для клиентов Office 365

Все обновления для клиентов Office 365 опубликованы в [каталоге обновлений Майкрософт](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Обновления клиента Office 365 позволяют программному обеспечению программного обеспечения для программного обеспечения программного обеспечения обновления клиента Office 365 аналогично любому другому обновлению WU с одним исключением; обновления клиента не содержат реальных полезных данных. Обновления клиента Office 365 не должны устанавливаться на всех клиентах, а использовать для запуска рабочих процессов с программным обеспечением с программным обеспечением, заменив команду установки на основе механизма установки на основе COM, показанного выше. 
  
**На следующем рисунке показана схема рабочего процесса обновления клиента Office 365.**

![Схема рабочего процесса для обновлений клиента O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Схема рабочего процесса для обновлений клиента O365PP")
  
Каждое публикуемое обновление клиента Office 365 содержит метаданные об обновлении. Эти метаданные содержат параметр с именем *мореинфаурл* , который можно использовать для получения следующих сведений: 
  
-  *Ver*: идентифицирует версию Office, связанную с этим обновлением. 
    
-  *Branch*: идентифицирует канал обновления для этого обновления. К значениям относятся Инсидерфаст, предварительные оценки, ежемесячные, целевые, общие. В будущем можно добавить дополнительные значения. 
    
-  *Arch*: идентифицирует архитектуру процессора, связанную с этим обновлением. 
    
-  *ксмлвер*: версия списка XML-файлов, которая должна использоваться для создания основного образа для этого обновления. 
    
-  *ксмлпас*: путь к ОФЛ. CAB-файл, который содержит списки XML-файлов. 
    
-  *млфиле*: имя списка файлов, который должен использоваться для этого обновления. Значение будет равно O365Client_32bit или O365Client_64bit и будет совпадать с Arch. 
    
Следующий URL-адрес — это пример параметра *мореинфаурл* , который ссылается на выпуск обновления клиента Office 365 для 32-разрядной версии Office с версией сборки 16.0.2342.2343 на текущем канале. 
  
https://officecdn.microsoft.com/pr/wsus/ofl.cab— Это расположение списков XML-файлов для этого обновления, в частности, в файле O365Client_32bit. XML в ОФЛ. Архива.
  
[Ветви обновлений для клиента Office 365](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a>Дополнительные метаданные для автоматизации промежуточного хранения контента

Кроме метаданных, которые публикуются, что определяет, есть ли дополнительные XML-файлы, опубликованные в сети CDN, которые могут помочь предоставить дополнительные сведения о клиентах Office 365, доступных из сети CDN Office.
  
**Инвентаризационные. ЯЗЫК**
  
Этот XML-файл находится в подписанном CAB-файле и опубликован в сети CDN Office по следующему URL [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab)-адресу:.
  
Метаданные, опубликованные в этом XML-файле, удобно использовать для определения того, какие продукты доступны для развертывания и обслуживания из сети CDN Office, а также различные варианты для каждого из них. 
  
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

Корневой узел **релеасеинфо\> содержит атрибут публишеддате, который определяет дату публикации этого файла. \<** 
  
**Узел SKU\> определяет индивидуальные единицы \<** хранения. 
  
- Атрибут *ProductID* определяет идентификатор, который передается в качестве атрибута ID в файле Configuration. XML при использовании ODT. Например, `<Product ID="O365ProPlusRetail">`. 
    
- Атрибут *по умолчанию* , если он имеет значение true, определяет рекомендованную конфигурацию. 
    
**Узлы приложений\> используются для определения отдельных приложений Office, поддерживаемых каждым \<** SKU. 
  
- Атрибут *Name* — это имя отображаемого приложения. 
    
- Атрибут *AppID* — это атрибут ID, передаваемый в файле Configuration. XML для ** \<узла\> ExcludeApp** при использовании ODT. Например, `<ExcludeApp ID="Publisher" />`. 
    
**РЕЛЕАСЕХИСТОРИ. ЯЗЫК**
  
Этот XML-файл находится в подписанном CAB-файле и опубликован в сети CDN Office в следующем расположении: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab). 
  
Метаданные, опубликованные в этом XML-файле, помогают определить, какие каналы поддерживаются для обслуживания обновлений из сети CDN Office, а также сведения о журнале сборки для каждого поддерживаемого канала.
  
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

Корневой узел ** \<релеасехистори\> ** содержит атрибут публишеддате, который определяет дату публикации этого файла. 
  
Узел ** \<UpdateChannel\> ** определяет поддерживаемый канал. 
  
- Атрибут *Name* определяет идентификатор канала, который используется для передачи в ODT из файла Configuration. XML в качестве атрибута Channel. 
    
  Пример: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">` 
    
  > [!NOTE] 
  > Этот атрибут устарел и используется только для обратной совместимости. Используйте атрибут ID вместо атрибута Name. 
    
- Атрибут *ID* определяет идентификатор канала, который используется для передачи в ODT из файла Configuration. XML в качестве атрибута Channel. 
    
  Пример: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">` 
    
- В качестве отображаемого имени используется атрибут **DisplayName** . 
    
Узел ** \<Update\> ** используется для определения каждого обновления, опубликованного для конкретного канала. 
  
- **Последний** атрибут, если он имеет значение true, определяет выпуск, который является последним выпуском для этого канала. 
    
- Атрибут **Version** определяет номер версии для этого конкретного обновления. 
    
- Атрибут **легациверсион** определяет полный номер версии для этого конкретного обновления. 
    
- Атрибут **Build** определяет номер сборки для этого конкретного обновления. 
    
- Атрибут **пубтиме** определяет дату и время публикации этого обновления в сети CDN Office. 
    

