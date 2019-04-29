---
title: Основные сведения о полностью доверенных формах
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath предоставляет возможность создавать полностью доверенные формы, которые имеют более высокие разрешения безопасности и могут получать доступ к системным ресурсам и другим компонентам на компьютере пользователя. В этой статье описывается, что такое полностью доверенная форма и зачем она используется, а также создание полностью доверенной формы с помощью ручного преобразования и регистрации стандартной формы или цифровой подписи стандартной формы.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430394"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="4afba-104">Основные сведения о полностью доверенных формах</span><span class="sxs-lookup"><span data-stu-id="4afba-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="4afba-105">InfoPath предоставляет возможность создавать полностью доверенные формы, которые имеют более высокие разрешения безопасности и могут получать доступ к системным ресурсам и другим компонентам на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="4afba-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="4afba-106">В этой статье описывается, что такое полностью доверенная форма и зачем она используется, а также создание полностью доверенной формы с помощью ручного преобразования и регистрации стандартной формы или цифровой подписи стандартной формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="4afba-p103">Шаблоны форм InfoPath можно развертывать с различными уровнями безопасности. Используемый уровень выбирается с учетом уровня доступа ко внешним ресурсам, который должен быть у формы. По умолчанию шаблоны формы InfoPath не могут обращаться к системным ресурсам и использовать программные компоненты, не отмеченные как безопасные для скриптов. Однако можно сделать так, что форма может получить доступ к системным и другим внешним ресурсам, включая программные компоненты, не отмеченные как безопасные для скриптов.</span><span class="sxs-lookup"><span data-stu-id="4afba-p103">InfoPath form templates can be deployed with varying levels of security. The level you use is dictated by the level of access to external resources that you want a form to have. By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting. However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="4afba-p104">Для использования формы приложение InfoPath должно иметь доступ к шаблону формы, на котором основана форма. При создании шаблона формы InfoPath создает запись в файле определений формы (XSF), который содержит URL-адрес шаблона формы. Форма на основе URL-адреса называется *песочницей*. Когда пользователь ее заполняет, форма добавляется в локальный кэш, при этом она не имеет доступа к системным ресурсам. Такой тип форм наследует разрешения домена, в котором она открывается.</span><span class="sxs-lookup"><span data-stu-id="4afba-p104">For a form to be used, InfoPath must be able to access the form template that the form is based on. When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template. A URL-based form is said to be *sandboxed*. When a user fills it out, the form is added in a local cache and denied access to system resources. This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="4afba-p105">Однако форму можно изменить таким образом, чтобы она была основана на универсальном имени ресурса (URN), что дает доступ к системным ресурсам. Такие формы называются *полностью доверенными*.</span><span class="sxs-lookup"><span data-stu-id="4afba-p105">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources. Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="4afba-118">Причины использования полностью доверенных форм</span><span class="sxs-lookup"><span data-stu-id="4afba-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="4afba-p106">Полностью доверенные формы обладают улучшенным набором разрешений, чем формы-"песочницы". Например, они могут содержать программный код, использующий внешние объекты для доступа к системным ресурсам, они могут использовать системные компоненты и элементы управления Microsoft ActiveX, не отмеченные как безопасные для скриптов, а также они могут применять пользовательскую бизнес-логику из сборок .NET.</span><span class="sxs-lookup"><span data-stu-id="4afba-p106">Fully trusted forms have a better set of permissions than sandboxed forms. For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="4afba-p107">Кроме того, некоторые элементы объектной модели InfoPath имеют уровень безопасности 3, то есть их можно использовать только в полностью доверенных формах. Например, для доступа к объекту Microsoft Office **CommandBars** используется свойство [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) класса InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , чтобы задать ссылку на него. Так как это свойство имеет уровень безопасности 3, его нельзя использовать не в полностью доверенной форме.</span><span class="sxs-lookup"><span data-stu-id="4afba-p107">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form. For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it. Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4afba-124">[!Примечание] Использование свойства [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) класса [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) или другого элемента объектной модели с уровнем безопасности 3 не в полностью доверенной форме приведет к ошибке "в разрешении отказано".</span><span class="sxs-lookup"><span data-stu-id="4afba-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="4afba-125">Что делает форму полностью доверенной?</span><span class="sxs-lookup"><span data-stu-id="4afba-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="4afba-126">Для создания и использования полностью доверенной формы необходимо выполнить следующие действия с применением интерфейса пользователя InfoPath и обработкой файлов формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="4afba-p108">Нужно включить параметр InfoPath, разрешающий использование полностью доверенных форм категории **Доверенные издатели** диалогового окна **Центр управления безопасностью**. Этот параметр должен быть включен, чтобы пользователи могли открывать полностью доверенные формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-p108">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box. This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="4afba-129">Зарегистрировать полностью доверенную форму на целевом компьютере с помощью метода **RegisterSolution** объекта **Application** InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4afba-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="4afba-130">Создание полностью доверенной формы</span><span class="sxs-lookup"><span data-stu-id="4afba-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="4afba-131">Форму можно создать вручную, для чего необходимо напрямую изменить некоторые файлы формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="4afba-132">Также можно использовать цифровую подпись шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="4afba-133">Ручное создание полностью доверенной формы</span><span class="sxs-lookup"><span data-stu-id="4afba-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="4afba-134">Чтобы создать полностью доверенную форму вручную, выполните следующие действия</span><span class="sxs-lookup"><span data-stu-id="4afba-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="4afba-135">Создайте архивную копию шаблона формы, которую необходимо сделать полностью доверенной.</span><span class="sxs-lookup"><span data-stu-id="4afba-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="4afba-136">Откройте шаблон формы в InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4afba-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="4afba-137">Сохраните исходные файлы формы на жестком диске, щелкнув вкладку **Файл**, выбрав **Опубликовать**, а затем — **Экспортировать исходные файлы**.</span><span class="sxs-lookup"><span data-stu-id="4afba-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="4afba-138">Укажите папку, в которой нужно сохранить исходные файлы формы, нажмите кнопку **ОК** и выйдите из конструктора InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4afba-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="4afba-139">В папке, содержащей файлы формы, откройте файл определений формы (XSF), который по умолчанию называется  `manifest.xsf`, в текстовом редакторе наподобие Блокнота.</span><span class="sxs-lookup"><span data-stu-id="4afba-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="4afba-140">Добавьте следующие атрибуты в элемент **xDocumentClass** XSF-файла:</span><span class="sxs-lookup"><span data-stu-id="4afba-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > [!Примечание] Значения, используемые для идентификатора URN могут быть любой строкой, если эта строка уникальна. После `urn:` префикса должно быть по крайней мере два значения, и эти значения должны быть разделены двоеточием. <span data-ttu-id="4afba-143">Кроме того, длина идентификатора URN не должна превышать 255 символов.</span><span class="sxs-lookup"><span data-stu-id="4afba-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="4afba-144">Сохраните и закройте XSF-файл, затем откройте XML-файл шаблона, который по умолчанию имеет имя  `Template.xml`, в текстовом редакторе наподобие Блокнота.</span><span class="sxs-lookup"><span data-stu-id="4afba-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="4afba-145">Удалите атрибут **href** из инструкции обработки  `mso-infoPathSolution` и замените ее на тот же атрибут **name**, используемый в шаге 6 для XSF-файла.</span><span class="sxs-lookup"><span data-stu-id="4afba-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="4afba-146">[!Примечание] Значения URN, используемые для атрибута **name**, должны быть одинаковыми для XSF-файла и XML-файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="4afba-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="4afba-147">Сохраните и закройте XML-файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="4afba-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="4afba-148">Запакуйте эти файлы в XSN-файл формата CAB с помощью средства наподобие makecab.exe.</span><span class="sxs-lookup"><span data-stu-id="4afba-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="4afba-p110">[!Примечание] Хотя конструктор форм InfoPath поддерживает упаковку файлов формы в XSN-файл, при этом форма преобразуется в форму на основе идентификатора URL. Поэтому следует упаковать файлы вручную, чтобы предотвратить изменение файлов формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-p110">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form. For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="4afba-p111">Создайте пользовательскую программу установки с помощью метода **RegisterSolution** объекта **Application** InfoPath, чтобы установить полностью доверенную форму. Простой способ создания такой программы заключается в том, чтобы создать файл скрипта, использующий следующие строки кода (с применением синтаксиса Microsoft JScript или VBScript):</span><span class="sxs-lookup"><span data-stu-id="4afba-p111">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form. A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> <span data-ttu-id="4afba-p112">[!Примечание] Хотя в этом примере используется простой файл скрипта, можно применять более надежный механизм установки, такой как файлы установщика Microsoft Windows (MSI). Убедитесь, что метод **RegisterSolution** правильно устанавливает полностью доверенную форму на целевом компьютере. Для доступа к методу **RegisterSolution** объекта **Application** InfoPath из Visual Basic или Visual Studio задайте ссылку на библиотеку типов Microsoft InfoPath 3.0, содержащуюся в файле IPEDITOR.dll, который установлен в папке C:\Program Files\Microsoft Office\Office14.</span><span class="sxs-lookup"><span data-stu-id="4afba-p112">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files. Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer. To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="4afba-156">Если нужно удалить полностью доверенную форму, можно воспользоваться методом **UnregisterSolution** объекта **Application**, как показано в следующих примерах JScript и VBScript.</span><span class="sxs-lookup"><span data-stu-id="4afba-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="4afba-157">Цифровое подписывание шаблона формы для создания полностью доверенной формы</span><span class="sxs-lookup"><span data-stu-id="4afba-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="4afba-158">Цифровая подпись шаблона формы позволяет развернуть полностью доверенный шаблон формы по электронной почте или на веб-сервере, например на сервере с Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="4afba-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="4afba-159">Выполните действия следующих трех процедур, чтобы сделать форму полностью доверенной, указав полное доверие для формы, используя цифровую подпись и опубликовав форму.</span><span class="sxs-lookup"><span data-stu-id="4afba-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="4afba-160">Цифровое подписывание формы</span><span class="sxs-lookup"><span data-stu-id="4afba-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="4afba-161">Откройте конструктор InfoPath, щелкните вкладку **File**, а затем выберите **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="4afba-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="4afba-162">В диалоговом окне **Параметры формы** выберите категорию **Безопасность и доверие**.</span><span class="sxs-lookup"><span data-stu-id="4afba-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="4afba-163">Снимите флажок **Автоматически определять уровень безопасности (рекомендуется)**.</span><span class="sxs-lookup"><span data-stu-id="4afba-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="4afba-164">Выберите **Полное доверие (у формы есть доступ к файлам и параметрам компьютера пользователя)**.</span><span class="sxs-lookup"><span data-stu-id="4afba-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="4afba-165">В разделе **Подписывание шаблона формы** выберите **Подписать этот шаблон формы**.</span><span class="sxs-lookup"><span data-stu-id="4afba-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="4afba-166">Щелкните **Выбор сертификата**, чтобы выбрать сертификат, загруженный и установленный ранее с поставщика доверенных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="4afba-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="4afba-167">Нажмите кнопку "ОК" два раза, чтобы завершить работу.</span><span class="sxs-lookup"><span data-stu-id="4afba-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="4afba-168">Публикация шаблона формы в библиотеке документов SharePoint</span><span class="sxs-lookup"><span data-stu-id="4afba-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="4afba-169">Щелкните вкладку **Файл**, выберите **Опубликовать**, а затем щелкните **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="4afba-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="4afba-170">Следуйте инструкциям **мастера публикации**, чтобы опубликовать шаблон формы в новой или существующей библиотеке документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4afba-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="4afba-171">Создание формы на основе полностью доверенного шаблона формы с цифровой подписью</span><span class="sxs-lookup"><span data-stu-id="4afba-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="4afba-172">В библиотеке документов SharePoint щелкните **Заполнить форму**.</span><span class="sxs-lookup"><span data-stu-id="4afba-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="4afba-p114">[!Примечание] После публикации шаблона формы в библиотеке документов SharePoint с помощью **мастера публикации** шаблон не отображается как элемент в библиотеке форм. При создании формы в этой библиотеке документов шаблон используется для новой формы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4afba-p114">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library. When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="4afba-p115">Если шаблон формы по умолчанию имеет цифровую подпись, InfoPath отображает предупреждение системы безопасности о шаблоне с цифровой подписью. Выберите **Всегда доверять файлам от этого поставщика и открывать их автоматически** и щелкните **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="4afba-p115">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template. Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="4afba-177">Использование полностью доверенной формы</span><span class="sxs-lookup"><span data-stu-id="4afba-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="4afba-p116">Использование полностью доверенной формы очень похоже на использование стандартной формы. Единственные значительные различия состоят в том, что полностью доверенная форма имеет доступ к ограниченным ресурсам, а предупреждения о безопасности не отображаются.</span><span class="sxs-lookup"><span data-stu-id="4afba-p116">Using a fully trusted form is very similar to using a standard form. The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4afba-p117">[!Примечание] Чтобы приложение InfoPath использовало полностью доверенную форму, пользователи должны убедиться, что флажок **Разрешить запуск полностью доверенных форм на моем компьютере** в категории **Доверенные издатели** диалогового окна **Центр управления безопасностью** установлен. Чтобы открыть диалоговое окно **Центр управления безопасностью**, выберите вкладку **Файл**, щелкните **Параметры** (под вкладкой **InfoPath**), щелкните **Центр управления безопасностью**, а затем выберите **Параметры центра управления безопасностью**.</span><span class="sxs-lookup"><span data-stu-id="4afba-p117">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box. To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="4afba-182">Полностью доверенную форму можно открыть в InfoPath в диалоговом окне **Заполнить форму**.</span><span class="sxs-lookup"><span data-stu-id="4afba-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="4afba-183">Диалоговое окно **Заполнить форму** открывается, если щелкнуть **Дополнительные формы** на панели задач окна **Заполнить форму** или выбрать **Заполнить форму** в меню **Файл**.</span><span class="sxs-lookup"><span data-stu-id="4afba-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="4afba-184">Изменение полностью доверенной формы</span><span class="sxs-lookup"><span data-stu-id="4afba-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="4afba-p118">Если нужно внести изменения только в XSN-файл, пользователи могут заменить существующие XSN-файлы на новый после внесения изменений. Им не придется повторно устанавливать его с помощью пользовательской программы установки.</span><span class="sxs-lookup"><span data-stu-id="4afba-p118">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made. They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="4afba-187">Однако при внесении изменений в файлы формы, которые содержит XSN-файл следует их упаковать, как это описано ранее, а пользователи должны повторно установить полностью доверенную форму.</span><span class="sxs-lookup"><span data-stu-id="4afba-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4afba-188">Лучше всего сохранить шаблон формы в формате XSN в конструкторе InfoPath, а затем следовать инструкциям, описанным в этой статье, чтобы создать полностью доверенную форму.</span><span class="sxs-lookup"><span data-stu-id="4afba-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="4afba-189">Заключение</span><span class="sxs-lookup"><span data-stu-id="4afba-189">Conclusion</span></span>

<span data-ttu-id="4afba-p119">В зависимости от деловых требований и потребностей пользователей возможно потребуется создать форму с более широким набором разрешений, чем у стандартной формы InfoPath. InfoPath позволяет изменить форму таким образом, чтобы она имела доступ к системным и другим внешним ресурсам, не отмеченным как безопасные для скриптов. Это можно сделать вручную, внеся изменения в файлы формы, которые содержит шаблон формы, и запустив скрипт установки или используя цифровую подпись шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="4afba-p119">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form. InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting. This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

