---
title: Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Проекты шаблонов форм, работающие с объектной моделью InfoPath 2003, используют службы MSXML для внутренней работы с XML. В управляемом коде зачастую проще воспользоваться поддержкой XML, предоставляемой пространством имен System.Xml в библиотеке классов .NET. Службы MSXML и файл System.Xml изначально не могут обмениваться объектами, поэтому при необходимости передать XML-данные между InfoPath и другим управляемым кодом требуется преобразовать XML-данные. Передавать XML-данные из объектов System.Xml в код формы InfoPath можно с помощью методик, приведенных в этой теме.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437401"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="34d52-107">Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="34d52-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="34d52-p102">Проекты шаблонов форм, работающие с объектной моделью InfoPath 2003, используют службы MSXML для внутренней работы с XML. В управляемом коде зачастую проще воспользоваться поддержкой XML, предоставляемой пространством имен **System.Xml** в библиотеке классов .NET. Службы MSXML и файл **System.Xml** изначально не могут обмениваться объектами, поэтому при необходимости передать XML-данные между InfoPath и другим управляемым кодом требуется преобразовать XML-данные. Передавать XML-данные из объектов **System.Xml** в код формы InfoPath можно с помощью методик, приведенных в этой теме.</span><span class="sxs-lookup"><span data-stu-id="34d52-p102">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML. In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library. MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted. You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="34d52-112">Чтобы использовать элементы пространства имен **System.Xml** в проекте с управляемым кодом, где используется объектная модель InfoPath 2003, необходимо добавить ссылку на **System.Xml** на вкладке **.NET** диалогового окна **Добавить ссылку** в наборе Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="34d52-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="34d52-113">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="34d52-113">**Notes**</span></span>
  
- <span data-ttu-id="34d52-114">Справочную информацию о MSXML см. в разделе MSXML SDK.</span><span class="sxs-lookup"><span data-stu-id="34d52-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="34d52-115">Элементы объектной модели MSXML, реализуемые пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , нельзя назначать делегатам в коде формы для шаблонов форм с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="34d52-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="34d52-p103">Если выполняется обновление кода шаблона формы для использования объектной модели, предоставляемой элементами пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , то по умолчанию используется **System.Xml**. Однако в этом случае необходимо вручную преобразовать весь код для использования новой объектной модели. Чтобы преобразовать шаблон формы для новой объектной модели, в категории **Программирование** диалогового окна **Параметры формы** щелкните **Обновить объектную модель**.</span><span class="sxs-lookup"><span data-stu-id="34d52-p103">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively. However, when doing so, you must manually convert all of your code to use the new object model. To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="34d52-119">Загрузка полной модели XML DOM из файла System.Xml</span><span class="sxs-lookup"><span data-stu-id="34d52-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="34d52-120">В следующем примере кода демонстрируется загрузка полной модели XML DOM из кода **System.Xml** с помощью метода InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) и элементов служб MSXML, реализуемых пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="34d52-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="34d52-p104">В следующих примерах требуется директива **using** или **Imports** для **System.Xml** в разделе объявлений модуля кода формы. Кроме того, поскольку метод **Load** класса **XmlDocument** требует разрешений **System.Security.Permissions.FileIOPermission**, необходимо настроить уровень безопасности шаблона формы как **Полное доверие**, используя категорию **Безопасность и доверие** диалогового окна **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="34d52-p104">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module. Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
```cs
// Create a System.Xml XmlDocument and load an XML file.
XmlDocument doc = new XmlDocument();
doc.Load("c:\\temp\\MyFile.xml");
// Create an MSXML DOM object.
IXMLDOMDocument newDoc = thisXDocument.CreateDOM();
// Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml);
```

```vb
' Create a System.Xml XmlDocument and load an XML file.
Dim doc As XmlDocument = New XmlDocument()
doc.Load("c:\temp\MyFile.xml");
' Create an MSXML DOM object.
Dim newDoc As IXMLDOMDocument = thisXDocument.CreateDOM()
' Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml)
```

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="34d52-123">Загрузка отдельного узла из файла System.Xml</span><span class="sxs-lookup"><span data-stu-id="34d52-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="34d52-p105">В следующем примере кода приводится функция, демонстрирующая метод клонирования отдельного узла из **System.Xml**. Элемент **XmlElement** использует реализованный метод MSXML **createNode**.</span><span class="sxs-lookup"><span data-stu-id="34d52-p105">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**. **XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="34d52-126">В следующем примере требуется директива **using** или **Imports** для **System.Xml** в разделе объявлений модуля кода формы.</span><span class="sxs-lookup"><span data-stu-id="34d52-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
```cs
// This function takes a System.Xml XmlElement object and 
// an MSXML IXMLDOMDocument object, and returns an MSXML 
// IXMLDOMNode object that is a copy of the XmlElement object.
public IXMLDOMNode CloneSystemXmlElementToMsxml(
   XmlElement systemXmlElement, IXMLDOMDocument msxmlDocument)
{
   IXMLDOMNode msxmlResultNode;
   // Create a new element from the MSXML DOM using the same 
   // namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(
      DOMNodeType.NODE_ELEMENT, 
      systemXmlElement.Name, 
      systemXmlElement.NamespaceURI);
   // Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString();
   return msxmlResultNode;
}
```

```vb
' This function takes a System.Xml XmlElement object and 
' an MSXML IXMLDOMDocument object, and returns an MSXML 
' IXMLDOMNode object that is a copy of the XmlElement object.
Public Function CloneSystemXmlElementToMsxml(_
   XmlElement systemXmlElement, _
   IXMLDOMDocument msxmlDocument) As IXMLDOMNode
   Dim msxmlResultNode As IXMLDOMNode
   ' Create a new element from the MSXML DOM using the same 
   ' namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(_
      DOMNodeType.NODE_ELEMENT, _
      systemXmlElement.Name, _
      systemXmlElement.NamespaceURI)
   ' Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString()
   Return msxmlResultNode
End Function
```


