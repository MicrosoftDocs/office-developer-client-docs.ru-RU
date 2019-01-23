---
title: Инструкция UPDATE (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6a0404c21b308f6e389ee5577cc212763e660774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717232"
---
# <a name="update-statement-microsoft-access-sql"></a>Инструкция UPDATE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает запрос на обновление, который изменяет значения в полях в указанной таблице на основании заданных условий.

## <a name="syntax"></a>Синтаксис

UPDATE *таблица* SET *новое_значение* WHERE *критерии*;

Инструкция UPDATE состоит из трех указанных ниже частей.

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
<td><p>Имя таблицы, содержащей данные, которые необходимо изменить.</p></td>
</tr>
<tr class="even">
<td><p><em>новое_значение</em></p></td>
<td><p>Выражение, указывающее значение, которое необходимо вставить в определенное поле обновляемых записей.</p></td>
</tr>
<tr class="odd">
<td><p><em>критерии</em></p></td>
<td><p>Выражение, определяющее, какие записи необходимо обновить. Будут обновлены только те записи, которые удовлетворяют условиям выражения.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Инструкция UPDATE особенно полезна, когда необходимо изменить большое количество записей либо когда записи, которые необходимо изменить, находятся в нескольких таблицах.

Вы можете изменить одновременно несколько полей. В следующем примере показано, как увеличить значения Order Amount на 10 процентов, а значения Freight на 3 процента для грузоотправителей в Соединенном Королевстве:

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- Инструкция UPDATE не создает результирующее множество. Кроме того, после обновления записи с помощью запроса на обновление вам не удастся отменить эту операцию. Если вам необходимо узнать, какие записи были обновлены, сначала изучите результаты выполнения запроса на выборку, использующего те же критерии, а затем запустите запрос на обновление.
- Всегда храните резервные копии данных. Если вы обновите не те записи, вы сможете восстановить их из резервных копий.



## <a name="example"></a>Пример

В этом примере показано, как изменить значения в поле ReportsTo на 5 для всех записей сотрудников, у которых поле ReportsTo имеет значение 2.

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
