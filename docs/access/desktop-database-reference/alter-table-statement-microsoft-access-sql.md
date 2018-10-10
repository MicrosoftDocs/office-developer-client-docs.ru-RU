---
title: ALTER TABLE Statement (Microsoft Access SQL)
TOCTitle: ALTER TABLE Statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8fc826d438973b4d079e9b90d3663ab755821cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482751"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="3c24f-102">ALTER TABLE Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3c24f-102">ALTER TABLE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="3c24f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c24f-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3c24f-104">Изменяет макет таблицы после его создания с помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="3c24f-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>


> [!NOTE]
> <span data-ttu-id="3c24f-105">Ядро СУБД Microsoft Access не поддерживает использование ALTER TABLE или любой другой инструкции языка определения данных (DDL), с базами данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3c24f-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="3c24f-106">Используйте методы создания DAO.</span><span class="sxs-lookup"><span data-stu-id="3c24f-106">Use the DAO Create methods instead.</span></span>



## <a name="syntax"></a><span data-ttu-id="3c24f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c24f-107">Syntax</span></span>

<span data-ttu-id="3c24f-108">ALTER TABLE в *таблице* {ДОБАВЬТЕ {СТОЛБЦА *типа поля*\[(*размер*)\] \[NOT NULL\] \[ограничения *индекса* \] | Изменение СТОЛБЦА *типа поля*\[(*размер*)\] | ОГРАНИЧЕНИЕ *multifieldindex*} | ПОМЕСТИТЕ {СТОЛБЦА *поле* я ограничение *имя_индекса*}}</span><span class="sxs-lookup"><span data-stu-id="3c24f-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="3c24f-109">Оператор ALTER TABLE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="3c24f-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c24f-110">Часть</span><span class="sxs-lookup"><span data-stu-id="3c24f-110">Part</span></span></p></th>
<th><p><span data-ttu-id="3c24f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3c24f-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c24f-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="3c24f-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-113">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c24f-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c24f-114"><em>поля</em></span><span class="sxs-lookup"><span data-stu-id="3c24f-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-115">Имя поля, по которому добавляется или удаляется из <em>таблицы</em>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-115">The name of the field to be added to or deleted from <em>table</em>.</span></span> <span data-ttu-id="3c24f-116">Или же имя поля, которое будет изменено в <em>таблице</em>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-116">Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c24f-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="3c24f-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-118">Тип данных <em>поля</em>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c24f-119"><em>size</em>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-120">Размер поля в знаках (только текст и двоичные поля).</span><span class="sxs-lookup"><span data-stu-id="3c24f-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c24f-121"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="3c24f-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-122">Индекс для <em>поля</em>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-122">The index for <em>field</em>.</span></span> <span data-ttu-id="3c24f-123">Для получения дополнительных сведений о способах создания этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">Предложение ограничения</a>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-123">For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c24f-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="3c24f-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-125">Определение составной индекс для добавления <em>в таблицу</em>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="3c24f-126">Для получения дополнительных сведений о способах создания этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">Предложение ограничения</a>.</span><span class="sxs-lookup"><span data-stu-id="3c24f-126">For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c24f-127"><em>имя_индекса</em></span><span class="sxs-lookup"><span data-stu-id="3c24f-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="3c24f-128">Имя составной индекс требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="3c24f-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3c24f-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c24f-129">Remarks</span></span>

<span data-ttu-id="3c24f-130">С помощью оператора изменения таблицы можно изменить существующую таблицу несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="3c24f-130">Using the ALTER TABLE statement you can alter an existing table in several ways.</span></span> <span data-ttu-id="3c24f-131">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3c24f-131">You can:</span></span>

  - <span data-ttu-id="3c24f-132">Используйте добавить столбец для добавления нового поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="3c24f-132">Use ADD COLUMN to add a new field to the table.</span></span> <span data-ttu-id="3c24f-133">Укажите имя поля, тип данных и (для текста и двоичный полей) требуемый размер.</span><span class="sxs-lookup"><span data-stu-id="3c24f-133">You specify the field name, data type, and (for Text and Binary fields) an optional size.</span></span> <span data-ttu-id="3c24f-134">Например следующий оператор добавляет 25-значный текстовое поле примечания к таблице Employees.</span><span class="sxs-lookup"><span data-stu-id="3c24f-134">For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
    ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
    ```
    
    <span data-ttu-id="3c24f-135">Можно также определить индекс для этого поля.</span><span class="sxs-lookup"><span data-stu-id="3c24f-135">You can also define an index on that field.</span></span> <span data-ttu-id="3c24f-136">Дополнительные сведения для одного поля индексов можно [Предложение ограничения](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="3c24f-136">For more information on single-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
    <span data-ttu-id="3c24f-137">Если указать не значение NULL для поля новые записи должны иметь допустимые данные в этих полях.</span><span class="sxs-lookup"><span data-stu-id="3c24f-137">If you specify NOT NULL for a field then new records are required to have valid data in that field.</span></span>

  - <span data-ttu-id="3c24f-138">Используйте ALTER COLUMN, чтобы изменить тип данных для существующего поля.</span><span class="sxs-lookup"><span data-stu-id="3c24f-138">Use ALTER COLUMN to change the data type of an existing field.</span></span> <span data-ttu-id="3c24f-139">Укажите имя поля, новый тип данных и требуемый размер для двоичных полей и текст.</span><span class="sxs-lookup"><span data-stu-id="3c24f-139">You specify the field name, the new data type, and an optional size for Text and Binary fields.</span></span> <span data-ttu-id="3c24f-140">Например следующий оператор изменяет тип данных поля в таблице сотрудников, называется ZipCode (изначально определена как целое число) текстового поля 10 символов:</span><span class="sxs-lookup"><span data-stu-id="3c24f-140">For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
    ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
    ```

  - <span data-ttu-id="3c24f-141">Используйте ограничение ADD для добавления составной индекс.</span><span class="sxs-lookup"><span data-stu-id="3c24f-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="3c24f-142">Для получения дополнительных сведений о составные индексы видеть [Предложение ограничения](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="3c24f-142">For more information on multiple-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>

  - <span data-ttu-id="3c24f-143">Удаление СТОЛБЦА используется для удаления поля.</span><span class="sxs-lookup"><span data-stu-id="3c24f-143">Use DROP COLUMN to delete a field.</span></span> <span data-ttu-id="3c24f-144">Указать только имя поля.</span><span class="sxs-lookup"><span data-stu-id="3c24f-144">You specify only the name of the field.</span></span>

  - <span data-ttu-id="3c24f-145">ПОМЕСТИТЕ ограничение используется для удаления составной индекс.</span><span class="sxs-lookup"><span data-stu-id="3c24f-145">Use DROP CONSTRAINT to delete a multiple-field index.</span></span> <span data-ttu-id="3c24f-146">Укажите следующие ограничения имя индекса зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="3c24f-146">You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="3c24f-147">Не удается добавить или удалить более одного поля или индекса за раз.</span><span class="sxs-lookup"><span data-stu-id="3c24f-147">You cannot add or delete more than one field or index at a time.</span></span></P>
> <LI>
> <P><span data-ttu-id="3c24f-148">Инструкция <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> можно использовать для добавления одного или нескольких полей индекса в таблицу и ALTER TABLE или инструкции <A href="drop-statement-microsoft-access-sql.md">DROP</A> можно использовать для удаления индекса, созданных с помощью ALTER TABLE или CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="3c24f-148">You can use the <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the <A href="drop-statement-microsoft-access-sql.md">DROP</A> statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span></P>
> <LI>
> <P><span data-ttu-id="3c24f-149">НЕ NULL можно использовать на одного поля или внутри именованного предложения ограничения для одного или для нескольких полей с именем ограничения.</span><span class="sxs-lookup"><span data-stu-id="3c24f-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="3c24f-150">Тем не менее можно применить к полю ограничение NOT NULL только один раз.</span><span class="sxs-lookup"><span data-stu-id="3c24f-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="3c24f-151">Попытка использовать это ограничение более одного раза появлению ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="3c24f-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="3c24f-152">Пример</span><span class="sxs-lookup"><span data-stu-id="3c24f-152">Example</span></span>

<span data-ttu-id="3c24f-153">В этом примере добавляет поле заработной платы с типом данных **деньги** в таблицу Employees.</span><span class="sxs-lookup"><span data-stu-id="3c24f-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

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

<span data-ttu-id="3c24f-154">В этом примере изменяется поле Salary и типа данных **деньги** **знаков**типу данных.</span><span class="sxs-lookup"><span data-stu-id="3c24f-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

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

<span data-ttu-id="3c24f-155">В этом примере удаляется поле Salary из таблицы сотрудников.</span><span class="sxs-lookup"><span data-stu-id="3c24f-155">This example removes the Salary field from the Employees table.</span></span>

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

<span data-ttu-id="3c24f-156">В этом примере добавляется внешний ключ для таблицы Orders.</span><span class="sxs-lookup"><span data-stu-id="3c24f-156">This example adds a foreign key to the Orders table.</span></span> <span data-ttu-id="3c24f-157">Внешний ключ основано на поле EmployeeID и ссылается на поле EmployeeID таблицы «Сотрудники».</span><span class="sxs-lookup"><span data-stu-id="3c24f-157">The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table.</span></span> <span data-ttu-id="3c24f-158">В этом примере не нужно указать поле EmployeeID после таблице Employees в предложении справочные материалы, поскольку EmployeeID — это первичный ключ в таблице сотрудников.</span><span class="sxs-lookup"><span data-stu-id="3c24f-158">In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

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

<span data-ttu-id="3c24f-159">В этом примере удаляется внешний ключ из таблицы заказов.</span><span class="sxs-lookup"><span data-stu-id="3c24f-159">This example removes the foreign key from the Orders table.</span></span>

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
