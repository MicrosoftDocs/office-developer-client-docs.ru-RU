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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299722"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003

Проекты шаблонов форм, работающие с объектной моделью InfoPath 2003, используют службы MSXML для внутренней работы с XML. В управляемом коде зачастую проще воспользоваться поддержкой XML, предоставляемой пространством имен **System.Xml** в библиотеке классов .NET. Службы MSXML и файл **System.Xml** изначально не могут обмениваться объектами, поэтому при необходимости передать XML-данные между InfoPath и другим управляемым кодом требуется преобразовать XML-данные. Передавать XML-данные из объектов **System.Xml** в код формы InfoPath можно с помощью методик, приведенных в этой теме. 
  
Чтобы использовать элементы пространства имен **System.Xml** в проекте с управляемым кодом, где используется объектная модель InfoPath 2003, необходимо добавить ссылку на **System.Xml** на вкладке **.NET** диалогового окна **Добавить ссылку** в наборе Visual Studio 2012. 
  
 **Примечания**
  
- Справочную информацию о MSXML см. в разделе MSXML SDK.
    
- Элементы объектной модели MSXML, реализуемые пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , нельзя назначать делегатам в коде формы для шаблонов форм с управляемым кодом. 
    
- Если выполняется обновление кода шаблона формы для использования объектной модели, предоставляемой элементами пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , то по умолчанию используется **System.Xml**. Однако в этом случае необходимо вручную преобразовать весь код для использования новой объектной модели. Чтобы преобразовать шаблон формы для новой объектной модели, в категории **Программирование** диалогового окна **Параметры формы** щелкните **Обновить объектную модель**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Загрузка полной модели XML DOM из файла System.Xml

В следующем примере кода демонстрируется загрузка полной модели XML DOM из кода **System.Xml** с помощью метода InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) и элементов служб MSXML, реализуемых пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
В следующих примерах требуется директива **using** или **Imports** для **System.Xml** в разделе объявлений модуля кода формы. Кроме того, поскольку метод **Load** класса **XmlDocument** требует разрешений **System.Security.Permissions.FileIOPermission**, необходимо настроить уровень безопасности шаблона формы как **Полное доверие**, используя категорию **Безопасность и доверие** диалогового окна **Параметры формы**. 
  
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

## <a name="loading-a-single-node-from-systemxml"></a>Загрузка отдельного узла из файла System.Xml

В следующем примере кода приводится функция, демонстрирующая метод клонирования отдельного узла из **System.Xml**. Элемент **XmlElement** использует реализованный метод MSXML **createNode**. 
  
В следующем примере требуется директива **using** или **Imports** для **System.Xml** в разделе объявлений модуля кода формы. 
  
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


