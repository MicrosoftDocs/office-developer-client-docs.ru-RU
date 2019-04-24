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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314646"
---
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="12d67-102">Макрокоманда SearchForRecord</span><span class="sxs-lookup"><span data-stu-id="12d67-102">SearchForRecord macro action</span></span>


<span data-ttu-id="12d67-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12d67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12d67-104">Вы можете использовать действие **сеарчфоррекорд** для поиска конкретной записи в таблице, запросе, форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="12d67-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="12d67-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="12d67-105">Setting</span></span>

<span data-ttu-id="12d67-106">Макрокоманда **сеарчфоррекорд** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="12d67-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12d67-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="12d67-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="12d67-108">Описание</span><span class="sxs-lookup"><span data-stu-id="12d67-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12d67-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-110">Введите или выберите тип объекта базы данных, в котором выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="12d67-110">Enter or select the type of database object that you are searching in.</span></span> <span data-ttu-id="12d67-111">Можно выбрать <strong>таблицу</strong>, <strong>запрос</strong>, <strong>форму</strong>или <strong>отчет</strong>.</span><span class="sxs-lookup"><span data-stu-id="12d67-111">You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12d67-112"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-113">Введите или выберите определенный объект, содержащий запись для поиска.</span><span class="sxs-lookup"><span data-stu-id="12d67-113">Enter or select the specific object that contains the record to search for.</span></span> <span data-ttu-id="12d67-114">В раскрывающемся списке отображаются все объекты базы данных выбранного типа для аргумента " <strong>тип объекта</strong> ".</span><span class="sxs-lookup"><span data-stu-id="12d67-114">The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12d67-115"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-116">Указание начальной точки и направления поиска.</span><span class="sxs-lookup"><span data-stu-id="12d67-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12d67-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="12d67-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="12d67-118">Описание</span><span class="sxs-lookup"><span data-stu-id="12d67-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12d67-119"><strong>Previous</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-120">Поиск в обратном направлении от текущей записи.</span><span class="sxs-lookup"><span data-stu-id="12d67-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12d67-121"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-122">Поиск вперед от текущей записи.</span><span class="sxs-lookup"><span data-stu-id="12d67-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12d67-123"><strong>First</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-124">Поиск вперед от первой записи.</span><span class="sxs-lookup"><span data-stu-id="12d67-124">Search forward from the first record.</span></span> <span data-ttu-id="12d67-125">Это значение используется по умолчанию для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="12d67-125">This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12d67-126"><strong>Last</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-127">Поиск назад от последней записи.</span><span class="sxs-lookup"><span data-stu-id="12d67-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12d67-128"><strong>Условие отбора</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-129">Введите критерии поиска, используя тот же синтаксис, что и в предложении WHERE языка SQL, без слова &quot;Where&quot;.</span><span class="sxs-lookup"><span data-stu-id="12d67-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="12d67-130">For example,</span><span class="sxs-lookup"><span data-stu-id="12d67-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="12d67-131">Чтобы создать условие, включающее значение из текстового поля формы, необходимо создать выражение, которое сцепляет первую часть критерия с именем текстового поля, содержащего значение для поиска.</span><span class="sxs-lookup"><span data-stu-id="12d67-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="12d67-132">Например, следующий критерий будет искать значение в поле Description (описание) в текстовом поле с именем Ткстдескриптион в форме Фрмкатегориес.</span><span class="sxs-lookup"><span data-stu-id="12d67-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="12d67-133">Обратите внимание на знак<strong>=</strong>равенства () в начале выражения и использование одинарных кавычек (<strong>'</strong>) с любой стороны ссылки на текстовое поле:</span><span class="sxs-lookup"><span data-stu-id="12d67-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="12d67-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="12d67-134">Remarks</span></span>

- <span data-ttu-id="12d67-135">В случаях, когда несколько записей соответствуют условиям в аргументе **условия WHERE** , следующие факторы определяют, какая запись найдена:</span><span class="sxs-lookup"><span data-stu-id="12d67-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="12d67-136">**Параметр записи аргумента** Дополнительные сведения об аргументе **Record** содержатся в таблице в разделе Параметры.</span><span class="sxs-lookup"><span data-stu-id="12d67-136">**The Record argument setting**See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="12d67-137">**Порядок сортировки записей** Например, если для аргумента **Record** задано значение **First**, изменение порядка сортировки записей может привести к изменению записи, которая будет найдена.</span><span class="sxs-lookup"><span data-stu-id="12d67-137">**The sort order of the records**For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="12d67-138">Перед выполнением этого действия должен быть открыт объект, указанный в аргументе **имя объекта** .</span><span class="sxs-lookup"><span data-stu-id="12d67-138">The object specified in the **Object Name** argument must be open before this action is run.</span></span> <span data-ttu-id="12d67-139">В противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="12d67-139">Otherwise, an error occurs.</span></span>

- <span data-ttu-id="12d67-140">Если условия в аргументе **условия WHERE** не выполнены, ошибка не возникнет и фокус остается на текущей записи.</span><span class="sxs-lookup"><span data-stu-id="12d67-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="12d67-141">При поиске предыдущей или следующей записи при достижении конца данных поиск не переносится.</span><span class="sxs-lookup"><span data-stu-id="12d67-141">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data.</span></span> <span data-ttu-id="12d67-142">Если другие записи, удовлетворяющие критериям, отсутствуют, то ошибка не возникнет и фокус остается на текущей записи.</span><span class="sxs-lookup"><span data-stu-id="12d67-142">If there are no further records that match the criteria, no error occurs and the focus remains on the current record.</span></span> <span data-ttu-id="12d67-143">Чтобы убедиться в том, что найдено совпадение, можно ввести условие для следующего действия и сделать условие таким же, как в аргументе **условие** отбора.</span><span class="sxs-lookup"><span data-stu-id="12d67-143">To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="12d67-144">Чтобы выполнить действие **сеарчфоррекорд** в модуле VBA, используйте метод **сеарчфоррекорд** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="12d67-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="12d67-145">Действие **сеарчфоррекорд** аналогично действию **[НайтиЗапись](findrecord-macro-action.md)** , но **сеарчфоррекорд** имеет более широкие возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="12d67-145">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features.</span></span> <span data-ttu-id="12d67-146">Макрокоманда " **НайтиЗапись** " используется в основном для поиска строк и дублирует функциональные возможности диалогового окна " **найти** ".</span><span class="sxs-lookup"><span data-stu-id="12d67-146">The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box.</span></span> <span data-ttu-id="12d67-147">Действие **сеарчфоррекорд** использует условия, которые являются более похожими на фильтры или запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="12d67-147">The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query.</span></span> <span data-ttu-id="12d67-148">В следующем списке показаны некоторые действия, которые можно выполнить с действием **сеарчфоррекорд** :</span><span class="sxs-lookup"><span data-stu-id="12d67-148">The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="12d67-149">В аргументе **условие WHERE** можно использовать сложные условия, такие как</span><span class="sxs-lookup"><span data-stu-id="12d67-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="12d67-150">Вы можете ссылаться на поля, которые находятся в источнике записей формы или отчета, но не отображаются в форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="12d67-150">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report.</span></span> <span data-ttu-id="12d67-151">В предыдущем примере ни описание, ни CategoryID не должны отображаться в форме или отчете, чтобы критерии работало.</span><span class="sxs-lookup"><span data-stu-id="12d67-151">In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="12d67-152">Можно использовать логические операторы, **\<** такие как, **\>**, **и**, **или**и **между**.</span><span class="sxs-lookup"><span data-stu-id="12d67-152">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**.</span></span> <span data-ttu-id="12d67-153">Макрокоманда **НайтиЗапись** соответствует только строкам, которые равны, начинаются с или содержат строку, в которой выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="12d67-153">The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="12d67-154">Пример</span><span class="sxs-lookup"><span data-stu-id="12d67-154">Example</span></span>

<span data-ttu-id="12d67-155">Следующий макрос сначала открывает таблицу Categories с помощью действия **опентабле** .</span><span class="sxs-lookup"><span data-stu-id="12d67-155">The following macro first opens the Categories table by using the **OpenTable** action.</span></span> <span data-ttu-id="12d67-156">Затем макрос использует действие **сеарчфоррекорд** для поиска первой записи в таблице, в которой поле Description имеет значение "напитки".</span><span class="sxs-lookup"><span data-stu-id="12d67-156">The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12d67-157">Действие</span><span class="sxs-lookup"><span data-stu-id="12d67-157">Action</span></span></p></th>
<th><p><span data-ttu-id="12d67-158">Аргументы</span><span class="sxs-lookup"><span data-stu-id="12d67-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12d67-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-160"><strong>Имя таблицы</strong>:<strong>представление</strong>Categories: <strong>режим даташитдата</strong>: <strong>Редактирование</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12d67-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="12d67-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="12d67-162"><strong>Тип объекта</strong>: <strong>TableObject имя</strong>:<strong>запись</strong>категорий: <strong>фирствхере условие</strong>: Описание = &quot;напитки&quot;</span><span class="sxs-lookup"><span data-stu-id="12d67-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

