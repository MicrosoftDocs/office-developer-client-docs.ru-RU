---
title: UNION Operation (Microsoft Access SQL)
TOCTitle: UNION Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 63ff883f35dabbbd69e1bf144eb32016f303c7ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879111"
---
# <a name="union-operation-microsoft-access-sql"></a>UNION Operation (Microsoft Access SQL)


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


## <a name="remarks"></a>Замечания

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
> <UL>
> <LI>
> <P>Предложение <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> или <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> в каждый аргумент <EM>запроса</EM> можно использовать для группировки возвращаемые данные.</P>
> <LI>
> <P>Предложение <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> в конце последний аргумент <EM>запроса</EM> можно использовать для отображения возвращаемых данных в указанном порядке.</P></LI></UL>



## <a name="example"></a>Пример

В этом примере показано получение имен и городов из всех поставщиков и клиентов в Бразилии.

В этом примере вызывается процедура EnumFields, которые можно найти в примере инструкции SELECT.

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
