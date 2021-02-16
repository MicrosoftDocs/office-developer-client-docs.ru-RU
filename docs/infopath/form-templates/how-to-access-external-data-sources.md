---
title: Доступ к внешним источникам данных
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- классы подключений к данным [infopath 2007],secondary data sources [InfoPath 2007],data [InfoPath 2007], secondary,DataSource class [InfoPath 2007],accessing external data sources [InfoPath 2007],DataSourceCollection class [InfoPath 2007],DataConnectionCollection class [InfoPath 2007],DataConnection class [InfoPath 2007],InfoPath 2007, accessing external data,data [InfoPath 2007], external sources
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
  
Каждый дополнительный источник данных представлен объектом, который был с помощью класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) и соответствует хранимым данным, полученным из внешнего источника данных, например из базы данных или запроса веб-службы. Эти источники данных указываются как дополнительные, поскольку при сохранении пользователем формы InfoPath сохраняются только данные из основного (или главного) источника данных, но не данные из дополнительных источников. Подключение к источнику данных представлено объектом, который был сконфицирован с помощью одного из классов "подключения к данным", например класса [WebServiceConnection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) который представляет подключение к данным веб-службы XML. 
  
Объект [DataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) который был установлен, представляет хранилище XML-данных, возвращаемого подключением к данным (из базы данных или запроса веб-службы),  а класс "подключение к данным" представляет само подключение к данным (как определено и названо с помощью команды "Подключения к данным" на вкладке "Данные").  
  
Объектная модель InfoPath поддерживает доступ к дополнительным источникам данных формы с помощью класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) в связи с классом [DataSourceCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) 
  
Объектная модель InfoPath также предоставляет набор классов подключений данных, где содержатся сведения об используемых формой подключениях данных.
  
> [!NOTE]
> В приложении Microsoft InfoPath 2003 подключение данных указывается как адаптер данных.  
  
Подключения к данным имеют два типа: подключения запросов используются для получения данных, которые затем хранятся во вторичном источнике данных. Подключения отправки используются, например, для отправки данных в базу данных или в веб-службу. Отправленные данные копируются из основных или дополнительных источников данных. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Обзор класса DataSourceCollection

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие свойства и методы, которые разработчики форм могут использовать для управления экземплярами объектов [DataSourceCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) которые содержит форма. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Возвращает количество экземпляров объектов  **DataSource** в семействе.  <br/> |
|[Метод GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Возвращает объект **IEnumerator**, который можно использовать для выполнения итерации по семейству.  <br/> |
|[Свойство Item[Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по значению индекса.  <br/> |
|[Свойство Item[String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по имени.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Обзор класса DataSource

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие методы и свойства, которые разработчики форм могут использовать для взаимодействия с дополнительным источником данных InfoPath. 
  
|**Название**|**Описание**|
|:-----|:-----|
|[Метод CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Возвращает объект [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) для доступа к источнику данных и его редактирования  <br/> |
|[Свойство QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Возвращает ссылку на связанный объект подключения данных.  <br/> Чтобы выполнить запрос подключения к данным и вставить возвращенные данные в XML-узел, связанный с объектом **DataSource,** используйте метод [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) связанного объекта подключения к данным.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Возвращает имя объекта **DataSource**.  <br/> |
|[Свойство ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает наличие у источника данных атрибута только для чтения  <br/> |
|[Метод GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Возвращает значение именованного свойства для указанного узла XML, который должен быть узлом **nonattribute** в основном источнике данных.  <br/> |
|[Метод SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Задает значение именованного свойства для указанного XML-узла, который должен являться узлом **nonattribute** в основном источнике данных.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Обзор классов подключений данных

Классы для доступа к подключениям к данным предоставляют различные свойства и методы, которые извлекать и отправлять данные через подключения к внешним источникам данных; Подключение к данным, связанное с объектом **DataSource,** зависит от типа подключения к внешним данным. InfoPath реализует следующие классы для доступа к подключениям к данным. 
  
|**Название**|**Описание**|
|:-----|:-----|
|[Класс AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Запрашивает источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|[Класс AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Отправляет данные в источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|[Класс SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Запрашивает библиотеку документов или список SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Отправляет данные в библиотеку документов или список SharePoint.  <br/> |
|[Класс WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Подключается к веб-службе XML.  <br/> |
|[Класс FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Запрашивает XML-файл.  <br/> |
|[Класс FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Отправляет данные в XML-файл.  <br/> |
|[Класс EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Отправка формы в виде вложения в сообщении электронной почты.  <br/> |
|[Класс BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Запрашивает внешний список на сервере с SharePoint Foundation 2010 или SharePoint Server 2010.  <br/> |
|[Класс BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Отправка во внешний список на сервере с SharePoint Foundation 2010 или SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Использование классов DataSourceCollection и DataSource

Доступ к объекту **DataSourceCollection,** который представляет коллекцию источников данных, связанных с шаблоном формы, можно получить с помощью свойства [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Например, при создании дополнительного источника данных Employees, получающего данные из таблицы Employees базы данных компании "Борей", можно использовать объект **DataSourceCollection** для указания ссылки на объект **DataSource**, представляющий полученные данные. 
  
В следующем примере кода имя дополнительного источника данных передается в свойство доступа класса **DataSourceCollection,** которое возвращает ссылку на объект **DataSource,** который представляет извлеченные данные таблицы Employees. XML-узел, где хранятся данные, полученные из дополнительного источника данных, отображается в окне сообщения с помощью метода **CreateNavigator** класса **DataSource** для доступа к свойству **InnerXml** класса **XPathNavigator**. 
  
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

Для управления данными, содержащимися в дополнительном источнике данных, используйте метод **CreateNavigator** класса **DataSource**, чтобы вернуть ссылку на объект **XPathNavigator**, расположенный на узле, где хранятся дополнительные данные. Чтобы управлять данными, можно воспользоваться свойствами и методами класса **XPathNavigator**. Дополнительные сведения см. в работе [с классами XPathNavigator и XPathNodeIterator.](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Использование классов DataConnectionCollection и DataConnection

Доступ [к объекту DataConnectionCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) представляюлю коллекцию подключений к данным, связанных с шаблоном формы, можно получить с помощью свойства [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) класса **XmlForm.** Например, при создании дополнительного источника данных Employees, получающего данные из таблицы Employees базы данных "Борей", можно использовать объект **DataConnectionCollection**, связанный  с шаблоном формы, для указания ссылки на объект **DataConnection**, представляющий подключение к базе данных. 
  
В следующем примере кода имя дополнительного источника данных передается в метод доступа класса **DataConnectionCollection**, который в данном случае возвращает ссылку на объект **ADOQueryConnection**, представляющий подключение к базе данных "Борей". Чтобы эта процедура работала правильно, необходимо явно привести возвращаемый объект к типу **ADOQueryConnection**. Свойство [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) интерфейса **ADOAdapterObject** используется для отображения строки подключения ADO в окне сообщения. 
  
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

