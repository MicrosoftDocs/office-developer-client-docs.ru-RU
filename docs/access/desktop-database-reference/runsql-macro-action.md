---
title: Макрокоманда RunSQL
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308997"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="352f8-102">Макрокоманда RunSQL</span><span class="sxs-lookup"><span data-stu-id="352f8-102">RunSQL macro action</span></span>

<span data-ttu-id="352f8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="352f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="352f8-104">Вы можете использовать действие **рунскл** для выполнения запроса на изменение с помощью соответствующего оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="352f8-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="352f8-105">Кроме того, можно выполнить запрос определения данных.</span><span class="sxs-lookup"><span data-stu-id="352f8-105">You can also run a data-definition query.</span></span>

> [!NOTE]
> <span data-ttu-id="352f8-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="352f8-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="352f8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="352f8-107">Setting</span></span>

<span data-ttu-id="352f8-108">Макрокоманда **рунскл** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="352f8-108">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="352f8-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="352f8-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="352f8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="352f8-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352f8-111"><strong>Оператор SQL</strong></span><span class="sxs-lookup"><span data-stu-id="352f8-111"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="352f8-112">Инструкция SQL для запроса на изменение или запроса на определение данных, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="352f8-112">The SQL statement for the action query or data-definition query you want to run.</span></span> <span data-ttu-id="352f8-113">Максимальная длина этого оператора составляет 255 символов.</span><span class="sxs-lookup"><span data-stu-id="352f8-113">The maximum length of this statement is 255 characters.</span></span> <span data-ttu-id="352f8-114">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="352f8-114">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f8-115"><strong>Использование транзакции</strong></span><span class="sxs-lookup"><span data-stu-id="352f8-115"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="352f8-116">Выберите <strong>Да</strong> , чтобы включить этот запрос в транзакцию.</span><span class="sxs-lookup"><span data-stu-id="352f8-116">Select <strong>Yes</strong> to include this query in a transaction.</span></span> <span data-ttu-id="352f8-117">Если вы не хотите использовать транзакцию, выберите <strong>нет</strong> .</span><span class="sxs-lookup"><span data-stu-id="352f8-117">Select <strong>No</strong> if you don't want to use a transaction.</span></span> <span data-ttu-id="352f8-118">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="352f8-118">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="352f8-119">Если для этого аргумента выбрано значение <strong>нет</strong> , запрос может выполняться быстрее.</span><span class="sxs-lookup"><span data-stu-id="352f8-119">If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="352f8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="352f8-120">Remarks</span></span>

<span data-ttu-id="352f8-121">Запросы на изменение можно использовать для добавления, удаления и обновления записей, а также для сохранения набора результатов запроса в виде новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="352f8-121">You can use action queries to append, delete, and update records and to save a query's result set as a new table.</span></span> <span data-ttu-id="352f8-122">С помощью запросов на определение данных можно создавать, изменять и удалять таблицы, а также создавать и удалять индексы.</span><span class="sxs-lookup"><span data-stu-id="352f8-122">You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes.</span></span> <span data-ttu-id="352f8-123">Вы можете использовать действие **рунскл** для выполнения этих операций непосредственно из макроса без необходимости использовать сохраненные запросы.</span><span class="sxs-lookup"><span data-stu-id="352f8-123">You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="352f8-124">Если необходимо ввести инструкцию SQL длиннее 255 символов, используйте метод **рунскл** объекта DoCmd в модуле \*\*\*\* Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="352f8-124">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="352f8-125">В VBA можно вводить инструкции SQL длиной до 32 768 символов.</span><span class="sxs-lookup"><span data-stu-id="352f8-125">You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="352f8-126">Запросы Access фактически являются операторами SQL, которые создаются при проектировании запроса с помощью сетки конструктора в окне запроса.</span><span class="sxs-lookup"><span data-stu-id="352f8-126">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window.</span></span> <span data-ttu-id="352f8-127">В приведенной ниже таблице показаны запросы на доступ и запросы на определение данных и соответствующие инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="352f8-127">The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="352f8-128">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="352f8-128">Query type</span></span></p></th>
<th><p><span data-ttu-id="352f8-129">Оператор SQL</span><span class="sxs-lookup"><span data-stu-id="352f8-129">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352f8-130"><strong>Действие</strong></span><span class="sxs-lookup"><span data-stu-id="352f8-130"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f8-131">Error</span><span class="sxs-lookup"><span data-stu-id="352f8-131">Append</span></span></p></td>
<td><p><span data-ttu-id="352f8-132">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="352f8-132">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f8-133">Delete</span><span class="sxs-lookup"><span data-stu-id="352f8-133">Delete</span></span></p></td>
<td><p><span data-ttu-id="352f8-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="352f8-134">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f8-135">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="352f8-135">Make-table</span></span></p></td>
<td><p><span data-ttu-id="352f8-136">Выберите... РАЗДЕЛЯЕТ</span><span class="sxs-lookup"><span data-stu-id="352f8-136">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f8-137">Update</span><span class="sxs-lookup"><span data-stu-id="352f8-137">Update</span></span></p></td>
<td><p><span data-ttu-id="352f8-138">UPDATE</span><span class="sxs-lookup"><span data-stu-id="352f8-138">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f8-139"><strong>Определение данных (только для SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="352f8-139"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f8-140">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="352f8-140">Create a table</span></span></p></td>
<td><p><span data-ttu-id="352f8-141">СОЗДАНИЕ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="352f8-141">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f8-142">Изменение таблицы</span><span class="sxs-lookup"><span data-stu-id="352f8-142">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="352f8-143">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="352f8-143">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f8-144">Удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="352f8-144">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="352f8-145">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="352f8-145">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f8-146">Создание индекса</span><span class="sxs-lookup"><span data-stu-id="352f8-146">Create an index</span></span></p></td>
<td><p><span data-ttu-id="352f8-147">СОЗДАНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="352f8-147">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f8-148">Удаление индекса</span><span class="sxs-lookup"><span data-stu-id="352f8-148">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="352f8-149">УДАЛЕНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="352f8-149">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="352f8-150">Кроме того, можно использовать предложение IN с этими операторами для изменения данных в другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="352f8-150">You can also use an IN clause with these statements to modify data in another database.</span></span>

> [!NOTE]
> <span data-ttu-id="352f8-151">Чтобы запустить запрос на выборку или перекрестный запрос из макроса, используйте аргумент View действия **OPENQUERY** , чтобы открыть существующий запрос на выборку или перекрестный запрос в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="352f8-151">To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view.</span></span> <span data-ttu-id="352f8-152">Вы также можете выполнять существующие запросы на действия и запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="352f8-152">You can also run existing action queries and SQL-specific queries in the same way.</span></span>
