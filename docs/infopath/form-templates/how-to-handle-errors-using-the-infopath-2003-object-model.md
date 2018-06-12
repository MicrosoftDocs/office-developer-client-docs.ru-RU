---
title: Обработка ошибок с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны форм с поддержкой веб-2003 InfoPath, обработки ошибок, совместимых с InfoPath 2003 шаблонов форм, обработки ошибок, шаблонов форм [InfoPath 2007], обработки ошибок, ошибок [InfoPath 2007], шаблонов форм совместимых с InfoPath 2003
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: При создании настраиваемых приложений разработчики должны выполнять обработку ошибок, включающую написание программного кода на наличие ошибок, вызываемых приложения или для создания и обнаружения настраиваемых ошибок. Объектная модель совместимых с InfoPath 2003 поддерживает обработку ошибок с помощью объекта ErrorObject в сочетании с семейства ErrorsCollection.
ms.openlocfilehash: 577e531d8943dc8fc3884cd81f68b11ca285c5d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807513"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Обработка ошибок с помощью объектной модели InfoPath 2003

При создании настраиваемых приложений разработчики должны выполнять обработку ошибок, включающую написание программного кода на наличие ошибок, вызываемых приложения или для создания и обнаружения настраиваемых ошибок. Объектная модель совместимых с InfoPath 2003 поддерживает обработку ошибок с помощью объекта [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) в сочетании с семейства [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
В приложении InfoPath могут возникать ошибки, когда данные, введенные в форму не удается выполнить проверку на соответствие схеме XML, при сбое ограничение нестандартной проверки, когда ошибка создается с помощью метода [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) объекта [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) или при создании ошибки с помощью метода [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) семейства [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
## <a name="overview-of-the-errorscollection-collection"></a>Обзор семейства ErrorsCollection

Семейство **ErrorsCollection** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами **ErrorObject** , содержащихся в коллекции. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)  <br/> |Создает объект **ErrorObject** и добавляет его в коллекцию.  <br/> |
|Метод [DELETE](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)  <br/> |Удаляет все объекты **ErrorObject** , связанные с указанным XML узлом и именем условия, за исключением пользовательских ошибок, добавленных с помощью метода **ReportError** .  <br/> |
|Метод [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx)  <br/> |Удаляет все объекты **ErrorObject** , содержащихся в коллекции.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)  <br/> |Возвращает количество объектов **ErrorObject** , содержащихся в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)  <br/> |Возвращает ссылку на объект **ErrorObject** , основываясь на указанном номере индекса.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Обзор объекта ErrorObject

Объект **ErrorObject** предоставляет следующие свойства, которые могут использоваться разработчиками форм для доступа к сведениям о возникшей ошибке. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx)  <br/> |Возвращает имя условия ошибки, или **значение null**, в зависимости от типа объекта **ErrorObject** .  <br/> |
|Свойство [DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx)  <br/> |Получает или задает подробное сообщение об ошибке для объекта **ErrorObject** .  <br/> |
|Свойство [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx)  <br/> |Получает или задает код ошибки для объекта **ErrorObject** .  <br/> |
|Свойство [узла](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx)  <br/> |Возвращает ссылку на узел XML, связанный с объектом **ErrorObject** .  <br/> |
|Свойство [ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx)  <br/> |Получает или задает краткое сообщение об ошибке для объекта **ErrorObject** .  <br/> |
|Свойство [ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx)  <br/> |Получает тип объекта **ErrorObject** .  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Использование ErrorsCollection и ErrorObject

Семейство **ErrorsCollection** доступен через свойство [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) объекта [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Семейство **ErrorsCollection** связан с XML-документом формы, что при возникновении ошибки, происходит в XML-документ. Следующий пример показывает, как цикла **foreach** Visual C# можно использовать для проверки ошибок, которые могут существовать в XML-документом формы. При наличии ошибок, функция обрабатывает каждую из них и, с помощью свойства **ShortErrorMessage** объекта **ErrorObject** отображает окно сообщения для пользователя. 
  
```cs
public void CheckErrors(IXMLDOMNode xmlNode)
{
   foreach(ErrorObject err in thisXDocument.Errors)
   {
      if(xmlNode==err.Node)
         thisXDocument.UI.Alert("The following error has occured: "
             + err.ShortErrorMessage + ".");
   }
}
```

Предыдущая функцию можно вызвать из одного из обработчиков событий проверки данных формы. Например при использовании в обработчике события [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) для поля в форме, вызов функции проходит аргумент узла XML, с помощью свойства [сайта](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) объекта [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) следующим образом. 
  
```cs
CheckErrors(e.Site);
```

В дополнение к обработке ошибок, сгенерированными InfoPath, разработчики форм также можно создать пользовательских ошибок с помощью метода **ReportError** объекта **DataDOMEventObject** или с помощью метода **Add** **ErrorsCollection** семейства сайтов. Для получения сведений об использовании методов **ReportError** или **Добавить** щелкните соответствующий метод в начале этого раздела. 
  
## <a name="handling-managed-code-exceptions"></a>Обработка исключений управляемого кода

Для обработки исключений, возникающих в шаблоне формы с управляемым кодом, можно воспользоваться методом "try-catch", как показано в следующем примере кода.
  
```cs
DataAdapters dataAdapters;
dataAdapters = thisXDocument.DataAdapters; 
XMLFileAdapterObject queryXMLFile = 
   (XMLFileAdapterObject)dataAdapters["form1"];
// Perform the query.
try
{
   queryXMLFile.Query();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to query.\n\n" + ex.Message);
}
// Perform the submit.
try
{
   queryXMLFile.Submit();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to submit.\n\n" + ex.Message);
}
```

Если в коде формы не используется обработка исключений "try-catch", то при отладке и просмотре приложение InfoPath будет отображать сведения о необработанных исключениях в диалоговом окне ошибок InfoPath.  
  

