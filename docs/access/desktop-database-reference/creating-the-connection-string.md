---
title: Создание строки подключения
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295329"
---
# <a name="creating-the-connection-string"></a>Создание строки подключения

**Область применения**: Access 2013, Office 2013

ADO напрямую поддерживает пять аргументов в строке подключения. Другие аргументы передаются поставщику, указанному в аргументе *Поставщик*, без какой-либо обработки ADO.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Поставщик</em></p></td>
<td><p>Задает имя поставщика, чтобы использовать для подключения.</p></td>
</tr>
<tr class="even">
<td><p><em>Имя файла</em></p></td>
<td><p>Указывает имя файла, соответствующего поставщику (например, исходный объект сохраненных данных), содержащий предварительно заданные сведения о подключении.</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em></p></td>
<td><p>Указывает строку подключения как абсолютный URL-адрес, определяющий ресурс, например файл или папку.</p></td>
</tr>
<tr class="even">
<td><p><em>Удаленный поставщик</em></p></td>
<td><p>Задает имя поставщика, которое будет использоваться при открытии подключения на стороне клиента. (Только для службы удаленных данных.)</p></td>
</tr>
<tr class="odd">
<td><p><em>Удаленный сервер</em></p></td>
<td><p>Указывает путь к серверу, который будет использоваться при открытии подключения на стороне клиента. (Только для службы удаленных данных.)</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> В следующих примерах и в руководстве программиста по ADO идентификатор пользователя "MyId" с паролем "123aBc" используется для проверки подлинности на сервере. Необходимо заменить эти значения действительными учетными данными для входа на сервер. Кроме того, замените имя вашего сервера на "Мисклсервер".

Приложение HelloData в главе 1 использовало следующую строку подключения:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

Единственным параметром ADO, указанным в этой строке подключения, является "Provider = SQLOLEDB", который указал поставщика Microsoft OLE DB для SQL Server. Другие допустимые параметры, которые можно передать в строке подключения, могут определяться с помощью ссылки на документацию отдельных поставщиков. В соответствии с документацией поставщика OLE DB для SQL Server можно заменить значение "Server" для параметра *источника данных* и "Database" для начального параметра *каталога* . Таким образом, следующая строка подключения будет давать результаты, идентичные первому:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

Чтобы открыть подключение, просто передайте строку подключения в качестве первого аргумента метода **Open** объекта **Connection** :

```vb 
 
objConn.Open m_sConnStr 
```

Также можно указать большую часть подобных сведений, задав свойства объекта **Connection** перед открытием подключения. Например, вы можете добиться того же результата, что и в строке подключения, с помощью следующего кода:

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

