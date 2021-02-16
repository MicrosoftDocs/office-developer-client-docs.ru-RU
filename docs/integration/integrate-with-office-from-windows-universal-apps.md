---
title: Интеграция универсальных приложений Windows с Office
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Вы можете интегрировать сторонние приложения на универсальной платформе приложений Windows с Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile. Универсальные приложения интегрируются с приложениями Office с помощью контрактов выбора файлов Windows, свойств Expando и контрактов обновления кэшированных файлов.
ms.openlocfilehash: ad04ccc3ceb6e0f1d53e4aebc12cf9724ab8ab66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299772"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Интеграция универсальных приложений Windows с Office

Вы можете интегрировать сторонние приложения на универсальной платформе приложений Windows с Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile. Универсальные приложения интегрируются с приложениями Office с помощью [контрактов выбора файлов Windows](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx), [свойств Expando](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx) и [контрактов обновления кэшированных файлов](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Когда вы интегрируете универсальное приложение с Excel, PowerPoint или Word Mobile, пользователи могут открывать предоставленные вашим приложением документы Office либо непосредственно в Office, либо используя Windows в вашем приложении. Кроме того, пользователи могут сохранять файлы в вашем универсальном приложении, которое отправляет их обратно в вашу службу.
  
Открытые таким образом файлы оказываются в списке последних использованных документов в Office, поэтому пользователи могут легко найти и открыть их.
  
Для интеграции ваше универсальное приложение должно:
    
- использовать [контракты выбора файлов](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx) в Windows;
    
- иметь возможность хранения файлов (например, приложение с доступом к облачному хранилищу).
    
## <a name="expando-properties"></a>Свойства Expando

Универсальные приложения Windows могут использовать свойства Expando для передачи дополнительной информации, связанной с файлами. Сведения об использовании этих свойств в Windows см. в разделе "System.ExpandoProperties" статьи [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx).
  
В таблице ниже описаны свойства, которые ваше приложение должно предоставить приложениям Office для применения сценариев открытия файлов. Если эти данные не предоставляются, все файлы в вашем приложении открываются как доступные только для чтения. То, смогут ли пользователи редактировать файлы, зависит от типа их лицензии Office, а также от типа документа, который они пытаются открыть.
  
Задайте эти свойства в наборе свойств **System.ExpandoProperties**. 
  
|**Свойство**|**Описание**|**Тип**|**Пример**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |Имя поставщика, которое видно пользователю. Отображается в различных местах в Office, например в списке последних использованных документов.  <br/> |String  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |Для лицензирования укажите тип владения/расположение документа: личный (принадлежит отдельному пользователю) или рабочий (принадлежит компании). Допустимые значения: 1 (личный) и 2 (рабочий). Например, если файл пользователя находится в хранилище компании Contoso, используйте значение "2" (рабочий).  <br/> |Unit32  <br/> | 1 или 2  <br/> Например, если файл пользователя находится в хранилище компании Contoso, для него устанавливается значение 2 (рабочий).  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |Юридическая часть, в которой вы заявляете, что предоставляемая вами информация соответствует нашим условиям использования. Эта часть не видна пользователю. Это соглашение между вами, поставщиком приложения и корпорацией Майкрософт.  <br/> Ниже приведен пример.  <br/> | String  <br/> | Я соглашаюсь с условиями, размещенными на странице [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) <br/> |
   
В приведенном ниже примере кода показано, как задать эти свойства.
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a>Контракты обновления кэшированных файлов

Если ваше приложение участвует в контрактах обновления кэшированных файлов, оно оповещается об изменениях, вносимых в файл другим универсальным приложением (например, Office). О том, как это работает в Windows, см. статью [Класс CachedFileUpdater](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Office использует параметр **AllowOnlyReaders** для открытия файлов для чтения и записи, предоставляемых вашим универсальным приложением с помощью контрактов выбора файлов. Это означает, что при открытии файла в Office он не может быть перемещен, удален, переименован или изменен другим приложением, включая ваше собственное. Office выполняет автоматическое сохранение файла, но задает свойство CachedFileManager.DeferUpdates, чтобы предотвратить активацию вашего приложения до закрытия документа приложением Office или до приостановки Office операционной системой Windows (при переключении пользователя на другое приложение). Ваше приложение может вносить записи в файл только после его закрытия приложением Office. 
  
Ваше приложение должно управлять всеми операциями передачи данных в службе, включая скачивание, обновление или отправку файлов.
  
В таблицах ниже перечислены параметры, задаваемые для управления взаимодействием между вашим приложением и Office.
  
|**Параметр**|**Описание**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |Задайте параметр **BeforeAccess**, чтобы позволить приложению обновлять файл перед его отправкой в Office.  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |Задайте параметр **ReadOnly**, чтобы файл был доступен только для чтения. Задайте параметр **AfterWrite**, чтобы класс CacheFileUpdater всегда запускал ваше приложение после того, как приложение Office завершит работу с файлом.  <br/><br/>**ПРИМЕЧАНИЕ**. Если вы не зададите параметр **AfterWrite**, ваше приложение не будет передавать сведения об изменениях. Это значит, что изменения, вносимые пользователем, будут иметь только локальный характер.           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |Задайте это свойство, чтобы ваше приложение всегда обновляло файл после получения к нему доступа пользователем в списке последних использованных файлов.  <br/> |
   
## <a name="invoking-office-from-your-app"></a>Вызов Office из вашего приложения

When a user opens an Office document from your app, the document can open in Excel Mobile, PowerPoint Mobile, and Word Mobile. For example, when a user selects a \*.docx file in your app, Word Mobile launches with the \*.docx file opened. The Office app that opens is based on which app the user associated with the file type.
  
Для открытия файлов из вашего приложения в Office рекомендуется использовать метод **LaunchFileAsync()**. Мы не рекомендуем использовать метод **LaunchUriAsync()** для запуска файла, так как вместо приложения Office он будет запускать приложение, зарегистрированное для схемы URI (браузер). Хотя метод **LaunchUriAsync()** с параметром **LauncherOptions.ContentType()** может вызвать приложение Office, в этом случае открываемый файл помечается в Office как временный и доступный только для чтения. 
  
Дополнительные сведения см. в статье [Класс Launcher](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx).
  
## <a name="temporary-and-read-only-files"></a>Временные файлы и файлы доступные только для чтения

В своем приложении задайте атрибут **FILE_ATTRIBUTE_TEMPORARY** для временных файлов и атрибут **FILE_ATTRIBUTE_READONLY** для файлов, доступных только для чтения. 
  
Файлы с заданным атрибутом **FILE_ATTRIBUTE_TEMPORARY** или **FILE_ATTRIBUTE_READONLY** открываются в Office как доступные только для чтения. Кроме того, при заданном атрибуте **FILE_ATTRIBUTE_TEMPORARY** файл не отображается в списке последних использованных документов. 
  
Дополнительные сведения об атрибутах см. в статье [Функция SetFileAttributes](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx).
  
## <a name="other-best-practices"></a>Наши рекомендации

Чтобы добиться оптимальной целостности файлов, например при конфликтующих изменениях или ошибках, используйте указанные ниже рекомендации.
  
- Предотвращение конфликтов сохранения
    
  - Приостановите отправку данных при возникновении конфликтов с сервером, чтобы избежать разветвления (оно допускается, только если в приложении Office больше нет открытых файлов, доступных для записи). Обычно если файл из вашего приложения открывается в Office, ваше приложение активируется только после закрытия Office или после его приостановки операционной системой Windows.
    
  - Если для устранения конфликтов вам нужен пользовательский интерфейс, используйте всплывающие уведомления. Полный пользовательский интерфейс не будет доступен, когда набор Office заблокирован.
    
- Устранение ошибок
    
  - При снятии блокировки следует уведомить пользователей о возникшем конфликте и сообщить им о способах решения проблемы в своем приложении.
    
## <a name="see-also"></a>См. также

- [Интеграция с Office](integrate-with-office.md)   
- [Интеграция клиентов синхронизации Win32 с приложениями Office](integrate-with-office-from-win32-sync-clients.md)
    

