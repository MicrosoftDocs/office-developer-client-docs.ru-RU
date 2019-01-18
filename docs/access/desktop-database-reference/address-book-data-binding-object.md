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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704303"
---
# <a name="address-book-data-binding-object"></a>Объект привязки к данным адресной книги


**Применимо к**: Access 2013, Office 2013

Приложение адресной книги использует [RDS. DataControl](datacontrol-object-rds.md) объект привязки данных из базы данных SQL Server к визуального объекта (в данном случае таблице DHTML) на странице HTML клиентского приложения. Логика программы VBScript событиями использует [RDS. DataControl](datacontrol-object-rds.md) для:

  - Запрос к базе данных, отправки обновлений в базу данных и обновить данные.

  - Разрешить пользователям перемещение к первому, затем предыдущий, или последней записи в таблице данных.

В следующем коде определяется **RDS. DataControl** компонента:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

Тег ОБЪЕКТА определяет **RDS. DataControl** компонента в программе. Тег включает два типа параметров:

  - Те, связанные с универсальный тег OBJECT.

  - Те, относящиеся к **RDS. DataControl** объекта.

## <a name="generic-object-tag-parameters"></a>Универсальный объект тег параметров

В следующей таблице описаны параметры, связанные с тег OBJECT.

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
<td><p><strong><em>CLASSID</em></strong></p></td>
<td><p>Уникальный, 128-бит номер, идентифицирующий тип внедренный объект в систему. Этот идентификатор сохраняется в локальном компьютере системного реестра. (Для класса идентификаторы <strong>RDS. DataControl</strong> , см <a href="datacontrol-object-rds.md">RDS. Объект DataControl</a>.)</p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>Определяет идентификатор уровня документов для внедренный объект, используемый для идентификации в коде.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>RDS. Параметры DataControl тег

В следующей таблице описаны параметры, относящиеся к **RDS. DataControl** объекта. (Чтобы получить полный список **RDS. DataControl** параметров объекта и способы их реализации, см [RDS. Объект DataControl](datacontrol-object-rds.md).)

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
<td><p>При использовании HTTP значение — это имя компьютера сервера, префикс https://.</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">ПОДКЛЮЧЕНИЕ</a></p></td>
<td><p>Предоставляет сведения о подключении, необходимые для <strong>RDS. DataControl</strong> для подключения к SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p>Задает или возвращает строку запроса, используемое для извлечения <a href="recordset-object-ado.md">записей</a>.</p></td>
</tr>
</tbody>
</table>

