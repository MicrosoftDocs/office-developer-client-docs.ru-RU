---
title: Инструкция CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706175"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="47854-102">Инструкция CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="47854-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="47854-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47854-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47854-104">Создает таблицу.</span><span class="sxs-lookup"><span data-stu-id="47854-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="47854-105">Ядро СУБД Microsoft Access не поддерживает использование CREATE TABLE или любых других инструкций DDL с базами данных не на основе ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="47854-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="47854-106">Используйте вместо этого методы DAO **Create**.</span><span class="sxs-lookup"><span data-stu-id="47854-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="47854-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47854-107">Syntax</span></span>

<span data-ttu-id="47854-108">CREATE \[TEMPORARY\] TABLE *таблица* (*поле1 тип* \[(*размер*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*индекс1*\] \[, *поле2* *тип* \[(*размер*)\] \[NOT NULL\] \[*индекс2*\] \[, …\]\] \[, CONSTRAINT *индекс_набора_полей* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="47854-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="47854-109">Инструкция CREATE TABLE включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="47854-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47854-110">Часть</span><span class="sxs-lookup"><span data-stu-id="47854-110">Part</span></span></p></th>
<th><p><span data-ttu-id="47854-111">Описание</span><span class="sxs-lookup"><span data-stu-id="47854-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47854-112"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="47854-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="47854-113">Имя таблицы, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="47854-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47854-114"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="47854-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="47854-115">Имена полей, которые создаются в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="47854-115">The name of field or fields to be created in the new table.</span></span> <span data-ttu-id="47854-116">Необходимо создать хотя бы одно поле.</span><span class="sxs-lookup"><span data-stu-id="47854-116">You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47854-117"><em>тип</em></span><span class="sxs-lookup"><span data-stu-id="47854-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="47854-118">Тип данных <em>поля</em> в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="47854-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47854-119"><em>размер</em></span><span class="sxs-lookup"><span data-stu-id="47854-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="47854-120">Размер поля в знаках (только для полей с типом данных TEXT и BINARY).</span><span class="sxs-lookup"><span data-stu-id="47854-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47854-121"><em>индекс1</em>, <em>индекс2</em></span><span class="sxs-lookup"><span data-stu-id="47854-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="47854-122">Предложение CONSTRAINT, определяющее индекс по одному полю.</span><span class="sxs-lookup"><span data-stu-id="47854-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="47854-123">Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="47854-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47854-124"><em>индекс_набора_полей</em></span><span class="sxs-lookup"><span data-stu-id="47854-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="47854-125">Предложение CONSTRAINT, определяющее индекс по нескольким полям.</span><span class="sxs-lookup"><span data-stu-id="47854-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="47854-126">Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="47854-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="47854-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="47854-127">Remarks</span></span>

<span data-ttu-id="47854-128">Используйте инструкцию CREATE TABLE, чтобы определить новую таблицу, поля и ограничения полей.</span><span class="sxs-lookup"><span data-stu-id="47854-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="47854-129">Если для поля определено свойство NOT NULL, поле обязательно должно содержать допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="47854-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="47854-130">Предложение CONSTRAINT накладывает на поле различные ограничения, и с помощью него можно задать первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="47854-130">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key.</span></span> <span data-ttu-id="47854-131">Для создания первичного ключа или дополнительных индексов в существующих таблицах можно использовать инструкцию [CREATE INDEX](create-index-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="47854-131">You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="47854-132">Свойство NOT NULL можно задавать для одного поля или внутри именованного предложения CONSTRAINT для одного или нескольких полей.</span><span class="sxs-lookup"><span data-stu-id="47854-132">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="47854-133">Свойство NOT NULL для поля можно задать только один раз.</span><span class="sxs-lookup"><span data-stu-id="47854-133">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="47854-134">Попытка определить это свойство повторно приведет к ошибке выполнения.</span><span class="sxs-lookup"><span data-stu-id="47854-134">Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="47854-135">Таблица, созданная с помощью атрибута TEMPORARY, доступна только в течение того сеанса, во время которого она была создана.</span><span class="sxs-lookup"><span data-stu-id="47854-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="47854-136">Она автоматически удаляется по завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="47854-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="47854-137">Несколько пользователей могут иметь доступ к временной таблице.</span><span class="sxs-lookup"><span data-stu-id="47854-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="47854-138">Атрибут WITH COMPRESSION можно использовать только с типами данных CHARACTER, MEMO (другое название — TEXT) и их синонимами.</span><span class="sxs-lookup"><span data-stu-id="47854-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="47854-139">Атрибут WITH COMPRESSION был добавлен для столбцов с типом данных CHARACTER из-за изменения формата представления знаков Юникода.</span><span class="sxs-lookup"><span data-stu-id="47854-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="47854-140">Каждый знак Юникода всегда занимает два байта.</span><span class="sxs-lookup"><span data-stu-id="47854-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="47854-141">Для существующих баз данных Microsoft Jet, содержащих преимущественно символьные данные, это может привести к почти двукратному увеличению размера при преобразовании в формат ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="47854-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="47854-142">Однако представление Юникода для многих наборов символов, которые прежде назывались однобайтовыми кодировками (SBCS), можно без труда сжать до одного байта на символ.</span><span class="sxs-lookup"><span data-stu-id="47854-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="47854-143">Если для столбца с типом данных CHARACTER задать этот атрибут, при сохранении данные автоматически будут сжиматься, а при извлечении из столбца — возвращаться в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="47854-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="47854-144">Столбцы с типом данных MEMO также могут содержать сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="47854-144">MEMO columns can also be defined to store data in a compressed format.</span></span> <span data-ttu-id="47854-145">Однако в этом случае существует ограничение.</span><span class="sxs-lookup"><span data-stu-id="47854-145">However, there is a limitation.</span></span> <span data-ttu-id="47854-146">Сжатию могут быть подвергнуты только те поля столбцов с типом данных MEMO, размер которых после сжатия не будет превышать 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="47854-146">Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed.</span></span> <span data-ttu-id="47854-147">Остальные поля столбцов с типом данных MEMO останутся в обычном состоянии.</span><span class="sxs-lookup"><span data-stu-id="47854-147">All other instances of MEMO columns will remain uncompressed.</span></span> <span data-ttu-id="47854-148">Таким образом, в пределах одной таблицы и одного столбца с типом данных MEMO одни данные могут быть подвергнуты сжатию, а другие — нет.</span><span class="sxs-lookup"><span data-stu-id="47854-148">This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="47854-149">Пример</span><span class="sxs-lookup"><span data-stu-id="47854-149">Example</span></span>

<span data-ttu-id="47854-150">В этом примере создается новая таблица с именем ThisTable и двумя текстовыми полями.</span><span class="sxs-lookup"><span data-stu-id="47854-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="47854-151">В этом примере создается новая таблица с именем MyTable с двумя текстовыми поля, полем даты и времени и уникальным индексом, состоящим из всех трех полей.</span><span class="sxs-lookup"><span data-stu-id="47854-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="47854-152">В этом примере создается новая таблица с двумя текстовыми полями и полем **Integer**.</span><span class="sxs-lookup"><span data-stu-id="47854-152">This example creates a new table with two text fields and an **Integer** field.</span></span> <span data-ttu-id="47854-153">Поле SSN является первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="47854-153">The SSN field is the primary key.</span></span>

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

<span data-ttu-id="47854-154">В этом примере создается новая таблица с именем `~~Kitsch'n Sync`, в которой показаны различные типы полей и индексов.</span><span class="sxs-lookup"><span data-stu-id="47854-154">This example creates a new table called `~~Kitsch'n Sync` that demonstrates all the different field and index types.</span></span> <span data-ttu-id="47854-155">Поле счетчика является первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="47854-155">The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
