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
# <a name="showallrecords-macro-action"></a><span data-ttu-id="3bbf3-102">Макрокоманда ShowAllRecords</span><span class="sxs-lookup"><span data-stu-id="3bbf3-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="3bbf3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bbf3-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3bbf3-104">Вы можете использовать действие **шоваллрекордс** для удаления фильтра из активной таблицы, набора результатов запроса или формы и отображения всех записей в таблице или наборе результатов или во всех записях в базовой таблице или запросе формы.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="3bbf3-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="3bbf3-105">Setting</span></span>

<span data-ttu-id="3bbf3-106">Макрокоманда **шоваллрекордс** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbf3-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="3bbf3-107">Remarks</span></span>

<span data-ttu-id="3bbf3-108">Вы можете использовать это действие, чтобы убедиться, что все записи (включая измененные и новые записи) отображаются для таблицы, набора результатов запроса или формы.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="3bbf3-109">Это действие вызывает обновление записей для формы или подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="3bbf3-110">Кроме того, с помощью этого действия можно удалить любой фильтр, примененный к действию **ПрименитьФильтр** , команду **фильтра** на вкладке " **Главная** " или "условие **отбора** " или " **условие** отбора" Макрокоманды "ОткрытьФорму" ( **OpenForm** ).</span><span class="sxs-lookup"><span data-stu-id="3bbf3-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="3bbf3-111">Это действие имеет тот же результат, что и кнопка **переключения фильтра** на вкладке **Главная** , или щелкните правой кнопкой мыши Отфильтрованное поле и выберите команду **Очистить фильтр от...** в представлении формы, макет или режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="3bbf3-112">Чтобы запустить действие **шоваллрекордс** в модуле Visual Basic для приложений (VBA), используйте метод **шоваллрекордс** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="3bbf3-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="3bbf3-113">Пример</span><span class="sxs-lookup"><span data-stu-id="3bbf3-113">Example</span></span>

<span data-ttu-id="3bbf3-114">**Применение фильтра с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="3bbf3-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="3bbf3-115">Следующий макрос содержит набор действий, каждый из которых фильтрует форму списка телефоны клиентов.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-115">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form.</span></span> <span data-ttu-id="3bbf3-116">В нем показано использование действий **ПрименитьФильтр**, **шоваллрекордс**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="3bbf3-116">It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions.</span></span> <span data-ttu-id="3bbf3-117">В нем также показано использование условий, чтобы определить, какой выключатель выбран в группе параметров в форме.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-117">It also shows the use of conditions to determine which toggle button in an option group has been selected on the form.</span></span> <span data-ttu-id="3bbf3-118">Каждая строка действий связана с выключателем, который выбирает набор записей, начинающихся с A, B, C и т. д., или всех записей.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-118">Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records.</span></span> <span data-ttu-id="3bbf3-119">Этот макрос необходимо вложить в событие **AfterUpdate** группы параметров компанинамефилтер.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-119">This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3bbf3-120">Условие</span><span class="sxs-lookup"><span data-stu-id="3bbf3-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="3bbf3-121">Действие</span><span class="sxs-lookup"><span data-stu-id="3bbf3-121">Action</span></span></p></th>
<th><p><span data-ttu-id="3bbf3-122">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="3bbf3-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="3bbf3-123">Комментарий</span><span class="sxs-lookup"><span data-stu-id="3bbf3-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3bbf3-124">[Фильтры имен компаний] = 1</span><span class="sxs-lookup"><span data-stu-id="3bbf3-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3bbf3-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbf3-126"><strong>Условие отбора</strong>: [название компании] &quot;Like [аàáâãä] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3bbf3-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-127">Фильтр для названий компаний, которые начинаются с A, À, Á, В, Ã или Ä.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbf3-128">[Фильтры имен компаний] = 2</span><span class="sxs-lookup"><span data-stu-id="3bbf3-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3bbf3-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbf3-130"><strong>Условие отбора</strong>: [название компании] &quot;Like B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3bbf3-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-131">Фильтр для названий компаний, которые начинаются с B.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbf3-132">[Фильтры имен компаний] = 3</span><span class="sxs-lookup"><span data-stu-id="3bbf3-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3bbf3-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbf3-134"><strong>Условие отбора</strong>: [название компании] &quot;Like [кç] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3bbf3-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-135">Фильтр для названий компаний, которые начинаются с C или Ç.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbf3-136">... Строки действий для D – Y имеют тот же формат, что и В C...</span><span class="sxs-lookup"><span data-stu-id="3bbf3-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbf3-137">[Фильтры имен компаний] = 26</span><span class="sxs-lookup"><span data-stu-id="3bbf3-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3bbf3-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbf3-139"><strong>Условие отбора</strong>: [название компании] &quot;Like [зæøå] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3bbf3-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-140">Фильтр для названий компаний, которые начинаются с Z, Æ, Ø или Å.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3bbf3-141">[Фильтры имен компаний] = 27</span><span class="sxs-lookup"><span data-stu-id="3bbf3-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="3bbf3-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3bbf3-143">Показать все записи.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3bbf3-144">[Рекордсетклоне]. RecordCount &gt;0</span><span class="sxs-lookup"><span data-stu-id="3bbf3-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="3bbf3-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="3bbf3-146"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="3bbf3-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="3bbf3-147">Если для выбранной буквы возвращаются записи, переместите фокус на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="3bbf3-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

