---
title: RunSQL Macro Action
TOCTitle: RunSQL Macro Action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ff4a363f6fbb05af582767f4b664f71f34d23357
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479819"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="40a4b-102">RunSQL Macro Action</span><span class="sxs-lookup"><span data-stu-id="40a4b-102">RunSQL Macro Action</span></span>


<span data-ttu-id="40a4b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40a4b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40a4b-104">**Макрокоманды ЗапускЗапросаSQL** можно использовать для выполнения запроса действие Access с помощью соответствующего оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="40a4b-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="40a4b-105">Также можно запустить управляющий запрос.</span><span class="sxs-lookup"><span data-stu-id="40a4b-105">You can also run a data-definition query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="40a4b-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="40a4b-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="40a4b-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="40a4b-108">Setting</span></span>

<span data-ttu-id="40a4b-109">**Макрокоманды ЗапускЗапросаSQL** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="40a4b-109">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40a4b-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="40a4b-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="40a4b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="40a4b-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-112"><strong>Оператор SQL</strong></span><span class="sxs-lookup"><span data-stu-id="40a4b-112"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="40a4b-113">Инструкции SQL для запроса или управляющий запрос будет запущена.</span><span class="sxs-lookup"><span data-stu-id="40a4b-113">The SQL statement for the action query or data-definition query you want to run.</span></span> <span data-ttu-id="40a4b-114">Максимальная длина этого оператора составляет 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="40a4b-114">The maximum length of this statement is 255 characters.</span></span> <span data-ttu-id="40a4b-115">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="40a4b-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a4b-116"><strong>Использование транзакций</strong></span><span class="sxs-lookup"><span data-stu-id="40a4b-116"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="40a4b-117">Выберите <strong>Да,</strong> Чтобы включить этот запрос в транзакции.</span><span class="sxs-lookup"><span data-stu-id="40a4b-117">Select <strong>Yes</strong> to include this query in a transaction.</span></span> <span data-ttu-id="40a4b-118">Выберите <strong>Нет,</strong> Если вы не хотите использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="40a4b-118">Select <strong>No</strong> if you don't want to use a transaction.</span></span> <span data-ttu-id="40a4b-119">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="40a4b-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="40a4b-120">Если выбран вариант <strong>Нет</strong> для этого аргумента, запрос может выполняться быстрее.</span><span class="sxs-lookup"><span data-stu-id="40a4b-120">If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="40a4b-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="40a4b-121">Remarks</span></span>

<span data-ttu-id="40a4b-122">Можно использовать запросы на добавление, удаление и обновление записей и сохранить как новую таблицу результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="40a4b-122">You can use action queries to append, delete, and update records and to save a query's result set as a new table.</span></span> <span data-ttu-id="40a4b-123">Определение данных запросов можно использовать создавать, изменять и удалять таблицы, а также создавать и удалять индексы.</span><span class="sxs-lookup"><span data-stu-id="40a4b-123">You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes.</span></span> <span data-ttu-id="40a4b-124">**Макрокоманды ЗапускЗапросаSQL** можно использовать для выполнения этих операций в макросе без необходимости использования сохраненных запросов.</span><span class="sxs-lookup"><span data-stu-id="40a4b-124">You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="40a4b-125">Если требуется ввести инструкции SQL более 255 символов, используйте метод **RunSQL** **объекта** в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="40a4b-125">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="40a4b-126">Можно ввести инструкций SQL длиной до 32 768 символов в VBA.</span><span class="sxs-lookup"><span data-stu-id="40a4b-126">You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="40a4b-127">Запросы доступа, фактически инструкций SQL, созданных при создании запроса с помощью конструктора сетки в окно запроса.</span><span class="sxs-lookup"><span data-stu-id="40a4b-127">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window.</span></span> <span data-ttu-id="40a4b-128">В следующей таблице показаны запросы доступа и данных, а также соответствующие им инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="40a4b-128">The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40a4b-129">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="40a4b-129">Query type</span></span></p></th>
<th><p><span data-ttu-id="40a4b-130">Оператор SQL</span><span class="sxs-lookup"><span data-stu-id="40a4b-130">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-131"><strong>Действие</strong></span><span class="sxs-lookup"><span data-stu-id="40a4b-131"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a4b-132">Добавление</span><span class="sxs-lookup"><span data-stu-id="40a4b-132">Append</span></span></p></td>
<td><p><span data-ttu-id="40a4b-133">ВСТАВКА В</span><span class="sxs-lookup"><span data-stu-id="40a4b-133">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-134">Delete</span><span class="sxs-lookup"><span data-stu-id="40a4b-134">Delete</span></span></p></td>
<td><p><span data-ttu-id="40a4b-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="40a4b-135">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a4b-136">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="40a4b-136">Make-table</span></span></p></td>
<td><p><span data-ttu-id="40a4b-137">ВЫБЕРИТЕ... В</span><span class="sxs-lookup"><span data-stu-id="40a4b-137">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-138">Update</span><span class="sxs-lookup"><span data-stu-id="40a4b-138">Update</span></span></p></td>
<td><p><span data-ttu-id="40a4b-139">ОБНОВЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40a4b-139">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a4b-140"><strong>Управляющий (относящиеся к SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="40a4b-140"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-141">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="40a4b-141">Create a table</span></span></p></td>
<td><p><span data-ttu-id="40a4b-142">СОЗДАНИЕ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="40a4b-142">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a4b-143">Изменение таблицы</span><span class="sxs-lookup"><span data-stu-id="40a4b-143">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="40a4b-144">ИЗМЕНЕНИЯ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="40a4b-144">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-145">Удаление таблицы</span><span class="sxs-lookup"><span data-stu-id="40a4b-145">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="40a4b-146">УДАЛЕНИЕ ТАБЛИЦЫ</span><span class="sxs-lookup"><span data-stu-id="40a4b-146">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a4b-147">Создание индекса</span><span class="sxs-lookup"><span data-stu-id="40a4b-147">Create an index</span></span></p></td>
<td><p><span data-ttu-id="40a4b-148">СОЗДАНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="40a4b-148">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a4b-149">Удаление индекса</span><span class="sxs-lookup"><span data-stu-id="40a4b-149">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="40a4b-150">УДАЛЕНИЕ ИНДЕКСА</span><span class="sxs-lookup"><span data-stu-id="40a4b-150">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40a4b-151">Можно также использовать предложения в эти инструкции для изменения данных в другую базу данных.</span><span class="sxs-lookup"><span data-stu-id="40a4b-151">You can also use an IN clause with these statements to modify data in another database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="40a4b-152">Для запуска запроса или перекрестного запроса из макросов, используйте представление, выберите аргумент <STRONG>ОткрытьЗапрос для открытия существующего</STRONG> запроса или перекрестный запрос в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="40a4b-152">To run a select query or crosstab query from a macro, use the View argument of the <STRONG>OpenQuery</STRONG> action to open an existing select query or crosstab query in Datasheet view.</span></span> <span data-ttu-id="40a4b-153">Также можно запустить существующие запросы на изменение и запросы SQL так же, как.</span><span class="sxs-lookup"><span data-stu-id="40a4b-153">You can also run existing action queries and SQL-specific queries in the same way.</span></span></P>


