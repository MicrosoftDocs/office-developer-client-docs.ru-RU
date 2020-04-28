---
title: Объект привязки к данным адресной книги
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fb5302d1c2b8e4eebb6dbe1a5906459834b8e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281869"
---
# <a name="address-book-data-binding-object"></a>Объект привязки к данным адресной книги


**Область применения**: Access 2013, Office 2013

Приложение адресной книги использует [RDS. Объект элемента управления](datacontrol-object-rds.md) данными для привязывания данных из базы данных SQL Server к визуальному объекту (в данном случае — таблице DHTML) на HTML-странице клиента приложения. Логика программы VBScript, основанной на событиях, использует [RDS. Элемент управления](datacontrol-object-rds.md) для:

  - Запросите базу данных, отправьте обновления в базу данных и обновите сетку данных.

  - Разрешить пользователям переходить к первой, следующей, предыдущей или последней записи в сетке данных.

В приведенном ниже коде определяется **RDS. Компонент управления** элементом:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

Тег OBJECT определяет **ActiveX RDS. Компонент элемента управления** "компонент" в программе. Тег включает два типа параметров:

  - Связанные с тегом универсального объекта.

  - Характерные для **RDS. Объект управления** DataObject.

## <a name="generic-object-tag-parameters"></a>Параметры тега универсального объекта

В следующей таблице описываются параметры, связанные с тегом объекта.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><em>КЛАССА</em></strong></p></td>
<td><p>Уникальный 128 разрядного числа, определяющего тип внедренного объекта в системе. Этот идентификатор сохраняется в системном реестре локального компьютера. (Идентификаторы класса <strong>RDS. Объект управления</strong> элементом, можно узнать в статье <a href="datacontrol-object-rds.md">RDS. Объект управления</a>элементом.)</p></td>
</tr>
<tr class="even">
<td><p><strong><em>Идентификатор</em></strong></p></td>
<td><p>Определяет идентификатор для внедренного объекта, который используется для определения кода на уровне документа.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>Рабочих. Параметры тега элемента управления "элемент управления"

В следующей таблице описываются параметры, характерные для **RDS. Объект управления** DataObject. (Полный список элементов **ActiveX RDS. Параметры объекта,** а когда их можно реализовать, ознакомьтесь с разрядом с [RDS. Объект управления](datacontrol-object-rds.md)элементом.)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="server-property-rds.md">СЕРВЕР</a></p></td>
<td><p>При использовании протокола HTTP значением является имя компьютера сервера, которому предшествует https://.</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">CONNECT</a></p></td>
<td><p>Предоставляет необходимые сведения о подключении для <strong>RDS. Элемент управления</strong> для подключения к SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p>Задает или возвращает строку запроса, используемую для получения объекта <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
</tbody>
</table>

