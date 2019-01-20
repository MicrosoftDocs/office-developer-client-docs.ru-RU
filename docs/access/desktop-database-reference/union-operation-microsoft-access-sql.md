---
title: Операция UNION (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716252"
---
# <a name="union-operation-microsoft-access-sql"></a>Операция UNION (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает запрос на объединение, выполняющий объединение результатов двух или более независимых запросов или таблиц.

## <a name="syntax"></a>Синтаксис

\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ … \]\]

Операция UNION состоит из следующих частей:

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
<td><p><em>query1-n</em></p></td>
<td><p>Оператор SELECT, имя сохраненного запроса или имя сохраненной таблицы с предшествующим ключевым словом TABLE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Вы можно выполнить слияние результатов двух или более запросов, таблиц и операторов SELECT в любой последовательности в одной операции UNION. В приведенном ниже примере выполняется объединение существующей таблицы с именем New Accounts и оператора SELECT:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

По умолчанию не возвращаются повторяющиеся записи при использовании операции UNION; тем не менее, вы можете включить предикат [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql), чтобы гарантировать, что будут возвращаться все записи. Это также сокращает время выполнения запроса.

Все запросы в операции UNION должны запрашивать одинаковое количество полей; тем не менее, поля не должны иметь одинаковый размер или тип данных.

Используйте псевдонимы только в первой инструкции SELECT, так как они не учитываются во всех остальных. В предложении ORDER BY необходимо ссылаться на поля так, как они называются в первом операторе SELECT.

> [!NOTE]
> - Вы можете использовать предложения [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) в каждом аргументе *запроса*, чтобы сгруппировать возвращаемые данные.
> - Вы можете использовать предложение [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) в конце последнего аргумента*запроса* для отображения возвращаемых данных в указанном порядке.

## <a name="example"></a>Пример

В этом примере показано получение названий и городов всех поставщиков и клиентов в Бразилии. В этом примере выполняется вызов процедуры EnumFields, который вы можете найти в примере для оператора SELECT.

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
