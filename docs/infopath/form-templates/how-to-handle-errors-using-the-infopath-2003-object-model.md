---
title: Обработка ошибок с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, handling errors, InfoPath 2003-compatible form templates, error handling,form templates [InfoPath 2007], error handling,error handling [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: При создании пользовательских приложений разработчики часто выполняют обработку ошибок, которая предполагает написание программы для проверки на наличие ошибок, созданных приложением, или для создания и инициирования пользовательских ошибок. Объектная модель, совместимая с InfoPath 2003, поддерживает обработку ошибок с помощью объекта ErrorObject в связи с коллекцией ErrorsCollection.
ms.openlocfilehash: 93991e33d8867f89454bec08b41ba83e98ab0a17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439480"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Обработка ошибок с помощью объектной модели InfoPath 2003

При создании пользовательских приложений разработчики часто выполняют обработку ошибок, которая предполагает написание программы для проверки на наличие ошибок, созданных приложением, или для создания и инициирования пользовательских ошибок. Объектная модель, совместимая с InfoPath 2003, поддерживает обработку ошибок с помощью объекта [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) в связи с коллекцией [ErrorsCollection.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) 
  
В InfoPath могут возникать ошибки, когда данные, вступив в форму, не удается проверка схемы XML, при сбое настраиваемого ограничения проверки, когда ошибка создается методом [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) объекта [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) или когда ошибка создается с помощью метода [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) коллекции [ErrorsCollection.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) 
  
## <a name="overview-of-the-errorscollection-collection"></a>Обзор семейства ErrorsCollection

Семейство **ErrorsCollection** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами **ErrorObject**, содержащимися в семействе. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)  <br/> |Создает объект **ErrorObject** и добавляет его в семейство.  <br/> |
|Метод [Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)  <br/> |Удаляет все объекты **ErrorObject**, связанные с указанным XML-узлом и именем условия, за исключением пользовательских ошибок, добавленных с помощью метода **ReportError**.  <br/> |
|[Метод DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx)  <br/> |Удаляет все объекты **ErrorObject** из семейства.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)  <br/> |Возвращает количество объектов **ErrorObject**, содержащихся в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)  <br/> |Возвращает ссылку на объект **ErrorObject**, основываясь на указанном номере индекса.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Обзор объекта ErrorObject

Объект **ErrorObject** предоставляет следующие свойства, которые могут использоваться разработчиками форм для доступа к сведениям о возникшей ошибке. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Свойство ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx)  <br/> |Возвращает имя условия ошибки или **null**, в зависимости от типа объекта **ErrorObject**.  <br/> |
|[Свойство DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx)  <br/> |Возвращает или задает подробное сообщение об ошибке для объекта **ErrorObject**.  <br/> |
|[Свойство ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx)  <br/> |Возвращает или задает код ошибки для объекта **ErrorObject**.  <br/> |
|[Свойство Node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx)  <br/> |Возвращает ссылку на XML-узел, связанный с объектом **ErrorObject**.  <br/> |
|[Свойство ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx)  <br/> |Возвращает или задает краткое сообщение об ошибке для объекта **ErrorObject**.  <br/> |
|[Свойство ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx)  <br/> |Возвращает тип объекта **ErrorObject**.  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Использование ErrorsCollection и ErrorObject

Коллекция **ErrorsCollection** имеет доступ к свойству [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) объекта [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) Семейство **ErrorsCollection** связано с базовым XML-документом формы, поэтому когда возникает ошибка, она возникает в XML-документе. В следующем примере демонстрируется использование цикла Visual C# **foreach** для проверки ошибок, которые могут присутствовать в базовом XML-документе формы. При наличии ошибок функция обрабатывает в цикле каждую из них и с помощью свойства **ShortErrorMessage** объекта **ErrorObject** отображает пользователю окно сообщения. 
  
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

Предыдущую функцию можно вызвать из одного из обработчиков событий проверки данных в форме. Например, при использовании в обработнике событий [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) для поля в форме вызов функции передает аргумент узла XML с помощью свойства [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) объекта [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) следующим образом. 
  
```cs
CheckErrors(e.Site);
```

Помимо обработки ошибок, создаваемых приложением InfoPath, разработчики форм также могут создавать пользовательские ошибки с помощью метода **ReportError** для объекта событий **DataDOMEventObject** или метода **Add** семейства **ErrorsCollection**. Для получения сведений об использовании методов **ReportError** и **Add** щелкните методы в начале данного раздела. 
  
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
  

