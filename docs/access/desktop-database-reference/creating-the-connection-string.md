---
title: Creating the Connection String
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8420beb2c6136123c334a55b68bd6601f214faa5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483014"
---
# <a name="creating-the-connection-string"></a>Creating the Connection String


**Применимо к**: Access 2013 | Office 2013

ADO поддерживает пять аргументов в строке подключения. Другие аргументы передаются поставщика с именем в аргументе *поставщика* без какой-либо обработки с ADO.

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
<td><p>Задает имя поставщика, который используется для подключения.</p></td>
</tr>
<tr class="even">
<td><p><em>Имя файла</em></p></td>
<td><p>Указывает имя файла от поставщика (например, объект источника постоянных данных), содержащий сведения о подключении к предварительно.</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em>.</p></td>
<td><p>Указывает строку подключения, как абсолютный URL-адрес, идентифицирующий ресурс, такой как файл или папку.</p></td>
</tr>
<tr class="even">
<td><p><em>Удаленный поставщик</em></p></td>
<td><p>Задает имя поставщика для использования при открытии подключения со стороны клиента. (Служба удаленных данных только.)</p></td>
</tr>
<tr class="odd">
<td><p><em>Удаленный сервер</em></p></td>
<td><p>Задает имя пути сервера, который будет использоваться при открытии подключения со стороны клиента. (Служба удаленных данных только.)</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>В следующих примерах и во всем Руководство программиста ADO идентификатор пользователя «Мой_идентификатор» пароль «123aBc» используется для проверки подлинности на сервере. Необходимо заменить эти значения с действительные учетные данные для сервера. Кроме того замените имя сервера для «MySqlServer».</P>



В приложении HelloData в раздел 1 используется следующая строка подключения:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

Единственный параметр ADO, предоставленные в этой строке подключения был «поставщика = SQLOLEDB», который указан поставщик Microsoft OLE DB для SQL Server. Другие допустимые параметры, которые могут быть переданы в строке подключения можно определить, обратившись к документации отдельные поставщики. В соответствии с поставщика OLE DB для документации по SQL Server можно заменить «Сервер» для параметра *Источник данных* и «База данных» для параметра *Initial Catalog* . Таким образом следующая строка подключения может привести к результатам совпадает с первым:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

Для открытия подключения, просто передайте строку подключения в качестве первого аргумента в метод **Open** объекта **подключения** :

```vb 
 
objConn.Open m_sConnStr 
```

Можно также предоставить большую часть этих сведений путем установки свойства объекта **подключения** перед открытием подключения. Например можно получить же эффект, что строка подключения выше, с помощью следующего кода:

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```
