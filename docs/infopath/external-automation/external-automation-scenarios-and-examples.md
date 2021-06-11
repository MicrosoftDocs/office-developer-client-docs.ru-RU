---
title: Сценарии и примеры автоматизации с использованием внешних решений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- автоматизация infopath 2007,forms [InfoPath 2007], добавление данных программным образом,автоматизация [InfoPath 2007], внешние сценарии
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Участники основной сборки Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) и сборки интеропов InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) поддерживают написание управляемого кода для автоматизации InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537817"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="a2065-104">Сценарии и примеры автоматизации с использованием внешних решений</span><span class="sxs-lookup"><span data-stu-id="a2065-104">External automation scenarios and examples</span></span>

<span data-ttu-id="a2065-105">Участники основной сборки Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) и сборки интеропов InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) поддерживают написание управляемого кода для автоматизации InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a2065-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="a2065-106">Создание ссылок на сборки Microsoft Office InfoPath и XML-сборки InfoPath</span><span class="sxs-lookup"><span data-stu-id="a2065-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="a2065-107">Чтобы написать управляемый код для автоматизации InfoPath, необходимо установить ссылки на первичное интеропоп microsoft InfoPath и сборки XML InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a2065-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="a2065-108">Основная сборка интероп-сборки Microsoft InfoPath обеспечивает поддержку обеспечения связи с объектной моделью COM, IPEDITOR.DLL с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2065-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="a2065-109">Сборка межконтинента InfoPath XML обеспечивает поддержку обеспечения связи с объектной моделью COM, MSXML (MSXML) с помощью [членов пространства](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) именMicrosoft.Office.Interop.InfoPath.Xml.</span><span class="sxs-lookup"><span data-stu-id="a2065-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a2065-110">Пользователи приложений с управляемым кодом, которые автоматизуют InfoPath, должны иметь infoPath, первичную сборку Microsoft Office InfoPath и сборку межсетей InfoPath XML, установленную на их компьютерах.</span><span class="sxs-lookup"><span data-stu-id="a2065-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="a2065-111">Параметр **.NET Programmability Support** в программе установки  InfoPath должен запускаться с моего компьютера для типичной установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a2065-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="a2065-112">В результате, до тех пор, пока платформа .NET Framework 1.1 Перераспределяемый или платформа .NET Framework 1.1 Комплект разработки программного обеспечения (SDK) или более поздний, эти сборки интеропов также будут установлены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2065-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="a2065-113">Если эти сборки не доступны на компьютере пользователя, необходимо подтвердить, что установлен платформа .NET Framework 1.1 или  более поздней сборки, а затем запустить программы и функции из панели управления, чтобы изменить установку и установить параметр поддержки программных возможностей **InfoPath** для запуска с моего компьютера **.** </span><span class="sxs-lookup"><span data-stu-id="a2065-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="a2065-114">В следующих процедурах описывается, как установить ссылки на основное Microsoft Office InfoPath и сборки интеропов InfoPath XML в Visual Studio проекте.</span><span class="sxs-lookup"><span data-stu-id="a2065-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="a2065-115">Чтобы установить ссылку на Microsoft. Office.Interop.InfoPath основная сборка межобучаемой связи, установите ссылку на библиотеку типа **Microsoft InfoPath 3.0** на вкладке **COM** диалогового окна **Add Reference.**</span><span class="sxs-lookup"><span data-stu-id="a2065-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="a2065-116">Несмотря на то, что вы установите ссылку со вкладки **COM,** установлена ссылка на первичную сборку Microsoft.Office.Interop.InfoPath.dll, установленную в кэше глобальной сборки (GAC) программой установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a2065-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="a2065-117">Установите ссылку на Microsoft. Office.Interop.InfoPath первичная сборка интеропов</span><span class="sxs-lookup"><span data-stu-id="a2065-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="a2065-118">Откройте проект Visual Studio управляемого кода.</span><span class="sxs-lookup"><span data-stu-id="a2065-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="a2065-119">В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="a2065-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="a2065-120">На **вкладке COM** дважды щелкните **библиотеку типа Microsoft InfoPath 3.0** и нажмите **кнопку ОК.**</span><span class="sxs-lookup"><span data-stu-id="a2065-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="a2065-121">Чтобы установить ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml, просмотрите файл Microsoft.Office.Interop.InfoPath.Xml.dll, установленный по умолчанию в  папке < диска>:\Program Files\Microsoft Office\OFFICE14.</span><span class="sxs-lookup"><span data-stu-id="a2065-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="a2065-122">Даже если вы указываете копию сборки в локальной файловой системе, эта процедура устанавливает ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml.dll, установленную в кэше глобальной сборки (GAC) программой установки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a2065-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="a2065-123">Установите ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml связи</span><span class="sxs-lookup"><span data-stu-id="a2065-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="a2065-124">Откройте или создайте проект управляемого кода Visual Studio, например консольное приложение **или Windows application.** </span><span class="sxs-lookup"><span data-stu-id="a2065-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="a2065-125">В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="a2065-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="a2065-126">На вкладке **.NET** щелкните **Обзор,** _перейдите_ к < диска>:\Program Files\Microsoft Office\OFFICE14 папке, а затем нажмите Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="a2065-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="a2065-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a2065-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="a2065-128">Автоматизация изменения значения поля</span><span class="sxs-lookup"><span data-stu-id="a2065-128">Automate changing the value of a field</span></span>

<span data-ttu-id="a2065-129">Предположим, что один из клиентов шаблона формы формы отчетов о продажах InfoPath недавно изменил свое имя с "Компания A" на "Компания B".</span><span class="sxs-lookup"><span data-stu-id="a2065-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="a2065-130">Разработчику будет предложено написать код, который автоматически обновляет формы отчетов о продажах, сохраненные из этого шаблона форм, чтобы отразить изменение имени.</span><span class="sxs-lookup"><span data-stu-id="a2065-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="a2065-131">Следующий сценарий предполагает форму, которая содержит текстовое поле, связанное с полем с именем клиента.</span><span class="sxs-lookup"><span data-stu-id="a2065-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="a2065-132">Создание шаблона и формы образца формы</span><span class="sxs-lookup"><span data-stu-id="a2065-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="a2065-133">Откройте InfoPath и создайте пустой шаблон формы.</span><span class="sxs-lookup"><span data-stu-id="a2065-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="a2065-134">Добавьте в **форму** управление текстовым полем и назови поле, привязанное к имени клиента управления.</span><span class="sxs-lookup"><span data-stu-id="a2065-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="a2065-135">В области **задач Fields** щелкните правой кнопкой мыши **папку myFields** и нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a2065-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="a2065-136">На **вкладке Подробные** сведения выберите и скопируйте значение, следующее пространство **имен:** и вклеите его в Блокнот другое расположение, где его можно получить.</span><span class="sxs-lookup"><span data-stu-id="a2065-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="a2065-137">Это значение потребуется позднее для настройки значения свойства **SelectionNamespaces** в коде.</span><span class="sxs-lookup"><span data-stu-id="a2065-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="a2065-138">Опубликуй шаблон формы в папку C:\Test и прими имя по умолчанию Template1.</span><span class="sxs-lookup"><span data-stu-id="a2065-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="a2065-139">Откройте шаблон формы, добавьте имя "Company A" в текстовое поле, связанное с полем customerName, а затем сохраните форму как "Form1".</span><span class="sxs-lookup"><span data-stu-id="a2065-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="a2065-140">Создайте управляемое приложение консоли кода, чтобы изменить имя с "Company A" на "Company B"</span><span class="sxs-lookup"><span data-stu-id="a2065-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="a2065-141">Откройте Visual Studio и создайте новое приложение visual C# или Visual Basic с именем UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="a2065-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="a2065-142">Создание ссылок на основные Microsoft Office infoPath и сборки XML InfoPath, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="a2065-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="a2065-143">Добавьте следующий код в файл Program.cs или Module1.vb, чтобы обновить значение пространства имен в параметре свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы.</span><span class="sxs-lookup"><span data-stu-id="a2065-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="a2065-144">Нажмите **кнопку Пуск отладки** в меню **отладки** для компиляции и запуска приложения консоли.</span><span class="sxs-lookup"><span data-stu-id="a2065-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="a2065-145">Приложение открывает форму, сохраненную как Form1.xml и циклы через все элементы customerName, содержащие значение Company A и изменения этого значения в компании B. После завершения операции новая копия формы будет сохранена Form2.xml папке C:\Test.</span><span class="sxs-lookup"><span data-stu-id="a2065-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="a2065-146">Автоматизация открытия формы и заполнения значений поля</span><span class="sxs-lookup"><span data-stu-id="a2065-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="a2065-147">В следующем примере автоматизируется открытие пустой формы и заполнение полей имени, фамилии и адресов в форме.</span><span class="sxs-lookup"><span data-stu-id="a2065-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="a2065-148">Этот сценарий предполагает форму, которая содержит три текстовых поля, привязанных к полям с именами FirstName, LastName и Address.</span><span class="sxs-lookup"><span data-stu-id="a2065-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="a2065-149">Создание шаблона и формы образца формы</span><span class="sxs-lookup"><span data-stu-id="a2065-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="a2065-150">Откройте InfoPath и создайте пустую форму.</span><span class="sxs-lookup"><span data-stu-id="a2065-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="a2065-151">Добавьте в форму три элемента управления текстовым полем и назови поля, связанные с элементами управления: FirstName, LastName и Address.</span><span class="sxs-lookup"><span data-stu-id="a2065-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="a2065-152">Добавьте любые другие нужные поля.</span><span class="sxs-lookup"><span data-stu-id="a2065-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="a2065-153">В области **задач Fields** щелкните правой кнопкой мыши **папку myFields** и нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a2065-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="a2065-154">На **вкладке Подробные** сведения выберите и скопируйте значение, следующее пространство **имен:** и вклеите его в Блокнот другое расположение, где его можно получить.</span><span class="sxs-lookup"><span data-stu-id="a2065-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="a2065-155">Это значение потребуется позднее для настройки значения свойства **SelectionNamespaces** в коде.</span><span class="sxs-lookup"><span data-stu-id="a2065-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="a2065-156">Опубликуй шаблон формы в папку C:\Temp и прими имя по умолчанию Template1.</span><span class="sxs-lookup"><span data-stu-id="a2065-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="a2065-157">Откройте шаблон формы и сохраните пустую форму как "Form1" для C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="a2065-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="a2065-158">Создайте управляемое приложение консоли кода, чтобы открыть форму и заполнить поля</span><span class="sxs-lookup"><span data-stu-id="a2065-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="a2065-159">Откройте Visual Studio и создайте новое приложение visual C# или Visual Basic с именем OpenForm.</span><span class="sxs-lookup"><span data-stu-id="a2065-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="a2065-160">Создание ссылок на основные Microsoft Office infoPath и сборки XML InfoPath, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="a2065-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="a2065-161">Добавьте следующий код в файл Program.cs или Module1.vb, чтобы обновить значение пространства имен в параметре свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы.</span><span class="sxs-lookup"><span data-stu-id="a2065-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="a2065-162">В меню **отладки** нажмите **кнопку Пуск отладки** для компиляции и запуска приложения консоли.</span><span class="sxs-lookup"><span data-stu-id="a2065-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="a2065-163">Приложение откроет форму, сохраненную как Form1.xml, и заполнит поля FirstName, LastName и Address значениями, указанными в коде, а затем сохранит форму, оставив InfoPath открытой.</span><span class="sxs-lookup"><span data-stu-id="a2065-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a2065-164">См. также</span><span class="sxs-lookup"><span data-stu-id="a2065-164">See also</span></span>

- [<span data-ttu-id="a2065-165">Сведения об основной сборке взаимодействия Microsoft Office InfoPath</span><span class="sxs-lookup"><span data-stu-id="a2065-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="a2065-166">Сведения о сборке взаимодействия XML InfoPath</span><span class="sxs-lookup"><span data-stu-id="a2065-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

