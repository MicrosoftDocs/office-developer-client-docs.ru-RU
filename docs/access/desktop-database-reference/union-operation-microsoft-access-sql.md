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
ms.openlocfilehash: 14e23b0df5344048fb510d8813a6e1bc2b9e1978
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026031"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="d741e-102">Операции ОБЪЕДИНЕНИЯ (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="d741e-102">UNION operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="d741e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d741e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d741e-104">Создает запрос на объединение, который объединяет результаты двух или более независимых запросов или таблиц.</span><span class="sxs-lookup"><span data-stu-id="d741e-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="d741e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d741e-105">Syntax</span></span>

<span data-ttu-id="d741e-106">\[В ТАБЛИЦЕ\] *query1* ОБЪЕДИНЕНИЕ \[все\] \[в ТАБЛИЦЕ\] *query2* \[ОБЪЕДИНЕНИЕ \[все\] \[в ТАБЛИЦЕ\] *queryn* \[ ...</span><span class="sxs-lookup"><span data-stu-id="d741e-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="d741e-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="d741e-107"></span></span>

<span data-ttu-id="d741e-108">Операции ОБЪЕДИНЕНИЯ состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="d741e-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d741e-109">Часть</span><span class="sxs-lookup"><span data-stu-id="d741e-109">Part</span></span></p></th>
<th><p><span data-ttu-id="d741e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d741e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d741e-111"><em>Query1 n</em></span><span class="sxs-lookup"><span data-stu-id="d741e-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="d741e-112">Инструкция SELECT, имя сохраненного запроса или имя сохраненной таблицы стоять ключевое слово в ТАБЛИЦЕ.</span><span class="sxs-lookup"><span data-stu-id="d741e-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d741e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="d741e-113">Remarks</span></span>

<span data-ttu-id="d741e-114">Можно объединить результаты двух или более запросов, таблиц и инструкций SELECT в любое сочетание за одну операцию ОБЪЕДИНЕНИЯ.</span><span class="sxs-lookup"><span data-stu-id="d741e-114">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation.</span></span> <span data-ttu-id="d741e-115">В следующем примере объединяются существующей таблицы с именем инструкции SELECT и новых учетных записей:</span><span class="sxs-lookup"><span data-stu-id="d741e-115">The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="d741e-116">По умолчанию повторяющиеся записи не возвращаются при использовании операции ОБЪЕДИНЕНИЯ; Тем не менее можно включить [все](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) предикат, чтобы убедиться, что возвращаются все записи.</span><span class="sxs-lookup"><span data-stu-id="d741e-116">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned.</span></span> <span data-ttu-id="d741e-117">Это также делает время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="d741e-117">This also makes the query run faster.</span></span>

<span data-ttu-id="d741e-118">Все запросы в операции ОБЪЕДИНЕНИЯ необходимо запросить такое же число полей; Тем не менее поля не должны иметь одинаковый размер или тип данных.</span><span class="sxs-lookup"><span data-stu-id="d741e-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="d741e-119">Используйте псевдонимы только в первой инструкции SELECT, так как они обрабатываются в любые другие пользователи.</span><span class="sxs-lookup"><span data-stu-id="d741e-119">Use aliases only in the first SELECT statement because they are ignored in any others.</span></span> <span data-ttu-id="d741e-120">В предложение ORDER BY ссылаться на поля, как они называются в первом операторе SELECT.</span><span class="sxs-lookup"><span data-stu-id="d741e-120">In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="d741e-121">Предложение [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) в каждый аргумент *запроса* можно использовать для группировки возвращаемые данные.</span><span class="sxs-lookup"><span data-stu-id="d741e-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="d741e-122">Предложение [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) в конце последний аргумент *запроса* можно использовать для отображения возвращаемых данных в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="d741e-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="d741e-123">Пример</span><span class="sxs-lookup"><span data-stu-id="d741e-123">Example</span></span>

<span data-ttu-id="d741e-124">В этом примере показано получение имен и городов из всех поставщиков и клиентов в Бразилии.</span><span class="sxs-lookup"><span data-stu-id="d741e-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="d741e-125">Он вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="d741e-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
