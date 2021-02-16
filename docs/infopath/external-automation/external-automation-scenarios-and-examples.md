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
# <a name="external-automation-scenarios-and-examples"></a>Сценарии и примеры автоматизации с использованием внешних решений

Члены, предоставляемые основной сборкой Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) и сборкой XML-кода (Microsoft.Office.Interop.InfoPath.Xml.dll) InfoPath, поддерживают написание управляемого кода для автоматизации InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Создание ссылок на сборки основного Microsoft Office InfoPath и XML-межпоиска InfoPath

Чтобы написать управляемый код для автоматизации InfoPath, необходимо установить ссылки на основное межкодовое и XML-сборки interop InfoPath. Основная сборка microsoft InfoPath обеспечивает поддержку обеспечения связи с объектной моделью COM, которая предоставляется IPEDITOR.DLL с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) Сборка XML-связи InfoPath обеспечивает поддержку обеспечения связи с объектной моделью COM, которая предоставляется MSXML [](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) (MSXML) с помощью членовMicrosoft.Office.Interop.InfoPath.Xmlпространства имен. 
  
> [!IMPORTANT]
> На компьютерах пользователей приложений с управляемым кодом, которые автоматизуют InfoPath, должны быть установлены InfoPath, основная сборка межсервейного Microsoft Office InfoPath и сборка XML-кода. Параметр **поддержки программируемости .NET** в программе установки  InfoPath настроен на запуск с моего компьютера для обычной установки InfoPath.
>  
> В результате, если установлен распространяемый пакет .NET Framework 1.1 или пакет SDK .NET Framework 1.1 или более поздней, эти сборки также будут установлены по умолчанию. Если эти сборки межпрограммного обеспечения недоступны на компьютере пользователя, необходимо подтвердить, что .NET Framework 1.1 или  более поздней установлена, а затем запустить программы и функции из панели управления, чтобы изменить настройку и настроить параметр поддержки программируемости **.NET** для InfoPath на запуск с моего **компьютера.**  
  
В следующих процедурах описывается, как установить ссылки на основное Microsoft Office infoPath и сборки XML-межсервации InfoPath в Visual Studio проекта.
  
Чтобы установить ссылку на основную сборку interop.InfoPath, установите ссылку на библиотеку типов **Microsoft InfoPath 3.0** на вкладке **COM** диалогового окна "Добавление ссылки".  Несмотря на то, что вы настроили ссылку на вкладку **COM,** эта ссылка устанавливается на основную сборку Microsoft.Office.Interop.InfoPath.dll, установленную в глобальном кэше сборок (GAC) программой установки InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Настройка ссылки на основную сборку межкоферной связи Microsoft.Office.Interop.InfoPath

1. Откройте проект Visual Studio управляемого кода.
    
2. В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.
    
3. На **вкладке COM** дважды **щелкните библиотеку типов Microsoft InfoPath 3.0** и нажмите кнопку **"ОК".**
    
Чтобы установить ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml, перейдите к файлу Microsoft.Office.Interop.InfoPath.Xml.dll, установленного по умолчанию в папке < _drive_>:\Program Files\Microsoft Office\OFFICE14. Хотя вы указываете копию сборки в локальной файловой системе, эта процедура устанавливает ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml.dll, установленную в глобальном кэше сборок (GAC) программой установки InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Настройка ссылки на сборку Microsoft.Office.Interop.InfoPath.Xml междомения

1. Откройте или создайте проект Visual Studio управляемого кода, например консольное приложение **или** **приложение для Windows.**
    
2. В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.
    
3. На вкладке **.NET** нажмите кнопку **"Обзор",** перейдите на диск <>:\Program Files\Microsoft Office\OFFICE14 и нажмите кнопку Microsoft.Office.Interop.InfoPath.Xml.dll. 
    
4. Нажмите **ОК**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Автоматизация изменения значения поля

Предположим, что один из пользователей шаблона формы отчета о продажах InfoPath недавно изменил свое имя с "Company A" на "Company B". Разработчику будет предложено написать код, который будет автоматически обновлять формы отчетов о продажах, сохраненные из этого шаблона формы, в связи с изменением имени. В следующем сценарии предполагается, что форма содержит текстовое поле, привязанное к полю customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Создание образца шаблона формы и формы

1. Откройте InfoPath и создайте пустой шаблон формы.
    
2. Добавьте в **форму текстовое** поле и привяжйте поле, привязанное к имени клиента.
    
3. В области **задач** "Поля" щелкните правой кнопкой мыши папку **myFields** и выберите **"Свойства".**
    
4. На **вкладке "Сведения"** выберите и скопируйте значение из следующего пространства **имен:** и в paste this into Notepad or some other location where you can retrieve it. Это значение потребуется позже для установки значения свойства **SelectionNamespaces** в коде. 
    
5. Опубликуем шаблон формы в папке C:\Test и примите имя по умолчанию Template1. 
    
6. Откройте шаблон формы, добавьте название "Company A" в текстовое поле, привязанное к полю customerName, а затем сохраните форму как "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Создайте консольное приложение с управляемым кодом, чтобы изменить имя с "Company A" на "Company B"

1. Откройте Visual Studio и создайте новое консольное приложение Visual C# или Visual Basic UpdateCustomer.
    
2. Создание ссылок на основные Microsoft Office infoPath и XML-сборки, как описано выше.
    
3. Добавьте следующий код в файл Program.cs или Module1.vb, обязательно обновив значение пространства имен в параметре для свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы. 
    
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

4. Нажмите **кнопку "Начать отладку"** в меню **"Отладка",** чтобы скомпилировать и запустить консольное приложение. 
    
   Приложение открывает форму, сохраненную как Form1.xml и циклы по всем элементам customerName, которые содержат значение Company A и изменяет это значение на Company B. После завершения операции новая копия формы будет сохранена Form2.xml папке C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Автоматизация открытия формы и заполнения значений полей

Следующий пример автоматизирует открытие пустой формы и заполнение полей имени, фамилии и адреса в форме. В этом сценарии предполагается форма, которая содержит три текстовых поля, привязанных к полям FirstName, LastName и Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Создание образца шаблона формы и формы

1. Откройте InfoPath и создайте пустую форму.
    
2. Добавьте три текстовых поля в форму и назовйте поля, привязанные к элементу управления: FirstName, LastName и Address. Добавьте любые другие нужные поля.
    
3. В области **задач** "Поля" щелкните правой кнопкой мыши папку **myFields** и выберите **"Свойства".**
    
4. На **вкладке "Сведения"** выберите и скопируйте значение из следующего пространства **имен:** и в paste this into Notepad or some other location where you can retrieve it. Это значение потребуется позже для установки значения свойства **SelectionNamespaces** в коде. 
    
5. Опубликуем шаблон формы в папке C:\Temp и примите имя по умолчанию Template1.
    
6. Откройте шаблон формы и сохраните пустую форму в формате "Form1" в C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Создание консольного приложения с управляемым кодом для открытия формы и заполнения полей

1. Откройте Visual Studio и создайте новое консольное приложение Visual C# Visual Basic с именем OpenForm.
    
2. Создание ссылок на основные Microsoft Office infoPath и XML-сборки, как описано выше.
    
3. Добавьте следующий код в файл Program.cs или Module1.vb, обязательно обновив значение пространства имен в параметре для свойства **SelectionNamespaces** со значением, которое вы скопировали при создании примера формы. 
    
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

4. В меню **"Отладка"** щелкните **"Начать** отладку", чтобы скомпилировать и запустить консольное приложение. 
    
   Приложение откроет форму, сохраненную как Form1.xml и заполнит поля FirstName, LastName и Address значениями, указанными в коде, а затем сохранит форму, оставив InfoPath открытым. 
    
## <a name="see-also"></a>См. также

- [Сведения об основной сборке взаимодействия Microsoft Office InfoPath](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Сведения о сборке взаимодействия XML InfoPath](about-the-infopath-xml-interop-assembly.md)

