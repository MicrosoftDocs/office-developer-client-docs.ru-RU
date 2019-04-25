---
title: Инструкция ALTER TABLE (Microsoft Access SQL)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297160"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="af48d-102">Инструкция ALTER TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="af48d-102">ALTER TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="af48d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af48d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af48d-104">Служит для изменения макета таблицы после того, как она была создана с помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="af48d-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="af48d-105">Ядро СУБД Microsoft Access не поддерживает использование ALTER TABLE или любых других инструкций DDL с базами данных, которые не основаны на Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="af48d-105">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="af48d-106">Используйте вместо этого методы DAO **Create**.</span><span class="sxs-lookup"><span data-stu-id="af48d-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="af48d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af48d-107">Syntax</span></span>

<span data-ttu-id="af48d-108">ALTER TABLE *таблица* {ADD {COLUMN *тип поля*\[(*размер*)\] \[NOT NULL\] \[CONSTRAINT *индекс*\] | ALTER COLUMN *тип поля*\[(*размер*)\] | CONSTRAINT *индекс_набора_полей*} | DROP {COLUMN *поле* I CONSTRAINT *имя_индекса*} }</span><span class="sxs-lookup"><span data-stu-id="af48d-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="af48d-109">Инструкция ALTER TABLE включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="af48d-109">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af48d-110">Часть</span><span class="sxs-lookup"><span data-stu-id="af48d-110">Part</span></span></p></th>
<th><p><span data-ttu-id="af48d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="af48d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af48d-112"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="af48d-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-113">Имя таблицы, которую требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="af48d-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af48d-114"><em>поле</em></span><span class="sxs-lookup"><span data-stu-id="af48d-114"><em>Field</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-115">Имя поля, которое будет добавлено в <em>таблицу</em>, удалено из нее</span><span class="sxs-lookup"><span data-stu-id="af48d-115">The name of the field to be added to or deleted from <em>table</em>.</span></span> <span data-ttu-id="af48d-116">или изменено в ней.</span><span class="sxs-lookup"><span data-stu-id="af48d-116">Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af48d-117"><em>тип</em></span><span class="sxs-lookup"><span data-stu-id="af48d-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-118">Тип данных <em>поля</em>.</span><span class="sxs-lookup"><span data-stu-id="af48d-118">The <em>Type</em> selection defines the data type of the custom field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af48d-119"><em>размер</em></span><span class="sxs-lookup"><span data-stu-id="af48d-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-120">Размер поля в знаках (только для полей с типом данных TEXT и BINARY).</span><span class="sxs-lookup"><span data-stu-id="af48d-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af48d-121"><em>индекс</em></span><span class="sxs-lookup"><span data-stu-id="af48d-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-122">Индекс <em>поля</em>.</span><span class="sxs-lookup"><span data-stu-id="af48d-122">The index for <em>field</em>.</span></span> <span data-ttu-id="af48d-123">Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="af48d-123">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af48d-124"><em>индекс_набора_полей</em></span><span class="sxs-lookup"><span data-stu-id="af48d-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-125">Индекс набора полей, добавляемых в <em>таблицу</em>.</span><span class="sxs-lookup"><span data-stu-id="af48d-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="af48d-126">Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="af48d-126">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af48d-127"><em>имя_индекса</em></span><span class="sxs-lookup"><span data-stu-id="af48d-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="af48d-128">Имя удаляемого индекса набора полей.</span><span class="sxs-lookup"><span data-stu-id="af48d-128">The name of the property to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="af48d-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="af48d-129">Remarks</span></span>

<span data-ttu-id="af48d-130">Изменить существующую таблицу с помощью инструкции ALTER TABLE можно несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="af48d-130">By using the ALTER TABLE statement, you can alter an existing table in several ways.</span></span> <span data-ttu-id="af48d-131">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="af48d-131">You can:</span></span>

- <span data-ttu-id="af48d-132">Добавить поле в таблицу, используя инструкцию ADD COLUMN.</span><span class="sxs-lookup"><span data-stu-id="af48d-132">Use ADD COLUMN to add a new field to the table.</span></span> <span data-ttu-id="af48d-133">Требуется указать имя поля и тип данных. Для полей с типом данных TEXT и BINARY можно также указать размер.</span><span class="sxs-lookup"><span data-stu-id="af48d-133">You specify the field name, data type, and (for Text and Binary fields) an optional size.</span></span> <span data-ttu-id="af48d-134">Например, следующая инструкция добавляет поле Notes с типом данных TEXT размером 25 знаков в таблицу Employees:</span><span class="sxs-lookup"><span data-stu-id="af48d-134">For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="af48d-135">Для этого поля можно также указать индекс.</span><span class="sxs-lookup"><span data-stu-id="af48d-135">You can also define an index on that field.</span></span> <span data-ttu-id="af48d-136">Дополнительные сведения об индексах одного поля см. в статье, посвященной [предложению CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="af48d-136">For more information about single-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="af48d-137">Если для поля определено свойство NOT NULL, поле обязательно должно содержать допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="af48d-137">If you specify NOT NULL for a field, new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="af48d-138">Изменить тип данных для существующего поля, используя инструкцию ALTER COLUMN.</span><span class="sxs-lookup"><span data-stu-id="af48d-138">Use ALTER COLUMN to change the data type of an existing field.</span></span> <span data-ttu-id="af48d-139">Требуется указать имя поля и новый тип данных. Для полей с типом данных TEXT и BINARY можно также указать размер.</span><span class="sxs-lookup"><span data-stu-id="af48d-139">You specify the field name, the new data type, and an optional size for Text and Binary fields.</span></span> <span data-ttu-id="af48d-140">Например, следующая инструкция в таблице Employees изменит тип данных поля ZipCode (начальный тип данных — INTEGER) на тип данных TEXT размером 10 знаков:</span><span class="sxs-lookup"><span data-stu-id="af48d-140">For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- <span data-ttu-id="af48d-141">Добавить индекс набора полей, используя инструкцию ADD CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="af48d-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="af48d-142">Дополнительные сведения об индексах набора полей см. в статье, посвященной [предложению CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="af48d-142">For more information about multiple-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="af48d-143">Удалить поле, используя инструкцию DROP COLUMN.</span><span class="sxs-lookup"><span data-stu-id="af48d-143">Use DROP COLUMN to delete a field.</span></span> <span data-ttu-id="af48d-144">Требуется указать только имя поля.</span><span class="sxs-lookup"><span data-stu-id="af48d-144">You specify only the name of the field.</span></span>

- <span data-ttu-id="af48d-145">Использовать DROP CONSTRAINT, чтобы удалить индекс набора полей.</span><span class="sxs-lookup"><span data-stu-id="af48d-145">Use DROP CONSTRAINT to delete a multiple-field index.</span></span> <span data-ttu-id="af48d-146">Требуется указать только имя индекса после зарезервированного слова CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="af48d-146">You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE] 
> - <span data-ttu-id="af48d-147">Невозможно одновременно добавить или удалить несколько полей или индексов.</span><span class="sxs-lookup"><span data-stu-id="af48d-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="af48d-148">Чтобы добавить индекс для одного поля или для набора полей в таблице, используйте инструкцию [CREATE INDEX](create-index-statement-microsoft-access-sql.md). Чтобы удалить индекс, созданный с помощью инструкции ALTER TABLE или CREATE INDEX, можно использовать инструкцию ALTER TABLE или [DROP](drop-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="af48d-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="af48d-149">Свойство NOT NULL можно задавать для одного поля или внутри именованного предложения CONSTRAINT для одного или нескольких полей.</span><span class="sxs-lookup"><span data-stu-id="af48d-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="af48d-150">Свойство NOT NULL для поля можно задать только один раз.</span><span class="sxs-lookup"><span data-stu-id="af48d-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="af48d-151">Попытка определить это свойство повторно приведет к ошибке выполнения.</span><span class="sxs-lookup"><span data-stu-id="af48d-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="af48d-152">Пример</span><span class="sxs-lookup"><span data-stu-id="af48d-152">Example</span></span>

<span data-ttu-id="af48d-153">В этом примере добавляется поле Salary (Заработная плата) с типом данных **Money** в таблицу Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="af48d-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

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

<span data-ttu-id="af48d-154">В этом примере тип данных поля Salary (Заработная плата) изменяется с **Money** на **Char**.</span><span class="sxs-lookup"><span data-stu-id="af48d-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

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

<span data-ttu-id="af48d-155">В этом примере удаляется поле Salary (Заработная плата) из таблицы Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="af48d-155">This example removes the Salary field from the Employees table.</span></span>

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

<span data-ttu-id="af48d-156">В этом примере добавляется внешний ключ для таблицы Orders (Заказы).</span><span class="sxs-lookup"><span data-stu-id="af48d-156">This example adds a foreign key to the Orders table.</span></span> <span data-ttu-id="af48d-157">Внешний ключ основан на поле EmployeeID (Код сотрудника) и ссылается на поле EmployeeID (Код сотрудника) таблицы Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="af48d-157">The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table.</span></span> <span data-ttu-id="af48d-158">В этом примере не требуется перечислять поле EmployeeID (Код сотрудника) после таблицы Employees (Сотрудники) в предложении REFERENCES, так как EmployeeID — это первичный ключ таблицы Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="af48d-158">In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

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

<span data-ttu-id="af48d-159">В этом примере удаляется внешний ключ из таблицы Orders (Заказы).</span><span class="sxs-lookup"><span data-stu-id="af48d-159">This example removes the foreign key from the Orders table.</span></span>

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
