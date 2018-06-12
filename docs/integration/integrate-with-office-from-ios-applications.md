---
title: Интеграция приложений для iOS с Office
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office для iOS предлагает расширяемое решение для интеграции с приложениями сторонних поставщиков. В этой статье описано, как интегрировать приложение для iOS и Office, перенаправляя пользователей из приложения в Office, а затем обратно.
ms.openlocfilehash: 2ba8e1a157953705b60ff0cac7d62bafade0c469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807613"
---
# <a name="integrate-with-office-from-ios-applications"></a>Интеграция приложений для iOS с Office

Office для iOS предлагает расширяемое решение для интеграции с приложениями сторонних поставщиков. В этой статье описано, как интегрировать приложение для iOS и Office, перенаправляя пользователей из приложения в Office, а затем обратно.
  
Можно сделать так, чтобы пользователи устройств iOS с установленным набором Office, открывали и редактировали файлы, хранящиеся в SharePoint или OneDrive, из любого приложения, а затем быстро возвращались в исходное приложение. Для этого настройте передачу файлов в Office через обработчики протоколов и такой вызов Office, который обеспечивает правильное реагирование Office.
  
Закончив редактирование файла, пользователи могут выбрать стрелку "Назад" в приложении Office, чтобы закрыть документ и вернуться в исходное приложение для хранения, если при запуске приложения Office ему передаются нужные данные.
  
## <a name="verify-that-office-has-been-installed"></a>Проверка того, установлен ли набор Office

Исходное приложение сначала должно проверить, установлено ли определенное приложение Office. На устройствах с iOS могут быть установлены следующие приложения Office для просмотра и редактирования документов:
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
Используйте метод [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html), чтобы определить, может ли ваше приложение открыть страницы ресурса. Этот метод принимает в качестве параметра URL-адрес ресурса и возвращает значение **No**, если приложение, способное обработать URL-адрес, недоступно. Если метод **canOpenURL** возвращает значение **No**, предложите пользователю установить Office.
  
### <a name="prompt-the-user-to-install-office"></a>Предложите пользователю установить Office

 Если определенное приложение Office не установлено, можно использовать объект [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html), чтобы отобразить в своем приложении ссылку на приложение Office в iTunes App Store. В приведенной ниже таблице указан идентификатор iTunes, который используется для вызова каждого приложения Office в Store Kit Product View Controller. 
  
|**Приложение Office**|**Идентификатор iTunes**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPad)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-ipad/id478105721?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-onenote-for-ipad/id478105721?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Вызов Office

Когда приложение Office установлено, ваше приложение, выполняющее перенаправление, может вызвать Office, передав следующие сведения: 
  
- протокол Office;
    
- режим открытия;
    
- URL-адрес;
    
- протокол с обратной связью;
    
- контекст документа.
    
Формат схемы:
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
Ниже приведен пример запроса для вызова файла Word для редактирования:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Протоколы Office

В приведенной ниже таблице перечислены протоколы для каждого приложения Office. 
  
|**Приложение**|**Протокол**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |onenote:  <br/> |
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
  
### <a name="passback-protocol-optional"></a>Протокол с обратной связью (необязательно)

Если вы хотите, чтобы при выборе стрелки "Назад" пользователи возвращались из Office в приложение для iOS, исходное приложение должно использовать протокол с обратной связью, в котором последовательно указаны дескриптор |p| и протокол приложения (без двоеточия). Убедитесь, что ваше приложение может правильно обрабатывать ответ от Office.
  
Формат схемы:
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>Контекст документа (необязательно)

Office не использует контекст документа, но исходному приложению он может понадобиться при обратном перенаправлении пользователя из Office. Если вы хотите, чтобы контекст документа возвращался в ваше приложение, последовательно укажите дескриптор |c| и нужный контекст в виде строки. В Office нет ограничений на длину строки, кроме установленных в операционной системе.
  
Формат схемы:
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>Возвращение пользователей в исходное приложение

Из соображений безопасности Office возвращает пользователей в исходное приложение, только если файл открыт успешно. Когда пользователь выбирает стрелку "Назад", Office отвечает исходному приложению с указанием протокола с обратной связью, режима открытия, URL-адреса, состояния ожидания отправки и контекста документа. Для состояния ожидания отправки используется дескриптор |z| и значение yes или no.
  
Формат схемы:
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Метод canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Класс UIApplication](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Объект SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

