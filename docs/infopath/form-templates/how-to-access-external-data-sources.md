---
title: Доступ к внешним источникам данных
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- классы подключения к данным [infopath 2007], вторичные источники данных [InfoPath 2007], данные [InfoPath 2007], secondary,Класс DataSource [InfoPath 2007], доступ к внешним источникам данных [InfoPath 2007], класс DataSourceCollection [InfoPath 2007], класс DataConnectionCollection [InfoPath 2007], класс DataConnection [InfoPath 2007], InfoPath 2007, доступ к внешним данным, данным [InfoPath 2007], внешним источникам
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
  
Каждый вторичный источник данных представляет объект, мгновенный с помощью класса [DataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) и соответствует хранимым данным, полученным из некоторых внешних источников данных, таких как база данных или запрос веб-службы. Эти источники данных указываются как дополнительные, поскольку при сохранении пользователем формы InfoPath сохраняются только данные из основного (или главного) источника данных, но не данные из дополнительных источников. Подключение к источнику данных представляет объект, мгновенный с помощью одного из классов "подключения к данным", например класса [WebServiceConnection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) который представляет подключение данных к веб-службе XML. 
  
Мгновенный объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) представляет хранилище XML-данных, возвращаемого подключением к данным (из базы данных или запроса веб-службы), а класс  "подключение к данным" представляет само подключение к данным (как определено и названо с помощью команды подключения к данным на вкладке **Data).** 
  
Объектная модель InfoPath поддерживает доступ к вторичным источникам данных формы с помощью класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) в связи с классом [DataSourceCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) 
  
Объектная модель InfoPath также предоставляет набор классов подключений данных, где содержатся сведения об используемых формой подключениях данных.
  
> [!NOTE]
> В приложении Microsoft InfoPath 2003 подключение данных указывается как адаптер данных.  
  
Существует два типа подключений данных. Подключения запросов используются для получения данных, которые затем сохраняются в дополнительном источнике данных. Подключения отправки используются для отправки данных, например, в базу данных или веб-службу. Отправленные данные копируются из основных или дополнительных источников данных. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Обзор класса DataSourceCollection

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие свойства и методы, которые разработчики форм могут использовать для управления экземплярами объектов [DataSourceCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) которые содержит форма. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Возвращает количество экземпляров объектов  **DataSource** в семействе.  <br/> |
|[Метод GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Возвращает объект **IEnumerator**, который можно использовать для выполнения итерации по семейству.  <br/> |
|[Свойство Item[Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по значению индекса.  <br/> |
|[Свойство Item[String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по имени.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Обзор класса DataSource

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующий метод и свойства, которые разработчики форм могут использовать для взаимодействия с дополнительным источником данных InfoPath. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Метод CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Возвращает объект [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) для доступа и редактирования источника данных  <br/> |
|[Свойство QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Возвращает ссылку на связанный объект подключения данных.  <br/> Чтобы выполнить запрос на подключение к данным и вставить возвращенные данные в XML-узел, связанный с объектом **DataSource,** используйте метод [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) связанного объекта подключения к данным.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Возвращает имя объекта **DataSource**.  <br/> |
|[Свойство ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает наличие у источника данных атрибута только для чтения  <br/> |
|[Метод GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Возвращает значение именованного свойства для указанного узла XML, который должен быть узлом **nonattribute** в основном источнике данных.  <br/> |
|[Метод SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Задает значение именованного свойства для указанного XML-узла, который должен являться узлом **nonattribute** в основном источнике данных.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Обзор классов подключений данных

Классы для доступа к подключениям данных представляют различные свойства и методы для получения и отправки данных через подключения к внешним источникам данных. Подключение данных, связанное с объектом **DataSource**, зависит от типа подключения внешних данных. Для доступа к подключениям данных приложение InfoPath реализует следующие классы. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Класс AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Запрашивает источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|[Класс AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Отправляет данные в источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|[Класс SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Запрашивает библиотеку документов или список SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Отправляет данные в библиотеку документов или список SharePoint.  <br/> |
|[Класс WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Подключается к веб-службе XML.  <br/> |
|[Класс FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Запрашивает XML-файл.  <br/> |
|[Класс FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Отправляет данные в XML-файл.  <br/> |
|[Класс EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Отправка формы в виде вложения в электронной почте.  <br/> |
|[Класс BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Запросы внешнего списка на сервере с SharePoint Foundation 2010 или SharePoint Server 2010.  <br/> |
|[Класс BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Представляет внешний список на сервере с SharePoint Foundation 2010 или SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Использование классов DataSourceCollection и DataSource

Объект **DataSourceCollection,** представляю который представляет коллекцию источников данных, связанных с шаблоном форм, можно получить доступ через свойство [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Например, при создании дополнительного источника данных Employees, получающего данные из таблицы Employees базы данных компании "Борей", можно использовать объект **DataSourceCollection** для указания ссылки на объект **DataSource**, представляющий полученные данные. 
  
В следующем примере кода имя вторичного источника данных передается свойству вспомогательного свойства класса **DataSourceCollection,** которое возвращает ссылку на объект **DataSource,** который представляет извлеченные данные таблицы Сотрудников. XML-узел, где хранятся данные, полученные из дополнительного источника данных, отображается в окне сообщения с помощью метода **CreateNavigator** класса **DataSource** для доступа к свойству **InnerXml** класса **XPathNavigator**. 
  
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

Для управления данными, содержащимися в дополнительном источнике данных, используйте метод **CreateNavigator** класса **DataSource**, чтобы вернуть ссылку на объект **XPathNavigator**, расположенный на узле, где хранятся дополнительные данные. Чтобы управлять данными, можно воспользоваться свойствами и методами класса **XPathNavigator**. Дополнительные сведения см. в этой ссылке [Работа с классами XPathNavigator и XPathNodeIterator.](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Использование классов DataConnectionCollection и DataConnection

К [объекту DataConnectionCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) представляюстоя коллекцию подключений к данным, связанным с шаблоном форм, можно получить доступ через свойство [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) класса **XmlForm.** Например, при создании дополнительного источника данных Employees, получающего данные из таблицы Employees базы данных "Борей", можно использовать объект **DataConnectionCollection**, связанный  с шаблоном формы, для указания ссылки на объект **DataConnection**, представляющий подключение к базе данных. 
  
В следующем примере кода имя дополнительного источника данных передается в метод доступа класса **DataConnectionCollection**, который в данном случае возвращает ссылку на объект **ADOQueryConnection**, представляющий подключение к базе данных "Борей". Чтобы эта процедура работала правильно, необходимо явно привести возвращаемый объект к типу **ADOQueryConnection**. Свойство [Подключение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) **интерфейса ADOAdapterObject** используется для отображения строки подключения ADO в поле сообщений. 
  
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

