---
title: Интеграция приложений Android с Office
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office для Android предоставляет расширенное решение, позволяющее интегрировать приложения сторонних производителей. Вы можете выполнить интеграцию с Office из своего приложения Android, передав пользователей из своего приложения в Office.
ms.openlocfilehash: 2fd60c7e86d3390bc5343f3e09fb2235f97e0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807607"
---
# <a name="integrate-with-office-from-android-applications"></a><span data-ttu-id="9d2fd-104">Интеграция приложений Android с Office</span><span class="sxs-lookup"><span data-stu-id="9d2fd-104">Integrate with Office from Android applications</span></span>

<span data-ttu-id="9d2fd-p102">Office для Android предоставляет расширенное решение, позволяющее интегрировать приложения сторонних производителей. Вы можете выполнить интеграцию с Office из своего приложения Android, передав пользователей из своего приложения в Office.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p102">Office for Android provides an extensible solution that enables integration with third-party applications. You can integrate with Office from your Android application by passing users from your application to Office.</span></span>
  
<span data-ttu-id="9d2fd-p103">Вы можете позволять пользователям, запустившим Office на устройстве Android, открывать и редактировать файлы, сохраненные в SharePoint или OneDrive из любого приложения. Для этого вам необходимо передать файлы в Office через обработчики протоколов и убедиться, что Office вызывается понятными для Office образом.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p103">You can enable users who are running Office on an Android device to open and edit files stored in SharePoint or OneDrive from any application. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="9d2fd-109">После того как пользователь завершит редактирование файла, они могут нажать на устройстве кнопку "Назад", чтобы вернуться к исходному приложению хранения.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-109">When a user is done editing a file, they can choose the back key on the device to return to the original storage application.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="9d2fd-110">Проверка того, установлен ли Office</span><span class="sxs-lookup"><span data-stu-id="9d2fd-110">Verify that Office has been installed</span></span>

<span data-ttu-id="9d2fd-p104">Исходное приложение сначала должно проверить, установлено ли определенное приложение Office. На устройствах с Android могут быть установлены следующие приложения Office для просмотра и редактирования документов:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on Android devices for document viewing and editing:</span></span> 
  
- <span data-ttu-id="9d2fd-113">Excel</span><span class="sxs-lookup"><span data-stu-id="9d2fd-113">Excel</span></span>
    
- <span data-ttu-id="9d2fd-114">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="9d2fd-114">PowerPoint</span></span>
    
- <span data-ttu-id="9d2fd-115">Word</span><span class="sxs-lookup"><span data-stu-id="9d2fd-115">Word</span></span>
    
<span data-ttu-id="9d2fd-p105">Для того чтобы определить, установлены ли на устройстве определенные приложения Office, используйте Android PackageManager. В следующей таблице перечислены имена пакетов для приложений Office, которые вы можете использовать в этом процессе.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p105">Use Android PackageManager to determine whether a particular Office application is installed on the device. The following table lists the package names for the Office applications that you can use in this process.</span></span>
  
|<span data-ttu-id="9d2fd-118">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-118">**Application**</span></span>|<span data-ttu-id="9d2fd-119">**Имя пакета**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-119">**Package name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d2fd-120">Excel</span><span class="sxs-lookup"><span data-stu-id="9d2fd-120">Excel</span></span>  <br/> |<span data-ttu-id="9d2fd-121">com.microsoft.office.excel</span><span class="sxs-lookup"><span data-stu-id="9d2fd-121">com.microsoft.office.excel</span></span>  <br/> |
|<span data-ttu-id="9d2fd-122">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="9d2fd-122">PowerPoint</span></span>  <br/> |<span data-ttu-id="9d2fd-123">com.microsoft.office.powerpoint</span><span class="sxs-lookup"><span data-stu-id="9d2fd-123">com.microsoft.office.powerpoint</span></span>  <br/> |
|<span data-ttu-id="9d2fd-124">Word</span><span class="sxs-lookup"><span data-stu-id="9d2fd-124">Word</span></span>  <br/> |<span data-ttu-id="9d2fd-125">com.microsoft.office.word</span><span class="sxs-lookup"><span data-stu-id="9d2fd-125">com.microsoft.office.word</span></span>  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="9d2fd-126">Предложение пользователю для установки Office</span><span class="sxs-lookup"><span data-stu-id="9d2fd-126">Prompt the user to install Office</span></span>

<span data-ttu-id="9d2fd-p106">Если определенное приложение Office не установлено, вы можете предложить пользователю установить это приложение. В следующей таблице перечислены доступные расположения для установки приложений Office.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p106">If a particular Office application is not installed, you can prompt the user to install the application. The following table lists the available install locations for Office applications.</span></span>
  
|<span data-ttu-id="9d2fd-129">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-129">**Application**</span></span>|<span data-ttu-id="9d2fd-130">**Магазин Google Play**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-130">**Google Play Store**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d2fd-131">Excel</span><span class="sxs-lookup"><span data-stu-id="9d2fd-131">Excel</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|<span data-ttu-id="9d2fd-132">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="9d2fd-132">PowerPoint</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|<span data-ttu-id="9d2fd-133">Word</span><span class="sxs-lookup"><span data-stu-id="9d2fd-133">Word</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="9d2fd-134">Вызов Office</span><span class="sxs-lookup"><span data-stu-id="9d2fd-134">Invoke Office</span></span>

<span data-ttu-id="9d2fd-135">Когда приложение Office установлено, ваше приложение, выполняющее перенаправление, может вызвать Office, передав следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-135">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span>
  
- <span data-ttu-id="9d2fd-136">протокол Office;</span><span class="sxs-lookup"><span data-stu-id="9d2fd-136">Office protocol</span></span>
    
- <span data-ttu-id="9d2fd-137">режим открытия;</span><span class="sxs-lookup"><span data-stu-id="9d2fd-137">Open mode</span></span>
    
- <span data-ttu-id="9d2fd-138">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="9d2fd-138">URL</span></span>
    
<span data-ttu-id="9d2fd-139">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-139">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>`
  
<span data-ttu-id="9d2fd-140">Ниже приведен пример запроса для вызова файла Word для редактирования:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-140">The following example shows a request to invoke a Word file for editing.</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a><span data-ttu-id="9d2fd-141">Протоколы Office</span><span class="sxs-lookup"><span data-stu-id="9d2fd-141">Office protocols</span></span>

<span data-ttu-id="9d2fd-142">В приведенной ниже таблице перечислены протоколы для каждого приложения Office.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-142">The following table lists the protocols for each Office application.</span></span>
  
|<span data-ttu-id="9d2fd-143">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-143">**Application**</span></span>|<span data-ttu-id="9d2fd-144">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-144">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d2fd-145">Excel</span><span class="sxs-lookup"><span data-stu-id="9d2fd-145">Excel</span></span>  <br/> |<span data-ttu-id="9d2fd-146">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-146">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="9d2fd-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="9d2fd-147">PowerPoint</span></span>  <br/> |<span data-ttu-id="9d2fd-148">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-148">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="9d2fd-149">Word</span><span class="sxs-lookup"><span data-stu-id="9d2fd-149">Word</span></span>  <br/> |<span data-ttu-id="9d2fd-150">ms-word:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-150">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="9d2fd-151">Режим открытия</span><span class="sxs-lookup"><span data-stu-id="9d2fd-151">Open mode</span></span>

<span data-ttu-id="9d2fd-p107">Приложения Office могут открывать файлы непосредственно в режиме просмотра (ofv) или правки (ofe). По умолчанию используется режим правки.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span>
  
<span data-ttu-id="9d2fd-154">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-154">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="9d2fd-155">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="9d2fd-155">URL</span></span>

<span data-ttu-id="9d2fd-156">URL-адрес состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-156">The URL includes three parts:</span></span>
  
- <span data-ttu-id="9d2fd-157">Объявление того, что файл будет открыт для редактирования (ofe)</span><span class="sxs-lookup"><span data-stu-id="9d2fd-157">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="9d2fd-158">Дескриптор URL-адреса (|u|)</span><span class="sxs-lookup"><span data-stu-id="9d2fd-158">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="9d2fd-159">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="9d2fd-159">The URL</span></span>
    
<span data-ttu-id="9d2fd-p108">URL-адрес должен быть зашифрован и быть прямой ссылкой на файл (без перенаправления). Если Office не сможет обработать формат URL-адреса, а также если загрузка не удастся, Office не вернет пользователя в исходное приложение.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span>
  
<span data-ttu-id="9d2fd-162">Формат схемы:</span><span class="sxs-lookup"><span data-stu-id="9d2fd-162">Schema format:</span></span>
  
 `|u|<document URL>`
  
## <a name="see-also"></a><span data-ttu-id="9d2fd-163">См. также</span><span class="sxs-lookup"><span data-stu-id="9d2fd-163">See also</span></span>
<span data-ttu-id="9d2fd-164"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="9d2fd-164"></span></span>

- [<span data-ttu-id="9d2fd-165">Интеграция с Office</span><span class="sxs-lookup"><span data-stu-id="9d2fd-165">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="9d2fd-166">PackageManager</span><span class="sxs-lookup"><span data-stu-id="9d2fd-166">PackageManager</span></span>](http://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [<span data-ttu-id="9d2fd-167">GetPackageManager()</span><span class="sxs-lookup"><span data-stu-id="9d2fd-167">GetPackageManager()</span></span>](http://developer.android.com/reference/android/content/Context.html)
    

