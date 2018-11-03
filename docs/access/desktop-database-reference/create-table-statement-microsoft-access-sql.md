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
ms.openlocfilehash: 4beb013b09ce136d6ffa7558225e01fae80da645
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937094"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="3a71f-102">Инструкция CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3a71f-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="3a71f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a71f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a71f-104">Создает новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="3a71f-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="3a71f-105">Ядро СУБД Microsoft Access не поддерживает использование CREATE TABLE или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3a71f-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="3a71f-106">Используйте методы DAO **Создать** .</span><span class="sxs-lookup"><span data-stu-id="3a71f-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a71f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a71f-107">Syntax</span></span>

<span data-ttu-id="3a71f-108">Создание \[ВРЕМЕННЫЕ\] таблицы в *таблице* (*Тип field1* \[(*размер*)\] \[NOT NULL\] \[с СЖАТИЕ | С помощью COMP\] \[ *ИНДЕКС1* \] \[, *поле2* *Тип* \[(*размер*)\] \[NOT NULL\] \[ *index2* \] \[,... \] \] \[, Ограничение *multifieldindex* \[,... \]\])</span><span class="sxs-lookup"><span data-stu-id="3a71f-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="3a71f-109">Инструкция CREATE TABLE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="3a71f-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a71f-110">Часть</span><span class="sxs-lookup"><span data-stu-id="3a71f-110">Part</span></span></p></th>
<th><p><span data-ttu-id="3a71f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3a71f-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a71f-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="3a71f-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="3a71f-113">Имя таблицы будет создан.</span><span class="sxs-lookup"><span data-stu-id="3a71f-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a71f-114"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="3a71f-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="3a71f-115">Имя поля или поля, созданные в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="3a71f-115">The name of field or fields to be created in the new table.</span></span> <span data-ttu-id="3a71f-116">Необходимо создать хотя бы одно поле.</span><span class="sxs-lookup"><span data-stu-id="3a71f-116">You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a71f-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="3a71f-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="3a71f-118">Тип данных <em>поля</em> в новую таблицу.</span><span class="sxs-lookup"><span data-stu-id="3a71f-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a71f-119"><em>size</em>.</span><span class="sxs-lookup"><span data-stu-id="3a71f-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="3a71f-120">Размер поля в знаках (только текст и двоичные поля).</span><span class="sxs-lookup"><span data-stu-id="3a71f-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a71f-121"><em>ИНДЕКС1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="3a71f-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="3a71f-122">Определяет индекс по одному полю предложения ограничения.</span><span class="sxs-lookup"><span data-stu-id="3a71f-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="3a71f-123">Дополнительные сведения о создании этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">предложение ограничения</a>.</span><span class="sxs-lookup"><span data-stu-id="3a71f-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a71f-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="3a71f-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="3a71f-125">Предложение ограничения, определяет составной индекс.</span><span class="sxs-lookup"><span data-stu-id="3a71f-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="3a71f-126">Дополнительные сведения о создании этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">предложение ограничения</a>.</span><span class="sxs-lookup"><span data-stu-id="3a71f-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3a71f-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a71f-127">Remarks</span></span>

<span data-ttu-id="3a71f-128">Используйте инструкцию CREATE TABLE, чтобы определить новую таблицу, поля и ограничения полей.</span><span class="sxs-lookup"><span data-stu-id="3a71f-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="3a71f-129">Если не указано значение NULL для поля, обязательно должно содержать допустимые данные в этих полях.</span><span class="sxs-lookup"><span data-stu-id="3a71f-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="3a71f-130">Предложение ограничения устанавливает различные ограничения на доступ к полю и можно использовать для создания основного ключа.</span><span class="sxs-lookup"><span data-stu-id="3a71f-130">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key.</span></span> <span data-ttu-id="3a71f-131">Инструкция [CREATE INDEX](create-index-statement-microsoft-access-sql.md) можно также использовать для создания основного ключа или дополнительных индексов для существующих таблиц.</span><span class="sxs-lookup"><span data-stu-id="3a71f-131">You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="3a71f-132">НЕ NULL можно использовать на одного поля или внутри именованного предложения ограничения для одного или для нескольких полей с именем ограничения.</span><span class="sxs-lookup"><span data-stu-id="3a71f-132">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="3a71f-133">Тем не менее можно применить к полю ограничение NOT NULL только один раз.</span><span class="sxs-lookup"><span data-stu-id="3a71f-133">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="3a71f-134">Попытка использовать это ограничение более одного раза приводит к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="3a71f-134">Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="3a71f-135">При создании ВРЕМЕННОЙ таблицы, этот номер виден только в рамках сеанса, в котором он был создан.</span><span class="sxs-lookup"><span data-stu-id="3a71f-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="3a71f-136">Автоматически удаляется при завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="3a71f-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="3a71f-137">Доступ к временные таблицы может быть более одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3a71f-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="3a71f-138">Атрибут с СЖАТИЯ может использоваться только с символов и MEMO (также известной как текст) типы данных и синонимы.</span><span class="sxs-lookup"><span data-stu-id="3a71f-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="3a71f-139">Атрибут СЖАТИЯ с был добавлен для столбцов символов из-за изменения в формат представления символ Юникода.</span><span class="sxs-lookup"><span data-stu-id="3a71f-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="3a71f-140">Символы Юникода требуется два байта для каждого символа.</span><span class="sxs-lookup"><span data-stu-id="3a71f-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="3a71f-141">Для существующих баз данных Microsoft Jet, которые содержат преимущественно символ данные это означает, что файл базы данных практически в два раза и в размер при преобразовании формат ядра базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3a71f-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="3a71f-142">Тем не менее Юникод многих наборов знаков, которые ранее идентификаторами как однобайтовых знаков задает (их Изготовителей), можно легко сжатием на один байт.</span><span class="sxs-lookup"><span data-stu-id="3a71f-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="3a71f-143">При определении столбца символ с помощью этого атрибута данных будут сжатию автоматически при сохранении и восстанавливаться при получении из столбца.</span><span class="sxs-lookup"><span data-stu-id="3a71f-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="3a71f-144">Также можно определить MEMO столбцов для хранения данных в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="3a71f-144">MEMO columns can also be defined to store data in a compressed format.</span></span> <span data-ttu-id="3a71f-145">Однако существует ограничение.</span><span class="sxs-lookup"><span data-stu-id="3a71f-145">However, there is a limitation.</span></span> <span data-ttu-id="3a71f-146">Только экземпляры MEMO столбцов, если сжат, помещается в 4096 байт или меньше, сжимаются.</span><span class="sxs-lookup"><span data-stu-id="3a71f-146">Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed.</span></span> <span data-ttu-id="3a71f-147">Все остальные экземпляры столбцов MEMO останутся в обычном состоянии.</span><span class="sxs-lookup"><span data-stu-id="3a71f-147">All other instances of MEMO columns will remain uncompressed.</span></span> <span data-ttu-id="3a71f-148">Это означает, что в указанной таблице, для определенного столбца ЗАМЕТКА может сжатием некоторые данные и не сжимаются некоторые данные.</span><span class="sxs-lookup"><span data-stu-id="3a71f-148">This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="3a71f-149">Пример</span><span class="sxs-lookup"><span data-stu-id="3a71f-149">Example</span></span>

<span data-ttu-id="3a71f-150">В этом примере создается новая таблица с именем ThisTable с двух текстовых полей.</span><span class="sxs-lookup"><span data-stu-id="3a71f-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="3a71f-151">В этом примере создается новая таблица с именем MyTable с двух текстовых полей, поля даты/времени и уникальный индекс, состоящих из всех трех полей.</span><span class="sxs-lookup"><span data-stu-id="3a71f-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="3a71f-152">В этом примере создается новая таблица с двух текстовых полей и **целого** поля.</span><span class="sxs-lookup"><span data-stu-id="3a71f-152">This example creates a new table with two text fields and an **Integer** field.</span></span> <span data-ttu-id="3a71f-153">В поле SSN — основной ключ.</span><span class="sxs-lookup"><span data-stu-id="3a71f-153">The SSN field is the primary key.</span></span>

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
