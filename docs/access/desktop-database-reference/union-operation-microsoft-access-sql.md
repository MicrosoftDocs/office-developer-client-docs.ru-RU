---
title: Операции ОБЪЕДИНЕНИЯ (Microsoft Access SQL)
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
ms.openlocfilehash: ed31f0105d8381667e1398fc5d91577d40998d81
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998821"
---
# <a name="union-operation-microsoft-access-sql"></a>Операции ОБЪЕДИНЕНИЯ (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Создает запрос на объединение, который объединяет результаты двух или более независимых запросов или таблиц.

## <a name="syntax"></a>Синтаксис

\[В ТАБЛИЦЕ\] *query1* ОБЪЕДИНЕНИЕ \[все\] \[в ТАБЛИЦЕ\] *query2* \[ОБЪЕДИНЕНИЕ \[все\] \[в ТАБЛИЦЕ\] *queryn* \[ ... \]\]

Операции ОБЪЕДИНЕНИЯ состоит из следующих частей:

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
<td><p><em>Query1 n</em></p></td>
<td><p>Инструкция SELECT, имя сохраненного запроса или имя сохраненной таблицы стоять ключевое слово в ТАБЛИЦЕ.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Можно объединить результаты двух или более запросов, таблиц и инструкций SELECT в любое сочетание за одну операцию ОБЪЕДИНЕНИЯ. В следующем примере объединяются существующей таблицы с именем инструкции SELECT и новых учетных записей:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

По умолчанию повторяющиеся записи не возвращаются при использовании операции ОБЪЕДИНЕНИЯ; Тем не менее можно включить [все](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) предикат, чтобы убедиться, что возвращаются все записи. Это также делает время выполнения запроса.

Все запросы в операции ОБЪЕДИНЕНИЯ необходимо запросить такое же число полей; Тем не менее поля не должны иметь одинаковый размер или тип данных.

Используйте псевдонимы только в первой инструкции SELECT, так как они обрабатываются в любые другие пользователи. В предложение ORDER BY ссылаться на поля, как они называются в первом операторе SELECT.

> [!NOTE]
> - Предложение [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) в каждый аргумент *запроса* можно использовать для группировки возвращаемые данные.
> - Предложение [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) в конце последний аргумент *запроса* можно использовать для отображения возвращаемых данных в указанном порядке.

## <a name="example"></a>Пример

В этом примере показано получение имен и городов из всех поставщиков и клиентов в Бразилии. Он вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.

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
