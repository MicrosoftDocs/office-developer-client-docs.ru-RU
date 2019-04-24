---
title: Инструкция DROP (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293653"
---
# <a name="drop-statement-microsoft-access-sql"></a>Инструкция DROP (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Удаляет существующую таблицу, процедуру или представление из базы данных либо удаляет существующий индекс из таблицы.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование инструкции DROP или любых инструкций DDL с базами данных с ядрами СУБД, отличными от Microsoft Access. Вместо этого используйте метод DAO **Delete**.

## <a name="syntax"></a>Синтаксис

DROP {TABLE *таблица* | INDEX *индекс* ON *таблица* | PROCEDURE *процедура* | VIEW *представление*}

Инструкция DROP состоит из трех указанных ниже частей.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>таблица</em></p></td>
<td><p>Имя таблицы, которую необходимо удалить, либо таблицы, из которой необходимо удалить индекс.</p></td>
</tr>
<tr class="even">
<td><p><em>процедура</em></p></td>
<td><p>Имя процедуры, которую необходимо удалить.</p></td>
</tr>
<tr class="odd">
<td><p><em>представление</em></p></td>
<td><p>Имя представления, которое необходимо удалить.</p></td>
</tr>
<tr class="even">
<td><p><em>индекс</em></p></td>
<td><p>Имя индекса, который необходимо удалить из <em>таблицы</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Чтобы можно было удалить таблицу или индекс из нее, необходимо сначала закрыть эту таблицу.

Кроме того, для удаления индекса из таблицы можно использовать инструкцию [ALTER TABLE](alter-table-statement-microsoft-access-sql.md).

С помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md) можно создать таблицу, а с помощью инструкции [CREATE INDEX](create-index-statement-microsoft-access-sql.md) или ALTER TABLE — создать индекс. Изменить таблицу можно с помощью инструкции ALTER TABLE.

## <a name="example"></a>Пример

В примере ниже предполагается, что существует гипотетический индекс NewIndex в таблице Employees в базе данных Northwind.

В этом примере показано, как удалить индекс MyIndex из таблицы Employees.

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере показано, как удалить таблицу Employees из базы данных.

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
