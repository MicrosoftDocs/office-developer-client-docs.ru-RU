---
title: Сценарии и примеры автоматизации с использованием внешних решений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- автоматизация infopath 2007,forms [InfoPath 2007], добавление данных программным путем,автоматизация [InfoPath 2007], внешние сценарии
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Члены, предоставляемые основной сборкой Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) и сборкой XML-кода (Microsoft.Office.Interop.InfoPath.Xml.dll) InfoPath, поддерживают написание управляемого кода для автоматизации InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537817"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="64730-104">Сценарии и примеры автоматизации с использованием внешних решений</span><span class="sxs-lookup"><span data-stu-id="64730-104">External automation scenarios and examples</span></span>

<span data-ttu-id="64730-105">Члены, предоставляемые основной сборкой Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) и сборкой XML-кода (Microsoft.Office.Interop.InfoPath.Xml.dll) InfoPath, поддерживают написание управляемого кода для автоматизации InfoPath.</span><span class="sxs-lookup"><span data-stu-id="64730-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="64730-106">Создание ссылок на сборки основного Microsoft Office InfoPath и XML-межпоиска InfoPath</span><span class="sxs-lookup"><span data-stu-id="64730-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="64730-107">Чтобы написать управляемый код для автоматизации InfoPath, необходимо установить ссылки на основное межкодовое и XML-сборки interop InfoPath.</span><span class="sxs-lookup"><span data-stu-id="64730-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="64730-108">Основная сборка microsoft InfoPath обеспечивает поддержку обеспечения связи с объектной моделью COM, которая предоставляется IPEDITOR.DLL с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx)</span><span class="sxs-lookup"><span data-stu-id="64730-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="64730-109">Сборка XML-связи InfoPath обеспечивает поддержку обеспечения связи с объектной моделью COM, которая предоставляется MSXML [](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) (MSXML) с помощью членовMicrosoft.Office.Interop.InfoPath.Xmlпространства имен.</span><span class="sxs-lookup"><span data-stu-id="64730-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="64730-110">На компьютерах пользователей приложений с управляемым кодом, которые автоматизуют InfoPath, должны быть установлены InfoPath, основная сборка межсервейного Microsoft Office InfoPath и сборка XML-кода.</span><span class="sxs-lookup"><span data-stu-id="64730-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="64730-111">Параметр **поддержки программируемости .NET** в программе установки  InfoPath настроен на запуск с моего компьютера для обычной установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="64730-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="64730-112">В результате, если установлен распространяемый пакет .NET Framework 1.1 или пакет SDK .NET Framework 1.1 или более поздней, эти сборки также будут установлены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64730-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="64730-113">Если эти сборки межпрограммного обеспечения недоступны на компьютере пользователя, необходимо подтвердить, что .NET Framework 1.1 или  более поздней установлена, а затем запустить программы и функции из панели управления, чтобы изменить настройку и настроить параметр поддержки программируемости **.NET** для InfoPath на запуск с моего **компьютера.** </span><span class="sxs-lookup"><span data-stu-id="64730-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="64730-114">В следующих процедурах описывается, как установить ссылки на основное Microsoft Office infoPath и сборки XML-межсервации InfoPath в Visual Studio проекта.</span><span class="sxs-lookup"><span data-stu-id="64730-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="64730-115">Чтобы установить ссылку на основную сборку interop.InfoPath, установите ссылку на библиотеку типов **Microsoft InfoPath 3.0** на вкладке **COM** диалогового окна "Добавление ссылки". </span><span class="sxs-lookup"><span data-stu-id="64730-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="64730-116">Несмотря на то, что вы настроили ссылку на вкладку **COM,** эта ссылка устанавливается на основную сборку Microsoft.Office.Interop.InfoPath.dll, установленную в глобальном кэше сборок (GAC) программой установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="64730-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="64730-117">Настройка ссылки на основную сборку межкоферной связи Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="64730-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="64730-118">Откройте проект Visual Studio управляемого кода.</span><span class="sxs-lookup"><span data-stu-id="64730-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="64730-119">В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="64730-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="64730-120">На **вкладке COM** дважды **щелкните библиотеку типов Microsoft InfoPath 3.0** и нажмите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="64730-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="64730-121">Чтобы установить ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml, перейдите к файлу Microsoft.Office.Interop.InfoPath.Xml.dll, установленного по умолчанию в папке < _drive_>:\Program Files\Microsoft Office\OFFICE14.</span><span class="sxs-lookup"><span data-stu-id="64730-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="64730-122">Хотя вы указываете копию сборки в локальной файловой системе, эта процедура устанавливает ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml.dll, установленную в глобальном кэше сборок (GAC) программой установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="64730-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="64730-123">Настройка ссылки на сборку Microsoft.Office.Interop.InfoPath.Xml междомения</span><span class="sxs-lookup"><span data-stu-id="64730-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="64730-124">Откройте или создайте проект Visual Studio управляемого кода, например консольное приложение **или** **приложение для Windows.**</span><span class="sxs-lookup"><span data-stu-id="64730-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="64730-125">В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="64730-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="64730-126">На вкладке **.NET** нажмите кнопку **"Обзор",** перейдите на диск <>:\Program Files\Microsoft Office\OFFICE14 и нажмите кнопку Microsoft.Office.Interop.InfoPath.Xml.dll. </span><span class="sxs-lookup"><span data-stu-id="64730-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="64730-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="64730-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="64730-128">Автоматизация изменения значения поля</span><span class="sxs-lookup"><span data-stu-id="64730-128">Automate changing the value of a field</span></span>

<span data-ttu-id="64730-129">Предположим, что один из пользователей шаблона формы отчета о продажах InfoPath недавно изменил свое имя с "Company A" на "Company B".</span><span class="sxs-lookup"><span data-stu-id="64730-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="64730-130">Разработчику будет предложено написать код, который будет автоматически обновлять формы отчетов о продажах, сохраненные из этого шаблона формы, в связи с изменением имени.</span><span class="sxs-lookup"><span data-stu-id="64730-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="64730-131">В следующем сценарии предполагается, что форма содержит текстовое поле, привязанное к полю customerName.</span><span class="sxs-lookup"><span data-stu-id="64730-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="64730-132">Создание образца шаблона формы и формы</span><span class="sxs-lookup"><span data-stu-id="64730-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="64730-133">Откройте InfoPath и создайте пустой шаблон формы.</span><span class="sxs-lookup"><span data-stu-id="64730-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="64730-134">Добавьте в **форму текстовое** поле и привяжйте поле, привязанное к имени клиента.</span><span class="sxs-lookup"><span data-stu-id="64730-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="64730-135">В области **задач** "Поля" щелкните правой кнопкой мыши папку **myFields** и выберите **"Свойства".**</span><span class="sxs-lookup"><span data-stu-id="64730-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="64730-136">На **вкладке "Сведения"** выберите и скопируйте значение из следующего пространства **имен:** и в paste this into Notepad or some other location where you can retrieve it.</span><span class="sxs-lookup"><span data-stu-id="64730-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="64730-137">Это значение потребуется позже для установки значения свойства **SelectionNamespaces** в коде.</span><span class="sxs-lookup"><span data-stu-id="64730-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="64730-138">Опубликуем шаблон формы в папке C:\Test и примите имя по умолчанию Template1.</span><span class="sxs-lookup"><span data-stu-id="64730-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="64730-139">Откройте шаблон формы, добавьте название "Company A" в текстовое поле, привязанное к полю customerName, а затем сохраните форму как "Form1".</span><span class="sxs-lookup"><span data-stu-id="64730-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="64730-140">Создайте консольное приложение с управляемым кодом, чтобы изменить имя с "Company A" на "Company B"</span><span class="sxs-lookup"><span data-stu-id="64730-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="64730-141">Откройте Visual Studio и создайте новое консольное приложение Visual C# или Visual Basic UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="64730-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="64730-142">Создание ссылок на основные Microsoft Office infoPath и XML-сборки, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="64730-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="64730-143">Добавьте следующий код в файл Program.cs или Module1.vb, обязательно обновив значение пространства имен в параметре для свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы.</span><span class="sxs-lookup"><span data-stu-id="64730-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="64730-144">Нажмите **кнопку "Начать отладку"** в меню **"Отладка",** чтобы скомпилировать и запустить консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="64730-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="64730-145">Приложение открывает форму, сохраненную как Form1.xml и циклы по всем элементам customerName, которые содержат значение Company A и изменяет это значение на Company B. После завершения операции новая копия формы будет сохранена Form2.xml папке C:\Test.</span><span class="sxs-lookup"><span data-stu-id="64730-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="64730-146">Автоматизация открытия формы и заполнения значений полей</span><span class="sxs-lookup"><span data-stu-id="64730-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="64730-147">Следующий пример автоматизирует открытие пустой формы и заполнение полей имени, фамилии и адреса в форме.</span><span class="sxs-lookup"><span data-stu-id="64730-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="64730-148">В этом сценарии предполагается форма, которая содержит три текстовых поля, привязанных к полям FirstName, LastName и Address.</span><span class="sxs-lookup"><span data-stu-id="64730-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="64730-149">Создание образца шаблона формы и формы</span><span class="sxs-lookup"><span data-stu-id="64730-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="64730-150">Откройте InfoPath и создайте пустую форму.</span><span class="sxs-lookup"><span data-stu-id="64730-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="64730-151">Добавьте три текстовых поля в форму и назовйте поля, привязанные к элементу управления: FirstName, LastName и Address.</span><span class="sxs-lookup"><span data-stu-id="64730-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="64730-152">Добавьте любые другие нужные поля.</span><span class="sxs-lookup"><span data-stu-id="64730-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="64730-153">В области **задач** "Поля" щелкните правой кнопкой мыши папку **myFields** и выберите **"Свойства".**</span><span class="sxs-lookup"><span data-stu-id="64730-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="64730-154">На **вкладке "Сведения"** выберите и скопируйте значение из следующего пространства **имен:** и в paste this into Notepad or some other location where you can retrieve it.</span><span class="sxs-lookup"><span data-stu-id="64730-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="64730-155">Это значение потребуется позже для установки значения свойства **SelectionNamespaces** в коде.</span><span class="sxs-lookup"><span data-stu-id="64730-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="64730-156">Опубликуем шаблон формы в папке C:\Temp и примите имя по умолчанию Template1.</span><span class="sxs-lookup"><span data-stu-id="64730-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="64730-157">Откройте шаблон формы и сохраните пустую форму в формате "Form1" в C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="64730-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="64730-158">Создание консольного приложения с управляемым кодом для открытия формы и заполнения полей</span><span class="sxs-lookup"><span data-stu-id="64730-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="64730-159">Откройте Visual Studio и создайте новое консольное приложение Visual C# Visual Basic с именем OpenForm.</span><span class="sxs-lookup"><span data-stu-id="64730-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="64730-160">Создание ссылок на основные Microsoft Office infoPath и XML-сборки, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="64730-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="64730-161">Добавьте следующий код в файл Program.cs или Module1.vb, обязательно обновив значение пространства имен в параметре для свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы.</span><span class="sxs-lookup"><span data-stu-id="64730-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="64730-162">В меню **"Отладка"** щелкните **"Начать** отладку", чтобы скомпилировать и запустить консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="64730-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="64730-163">Приложение откроет форму, сохраненную как Form1.xml и заполнит поля FirstName, LastName и Address значениями, указанными в коде, а затем сохранит форму, оставив InfoPath открытым.</span><span class="sxs-lookup"><span data-stu-id="64730-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="64730-164">См. также</span><span class="sxs-lookup"><span data-stu-id="64730-164">See also</span></span>

- [<span data-ttu-id="64730-165">Сведения об основной сборке взаимодействия Microsoft Office InfoPath</span><span class="sxs-lookup"><span data-stu-id="64730-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="64730-166">Сведения о сборке взаимодействия XML InfoPath</span><span class="sxs-lookup"><span data-stu-id="64730-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

