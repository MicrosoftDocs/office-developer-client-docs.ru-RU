---
title: Сценарии внешней автоматизации и примеры
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Автоматизация infopath 2007, форм [InfoPath 2007] программным путем добавления данных, автоматизации [InfoPath 2007], внешних сценариев
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Члены предоставлено Microsoft Office InfoPath основной сборки взаимодействия (Microsoft.Office.Interop.InfoPath.dll) и сборке взаимодействия InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) поддержку написания управляемого кода для автоматизации InfoPath.
ms.openlocfilehash: 1c76e5cb659c9d3f39eec4a7e517ab57c98c858a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807384"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="8c4ad-104">Сценарии внешней автоматизации и примеры</span><span class="sxs-lookup"><span data-stu-id="8c4ad-104">External automation scenarios and examples</span></span>

<span data-ttu-id="8c4ad-105">Члены предоставлено Microsoft Office InfoPath основной сборки взаимодействия (Microsoft.Office.Interop.InfoPath.dll) и сборке взаимодействия InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) поддержку написания управляемого кода для автоматизации InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="8c4ad-106">Создание ссылок на сборки основной взаимодействия Microsoft Office InfoPath и InfoPath XML взаимодействия</span><span class="sxs-lookup"><span data-stu-id="8c4ad-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="8c4ad-107">Для создания управляемого кода для автоматизации InfoPath, необходимо установить ссылки на основной сборке взаимодействия Microsoft InfoPath и сборки взаимодействия InfoPath XML.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="8c4ad-108">Основной сборки взаимодействия Microsoft InfoPath поддерживает взаимодействие с помощью объектной модели COM, предоставляемые элементом IPEDITOR. DLL-Библиотеку с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c4ad-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="8c4ad-109">Сборки взаимодействия InfoPath XML поддерживает взаимодействие с помощью объектной модели COM, предоставляемые с Microsoft XML Core Services (MSXML) с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) .</span><span class="sxs-lookup"><span data-stu-id="8c4ad-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8c4ad-110">Для приложений с управляемым кодом, которые автоматизируют InfoPath пользователям InfoPath, основной сборки взаимодействия Microsoft Office InfoPath и сборке взаимодействия InfoPath XML, установленных на их компьютерах.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="8c4ad-111">**Поддержка программирования .NET** в программе установки InfoPath был установлен на **запускать с моего компьютера** для обычной установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="8c4ad-112">В результате установке до .NET Framework 1.1 распространяемого или .NET Framework 1.1 Software Development Kit (SDK) или более поздняя версия этих сборок взаимодействия будет также установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="8c4ad-113">Если эти сборки взаимодействия недоступны на компьютере пользователя, необходимо подтвердить, что установки .NET Framework 1.1 или более поздней версии и запустите **программы и компоненты** **Панели управления** для изменения программы установки и настройки **программирования .NET Поддержка** параметр InfoPath, чтобы **запускать с моего компьютера**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="8c4ad-114">Далее описывается, как задать ссылки на основной сборке взаимодействия Microsoft Office InfoPath и InfoPath XML сборки взаимодействия в проекте Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="8c4ad-115">Чтобы задать ссылку на основной сборки взаимодействия Microsoft.Office.Interop.InfoPath, задайте ссылку на **Библиотеку типа Microsoft InfoPath 3.0** на вкладку **COM** диалогового окна **Добавить ссылку** .</span><span class="sxs-lookup"><span data-stu-id="8c4ad-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="8c4ad-116">Несмотря на то, что нужно задать ссылку на вкладке **COM** , ссылку устанавливается в основной сборке взаимодействия Microsoft.Office.Interop.InfoPath.dll, которая устанавливается в глобальный кэш сборок (GAC), программа установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="8c4ad-117">Задайте ссылку на основной сборки взаимодействия Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="8c4ad-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="8c4ad-118">Откройте проект управляемого кода в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="8c4ad-119">В **Обозревателе решений**щелкните правой кнопкой мыши **ссылки**и выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="8c4ad-120">На вкладке **COM** дважды щелкните **Библиотека типов Microsoft InfoPath 3.0**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="8c4ad-121">Чтобы задать ссылку на сборку взаимодействия Microsoft.Office.Interop.InfoPath.Xml, перейдите к файлу Microsoft.Office.Interop.InfoPath.Xml.dll, установленной по умолчанию в < _диск_>: \Program Files\Microsoft Office\OFFICE14 папки .</span><span class="sxs-lookup"><span data-stu-id="8c4ad-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="8c4ad-122">Несмотря на то, что указан копии сборки в локальной файловой системе, эта процедура устанавливает ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml.dll, которая устанавливается в глобальный кэш сборок (GAC), программа установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="8c4ad-123">Задать ссылку на сборку взаимодействия Microsoft.Office.Interop.InfoPath.Xml</span><span class="sxs-lookup"><span data-stu-id="8c4ad-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="8c4ad-124">Откройте или создайте проект управляемого кода в Visual Studio, такие как **Консольное приложение** или **Приложение Windows**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="8c4ad-125">В **Обозревателе решений**щелкните правой кнопкой мыши **ссылки**и выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="8c4ad-126">На вкладке **.NET** , нажмите кнопку **Обзор**, перейдите к < _диск_>: \Program Files\Microsoft Office\OFFICE14 папки, а затем нажмите кнопку Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="8c4ad-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="8c4ad-128">Автоматизация при изменении значения поля</span><span class="sxs-lookup"><span data-stu-id="8c4ad-128">Automate changing the value of a field</span></span>

<span data-ttu-id="8c4ad-129">Предположим, что один из клиентов пользователя шаблон формы InfoPath отчет о продажах недавно изменен его имя компании «A» в «компания б».</span><span class="sxs-lookup"><span data-stu-id="8c4ad-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="8c4ad-130">Разработчик требуется написать код, который будет автоматически обновлять отчет о продажах формы, сохраненные в этот шаблон формы в соответствии с изменением имени.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="8c4ad-131">Следующие сценарии предполагается наличие формы, который содержит текстовое поле, к которому привязан к полю с именем customerName.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="8c4ad-132">Создайте образец шаблона форм и форм</span><span class="sxs-lookup"><span data-stu-id="8c4ad-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="8c4ad-133">Откройте InfoPath и создайте шаблон пустой формы.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="8c4ad-134">Добавьте в форму элемент управления **Текстовое поле** и имя поля, связанного с customerName элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="8c4ad-135">В области задач **поля** щелкните правой кнопкой мыши папку **myFields** и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="8c4ad-136">На вкладке **сведения** выберите и скопируйте следующее значение **пространство имен:**, а затем вставить скрипт в блокноте или другом местоположении, где его можно получить.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="8c4ad-137">Необходимо будет это значение более поздней версии для установки значения свойства **SelectionNamespaces** в коде.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="8c4ad-138">Публикация шаблона формы в папку с именем C:\Test и примите имя по умолчанию шаблон1.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="8c4ad-139">Откройте шаблон формы, добавьте имя «Компании A» в текстовом поле, связанный с полем customerName и затем сохранить форму как «Form1».</span><span class="sxs-lookup"><span data-stu-id="8c4ad-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="8c4ad-140">Создание консольного приложения управляемого кода для изменения имени компании «A» для «Компании B»</span><span class="sxs-lookup"><span data-stu-id="8c4ad-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="8c4ad-141">Откройте Visual Studio и создайте новый Visual C# или Visual Basic консольного приложения с именем UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="8c4ad-142">Установите ссылки на основной сборке взаимодействия Microsoft Office InfoPath и InfoPath XML сборок взаимодействия, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="8c4ad-143">Добавьте следующий код в файле Program.cs или Module1.vb, убедитесь, что обновление значение пространства имен в текущее значение свойства **SelectionNamespaces** со значением, скопированные во время создания пример формы.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace UpdateCustomer
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp = 
                new Microsoft.Office.Interop.InfoPath.Application();
            // Get a reference the XDocuments collection 
            // and open the sample form.
            XDocumentsCollection myXDocs = myApp.XDocuments;
            XDocument myXDoc = myXDocs.Open("C:\\Test\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Access the XML DOM for the underlying XML document using
            // the DOM property. Note that you must cast to the 
            // IXMLDOMDocument2 type from the
            // Microsoft.Office.Interop.InfoPath.Xml namespace
            // to access the XML DOM.
            IXMLDOMDocument2 myXMLDoc = myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace 
            // value below with that of your sample form.
            myXMLDoc.setProperty("SelectionNamespaces",
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Select all instances of customerName that contain 
            //'Company A'.
            IXMLDOMNodeList myNames = 
                myXMLDoc.selectNodes(
                "//my:customerName[. = 'Company A']");
            // Check to determine if any nodes were returned.
            if (myNames.length < 1)
            Console.WriteLine(
                "No elements containing 'Company A' were found.");
            // Loop through the list updating to 'Company B'.
            IXMLDOMNode myName = myNames.nextNode();
            while (myName != null)
            {
                myName.text = "Company B";
                myName = myNames.nextNode();
            }
            // Save the updated form as Form2.xml and close out.
            myXDoc.SaveAs("C:\\Test\\Form2.xml");
            myXDocs.Close(0);
            myApp.Quit(false);
            Console.WriteLine("Finished!");
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application()
          ' Get a reference the XDocuments collection 
          ' and open the sample form.
          Dim myXDocs As XDocumentsCollection = myApp.XDocuments
          Dim myXDoc As XDocument = myXDocs.Open( _
            "C:\\Test\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Access the XML DOM for the underlying XML document using
          ' the DOM property. Note that you must cast to the 
          ' IXMLDOMDocument2 type from the
          ' Microsoft.Office.Interop.InfoPath.Xml namespace
          ' to access the XML DOM.
          Dim myXMLDoc As IXMLDOMDocument2 = _
            DirectCast(myXDoc.DOM, IXMLDOMDocument2)
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace 
          ' value below with that of your sample form.
          myXMLDoc.setProperty("SelectionNamespaces", _
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Select all instances of customerName that contain 
          ''Company A'.
          Dim myNames As IXMLDOMNodeList = _
      myXMLDoc.selectNodes("//my:customerName[. = 'Company A']")
          ' Check to determine if any nodes were returned.
          If (myNames.length < 1) Then
            Console.WriteLine( _
                "No elements containing 'Company A' were found.")
          Else
            ' Loop through the list updating to 'Company B'.
            Dim myName As IXMLDOMNode = myNames.nextNode()
            While (myName IsNot Nothing)
                myName.text = "Company B"
                myName = myNames.nextNode()
            End While
          End If
          ' Save the updated form as Form2.xml and close out.
          myXDoc.SaveAs("C:\\Test\\Form2.xml")
          myXDocs.Close(0)
          myApp.Quit(False)
          Console.WriteLine("Finished!")
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="8c4ad-144">Нажмите кнопку **Начать отладку** в меню **Отладка** , чтобы скомпилировать и запустить консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="8c4ad-145">Приложение открывает форму, сохраняемый в виде Form1.xml и перебирает все элементы customerName, которые содержат значение компании A и изменяет это значение на компании B. После завершения операции новую копию формы сохраняется в виде Form2.xml в папке C:\Test.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="8c4ad-146">Автоматизировать открытия формы и заполнение значений полей</span><span class="sxs-lookup"><span data-stu-id="8c4ad-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="8c4ad-147">Следующий пример автоматизирует Открытие пустая форма и заполнение имя, Фамилия и поля адреса в форме.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="8c4ad-148">Этот сценарий предполагает форме, которая содержит три текстовых полей, которые связаны с полями с именами FirstName, LastName и адрес.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="8c4ad-149">Создайте образец шаблона форм и форм</span><span class="sxs-lookup"><span data-stu-id="8c4ad-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="8c4ad-150">Откройте InfoPath и создайте пустой формы.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="8c4ad-151">Добавьте три элемента управления текстовых полей в форму и назовите полей, привязанных к элементам управления: FirstName, LastName и адрес.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="8c4ad-152">Добавьте нужные поля.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="8c4ad-153">В области задач **поля** щелкните правой кнопкой мыши папку **myFields** и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="8c4ad-154">На вкладке **сведения** выберите и скопируйте следующее значение **пространство имен:**, а затем вставить скрипт в блокноте или другом местоположении, где его можно получить.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="8c4ad-155">Необходимо будет это значение более поздней версии для установки значения свойства **SelectionNamespaces** в коде.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="8c4ad-156">Публикация шаблона формы в папку с именем C:\Temp и примите имя по умолчанию шаблон1.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="8c4ad-157">Откройте шаблон формы и сохранить как «Form1», чтобы C:\Temp пустая форма.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="8c4ad-158">Создание консольного приложения управляемого кода для открытия формы и заполнения полей</span><span class="sxs-lookup"><span data-stu-id="8c4ad-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="8c4ad-159">Откройте Visual Studio и создайте новый Visual C# или Visual Basic консольного приложения с именем ОткрытьФорму.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="8c4ad-160">Установите ссылки на основной сборке взаимодействия Microsoft Office InfoPath и InfoPath XML сборок взаимодействия, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="8c4ad-161">Добавьте следующий код в файле Program.cs или Module1.vb, убедитесь, что обновление значение пространства имен в текущее значение свойства **SelectionNamespaces** со значением, скопированные во время создания пример формы.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace OpenForm
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp=
                new Microsoft.Office.Interop.InfoPath.Application();
            // Create an InfoPath XDocument variable and open 
            // the blank form.
            XDocument myXDoc = myApp.XDocuments.Open(
                "c:\\temp\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Create an IXMLDOMDocument2 variable and access 
            // the XML DOM from the underlying XML document
            // using the DOM property of the XDocument object. 
            // Note that you must cast to IXMLDOMDocument2 to do so.
            IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace
            // value below with that of your sample form.
            doc.setProperty("SelectionNamespaces","xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Pre-populate the fields with specified values.
            doc.selectSingleNode("//my:FirstName").text="My Name";
            doc.selectSingleNode("//my:LastName").text="My LastName";
            doc.selectSingleNode("//my:Address").text="My Address";
            // Save the form, leaving InfoPath open.
            myXDoc.Save();
            
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application
          ' Create an InfoPath XDocument variable and open 
          ' the blank form.
          Dim myXDoc As XDocument = myApp.XDocuments.Open( _
            "c:\\temp\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Create an IXMLDOMDocument2 variable and access 
          ' the XML DOM from the underlying XML document
          ' using the DOM property of the XDocument object.
          Dim doc As IXMLDOMDocument2 = myXDoc.DOM
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace
          ' value below with that of your sample form.
          doc.setProperty("SelectionNamespaces", "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="8c4ad-162">В меню **Отладка** выберите **Начать отладку** , чтобы скомпилировать и запустить консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="8c4ad-163">Приложение будет Открытие формы, сохраняемый в виде Form1.xml и заполните поля FirstName, LastName и адрес с помощью значения, заданные в примере кода и сохраните форму, не закрывая InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8c4ad-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8c4ad-164">См. также</span><span class="sxs-lookup"><span data-stu-id="8c4ad-164">See also</span></span>

- [<span data-ttu-id="8c4ad-165">О сборке взаимодействия Microsoft Office InfoPath основной</span><span class="sxs-lookup"><span data-stu-id="8c4ad-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="8c4ad-166">О сборке взаимодействия InfoPath XML</span><span class="sxs-lookup"><span data-stu-id="8c4ad-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

