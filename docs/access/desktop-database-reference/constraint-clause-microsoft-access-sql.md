---
title: CONSTRAINT Clause (Microsoft Access SQL)
TOCTitle: CONSTRAINT Clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7b26033c8026591c87e4d0f9e077380862e39f16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480008"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="4d135-102">CONSTRAINT Clause (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4d135-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="4d135-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d135-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4d135-104">Ограничение аналогична индекса, хотя он также можно использовать для создания связи с другой таблицей.</span><span class="sxs-lookup"><span data-stu-id="4d135-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="4d135-105">Используйте предложение ограничения в инструкциях [CREATE TABLE](create-table-statement-microsoft-access-sql.md) и [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) для создания или удаления ограничения.</span><span class="sxs-lookup"><span data-stu-id="4d135-105">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints.</span></span> <span data-ttu-id="4d135-106">Существует два типа предложений ограничений: один для создания ограничения на одно поле и для создания ограничения на более одного поля.</span><span class="sxs-lookup"><span data-stu-id="4d135-106">There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>


> [!NOTE]
> <span data-ttu-id="4d135-107">Ядро СУБД Microsoft Access не поддерживает использование ограничения или любой другой инструкции языка определения данных (DDL), с базами данных, ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4d135-107">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="4d135-108">Используйте методы создания DAO.</span><span class="sxs-lookup"><span data-stu-id="4d135-108">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d135-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d135-109">Syntax</span></span>

<span data-ttu-id="4d135-110">Простые ограничения:</span><span class="sxs-lookup"><span data-stu-id="4d135-110">Single-field constraint:</span></span>

<span data-ttu-id="4d135-111">ОГРАНИЧЕНИЕ *имени* {первичный ключ | УНИКАЛЬНЫЙ | NOT NULL | Справочные материалы *таблицавнешнегоключа* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | ЗАДАЙТЕ значение NULL,\] \[ON DELETE CASCADE | ЗАДАЙТЕ значение NULL,\]}</span><span class="sxs-lookup"><span data-stu-id="4d135-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="4d135-112">Составные ограничения:</span><span class="sxs-lookup"><span data-stu-id="4d135-112">Multiple-field constraint:</span></span>

<span data-ttu-id="4d135-113">ОГРАНИЧЕНИЕ *имени* {первичный ключ (*primary1*\[, *primary2* \[,... \]\]) | УНИКАЛЬНЫЙ (*unique1*\[, *unique2* \[,... \]\]) | NOT NULL (*notnull1*\[, *notnull2* \[,... \]\]) | ВНЕШНИЙ ключ \[без ИНДЕКСА\] (*аргументов ссылка1*\[, *ref2* \[,... \] \]) Ссылки *таблицавнешнегоключа* \[(*foreignfield1* \[, *foreignfield2* \[,... \] \])\] \[ON UPDATE CASCADE | ЗАДАЙТЕ значение NULL,\] \[ON DELETE CASCADE | ЗАДАЙТЕ значение NULL,\]}</span><span class="sxs-lookup"><span data-stu-id="4d135-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="4d135-114">Предложение ограничения состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="4d135-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d135-115">Часть</span><span class="sxs-lookup"><span data-stu-id="4d135-115">Part</span></span></p></th>
<th><p><span data-ttu-id="4d135-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4d135-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d135-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="4d135-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-118">Имя ограничения будет создан.</span><span class="sxs-lookup"><span data-stu-id="4d135-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d135-119"><em>primary1</em>, <em>primary2</em></span><span class="sxs-lookup"><span data-stu-id="4d135-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-120">Имя поля или полей, определяемых первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="4d135-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d135-121"><em>unique1</em>, <em>unique2</em></span><span class="sxs-lookup"><span data-stu-id="4d135-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-122">Имя поля или полей, определяемых как уникальный ключ.</span><span class="sxs-lookup"><span data-stu-id="4d135-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d135-123"><em>notnull1 notnull2</em></span><span class="sxs-lookup"><span data-stu-id="4d135-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-124">Имя поля, которые ограничены непустых значений.</span><span class="sxs-lookup"><span data-stu-id="4d135-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d135-125"><em>аргументов ссылка1</em>, <em>ref2</em></span><span class="sxs-lookup"><span data-stu-id="4d135-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-126">Имя поля внешнего ключа или полей, которые ссылаются на поля в другой таблице.</span><span class="sxs-lookup"><span data-stu-id="4d135-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d135-127"><em>таблицавнешнегоключа</em></span><span class="sxs-lookup"><span data-stu-id="4d135-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-128">Имя внешнего таблицы, содержащей поле или поля, указанного идентификатором <em>foreignfield</em>.</span><span class="sxs-lookup"><span data-stu-id="4d135-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d135-129"><em>foreignfield1</em>, <em>foreignfield2</em></span><span class="sxs-lookup"><span data-stu-id="4d135-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="4d135-130">Имя поля в <em>таблицавнешнегоключа</em> , указанного идентификатором <em>аргументов ссылка1</em>, <em>ref2</em>.</span><span class="sxs-lookup"><span data-stu-id="4d135-130">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>.</span></span> <span data-ttu-id="4d135-131">Это предложение можно опустить, если указанное поле первичный ключ <em>таблицавнешнегоключа</em>.</span><span class="sxs-lookup"><span data-stu-id="4d135-131">You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4d135-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d135-132">Remarks</span></span>

<span data-ttu-id="4d135-133">Используйте следующий синтаксис для простых ограничений в предложении определения поля инструкции ALTER TABLE или CREATE TABLE сразу после спецификации тип данных.</span><span class="sxs-lookup"><span data-stu-id="4d135-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="4d135-134">Используйте синтаксис для составные ограничения при использовании зарезервированным словом ограничение за пределами предложение определение поля в оператор ALTER TABLE или CREATE TABLE.</span><span class="sxs-lookup"><span data-stu-id="4d135-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="4d135-135">Использование ограничения можно назначить полю один из следующих типов ограничений:</span><span class="sxs-lookup"><span data-stu-id="4d135-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="4d135-136">УНИКАЛЬНЫЙ зарезервированным словом можно использовать для назначения поля в качестве уникального ключа.</span><span class="sxs-lookup"><span data-stu-id="4d135-136">You can use the UNIQUE reserved word to designate a field as a unique key.</span></span> <span data-ttu-id="4d135-137">Это означает, что две записи в таблице может иметь такое же значение в этом поле.</span><span class="sxs-lookup"><span data-stu-id="4d135-137">This means that no two records in the table can have the same value in this field.</span></span> <span data-ttu-id="4d135-138">Можно ограничить все поля или список полей как уникальный.</span><span class="sxs-lookup"><span data-stu-id="4d135-138">You can constrain any field or list of fields as unique.</span></span> <span data-ttu-id="4d135-139">Если составные ограничения используется в качестве уникального ключа, объединенные значения всех полей в индексе должно быть уникальным, даже в том случае, если две или более записи с таким же значением в одном из полей.</span><span class="sxs-lookup"><span data-stu-id="4d135-139">If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="4d135-140">ПЕРВИЧНЫЙ ключ зарезервированные слова можно использовать для назначения одного поля или набор полей в таблице в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="4d135-140">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key.</span></span> <span data-ttu-id="4d135-141">Все значения в первичный ключ должно быть уникальным и не **может быть Null**и может существовать только один первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="4d135-141">All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="4d135-142">Не задано ограничение первичный ключ в таблице, уже имеет первичный ключ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="4d135-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="4d135-143">ВНЕШНИЙ ключ для зарезервированные слова используются для назначения поля в качестве внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="4d135-143">You can use the FOREIGN KEY reserved words to designate a field as a foreign key.</span></span> <span data-ttu-id="4d135-144">Если первичный ключ внешней таблицы состоит из нескольких полей, необходимо использовать определении ограничения нескольких полей со списком всех ссылающиеся поля, имя внешней таблицы и имена указанного поля в таблице внешнего в том же порядке что перечислены ссылающиеся поля.</span><span class="sxs-lookup"><span data-stu-id="4d135-144">If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed.</span></span> <span data-ttu-id="4d135-145">Если указанного поля или поля таблицы внешнего первичный ключ, не нужно указывать поля, который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="4d135-145">If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields.</span></span> <span data-ttu-id="4d135-146">По умолчанию ядро базы данных происходит так, как в случае первичный ключ таблицы внешнего указанного поля.</span><span class="sxs-lookup"><span data-stu-id="4d135-146">By default the database engine behaves as if the foreign table's primary key is the referenced fields.</span></span> <span data-ttu-id="4d135-147">Ограничения внешнего ключа задают конкретные действия, выполняемые при изменении значения соответствующего первичного ключа:</span><span class="sxs-lookup"><span data-stu-id="4d135-147">Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="4d135-148">Можно указать действий, выполняемых на основании соответствующих действий, выполняемых на первичный ключ в таблице, на котором определяется ограничение таблицы внешнего.</span><span class="sxs-lookup"><span data-stu-id="4d135-148">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined.</span></span> <span data-ttu-id="4d135-149">Например рассмотрим следующее определение для таблицы клиентов.</span><span class="sxs-lookup"><span data-stu-id="4d135-149">For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="4d135-150">Рассмотрим следующее определение таблицы Orders, в котором определяется внешнего ключа ссылки на первичный ключ в таблице клиентов.</span><span class="sxs-lookup"><span data-stu-id="4d135-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="4d135-151">Предложение ON DELETE CASCADE и ON UPDATE CASCADE определены для внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="4d135-151">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key.</span></span> <span data-ttu-id="4d135-152">Предложения ON CASCADE обновление означает, что если идентификатора клиента (CustId) обновляется в таблице клиентов, обновление будет каскадным таблицы заказов.</span><span class="sxs-lookup"><span data-stu-id="4d135-152">The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table.</span></span> <span data-ttu-id="4d135-153">Каждый заказ, содержащий соответствующее значение идентификатора клиента будут автоматически обновлены с новым значением.</span><span class="sxs-lookup"><span data-stu-id="4d135-153">Each order containing a corresponding customer identifier value will be updated automatically with the new value.</span></span> <span data-ttu-id="4d135-154">Предложение ON DELETE CASCADE означает, что при удалении клиента из таблицы Клиент все строки в таблице Orders, содержащий то же значение идентификатора клиента также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="4d135-154">The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted.</span></span> <span data-ttu-id="4d135-155">Рассмотрим следующие различные определения таблицы Orders с использованием действия SET NULL вместо действия CASCADE.</span><span class="sxs-lookup"><span data-stu-id="4d135-155">Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="4d135-156">Предложение ON UPDATE SET NULL означает, что если идентификатора клиента (CustId) обновляется в таблице клиентов, соответствующие значения внешнего ключа в таблице Orders автоматически устанавливается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4d135-156">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL.</span></span> <span data-ttu-id="4d135-157">Аналогично предложение ON DELETE SET NULL означает, что при удалении клиента из таблицы Клиент все соответствующие внешние ключи в таблице Orders автоматически устанавливается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4d135-157">Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="4d135-158">Чтобы запретить автоматическое создание индексов для внешних ключей, можно использовать модификатор NO INDEX.</span><span class="sxs-lookup"><span data-stu-id="4d135-158">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used.</span></span> <span data-ttu-id="4d135-159">Определение внешнего ключа в этой форме можно использовать только в тех случаях, где результирующего значения индексов будут часто повторяться.</span><span class="sxs-lookup"><span data-stu-id="4d135-159">This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated.</span></span> <span data-ttu-id="4d135-160">Где часто повторяющихся значений в индексе внешнего ключа, с помощью индекса может быть менее эффективным, чем просто сканирование таблицы.</span><span class="sxs-lookup"><span data-stu-id="4d135-160">Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan.</span></span> <span data-ttu-id="4d135-161">Сохранение такого индекса, со строками вставлен и удалены из таблицы снижает производительность и не предоставляет никаких преимуществ.</span><span class="sxs-lookup"><span data-stu-id="4d135-161">Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="4d135-162">Пример</span><span class="sxs-lookup"><span data-stu-id="4d135-162">Example</span></span>

<span data-ttu-id="4d135-163">В этом примере создается новая таблица с именем ThisTable с двух текстовых полей.</span><span class="sxs-lookup"><span data-stu-id="4d135-163">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="4d135-164">В этом примере создается новая таблица с именем MyTable с двух текстовых полей, поля даты/времени и уникальный индекс, состоящих из всех трех полей.</span><span class="sxs-lookup"><span data-stu-id="4d135-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="4d135-165">В этом примере создается новая таблица с двух текстовых полей и **целого** поля.</span><span class="sxs-lookup"><span data-stu-id="4d135-165">This example creates a new table with two text fields and an **Integer** field.</span></span> <span data-ttu-id="4d135-166">В поле SSN — основной ключ.</span><span class="sxs-lookup"><span data-stu-id="4d135-166">The SSN field is the primary key.</span></span>

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

