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
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295431"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="58f8a-102">Инструкция CREATE INDEX (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="58f8a-102">CREATE INDEX Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="58f8a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="58f8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="58f8a-104">Создает новый индекс в существующей таблице.</span><span class="sxs-lookup"><span data-stu-id="58f8a-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="58f8a-105">Ядро СУБД Microsoft Access не поддерживает использование CREATE INDEX (кроме как для создания псевдоиндекса в связанной таблице ODBC) или любых других инструкций DDL с базами данных, которые не основаны на ядре СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="58f8a-105">For non-Microsoft Access database engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="58f8a-106">Используйте вместо этого методы DAO **Create**.</span><span class="sxs-lookup"><span data-stu-id="58f8a-106">Use the DAO **Create** methods instead.</span></span> <span data-ttu-id="58f8a-107">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="58f8a-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58f8a-108">Syntax</span></span>

<span data-ttu-id="58f8a-109">CREATE \[ UNIQUE \] INDEX *индекс* ON *таблица* (*поле* \[ASC|DESC\]\[, *поле* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span><span class="sxs-lookup"><span data-stu-id="58f8a-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span></span>

<span data-ttu-id="58f8a-110">Инструкция CREATE INDEX включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="58f8a-110">The CREATE PROCEDURE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58f8a-111">Часть</span><span class="sxs-lookup"><span data-stu-id="58f8a-111">Part</span></span></p></th>
<th><p><span data-ttu-id="58f8a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="58f8a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58f8a-113"><em>индекс</em></span><span class="sxs-lookup"><span data-stu-id="58f8a-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="58f8a-114">Имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="58f8a-114">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58f8a-115"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="58f8a-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="58f8a-116">Имя существующей таблицы, в которой будет создан индекс.</span><span class="sxs-lookup"><span data-stu-id="58f8a-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58f8a-117"><em>поле</em></span><span class="sxs-lookup"><span data-stu-id="58f8a-117"><em>Field</em></span></span></p></td>
<td><p><span data-ttu-id="58f8a-118">Имя одного или нескольких полей для индексации.</span><span class="sxs-lookup"><span data-stu-id="58f8a-118">The name of the field or fields to be designated the primary key.</span></span> <span data-ttu-id="58f8a-119">Чтобы создать индекс по одному полю, укажите имя поля в круглых скобках после имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="58f8a-119">To create a single-field index, list the field name in parentheses following the table name.</span></span> <span data-ttu-id="58f8a-120">Чтобы создать индекс по нескольким полям, укажите имена всех полей, включаемых в индекс.</span><span class="sxs-lookup"><span data-stu-id="58f8a-120">To create a multiple-field index, list the name of each field to be included in the index.</span></span> <span data-ttu-id="58f8a-121">Чтобы создать индексы с упорядочением по убыванию, используйте зарезервированное слово DESC; в противном случае будут созданы индексы с упорядочением по возрастанию.</span><span class="sxs-lookup"><span data-stu-id="58f8a-121">To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="58f8a-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="58f8a-122">Remarks</span></span>

<span data-ttu-id="58f8a-123">Чтобы запретить появление повторяющихся значений в одном или нескольких индексированных полях, используйте зарезервированное слово UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="58f8a-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="58f8a-124">Чтобы определить правила проверки данных, можно использовать необязательное предложение WITH.</span><span class="sxs-lookup"><span data-stu-id="58f8a-124">In the optional WITH clause, you can enforce data validation rules.</span></span> <span data-ttu-id="58f8a-125">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="58f8a-125">You can:</span></span>

- <span data-ttu-id="58f8a-126">Запретить значения NULL в индексированных полях новых записей с помощью параметра DISALLOW NULL.</span><span class="sxs-lookup"><span data-stu-id="58f8a-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="58f8a-127">Предотвратить индексирование записей со значениями **NULL** в одном или нескольких индексированных полях с помощью параметра IGNORE NULL.</span><span class="sxs-lookup"><span data-stu-id="58f8a-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="58f8a-128">Определить одно или несколько индексированных полей в качестве первичного ключа с помощью зарезервированного слова PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="58f8a-128">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word.</span></span> <span data-ttu-id="58f8a-129">Поскольку подразумевается, что первичный ключ уникален, зарезервированное слово UNIQUE можно опустить.</span><span class="sxs-lookup"><span data-stu-id="58f8a-129">This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="58f8a-130">Инструкция CREATE INDEX может быть использована для создания псевдоиндекса в связанной таблице источника данных ODBC, такого как Microsoft SQL Server, если в ней еще нет индекса.</span><span class="sxs-lookup"><span data-stu-id="58f8a-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft SQL Server, that does not already have an index.</span></span> <span data-ttu-id="58f8a-131">Для создания псевдоиндекса не требуется разрешения или доступа к удаленному серверу, а на удаленном сервере никак не отразится наличие псевдоиндекса.</span><span class="sxs-lookup"><span data-stu-id="58f8a-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="58f8a-132">Для связанных и исходных таблиц используется один и тот же синтаксис.</span><span class="sxs-lookup"><span data-stu-id="58f8a-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="58f8a-133">Особенно полезным может быть создание псевдоиндекса в таблице, которая будет использоваться преимущественно для чтения.</span><span class="sxs-lookup"><span data-stu-id="58f8a-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="58f8a-134">Чтобы добавить индекс по одному полю или по набору полей в таблице, можно также воспользоваться инструкцией [ALTER TABLE](alter-table-statement-microsoft-access-sql.md). Чтобы удалить индекс, созданный с помощью инструкции ALTER TABLE или CREATE INDEX, можно воспользоваться инструкцией ALTER TABLE или [DROP](drop-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="58f8a-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="58f8a-135">Если в таблице уже есть первичный ключ, не используйте зарезервированное слово PRIMARY при создании в ней нового индекса: это приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="58f8a-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="58f8a-136">Пример</span><span class="sxs-lookup"><span data-stu-id="58f8a-136">Example</span></span>

<span data-ttu-id="58f8a-137">В этом примере создается индекс, состоящий из полей Home Phone (Домашний телефон) и Extension (Расширение) в таблице Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="58f8a-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

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

<span data-ttu-id="58f8a-138">В этом примере создается индекс в таблице Customers (Клиенты) с помощью поля CustomerID (КодКлиента).</span><span class="sxs-lookup"><span data-stu-id="58f8a-138">This example creates an index on the Customers table using the CustomerID field.</span></span> <span data-ttu-id="58f8a-139">Никакие две записи не могут содержать одинаковые данные в поле CustomerID (КодКлиента), и не допускаются значения NULL.</span><span class="sxs-lookup"><span data-stu-id="58f8a-139">No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

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
