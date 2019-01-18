---
title: Оператор ALTER TABLE (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b8bd9abac3aee8be8fe52e555fcd5247e804f258
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701601"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="ca6a6-102">Оператор ALTER TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ca6a6-102">ALTER TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ca6a6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca6a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca6a6-104">Изменяет макет таблицы после его создания с помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6a6-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="ca6a6-105">Ядро СУБД Microsoft Access не поддерживает использование ALTER TABLE или любой другой инструкции языка определения данных (DDL), с базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="ca6a6-106">Используйте методы DAO **Создать** .</span><span class="sxs-lookup"><span data-stu-id="ca6a6-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6a6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca6a6-107">Syntax</span></span>

<span data-ttu-id="ca6a6-108">ALTER TABLE в *таблице* {ДОБАВЬТЕ {СТОЛБЦА *типа поля*\[(*размер*)\] \[NOT NULL\] \[ограничения *индекса* \] | Изменение СТОЛБЦА *типа поля*\[(*размер*)\] | ОГРАНИЧЕНИЕ *multifieldindex*} | ПОМЕСТИТЕ {СТОЛБЦА *поле* я ограничение *имя_индекса*}}</span><span class="sxs-lookup"><span data-stu-id="ca6a6-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="ca6a6-109">Оператор ALTER TABLE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="ca6a6-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca6a6-110">Часть</span><span class="sxs-lookup"><span data-stu-id="ca6a6-110">Part</span></span></p></th>
<th><p><span data-ttu-id="ca6a6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ca6a6-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca6a6-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-113">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca6a6-114"><em>поля</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-115">Имя поля, по которому добавляется или удаляется из <em>таблицы</em>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-115">The name of the field to be added to or deleted from <em>table</em>.</span></span> <span data-ttu-id="ca6a6-116">Или же имя поля, которое будет изменено в <em>таблице</em>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-116">Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca6a6-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-118">Тип данных <em>поля</em>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca6a6-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-120">Размер поля в знаках (только текст и двоичные поля).</span><span class="sxs-lookup"><span data-stu-id="ca6a6-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca6a6-121"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-122">Индекс для <em>поля</em>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-122">The index for <em>field</em>.</span></span> <span data-ttu-id="ca6a6-123">Дополнительные сведения о способах создания этого индекса см в <a href="constraint-clause-microsoft-access-sql.md">предложении ограничения</a>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-123">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca6a6-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-125">Определение составной индекс для добавления <em>в таблицу</em>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="ca6a6-126">Дополнительные сведения о способах создания этого индекса см в <a href="constraint-clause-microsoft-access-sql.md">предложении ограничения</a>.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-126">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca6a6-127"><em>имя_индекса</em></span><span class="sxs-lookup"><span data-stu-id="ca6a6-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="ca6a6-128">Имя составной индекс требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ca6a6-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca6a6-129">Remarks</span></span>

<span data-ttu-id="ca6a6-130">С помощью оператора изменения таблицы, можно изменить существующую таблицу несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-130">By using the ALTER TABLE statement, you can alter an existing table in several ways.</span></span> <span data-ttu-id="ca6a6-131">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-131">You can:</span></span>

- <span data-ttu-id="ca6a6-132">Используйте добавить столбец для добавления нового поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-132">Use ADD COLUMN to add a new field to the table.</span></span> <span data-ttu-id="ca6a6-133">Укажите имя поля, тип данных и (для текста и двоичный полей) требуемый размер.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-133">You specify the field name, data type, and (for Text and Binary fields) an optional size.</span></span> <span data-ttu-id="ca6a6-134">Например следующий оператор добавляет 25-значный текстовое поле примечания к таблице Employees.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-134">For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="ca6a6-135">Можно также определить индекс для этого поля.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-135">You can also define an index on that field.</span></span> <span data-ttu-id="ca6a6-136">Дополнительные сведения о отдельного поля индексов можно [предложение ограничения](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="ca6a6-136">For more information about single-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="ca6a6-137">При указании NOT NULL для поля, обязательно должно содержать допустимые данные в этих полях.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-137">If you specify NOT NULL for a field, new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="ca6a6-138">Используйте ALTER COLUMN, чтобы изменить тип данных для существующего поля.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-138">Use ALTER COLUMN to change the data type of an existing field.</span></span> <span data-ttu-id="ca6a6-139">Укажите имя поля, новый тип данных и требуемый размер для двоичных полей и текст.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-139">You specify the field name, the new data type, and an optional size for Text and Binary fields.</span></span> <span data-ttu-id="ca6a6-140">Например следующий оператор изменяет тип данных поля в таблице сотрудников, называется ZipCode (изначально определена как целое число) текстового поля 10 символов:</span><span class="sxs-lookup"><span data-stu-id="ca6a6-140">For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- <span data-ttu-id="ca6a6-141">Используйте ограничение ADD для добавления составной индекс.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="ca6a6-142">Дополнительные сведения о составные индексы можно [предложение ограничения](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="ca6a6-142">For more information about multiple-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="ca6a6-143">Удаление СТОЛБЦА используется для удаления поля.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-143">Use DROP COLUMN to delete a field.</span></span> <span data-ttu-id="ca6a6-144">Указать только имя поля.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-144">You specify only the name of the field.</span></span>

- <span data-ttu-id="ca6a6-145">ПОМЕСТИТЕ ограничение используется для удаления составной индекс.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-145">Use DROP CONSTRAINT to delete a multiple-field index.</span></span> <span data-ttu-id="ca6a6-146">Укажите следующие ограничения имя индекса зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-146">You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE] 
> - <span data-ttu-id="ca6a6-147">Не удается добавить или удалить более одного поля или индекса за раз.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="ca6a6-148">Инструкция [CREATE INDEX](create-index-statement-microsoft-access-sql.md) можно использовать для добавления одного или нескольких полей индекса в таблицу и ALTER TABLE или инструкции [DROP](drop-statement-microsoft-access-sql.md) можно использовать для удаления индекса, созданных с помощью ALTER TABLE или CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="ca6a6-149">НЕ NULL можно использовать на одного поля или внутри именованного предложения ограничения для одного или для нескольких полей с именем ограничения.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="ca6a6-150">Тем не менее можно применить к полю ограничение NOT NULL только один раз.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="ca6a6-151">Попытка использовать это ограничение более одного раза появлению ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="ca6a6-152">Пример</span><span class="sxs-lookup"><span data-stu-id="ca6a6-152">Example</span></span>

<span data-ttu-id="ca6a6-153">В этом примере добавляет поле заработной платы с типом данных **деньги** в таблицу Employees.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="ca6a6-154">В этом примере изменяется поле Salary и типа данных **деньги** **знаков**типу данных.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="ca6a6-155">В этом примере удаляется поле Salary из таблицы сотрудников.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-155">This example removes the Salary field from the Employees table.</span></span>

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="ca6a6-156">В этом примере добавляется внешний ключ для таблицы Orders.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-156">This example adds a foreign key to the Orders table.</span></span> <span data-ttu-id="ca6a6-157">Внешний ключ основано на поле EmployeeID и ссылается на поле EmployeeID таблицы «Сотрудники».</span><span class="sxs-lookup"><span data-stu-id="ca6a6-157">The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table.</span></span> <span data-ttu-id="ca6a6-158">В этом примере не нужно указать поле EmployeeID после таблице Employees в предложении справочные материалы, поскольку EmployeeID — это первичный ключ в таблице сотрудников.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-158">In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="ca6a6-159">В этом примере удаляется внешний ключ из таблицы заказов.</span><span class="sxs-lookup"><span data-stu-id="ca6a6-159">This example removes the foreign key from the Orders table.</span></span>

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
