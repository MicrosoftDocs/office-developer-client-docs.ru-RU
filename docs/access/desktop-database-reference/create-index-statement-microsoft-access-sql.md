---
title: Инструкция CREATE INDEX (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1b12fcf4d92bbe0949065557973efe94688a7a30
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937206"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="0a069-102">Инструкция CREATE INDEX (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0a069-102">CREATE INDEX statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="0a069-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a069-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a069-104">Создает новый индекс на существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="0a069-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="0a069-105">Для баз данных ядра базы данных Microsoft Access ядро базы данных Microsoft Access не поддерживает использование CREATE INDEX (за исключением создания псевдоиндекса на связанная таблица ODBC) и любых других инструкций языка (DDL).</span><span class="sxs-lookup"><span data-stu-id="0a069-105">For non-Microsoft Access database engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="0a069-106">Используйте методы DAO **Создать** .</span><span class="sxs-lookup"><span data-stu-id="0a069-106">Use the DAO **Create** methods instead.</span></span> <span data-ttu-id="0a069-107">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0a069-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a069-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a069-108">Syntax</span></span>

<span data-ttu-id="0a069-109">Создание \[ UNIQUE \] д *индекса* ИНДЕКСА *в таблице* (*поле* \[ASC | DESC\]\[, *поле* \[ASC | DESC\],... \]) \[WITH {ОСНОВНОЙ | DISALLOW NULL | ПРОПУСК NULL}\]</span><span class="sxs-lookup"><span data-stu-id="0a069-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span></span>

<span data-ttu-id="0a069-110">Инструкция CREATE INDEX состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="0a069-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a069-111">Часть</span><span class="sxs-lookup"><span data-stu-id="0a069-111">Part</span></span></p></th>
<th><p><span data-ttu-id="0a069-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0a069-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a069-113"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="0a069-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="0a069-114">Имя индекс, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="0a069-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a069-115"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="0a069-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="0a069-116">Имя существующей таблицы, которая будет содержать индекс.</span><span class="sxs-lookup"><span data-stu-id="0a069-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a069-117"><em>поля</em></span><span class="sxs-lookup"><span data-stu-id="0a069-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="0a069-118">Имя поля для индексирования.</span><span class="sxs-lookup"><span data-stu-id="0a069-118">The name of the field or fields to be indexed.</span></span> <span data-ttu-id="0a069-119">Чтобы создать индекс по одному полю, укажите имя поля в скобках после имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="0a069-119">To create a single-field index, list the field name in parentheses following the table name.</span></span> <span data-ttu-id="0a069-120">Чтобы создать составной индекс, укажите имена всех полей, включаемых в индекс.</span><span class="sxs-lookup"><span data-stu-id="0a069-120">To create a multiple-field index, list the name of each field to be included in the index.</span></span> <span data-ttu-id="0a069-121">Для создания индексов по убыванию используйте слово DESC; в противном случае индексов предполагается, что будет по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="0a069-121">To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0a069-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a069-122">Remarks</span></span>

<span data-ttu-id="0a069-123">Чтобы запретить повторяющиеся значения в одном или нескольких индексированных полей различные записи, используйте УНИКАЛЬНОЕ зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="0a069-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="0a069-124">В необязательном с предложения может задать правила проверки данных.</span><span class="sxs-lookup"><span data-stu-id="0a069-124">In the optional WITH clause, you can enforce data validation rules.</span></span> <span data-ttu-id="0a069-125">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0a069-125">You can:</span></span>

- <span data-ttu-id="0a069-126">Запретить Null записей в одном или нескольких индексированных полях для новых записей с помощью параметра DISALLOW NULL.</span><span class="sxs-lookup"><span data-stu-id="0a069-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="0a069-127">Запретить **пустые** записи в индексированные поля или полей, включенных в индекс с помощью параметра IGNORE NULL.</span><span class="sxs-lookup"><span data-stu-id="0a069-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="0a069-128">Назначьте индексированных полей или поля в качестве первичного ключа с помощью ОСНОВНОЙ зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="0a069-128">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word.</span></span> <span data-ttu-id="0a069-129">Это означает, что ключ является уникальным, поэтому можно опустить УНИКАЛЬНЫЙ зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="0a069-129">This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="0a069-130">CREATE INDEX можно использовать для создания псевдоиндекса в связанной таблицы в источник данных ODBC, например Microsoft SQL Server, который не имеет индекса.</span><span class="sxs-lookup"><span data-stu-id="0a069-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft SQL Server, that does not already have an index.</span></span> <span data-ttu-id="0a069-131">Нет необходимости разрешения и доступ к удаленному серверу для создания псевдоиндекса и удаленной базы данных не и не затрагиваются псевдоиндекса.</span><span class="sxs-lookup"><span data-stu-id="0a069-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="0a069-132">Используйте тот же синтаксис для связанных и оригинальных таблиц.</span><span class="sxs-lookup"><span data-stu-id="0a069-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="0a069-133">Создание виртуального индекса в таблице, которая будет использоваться только для чтения может быть особенно полезным.</span><span class="sxs-lookup"><span data-stu-id="0a069-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="0a069-134">Можно также использовать инструкцию [ALTER](alter-table-statement-microsoft-access-sql.md) для добавления одного или нескольких полей индекса в таблицу и инструкцию ALTER или инструкции [DROP](drop-statement-microsoft-access-sql.md) можно использовать для удаления индекса, созданных с помощью ALTER TABLE или CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="0a069-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="0a069-135">Не используйте ОСНОВНОЙ зарезервированным словом при создании нового индекса в таблице, уже имеет первичный ключ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0a069-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="0a069-136">Пример</span><span class="sxs-lookup"><span data-stu-id="0a069-136">Example</span></span>

<span data-ttu-id="0a069-137">В этом примере создается индекс, состоящий из поля домашний телефон и расширение в таблице сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0a069-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="0a069-138">В этом примере создается индекса на таблице Customers, с помощью поля CustomerID.</span><span class="sxs-lookup"><span data-stu-id="0a069-138">This example creates an index on the Customers table using the CustomerID field.</span></span> <span data-ttu-id="0a069-139">Две записи не могут иметь те же данные в поле CustomerID и значения Null не разрешены.</span><span class="sxs-lookup"><span data-stu-id="0a069-139">No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
