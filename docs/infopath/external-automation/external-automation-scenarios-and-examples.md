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
# <a name="external-automation-scenarios-and-examples"></a>Сценарии и примеры автоматизации с использованием внешних решений

Участники основной сборки Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) и сборки интеропов InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) поддерживают написание управляемого кода для автоматизации InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Создание ссылок на сборки Microsoft Office InfoPath и XML-сборки InfoPath

Чтобы написать управляемый код для автоматизации InfoPath, необходимо установить ссылки на первичное интеропоп microsoft InfoPath и сборки XML InfoPath. Основная сборка интероп-сборки Microsoft InfoPath обеспечивает поддержку обеспечения связи с объектной моделью COM, IPEDITOR.DLL с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) Сборка межконтинента InfoPath XML обеспечивает поддержку обеспечения связи с объектной моделью COM, MSXML (MSXML) с помощью [членов пространства](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) именMicrosoft.Office.Interop.InfoPath.Xml. 
  
> [!IMPORTANT]
> Пользователи приложений с управляемым кодом, которые автоматизуют InfoPath, должны иметь infoPath, первичную сборку Microsoft Office InfoPath и сборку межсетей InfoPath XML, установленную на их компьютерах. Параметр **.NET Programmability Support** в программе установки  InfoPath должен запускаться с моего компьютера для типичной установки InfoPath.
>  
> В результате, до тех пор, пока платформа .NET Framework 1.1 Перераспределяемый или платформа .NET Framework 1.1 Комплект разработки программного обеспечения (SDK) или более поздний, эти сборки интеропов также будут установлены по умолчанию. Если эти сборки не доступны на компьютере пользователя, необходимо подтвердить, что установлен платформа .NET Framework 1.1 или  более поздней сборки, а затем запустить программы и функции из панели управления, чтобы изменить установку и установить параметр поддержки программных возможностей **InfoPath** для запуска с моего компьютера **.**  
  
В следующих процедурах описывается, как установить ссылки на основное Microsoft Office InfoPath и сборки интеропов InfoPath XML в Visual Studio проекте.
  
Чтобы установить ссылку на Microsoft. Office.Interop.InfoPath основная сборка межобучаемой связи, установите ссылку на библиотеку типа **Microsoft InfoPath 3.0** на вкладке **COM** диалогового окна **Add Reference.** Несмотря на то, что вы установите ссылку со вкладки **COM,** установлена ссылка на первичную сборку Microsoft.Office.Interop.InfoPath.dll, установленную в кэше глобальной сборки (GAC) программой установки InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Установите ссылку на Microsoft. Office.Interop.InfoPath первичная сборка интеропов

1. Откройте проект Visual Studio управляемого кода.
    
2. В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.
    
3. На **вкладке COM** дважды щелкните **библиотеку типа Microsoft InfoPath 3.0** и нажмите **кнопку ОК.**
    
Чтобы установить ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml, просмотрите файл Microsoft.Office.Interop.InfoPath.Xml.dll, установленный по умолчанию в  папке < диска>:\Program Files\Microsoft Office\OFFICE14. Даже если вы указываете копию сборки в локальной файловой системе, эта процедура устанавливает ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml.dll, установленную в кэше глобальной сборки (GAC) программой установки InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Установите ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml связи

1. Откройте или создайте проект управляемого кода Visual Studio, например консольное приложение **или Windows application.** 
    
2. В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.
    
3. На вкладке **.NET** щелкните **Обзор,** _перейдите_ к < диска>:\Program Files\Microsoft Office\OFFICE14 папке, а затем нажмите Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Нажмите кнопку **ОК**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Автоматизация изменения значения поля

Предположим, что один из клиентов шаблона формы формы отчетов о продажах InfoPath недавно изменил свое имя с "Компания A" на "Компания B". Разработчику будет предложено написать код, который автоматически обновляет формы отчетов о продажах, сохраненные из этого шаблона форм, чтобы отразить изменение имени. Следующий сценарий предполагает форму, которая содержит текстовое поле, связанное с полем с именем клиента.
  
### <a name="create-the-sample-form-template-and-form"></a>Создание шаблона и формы образца формы

1. Откройте InfoPath и создайте пустой шаблон формы.
    
2. Добавьте в **форму** управление текстовым полем и назови поле, привязанное к имени клиента управления.
    
3. В области **задач Fields** щелкните правой кнопкой мыши **папку myFields** и нажмите кнопку **Свойства**.
    
4. На **вкладке Подробные** сведения выберите и скопируйте значение, следующее пространство **имен:** и вклеите его в Блокнот другое расположение, где его можно получить. Это значение потребуется позднее для настройки значения свойства **SelectionNamespaces** в коде. 
    
5. Опубликуй шаблон формы в папку C:\Test и прими имя по умолчанию Template1. 
    
6. Откройте шаблон формы, добавьте имя "Company A" в текстовое поле, связанное с полем customerName, а затем сохраните форму как "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Создайте управляемое приложение консоли кода, чтобы изменить имя с "Company A" на "Company B"

1. Откройте Visual Studio и создайте новое приложение visual C# или Visual Basic с именем UpdateCustomer.
    
2. Создание ссылок на основные Microsoft Office infoPath и сборки XML InfoPath, как описано выше.
    
3. Добавьте следующий код в файл Program.cs или Module1.vb, чтобы обновить значение пространства имен в параметре свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы. 
    
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

4. Нажмите **кнопку Пуск отладки** в меню **отладки** для компиляции и запуска приложения консоли. 
    
   Приложение открывает форму, сохраненную как Form1.xml и циклы через все элементы customerName, содержащие значение Company A и изменения этого значения в компании B. После завершения операции новая копия формы будет сохранена Form2.xml папке C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Автоматизация открытия формы и заполнения значений поля

В следующем примере автоматизируется открытие пустой формы и заполнение полей имени, фамилии и адресов в форме. Этот сценарий предполагает форму, которая содержит три текстовых поля, привязанных к полям с именами FirstName, LastName и Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Создание шаблона и формы образца формы

1. Откройте InfoPath и создайте пустую форму.
    
2. Добавьте в форму три элемента управления текстовым полем и назови поля, связанные с элементами управления: FirstName, LastName и Address. Добавьте любые другие нужные поля.
    
3. В области **задач Fields** щелкните правой кнопкой мыши **папку myFields** и нажмите кнопку **Свойства**.
    
4. На **вкладке Подробные** сведения выберите и скопируйте значение, следующее пространство **имен:** и вклеите его в Блокнот другое расположение, где его можно получить. Это значение потребуется позднее для настройки значения свойства **SelectionNamespaces** в коде. 
    
5. Опубликуй шаблон формы в папку C:\Temp и прими имя по умолчанию Template1.
    
6. Откройте шаблон формы и сохраните пустую форму как "Form1" для C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Создайте управляемое приложение консоли кода, чтобы открыть форму и заполнить поля

1. Откройте Visual Studio и создайте новое приложение visual C# или Visual Basic с именем OpenForm.
    
2. Создание ссылок на основные Microsoft Office infoPath и сборки XML InfoPath, как описано выше.
    
3. Добавьте следующий код в файл Program.cs или Module1.vb, чтобы обновить значение пространства имен в параметре свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы. 
    
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

4. В меню **отладки** нажмите **кнопку Пуск отладки** для компиляции и запуска приложения консоли. 
    
   Приложение откроет форму, сохраненную как Form1.xml, и заполнит поля FirstName, LastName и Address значениями, указанными в коде, а затем сохранит форму, оставив InfoPath открытой. 
    
## <a name="see-also"></a>См. также

- [Сведения об основной сборке взаимодействия Microsoft Office InfoPath](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Сведения о сборке взаимодействия XML InfoPath](about-the-infopath-xml-interop-assembly.md)

