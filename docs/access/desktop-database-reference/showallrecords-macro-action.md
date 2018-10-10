---
title: ShowAllRecords Macro Action
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 40221ce69a03f619bd15a5a89af9018c66c52791
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482738"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="02455-102">ShowAllRecords Macro Action</span><span class="sxs-lookup"><span data-stu-id="02455-102">ShowAllRecords Macro Action</span></span>


<span data-ttu-id="02455-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="02455-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="02455-104">Можно использовать **ПоказатьВсеЗаписи** для удаления любого фильтра из активной таблицы, набор результатов запроса или формы и отображения всех записей в таблице или результирующего набора или всех записей в виде таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="02455-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="02455-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="02455-105">Setting</span></span>

<span data-ttu-id="02455-106">**ПоказатьВсеЗаписи** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="02455-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="02455-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="02455-107">Remarks</span></span>

<span data-ttu-id="02455-108">Чтобы убедиться, что все записи (включая все измененные или новые записи) отображаются для таблицы, набор результатов запроса или формы, можно использовать это действие.</span><span class="sxs-lookup"><span data-stu-id="02455-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="02455-109">Это действие позволяет обновление записей для формы или подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="02455-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="02455-110">Это действие также можно использовать для удаления, которая была применена с \*\*ПрименитьФильтр команду **Фильтр** на вкладке " **Главная** " **Имя фильтра** или аргумент **Условие** **этого** \*\* фильтра.</span><span class="sxs-lookup"><span data-stu-id="02455-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="02455-111">Это действие имеет тот же эффект, нажав кнопку **Переключить фильтр** на вкладке **Главная** или щелкнув правой кнопкой мыши поля и нажав кнопку **... Очистить фильтр из** представления формы, в режиме или режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="02455-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="02455-112">Чтобы запустить **ПоказатьВсеЗаписи** в Visual Basic для приложений (VBA) модуль, используйте метод **ПоказатьВсеЗаписи** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="02455-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="02455-113">Пример</span><span class="sxs-lookup"><span data-stu-id="02455-113">Example</span></span>

<span data-ttu-id="02455-114">**Применение фильтра с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="02455-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="02455-115">Следующий макрос содержит набор действий, каждая из которых для фильтрации записей формы Телефоны клиентов.</span><span class="sxs-lookup"><span data-stu-id="02455-115">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form.</span></span> <span data-ttu-id="02455-116">Демонстрируется использование **ApplyFilter**, **ПоказатьВсеЗаписи**и **КЭлементуУправления** действия.</span><span class="sxs-lookup"><span data-stu-id="02455-116">It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions.</span></span> <span data-ttu-id="02455-117">Также демонстрируется использование условий для определения выбора выключателя в группы переключателей на форме.</span><span class="sxs-lookup"><span data-stu-id="02455-117">It also shows the use of conditions to determine which toggle button in an option group has been selected on the form.</span></span> <span data-ttu-id="02455-118">Каждая строка связан с помощью переключателя (en), которая выбирает набора записей, начиная с A, B, C и т. д или для всех записей.</span><span class="sxs-lookup"><span data-stu-id="02455-118">Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records.</span></span> <span data-ttu-id="02455-119">Этот макрос должен быть связан события **AfterUpdate** CompanyNameFilter группы.</span><span class="sxs-lookup"><span data-stu-id="02455-119">This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02455-120">Condition</span><span class="sxs-lookup"><span data-stu-id="02455-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="02455-121">Действие</span><span class="sxs-lookup"><span data-stu-id="02455-121">Action</span></span></p></th>
<th><p><span data-ttu-id="02455-122">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="02455-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="02455-123">Comment</span><span class="sxs-lookup"><span data-stu-id="02455-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02455-124">[Фильтр по имени организации] = 1</span><span class="sxs-lookup"><span data-stu-id="02455-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="02455-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="02455-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="02455-126"><strong>Условие отбора</strong>: [название организации] как &quot;[AАБВГД] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="02455-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="02455-127">Фильтр по именам организаций, которые начинаются с отчетные, Б, В, Г или Ä.</span><span class="sxs-lookup"><span data-stu-id="02455-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02455-128">[Фильтр по имени организации] = 2</span><span class="sxs-lookup"><span data-stu-id="02455-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="02455-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="02455-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="02455-130"><strong>Условие отбора</strong>: [название организации] как &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="02455-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="02455-131">Фильтр по именам организаций, которые начинаются с б.</span><span class="sxs-lookup"><span data-stu-id="02455-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02455-132">[Фильтр по имени организации] = 3</span><span class="sxs-lookup"><span data-stu-id="02455-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="02455-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="02455-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="02455-134"><strong>Условие отбора</strong>: [название организации] как &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="02455-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="02455-135">Фильтр по именам организаций, которые начинаются с или З.</span><span class="sxs-lookup"><span data-stu-id="02455-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02455-136">... Строки действий для D по Y имеют тот же формат как буквы от A до C...</span><span class="sxs-lookup"><span data-stu-id="02455-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02455-137">[Фильтр по имени организации] = 26</span><span class="sxs-lookup"><span data-stu-id="02455-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="02455-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="02455-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="02455-139"><strong>Условие отбора</strong>: [название организации] как &quot;[ZЖШЕ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="02455-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="02455-140">Фильтр для названия компаний, начинающиеся со Z, Æ, Ш или Е.</span><span class="sxs-lookup"><span data-stu-id="02455-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02455-141">[Фильтр по имени организации] = 27</span><span class="sxs-lookup"><span data-stu-id="02455-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="02455-142"><strong>ПоказатьВсеЗаписи</strong></span><span class="sxs-lookup"><span data-stu-id="02455-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="02455-143">Отображение всех записей.</span><span class="sxs-lookup"><span data-stu-id="02455-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02455-144">[RecordsetClone]. [ЧислоЗаписей] &gt;0</span><span class="sxs-lookup"><span data-stu-id="02455-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="02455-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="02455-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="02455-146"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="02455-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="02455-147">Если возвращаются записи для выбранных букв, фокус перемещается к элементу управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="02455-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

