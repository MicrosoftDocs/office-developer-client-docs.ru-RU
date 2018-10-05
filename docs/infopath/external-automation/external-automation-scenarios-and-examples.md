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
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383165"
---
# <a name="external-automation-scenarios-and-examples"></a>Сценарии внешней автоматизации и примеры

Члены предоставлено Microsoft Office InfoPath основной сборки взаимодействия (Microsoft.Office.Interop.InfoPath.dll) и сборке взаимодействия InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) поддержку написания управляемого кода для автоматизации InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Создание ссылок на сборки основной взаимодействия Microsoft Office InfoPath и InfoPath XML взаимодействия

Для создания управляемого кода для автоматизации InfoPath, необходимо установить ссылки на основной сборке взаимодействия Microsoft InfoPath и сборки взаимодействия InfoPath XML. Основной сборки взаимодействия Microsoft InfoPath поддерживает взаимодействие с помощью объектной модели COM, предоставляемые элементом IPEDITOR. DLL-Библиотеку с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . Сборки взаимодействия InfoPath XML поддерживает взаимодействие с помощью объектной модели COM, предоставляемые с Microsoft XML Core Services (MSXML) с помощью членов пространства имен [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Для приложений с управляемым кодом, которые автоматизируют InfoPath пользователям InfoPath, основной сборки взаимодействия Microsoft Office InfoPath и сборке взаимодействия InfoPath XML, установленных на их компьютерах. **Поддержка программирования .NET** в программе установки InfoPath был установлен на **запускать с моего компьютера** для обычной установки InfoPath.
>  
> В результате установке до .NET Framework 1.1 распространяемого или .NET Framework 1.1 Software Development Kit (SDK) или более поздняя версия этих сборок взаимодействия будет также установлен по умолчанию. Если эти сборки взаимодействия недоступны на компьютере пользователя, необходимо подтвердить, что установки .NET Framework 1.1 или более поздней версии и запустите **программы и компоненты** **Панели управления** для изменения программы установки и настройки **программирования .NET Поддержка** параметр InfoPath, чтобы **запускать с моего компьютера**. 
  
Далее описывается, как задать ссылки на основной сборке взаимодействия Microsoft Office InfoPath и InfoPath XML сборки взаимодействия в проекте Visual Studio.
  
Чтобы задать ссылку на основной сборки взаимодействия Microsoft.Office.Interop.InfoPath, задайте ссылку на **Библиотеку типа Microsoft InfoPath 3.0** на вкладку **COM** диалогового окна **Добавить ссылку** . Несмотря на то, что нужно задать ссылку на вкладке **COM** , ссылку устанавливается в основной сборке взаимодействия Microsoft.Office.Interop.InfoPath.dll, которая устанавливается в глобальный кэш сборок (GAC), программа установки InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Задайте ссылку на основной сборки взаимодействия Microsoft.Office.Interop.InfoPath

1. Откройте проект управляемого кода в Visual Studio.
    
2. В **Обозревателе решений**щелкните правой кнопкой мыши **ссылки**и выберите команду **Добавить ссылку**.
    
3. На вкладке **COM** дважды щелкните **Библиотека типов Microsoft InfoPath 3.0**и нажмите кнопку **ОК**.
    
Чтобы задать ссылку на сборку взаимодействия Microsoft.Office.Interop.InfoPath.Xml, перейдите к файлу Microsoft.Office.Interop.InfoPath.Xml.dll, установленной по умолчанию в < _диск_>: \Program Files\Microsoft Office\OFFICE14 папки . Несмотря на то, что указан копии сборки в локальной файловой системе, эта процедура устанавливает ссылку на сборку Microsoft.Office.Interop.InfoPath.Xml.dll, которая устанавливается в глобальный кэш сборок (GAC), программа установки InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Задать ссылку на сборку взаимодействия Microsoft.Office.Interop.InfoPath.Xml

1. Откройте или создайте проект управляемого кода в Visual Studio, такие как **Консольное приложение** или **Приложение Windows**.
    
2. В **Обозревателе решений**щелкните правой кнопкой мыши **ссылки**и выберите команду **Добавить ссылку**.
    
3. На вкладке **.NET** , нажмите кнопку **Обзор**, перейдите к < _диск_>: \Program Files\Microsoft Office\OFFICE14 папки, а затем нажмите кнопку Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Нажмите кнопку **ОК**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Автоматизация при изменении значения поля

Предположим, что один из клиентов пользователя шаблон формы InfoPath отчет о продажах недавно изменен его имя компании «A» в «компания б». Разработчик требуется написать код, который будет автоматически обновлять отчет о продажах формы, сохраненные в этот шаблон формы в соответствии с изменением имени. Следующие сценарии предполагается наличие формы, который содержит текстовое поле, к которому привязан к полю с именем customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Создайте образец шаблона форм и форм

1. Откройте InfoPath и создайте шаблон пустой формы.
    
2. Добавьте в форму элемент управления **Текстовое поле** и имя поля, связанного с customerName элемента управления.
    
3. В области задач **поля** щелкните правой кнопкой мыши папку **myFields** и выберите пункт **Свойства**.
    
4. На вкладке **сведения** выберите и скопируйте следующее значение **пространство имен:**, а затем вставить скрипт в блокноте или другом местоположении, где его можно получить. Необходимо будет это значение более поздней версии для установки значения свойства **SelectionNamespaces** в коде. 
    
5. Публикация шаблона формы в папку с именем C:\Test и примите имя по умолчанию шаблон1. 
    
6. Откройте шаблон формы, добавьте имя «Компании A» в текстовом поле, связанный с полем customerName и затем сохранить форму как «Form1». 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Создание консольного приложения управляемого кода для изменения имени компании «A» для «Компании B»

1. Откройте Visual Studio и создайте новый Visual C# или Visual Basic консольного приложения с именем UpdateCustomer.
    
2. Установите ссылки на основной сборке взаимодействия Microsoft Office InfoPath и InfoPath XML сборок взаимодействия, как описано выше.
    
3. Добавьте следующий код в файле Program.cs или Module1.vb, убедитесь, что обновление значение пространства имен в текущее значение свойства **SelectionNamespaces** со значением, скопированные во время создания пример формы. 
    
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
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

4. Нажмите кнопку **Начать отладку** в меню **Отладка** , чтобы скомпилировать и запустить консольное приложение. 
    
   Приложение открывает форму, сохраняемый в виде Form1.xml и перебирает все элементы customerName, которые содержат значение компании A и изменяет это значение на компании B. После завершения операции новую копию формы сохраняется в виде Form2.xml в папке C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Автоматизировать открытия формы и заполнение значений полей

Следующий пример автоматизирует Открытие пустая форма и заполнение имя, Фамилия и поля адреса в форме. Этот сценарий предполагает форме, которая содержит три текстовых полей, которые связаны с полями с именами FirstName, LastName и адрес.
  
### <a name="create-the-sample-form-template-and-form"></a>Создайте образец шаблона форм и форм

1. Откройте InfoPath и создайте пустой формы.
    
2. Добавьте три элемента управления текстовых полей в форму и назовите полей, привязанных к элементам управления: FirstName, LastName и адрес. Добавьте нужные поля.
    
3. В области задач **поля** щелкните правой кнопкой мыши папку **myFields** и выберите пункт **Свойства**.
    
4. На вкладке **сведения** выберите и скопируйте следующее значение **пространство имен:**, а затем вставить скрипт в блокноте или другом местоположении, где его можно получить. Необходимо будет это значение более поздней версии для установки значения свойства **SelectionNamespaces** в коде. 
    
5. Публикация шаблона формы в папку с именем C:\Temp и примите имя по умолчанию шаблон1.
    
6. Откройте шаблон формы и сохранить как «Form1», чтобы C:\Temp пустая форма.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Создание консольного приложения управляемого кода для открытия формы и заполнения полей

1. Откройте Visual Studio и создайте новый Visual C# или Visual Basic консольного приложения с именем ОткрытьФорму.
    
2. Установите ссылки на основной сборке взаимодействия Microsoft Office InfoPath и InfoPath XML сборок взаимодействия, как описано выше.
    
3. Добавьте следующий код в файле Program.cs или Module1.vb, убедитесь, что обновление значение пространства имен в текущее значение свойства **SelectionNamespaces** со значением, скопированные во время создания пример формы. 
    
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
            doc.setProperty("SelectionNamespaces","xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
          doc.setProperty("SelectionNamespaces", "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. В меню **Отладка** выберите **Начать отладку** , чтобы скомпилировать и запустить консольное приложение. 
    
   Приложение будет Открытие формы, сохраняемый в виде Form1.xml и заполните поля FirstName, LastName и адрес с помощью значения, заданные в примере кода и сохраните форму, не закрывая InfoPath. 
    
## <a name="see-also"></a>См. также

- [Сведения об основной сборке взаимодействия Microsoft Office InfoPath](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Сведения о сборке взаимодействия XML InfoPath](about-the-infopath-xml-interop-assembly.md)

