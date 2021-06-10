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

Приложение Адресная книга использует [RDS. Объект DataControl](datacontrol-object-rds.md) для привязки данных из SQL Server базы данных к визуальному объекту (в данном случае таблице DHTML) на странице HTML клиента приложения. В логике программы VBScript, управляемой событиями, используется [RDS. DataControl:](datacontrol-object-rds.md)

  - Запрос базы данных, отправка обновлений в базу данных и обновление сетки данных.

  - Разрешить пользователям перейти к первой, следующей, предыдущей или последней записи в сетке данных.

Следующий код определяет **RDS. Компонент DataControl:**

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

Тег OBJECT определяет **RDS. Компонент DataControl** в программе. Тег содержит два типа параметров:

  - Те, которые связаны с общим тегом OBJECT.

  - Те, которые специфиальна **для RDS. Объект DataControl.**

## <a name="generic-object-tag-parameters"></a>Общие параметры тегов ОБЪЕКТА

В следующей таблице описываются параметры, связанные с тегом OBJECT.

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
<td><p>Уникальный 128-битный номер, который определяет тип встроенного объекта в систему. Этот идентификатор поддерживается в реестре системы локального компьютера. (Для классового IDs <strong>RDS. Объект DataControl</strong> см. в <a href="datacontrol-object-rds.md">RDS. Объект DataControl.)</a></p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>Определяет идентификатор для встроенного объекта, используемого для его идентификации в коде.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>RDS. Параметры тегов DataControl

В следующей таблице описываются параметры, определенные **RDS. Объект DataControl.** (Полный список **RDS. Параметры объектов DataControl** и их реализация см. в [RDS. Объект DataControl.)](datacontrol-object-rds.md)

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
<td><p><a href="server-property-rds.md">SERVER</a></p></td>
<td><p>Если вы используете HTTP, значение — это имя серверного компьютера, предшествующего https://.</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">CONNECT</a></p></td>
<td><p>Предоставляет необходимые сведения о подключении для <strong>RDS. DataControl</strong> для подключения к SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p>Задает или возвращает строку запроса, используемую для получения <a href="recordset-object-ado.md">набора записей.</a></p></td>
</tr>
</tbody>
</table>

