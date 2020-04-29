---
title: Интеграция приложений для iOS с Office
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office для iOS предлагает расширяемое решение для интеграции с приложениями сторонних поставщиков. В этой статье описано, как интегрировать приложение для iOS и Office, перенаправляя пользователей из приложения в Office, а затем обратно.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413852"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="0cb03-104">Интеграция приложений для iOS с Office</span><span class="sxs-lookup"><span data-stu-id="0cb03-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="0cb03-p102">Office для iOS предлагает расширяемое решение для интеграции с приложениями сторонних поставщиков. В этой статье описано, как интегрировать приложение для iOS и Office, перенаправляя пользователей из приложения в Office, а затем обратно.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p102">Office for iOS provides an extensible solution that enables integration with third-party applications. This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="0cb03-p103">Можно сделать так, чтобы пользователи устройств iOS с установленным набором Office, открывали и редактировали файлы, хранящиеся в SharePoint или OneDrive, из любого приложения, а затем быстро возвращались в исходное приложение. Для этого настройте передачу файлов в Office через обработчики протоколов и такой вызов Office, который обеспечивает правильное реагирование Office.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p103">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="0cb03-109">Закончив редактирование файла, пользователи могут выбрать стрелку "Назад" в приложении Office, чтобы закрыть документ и вернуться в исходное приложение для хранения, если при запуске приложения Office ему передаются нужные данные.</span><span class="sxs-lookup"><span data-stu-id="0cb03-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="0cb03-110">Проверка того, установлен ли набор Office</span><span class="sxs-lookup"><span data-stu-id="0cb03-110">Verify that Office has been installed</span></span>

<span data-ttu-id="0cb03-p104">Исходное приложение сначала должно проверить, установлено ли определенное приложение Office. На устройствах с iOS могут быть установлены следующие приложения Office для просмотра и редактирования документов:</span><span class="sxs-lookup"><span data-stu-id="0cb03-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="0cb03-113">Excel</span><span class="sxs-lookup"><span data-stu-id="0cb03-113">Excel</span></span>
    
- <span data-ttu-id="0cb03-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="0cb03-114">OneNote</span></span>
    
- <span data-ttu-id="0cb03-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="0cb03-115">PowerPoint</span></span>
    
- <span data-ttu-id="0cb03-116">Word</span><span class="sxs-lookup"><span data-stu-id="0cb03-116">Word</span></span>
    
<span data-ttu-id="0cb03-p105">Используйте метод [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html), чтобы определить, может ли ваше приложение открыть страницы ресурса. Этот метод принимает в качестве параметра URL-адрес ресурса и возвращает значение **No**, если приложение, способное обработать URL-адрес, недоступно. Если метод **canOpenURL** возвращает значение **No**, предложите пользователю установить Office.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p105">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource. This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available. If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="0cb03-120">Предложите пользователю установить Office</span><span class="sxs-lookup"><span data-stu-id="0cb03-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="0cb03-p106">Если определенное приложение Office не установлено, можно использовать объект [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html), чтобы отобразить в своем приложении ссылку на приложение Office в iTunes App Store. В приведенной ниже таблице указан идентификатор iTunes, который используется для вызова каждого приложения Office в Store Kit Product View Controller.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p106">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install. The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="0cb03-123">**Приложение Office**</span><span class="sxs-lookup"><span data-stu-id="0cb03-123">**Office application**</span></span>|<span data-ttu-id="0cb03-124">**Идентификатор iTunes**</span><span class="sxs-lookup"><span data-stu-id="0cb03-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cb03-125">Excel</span><span class="sxs-lookup"><span data-stu-id="0cb03-125">Excel</span></span>  <br/> |[<span data-ttu-id="0cb03-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="0cb03-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="0cb03-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="0cb03-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="0cb03-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="0cb03-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="0cb03-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="0cb03-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="0cb03-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="0cb03-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="0cb03-131">Word</span><span class="sxs-lookup"><span data-stu-id="0cb03-131">Word</span></span>  <br/> |[<span data-ttu-id="0cb03-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="0cb03-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="0cb03-133">Вызов Office</span><span class="sxs-lookup"><span data-stu-id="0cb03-133">Invoke Office</span></span>

<span data-ttu-id="0cb03-134">Когда приложение Office установлено, ваше приложение, выполняющее перенаправление, может вызвать Office, передав следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="0cb03-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="0cb03-135">протокол Office;</span><span class="sxs-lookup"><span data-stu-id="0cb03-135">Office protocol</span></span>
    
- <span data-ttu-id="0cb03-136">режим открытия;</span><span class="sxs-lookup"><span data-stu-id="0cb03-136">Open mode</span></span>
    
- <span data-ttu-id="0cb03-137">URL-адрес;</span><span class="sxs-lookup"><span data-stu-id="0cb03-137">URL</span></span>
    
- <span data-ttu-id="0cb03-138">протокол с обратной связью;</span><span class="sxs-lookup"><span data-stu-id="0cb03-138">Passback protocol</span></span>
    
- <span data-ttu-id="0cb03-139">контекст документа.</span><span class="sxs-lookup"><span data-stu-id="0cb03-139">Document context</span></span>
    
<span data-ttu-id="0cb03-140">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="0cb03-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="0cb03-141">Ниже приведен пример запроса для вызова файла Word для редактирования:</span><span class="sxs-lookup"><span data-stu-id="0cb03-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="0cb03-142">Протоколы Office</span><span class="sxs-lookup"><span data-stu-id="0cb03-142">Office protocols</span></span>

<span data-ttu-id="0cb03-143">В приведенной ниже таблице перечислены протоколы для каждого приложения Office.</span><span class="sxs-lookup"><span data-stu-id="0cb03-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="0cb03-144">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="0cb03-144">**Application**</span></span>|<span data-ttu-id="0cb03-145">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="0cb03-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cb03-146">Excel</span><span class="sxs-lookup"><span data-stu-id="0cb03-146">Excel</span></span>  <br/> |<span data-ttu-id="0cb03-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="0cb03-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="0cb03-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="0cb03-148">OneNote</span></span>  <br/> |<span data-ttu-id="0cb03-149">onenote:</span><span class="sxs-lookup"><span data-stu-id="0cb03-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="0cb03-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="0cb03-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="0cb03-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="0cb03-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="0cb03-152">Word</span><span class="sxs-lookup"><span data-stu-id="0cb03-152">Word</span></span>  <br/> |<span data-ttu-id="0cb03-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="0cb03-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="0cb03-154">Режим открытия</span><span class="sxs-lookup"><span data-stu-id="0cb03-154">Open mode</span></span>

<span data-ttu-id="0cb03-p107">Приложения Office могут открывать файлы непосредственно в режиме просмотра (ofv) или правки (ofe). По умолчанию используется режим правки.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span> 
  
<span data-ttu-id="0cb03-157">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="0cb03-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="0cb03-158">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="0cb03-158">URL</span></span>

<span data-ttu-id="0cb03-159">URL-адрес состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="0cb03-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="0cb03-160">Объявление того, что файл будет открыт для редактирования (ofe)</span><span class="sxs-lookup"><span data-stu-id="0cb03-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="0cb03-161">Дескриптор URL-адреса (|u|)</span><span class="sxs-lookup"><span data-stu-id="0cb03-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="0cb03-162">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="0cb03-162">The URL</span></span>
    
<span data-ttu-id="0cb03-p108">URL-адрес должен быть зашифрован и быть прямой ссылкой на файл (без перенаправления). Если Office не сможет обработать формат URL-адреса, а также если загрузка не удастся, Office не вернет пользователя в исходное приложение.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="0cb03-165">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="0cb03-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="0cb03-166">Протокол с обратной связью (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0cb03-166">Passback protocol (optional)</span></span>

<span data-ttu-id="0cb03-p109">Если вы хотите, чтобы при выборе стрелки "Назад" пользователи возвращались из Office в приложение для iOS, исходное приложение должно использовать протокол с обратной связью, в котором последовательно указаны дескриптор |p| и протокол приложения (без двоеточия). Убедитесь, что ваше приложение может правильно обрабатывать ответ от Office.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p109">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon). You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="0cb03-169">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="0cb03-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="0cb03-170">Контекст документа (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0cb03-170">Document context (optional)</span></span>

<span data-ttu-id="0cb03-p110">Office не использует контекст документа, но исходному приложению он может понадобиться при обратном перенаправлении пользователя из Office. Если вы хотите, чтобы контекст документа возвращался в ваше приложение, последовательно укажите дескриптор |c| и нужный контекст в виде строки. В Office нет ограничений на длину строки, кроме установленных в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p110">Office doesn't use the document context, but the referring application might need it when Office passes a user back. If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string. Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="0cb03-174">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="0cb03-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="0cb03-175">Возвращение пользователей в исходное приложение</span><span class="sxs-lookup"><span data-stu-id="0cb03-175">Return users to the referring application</span></span>

<span data-ttu-id="0cb03-p111">Из соображений безопасности Office возвращает пользователей в исходное приложение, только если файл открыт успешно. Когда пользователь выбирает стрелку "Назад", Office отвечает исходному приложению с указанием протокола с обратной связью, режима открытия, URL-адреса, состояния ожидания отправки и контекста документа. Для состояния ожидания отправки используется дескриптор |z| и значение yes или no.</span><span class="sxs-lookup"><span data-stu-id="0cb03-p111">For security reasons, Office only returns users to the referring application if the file opened successfully. When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context. The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="0cb03-179">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="0cb03-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="0cb03-180">См. также</span><span class="sxs-lookup"><span data-stu-id="0cb03-180">See also</span></span>
<span data-ttu-id="0cb03-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="0cb03-181"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="0cb03-182">Метод canOpenURL</span><span class="sxs-lookup"><span data-stu-id="0cb03-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="0cb03-183">Класс UIApplication</span><span class="sxs-lookup"><span data-stu-id="0cb03-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="0cb03-184">Объект SKProductViewController</span><span class="sxs-lookup"><span data-stu-id="0cb03-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

