---
title: SELECT.INTO Statement (Microsoft Access SQL)
TOCTitle: SELECT.INTO Statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4122421642b9746b5832984bf784faf65c603fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480338"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="8593d-102">SELECT.INTO Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8593d-102">SELECT.INTO Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="8593d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8593d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8593d-104">Создает запрос на создание таблицы.</span><span class="sxs-lookup"><span data-stu-id="8593d-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="8593d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8593d-105">Syntax</span></span>

<span data-ttu-id="8593d-106">Выбор *field1*\[, *поле2*\[,... \] \] В *новой_таблицы* \[в *внешняя_база_данных* \] из *источника*</span><span class="sxs-lookup"><span data-stu-id="8593d-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="8593d-107">Выбор... В оператор состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="8593d-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8593d-108">Часть</span><span class="sxs-lookup"><span data-stu-id="8593d-108">Part</span></span></p></th>
<th><p><span data-ttu-id="8593d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8593d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8593d-110"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="8593d-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="8593d-111">Имя поля, которые копируются в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="8593d-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8593d-112"><em>новой_таблицы</em></span><span class="sxs-lookup"><span data-stu-id="8593d-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="8593d-113">Имя таблицы будет создан.</span><span class="sxs-lookup"><span data-stu-id="8593d-113">The name of the table to be created.</span></span> <span data-ttu-id="8593d-114">Он должен соответствовать типу стандартным соглашениям об именах.</span><span class="sxs-lookup"><span data-stu-id="8593d-114">It must conform to standard naming conventions.</span></span> <span data-ttu-id="8593d-115">Если <em>новой_таблицы</em> совпадает с именем существующей таблицы, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8593d-115">If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8593d-116"><em>внешняя_база_данных</em></span><span class="sxs-lookup"><span data-stu-id="8593d-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="8593d-117">Путь к внешней базе данных.</span><span class="sxs-lookup"><span data-stu-id="8593d-117">The path to an external database.</span></span> <span data-ttu-id="8593d-118">Описание пути в разделе <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">в</a> предложение.</span><span class="sxs-lookup"><span data-stu-id="8593d-118">For a description of the path, see the <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8593d-119"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="8593d-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="8593d-120">Имя существующей таблицы, из которой будут выбраны записи.</span><span class="sxs-lookup"><span data-stu-id="8593d-120">The name of the existing table from which records are selected.</span></span> <span data-ttu-id="8593d-121">Это может быть одной или нескольких таблиц или запроса.</span><span class="sxs-lookup"><span data-stu-id="8593d-121">This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8593d-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="8593d-122">Remarks</span></span>

<span data-ttu-id="8593d-123">Запросы на создание таблиц можно использовать для архивации записей, создания резервных копий таблиц или создания копий для экспорта в другую базу данных или для использования в качестве основы для отчетов, отображающих данные за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="8593d-123">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period.</span></span> <span data-ttu-id="8593d-124">Например можно создать ежемесячные продажи региона отчета с помощью одного запроса создание таблицы каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="8593d-124">For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="8593d-125">Можно определить первичный ключ для новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="8593d-125">You may want to define a primary key for the new table.</span></span> <span data-ttu-id="8593d-126">При создании таблицы поля в новую таблицу наследование типа данных и поля размера каждое поле в таблицах запроса, но не другие поля или свойства таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="8593d-126">When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span></P>
> <LI>
> <P><span data-ttu-id="8593d-127">Добавление данных в существующую таблицу, используйте оператор <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A> для создания запроса на добавление.</span><span class="sxs-lookup"><span data-stu-id="8593d-127">To add data to an existing table, use the <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A> statement instead to create an append query.</span></span></P>
> <LI>
> <P><span data-ttu-id="8593d-128">Чтобы узнать, какие записи будет установлен и перед запуском создание таблицы, сначала проверьте результаты <A href="select-statement-microsoft-access-sql.md">ВЫБЕРИТЕ</A> оператор, который использует же критерии выбора.</span><span class="sxs-lookup"><span data-stu-id="8593d-128">To find out which records will be selected before you run the make-table query, first examine the results of a <A href="select-statement-microsoft-access-sql.md">SELECT</A> statement that uses the same selection criteria.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="8593d-129">Пример</span><span class="sxs-lookup"><span data-stu-id="8593d-129">Example</span></span>

<span data-ttu-id="8593d-130">В этом примере выбирает все записи в таблице сотрудников и копирует их в новую таблицу с именем экстренного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8593d-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
