---
title: Добавление обработчика событий с помощью объектной модели InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- событие OnAfterImport [InfoPath 2007], событие OnAfterChange [InfoPath 2007], событие OnBeforeChange [InfoPath 2007], OnSubmitRequest событие [InfoPath 2007], событие OnVersionUpgrade [InfoPath 2007], шаблоны форм, совместимые с InfoPath 2003, обработчики событий, событие OnLoad [InfoPath 2007], обработчики событий [InfoPath 2007], добавление с помощью InfoPath 2003 объектная модель, reevent [InfoPath 2007], событие OnContextChange [InfoPath 2007], OnSaveRequest событие [InfoPath 2007], событие OnLoad [InfoPath 2007], OnSwitchView 2007 , Событие OnSign [InfoPath 2007], событие OnMergeRequest [InfoPath 2007]
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
# <a name="add-an-event-handler-using-the-infopath-object-model"></a><span data-ttu-id="452e2-104">Добавление обработчика событий с помощью объектной модели InfoPath</span><span class="sxs-lookup"><span data-stu-id="452e2-104">Add an event handler using the InfoPath object model</span></span>

<span data-ttu-id="452e2-105">Команды меню для добавления функций обработчика событий в проекте шаблона формы, совместимом с объектной моделью InfoPath 2003, аналогичны другим типам шаблонов форм.</span><span class="sxs-lookup"><span data-stu-id="452e2-105">The menu commands for adding event handler functions in a form template project that is compatible with the InfoPath 2003 object model are essentially the same as those for other types of form templates.</span></span> <span data-ttu-id="452e2-106">Например, чтобы добавить обработчик событий **OnLoad** с открытым шаблоном формы в конструкторе InfoPath, щелкните команду **при загрузке события** на вкладке **разработчик** . Фокус автоматически переключается на код формы обработчика событий **OnLoad** в редакторе кода Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="452e2-106">For example, in order to add an **OnLoad** event handler, with the form template open in the InfoPath designer, click the **On Load Event** command on the **Developer** tab. The focus automatically switches to the form code for the **OnLoad** event handler in the Visual Studio 2012 code editor.</span></span> 
  
<span data-ttu-id="452e2-107">В проектах шаблонов форм с управляемым кодом, совместимых с InfoPath 2003, класс, содержащий функции обработчиков событий и собственно обработчики событий, идентифицируется по относящимся к InfoPath атрибутам в модуле кода.</span><span class="sxs-lookup"><span data-stu-id="452e2-107">In managed-code form template projects compatible with InfoPath 2003, the class that contains event handler functions and the event handlers themselves are identified by attributes specific to InfoPath in the code module.</span></span>

## <a name="adding-event-handlers"></a><span data-ttu-id="452e2-108">Добавление обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="452e2-108">Adding event handlers</span></span>

<span data-ttu-id="452e2-109">Во всех следующих процедурах предполагается, что в Microsoft InfoPath открыт проект шаблона формы с помощью Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="452e2-109">All of the following procedures assume that you have a form template project open in Microsoft InfoPath with Visual Studio 2012.</span></span>
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a><span data-ttu-id="452e2-110">Добавление обработчика событий "OnClick" для кнопки</span><span class="sxs-lookup"><span data-stu-id="452e2-110">Add an event handler for the OnClick event of a command button</span></span>

1. <span data-ttu-id="452e2-111">Чтобы добавить кнопку в форму, в области **Элементы управления** щелкните элемент **Кнопка**.</span><span class="sxs-lookup"><span data-stu-id="452e2-111">In the **Controls** pane, click **Button** to add a button to the form.</span></span> 
    
2. <span data-ttu-id="452e2-112">На вкладке  **Свойства** щелкните  **Пользовательский код**.</span><span class="sxs-lookup"><span data-stu-id="452e2-112">On the **Properties** tab, click **Custom Code**.</span></span>
    
   <span data-ttu-id="452e2-113">Фокус переключится на заглушку обработчика событий для события [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) в редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="452e2-113">The focus switches to the stub for the event handler for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a><span data-ttu-id="452e2-114">Добавление обработчика событий "OnBeforeChange", "OnValidate" или "OnAfterChange" для поля или группы</span><span class="sxs-lookup"><span data-stu-id="452e2-114">Add an event handler for the OnBeforeChange, OnValidate, or OnAfterChange event of a field or group</span></span>

1. <span data-ttu-id="452e2-115">Щелкните правой кнопкой мыши элемент управления ввода данных, связанный с полем или группой, например элемент управления **Текстовое поле**.</span><span class="sxs-lookup"><span data-stu-id="452e2-115">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
2. <span data-ttu-id="452e2-116">Наведите указатель на пункт **Программирование** и щелкните одну из команд, например, **Событие OnValidate**.</span><span class="sxs-lookup"><span data-stu-id="452e2-116">Point to **Programming**, and then click one of the commands, such as **On Validate Event**.</span></span>
    
   <span data-ttu-id="452e2-117">Фокус переключится на заглушку обработчика событий для одного из следующих событий в редакторе кода: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [onvalidateий](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)или [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span><span class="sxs-lookup"><span data-stu-id="452e2-117">The focus switches to the stub for the event handler for one of the following events in the code editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx), or [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a><span data-ttu-id="452e2-118">Добавление обработчика событий "OnLoad", "OnSwitchView", "OnContextChange" или "OnSign" для формы</span><span class="sxs-lookup"><span data-stu-id="452e2-118">Add an event handler for the OnLoad, OnSwitchView, OnContextChange, or OnSign event of a form</span></span>

- <span data-ttu-id="452e2-119">В меню **Сервис** выберите пункт **Программирование** и щелкните событие формы, для которого требуется написать обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="452e2-119">On the **Tools** menu, point to **Programming**, and then click the form event that you want to write an event handler for.</span></span>
    
    <span data-ttu-id="452e2-120">Фокус переключится на заглушку обработчика событий для одного из следующих элементов в редакторе кода: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)или [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span><span class="sxs-lookup"><span data-stu-id="452e2-120">The focus switches to the stub for the event handler for one of the following in the code editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx), or [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a><span data-ttu-id="452e2-121">Добавление обработчика событий "OnSubmitRequest" для формы</span><span class="sxs-lookup"><span data-stu-id="452e2-121">Add an event handler for the OnSubmitRequest event of a form</span></span>

1. <span data-ttu-id="452e2-122">На вкладке **Данные** щелкните **Параметры отправки**.</span><span class="sxs-lookup"><span data-stu-id="452e2-122">On the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="452e2-123">Установите флажок **Разрешить пользователям отправлять эту форму** и щелкните **Выполнить пользовательское действие с использованием кода**.</span><span class="sxs-lookup"><span data-stu-id="452e2-123">Select the **Allow users to submit this form** check box, and then click **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="452e2-124">Нажмите кнопку **Редактировать код**, а затем кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="452e2-124">Click **Edit Code**, and then click **OK**.</span></span>
    
   <span data-ttu-id="452e2-125">Фокус переключится на заглушку обработчика событий для события [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) в редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="452e2-125">The focus switches to the stub for the event handler for the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a><span data-ttu-id="452e2-126">Добавление обработчика событий "OnSaveRequest" для формы</span><span class="sxs-lookup"><span data-stu-id="452e2-126">Add an event handler for the OnSaveRequest event of a form</span></span>

1. <span data-ttu-id="452e2-127">Перейдите на вкладку **Файл** и нажмите кнопку **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="452e2-127">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="452e2-128">В категории **Сохранение** последовательно щелкните пункты **Сохранить с использованием пользовательского кода**, **Изменить** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="452e2-128">In the **Save** category, click **Save using custom code**, click **Edit**, and then click **OK**.</span></span>
    
   <span data-ttu-id="452e2-129">Фокус переключится на заглушку обработчика событий для события [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) в редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="452e2-129">The focus switches to the stub for the event handler for the [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a><span data-ttu-id="452e2-130">Добавление обработчика событий "OnVersionUpgrade" для формы</span><span class="sxs-lookup"><span data-stu-id="452e2-130">Add an event handler for the OnVersionUpgrade event of a form</span></span>

1. <span data-ttu-id="452e2-131">На вкладке **Файл** выберите пункт **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="452e2-131">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="452e2-132">В категории **Управление версиями** выберите **Использовать специальное событие** из списка **Обновить существующие формы**, щелкните **Изменить**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="452e2-132">In the **Versioning** category, select **Use custom event** from the **Update existing forms** list, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="452e2-133">Фокус переключится на заглушку обработчика событий для события [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) в редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="452e2-133">The focus switches to the stub for the event handler for the [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a><span data-ttu-id="452e2-134">Добавление обработчика событий "OnMergeRequest" для формы</span><span class="sxs-lookup"><span data-stu-id="452e2-134">Add an event handler for the OnMergeRequest event of a form</span></span>

1. <span data-ttu-id="452e2-135">На вкладке **Файл** выберите пункт **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="452e2-135">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="452e2-136">В категории **Дополнительно** установите флажки **Разрешить объединение форм** и **Объединить с использованием пользовательского кода** и щелкните **Изменить** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="452e2-136">In the **Advanced** category, select the **Enable Form merging** and the **Merge using custom code** check boxes, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="452e2-137">Фокус переключится на заглушку обработчика событий для события [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) в редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="452e2-137">The focus switches to the stub for the event handler for the [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) event in the code editor.</span></span> 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a><span data-ttu-id="452e2-138">Добавление обработчика событий для события OnAfterImport</span><span class="sxs-lookup"><span data-stu-id="452e2-138">Adding an event handler for the OnAfterImport event</span></span>

<span data-ttu-id="452e2-139">Чтобы добавить обработчики событий для события [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , необходимо открыть код формы для шаблона формы с управляемым кодом и добавить функцию обработчика событий вручную.</span><span class="sxs-lookup"><span data-stu-id="452e2-139">To add event handlers for the [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) event, you must open the form code for your managed-code form template and add the event handler function manually.</span></span> <span data-ttu-id="452e2-140">Для получения сведений о способах написания обработчика для этого события щелкните ссылку для события **OnAfterImport**.</span><span class="sxs-lookup"><span data-stu-id="452e2-140">For information on how to write an event handler for this event, click the link for the **OnAfterImport** event.</span></span> 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a><span data-ttu-id="452e2-141">Добавление обработчика событий для дополнительного источника данных</span><span class="sxs-lookup"><span data-stu-id="452e2-141">Adding an event handler for a secondary data source</span></span>

<span data-ttu-id="452e2-p103">Способы добавления обработчика событий для дополнительного источника данных продемонстрированы в приведенном далее примере. В этом примере предполагается наличие дополнительного источника данных из файла ресурсов books.xml, использующего следующую схему:</span><span class="sxs-lookup"><span data-stu-id="452e2-p103">The following example shows how to add an event handler for a secondary data source. The example assumes a secondary data source from a resource file named books.xml, which has the following schema:</span></span>
  
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

<span data-ttu-id="452e2-144">Представление формы строится на основе этого источника данных.</span><span class="sxs-lookup"><span data-stu-id="452e2-144">The form's view is built from this data source.</span></span> <span data-ttu-id="452e2-145">Код формы создает хэш-таблицу, включающую список авторов и количество написанных ими книг.</span><span class="sxs-lookup"><span data-stu-id="452e2-145">The form code creates a hash table based on the authors and the number of books they have written.</span></span> <span data-ttu-id="452e2-146">Можно обновить записи таблицы, отображаемой в представлении, после чего обработчик событий **OnAfterChange** обновит хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="452e2-146">You can update an entry from the table shown in the view and the **OnAfterChange** event handler updates the hash table.</span></span> <span data-ttu-id="452e2-147">Обратите внимание, что свойство [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) атрибута **инфопасевенсандлер** (реализуемого классом [инфопасевенсандлераттрибуте](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) используется для ссылки на дополнительный источник данных.</span><span class="sxs-lookup"><span data-stu-id="452e2-147">Note that the [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) property of the **InfoPathEventHandler** attribute (which is implemented by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is used to reference the secondary data source.</span></span> 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a><span data-ttu-id="452e2-148">Способ идентификации класса, содержащего обработчики событий</span><span class="sxs-lookup"><span data-stu-id="452e2-148">How the class that contains event handlers is identified</span></span>

<span data-ttu-id="452e2-149">При создании нового проекта шаблона формы InfoPath, совместимого с объектной моделью управляемого кода InfoPath 2003, к классу, расположенному в начале модуля кода формы, добавляется атрибут уровня сборки **System.ComponentModel.Description**, позволяющий идентифицировать класс, содержащий все обработчики событий для шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="452e2-149">When you create a new InfoPath form template project that is compatible with the InfoPath 2003 managed code object model, an assembly-level **System.ComponentModel.Description** attribute is applied to the class at the beginning of the form code module to identify the class that contains all event handlers for the form template.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="452e2-150">Не изменяйте атрибут **System.ComponentModel.Description** в этом классе.</span><span class="sxs-lookup"><span data-stu-id="452e2-150">Do not modify the **System.ComponentModel.Description** attribute in this class.</span></span> <span data-ttu-id="452e2-151">При его изменении шаблон формы не сможет идентифицировать расположение обработчиков событий, и обработчики событий не запустятся.</span><span class="sxs-lookup"><span data-stu-id="452e2-151">If you do so, your form template will not be able to identify where event handlers are located, and the event handlers will fail to run.</span></span> 
  
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

## <a name="how-event-handlers-are-identified"></a><span data-ttu-id="452e2-152">Идентификация обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="452e2-152">How event handlers are identified</span></span>

<span data-ttu-id="452e2-153">Когда новый обработчик событий добавляется с помощью команд меню или кнопок пользовательского интерфейса в режиме конструктора InfoPath, в форму записывается заглушка для функции обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="452e2-153">When you add a new event handler using menu commands or buttons in the InfoPath design mode user interface, the stub for the event handler function is written into the form.</span></span> <span data-ttu-id="452e2-154">В следующем примере показан обработчик событий заглушки, созданный для элемента OnValidate [, добавленного](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) для поля с именем "Total".</span><span class="sxs-lookup"><span data-stu-id="452e2-154">The following example shows the stub event handler created for an [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) added for a field named 'total'.</span></span> 
  
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

<span data-ttu-id="452e2-155">Затем можно добавить код, который вызывает членов объектной модели InfoPath с помощью закрытых кэшированных `thisXDocument` членов или `thisApplication` переменных, или используя элементы, к которым получен доступ из `e` объекта **EventArgs** , полученного обработчиком событий:</span><span class="sxs-lookup"><span data-stu-id="452e2-155">You can then add code that invokes members of the InfoPath object model using the private cached members of the  `thisXDocument` or  `thisApplication` variables, or by using the members accessed from the  `e` **EventArgs** object received by the event handler:</span></span> 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

<span data-ttu-id="452e2-156">Атрибут **инфопасевенсандлер** (как определено классом [инфопасевенсандлераттрибуте](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) является настраиваемым атрибутом для функций, которые будут использоваться в качестве обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="452e2-156">The **InfoPathEventHandler** attribute (as defined by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is the custom attribute for functions that will be used as event handlers.</span></span> 
  
<span data-ttu-id="452e2-157">Если это необходимо для события, параметр **матчпас** (как определено свойством [матчпас](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) класса **инфопасевенсандлераттрибуте** ) указывает выражение XPath, которое определяет источник события.</span><span class="sxs-lookup"><span data-stu-id="452e2-157">When required by the event, the **MatchPath** parameter (as defined by the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies an XPath expression that identifies the event source.</span></span> <span data-ttu-id="452e2-158">Параметр **EventType** (как определено свойством [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) класса **инфопасевенсандлераттрибуте** ) указывает тип события.</span><span class="sxs-lookup"><span data-stu-id="452e2-158">The **EventType** parameter (as defined by the [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies the type of event.</span></span> <span data-ttu-id="452e2-159">Не следует менять значения этих параметров.</span><span class="sxs-lookup"><span data-stu-id="452e2-159">You should not change the values of these parameters.</span></span> <span data-ttu-id="452e2-160">Изменение этих значений может привести к неправильной компиляции обработчика событий или к отсутствию ожидаемого уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="452e2-160">If the values of these parameters are changed, the event handler may not compile correctly, or event notification will not occur as expected.</span></span> 
  
## <a name="obfuscating-code-in-event-handlers"></a><span data-ttu-id="452e2-161">Код маскировки в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="452e2-161">Obfuscating code in event handlers</span></span>

<span data-ttu-id="452e2-162">Если запустить служебную программу запутывания для сборки, которая создается при компиляции шаблона формы с управляемым кодом ( *имяПроекта* . dll), InfoPath не сможет загрузить сборку, когда пользователь откроет форму.</span><span class="sxs-lookup"><span data-stu-id="452e2-162">If you run an obfuscator utility on the assembly that is generated when a managed-code form template is compiled ( *projectname*  .dll), InfoPath will not be able to load the assembly when a user opens the form.</span></span> <span data-ttu-id="452e2-163">Если требуется скрыть код обработчиков событий или другой код формы, следует поместить код, который требуется скрыть, в отдельную сборку и указать в проекте ссылку на эту сборку, а затем вызвать элементы связанной сборки из файла FormCode.cs или FormCode.vb.</span><span class="sxs-lookup"><span data-stu-id="452e2-163">If you want to obfuscate the code for your event handlers or other form code, you must put the code that you want to obfuscate in a separate assembly, and reference that assembly in your project, and then call members of the referenced assembly from FormCode.cs or FormCode.vb.</span></span> <span data-ttu-id="452e2-164">Очень важно запускать средство скрытия кода только для отдельной сборки, связанной с проектом посредством ссылки.</span><span class="sxs-lookup"><span data-stu-id="452e2-164">It is important that you run the obfuscator utility only on the referenced assembly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="452e2-165">См. также</span><span class="sxs-lookup"><span data-stu-id="452e2-165">See also</span></span>

- [<span data-ttu-id="452e2-166">Реагирование на события формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="452e2-166">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

