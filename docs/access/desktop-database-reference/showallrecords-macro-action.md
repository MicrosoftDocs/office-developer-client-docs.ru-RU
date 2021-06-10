---
title: Макрокоманда ShowAllRecords
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308647"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="613f4-102">Макрокоманда ShowAllRecords</span><span class="sxs-lookup"><span data-stu-id="613f4-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="613f4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="613f4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="613f4-104">Вы можете использовать действие **ShowAllRecords** для удаления любого примененного фильтра из активной таблицы, набора результатов запроса или формы и отображения всех записей в таблице или наборе результатов или всех записей в таблице или запросе формы.</span><span class="sxs-lookup"><span data-stu-id="613f4-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="613f4-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="613f4-105">Setting</span></span>

<span data-ttu-id="613f4-106">Действие **ShowAllRecords** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="613f4-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="613f4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="613f4-107">Remarks</span></span>

<span data-ttu-id="613f4-108">Это действие можно использовать для отображения всех записей (включая измененные или новые) для таблицы, набора результатов запроса или формы.</span><span class="sxs-lookup"><span data-stu-id="613f4-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="613f4-109">Это действие вызывает requery записей для формы или подформы.</span><span class="sxs-lookup"><span data-stu-id="613f4-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="613f4-110">Это действие также можно использовать для удаления любого фильтра, применяемого  с помощью действия **ApplyFilter,** команды Filter на вкладке **Home** или аргумента **Filter Name** or **Where Condition** действия **OpenForm.**</span><span class="sxs-lookup"><span data-stu-id="613f4-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="613f4-111">Это действие имеет тот же эффект, что  щелкнуть фильтр **Toggle** на вкладке Home или щелкнуть правой кнопкой мыши фильтрованное поле и щелкнуть фильтр **Clear из...** в представлении формы, представлении макета или представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="613f4-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="613f4-112">Чтобы выполнить действие **ShowAllRecords** в модуле Visual Basic для приложений (VBA), используйте метод **ShowAllRecords** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="613f4-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="613f4-113">Пример</span><span class="sxs-lookup"><span data-stu-id="613f4-113">Example</span></span>

<span data-ttu-id="613f4-114">**Применение фильтра с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="613f4-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="613f4-115">Следующий макрос содержит набор действий, каждый из которых фильтрует записи для формы списка Телефон клиента.</span><span class="sxs-lookup"><span data-stu-id="613f4-115">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form.</span></span> <span data-ttu-id="613f4-116">В нем показано использование действий **ApplyFilter,** **ShowAllRecords** и **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="613f4-116">It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions.</span></span> <span data-ttu-id="613f4-117">В нем также показано использование условий для определения того, какая кнопка для включения в группу опций была выбрана в форме.</span><span class="sxs-lookup"><span data-stu-id="613f4-117">It also shows the use of conditions to determine which toggle button in an option group has been selected on the form.</span></span> <span data-ttu-id="613f4-118">Каждая строка действий связана с кнопкой toggle, которая выбирает набор записей, начиная с A, B, C и так далее или всех записей.</span><span class="sxs-lookup"><span data-stu-id="613f4-118">Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records.</span></span> <span data-ttu-id="613f4-119">Этот макрос должен быть присоединен к событию **AfterUpdate** группы параметра CompanyNameFilter.</span><span class="sxs-lookup"><span data-stu-id="613f4-119">This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="613f4-120">Условие</span><span class="sxs-lookup"><span data-stu-id="613f4-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="613f4-121">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="613f4-121">Action</span></span></p></th>
<th><p><span data-ttu-id="613f4-122">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="613f4-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="613f4-123">Примечание</span><span class="sxs-lookup"><span data-stu-id="613f4-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="613f4-124">[Фильтры имени компании] =1</span><span class="sxs-lookup"><span data-stu-id="613f4-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="613f4-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="613f4-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="613f4-126"><strong>Где условие:</strong>[имя компании] Как &quot; [AÀÁÂÃÄ]\*&quot;</span><span class="sxs-lookup"><span data-stu-id="613f4-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="613f4-127">Фильтр для имен компаний, которые начинаются с A, À, Á, Â, Ã или Ä.</span><span class="sxs-lookup"><span data-stu-id="613f4-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613f4-128">[Фильтры имени компании] =2</span><span class="sxs-lookup"><span data-stu-id="613f4-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="613f4-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="613f4-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="613f4-130"><strong>Где условие</strong>: [Имя компании] Как &quot; B\*&quot;</span><span class="sxs-lookup"><span data-stu-id="613f4-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="613f4-131">Фильтр для имен компаний, которые начинаются с B.</span><span class="sxs-lookup"><span data-stu-id="613f4-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613f4-132">[Фильтры имени компании] =3</span><span class="sxs-lookup"><span data-stu-id="613f4-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="613f4-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="613f4-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="613f4-134"><strong>Где условие:</strong>[Имя компании] Как &quot; [CÇ]\*&quot;</span><span class="sxs-lookup"><span data-stu-id="613f4-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="613f4-135">Фильтр для имен компаний, которые начинаются с C или Ç.</span><span class="sxs-lookup"><span data-stu-id="613f4-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613f4-136">... Строки действия для D до Y имеют тот же формат, что и A through C ...</span><span class="sxs-lookup"><span data-stu-id="613f4-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613f4-137">[Фильтры имени компании] =26</span><span class="sxs-lookup"><span data-stu-id="613f4-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="613f4-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="613f4-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="613f4-139"><strong>Где условие:</strong>[имя компании] Как &quot; [ZÆØÅ]\*&quot;</span><span class="sxs-lookup"><span data-stu-id="613f4-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="613f4-140">Фильтр для имен компаний, которые начинаются с Z, Æ, Ø или Å.</span><span class="sxs-lookup"><span data-stu-id="613f4-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="613f4-141">[Фильтры имени компании] =27</span><span class="sxs-lookup"><span data-stu-id="613f4-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="613f4-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="613f4-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="613f4-143">Показать все записи.</span><span class="sxs-lookup"><span data-stu-id="613f4-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="613f4-144">[RecordsetClone]. [RecordCount] &gt; 0</span><span class="sxs-lookup"><span data-stu-id="613f4-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="613f4-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="613f4-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="613f4-146"><strong>Имя управления:</strong>CompanyName</span><span class="sxs-lookup"><span data-stu-id="613f4-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="613f4-147">Если записи возвращаются для выбранного письма, переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="613f4-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

