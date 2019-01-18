---
title: Макрокоманда SearchForRecord
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: efa763a77250e1d5c617358f31421804c772468b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702112"
---
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="8dbc1-102">Макрокоманда SearchForRecord</span><span class="sxs-lookup"><span data-stu-id="8dbc1-102">SearchForRecord macro action</span></span>


<span data-ttu-id="8dbc1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dbc1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8dbc1-104">Можно использовать действие **ПоискЗаписи** поиск определенной записи в таблице, запрос, форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="8dbc1-105">Setting</span><span class="sxs-lookup"><span data-stu-id="8dbc1-105">Setting</span></span>

<span data-ttu-id="8dbc1-106">Действие **ПоискЗаписи** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8dbc1-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="8dbc1-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8dbc1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8dbc1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dbc1-109"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-110">Введите или выберите тип объекта базы данных выполняется поиск в.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-110">Enter or select the type of database object that you are searching in.</span></span> <span data-ttu-id="8dbc1-111">Можно выбрать <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>или <strong>отчета</strong>.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-111">You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dbc1-112"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-113">Введите или выберите объект, содержащий записи для поиска.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-113">Enter or select the specific object that contains the record to search for.</span></span> <span data-ttu-id="8dbc1-114">Раскрывающемся списке содержит все объекты базы данных, выбранного для аргумента <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-114">The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dbc1-115"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-116">Укажите начальную точку и направление поиска.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8dbc1-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="8dbc1-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="8dbc1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8dbc1-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dbc1-119"><strong>Previous</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-120">Поиска в обратном направлении от текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dbc1-121"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-122">Поиск вперед из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8dbc1-123"><strong>First</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-124">Поиск вперед из первой записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-124">Search forward from the first record.</span></span> <span data-ttu-id="8dbc1-125">Это значение по умолчанию для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-125">This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dbc1-126"><strong>Last</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-127">Поиска в обратном направлении от последней записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dbc1-128"><strong>Условие отбора</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-129">Введите условия поиска, используя тот же синтаксис как предложение SQL WHERE только без слова &quot;ГДЕ&quot;.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="8dbc1-130">Например:</span><span class="sxs-lookup"><span data-stu-id="8dbc1-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="8dbc1-131">Чтобы создать условия, которое содержит значение из текстового поля в форме, необходимо создать выражение, которое объединяет первая часть критерий с именем текстовое поле, содержащее значение для поиска.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="8dbc1-132">Например следующий критерий выполняет поиск поле Описание для значения в текстовом поле с именем txtDescription на форму с именем frmCategories.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="8dbc1-133">Обратите внимание, знак равенства (<strong>=</strong>) в начале выражения и использование по обеим сторонам от ссылку текстовое поле в одинарные кавычки (<strong></strong>'):</span><span class="sxs-lookup"><span data-stu-id="8dbc1-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8dbc1-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="8dbc1-134">Remarks</span></span>

- <span data-ttu-id="8dbc1-135">В случаях, когда несколько записей совпадает критерии в аргументе **Условие** влияют следующие факторы найдено записей:</span><span class="sxs-lookup"><span data-stu-id="8dbc1-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="8dbc1-136">**Значение аргумента записи** В разделе таблицы в разделе Параметры Дополнительные сведения о **записи** аргумента.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-136">**The Record argument setting**See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="8dbc1-137">**Порядок сортировки записей** Например если аргумент **запись** имеет значение **первой**, изменение порядка сортировки записей может изменяться найдено записей.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-137">**The sort order of the records**For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="8dbc1-138">Объект, указанный в аргументе **Имя объекта** необходимо открыть перед выполнением этой операции.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-138">The object specified in the **Object Name** argument must be open before this action is run.</span></span> <span data-ttu-id="8dbc1-139">В противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-139">Otherwise, an error occurs.</span></span>

- <span data-ttu-id="8dbc1-140">Если критерии в аргументе **Условие** не выполняются, ошибка не происходит, и фокус остается на текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="8dbc1-141">При поиске для записи предыдущему или следующему поиска не «переносится» при достижении конца данных.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-141">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data.</span></span> <span data-ttu-id="8dbc1-142">Если нет дополнительных записей, которые соответствуют условиям, ошибка не происходит, и фокус остается на текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-142">If there are no further records that match the criteria, no error occurs and the focus remains on the current record.</span></span> <span data-ttu-id="8dbc1-143">Чтобы убедиться в том, что было найдено, введите условие для следующего действия и сделать условие то же, что критерии в аргументе **Условие** .</span><span class="sxs-lookup"><span data-stu-id="8dbc1-143">To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="8dbc1-144">Чтобы выполнить действие **ПоискЗаписи** в модуле VBA, используйте метод **ПоискЗаписи** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="8dbc1-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="8dbc1-145">Действие **ПоискЗаписи** аналогична **[НайтиЗапись](findrecord-macro-action.md)** , но **ПоискЗаписи** имеет более мощные функциональные возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-145">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features.</span></span> <span data-ttu-id="8dbc1-146">**НайтиЗапись** в основном используется для поиска строк и дублирует функциональные возможности диалогового окна **Найти** .</span><span class="sxs-lookup"><span data-stu-id="8dbc1-146">The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box.</span></span> <span data-ttu-id="8dbc1-147">Действие **ПоискЗаписи** использует критерии, по которым наиболее точно параметрам фильтра или запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-147">The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query.</span></span> <span data-ttu-id="8dbc1-148">Перечисленные ниже показано несколько действий, которые можно делать с **ПоискЗаписи** действие:</span><span class="sxs-lookup"><span data-stu-id="8dbc1-148">The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="8dbc1-149">Можно использовать константы в аргументе **Условие** , такие как</span><span class="sxs-lookup"><span data-stu-id="8dbc1-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="8dbc1-150">Можно обратиться к полям, которые находятся в источника записей в форму или отчет, но не отображаются на форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-150">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report.</span></span> <span data-ttu-id="8dbc1-151">В предыдущем примере описание ни идентификатор категории должны отображаться на форму или отчет в качестве условия для работы.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-151">In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="8dbc1-152">Можно использовать логические операторы, такие как **\<**, **\>**, **и**, **или**и **BETWEEN**.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-152">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**.</span></span> <span data-ttu-id="8dbc1-153">**НайтиЗапись** соответствует только строк, равно, начать с или содержат строку, поиск.</span><span class="sxs-lookup"><span data-stu-id="8dbc1-153">The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="8dbc1-154">Пример</span><span class="sxs-lookup"><span data-stu-id="8dbc1-154">Example</span></span>

<span data-ttu-id="8dbc1-155">Следующий макрос сначала открывается в таблице категорий с помощью **ОткрытьТаблицу** .</span><span class="sxs-lookup"><span data-stu-id="8dbc1-155">The following macro first opens the Categories table by using the **OpenTable** action.</span></span> <span data-ttu-id="8dbc1-156">Макрос использует действие **ПоискЗаписи** для поиска первой записи в таблице где поле Описание = «Напитки».</span><span class="sxs-lookup"><span data-stu-id="8dbc1-156">The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8dbc1-157">Action</span><span class="sxs-lookup"><span data-stu-id="8dbc1-157">Action</span></span></p></th>
<th><p><span data-ttu-id="8dbc1-158">Arguments</span><span class="sxs-lookup"><span data-stu-id="8dbc1-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8dbc1-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-160"><strong>Имя таблицы</strong>: категории<strong>представление</strong>: <strong>Режим DatasheetData</strong>: <strong>Редактирование</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8dbc1-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="8dbc1-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="8dbc1-162"><strong>Тип объекта</strong>: <strong>Имя TableObject</strong>: категорий<strong>запись</strong>: <strong>Условие FirstWhere</strong>: описание = &quot;Напитки&quot;</span><span class="sxs-lookup"><span data-stu-id="8dbc1-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

