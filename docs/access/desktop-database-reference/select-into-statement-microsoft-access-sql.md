---
title: Инструкция SELECT.INTO (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308724"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="4aa4b-102">Инструкция SELECT.INTO (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4aa4b-102">SELECT.INTO Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4aa4b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4aa4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4aa4b-104">Создает запрос на создание таблицы.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aa4b-105">Syntax</span></span>

<span data-ttu-id="4aa4b-106">SELECT *поле1*\[, *поле2*\[, …\]\] INTO *новая_таблица* \[IN *внешняя_база_данных*\] FROM *источник*</span><span class="sxs-lookup"><span data-stu-id="4aa4b-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="4aa4b-107">Инструкция SELECT...INTO состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="4aa4b-107">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4aa4b-108">Часть</span><span class="sxs-lookup"><span data-stu-id="4aa4b-108">Part</span></span></p></th>
<th><p><span data-ttu-id="4aa4b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4aa4b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4aa4b-110"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="4aa4b-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="4aa4b-111">Имена полей, которые требуется скопировать в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4aa4b-112"><em>новая_таблица</em></span><span class="sxs-lookup"><span data-stu-id="4aa4b-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="4aa4b-113">Имя таблицы, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-113">The name of the constraint to be created.</span></span> <span data-ttu-id="4aa4b-114">Необходимо соблюдать стандартные соглашения об именовании.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-114">It must follow standard naming conventions.</span></span> <span data-ttu-id="4aa4b-115">При совпадении имен <em>новой_таблицы</em> и существующей таблицы возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-115">If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4aa4b-116"><em>внешняя_база_данных</em></span><span class="sxs-lookup"><span data-stu-id="4aa4b-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="4aa4b-117">Путь к внешней базе данных.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-117">The path to an external database.</span></span> <span data-ttu-id="4aa4b-118">Описание пути см. в статье, посвященной предложению <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-118">For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4aa4b-119"><em>источник</em></span><span class="sxs-lookup"><span data-stu-id="4aa4b-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="4aa4b-120">Имя существующей таблицы, из которой отбираются записи.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-120">The name of the table containing the fields from which records are selected.</span></span> <span data-ttu-id="4aa4b-121">Источником может быть одна или несколько таблиц, а также запрос.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-121">This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4aa4b-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="4aa4b-122">Remarks</span></span>

<span data-ttu-id="4aa4b-123">Запросы на создание таблиц можно использовать для архивации записей, для создания резервных копий таблиц, а также для создания копий с целью экспорта в другую базу данных или формирования отчетов, отображающих данные за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-123">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period.</span></span> <span data-ttu-id="4aa4b-124">Например, отчет "Ежемесячные продажи по регионам" можно составлять, выполняя каждый месяц один и тот же запрос на создание таблиц.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-124">For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="4aa4b-125">Может возникнуть необходимость определить первичный ключ для новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-125">You may want to define a primary key for the new table.</span></span> <span data-ttu-id="4aa4b-126">При создании таблицы ее поля наследуют тип данных и размеры полей базовых таблиц запроса. Другие параметры полей не переносятся.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-126">When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="4aa4b-127">Чтобы добавить данные в таблицу, используйте вместо запроса на добавление инструкцию [INSERT INTO](insert-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="4aa4b-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="4aa4b-128">Чтобы определить, какие записи будут отобраны, до выполнения запроса на создание таблицы, сначала проверьте результат инструкции [SELECT](select-statement-microsoft-access-sql.md) с такими же условиями отбора.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="4aa4b-129">Пример</span><span class="sxs-lookup"><span data-stu-id="4aa4b-129">Example</span></span>

<span data-ttu-id="4aa4b-130">В этом примере отбираются все записи в таблице Employees, которые копируются в новую таблицу Emp Backup.</span><span class="sxs-lookup"><span data-stu-id="4aa4b-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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
