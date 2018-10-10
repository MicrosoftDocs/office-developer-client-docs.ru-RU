---
title: Converting DAO Code to ADO
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479780"
---
# <a name="converting-dao-code-to-ado"></a>Converting DAO Code to ADO

**Применимо к**: Access 2013 | Office 2013

> [!NOTE]
> Версии библиотеки DAO перед 3.6 не предоставляются и не поддерживаются в клиенте.

## <a name="dao-to-ado-object-map"></a>DAO карту объект ADO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO(ADODB)</strong></p></th>
<th><p><strong>Примечание</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Отсутствует</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Рабочая область</p></td>
<td><p>Отсутствует</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>База данных</p></td>
<td><p>Подключение</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Набор записей</p></td>
<td><p>Набор записей</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Добавляющий</p></td>
<td><p>Набор ключей</p></td>
<td><p>Получает набор указатели на записей в наборе</p></td>
</tr>
<tr class="even">
<td><p>Тип моментальных снимков</p></td>
<td><p>Статическое</p></td>
<td><p>Оба Получение полного записей, но могут быть обновлены статического набора записей.</p></td>
</tr>
<tr class="odd">
<td><p>Тип таблицы</p></td>
<td><p>Набор ключей с adCmdTableDirect параметр</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Поле</p></td>
<td><p>Поле</p></td>
<td><p>Если в наборе записей</p></td>
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
> Перемещение фокуса из текущей записи через **MoveNext, MoveLast, MoveFirst, MovePrevious** без использования метода **CancelUpdate** неявного выполнения метода **Update** .

### <a name="about-the-contributors"></a>О участники

**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества. UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.

- [Выбор между DAO и ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



