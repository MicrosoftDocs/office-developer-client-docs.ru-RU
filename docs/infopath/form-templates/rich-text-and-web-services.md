---
title: Форматированный текст и веб-службы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath поддерживает присоединение элемента управления Форматированный текст в форме к элементу XML, полученному от веб-службы, с последующей отправкой данных из элемента управленияформатированный текстэлементу XML посредством веб-службы. Элемент должен соответствовать формату XHTML. Например, схема элемента с именем MyRichTextElement, содержащая форматированный текст, будет иметь следующее определение схемы XML:'
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299848"
---
# <a name="rich-text-and-web-services"></a>Форматированный текст и веб-службы

Microsoft InfoPath поддерживает присоединение элемента управления **Форматированный текст** в форме к элементу XML, полученному от веб-службы, с последующей отправкой данных из элемента управления "форматированный текст" элементу XML посредством веб-службы. Элемент должен соответствовать формату XHTML. Например, схема элемента с именем  `MyRichTextElement`, содержащая форматированный текст, будет иметь следующее определение схемы XML: 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

Перед присоединением элемента управления **Форматированный текст** к элементу XHTML последний должен быть помещен в узел-оболочку; этот узел-оболочка может принадлежать любому произвольному пространству имен. Он может иметь следующий вид: 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

В этой теме описан процесс создания веб-службы, способной отправлять и получать XHTML, а также процесс использования InfoPath для прикрепления параметров. Здесь не даются подробные инструкции по созданию веб-службы. Предполагается, что читающий уже имеет некоторый опыт работы с веб-службами.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Проектирование веб-службы для получения и отправки XHTML

Использованная в примере веб-служба хранит данные XHTML, которые она отправляет и получает в XML-файле, на сервере. Этот файл с именем out.xml выполняет функцию источника данных, в котором хранятся данные XHTML. Существует два метода, позволяющих клиентскому приложению взаимодействовать с источником данных,   `getXhtml` и  `setXhtml`. Метод  `getXhtml` веб-службы возвращает **XmlNode**, содержащий XHTML, который можно прикрепить к элементу управления "форматированный текст" InfoPath. Метод  `setXhtml` веб-службы получает **XmlNode** в качестве данных для хранения в файле out.xml. 
  
> [!NOTE]
> [!Примечание] Эти веб-методы требуют использования операторов **using**, ссылающихся на пространства имен **System.IO** и **System.Xml**. 
  
Метод  `getXhtml` пытается загрузить данные XML, возвращаемые из файла out.xml, в папку Data на диске C. Если это не удается, например, по причине отсутствия файла или отсутствия допустимого XML, метод возвращает пустой элемент HTML **DIV**, ссылающийся на пространство имен XHTML. 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "https://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "https://someNameSpace"); 
 
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
                tempDocument.LoadXml("<div xmlns=\"https://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

Метод  `setXhtml` веб-службы получает XHTML от элемента управления **Форматированный текст** формы InfoPath. Поскольку веб-службы не поддерживают список узлов при отправке веб-службе поля с форматированным текстом, содержащего несколько строк, веб-служба получает только первую строку и игнорирует все остальные. 
  
В образце метода  `setXhtml` предполагается, что он получает узел XML верхнего уровня, который в большинстве случаев помещен в оболочку элемента **DIV**. Если полученный XML не содержит элемент в оболочке, например если текст внутри элемента управления **Форматированный текст** не имеет форматирования, метод распознает это, проверяя, указывает ли свойство **NodeType** на то, что переданный XML является текстовым узлом. Если XML является текстовым узлом, метод создает элемент **DIV** и копирует содержимое текстового узла в **DIV**, чтобы элемент **DIV** содержал дочерний текстовый узел с текстом, отправленным веб-службе. Полученный методом XML записывается в файл out.xml в папке Data на диске C. 
  
> [!NOTE]
> [!Примечание] Пример метода  `setXhtml` написан для получения данных XHTML любого объема. В действительности рекомендуется выяснить объем отправляемых данных и установить предельный объем. 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>Создание формы InfoPath, обменивающейся данными с образцом веб-службы

Выполните следующие действия, чтобы создать форму для тестирования образца веб-службы.
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>Создание формы, подключающейся к образцу веб-службы

1. Откройте конструктор форм InfoPath.
    
2. На вкладке **Создать** щелкните дважды **Веб-служба** в разделе **Дополнительные шаблоны форм**.
    
3. В диалоговом окне **мастера подключения данных** выберите **Получить данные** и нажмите кнопку **Далее**.
    
4. Укажите адрес веб-службы, содержащей образец методов веб-служб, и нажмите кнопку **Далее**. 
    
5. Для метода получения выберите в качестве операции **getXhtml** и нажмите кнопку **Далее**.
    
6. Метод **getXHTML** веб-службы не имеет параметров, поэтому нажмите кнопку **Далее**.
    
7. Нажмите кнопку **Готово**.
    
8. На вкладке **Данные** в группе **Действия отправки** выберите **В другие расположения** и щелкните **Веб-служба**, чтобы использовать для отправки данных ту же веб-службу. 
    
9. Укажите адрес веб-службы, содержащей образец методов веб-служб, и нажмите кнопку **Далее**.
    
10. Для метода отправки выберите в качестве операции **setXhtml** и нажмите кнопку **Далее**.
    
11. Щелкните **Изменить**, последовательно разверните папки **dataFields**, **s0:getXhtmlResponse** и **getXhtmlResult** и выберите элемент **MyRichTextElement**, после чего нажмите кнопку **Далее**.
    
12. Нажмите кнопку **Готово**.
    
13. В области задач **Поля** разверните папку **dataFields**. 
    
14. Последовательно разверните папки **s0:getXhtmlResponse** и **getXhtmlResult** и перетащите элемент **MyRichTextElement** в форму. InfoPath определит, что элемент **MyRichTextElement** является элементом XHTML, и будет использовать для прикрепления к нему элемент управления "форматированный текст". 
    
15. Сохраните или опубликуйте форму.
    
Чтобы протестировать форму, откройте ее, введите произвольный форматированный объект, например изображение, таблицу или форматированный текст. Нажмите кнопку **Отправить** на ленте, чтобы сохранить форматированное содержимое в файле out.xml на сервере. Нажмите кнопку **Запрос** на вкладке **Вид**, после чего нажмите кнопку **Выполнить запрос** в форме. В элементе управления **Форматированный текст** должно отобразиться содержимое XHTML из файла out.xml. Если в поле форматированного текста представлено несколько строк, веб-служба примет только первую строку, проигнорировав все остальные. 
  

