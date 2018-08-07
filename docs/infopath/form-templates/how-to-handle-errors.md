---
title: Обработка ошибок
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- ошибки [infopath 2007], обработка, InfoPath 2007, обработку ошибок, FormError [InfoPath 2007], [InfoPath 2007] обработки ошибок, FormErrorCollection [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: При создании настраиваемых приложений разработчики должны выполнять обработку ошибок, включающую написание программного кода на наличие ошибок, вызываемых приложения или для создания и обнаружения настраиваемых ошибок. Объектная модель InfoPath, автор Microsoft.Office.InfoPath пространство имен поддерживает обработку ошибок с помощью класса FormError в сочетании с классом FormErrorCollection.
ms.openlocfilehash: 3bfad103c31d0b5364d1c75acfbb2f590f7658bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807509"
---
# <a name="handle-errors"></a>Обработка ошибок

При создании настраиваемых приложений разработчики должны выполнять обработку ошибок, включающую написание программного кода на наличие ошибок, вызываемых приложения или для создания и обнаружения настраиваемых ошибок. Объектная модель InfoPath, автор [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) пространство имен поддерживает обработку ошибок с помощью класса [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) в сочетании с классом [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
  
Ниже перечислены причины, по которым в приложении InfoPath могут возникать ошибки.
  
- Введенным данным не удается пройти проверку на соответствие схеме XML.
    
- Неудачный результат проверки на соответствие пользовательским ограничениям.
    
- Когда ошибка создается с помощью метода [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) объекта события [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) . 
    
- Пользовательские ошибки создания с помощью метода [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) класса [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Обзор класса "FormErrorCollection"

Класс [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) , содержащихся в коллекции. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) (+ 3 перегрузки)  <br/> |Создает объект **FormError** и добавляет его в коллекцию.  <br/> |
|Метод [DELETE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) (+ 1 перегрузка)  <br/> |Удаляет указанную пользовательскую ошибку из коллекции.   <br/> |
|Метод [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx)  <br/> |Удаляет все объекты **FormError** из коллекции.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+ 1 перегрузка)  <br/> |Возвращает все объекты **FormError** с указанным именем или типом, находящиеся в коллекции.   <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)  <br/> |Возвращает количество объектов **FormError**, содержащихся в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)  <br/> |Возвращает ссылку на объект **FormError**, основываясь на указанном номере индекса.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Обзор класса "FormError"

Класс [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) предоставляет следующие свойства, которые могут использоваться разработчиками форм для доступа к сведениям о возникшей ошибке. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx)  <br/> |Возвращает или задает подробное сообщение об ошибке для объекта **FormError**.  <br/> |
|Свойство [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx)  <br/> |Возвращает или задает код ошибки для объекта **FormError**.  <br/> |
|Свойства [сайта](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Возвращает объект **XPathNavigator**, расположенном в узле, связанном с объектом **FormError**.  <br/> |
|Свойство [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx)  <br/> |Возвращает или задает краткое сообщение об ошибке для объекта **FormError**.  <br/> |
|Свойство [FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx)  <br/> |Возвращает тип объекта **FormError**.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Использование классов "FormErrorCollection" и "FormError"

Объекта **FormErrorCollection** , связанного с формой доступен через свойство [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) объекта [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Объект **FormErrorCollection** связан с XML-документом формы, чтобы при возникновении ошибки ее и любые другие сообщения об ошибках можно получить доступ и управлять в документе XML. Следующий пример показывает, как цикл может использоваться для проверки ошибок, которые могут существовать в XML-документом формы. При наличии ошибок, функция обрабатывает каждую из них и, с помощью свойства **сообщения** для объекта **FormError** отображает окно сообщения для пользователя. 
  
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

Предыдущая функцию можно вызвать из одного из обработчиков событий проверки данных формы. Например при использовании обработчика событий для события [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) поля в форме, вызов функции проходит аргумент узла XML, с помощью свойства [сайта](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) объекта [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) событий следующим образом. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

В дополнение к обработке ошибок, сгенерированными InfoPath, разработчики форм также можно создать пользовательских ошибок с помощью метода [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) объекта события [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) или с помощью [Добавить ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)метод класса [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . Для получения сведений об использовании методов [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) или [Добавить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) ссылки для этих методов в начале этого раздела. 
  
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

1. Откройте конструктор InfoPath и затем перейдите на вкладку **файл** . 
    
2. Щелкните **Параметры**, затем выберите **Параметры InfoPath** в категории **Общие**. 
    
3. На вкладке **Дополнительно** установите флажок **Уведомлять об ошибках кода Visual Basic и C#**. 
    

