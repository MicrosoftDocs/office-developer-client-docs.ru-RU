---
title: Доступ к данным форм с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- интерфейс XDocument [InfoPath 2007], шаблоны форм, совместимые с InfoPath 2003, доступ к данным форм, интерфейс XDocumentsCollection [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Если требуется расширить функциональность формы InfoPath, то зачастую требуется обеспечить программный доступ к сведениям о базовом XML-документе формы или к данным, содержащимся в этом XML-документе, а также выполнить некоторые действия над XML-документом. Объектная модель InfoPath поддерживает доступ к базовому XML-документу формы и управление им с помощью интерфейса XDocument в связи с интерфейсом XDocumentsCollection.
ms.openlocfilehash: 803122c6c377686a85f11cf48b76876c056f2ec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303677"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Доступ к данным форм с помощью объектной модели InfoPath 2003

Если требуется расширить функциональность формы InfoPath, то зачастую требуется обеспечить программный доступ к сведениям о базовом XML-документе формы или к данным, содержащимся в этом XML-документе, а также выполнить некоторые действия над XML-документом. Объектная модель InfoPath поддерживает доступ к базовому XML-документу формы и управление им с помощью интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) в связи с интерфейсом [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) . 
  
Интерфейс **XDocument** является одним из наиболее полезных в объектной модели InfoPath, поскольку предоставляет ряд свойств, методов и событий, которые не только взаимодействуют с базовым XML-документом формы, но и выполняют многие действия, доступные в интерфейсе пользователя InfoPath. В проекте с управляемым кодом, созданном с помощью объектной модели, совместимой с InfoPath 2003 **** , переменная типа XDocument `thisXDocument` автоматически определяется в `_StartUp` методе класса, содержащего обработчики событий в коде формы проекта. . Вы можете использовать `thisXDocument` переменную в коде формы, чтобы получить доступ к интерфейсу **XDocument** и его членам. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Обзор интерфейса XDocumentsCollection

Интерфейс **XDocumentsCollection** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами **XDocument**, содержащимися в семействе. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Закрывает указанную форму.  <br/> |
|Метод [New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx)  <br/> |Создает новую форму на основе существующей формы.  <br/> |
|Метод [NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx)  <br/> |Создает новую форму на основе существующего шаблона формы.  <br/> |
|Метод [невфромсолутионвисдата](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Создает новую форму InfoPath с использованием указанных XML-данных и шаблона формы.  <br/> |
|Метод [Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx)  <br/> |Открывает указанную форму.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Возвращает количество объектов  **XDocument** в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **XDocument**.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Обзор интерфейса XDocument

Интерфейс **XDocument** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с базовым XML-документом формы и выполнения действий над ним. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Возвращает строковое значение указанной переменной данных.  <br/> |
|Метод [GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Возвращает ссылку на модель XML DOM, связанную с указанным объектом **DataObject**.  <br/> |
|Метод [ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx)  <br/> |Импортирует (или объединяет) указанную форму в открытую в данный момент форму.  <br/> |
|Метод [PrintOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx)  <br/> |Распечатывает текущее представление формы.  <br/> |
|Метод [запроса](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx)  <br/> |Возвращает данные из адаптера данных, связанного с формой.  <br/> |
|Метод [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Сохраняет открытую в данный момент форму.  <br/> |
|Метод [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)  <br/> |Сохраняет открытую в данный момент форму с указанным именем.  <br/> |
|Метод [SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Задает значение указанной переменной данных.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx) Метод reоправить  <br/> |Отправляет форму в соответствии с операцией отправки, указанной в режиме конструктора.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) Свойство DataObjects  <br/> |Возвращает ссылку на семейство **DataObjects**.  <br/> |
|Свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Возвращает ссылку на модель XML DOM, заполненную исходными XML-данными формы.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx) Свойство Errors  <br/> |Возвращает ссылку на семейство **Errors**.  <br/> |
|Свойство [Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx)  <br/> |Возвращает ссылку на объект, представляющий все функции и переменные, содержащиеся в файле кода формы.  <br/> |
|Свойство [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx)  <br/> |Возвращает значение **Boolean**, указывающее факт изменения данных в форме.  <br/> |
|Свойство [исдомреадонли](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx)  <br/> |Возвращает значение **Boolean**, указывающее наличие атрибута только для чтения у модели XML DOM.  <br/> |
|Свойство [IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx)  <br/> |Возвращает значение **Boolean**, указывающее факт сохранения формы после ее создания.  <br/> |
|Свойство [IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx)  <br/> |Возвращает значение **Boolean**, указывающее наличие режима формы только для чтения.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) Свойство с подписью  <br/> |Возвращает значение **Boolean**, указывающее наличие подписи для формы.  <br/> |
|Свойство [Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx)  <br/> |Указывает или возвращает строковое значение языка, используемого для формы.  <br/> |
|Свойство [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx)  <br/> |Возвращает ссылку на объект адаптера данных.  <br/> |
|Свойство [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx)  <br/> |Возвращает ссылку на объект **Solution**.  <br/> |
|Свойство [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)  <br/> |Возвращает ссылку на объект **UI**.  <br/> |
|Свойство [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx)  <br/> |Возвращает строковое значение, содержащее URI-идентификатор формы.  <br/> |
|Свойство [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx)  <br/> |Возвращает ссылку на объект **View**.  <br/> |
|Свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx)  <br/> |Возвращает ссылку на семейство **ViewInfos**.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Использование семейства XDocuments и интерфейсов XDocument

Доступ к интерфейсу **XDocumentsCollection** осуществляется с помощью свойства [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . В проекте с управляемым кодом, созданном с помощью объектной модели, совместимой с InfoPath 2003 **** , можно получить доступ к `thisApplication` интерфейсу XDocumentsCollection с помощью переменной, `_StartUp` созданной в методе кода формы проекта. В следующих строках кода создается переменная, которая указывает на интерфейс **XDocumentsCollection** текущего проекта. 
  
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

В проекте с управляемым кодом, созданном с помощью объектной модели, совместимой с InfoPath 2003 **** , можно получить доступ к `thisXDocument` интерфейсу XDocument с помощью переменной, `StartUp` созданной в методе кода формы проекта. Следующая строка кода использует `thisXDocument` переменную для доступа к интерфейсу **XDocument** текущего проекта для отображения URI открытой в данный момент формы в оповещении. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Если интерфейс **XDocument** используется для доступа к базовому XML-документу формы, то доступ осуществляется к XML-документу, связанному с открытой в данный момент формой. 
  
Основным свойством интерфейса **XDocument** является свойство **DOM**. Это свойство возвращает ссылку на модель XML DOM, заполненную исходными XML-данными формы. При использовании свойства **DOM** можно применять все свойства и методы, которые поддерживаются моделью XML DOM. Например, следующий код использует свойство **XML** XML DOM для возврата и отображения всего содержимого базового XML-документа формы. 
  
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
> Чтобы узнать больше о XML DOM и всех поддерживаемых им свойствах и методах, ознакомьтесь с ПАКЕТом SDK для MSXML на сайте MSDN. 
  

