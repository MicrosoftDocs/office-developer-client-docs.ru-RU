---
title: Инструкция CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295361"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="1fc83-102">Инструкция CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1fc83-102">CREATE TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="1fc83-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fc83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1fc83-104">Создает таблицу.</span><span class="sxs-lookup"><span data-stu-id="1fc83-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="1fc83-105">Ядро СУБД Microsoft Access не поддерживает использование CREATE TABLE или любых других инструкций DDL с базами данных не на основе ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1fc83-105">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="1fc83-106">Используйте вместо этого методы DAO **Create**.</span><span class="sxs-lookup"><span data-stu-id="1fc83-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc83-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fc83-107">Syntax</span></span>

<span data-ttu-id="1fc83-108">CREATE \[TEMPORARY\] TABLE *таблица* (*поле1 тип* \[(*размер*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*индекс1*\] \[, *поле2* *тип* \[(*размер*)\] \[NOT NULL\] \[*индекс2*\] \[, …\]\] \[, CONSTRAINT *индекс_набора_полей* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="1fc83-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="1fc83-109">Инструкция CREATE TABLE включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="1fc83-109">The CREATE PROCEDURE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fc83-110">Часть</span><span class="sxs-lookup"><span data-stu-id="1fc83-110">Part</span></span></p></th>
<th><p><span data-ttu-id="1fc83-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1fc83-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fc83-112"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="1fc83-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="1fc83-113">Имя таблицы, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="1fc83-113">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fc83-114"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="1fc83-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="1fc83-115">Имена полей, которые создаются в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="1fc83-115">The name of field or fields to be created in the new table.</span></span> <span data-ttu-id="1fc83-116">Необходимо создать хотя бы одно поле.</span><span class="sxs-lookup"><span data-stu-id="1fc83-116">You must create at least one UM hunt group.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fc83-117"><em>тип</em></span><span class="sxs-lookup"><span data-stu-id="1fc83-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="1fc83-118">Тип данных <em>поля</em> в новой таблице.</span><span class="sxs-lookup"><span data-stu-id="1fc83-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fc83-119"><em>размер</em></span><span class="sxs-lookup"><span data-stu-id="1fc83-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="1fc83-120">Размер поля в знаках (только для полей с типом данных TEXT и BINARY).</span><span class="sxs-lookup"><span data-stu-id="1fc83-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fc83-121"><em>индекс1</em>, <em>индекс2</em></span><span class="sxs-lookup"><span data-stu-id="1fc83-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="1fc83-122">Предложение CONSTRAINT, определяющее индекс по одному полю.</span><span class="sxs-lookup"><span data-stu-id="1fc83-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="1fc83-123">Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="1fc83-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fc83-124"><em>индекс_набора_полей</em></span><span class="sxs-lookup"><span data-stu-id="1fc83-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="1fc83-125">Предложение CONSTRAINT, определяющее индекс по нескольким полям.</span><span class="sxs-lookup"><span data-stu-id="1fc83-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="1fc83-126">Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="1fc83-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1fc83-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="1fc83-127">Remarks</span></span>

<span data-ttu-id="1fc83-128">Используйте инструкцию CREATE TABLE, чтобы определить новую таблицу, поля и ограничения полей.</span><span class="sxs-lookup"><span data-stu-id="1fc83-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="1fc83-129">Если для поля определено свойство NOT NULL, поле обязательно должно содержать допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="1fc83-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="1fc83-130">Предложение CONSTRAINT накладывает на поле различные ограничения, и с помощью него можно задать первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="1fc83-130">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key.</span></span> <span data-ttu-id="1fc83-131">Для создания первичного ключа или дополнительных индексов в существующих таблицах можно использовать инструкцию [CREATE INDEX](create-index-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="1fc83-131">You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="1fc83-132">Свойство NOT NULL можно задавать для одного поля или внутри именованного предложения CONSTRAINT для одного или нескольких полей.</span><span class="sxs-lookup"><span data-stu-id="1fc83-132">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="1fc83-133">Свойство NOT NULL для поля можно задать только один раз.</span><span class="sxs-lookup"><span data-stu-id="1fc83-133">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="1fc83-134">Попытка определить это свойство повторно приведет к ошибке выполнения.</span><span class="sxs-lookup"><span data-stu-id="1fc83-134">Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="1fc83-135">Таблица, созданная с помощью атрибута TEMPORARY, доступна только в течение того сеанса, во время которого она была создана.</span><span class="sxs-lookup"><span data-stu-id="1fc83-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="1fc83-136">Она автоматически удаляется по завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="1fc83-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="1fc83-137">Несколько пользователей могут иметь доступ к временной таблице.</span><span class="sxs-lookup"><span data-stu-id="1fc83-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="1fc83-138">Атрибут WITH COMPRESSION можно использовать только с типами данных CHARACTER, MEMO (другое название — TEXT) и их синонимами.</span><span class="sxs-lookup"><span data-stu-id="1fc83-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="1fc83-139">Атрибут WITH COMPRESSION был добавлен для столбцов с типом данных CHARACTER из-за изменения формата представления знаков Юникода.</span><span class="sxs-lookup"><span data-stu-id="1fc83-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="1fc83-140">Каждый знак Юникода всегда занимает два байта.</span><span class="sxs-lookup"><span data-stu-id="1fc83-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="1fc83-141">Для существующих баз данных Microsoft Jet, содержащих преимущественно символьные данные, это может привести к почти двукратному увеличению размера при преобразовании в формат ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1fc83-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="1fc83-142">Однако представление Юникода для многих наборов символов, которые прежде назывались однобайтовыми кодировками (SBCS), можно без труда сжать до одного байта на символ.</span><span class="sxs-lookup"><span data-stu-id="1fc83-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="1fc83-143">Если для столбца с типом данных CHARACTER задать этот атрибут, при сохранении данные автоматически будут сжиматься, а при извлечении из столбца — возвращаться в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="1fc83-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="1fc83-144">Столбцы с типом данных MEMO также могут содержать сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="1fc83-144">MEMO columns can also be defined to store data in a compressed format.</span></span> <span data-ttu-id="1fc83-145">Однако в этом случае существует ограничение.</span><span class="sxs-lookup"><span data-stu-id="1fc83-145">However, there is a workaround.</span></span> <span data-ttu-id="1fc83-146">Сжатию могут быть подвергнуты только те поля столбцов с типом данных MEMO, размер которых после сжатия не будет превышать 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="1fc83-146">Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed.</span></span> <span data-ttu-id="1fc83-147">Остальные поля столбцов с типом данных MEMO останутся в обычном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1fc83-147">All other instances of MEMO columns will remain uncompressed.</span></span> <span data-ttu-id="1fc83-148">Таким образом, в пределах одной таблицы и одного столбца с типом данных MEMO одни данные могут быть подвергнуты сжатию, а другие — нет.</span><span class="sxs-lookup"><span data-stu-id="1fc83-148">This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="1fc83-149">Пример</span><span class="sxs-lookup"><span data-stu-id="1fc83-149">Example</span></span>

<span data-ttu-id="1fc83-150">В этом примере создается новая таблица с именем ThisTable и двумя текстовыми полями.</span><span class="sxs-lookup"><span data-stu-id="1fc83-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="1fc83-151">В этом примере создается новая таблица с именем MyTable с двумя текстовыми поля, полем даты и времени и уникальным индексом, состоящим из всех трех полей.</span><span class="sxs-lookup"><span data-stu-id="1fc83-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="1fc83-152">В этом примере создается новая таблица с двумя текстовыми полями и полем **Integer**.</span><span class="sxs-lookup"><span data-stu-id="1fc83-152">This example creates a new table with two text fields and an **Integer** field.</span></span> <span data-ttu-id="1fc83-153">Поле SSN является первичным ключом.</span><span class="sxs-lookup"><span data-stu-id="1fc83-153">The SSN field is the primary key.</span></span>

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
