---
title: Доступа к внешним источникам данных
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- классов подключений данных [infopath 2007], дополнительным источникам данных [InfoPath 2007], данных [InfoPath 2007], дополнительный, класс DataSource [InfoPath 2007], доступ к внешним источникам данных [InfoPath 2007], класс DataSourceCollection [InfoPath 2007] Класс DataConnectionCollection [InfoPath 2007], класс DataConnection [InfoPath 2007], InfoPath 2007, доступ к внешним данным, данные [InfoPath 2007] внешних источников
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: При работе с шаблона формы InfoPath можно написать код для доступа к дополнительным источникам данных формы и работы с данными, которые они содержат.
ms.openlocfilehash: e26708e0033bbfe4110ac522dd1e0a0dd037c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807493"
---
# <a name="access-external-data-sources"></a>Доступа к внешним источникам данных

При работе с шаблона формы InfoPath можно написать код для доступа к дополнительным источникам данных формы и работы с данными, которые они содержат. 
  
Каждый дополнительный источник данных представлены объектом создан с помощью класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) и соответствующий сохраненные данные, полученные из внешнего источника данных, например база данных или веб-службы запросов. Следующие источники данных будут называться дополнительный так как при сохранении формы InfoPath, пользователь является сохранение данных только в источнике данных основной (или основной), не данные в дополнительные источники данных. Подключение к источнику данных, представленного объект, созданный с помощью одного из классов «подключение к данным», такие как класс [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) , который представляет подключение к веб-службе XML. 
  
Представляет экземпляр объекта [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) хранилище данных XML, возвращенный подключения к данным (из базы данных или веб-службы запросов) и класс «подключение к данным» представляет само подключение к данным (как определенной и именованные с помощью **данных Подключения к** на вкладке **данные** ). 
  
Объектная модель InfoPath поддерживает доступ к источникам данных дополнительного формы посредством использования класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) в сочетании с классом [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) . 
  
Объектная модель InfoPath также предоставляет набор классов подключений данных, где содержатся сведения об используемых формой подключениях данных.
  
> [!NOTE]
> В Microsoft InfoPath 2003 подключение данных называется адаптера данных. 
  
Подключения к данным могут быть двух типов: подключения запроса, используемые для получения данных, которая хранится в дополнительного источника данных. Отправка подключения, используемые для отправки данных в базу данных или веб-службы, например. Переданные данные копируются из главного или дополнительного источника данных. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Обзор класса DataSourceCollection

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие свойства и методы, которые могут использоваться разработчиками форм для управления экземплярами объекта [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) , содержащимися в форме. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Возвращает количество экземпляров объектов **DataSource** , содержащихся в коллекции.  <br/> |
|Метод [GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Возвращает объект **IEnumerator** , который можно использовать для итерации по коллекции.  <br/> |
|Свойство [Item [Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по значению индекса.  <br/> |
|Свойство [Item [String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **DataSource** по имени.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Обзор класса DataSource

Класс [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с дополнительным источником данных InfoPath. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Возвращает объект [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) для доступа и редактирования источника данных  <br/> |
|Свойство [QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Возвращает ссылку на связанный объект подключения данных.   <br/> Чтобы выполнить запрос на подключение к данным и вставка возвращенные данные в XML-ФАЙЛЕ в узле XML, связанного с объектом **источника данных** , используйте метод [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) связанный объект подключения данных.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Возвращает имя объекта **DataSource** .  <br/> |
|Свойство [только для чтения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает наличие у источника данных атрибута только для чтения  <br/> |
|Метод [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Получает значение именованного свойства для указанного узла XML, который должен быть **узлом nonattribute в основном источнике данных** .  <br/> |
|Метод [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Задает значение именованного свойства для указанного узла XML, который должен быть **узлом nonattribute в основном источнике данных** .  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Обзор классов подключений данных

Классы для доступа к подключений к данным предоставляют различные свойства и методы для получения и отправки данных через подключения к внешним источникам данных; подключение к данным, связанного с объектом **источника данных** , зависит от типа подключения к внешним данным. InfoPath реализует следующие классы для доступа к подключений к данным. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Класс [AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Запрашивает источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|Класс [AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Отправляет данные в источник данных ADO/OLEDB, ограничивается Microsoft Access и Microsoft SQL Server.  <br/> |
|Класс [SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Запрашивает библиотеку документов или список SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Отправляет данные в библиотеку документов или список SharePoint.  <br/> |
|Класс [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Подключается к веб-службе XML.  <br/> |
|Класс [FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Запрашивает XML-файл.  <br/> |
|Класс [FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Отправляет данные в XML-файл.  <br/> |
|Класс [EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Отправляет форму в виде вложения в сообщении электронной почты.  <br/> |
|Класс [BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Запрашивает внешний список на сервере под управлением SharePoint Foundation 2010 и SharePoint Server 2010.  <br/> |
|Класс [BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Отправляет данные во внешний список на сервере под управлением SharePoint Foundation 2010 и SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Использование классов DataSourceCollection и DataSource

**DataSourceCollection** объект, представляющий коллекцию источников данных, связанных с шаблоном формы доступен через свойство [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Например, при создании дополнительного источника данных с именем сотрудников, который получает данные из таблицы Employees базы данных Northwind, можно использовать объекта **DataSourceCollection** для задания ссылки на объект **DataSource** , который представляет извлеченные данные. 
  
В следующем примере кода имя дополнительного источника данных передается свойство доступа класса **DataSourceCollection** , которое возвращает ссылку на объект **DataSource** , который представляет извлеченные данные в таблице сотрудников. Узел XML, в которой хранятся извлеченные данные из дополнительного источника данных отображается в окне сообщения с помощью метода **CreateNavigator** класса **источника данных** для доступа к свойству **InnerXml** класса **XPathNavigator** . 
  
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

Для работы с данными, в дополнительного источника данных, используйте метод **CreateNavigator** класса **DataSource** возвращает ссылку на объект **XPathNavigator** , размещенный в узле, где хранится дополнительных данных. Можно использовать свойства и методы класса **XPathNavigator** для работы с данными. Для получения дополнительных сведений см [классов XPathNavigator и XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Использование классов DataConnectionCollection и DataConnection

[DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) объект, представляющий коллекцию подключений к данным, связанного с шаблоном формы доступен через свойство [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) класса **XmlForm** . Например при создании дополнительного источника данных с именем сотрудников, который получает данные из таблицы Employees базы данных Northwind, можно использовать объект **DataConnectionCollection** , связанный с шаблоном формы для задания ссылки на ** Подключение данных** , который представляет подключение к базе данных. 
  
В следующем примере кода имя дополнительного источника данных передается свойство доступа к данным класс **DataConnectionCollection** , который в этом случае возвращает ссылку на объект **ADOQueryConnection** , который представляет подключение к базе данных "Борей". Для правильной работы необходимо явно привести объект, возвращаемых к типу **ADOQueryConnection** . Свойство [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) интерфейса **ADOAdapterObject** используется для отображения в окне сообщения строки подключения ADO. 
  
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

