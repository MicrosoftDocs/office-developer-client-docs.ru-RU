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
ms.openlocfilehash: 0527f5a55235fa36725152d228dfd2294c63bf53
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996876"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="a1b9c-102">Макрокоманда RunSQL</span><span class="sxs-lookup"><span data-stu-id="a1b9c-102">RunSQL macro action</span></span>

<span data-ttu-id="a1b9c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1b9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1b9c-104">**Макрокоманды ЗапускЗапросаSQL** можно использовать для выполнения запроса действие Access с помощью соответствующего оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="a1b9c-105">Также можно запустить управляющий запрос.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-105">You can also run a data-definition query.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b9c-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="a1b9c-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="a1b9c-107">Setting</span></span>

<span data-ttu-id="a1b9c-108">**Макрокоманды ЗапускЗапросаSQL** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-108">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1b9c-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a1b9c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a1b9c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a1b9c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-111"><strong>Оператор SQL</strong></span><span class="sxs-lookup"><span data-stu-id="a1b9c-111"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b9c-112">Инструкции SQL для запроса или управляющий запрос будет запущена.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-112">The SQL statement for the action query or data-definition query you want to run.</span></span> <span data-ttu-id="a1b9c-113">Максимальная длина этого оператора составляет 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-113">The maximum length of this statement is 255 characters.</span></span> <span data-ttu-id="a1b9c-114">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-114">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b9c-115"><strong>Использование транзакций</strong></span><span class="sxs-lookup"><span data-stu-id="a1b9c-115"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="a1b9c-116">Выберите <strong>Да,</strong> Чтобы включить этот запрос в транзакции.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-116">Select <strong>Yes</strong> to include this query in a transaction.</span></span> <span data-ttu-id="a1b9c-117">Выберите <strong>Нет,</strong> Если вы не хотите использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-117">Select <strong>No</strong> if you don't want to use a transaction.</span></span> <span data-ttu-id="a1b9c-118">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-118">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="a1b9c-119">Если выбран вариант <strong>Нет</strong> для этого аргумента, запрос может выполняться быстрее.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-119">If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a1b9c-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1b9c-120">Remarks</span></span>

<span data-ttu-id="a1b9c-121">Можно использовать запросы на добавление, удаление и обновление записей и сохранить как новую таблицу результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-121">You can use action queries to append, delete, and update records and to save a query's result set as a new table.</span></span> <span data-ttu-id="a1b9c-122">Определение данных запросов можно использовать создавать, изменять и удалять таблицы, а также создавать и удалять индексы.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-122">You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes.</span></span> <span data-ttu-id="a1b9c-123">**Макрокоманды ЗапускЗапросаSQL** можно использовать для выполнения этих операций в макросе без необходимости использования сохраненных запросов.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-123">You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="a1b9c-124">Если требуется ввести инструкции SQL более 255 символов, используйте метод **RunSQL** **объекта** в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-124">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="a1b9c-125">Можно ввести инструкций SQL длиной до 32 768 символов в VBA.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-125">You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="a1b9c-126">Запросы доступа, фактически инструкций SQL, созданных при создании запроса с помощью конструктора сетки в окно запроса.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-126">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window.</span></span> <span data-ttu-id="a1b9c-127">В следующей таблице показаны запросы доступа и данных, а также соответствующие им инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-127">The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1b9c-128">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="a1b9c-128">Query type</span></span></p></th>
<th><p><span data-ttu-id="a1b9c-129">Оператор SQL</span><span class="sxs-lookup"><span data-stu-id="a1b9c-129">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-130"><strong>Действие</strong></span><span class="sxs-lookup"><span data-stu-id="a1b9c-130"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b9c-131">Добавление</span><span class="sxs-lookup"><span data-stu-id="a1b9c-131">Append</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-132">ВСТАВКА В</span><span class="sxs-lookup"><span data-stu-id="a1b9c-132">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-133">Delete</span><span class="sxs-lookup"><span data-stu-id="a1b9c-133">Delete</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="a1b9c-134">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b9c-135">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="a1b9c-135">Make-table</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-136">ВЫБЕРИТЕ... В</span><span class="sxs-lookup"><span data-stu-id="a1b9c-136">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-137">Update</span><span class="sxs-lookup"><span data-stu-id="a1b9c-137">Update</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-138">ОБНОВЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1b9c-138">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b9c-139"><strong>Управляющий (относящиеся к SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="a1b9c-139"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-140">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="a1b9c-140">Create a table</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-141">СОЗДАНИЕ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="a1b9c-141">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b9c-142">Изменение таблицы</span><span class="sxs-lookup"><span data-stu-id="a1b9c-142">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-143">ИЗМЕНЕНИЯ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="a1b9c-143">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-144">Удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="a1b9c-144">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-145">УДАЛЕНИЕ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="a1b9c-145">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1b9c-146">Создание индекса</span><span class="sxs-lookup"><span data-stu-id="a1b9c-146">Create an index</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-147">СОЗДАНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="a1b9c-147">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1b9c-148">Удаление индекса</span><span class="sxs-lookup"><span data-stu-id="a1b9c-148">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="a1b9c-149">УДАЛЕНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="a1b9c-149">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1b9c-150">Можно также использовать предложения в эти инструкции для изменения данных в другую базу данных.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-150">You can also use an IN clause with these statements to modify data in another database.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b9c-151">Для запуска запроса или перекрестного запроса из макросов, используйте представление, выберите аргумент **ОткрытьЗапрос для открытия существующего** запроса или перекрестный запрос в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-151">To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view.</span></span> <span data-ttu-id="a1b9c-152">Также можно запустить существующие запросы на изменение и запросы SQL так же, как.</span><span class="sxs-lookup"><span data-stu-id="a1b9c-152">You can also run existing action queries and SQL-specific queries in the same way.</span></span>
