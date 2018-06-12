---
title: Доступа к внешним источникам данных с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Источники данных [infopath 2007], доступ к объектной модели infopath 2003, совместимых с InfoPath 2003 шаблонов форм, доступ к внешним данным
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: При работе с шаблоном формы InfoPath, использующим объектную модель, совместимую с InfoPath 2003, можно написать код для доступа к дополнительным источникам данных формы и управления содержащимися в них данными.
ms.openlocfilehash: cf06cdc6a02eba855442cdab4c3c698ed3f4425f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807486"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Доступа к внешним источникам данных с помощью объектной модели InfoPath 2003

При работе с шаблоном формы InfoPath, использующим объектную модель, совместимую с InfoPath 2003, можно написать код для доступа к дополнительным источникам данных формы и управления содержащимися в них данными.
  
Каждый дополнительный источник данных представлены объектом создан с помощью интерфейса [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) и соответствующий сохраненные данные, полученные из внешнего источника данных, например база данных или веб-службы запросов. Следующие источники данных будут называться дополнительный так как при сохранении формы InfoPath, пользователь является сохранение данных только в основном источнике данных, не данные в дополнительные источники данных. Подключение к источнику данных, представленного объект, созданный с помощью одного из интерфейсов «адаптер данных», например, интерфейс [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) , который представляет подключение к веб-службе XML. 
  
Представляет экземпляр объекта [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) хранилище данных XML, возвращенных подключения к данным (к базе данных или веб-службы запросов) и адаптер данных представляет само подключение к данным. 
  
Объектная модель InfoPath поддерживает доступ к источникам данных дополнительного формы посредством использования интерфейса [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) в сочетании с помощью интерфейса [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) . 
  
Также объектная модель InfoPath предоставляет набор объектов адаптера данных, содержащий сведения об используемых формой подключениях к данным.  
  
Существует два типа адаптеров данных: запроса адаптеров и отправки адаптеров. Для получения данных, которая хранится в дополнительного источника данных в то время как отправить адаптеров используются для отправки данных в базу данных или веб-службы, например используются адаптеры запроса. Переданные данные копируются из главного или дополнительного источника данных. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Обзор интерфейса DataObjectsCollection

Интерфейс [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) предоставляет следующие свойства и методы, которые могут использоваться разработчиками форм для управления экземплярами [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , содержащимися в форме. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Возвращает количество экземпляров **DataSourceObject** в семействе сайтов.  <br/> |
|Метод [GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Возвращает объект **IEnumerator** , который можно использовать для итерации по коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Возвращает ссылку на указанный экземпляр **DataSourceObject** .  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Обзор интерфейса DataSourceObject

Интерфейс [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с дополнительным источником данных InfoPath. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx)  <br/> |Выполняет запрос для адаптера данных и вставляет возвращенные данные XML в модели объектов документа XML (DOM), связанную с **DataSourceObject**.  <br/> |
|Свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Возвращает ссылку на модель XML DOM, используемую для хранения и обработки данных с помощью **DataSourceObject**.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Возвращает строковое значение, указывающее имя объекта **DataSourceObject**.  <br/> |
|Свойство [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Возвращает ссылку на связанный объект адаптера данных.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Обзор интерфейсов адаптера данных

Интерфейсы для доступа к адаптеров данных предоставляют различные свойства и методы для получения и отправки данных через подключения к внешним источникам данных; адаптер данных, связанный с объектом [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , зависит от типа подключения к внешним данным. InfoPath реализует следующие интерфейсы для доступа к адаптеров данных. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Интерфейс [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Подключается к источникам данных ADO/OLEDB, которые ограничены Microsoft Access и Microsoft SQL Server™.  <br/> |
|Интерфейс [SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Подключается к библиотеке документов или списку SharePoint.  <br/> |
|Интерфейс [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Подключается к веб-службам XML.  <br/> |
|Объект [XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Подключается к XML-файлу.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Использование интерфейсов DataSourceObjects и DataSourceObject

Коллекция **DataSourceObjects** доступен через свойство [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) интерфейс [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Например при создании дополнительного источника данных с именем сотрудников, который получает данные из таблицы Employees базы данных Northwind Traders Microsoft Access, можно использовать семейства **DataSourceObjects** для задания ссылки на **DataObject** Объект, представляющий извлеченные данные. 
  
В следующем примере кода свойство доступа интерфейса **DataObjectsCollection** , которое возвращает ссылку на объект **DataSourceObject** передается имя дополнительного источника данных. Данные из дополнительного источника данных отображается в окне сообщения с помощью свойства **DOM** интерфейса **DataSourceObject** для доступа к свойству **xml** DOM XML. 
  
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

Для обработки данных, содержащихся в дополнительного источника данных, используйте свойство **DOM** интерфейса **DataSourceObject** возвращает ссылку на модель XML DOM, содержащий данные. Если у вас есть ссылку на модель XML DOM, можно использовать все его свойства и методы для работы с данными, которые он содержит. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Использование интерфейсов DataAdaptersCollection и DataAdapterObject

Интерфейс [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) доступен через свойство [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) интерфейс **XDocument** . Например при создании дополнительного источника данных с именем сотрудников, который получает данные из таблицы Employees базы данных Northwind Traders Microsoft Access, можно использовать семейства **DataAdapterObjects** для задания ссылки на ** DataAdapterObject** , который представляет подключение к базе данных. 
  
В следующем примере кода имя дополнительного источника данных передается **DataAdaptersCollection**, который в этом случае возвращает ссылку на экземпляр **ADOAdapterObject** , представляющий подключение со значением свойства доступа к данным для базы данных Northwind Microsoft Access. Для правильной работы необходимо явно привести объект, возвращаемых как **ADOAdapterObject**. Свойство [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) интерфейса **ADOAdapterObject** используется для отображения в окне сообщения строки подключения ADO. 
  
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


