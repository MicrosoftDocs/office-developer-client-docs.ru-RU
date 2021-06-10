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
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="56afc-102">Макрокоманда SearchForRecord</span><span class="sxs-lookup"><span data-stu-id="56afc-102">SearchForRecord macro action</span></span>


<span data-ttu-id="56afc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56afc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56afc-104">Вы можете использовать **действие SearchForRecord** для поиска определенной записи в таблице, запросе, форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="56afc-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="56afc-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="56afc-105">Setting</span></span>

<span data-ttu-id="56afc-106">Действие **SearchForRecord имеет** следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="56afc-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56afc-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="56afc-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="56afc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="56afc-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56afc-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-110">Введите или выберите тип объекта базы данных, в который вы ищете.</span><span class="sxs-lookup"><span data-stu-id="56afc-110">Enter or select the type of database object that you are searching in.</span></span> <span data-ttu-id="56afc-111">Вы можете выбрать <strong>таблицу,</strong> <strong>запрос,</strong> <strong>форму</strong>или <strong>отчет.</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-111">You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56afc-112"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-113">Введите или выберите определенный объект, содержащий запись для поиска.</span><span class="sxs-lookup"><span data-stu-id="56afc-113">Enter or select the specific object that contains the record to search for.</span></span> <span data-ttu-id="56afc-114">В выпадаемом списке показаны все объекты базы данных типа, выбранного для <strong>аргумента Object Type.</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-114">The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56afc-115"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-116">Укажите отправную точку и направление поиска.</span><span class="sxs-lookup"><span data-stu-id="56afc-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56afc-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="56afc-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="56afc-118">Описание</span><span class="sxs-lookup"><span data-stu-id="56afc-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56afc-119"><strong>Previous</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-120">Поиск в обратном направлении от текущей записи.</span><span class="sxs-lookup"><span data-stu-id="56afc-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56afc-121"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-122">Поиск вперед из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="56afc-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56afc-123"><strong>First</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-124">Поиск вперед из первой записи.</span><span class="sxs-lookup"><span data-stu-id="56afc-124">Search forward from the first record.</span></span> <span data-ttu-id="56afc-125">Это значение по умолчанию для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="56afc-125">This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56afc-126"><strong>Last</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-127">Поиск назад из последней записи.</span><span class="sxs-lookup"><span data-stu-id="56afc-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56afc-128"><strong>Где состояние</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-129">Введите критерии поиска, используя тот же синтаксис, что и SQL where, только без &quot; слова WHERE &quot; .</span><span class="sxs-lookup"><span data-stu-id="56afc-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="56afc-130">Пример.</span><span class="sxs-lookup"><span data-stu-id="56afc-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="56afc-131">Чтобы создать критерий, содержащий значение из текстового окна в форме, необходимо создать выражение, которое соединять первую часть критерия с именем текстового окна, содержащего значение, для которого необходимо искать.</span><span class="sxs-lookup"><span data-stu-id="56afc-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="56afc-132">Например, следующий критерий будет искать в поле Описание значение в текстовом поле с именем txtDescription в форме с именем frmCategories.</span><span class="sxs-lookup"><span data-stu-id="56afc-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="56afc-133">Обратите внимание на равный знак () в начале выражения и использование одиночных кавычках ( ' ) по обе стороны ссылки <strong>=</strong> на текстовое<strong></strong>поле:</span><span class="sxs-lookup"><span data-stu-id="56afc-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="56afc-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="56afc-134">Remarks</span></span>

- <span data-ttu-id="56afc-135">В тех случаях, когда несколько записей соответствуют критериям аргумента **Where Condition,** следующие факторы определяют, какая запись найдена:</span><span class="sxs-lookup"><span data-stu-id="56afc-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="56afc-136">**Параметр Аргумент Записи** Дополнительные сведения о аргументе Запись см. в Параметры в разделе **"Запись".**</span><span class="sxs-lookup"><span data-stu-id="56afc-136">**The Record argument setting** See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="56afc-137">**Порядок сортировки записей** Например, если аргумент **Записи** настроен на **First,** изменение порядка сортировки записей может изменить найденную запись.</span><span class="sxs-lookup"><span data-stu-id="56afc-137">**The sort order of the records** For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="56afc-138">Объект, указанный в **аргументе "Имя объекта",** должен быть открыт перед запуском этого действия.</span><span class="sxs-lookup"><span data-stu-id="56afc-138">The object specified in the **Object Name** argument must be open before this action is run.</span></span> <span data-ttu-id="56afc-139">В противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="56afc-139">Otherwise, an error occurs.</span></span>

- <span data-ttu-id="56afc-140">Если критерии в аргументе **Where Condition** не выполнены, ошибка не возникает, и основное внимание остается на текущей записи.</span><span class="sxs-lookup"><span data-stu-id="56afc-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="56afc-141">При поиске предыдущей или следующей записи поиск не "оборачивается", когда достигает конца данных.</span><span class="sxs-lookup"><span data-stu-id="56afc-141">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data.</span></span> <span data-ttu-id="56afc-142">Если нет дополнительных записей, которые соответствуют критериям, ошибки не происходит, и основное внимание остается на текущей записи.</span><span class="sxs-lookup"><span data-stu-id="56afc-142">If there are no further records that match the criteria, no error occurs and the focus remains on the current record.</span></span> <span data-ttu-id="56afc-143">Чтобы убедиться в обнаружении совпадения, можно ввести условие для следующего действия и сделать условие таким же, как и критерии в аргументе **Where Condition.**</span><span class="sxs-lookup"><span data-stu-id="56afc-143">To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="56afc-144">Чтобы выполнить **действие SearchForRecord** в модуле VBA, используйте метод **SearchForRecord** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="56afc-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="56afc-145">Действие **SearchForRecord** аналогично действию **[FindRecord,](findrecord-macro-action.md)** но **SearchForRecord имеет** более мощные функции поиска.</span><span class="sxs-lookup"><span data-stu-id="56afc-145">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features.</span></span> <span data-ttu-id="56afc-146">Действие **FindRecord** используется в основном для поиска строк и дублирует функции диалогового окна **Find.**</span><span class="sxs-lookup"><span data-stu-id="56afc-146">The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box.</span></span> <span data-ttu-id="56afc-147">Действие **SearchForRecord использует** критерии, которые больше похожи на критерии фильтра или SQL запроса.</span><span class="sxs-lookup"><span data-stu-id="56afc-147">The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query.</span></span> <span data-ttu-id="56afc-148">В следующем списке показано, что можно сделать с действием **SearchForRecord:**</span><span class="sxs-lookup"><span data-stu-id="56afc-148">The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="56afc-149">В аргументе Where **Condition** можно использовать сложные критерии, такие как</span><span class="sxs-lookup"><span data-stu-id="56afc-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="56afc-150">Вы можете ссылаться на поля, которые находятся в источнике записи формы или отчета, но не отображаются в форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="56afc-150">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report.</span></span> <span data-ttu-id="56afc-151">В предыдущем примере ни Описание, ни CategoryID не должны отображаться в форме или отчете для работы критериев.</span><span class="sxs-lookup"><span data-stu-id="56afc-151">In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="56afc-152">Вы можете использовать логических операторов, таких как **\<** , И , ИЛИ , **\>** **и** **МЕЖДУ**. </span><span class="sxs-lookup"><span data-stu-id="56afc-152">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**.</span></span> <span data-ttu-id="56afc-153">Действие **FindRecord** совпадает только со строками, которые равны, начинаются с строки, для которых ведется поиск, или содержат ее.</span><span class="sxs-lookup"><span data-stu-id="56afc-153">The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="56afc-154">Пример</span><span class="sxs-lookup"><span data-stu-id="56afc-154">Example</span></span>

<span data-ttu-id="56afc-155">Следующий макрос открывает таблицу Категорий с помощью **действия OpenTable.**</span><span class="sxs-lookup"><span data-stu-id="56afc-155">The following macro first opens the Categories table by using the **OpenTable** action.</span></span> <span data-ttu-id="56afc-156">Затем макрос использует **действие SearchForRecord** для поиска первой записи в таблице, где поле Description равно "Напитки".</span><span class="sxs-lookup"><span data-stu-id="56afc-156">The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56afc-157">Action</span><span class="sxs-lookup"><span data-stu-id="56afc-157">Action</span></span></p></th>
<th><p><span data-ttu-id="56afc-158">Аргументы</span><span class="sxs-lookup"><span data-stu-id="56afc-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56afc-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-160"><strong>Имя</strong>таблицы:<strong></strong>Просмотр категорий: <strong>Режим DatasheetData</strong>: <strong>Изменение</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56afc-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="56afc-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="56afc-162"><strong>Тип объекта:</strong> <strong>Имя TableObject</strong>: Запись категорий<strong>:</strong>Состояние <strong>FirstWhere</strong>: Описание = &quot; Напитки&quot;</span><span class="sxs-lookup"><span data-stu-id="56afc-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

