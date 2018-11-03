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
ms.openlocfilehash: 1a61512c58ccbde82072fa4d8105c82b9f145ebc
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937423"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="4f274-102">Операции ОБЪЕДИНЕНИЯ (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4f274-102">UNION operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="4f274-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f274-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f274-104">Создает запрос на объединение, который объединяет результаты двух или более независимых запросов или таблиц.</span><span class="sxs-lookup"><span data-stu-id="4f274-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f274-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f274-105">Syntax</span></span>

<span data-ttu-id="4f274-106">\[В ТАБЛИЦЕ\] *query1* ОБЪЕДИНЕНИЕ \[все\] \[в ТАБЛИЦЕ\] *query2* \[ОБЪЕДИНЕНИЕ \[все\] \[в ТАБЛИЦЕ\] *queryn* \[ ...</span><span class="sxs-lookup"><span data-stu-id="4f274-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="4f274-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="4f274-107"></span></span>

<span data-ttu-id="4f274-108">Операции ОБЪЕДИНЕНИЯ состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="4f274-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f274-109">Часть</span><span class="sxs-lookup"><span data-stu-id="4f274-109">Part</span></span></p></th>
<th><p><span data-ttu-id="4f274-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4f274-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f274-111"><em>Query1 n</em></span><span class="sxs-lookup"><span data-stu-id="4f274-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="4f274-112">Инструкция SELECT, имя сохраненного запроса или имя сохраненной таблицы стоять ключевое слово в ТАБЛИЦЕ.</span><span class="sxs-lookup"><span data-stu-id="4f274-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4f274-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f274-113">Remarks</span></span>

<span data-ttu-id="4f274-114">Можно объединить результаты двух или более запросов, таблиц и инструкций SELECT в любое сочетание за одну операцию ОБЪЕДИНЕНИЯ.</span><span class="sxs-lookup"><span data-stu-id="4f274-114">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation.</span></span> <span data-ttu-id="4f274-115">В следующем примере объединяются существующей таблицы с именем инструкции SELECT и новых учетных записей:</span><span class="sxs-lookup"><span data-stu-id="4f274-115">The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="4f274-116">По умолчанию повторяющиеся записи не возвращаются при использовании операции ОБЪЕДИНЕНИЯ; Тем не менее можно включить [все](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) предикат, чтобы убедиться, что возвращаются все записи.</span><span class="sxs-lookup"><span data-stu-id="4f274-116">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to ensure that all records are returned.</span></span> <span data-ttu-id="4f274-117">Это также делает время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="4f274-117">This also makes the query run faster.</span></span>

<span data-ttu-id="4f274-118">Все запросы в операции ОБЪЕДИНЕНИЯ необходимо запросить такое же число полей; Тем не менее поля не должны иметь одинаковый размер или тип данных.</span><span class="sxs-lookup"><span data-stu-id="4f274-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="4f274-119">Используйте псевдонимы только в первой инструкции SELECT, так как они обрабатываются в любые другие пользователи.</span><span class="sxs-lookup"><span data-stu-id="4f274-119">Use aliases only in the first SELECT statement because they are ignored in any others.</span></span> <span data-ttu-id="4f274-120">В предложение ORDER BY ссылаться на поля, как они называются в первом операторе SELECT.</span><span class="sxs-lookup"><span data-stu-id="4f274-120">In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="4f274-121">Предложение <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> или <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> в каждый аргумент <EM>запроса</EM> можно использовать для группировки возвращаемые данные.</span><span class="sxs-lookup"><span data-stu-id="4f274-121">You can use a <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> or <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> clause in each <EM>query</EM> argument to group the returned data.</span></span></P>
> <LI>
> <P><span data-ttu-id="4f274-122">Предложение <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> в конце последний аргумент <EM>запроса</EM> можно использовать для отображения возвращаемых данных в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="4f274-122">You can use an <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> clause at the end of the last <EM>query</EM> argument to display the returned data in a specified order.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="4f274-123">Пример</span><span class="sxs-lookup"><span data-stu-id="4f274-123">Example</span></span>

<span data-ttu-id="4f274-124">В этом примере показано получение имен и городов из всех поставщиков и клиентов в Бразилии.</span><span class="sxs-lookup"><span data-stu-id="4f274-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="4f274-125">Он вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="4f274-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
