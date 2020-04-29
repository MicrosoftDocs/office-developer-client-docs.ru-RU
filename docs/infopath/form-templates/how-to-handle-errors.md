---
title: Обработка ошибок
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- ошибки [InfoPath 2007], обработка, FormErrorCollection [InfoPath 2007], InfoPath 2007, обработка ошибок, FormError [InfoPath 2007], обработка ошибок [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: При создании пользовательских приложений разработчики часто выполняют обработку ошибок, которая предполагает написание программы для проверки на наличие ошибок, созданных приложением, или для создания и инициирования пользовательских ошибок. Объектная модель InfoPath, предоставляемая пространством имен Microsoft. Office. InfoPath, поддерживает обработку ошибок с помощью класса FormError в связи с классом FormErrorCollection.
ms.openlocfilehash: 30cf649188b7e4cbc35469d2a50540bb13ecb38d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410779"
---
# <a name="handle-errors"></a>Обработка ошибок

При создании пользовательских приложений разработчики часто выполняют обработку ошибок, которая предполагает написание программы для проверки на наличие ошибок, созданных приложением, или для создания и инициирования пользовательских ошибок. Объектная модель InfoPath, предоставляемая пространством имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , поддерживает обработку ошибок с помощью класса [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) в связи с классом [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
  
Ниже перечислены причины, по которым в приложении InfoPath могут возникать ошибки.
  
- Введенным данным не удается пройти проверку на соответствие схеме XML.
    
- Неудачный результат проверки на соответствие пользовательским ограничениям.
    
- При создании ошибки методом [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) объекта события [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) . 
    
- При создании пользовательской ошибки с помощью метода [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) класса [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Обзор класса "FormErrorCollection"

Класс [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) , содержащимися в коллекции. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) (+ 3 перегрузки)  <br/> |Создает объект **FormError** и добавляет его в коллекцию.  <br/> |
|Метод [Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) (+ 1 перегрузка)  <br/> |Удаляет указанную пользовательскую ошибку из коллекции.  <br/> |
|Метод [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx)  <br/> |Удаляет все объекты **FormError** из коллекции.  <br/> |
|[Возникли ошибки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+ 1 перегрузка)  <br/> |Возвращает все объекты **FormError** с указанным именем или типом, находящиеся в коллекции.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)  <br/> |Возвращает количество объектов **FormError**, содержащихся в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)  <br/> |Возвращает ссылку на объект **FormError**, основываясь на указанном номере индекса.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Обзор класса "FormError"

Класс [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) предоставляет следующие свойства, которые могут использоваться разработчиками форм для доступа к сведениям о произошедшей ошибке. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Свойство [детаиледмессаже](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx)  <br/> |Возвращает или задает подробное сообщение об ошибке для объекта **FormError**.  <br/> |
|Свойство [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx)  <br/> |Возвращает или задает код ошибки для объекта **FormError**.  <br/> |
|Свойство [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Возвращает объект **XPathNavigator**, расположенном в узле, связанном с объектом **FormError**.  <br/> |
|Свойство [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx)  <br/> |Возвращает или задает краткое сообщение об ошибке для объекта **FormError**.  <br/> |
|Свойство [FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx)  <br/> |Возвращает тип объекта **FormError**.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Использование классов "FormErrorCollection" и "FormError"

Доступ к объекту **FormErrorCollection** , связанному с формой, осуществляется через свойство [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) объекта [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Объект **FormErrorCollection** связан с базовым XML-документом формы, поэтому при возникновении ошибки можно получить доступ к этой и любым дополнительным ошибкам XML и управлять ими в текущем документе. В следующем примере демонстрируется использование цикла для поиска возможных ошибок в базовом XML-документе формы. Если ошибки присутствуют, то эта функция обрабатывает в цикле каждую из них и отображает пользователю окна сообщения с помощью свойства **Message** объекта **FormError**. 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

Предыдущую функцию можно вызвать из одного из обработчиков событий проверки данных в форме. Например, при использовании в обработчике событий для события [Change](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) поля в форме вызов функции передаст аргумент узла XML с помощью свойства [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) объекта события [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) следующим образом. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Кроме обработки ошибок, создаваемых InfoPath, разработчики форм могут также создавать настраиваемые ошибки с помощью метода [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) объекта события [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) или с помощью метода [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) класса [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . Для получения сведений об использовании методов [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) или [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) , щелкните ссылки этих методов в начале этой статьи. 
  
## <a name="handling-managed-code-exceptions"></a>Обработка исключений управляемого кода

Для обработки исключений, возникающих в шаблоне формы с управляемым кодом, можно воспользоваться методом "try-catch", как показано в следующем примере кода.
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

Если в коде формы не используется обработка исключений "try-catch", то при отладке и просмотре приложение InfoPath будет отображать сведения о необработанных исключениях в диалоговом окне ошибок InfoPath. Кроме того, по умолчанию необработанные исключения не отображаются в диалоговом окне InfoPath во время выполнения при развертывании шаблона формы с управляемым кодом. Чтобы отображать сведения о необработанных исключениях во время выполнения, воспользуйтесь приведенной ниже процедурой.
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Включение уведомлений для необработанных исключений управляемого кода во время выполнения

1. Откройте конструктор InfoPath и перейдите на вкладку **файл** . 
    
2. Щелкните **Параметры**, затем выберите **Параметры InfoPath** в категории **Общие**. 
    
3. На вкладке **Дополнительно** установите флажок **Уведомлять об ошибках кода Visual Basic и C#**. 
    

