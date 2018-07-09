---
title: Форматированный текст и веб-службы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath поддерживает присоединение элемента управления Форматированный текст в форме к элементу XML, полученному от веб-службы, с последующей отправкой данных из элемента управленияформатированный текстэлементу XML посредством веб-службы. Элемент должен соответствовать формату XHTML. Например, схема элемента с именем MyRichTextElement, содержащая форматированный текст, будет иметь следующее определение схемы XML:'
ms.openlocfilehash: 07a7a3dbc0f054160adce54e316b01797feacd8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807587"
---
# <a name="rich-text-and-web-services"></a><span data-ttu-id="0c749-105">Форматированный текст и веб-службы</span><span class="sxs-lookup"><span data-stu-id="0c749-105">Rich Text and Web Services</span></span>

<span data-ttu-id="0c749-p102">Microsoft InfoPath поддерживает присоединение элемента управления **Форматированный текст** в форме к элементу XML, полученному от веб-службы, с последующей отправкой данных из элемента управления "форматированный текст" элементу XML посредством веб-службы. Элемент должен соответствовать формату XHTML. Например, схема элемента с именем  `MyRichTextElement`, содержащая форматированный текст, будет иметь следующее определение схемы XML:</span><span class="sxs-lookup"><span data-stu-id="0c749-p102">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service. The element must adhere to the Extensible HyperText Markup Language (XHTML) format. For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

<span data-ttu-id="0c749-p103">Перед присоединением элемента управления **Форматированный текст** к элементу XHTML последний должен быть помещен в узел-оболочку; этот узел-оболочка может принадлежать любому произвольному пространству имен. Он может иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="0c749-p103">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace. The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="0c749-p104">В этой теме описан процесс создания веб-службы, способной отправлять и получать XHTML, а также процесс использования InfoPath для прикрепления параметров. Здесь не даются подробные инструкции по созданию веб-службы. Предполагается, что читающий уже имеет некоторый опыт работы с веб-службами.</span><span class="sxs-lookup"><span data-stu-id="0c749-p104">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters. This topic does not provide detailed instructions on how to create such a Web service. It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="0c749-114">Проектирование веб-службы для получения и отправки XHTML</span><span class="sxs-lookup"><span data-stu-id="0c749-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="0c749-p105">Использованная в примере веб-служба хранит данные XHTML, которые она отправляет и получает в XML-файле, на сервере. Этот файл с именем out.xml выполняет функцию источника данных, в котором хранятся данные XHTML. Существует два метода, позволяющих клиентскому приложению взаимодействовать с источником данных,   `getXhtml` и  `setXhtml`. Метод  `getXhtml` веб-службы возвращает **XmlNode**, содержащий XHTML, который можно прикрепить к элементу управления "форматированный текст" InfoPath. Метод  `setXhtml` веб-службы получает **XmlNode** в качестве данных для хранения в файле out.xml.</span><span class="sxs-lookup"><span data-stu-id="0c749-p105">The example Web service stores the XHTML data that it sends and receives in an XML file on the server. This file that is named out.xml, acts as a data source that stores the XHTML data. There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`. The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control. The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0c749-120">Эти веб-методы требуют использования операторов **using**, ссылающихся на пространства имен **System.IO** и **System.Xml**.</span><span class="sxs-lookup"><span data-stu-id="0c749-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="0c749-121">Метод  `getXhtml` пытается загрузить данные XML, возвращаемые из файла out.xml, в папку Data на диске C. Если это не удается, например, по причине отсутствия файла или отсутствия допустимого XML, метод возвращает пустой элемент HTML **DIV**, ссылающийся на пространство имен XHTML.</span><span class="sxs-lookup"><span data-stu-id="0c749-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "http://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "http://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"http://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

<span data-ttu-id="0c749-p106">Метод  `setXhtml` веб-службы получает XHTML от элемента управления **Форматированный текст** формы InfoPath. Поскольку веб-службы не поддерживают список узлов при отправке веб-службе поля с форматированным текстом, содержащего несколько строк, веб-служба получает только первую строку и игнорирует все остальные.</span><span class="sxs-lookup"><span data-stu-id="0c749-p106">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form. Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="0c749-p107">В образце метода  `setXhtml` предполагается, что он получает узел XML верхнего уровня, который в большинстве случаев помещен в оболочку элемента **DIV**. Если полученный XML не содержит элемент в оболочке, например если текст внутри элемента управления **Форматированный текст** не имеет форматирования, метод распознает это, проверяя, указывает ли свойство **NodeType** на то, что переданный XML является текстовым узлом. Если XML является текстовым узлом, метод создает элемент **DIV** и копирует содержимое текстового узла в **DIV**, чтобы элемент **DIV** содержал дочерний текстовый узел с текстом, отправленным веб-службе. Полученный методом XML записывается в файл out.xml в папке Data на диске C.</span><span class="sxs-lookup"><span data-stu-id="0c749-p107">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element. If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node. If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service. The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0c749-p108">Пример метода  `setXhtml` написан для получения данных XHTML любого объема. В действительности рекомендуется выяснить объем отправляемых данных и установить предельный объем.</span><span class="sxs-lookup"><span data-stu-id="0c749-p108">The sample  `setXhtml` method was written to accept XHTML data of any size. In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="0c749-130">Создание формы InfoPath, обменивающейся данными с образцом веб-службы</span><span class="sxs-lookup"><span data-stu-id="0c749-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="0c749-131">Выполните следующие действия, чтобы создать форму для тестирования образца веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0c749-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="0c749-132">Создание формы, подключающейся к образцу веб-службы</span><span class="sxs-lookup"><span data-stu-id="0c749-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="0c749-133">Откройте конструктор форм InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0c749-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="0c749-134">На вкладке **Создать** щелкните дважды **Веб-служба** в разделе **Дополнительные шаблоны форм**.</span><span class="sxs-lookup"><span data-stu-id="0c749-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="0c749-135">В диалоговом окне **мастера подключения данных** выберите **Получить данные** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="0c749-136">Укажите адрес веб-службы, содержащей образец методов веб-служб, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="0c749-137">Для метода получения выберите в качестве операции **getXhtml** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="0c749-138">Метод **getXHTML** веб-службы не имеет параметров, поэтому нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="0c749-139">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="0c749-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="0c749-140">На вкладке **Данные** в группе **Действия отправки** выберите **В другие расположения** и щелкните **Веб-служба**, чтобы использовать для отправки данных ту же веб-службу.</span><span class="sxs-lookup"><span data-stu-id="0c749-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="0c749-141">Укажите адрес веб-службы, содержащей образец методов веб-служб, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="0c749-142">Для метода отправки выберите в качестве операции **setXhtml** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="0c749-143">Щелкните **Изменить**, последовательно разверните папки **dataFields**, **s0:getXhtmlResponse** и **getXhtmlResult** и выберите элемент **MyRichTextElement**, после чего нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0c749-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="0c749-144">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="0c749-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="0c749-145">В области задач **Поля** разверните папку **dataFields**.</span><span class="sxs-lookup"><span data-stu-id="0c749-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="0c749-p109">Последовательно разверните папки **s0:getXhtmlResponse** и **getXhtmlResult** и перетащите элемент **MyRichTextElement** в форму. InfoPath определит, что элемент **MyRichTextElement** является элементом XHTML, и будет использовать для прикрепления к нему элемент управления "форматированный текст".</span><span class="sxs-lookup"><span data-stu-id="0c749-p109">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form. InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="0c749-148">Сохраните или опубликуйте форму.</span><span class="sxs-lookup"><span data-stu-id="0c749-148">Save or publish the form.</span></span>
    
<span data-ttu-id="0c749-p110">Чтобы протестировать форму, откройте ее, введите произвольный форматированный объект, например изображение, таблицу или форматированный текст. Нажмите кнопку **Отправить** на ленте, чтобы сохранить форматированное содержимое в файле out.xml на сервере. Нажмите кнопку **Запрос** на вкладке **Вид**, после чего нажмите кнопку **Выполнить запрос** в форме. В элементе управления **Форматированный текст** должно отобразиться содержимое XHTML из файла out.xml. Если в поле форматированного текста представлено несколько строк, веб-служба примет только первую строку, проигнорировав все остальные.</span><span class="sxs-lookup"><span data-stu-id="0c749-p110">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text. Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server. Click **Query** on the **View** tab, and then click the **Run Query** button on the form. The **Rich Text Box** control should display the XHTML content from the out.xml file. If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

