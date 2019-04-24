---
title: Добавление обработчика событий с помощью объектной модели InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- событие OnAfterImport [InfoPath 2007], событие OnAfterChange [InfoPath 2007], событие OnBeforeChange [InfoPath 2007], OnSubmitRequest событие [InfoPath 2007], событие OnVersionUpgrade [InfoPath 2007], шаблоны форм, совместимые с InfoPath 2003,, обработчики событий событие onload [infopath 2007], обработчики событий [infopath 2007], добавление с помощью объектной модели infopath 2003, событие reload [InfoPath 2007], событие OnContextChange [InfoPath 2007], событие OnSaveRequest [infopath 2007], событие onload [infopath 2007], Событие OnSwitchView [InfoPath 2007], событие onSign [InfoPath 2007], событие OnMergeRequest [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Команды меню для добавления функций обработчика событий в проекте шаблона формы, совместимом с объектной моделью InfoPath 2003, аналогичны другим типам шаблонов форм.
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303670"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Добавление обработчика событий с помощью объектной модели InfoPath

Команды меню для добавления функций обработчика событий в проекте шаблона формы, совместимом с объектной моделью InfoPath 2003, аналогичны другим типам шаблонов форм. Например, чтобы добавить обработчик событий OnLoad **** с открытым шаблоном формы в конструкторе InfoPath, щелкните команду **при загрузке события** на вкладке **разработчик** . Фокус автоматически переключается на код формы обработчика **** событий OnLoad в редакторе кода Visual Studio 2012. 
  
В проектах шаблонов форм с управляемым кодом, совместимых с InfoPath 2003, класс, содержащий функции обработчиков событий и собственно обработчики событий, идентифицируется по относящимся к InfoPath атрибутам в модуле кода.

## <a name="adding-event-handlers"></a>Добавление обработчиков событий

Во всех следующих процедурах предполагается, что в Microsoft InfoPath открыт проект шаблона формы с помощью Visual Studio 2012.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Добавление обработчика событий "OnClick" для кнопки

1. Чтобы добавить кнопку в форму, в области **Элементы управления** щелкните элемент **Кнопка**. 
    
2. На вкладке  **Свойства** щелкните  **Пользовательский код**.
    
   Фокус переключится на заглушку обработчика событий для события [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) в редакторе кода. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Добавление обработчика событий "OnBeforeChange", "OnValidate" или "OnAfterChange" для поля или группы

1. Щелкните правой кнопкой мыши элемент управления ввода данных, связанный с полем или группой, например элемент управления **Текстовое поле**. 
    
2. Наведите указатель на пункт **Программирование** и щелкните одну из команд, например, **Событие OnValidate**.
    
   Фокус переключится на заглушку обработчика событий для одного из следующих событий в редакторе кода: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), onvalidateий [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)или [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Добавление обработчика событий "OnLoad", "OnSwitchView", "OnContextChange" или "OnSign" для формы

- В меню **Сервис** выберите пункт **Программирование** и щелкните событие формы, для которого требуется написать обработчик событий.
    
    Фокус переключится на заглушку обработчика событий для одного из следующих элементов в редакторе кода: OnLoad [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)или OnLoad. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Добавление обработчика событий "OnSubmitRequest" для формы

1. На вкладке **Данные** щелкните **Параметры отправки**.
    
2. Установите флажок **Разрешить пользователям отправлять эту форму** и щелкните **Выполнить пользовательское действие с использованием кода**.
    
3. Нажмите кнопку **Редактировать код**, а затем кнопку **ОК**.
    
   Фокус переключится на заглушку обработчика событий для события [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) в редакторе кода. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Добавление обработчика событий "OnSaveRequest" для формы

1. Перейдите на вкладку **Файл** и нажмите кнопку **Параметры формы**.
    
2. В категории **Сохранение** последовательно щелкните пункты **Сохранить с использованием пользовательского кода**, **Изменить** и нажмите кнопку **ОК**.
    
   Фокус переключится на заглушку обработчика событий для события [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) в редакторе кода. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Добавление обработчика событий "OnVersionUpgrade" для формы

1. На вкладке **Файл** выберите пункт **Параметры формы**.
    
2. В категории **Управление версиями** выберите **Использовать специальное событие** из списка **Обновить существующие формы**, щелкните **Изменить**, а затем нажмите кнопку **ОК**.
    
    Фокус переключится на заглушку обработчика событий для события [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) в редакторе кода. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Добавление обработчика событий "OnMergeRequest" для формы

1. На вкладке **Файл** выберите пункт **Параметры формы**.
    
2. В категории **Дополнительно** установите флажки **Разрешить объединение форм** и **Объединить с использованием пользовательского кода** и щелкните **Изменить** и нажмите кнопку **ОК**.
    
    Фокус переключится на заглушку обработчика событий для события [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) в редакторе кода. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Добавление обработчика событий для события OnAfterImport

Чтобы добавить обработчики событий для события [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , необходимо открыть код формы для шаблона формы с управляемым кодом и добавить функцию обработчика событий вручную. Для получения сведений о способах написания обработчика для этого события щелкните ссылку для события **OnAfterImport**. 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Добавление обработчика событий для дополнительного источника данных

Способы добавления обработчика событий для дополнительного источника данных продемонстрированы в приведенном далее примере. В этом примере предполагается наличие дополнительного источника данных из файла ресурсов books.xml, использующего следующую схему:
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema">
    <xsd:element name="catalog">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element ref="book" minOccurs="0" maxOccurs="unbounded"></xsd:element>
            </xsd:sequence>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="genre" type="xsd:string"></xsd:element>
    <xsd:element name="author" type="xsd:string"></xsd:element>
    <xsd:element name="book">
        <xsd:complexType>
            <xsd:all>
                <xsd:element ref="author" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="title" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="genre" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="price" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="publish_date" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="description" minOccurs="0" maxOccurs="1"></xsd:element>
            </xsd:all>
            <xsd:attribute ref="id"></xsd:attribute>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="price" type="xsd:string"></xsd:element>
    <xsd:element name="title" type="xsd:string"></xsd:element>
    <xsd:element name="publish_date" type="xsd:string"></xsd:element>
    <xsd:element name="description" type="xsd:string"></xsd:element>
    <xsd:attribute name="id" type="xsd:string"></xsd:attribute>
</xsd:schema>

```

<br/>

Представление формы строится на основе этого источника данных. Код формы создает хэш-таблицу, включающую список авторов и количество написанных ими книг. Можно обновить записи таблицы, отображаемой в представлении, после чего обработчик событий **OnAfterChange** обновит хэш-таблицу. Обратите внимание, что свойство [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) атрибута **инфопасевенсандлер** (реализуемого классом [инфопасевенсандлераттрибуте](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) используется для ссылки на дополнительный источник данных. 
  
```cs
namespace AuxDom
{
    // InfoPathNamespace attribute goes here.
    public class AuxDom
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        private Hashtable authors;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            authors = new Hashtable();
        }
        public void _Shutdown()
        {
            authors.Clear();
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
        public void OnLoad(DocReturnEvent e)
        {
            IXMLDOMDocument books = thisXDocument.GetDOM("books");
            DOMNodeList externalAuthors = books.selectNodes("/catalog/book/author");
            foreach (IXMLDOMNode authorNode in externalAuthors)
            {
                AddBookFromAuthor(authorNode.text);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="/catalog/book/author", EventType=InfoPathEventType.OnAfterChange, DataObject="books")]
        public void books__author_OnAfterChange(DataDOMEvent e)
        {
            if (e.IsUndoRedo)
            {
                // An undo or redo operation has occurred and the DOM 
                // is read-only.
                return;
            }
            
            if (e.Source.text != e.NewValue.ToString())
            {
                RemoveBookFromAuthor(e.OldValue.ToString());
                AddBookFromAuthor(e.NewValue.ToString());
            }
        }
        private void AddBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] + 1;
            }
            else
            {
                authors.Add(authorName, 1);
            }
        }
        private void RemoveBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] - 1;
            }
            if ((int)authors[authorName] == 0)
            {
                authors.Remove(authorName);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="ShowAuthors", EventType=InfoPathEventType.OnClick)]
        public void ShowAuthors_OnClick(DocActionEvent e)
        {
            // Write your code here.
            StringBuilder report = new StringBuilder();
            foreach (string authorName in authors.Keys)
            {
                report.Append(authorName + ",\t\t\t");
                report.Append(authors[authorName] + "\n");
            }
            thisXDocument.UI.Alert(report.ToString());
        }
    }
}

```

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Способ идентификации класса, содержащего обработчики событий

При создании нового проекта шаблона формы InfoPath, совместимого с объектной моделью управляемого кода InfoPath 2003, к классу, расположенному в начале модуля кода формы, добавляется атрибут уровня сборки **System.ComponentModel.Description**, позволяющий идентифицировать класс, содержащий все обработчики событий для шаблона формы. 
  
> [!IMPORTANT]
> Не изменяйте атрибут **System.ComponentModel.Description** в этом классе. При его изменении шаблон формы не сможет идентифицировать расположение обработчиков событий, и обработчики событий не запустятся. 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the // form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute(    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
' Office integration attribute. Identifies the startup class for the form. Do not modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
```

## <a name="how-event-handlers-are-identified"></a>Идентификация обработчиков событий

Когда новый обработчик событий добавляется с помощью команд меню или кнопок пользовательского интерфейса в режиме конструктора InfoPath, в форму записывается заглушка для функции обработчика событий. В следующем примере показан обработчик событий заглушки, созданный для [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) элемента OnValidate, добавленного для поля с именем "Total". 
  
```cs
[InfoPathEventHandler(MatchPath="/invoice/total", EventType=InfoPathEventType.OnValidate)]
public void total_OnValidate(DataDOMEvent e)
{
    // Write your code here.
}

```

```vb
<InfoPathEventHandler(MatchPath:="/invoice/total",EventType:= OnValidate)> Public Sub total_OnValidate(ByVal e As EventArgs)
    ' Write your code here.
End Sub

```

Затем можно добавить код, который вызывает членов объектной модели InfoPath с помощью закрытых кэшированных `thisXDocument` членов или `thisApplication` переменных, или используя элементы, к которым получен доступ из `e` объекта **EventArgs** , полученного обработчиком событий: 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

Атрибут **инфопасевенсандлер** (как определено классом [инфопасевенсандлераттрибуте](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) является настраиваемым атрибутом для функций, которые будут использоваться в качестве обработчиков событий. 
  
Если это необходимо для события, параметр **матчпас** (как определено свойством [матчпас](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) класса **инфопасевенсандлераттрибуте** ) указывает выражение XPath, которое определяет источник события. Параметр **EventType** (как определено свойством [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) класса **инфопасевенсандлераттрибуте** ) указывает тип события. Не следует менять значения этих параметров. Изменение этих значений может привести к неправильной компиляции обработчика событий или к отсутствию ожидаемого уведомления о событии. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Код маскировки в обработчиках событий

Если запустить служебную программу запутывания для сборки, которая создается при компиляции шаблона формы с управляемым кодом ( *имяПроекта* . dll), InfoPath не сможет загрузить сборку, когда пользователь откроет форму. Если требуется скрыть код обработчиков событий или другой код формы, следует поместить код, который требуется скрыть, в отдельную сборку и указать в проекте ссылку на эту сборку, а затем вызвать элементы связанной сборки из файла FormCode.cs или FormCode.vb. Очень важно запускать средство скрытия кода только для отдельной сборки, связанной с проектом посредством ссылки. 
  
## <a name="see-also"></a>См. также

- [Реагирование на события формы с помощью объектной модели InfoPath 2003](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

