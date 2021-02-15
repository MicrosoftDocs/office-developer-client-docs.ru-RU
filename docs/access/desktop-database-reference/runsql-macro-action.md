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
# <a name="runsql-macro-action"></a><span data-ttu-id="eef99-102">Макрокоманда RunSQL</span><span class="sxs-lookup"><span data-stu-id="eef99-102">RunSQL macro action</span></span>

<span data-ttu-id="eef99-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eef99-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eef99-104">Вы можете использовать действие **RunSQL** для выполнения запроса на действие Access с помощью соответствующего SQL.</span><span class="sxs-lookup"><span data-stu-id="eef99-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="eef99-105">Вы также можете выполнить запрос определения данных.</span><span class="sxs-lookup"><span data-stu-id="eef99-105">You can also run a data-definition query.</span></span>

> [!NOTE]
> <span data-ttu-id="eef99-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="eef99-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="eef99-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="eef99-107">Setting</span></span>

<span data-ttu-id="eef99-108">Действие **RunSQL** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="eef99-108">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eef99-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="eef99-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="eef99-110">Описание</span><span class="sxs-lookup"><span data-stu-id="eef99-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eef99-111"><strong>SQL Statement</strong></span><span class="sxs-lookup"><span data-stu-id="eef99-111"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="eef99-112">The SQL statement for the action query or data-definition query you want to run.</span><span class="sxs-lookup"><span data-stu-id="eef99-112">The SQL statement for the action query or data-definition query you want to run.</span></span> <span data-ttu-id="eef99-113">Максимальная длина этого заявления составляет 255 символов.</span><span class="sxs-lookup"><span data-stu-id="eef99-113">The maximum length of this statement is 255 characters.</span></span> <span data-ttu-id="eef99-114">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="eef99-114">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eef99-115"><strong>Использование транзакции</strong></span><span class="sxs-lookup"><span data-stu-id="eef99-115"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="eef99-116">Выберите <strong>"Да",</strong> чтобы включить этот запрос в транзакцию.</span><span class="sxs-lookup"><span data-stu-id="eef99-116">Select <strong>Yes</strong> to include this query in a transaction.</span></span> <span data-ttu-id="eef99-117">Выберите <strong>"Нет",</strong> если вы не хотите использовать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="eef99-117">Select <strong>No</strong> if you don't want to use a transaction.</span></span> <span data-ttu-id="eef99-118">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="eef99-118">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="eef99-119">Если для этого <strong>аргумента</strong> выбрано "Нет", запрос может работать быстрее.</span><span class="sxs-lookup"><span data-stu-id="eef99-119">If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="eef99-120">Заметки</span><span class="sxs-lookup"><span data-stu-id="eef99-120">Remarks</span></span>

<span data-ttu-id="eef99-121">Запросы действий можно использовать для приложения, удаления и обновления записей, а также для сохранения набора результатов запроса в качестве новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="eef99-121">You can use action queries to append, delete, and update records and to save a query's result set as a new table.</span></span> <span data-ttu-id="eef99-122">Запросы определения данных можно использовать для создания, изменения и удаления таблиц, а также для создания и удаления индексов.</span><span class="sxs-lookup"><span data-stu-id="eef99-122">You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes.</span></span> <span data-ttu-id="eef99-123">Действие **RunSQL** можно использовать для выполнения этих операций непосредственно из макроса без использования сохраненных запросов.</span><span class="sxs-lookup"><span data-stu-id="eef99-123">You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="eef99-124">Если требуется ввести SQL длиной более 255 символов, используйте метод **RunSQL** объекта **DoCmd** в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="eef99-124">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="eef99-125">В VBA можно ввести SQL до 32 768 символов.</span><span class="sxs-lookup"><span data-stu-id="eef99-125">You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="eef99-126">Запросы на доступ SQL, которые создаются при разработке запроса с помощью сетки конструктора в окне запроса.</span><span class="sxs-lookup"><span data-stu-id="eef99-126">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window.</span></span> <span data-ttu-id="eef99-127">В следующей таблице показаны запросы действий Access и запросы определения данных, а также соответствующие SQL данных.</span><span class="sxs-lookup"><span data-stu-id="eef99-127">The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eef99-128">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="eef99-128">Query type</span></span></p></th>
<th><p><span data-ttu-id="eef99-129">SQL</span><span class="sxs-lookup"><span data-stu-id="eef99-129">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eef99-130"><strong>Действие</strong></span><span class="sxs-lookup"><span data-stu-id="eef99-130"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eef99-131">Append</span><span class="sxs-lookup"><span data-stu-id="eef99-131">Append</span></span></p></td>
<td><p><span data-ttu-id="eef99-132">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="eef99-132">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eef99-133">Удаление</span><span class="sxs-lookup"><span data-stu-id="eef99-133">Delete</span></span></p></td>
<td><p><span data-ttu-id="eef99-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="eef99-134">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eef99-135">Make-table</span><span class="sxs-lookup"><span data-stu-id="eef99-135">Make-table</span></span></p></td>
<td><p><span data-ttu-id="eef99-136">SELECT... INTO</span><span class="sxs-lookup"><span data-stu-id="eef99-136">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eef99-137">Update</span><span class="sxs-lookup"><span data-stu-id="eef99-137">Update</span></span></p></td>
<td><p><span data-ttu-id="eef99-138">UPDATE</span><span class="sxs-lookup"><span data-stu-id="eef99-138">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eef99-139"><strong>Определение данных (SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="eef99-139"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eef99-140">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="eef99-140">Create a table</span></span></p></td>
<td><p><span data-ttu-id="eef99-141">СОЗДАНИЕ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="eef99-141">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eef99-142">Изменение таблицы</span><span class="sxs-lookup"><span data-stu-id="eef99-142">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="eef99-143">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="eef99-143">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eef99-144">Удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="eef99-144">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="eef99-145">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="eef99-145">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eef99-146">Создание индекса</span><span class="sxs-lookup"><span data-stu-id="eef99-146">Create an index</span></span></p></td>
<td><p><span data-ttu-id="eef99-147">СОЗДАНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="eef99-147">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eef99-148">Удаление индекса</span><span class="sxs-lookup"><span data-stu-id="eef99-148">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="eef99-149">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="eef99-149">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eef99-150">Вы также можете использовать предложение IN с этими заявлениями для изменения данных в другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="eef99-150">You can also use an IN clause with these statements to modify data in another database.</span></span>

> [!NOTE]
> <span data-ttu-id="eef99-151">Чтобы выполнить запрос на выборку или перекрестный запрос из макроса, используйте аргумент View действия **OpenQuery,** чтобы открыть существующий запрос на выборку или перекрестный запрос в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="eef99-151">To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view.</span></span> <span data-ttu-id="eef99-152">Вы также можете запускать существующие запросы действий и SQL определенным образом.</span><span class="sxs-lookup"><span data-stu-id="eef99-152">You can also run existing action queries and SQL-specific queries in the same way.</span></span>
