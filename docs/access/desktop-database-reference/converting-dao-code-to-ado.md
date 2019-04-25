---
title: Преобразование кода DAO в ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295522"
---
# <a name="convert-dao-code-to-ado"></a>Преобразование кода DAO в ADO

**Область применения**: Access 2013, Office 2013

> [!NOTE]
> Библиотеки DAO до версии 3.6 не предоставляются и не поддерживаются в Access.

## <a name="dao-to-ado-object-map"></a>Сопоставление объектов DAO с ADO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO (ADODB)</strong></p></th>
<th><p><strong>Примечание</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Нет</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>Нет</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Database</p></td>
<td><p>Connection</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Recordset</p></td>
<td><p>Recordset</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Тип "Динамический набор"</p></td>
<td><p>Keyset</p></td>
<td><p>Извлекает набор указателей на записи в наборе записей.</p></td>
</tr>
<tr class="even">
<td><p>Тип "Статический набор"</p></td>
<td><p>Static</p></td>
<td><p>Оба извлекают полные записи, но набор записей Static можно обновлять.</p></td>
</tr>
<tr class="odd">
<td><p>Табличный тип</p></td>
<td><p>Keyset с параметром adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>При ссылке на набор записей.</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Открытие набора записей

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Изменение набора записей

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Открытие набора записей

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Изменение набора записей

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> Перемещение фокуса с текущей записи с помощью методов **MoveNext, MoveLast, MoveFirst, MovePrevious** без предварительного использования метода **CancelUpdate** неявно запускает метод **Update**.

### <a name="about-the-contributors"></a>Об участниках

**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com). UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.

- [Выбор между DAO и ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

