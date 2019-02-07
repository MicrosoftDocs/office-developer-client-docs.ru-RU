---
title: Предложение CONSTRAINT (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 356620376658bb927c690056f4de9a01554aa47e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703785"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="3a423-102">Предложение CONSTRAINT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3a423-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="3a423-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a423-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a423-104">Ограничение похоже на индекс, несмотря на то, что его можно также использовать для создания связи с другой таблицей.</span><span class="sxs-lookup"><span data-stu-id="3a423-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="3a423-105">Вы можете использовать предложение CONSTRAINT в операторах [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) и [CREATE TABLE](create-table-statement-microsoft-access-sql.md)для создания или удаления ограничений.</span><span class="sxs-lookup"><span data-stu-id="3a423-105">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints.</span></span> <span data-ttu-id="3a423-106">Существует два типа предложений CONSTRAINT: одно для создания ограничения на отдельное поле, а другое — для создания ограничения на несколько полей.</span><span class="sxs-lookup"><span data-stu-id="3a423-106">There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>

> [!NOTE]
> <span data-ttu-id="3a423-107">Ядро СУБД Access не поддерживает использование CONSTRAINT или любые инструкции DDL с базами данных, которые не являются базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3a423-107">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="3a423-108">Используйте вместо этого методы DAO **Create**.</span><span class="sxs-lookup"><span data-stu-id="3a423-108">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a423-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a423-109">Syntax</span></span>

### <a name="single-field-constraint"></a><span data-ttu-id="3a423-110">Ограничения одного поля</span><span class="sxs-lookup"><span data-stu-id="3a423-110">Single-field constraint</span></span>

<span data-ttu-id="3a423-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span><span class="sxs-lookup"><span data-stu-id="3a423-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

### <a name="multiple-field-constraint"></a><span data-ttu-id="3a423-112">Ограничения нескольких полей</span><span class="sxs-lookup"><span data-stu-id="3a423-112">Multiple-field constraint</span></span>

<span data-ttu-id="3a423-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span><span class="sxs-lookup"><span data-stu-id="3a423-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="3a423-114">Предложение CONSTRAINT состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="3a423-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a423-115">Часть</span><span class="sxs-lookup"><span data-stu-id="3a423-115">Part</span></span></p></th>
<th><p><span data-ttu-id="3a423-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3a423-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a423-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="3a423-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-118">Имя ограничения, которое необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="3a423-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a423-119"><em>primary1</em>, <em>primary2</em></span><span class="sxs-lookup"><span data-stu-id="3a423-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-120">Имя поля или полей, которые будут являться первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="3a423-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a423-121"><em>unique1</em>, <em>unique2</em></span><span class="sxs-lookup"><span data-stu-id="3a423-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-122">Имя поля или полей, которые будут являться уникальным ключом.</span><span class="sxs-lookup"><span data-stu-id="3a423-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a423-123"><em>notnull1, notnull2</em></span><span class="sxs-lookup"><span data-stu-id="3a423-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-124">Имя поля или полей, в которых допускаются только значения, отличные от Null.</span><span class="sxs-lookup"><span data-stu-id="3a423-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a423-125"><em>ref1</em>, <em>ref2</em></span><span class="sxs-lookup"><span data-stu-id="3a423-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-126">Имя поля или полей внешнего ключа, который ссылается на поля в другой таблице.</span><span class="sxs-lookup"><span data-stu-id="3a423-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a423-127"><em>foreigntable</em></span><span class="sxs-lookup"><span data-stu-id="3a423-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-128">Имя внешней таблицы, содержащей одно или несколько полей, заданных <em>foreignfield</em>.</span><span class="sxs-lookup"><span data-stu-id="3a423-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a423-129"><em>foreignfield1</em>, <em>foreignfield2</em></span><span class="sxs-lookup"><span data-stu-id="3a423-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="3a423-130">Имя поля или полей в <em>foreigntable</em>, определяемых <em>ref1</em>, <em>ref2</em>.</span><span class="sxs-lookup"><span data-stu-id="3a423-130">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>.</span></span> <span data-ttu-id="3a423-131">Это предложение можно опустить, если поле, на которое ссылаются, представляет собой первичный ключ <em>foreigntable</em>.</span><span class="sxs-lookup"><span data-stu-id="3a423-131">You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3a423-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a423-132">Remarks</span></span>

<span data-ttu-id="3a423-133">Используйте синтаксис для ограничения одного поля в предложении, определяющем поле, инструкции ALTER TABLE или CREATE TABLE непосредственно после спецификации типа данных поля.</span><span class="sxs-lookup"><span data-stu-id="3a423-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="3a423-134">Используйте данный синтаксис для ограничения нескольких полей в случае, когда вы используете зарезервированное слово CONSTRAINT за пределами определяющего поле предложения в операторе ALTER TABLE или CREATE TABLE.</span><span class="sxs-lookup"><span data-stu-id="3a423-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="3a423-135">С помощью CONSTRAINT можно назначить поле в качестве одного из следующих типов ограничений:</span><span class="sxs-lookup"><span data-stu-id="3a423-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="3a423-136">Чтобы указать поле в качестве уникального ключа, можно использовать зарезервированное слово UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="3a423-136">You can use the UNIQUE reserved word to designate a field as a unique key.</span></span> <span data-ttu-id="3a423-137">Это значит, что две записи в таблице не могут иметь одно и то же значение в этом поле.</span><span class="sxs-lookup"><span data-stu-id="3a423-137">This means that no two records in the table can have the same value in this field.</span></span> <span data-ttu-id="3a423-138">Вы можете определить любое поле или поля как уникальные.</span><span class="sxs-lookup"><span data-stu-id="3a423-138">You can constrain any field or list of fields as unique.</span></span> <span data-ttu-id="3a423-139">Если ограничение для нескольких полей используется в качестве уникального ключа, объединенные значения всех полей в индексе должны быть уникальными, даже если несколько записей имеют одинаковое значение в одном из полей.</span><span class="sxs-lookup"><span data-stu-id="3a423-139">If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="3a423-140">С помощью зарезервированного слова PRIMARY KEY можно назначить одно поле или набор полей в таблице в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="3a423-140">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key.</span></span> <span data-ttu-id="3a423-141">Все значения в первичном ключе должны быть уникальными и не быть равными **Null**, а у таблицы может быть только один первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="3a423-141">All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="3a423-142">Не используйте ограничение PRIMARY KEY в таблице, в которой уже есть первичный ключ; если вы сделаете это, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a423-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="3a423-143">С помощью зарезервированного слова FOREIGN KEY можно назначить поле в качестве внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="3a423-143">You can use the FOREIGN KEY reserved words to designate a field as a foreign key.</span></span> <span data-ttu-id="3a423-144">Если первичный ключ внешней таблицы состоит из нескольких полей, необходимо использовать определение ограничения для нескольких полей со списком всех полей со ссылками, имя внешней таблицы и названия полей со ссылками во внешней таблице в том же порядке, в каком перечислены поля со ссылками.</span><span class="sxs-lookup"><span data-stu-id="3a423-144">If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed.</span></span> <span data-ttu-id="3a423-145">Если поле или поля, на которые указывает ссылка, представляют собой первичный ключ внешней таблицы, вы можете их не указывать.</span><span class="sxs-lookup"><span data-stu-id="3a423-145">If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields.</span></span> <span data-ttu-id="3a423-146">Ядро СУБД по умолчанию считает такие поля первичным ключом внешней таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a423-146">By default the database engine behaves as if the foreign table's primary key is the referenced fields.</span></span> <span data-ttu-id="3a423-147">Ограничения внешнего ключа указывают определенные действия, которые необходимо выполнить при изменении соответствующего значения первичного ключа:</span><span class="sxs-lookup"><span data-stu-id="3a423-147">Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="3a423-148">Вы можете указать действия для выполнения для внешней таблицы с учетом соответствующего действия, выполняемого для первичного ключа в таблице, в котором содержится определение CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="3a423-148">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined.</span></span> <span data-ttu-id="3a423-149">Например, допустим, что у таблицы "Клиенты" следующее определение:</span><span class="sxs-lookup"><span data-stu-id="3a423-149">For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="3a423-150">Рассмотрим следующее определение таблицы "Заказы", которое определяет отношение внешнего ключа, ссылающегося на первичный ключ таблицы "Клиенты":</span><span class="sxs-lookup"><span data-stu-id="3a423-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="3a423-151">Предложения ON UPDATE CASCADE и ON DELETE CASCADE определяются для внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="3a423-151">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key.</span></span> <span data-ttu-id="3a423-152">Предложение ON UPDATE CASCADE означает, что если в таблице "Клиенты" обновляется идентификатор клиента (CustId), будет выполняться каскадное обновление таблицы "Заказы".</span><span class="sxs-lookup"><span data-stu-id="3a423-152">The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table.</span></span> <span data-ttu-id="3a423-153">Каждый заказ, содержащий соответствующее значение идентификатора клиента, будет автоматически обновляться новым значением.</span><span class="sxs-lookup"><span data-stu-id="3a423-153">Each order containing a corresponding customer identifier value will be updated automatically with the new value.</span></span> <span data-ttu-id="3a423-154">Предложение ON DELETE CASCADE означает, что если клиент удаляется из таблицы "Клиенты", все строки в таблице "Заказы", содержащие то же значение идентификатора клиента, также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="3a423-154">The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted.</span></span> <span data-ttu-id="3a423-155">Рассмотрим другое определение таблицы "Заказы", в котором вместо действия CASCADE используется SET NULL:</span><span class="sxs-lookup"><span data-stu-id="3a423-155">Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="3a423-156">Предложение ON UPDATE SET NULL означает, что при обновлении идентификатора клиента (CustId) в таблице "Клиенты" для соответствующих значений внешнего ключа из таблицы "Заказы" будет автоматически установлено значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3a423-156">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL.</span></span> <span data-ttu-id="3a423-157">Предложение ON DELETE SET NULL означает, что при удалении клиента из таблицы "Клиенты" для всех соответствующих внешних ключей в таблице "Заказы" будет автоматически установлено значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3a423-157">Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="3a423-158">Чтобы предотвратить автоматическое создание индексов для внешних ключей, можно использовать модификатор NO INDEX.</span><span class="sxs-lookup"><span data-stu-id="3a423-158">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used.</span></span> <span data-ttu-id="3a423-159">Данная форма определения внешнего ключа должна применяться только в случаях, где получаемые в результате значения индекса часто будут дублироваться.</span><span class="sxs-lookup"><span data-stu-id="3a423-159">This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated.</span></span> <span data-ttu-id="3a423-160">Если значения в индексе внешнего ключа часто дублируются, использование индекса может быть менее эффективным, чем простое выполнение сканирования таблицы.</span><span class="sxs-lookup"><span data-stu-id="3a423-160">Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan.</span></span> <span data-ttu-id="3a423-161">Использование данного типа индекса со строками, вставляемыми и удаляемыми из таблицы, ухудшает производительность и не дает никаких преимуществ.</span><span class="sxs-lookup"><span data-stu-id="3a423-161">Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="3a423-162">Пример</span><span class="sxs-lookup"><span data-stu-id="3a423-162">Example</span></span>

<span data-ttu-id="3a423-163">В этом примере создается новая таблица с именем ThisTable и двумя текстовыми полями.</span><span class="sxs-lookup"><span data-stu-id="3a423-163">This example creates a new table called ThisTable with two text fields.</span></span>

```vb 
 Sub CreateTableX1()    
Dim dbs As Database 
 
    ' Modify this line to include the path to Northwind 
    ' on your computer. 
    Set dbs = OpenDatabase("Northwind.mdb") 
 
    ' Create a table with two text fields. 
    dbs.Execute "CREATE TABLE ThisTable " _ 
        & "(FirstName CHAR, LastName CHAR);" 
 
    dbs.Close 
 
End Sub
```

<br/>

<span data-ttu-id="3a423-164">В этом примере создается новая таблица с именем MyTable с двумя текстовыми поля, полем даты и времени и уникальным индексом, состоящим из всех трех полей.</span><span class="sxs-lookup"><span data-stu-id="3a423-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="3a423-165">В этом примере создается новая таблица с двумя текстовыми полями и полем **Integer**.</span><span class="sxs-lookup"><span data-stu-id="3a423-165">This example creates a new table with two text fields and an **Integer** field.</span></span> <span data-ttu-id="3a423-166">Поле SSN является первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="3a423-166">The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

