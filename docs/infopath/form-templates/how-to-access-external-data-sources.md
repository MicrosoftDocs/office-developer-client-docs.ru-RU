---
title: Доступ к внешним источникам данных
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- классы подключений к данным [InfoPath 2007], дополнительные источники данных [InfoPath 2007], данные [InfoPath 2007], дополнительный, класс DataSource [InfoPath 2007], доступ к внешним источникам данных [InfoPath 2007], Класс DataSourceCollection [InfoPath 2007], Класс DataConnectionCollection [InfoPath 2007], класс подключения к данным [InfoPath 2007], InfoPath 2007, доступ к внешним данным, Data [InfoPath 2007], внешние источники
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: При работе с шаблоном формы InfoPath можно написать код для доступа к дополнительным источникам данных формы и управления содержащимися в них данными.
ms.openlocfilehash: f6957c561231eef0e3e4df6deb09ae89f85afcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408315"
---
# <a name="access-external-data-sources"></a>Доступ к внешним источникам данных

При работе с шаблоном формы InfoPath можно написать код для доступа к дополнительным источникам данных формы и управления содержащимися в них данными. 
  
Каждый дополнительный источник данных представлен объектом, созданным с помощью класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , и соответствует сохраненным данным, полученным из внешнего источника данных, например базы данных или запроса веб-службы. Эти источники данных указываются как дополнительные, поскольку при сохранении пользователем формы InfoPath сохраняются только данные из основного (или главного) источника данных, но не данные из дополнительных источников. Подключение к источнику данных представлено объектом, созданным с помощью одного из классов "подключение к данным", например класс [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) , который представляет подключение данных к веб-службе XML. 
  
Экземпляр объекта [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) представляет хранилище XML-данных, возвращенных подключением к данным (из базы данных или запроса веб-службы), а класс подключения к данным представляет само подключение данных (как определено и названо с использованием **данных **Команда "подключения" на вкладке " **данные** ". 
  
Объектная модель InfoPath поддерживает доступ к дополнительным источникам данных формы с помощью класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) в связи с классом [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) . 
  
Объектная модель InfoPath также предоставляет набор классов подключений данных, где содержатся сведения об используемых формой подключениях данных.
  
> [!NOTE]
> В приложении Microsoft InfoPath 2003 подключение данных указывается как адаптер данных.  
  
Подключения к данным бывают двух типов: подключения к запросам используются для получения данных, которые затем хранятся в дополнительном источнике данных. Подключения для отправления используются для отсылки данных в базу данных или веб-службу, например. Отправленные данные копируются из основных или дополнительных источников данных. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Обзор класса DataSourceCollection

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие свойства и методы, которые могут использоваться разработчиками форм для управления экземплярами объектов [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) , содержащимися в форме. 
  
|**Name**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Возвращает количество экземпляров объектов  **DataSource** в семействе.  <br/> |
|Метод [GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Возвращает объект **IEnumerator**, который можно использовать для выполнения итерации по семейству.  <br/> |
|Свойство [Item [Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по значению индекса.  <br/> |
|Свойство [Item [String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по имени.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Обзор класса DataSource

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с дополнительным источником данных InfoPath. 
  
|**Name**|**Описание**|
|:-----|:-----|
|Метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Возвращает объект [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) для доступа к источнику данных и его изменения  <br/> |
|Свойство [куериконнектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Возвращает ссылку на связанный объект подключения данных.  <br/> Чтобы выполнить запрос для подключения данных и вставить возвращенные данные в виде XML-кода в узел XML, связанный с объектом **DataSource** , используйте метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) связанного объекта подключения данных.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Возвращает имя объекта **DataSource**.  <br/> |
|Свойство [ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает наличие у источника данных атрибута только для чтения  <br/> |
|Метод [жетнамеднодепроперти](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Возвращает значение именованного свойства для указанного узла XML, который должен быть узлом **nonattribute** в основном источнике данных.  <br/> |
|Метод [сетнамеднодепроперти](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Задает значение именованного свойства для указанного XML-узла, который должен являться узлом **nonattribute** в основном источнике данных.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Обзор классов подключений данных

Классы для доступа к подключениям к данным предоставляют различные свойства и методы, которые извлекают и отправляют данные через подключения к внешним источникам данных; подключение к данным, связанное с объектом **DataSource** , зависит от типа подключения к внешним данным. InfoPath реализует следующие классы для доступа к подключениям к данным. 
  
|**Name**|**Описание**|
|:-----|:-----|
|Класс [ADOQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Запрашивает источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|Класс [AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Отправляет данные в источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|Класс [шарепоинтлистрвкуериконнектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Запрашивает библиотеку документов или список SharePoint.  <br/> |
|[Шарепоинтлистрвсубмитконнектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Отправляет данные в библиотеку документов или список SharePoint.  <br/> |
|Класс [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Подключается к веб-службе XML.  <br/> |
|Класс [FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Запрашивает XML-файл.  <br/> |
|Класс [FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Отправляет данные в XML-файл.  <br/> |
|Класс [EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Отправка формы в виде вложения в сообщение электронной почты.  <br/> |
|Класс [бдккуериконнектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Запрос внешнего списка на сервере, на котором работает SharePoint Foundation 2010 или SharePoint Server 2010.  <br/> |
|Класс [бдксубмитконнектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |ОтПравляются во внешний список на сервере, на котором работает SharePoint Foundation 2010 или SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Использование классов DataSourceCollection и DataSource

Доступ к объекту **DataSourceCollection** , представляющему коллекцию источников данных, связанных с шаблоном формы, осуществляется через [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) свойство DataSources класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Например, при создании дополнительного источника данных Employees, получающего данные из таблицы Employees базы данных компании "Борей", можно использовать объект **DataSourceCollection** для указания ссылки на объект **DataSource**, представляющий полученные данные. 
  
В следующем примере кода имя дополнительного источника данных передается в свойство аксессор класса **DataSourceCollection** , которое возвращает ссылку на объект **DataSource** , представляющий извлеченные данные таблицы Employees. XML-узел, где хранятся данные, полученные из дополнительного источника данных, отображается в окне сообщения с помощью метода **CreateNavigator** класса **DataSource** для доступа к свойству **InnerXml** класса **XPathNavigator**. 
  
```cs
// Instantiate a variable to access the specified data source
// from the DataSourceCollection of the form.
DataSource myDataSource = 
   this.DataSources["Employees"];
// Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " +
   myDataSource.CreateNavigator().InnerXml.ToString());
```

```vb
' Instantiate a variable to access the specified data source
' from the DataSourceCollection of the form.
Dim myDataSource As DataSource = _
   Me.DataSources("Employees")
' Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " &amp; _
   myDataSource.CreateNavigator().InnerXml.ToString())
```

Для управления данными, содержащимися в дополнительном источнике данных, используйте метод **CreateNavigator** класса **DataSource**, чтобы вернуть ссылку на объект **XPathNavigator**, расположенный на узле, где хранятся дополнительные данные. Чтобы управлять данными, можно воспользоваться свойствами и методами класса **XPathNavigator**. Дополнительные сведения см. в статье Work of the [xpathnavigators and XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Использование классов DataConnectionCollection и DataConnection

Доступ к объекту [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) , представляющему коллекцию подключений данных, связанных с шаблоном формы, осуществляется с [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) помощью свойства Connections класса **XmlForm** . Например, при создании дополнительного источника данных Employees, получающего данные из таблицы Employees базы данных "Борей", можно использовать объект **DataConnectionCollection**, связанный  с шаблоном формы, для указания ссылки на объект **DataConnection**, представляющий подключение к базе данных. 
  
В следующем примере кода имя дополнительного источника данных передается в метод доступа класса **DataConnectionCollection**, который в данном случае возвращает ссылку на объект **ADOQueryConnection**, представляющий подключение к базе данных "Борей". Чтобы эта процедура работала правильно, необходимо явно привести возвращаемый объект к типу **ADOQueryConnection**. Свойство [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) интерфейса **адоадаптеробжект** используется для отображения строки подключения ADO в окне сообщения. 
  
```cs
// Instantiate a variable to access the specified data connection
// from the DataConnectionCollection of the form. 
// You must cast to the specific data connection type
// (ADOQueryConnection) before you can access the data connection.
ADOQueryConnection myADOConnection = 
   (ADOQueryConnection)this.DataConnections["Employees"];
// Display the connection information for the data connection.
MessageBox.Show("Connection string: " + myADOConnection.Connection);
```

```vb
' Instantiate a variable to access the specified data connection
' from the DataConnectionCollection of the form. 
' You must cast to the specific data connection type
' (ADOQueryConnection) before you can access the data connection.
Dim myADOConnection As ADOQueryConnection = _
   DirectCast(Me.DataConnections("Employees"), ADOQueryConnection)
' Display the connection information for the data connection.
MessageBox.Show("Connection string: " &amp; myADOConnection.Connection)
```

## <a name="see-also"></a>См. также



[Создание шаблонов форм InfoPath, работающих со службами InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

