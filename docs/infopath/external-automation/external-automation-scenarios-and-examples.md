---
title: Сценарии и примеры автоматизации с использованием внешних решений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Автоматизация InfoPath 2007, Forms [InfoPath 2007], добавление данных программным путем, Автоматизация [InfoPath 2007], внешние сценарии
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Элементы, предоставляемые основной сборкой взаимодействия Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) и сборкой InfoPath XML Interop (Microsoft. Office. Interop. InfoPath. XML. dll), поддерживают написание управляемого кода для автоматизации InfoPath.
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310201"
---
# <a name="external-automation-scenarios-and-examples"></a>Сценарии и примеры автоматизации с использованием внешних решений

Элементы, предоставляемые основной сборкой взаимодействия Microsoft Office InfoPath (Microsoft. Office. Interop. InfoPath. dll) и сборкой InfoPath XML Interop (Microsoft. Office. Interop. InfoPath. XML. dll), поддерживают написание управляемого кода для автоматизации InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Установка ссылок на основные сборки взаимодействия Microsoft Office InfoPath и сборки XML-взаимодействия InfoPath

Для написания управляемого кода для автоматизации InfoPath необходимо установить ссылки на основные взаимодействия Microsoft InfoPath и сборки взаимодействия InfoPath XML. Основная сборка взаимодействия Microsoft InfoPath обеспечивает поддержку взаимодействия с объектной моделью COM, предоставляемой ИПЕДИТОР. DLL с помощью членов пространства имен [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . Сборка взаимодействия InfoPath в InfoPath обеспечивает поддержку взаимодействия с объектной моделью COM, предоставляемой основными службами Microsoft XML (MSXML), с помощью членов пространства имен [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Пользователи управляемых приложений с управляемым кодом, которые автоматизируют InfoPath, должны иметь InfoPath, основную сборку взаимодействия Microsoft Office InfoPath и сборку XML-взаимодействия InfoPath, установленную на их компьютерах. Параметр **Поддержка программирования .NET** в программе установки InfoPath настроен на **Запуск с моего компьютера** для обычной установки InfoPath.
>  
> В результате, если установлен распространяемый пакет .NET Framework 1,1 или пакет средств разработки программного обеспечения .NET Framework 1,1 (SDK) или более поздней версии, эти сборки взаимодействия также будут установлены по умолчанию. Если эти сборки взаимодействия недоступны на компьютере пользователя, необходимо убедиться в том, что установлена платформа .NET Framework 1,1 или более поздней версии, а затем запустить **программы и компоненты** с **панели управления** , чтобы изменить настройки программы установки и настроить возможности **программирования .NET. Поддержка** возможности InfoPath для **запуска с моего компьютера**. 
  
В следующих процедурах описывается, как задать ссылки на основные взаимодействия Microsoft Office InfoPath и сборки InfoPath XML Interop в проекте Visual Studio.
  
Чтобы задать ссылку на основную сборку взаимодействия Microsoft. Office. Interop. InfoPath, задайте ссылку на **библиотеку типов Microsoft InfoPath 3,0** на вкладке **com** диалогового окна **Добавление ссылки** . Несмотря на то, что вы задаете ссылку на вкладке **com** , в программе установки InfoPath устанавливается ссылка на основную сборку взаимодействия Microsoft. Office. Interop. InfoPath. dll, которая устанавливается в глобальном кэше сборок (GAC). 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Задайте ссылку на основную сборку взаимодействия Microsoft. Office. Interop. InfoPath.

1. Откройте проект Visual Studio с управляемым кодом.
    
2. В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.
    
3. На вкладке **com** дважды щелкните элемент **Библиотека типов Microsoft InfoPath 3,0**и нажмите кнопку **ОК**.
    
Чтобы задать ссылку на сборку взаимодействия Microsoft. Office. Interop. InfoPath. XML, найдите файл Microsoft. Office. Interop. InfoPath. XML. dll, установленный по умолчанию в папке _Лт_ _Drive__гт_: \Program Files\Microsoft office\office14. Folder . Несмотря на то, что вы указали копию сборки в локальной файловой системе, эта процедура создает ссылку на сборку Microsoft. Office. Interop. InfoPath. XML. dll, установленную в глобальном кэше сборок программой установки InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Задайте ссылку на сборку взаимодействия Microsoft. Office. Interop. InfoPath. XML.

1. Откройте или создайте проект управляемого кода Visual Studio, например консольное **приложение** или **приложение Windows**.
    
2. В окне **Обозреватель решений** щелкните правой кнопкой мыши **Ссылки**, а затем выберите команду **Добавить ссылку**.
    
3. На вкладке **.NET** нажмите кнопку **Обзор**, перейдите к папке _лт_ _Drive__гт_: \Program Files\Microsoft Office\office14. Folder, а затем выберите Microsoft. Office. Interop. InfoPath. XML. dll.
    
4. Нажмите кнопку **ОК**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Автоматизация изменения значения поля

Предположим, что один из клиентов пользователя в шаблоне формы отчета о продажах InfoPath недавно изменил свое имя с "Company A" на "Company B". Разработчику предлагается написать код, который будет автоматически обновлять формы отчета о продажах, сохраненные в этом шаблоне формы, в соответствии с изменением имени. В следующем сценарии предполагается форма, содержащая текстовое поле, которое привязано к полю с именем customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Создание образца шаблона формы и формы

1. Откройте InfoPath и создайте пустой шаблон формы.
    
2. Добавьте в форму элемент управления **"текстовое поле"** и присвойте полю имя, привязанному к элементу управления CustomerName.
    
3. В области задач **поля** щелкните правой кнопкой мыши папку **myFields** и выберите пункт **Свойства**.
    
4. На вкладке **сведения** выберите и скопируйте значение в поле **пространство имен:**, а затем вставьте его в Блокнот или другое место, где его можно восстановить. Это значение потребуется позже для установки значения свойства **селектионнамеспацес** в коде. 
    
5. Опубликуйте шаблон формы в папке с именем C:\Test и оставьте имя по умолчанию (Template1). 
    
6. Откройте шаблон формы, добавьте имя "Company A" в текстовое поле, связанное с полем customerName, а затем сохраните форму как "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Создание консольного приложения управляемого кода для изменения имени с "Company A" на "Company B"

1. Откройте Visual Studio и создайте консольное приложение Visual C# или Visual Basic с именем UpdateCustomer.
    
2. Создайте ссылки на сборки взаимодействия с основными взаимодействием Microsoft Office InfoPath и сборки InfoPath XML InfoPath, как описано выше.
    
3. Добавьте следующий код в файл Program.cs или Module1. vb, чтобы обновить значение пространства имен в параметре для свойства **селектионнамеспацес** со значением, скопированным при создании учебной формы. 
    
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

4. Для компиляции и запуска консольного приложения выберите команду **начать отладку** в меню **Отладка** . 
    
   Приложение открывает форму, сохраненную как Form1. XML, и выполняет цикл по всем элементам customerName, содержащим значение Company Company, и изменяет значение на Company B. После завершения операции новая копия формы сохраняется в виде Form2. XML в папке C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Автоматизация открытия формы и заполнение значений полей

В приведенном ниже примере показано, как автоматизировать открытие пустой формы и заполнение поля имя, фамилия и адрес в форме. В этом сценарии предполагается, что форма содержит три текстовых поля, которые привязаны к полям "FirstName", "LastName" и "Address".
  
### <a name="create-the-sample-form-template-and-form"></a>Создание образца шаблона формы и формы

1. Откройте InfoPath и создайте пустую форму.
    
2. Добавьте в форму три элемента управления текстового поля и назовите поля, привязанные к элементам управления: FirstName, LastName и Address. Добавьте любые другие нужные поля.
    
3. В области задач **поля** щелкните правой кнопкой мыши папку **myFields** и выберите пункт **Свойства**.
    
4. На вкладке **сведения** выберите и скопируйте значение в поле **пространство имен:**, а затем вставьте его в Блокнот или другое место, где его можно восстановить. Это значение потребуется позже для установки значения свойства **селектионнамеспацес** в коде. 
    
5. Опубликуйте шаблон формы в папке C:\Temp и оставьте имя по умолчанию (Template1).
    
6. Откройте шаблон формы и сохраните пустую форму как "Form1" в C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Создание консольного приложения управляемого кода для открытия формы и заполнения полей

1. Откройте Visual Studio и создайте консольное приложение Visual C# или Visual Basic с именем OpenForm.
    
2. Создайте ссылки на сборки взаимодействия с основными взаимодействием Microsoft Office InfoPath и сборки InfoPath XML InfoPath, как описано выше.
    
3. Добавьте следующий код в файл Program.cs или Module1. vb, чтобы обновить значение пространства имен в параметре для свойства **селектионнамеспацес** со значением, скопированным при создании учебной формы. 
    
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

4. В меню **Отладка** выберите команду **начать отладку** , чтобы скомпилировать и запустить консольное приложение. 
    
   Приложение будет открывать форму, сохраненную как Form1. XML, и заполните поля FirstName, LastName и Address значениями, указанными в коде, а затем сохраните форму, оставив InfoPath открытым. 
    
## <a name="see-also"></a>См. также

- [Сведения об основной сборке взаимодействия Microsoft Office InfoPath](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Сведения о сборке взаимодействия XML InfoPath](about-the-infopath-xml-interop-assembly.md)

