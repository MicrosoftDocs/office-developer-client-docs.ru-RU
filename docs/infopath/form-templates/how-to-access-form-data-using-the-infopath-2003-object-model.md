---
title: Доступ к данным форм с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- интерфейс XDocument [infopath 2007], совместимых с InfoPath 2003 шаблонов форм, доступ к данным формы, интерфейс XDocumentsCollection [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Флажок расширить функциональность формы InfoPath, часто бывает необходимо программным способом доступа к сведениям о базовом документе XML формы, доступ к данным, который содержит XML-документа или выполнение некоторых действий с документом XML. Объектная модель InfoPath поддерживает доступ к и работа с XML-документом формы посредством использования интерфейса XDocument в сочетании с помощью интерфейса XDocumentsCollection.
ms.openlocfilehash: 24e9abc8ce7327ab94b3608f1279c0f0d381ea83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807490"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Доступ к данным форм с помощью объектной модели InfoPath 2003

Флажок расширить функциональность формы InfoPath, часто бывает необходимо программным способом доступа к сведениям о базовом документе XML формы, доступ к данным, который содержит XML-документа или выполнение некоторых действий с документом XML. Объектная модель InfoPath поддерживает доступ к и работа с XML-документом формы посредством использования интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) в сочетании с помощью интерфейса [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) . 
  
Интерфейс **XDocument** — это один из самых полезных типов в объектной модели InfoPath, так как он содержит различные свойства, методы и события, которые не только взаимодействия с базовым XML формы документов, но также выполнять множество действий, доступны в пользовательском интерфейсе InfoPath. В проекте управляемым кодом, созданных с помощью объектной модели совместимых с InfoPath 2003, переменной введите **XDocument** , который называется `thisXDocument` автоматически определяется в `_StartUp` метод класса, содержащего обработчики событий в коде формы проекта . Можно использовать `thisXDocument` переменной в форме кода для доступа к интерфейс **XDocument** и его элементы. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Обзор интерфейса XDocumentsCollection

Интерфейс **XDocumentsCollection** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами **XDocument**, содержащимися в семействе. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Закрывает указанную форму.  <br/> |
|Метод [New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx)  <br/> |Создает новую форму на основе существующей формы.  <br/> |
|Метод [NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx)  <br/> |Создает новую форму на основе существующего шаблона формы.  <br/> |
|Метод [NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Создает новую форму InfoPath с использованием указанных XML-данных и шаблона формы.   <br/> |
|Метод [Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx)  <br/> |Открывает указанную форму.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Возвращает количество объектов  **XDocument** в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **XDocument**.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Обзор интерфейса XDocument

Интерфейс **XDocument** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с базовым XML-документом формы и выполнения действий над ним. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Возвращает строковое значение указанной переменной данных.  <br/> |
|Метод [getDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Возвращает ссылку на модель XML DOM, связанную с указанным объектом **DataObject**.  <br/> |
|Метод [ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx)  <br/> |Импортирует (или объединяет) указанную форму в открытую в данный момент форму.  <br/> |
|Метод [printOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx)  <br/> |Распечатывает текущее представление формы.  <br/> |
|Метод [Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx)  <br/> |Возвращает данные из адаптера данных, связанного с формой.  <br/> |
|Метод [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Сохраняет открытую в данный момент форму.  <br/> |
|Метод [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)  <br/> |Сохраняет открытую в данный момент форму с указанным именем.  <br/> |
|Метод [SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Задает значение указанной переменной данных.  <br/> |
|Метод [Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx)  <br/> |Отправляет форму в соответствии с операцией отправки, указанной в режиме конструктора.  <br/> |
|Свойство [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx)  <br/> |Возвращает ссылку на семейство **DataObjects**.  <br/> |
|Свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Возвращает ссылку на модель XML DOM, заполненную исходными XML-данными формы.  <br/> |
|Свойство [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx)  <br/> |Возвращает ссылку на семейство **Errors**.  <br/> |
|Свойство [Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx)  <br/> |Возвращает ссылку на объект, представляющий все функции и переменные, содержащиеся в файле кода формы.  <br/> |
|Свойство [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx)  <br/> |Возвращает значение **Boolean**, указывающее факт изменения данных в форме.  <br/> |
|Свойство [IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx)  <br/> |Возвращает значение **Boolean**, указывающее наличие атрибута только для чтения у модели XML DOM.  <br/> |
|Свойство [IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx)  <br/> |Возвращает значение **Boolean**, указывающее факт сохранения формы после ее создания.  <br/> |
|Свойство [IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx)  <br/> |Возвращает значение **Boolean**, указывающее наличие режима формы только для чтения.  <br/> |
|Свойство [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx)  <br/> |Возвращает значение **Boolean**, указывающее наличие подписи для формы.  <br/> |
|Свойство [Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx)  <br/> |Указывает или возвращает строковое значение языка, используемого для формы.  <br/> |
|Свойство [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx)  <br/> |Возвращает ссылку на объект адаптера данных.  <br/> |
|Свойство [решения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx)  <br/> |Возвращает ссылку на объект **Solution**.  <br/> |
|Свойство [пользовательского интерфейса](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)  <br/> |Возвращает ссылку на объект **UI**.  <br/> |
|Свойство [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx)  <br/> |Возвращает строковое значение, содержащее URI-идентификатор формы.  <br/> |
|[Просмотр](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) свойств  <br/> |Возвращает ссылку на объект **View**.  <br/> |
|Свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx)  <br/> |Возвращает ссылку на семейство **ViewInfos**.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Использование семейства XDocuments и интерфейсов XDocument

Интерфейс **XDocumentsCollection** доступен через свойство [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . В проекте управляемым кодом, созданных с помощью объектной модели совместимых с InfoPath 2003, можно получить доступ к интерфейс **XDocumentsCollection** с помощью `thisApplication` переменной, которая создается в `_StartUp` метода проекта кода формы. Следующие строки кода создайте переменную, которая ссылается на интерфейс **XDocumentsCollection** текущего проекта. 
  
```cs
XDocumentsCollection xdocs;
xdocs = thisApplication.XDocuments;
// Write code here to work with the XDocumentsCollection.
```

```vb
Dim xdocs As XDocumentsCollection
xdocs = thisApplication.XDocuments
' Write code here to work with the XDocumentsCollection.
```

В проекте управляемым кодом, созданных с помощью объектной модели совместимых с InfoPath 2003, можно получить доступ к интерфейс **XDocument** с помощью `thisXDocument` переменной, которая создается в `StartUp` метода проекта кода формы. В следующей строке кода использует `thisXDocument` переменную для доступа к интерфейс **XDocument** текущего проекта для отображения URI текущей открытой формы в сообщения с оповещением. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Если интерфейс **XDocument** используется для доступа к базовому XML-документу формы, то доступ осуществляется к XML-документу, связанному с открытой в данный момент формой. 
  
Ключевые свойства интерфейса **XDocument** является свойство **DOM** . Данное свойство возвращает ссылку на модель XML DOM, заполненную исходными XML-данными формы. При использовании свойства **DOM** , можно использовать все свойства и методы, поддерживаемые DOM XML. Например следующий код использует свойство **xml** XML DOM для определения и отображения все содержимое XML-документом формы. 
  
```cs
string xmldoc;
xmldoc = thisXDocument.DOM.xml;
// Display xml.
thisXDocument.UI.Alert(xmldoc);
```

```vb
Dim xmldoc As String
xmldoc = thisXDocument.DOM.xml
' Display xml.
thisXDocument.UI.Alert(xmldoc)
```

> [!NOTE]
> Чтобы узнать больше о XML DOM и все свойства и методы, которые он поддерживает, см в пакете SDK MSXML. 
  

