---
title: Интеграция приложений Android с Office
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office для Android предоставляет расширенное решение, позволяющее интегрировать приложения сторонних производителей. Вы можете выполнить интеграцию с Office из своего приложения Android, передав пользователей из своего приложения в Office.
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303152"
---
# <a name="integrate-with-office-from-android-applications"></a>Интеграция приложений Android с Office

Office для Android предоставляет расширенное решение, позволяющее интегрировать приложения сторонних производителей. Вы можете выполнить интеграцию с Office из своего приложения Android, передав пользователей из своего приложения в Office.
  
Вы можете позволять пользователям, запустившим Office на устройстве Android, открывать и редактировать файлы, сохраненные в SharePoint или OneDrive из любого приложения. Для этого вам необходимо передать файлы в Office через обработчики протоколов и убедиться, что Office вызывается понятными для Office образом.
  
После того как пользователь завершит редактирование файла, они могут нажать на устройстве кнопку "Назад", чтобы вернуться к исходному приложению хранения.
  
## <a name="verify-that-office-has-been-installed"></a>Проверка того, установлен ли Office

Исходное приложение сначала должно проверить, установлено ли определенное приложение Office. На устройствах с Android могут быть установлены следующие приложения Office для просмотра и редактирования документов: 
  
- Excel
    
- PowerPoint
    
- Word
    
Для того чтобы определить, установлены ли на устройстве определенные приложения Office, используйте Android PackageManager. В следующей таблице перечислены имена пакетов для приложений Office, которые вы можете использовать в этом процессе.
  
|**Приложение**|**Имя пакета**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.office.excel  <br/> |
|PowerPoint  <br/> |com.microsoft.office.powerpoint  <br/> |
|Word  <br/> |com.microsoft.office.word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Предложение пользователю для установки Office

Если определенное приложение Office не установлено, вы можете предложить пользователю установить это приложение. В следующей таблице перечислены доступные расположения для установки приложений Office.
  
|**Приложение**|**Магазин Google Play**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Вызов Office

Когда приложение Office установлено, ваше приложение, выполняющее перенаправление, может вызвать Office, передав следующие сведения:
  
- протокол Office;
    
- режим открытия;
    
- URL-адрес.
    
Формат схемы:
  
 `<Office protocol><open mode>|u|<URL>`
  
Ниже приведен пример запроса для вызова файла Word для редактирования:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Протоколы Office

В приведенной ниже таблице перечислены протоколы для каждого приложения Office.
  
|**Приложение**|**Протокол**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Режим открытия

Приложения Office могут открывать файлы непосредственно в режиме просмотра (ofv) или правки (ofe). По умолчанию используется режим правки.
  
Формат схемы:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL-адрес

URL-адрес состоит из трех частей:
  
- Объявление того, что файл будет открыт для редактирования (ofe)
    
- Дескриптор URL-адреса (|u|)
    
- URL-адрес
    
URL-адрес должен быть зашифрован и быть прямой ссылкой на файл (без перенаправления). Если Office не сможет обработать формат URL-адреса, а также если загрузка не удастся, Office не вернет пользователя в исходное приложение.
  
Формат схемы:
  
 `|u|<document URL>`
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Интеграция с Office](integrate-with-office.md)
    
- [PackageManager](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](https://developer.android.com/reference/android/content/Context.html)
    

