---
title: Доступ к внешним источникам данных с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- источники данных [InfoPath 2007], доступ с помощью объектной модели InfoPath 2003, шаблоны форм, совместимые с InfoPath 2003, доступ к внешним данным
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: При работе с шаблоном формы InfoPath, использующим объектную модель, совместимую с InfoPath 2003, можно написать код для доступа к дополнительным источникам данных формы и управления содержащимися в них данными.
ms.openlocfilehash: 569f029b412328f4d49e3079eaf207dc1556fc4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303698"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Доступ к внешним источникам данных с помощью объектной модели InfoPath 2003

При работе с шаблоном формы InfoPath, использующим объектную модель, совместимую с InfoPath 2003, можно написать код для доступа к дополнительным источникам данных формы и управления содержащимися в них данными.
  
Каждый дополнительный источник данных представлен объектом, созданным с помощью интерфейса [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , и соответствует сохраненным данным, полученным из внешнего источника данных, например базы данных или запроса веб-службы. Эти источники данных указываются как дополнительные, поскольку при сохранении пользователем формы InfoPath сохраняются только данные из основного источника данных, но не данные из дополнительных источников. Подключение к источнику данных представлено объектом, созданным с помощью одного из интерфейсов "адаптер данных", таких как интерфейс [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) , который представляет подключение к данным веб-службе XML. 
  
Созданный экземпляр объекта [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) представляет хранилище XML-данных, возвращаемых подключением данных (в запрос базы данных или веб-службы), а адаптер данных представляет само подключение данных. 
  
Объектная модель InfoPath поддерживает доступ к дополнительным источникам данных формы с помощью интерфейса [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) в связи с интерфейсом [датаобжектсколлектион](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) . 
  
Также объектная модель InfoPath предоставляет набор объектов адаптера данных, содержащий сведения об используемых формой подключениях к данным. 
  
Существует два типа адаптеров данных: адаптеры запросов и адаптеры отправки. Адаптеры запросов используются для получения данных, которые затем сохраняются в дополнительном источнике данных, а адаптеры отправки используются для отправки данных, например, в базу данных или в веб-службу. Отправленные данные копируются из основных или дополнительных источников данных. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Обзор интерфейса DataObjectsCollection

Интерфейс [датаобжектсколлектион](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) предоставляет следующие свойства и методы, которые могут использоваться разработчиками форм для управления экземплярами [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , содержащимися в форме. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Возвращает количество экземпляров **DataSourceObject** в семействе.  <br/> |
|Метод [GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Возвращает объект **IEnumerator**, который можно использовать для выполнения итерации по семейству.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Возвращает ссылку на указанный экземпляр **DataSourceObject**.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Обзор интерфейса DataSourceObject

Интерфейс [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с дополнительным источником данных InfoPath. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [запроса](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx)  <br/> |Выполняет запрос для адаптера данных и вставляет возвращенные данные в виде XML в модель XML DOM, связанную с **DataSourceObject**.  <br/> |
|Свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Возвращает ссылку на модель XML DOM, используемую для хранения и обработки данных с помощью **DataSourceObject**.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Возвращает строковое значение, указывающее имя объекта **DataSourceObject**.  <br/> |
|Свойство [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Возвращает ссылку на связанный объект адаптера данных.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Обзор интерфейсов адаптера данных

Интерфейсы для доступа к адаптерам данных предоставляют различные свойства и методы, которые извлекают и отправляют данные через подключения к внешним источникам данных; адаптер данных, связанный с объектом [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , зависит от типа подключения к внешним данным. InfoPath реализует следующие интерфейсы для доступа к адаптерам данных. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Интерфейс [адоадаптеробжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Подключается к источникам данных ADO/OLEDB, которые ограничены Microsoft Access и Microsoft SQL Server™.  <br/> |
|Интерфейс [шарепоинтлистадаптеробжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Подключается к библиотеке документов или списку SharePoint.  <br/> |
|Интерфейс [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Подключается к веб-службам XML.  <br/> |
|Объект [XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Подключается к XML-файлу.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Использование интерфейсов DataSourceObjects и DataSourceObject

Доступ к коллекции **датасаурцеобжектс** осуществляется через свойство [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Например, если создать дополнительный источник данных "Employees", который получает данные из таблицы "Employees" базы данных Microsoft Access компании "Борей", то можно использовать семейство **DataSourceObjects** для указания ссылки на объект **DataObject**, представляющий полученные данные. 
  
В следующем примере кода имя дополнительного источника данных передается в метод доступа интерфейса **DataObjectsCollection**, который возвращает ссылку на объект **DataSourceObject**. Данные из дополнительного источника данных отображаются в окне сообщения с помощью свойства **DOM** интерфейса **DataSourceObject** для доступа к свойству **xml** модели XML DOM. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataObjectsCollection of the form.
   // You must explicitly cast to the DataSourceObject type 
   // before you can access the data object.
   DataSourceObject myDataObject = 
      thisXDocument.DataObjects["Employees"] as DataSourceObject;
   // Display the data from the secondary data source using the 
   // XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object
   ' from the DataObjectsCollection of the form.
   Dim myDataObject As DataSourceObject = _
      thisXDocument.DataObjects("Employees")
   ' Display the data from the secondary data source using the 
   ' XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml)
End Sub
```

Для управления данными, содержащимися в дополнительном источнике данных, используйте свойство **DOM** интерфейса **DataSourceObject**, чтобы вернуть ссылку на модель XML DOM, содержащую данные. После получения ссылки на модель XML DOM можно пользоваться любыми свойствами и методами этой модели для управления этими данными. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Использование интерфейсов DataAdaptersCollection и DataAdapterObject

Доступ к интерфейсу [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) осуществляется с [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) помощью свойства Adapters интерфейса **XDocument** . Например, если создать дополнительный источник данных "Employees", который получает данные из таблицы "Employees" базы данных Microsoft Access компании "Борей", то можно использовать семейство **DataAdapterObjects** для указания ссылки на объект **DataAdapterObject**, представляющий подключение к базе данных. 
  
В следующем примере кода имя дополнительного источника данных передается в метод доступа интерфейса **DataAdaptersCollection**, который в этом случае возвращает ссылку на экземпляр **ADOAdapterObject**, представляющий подключение к базе данных Microsoft Access компании "Борей". Чтобы эта схема работала правильно, необходимо использовать явное приведение объекта, возвращаемого в виде **ADOAdapterObject**. Свойство [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) интерфейса **адоадаптеробжект** используется для отображения строки подключения ADO в окне сообщения. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataAdaptersCollection of the form. 
   // You must explicitly cast to the specific adapter type
   // (ADOAdapterObject) before you can access the data adapter.
   ADOAdapterObject myADOAdapter = 
      thisXDocument.DataAdapters["Employees"] as ADOAdapterObject;
   // Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object. 
   ' You must explicitly cast to the specific adapter type
   ' (ADOAdapterObject) before you can access the data adapter.
   Dim myADOAdapter As ADOAdapterObject = _
      thisXDocument.DataAdapters("Employees")
   ' Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection)
End Sub
```


