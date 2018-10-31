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
ms.openlocfilehash: 7a761fbc6404cf72818271b956bfc63516942d25
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863285"
---
# <a name="update-statement-microsoft-access-sql"></a>Инструкция UPDATE (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Создает запрос на обновление, которое изменяет значения в полях в указанной таблице на основании указанных критериев.

## <a name="syntax"></a>Синтаксис

ОБНОВЛЕНИЕ *таблицы* НАБОР *newvalue* WHERE *критериям*;

Инструкция UPDATE состоит из следующих частей:

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
<td><p><em>table</em></p></td>
<td><p>Имя таблицы, содержащей данные, которые требуется изменить.</p></td>
</tr>
<tr class="even">
<td><p><em>новое значение</em></p></td>
<td><p>Выражение, которое определяет значение для вставки в определенное поле обновляемых записей.</p></td>
</tr>
<tr class="odd">
<td><p><em>критерии</em></p></td>
<td><p>Выражение, которое определяет, какие записи будут обновлены. Обновляются только записи, которые удовлетворяют выражения.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Обновление особенно полезен при изменяемый большое количество записей или когда записи, которые требуется изменить находятся в нескольких таблиц.

В то же время можно изменить несколько полей. В следующем примере увеличивается значения сумма заказа на 10 процентов и значения Доставка на 3 процента для поставщиков в Великобритании:

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- ОБНОВЛЕНИЕ не создает набора результатов. Кроме того после обновления записей с помощью запроса на обновление нельзя отменить операцию. Если вы хотите знать, какие записи будут обновлены, выполните результатов выберите запрос, который использует тем же условиям и затем выполните запрос на обновление.
- Создавать резервные копии данных в любое время. При обновлении неверный записей, их можно восстановить из резервной копии.



## <a name="example"></a>Пример

В этом примере изменяется значений в поле Подчиняется до 5 для всех записей сотрудников, которые в настоящее время имеют значений подчиняется 2.

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
