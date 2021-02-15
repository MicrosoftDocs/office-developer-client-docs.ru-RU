---
title: Макрокоманда OpenReport
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288352"
---
# <a name="openreport-macro-action"></a><span data-ttu-id="566f0-102">Макрокоманда OpenReport</span><span class="sxs-lookup"><span data-stu-id="566f0-102">OpenReport macro action</span></span>

<span data-ttu-id="566f0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="566f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="566f0-104">С помощью действия **OpenReport** можно открыть отчет в режиме конструктора или предварительного просмотра или отправить отчет непосредственно на принтер.</span><span class="sxs-lookup"><span data-stu-id="566f0-104">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer.</span></span> <span data-ttu-id="566f0-105">Кроме того, вы можете ограничить записи, которые будут печататься в отчете.</span><span class="sxs-lookup"><span data-stu-id="566f0-105">You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="566f0-106">Setting</span><span class="sxs-lookup"><span data-stu-id="566f0-106">Setting</span></span>

<span data-ttu-id="566f0-107">Действие **OpenReport** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="566f0-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="566f0-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="566f0-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="566f0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="566f0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="566f0-110">Имя отчета</span><span class="sxs-lookup"><span data-stu-id="566f0-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="566f0-111">Имя отчета, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="566f0-111">The name of the report to open.</span></span> <span data-ttu-id="566f0-112">В <strong>поле "Имя отчета"</strong> в <strong></strong> разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все отчеты в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="566f0-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="566f0-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="566f0-113">This is a required argument.</span></span> <span data-ttu-id="566f0-114">При запуске макроса, содержащего действие OpenReport в базе данных библиотеки, Microsoft Access сначала ищет отчет с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="566f0-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="566f0-115">Просмотр</span><span class="sxs-lookup"><span data-stu-id="566f0-115">View</span></span></p></td>
<td><p><span data-ttu-id="566f0-116">Представление, в котором будет открыт отчет.</span><span class="sxs-lookup"><span data-stu-id="566f0-116">The view in which the report will open.</span></span> <span data-ttu-id="566f0-117">Нажмите <strong>кнопку "Печать"</strong> (немедленно распечатайте отчет), <strong>"Разработка"</strong>или "Предварительный <strong>просмотр"</strong> в <strong>поле "Вид".</strong></span><span class="sxs-lookup"><span data-stu-id="566f0-117">Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="566f0-118">Значение по умолчанию <strong>— Print</strong>.</span><span class="sxs-lookup"><span data-stu-id="566f0-118">The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="566f0-119">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="566f0-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="566f0-120">Фильтр, ограничивающий записи отчета.</span><span class="sxs-lookup"><span data-stu-id="566f0-120">A filter that restricts the report's records.</span></span> <span data-ttu-id="566f0-121">Можно ввести имя существующего запроса или фильтра, сохраненного в качестве запроса.</span><span class="sxs-lookup"><span data-stu-id="566f0-121">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="566f0-122">Однако запрос должен включать все поля в открываемом отчете или иметь свойство <strong>OutputAllFields</strong> со свойством <strong>Yes.</strong></span><span class="sxs-lookup"><span data-stu-id="566f0-122">However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="566f0-123">Where Condition</span><span class="sxs-lookup"><span data-stu-id="566f0-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="566f0-124">Допустимый SQL WHERE (без слова WHERE) или выражение, которое Access использует для выбора записей из таблицы или запроса отчета.</span><span class="sxs-lookup"><span data-stu-id="566f0-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="566f0-125">Если выбрать фильтр с аргументом "Имя фильтра", Access применяет это предложение WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="566f0-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="566f0-126">Чтобы открыть отчет и ограничить его записи теми, которые указаны значением для управления в форме, используйте следующее выражение:</span><span class="sxs-lookup"><span data-stu-id="566f0-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="566f0-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong><em>formname</em><strong>]! [</strong><em>controlname on form</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="566f0-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="566f0-128">Замените <em>имя поля</em> именем поля в таблице или запросе отчета, который нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="566f0-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="566f0-129">Замените <em>имя формы</em> и имя <em>controlname</em> в форме и на имя формы и на то, что в форме содержится значение, которое должны соответствовать записям в отчете.</span><span class="sxs-lookup"><span data-stu-id="566f0-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="566f0-130"><b>ПРИМЕЧАНИЕ.</b>Максимальная длина аргумента Where Condition составляет 255 символов.</span><span class="sxs-lookup"><span data-stu-id="566f0-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="566f0-131">Если требуется ввести более сложную SQL WHERE, используйте метод <b>OpenReport</b> объекта <b>DoCmd</b> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="566f0-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="566f0-132">В VBA SQL ввести заявления о предложении WHERE до 32 768 символов.</span><span class="sxs-lookup"><span data-stu-id="566f0-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="566f0-133">Режим окна</span><span class="sxs-lookup"><span data-stu-id="566f0-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="566f0-134">Режим открытия отчета.</span><span class="sxs-lookup"><span data-stu-id="566f0-134">The mode in which the report will open.</span></span> <span data-ttu-id="566f0-135">Щелкните <strong>"Обычный",</strong> <strong>"Скрытый",</strong>"Значок" <strong>или "Диалоговое</strong> окно" в <strong>окне "Режим</strong> окна". <strong></strong></span><span class="sxs-lookup"><span data-stu-id="566f0-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="566f0-136">Значение по умолчанию — <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="566f0-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="566f0-137"><b>ПРИМЕЧАНИЕ.</b>Некоторые параметры аргументов в режиме окна не применяются при использовании документов с вкладками.</span><span class="sxs-lookup"><span data-stu-id="566f0-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="566f0-138">Чтобы переключиться на перекрывающиеся окна:</span><span class="sxs-lookup"><span data-stu-id="566f0-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="566f0-139">Нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="566f0-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="566f0-140">В <strong>диалоговом окне "Параметры</strong> Access" щелкните <strong>"Текущая база данных".</strong></span><span class="sxs-lookup"><span data-stu-id="566f0-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="566f0-141">В разделе <strong>"Параметры приложения"</strong> в разделе <strong>"Параметры окна документа"</strong>щелкните <strong>"Перекрывающиеся окна Windows".</strong></span><span class="sxs-lookup"><span data-stu-id="566f0-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="566f0-142">Нажмите <strong>кнопку "ОК",</strong>а затем закроем и снова откроете базу данных.</span><span class="sxs-lookup"><span data-stu-id="566f0-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="566f0-143">Заметки</span><span class="sxs-lookup"><span data-stu-id="566f0-143">Remarks</span></span>

<span data-ttu-id="566f0-144">Параметр **"Печать"** для аргумента **View** немедленно печатает отчет с использованием  текущих параметров принтера, не выведя диалоговое окно "Печать".</span><span class="sxs-lookup"><span data-stu-id="566f0-144">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box.</span></span> <span data-ttu-id="566f0-145">Вы также можете использовать действие **OpenReport,** чтобы открыть и настроить отчет, а затем с помощью действия PrintOut распечатать его.</span><span class="sxs-lookup"><span data-stu-id="566f0-145">You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it.</span></span> <span data-ttu-id="566f0-146">Например, может потребоваться изменить отчет или использовать действие **PrintOut** для изменения параметров принтера перед печатью.</span><span class="sxs-lookup"><span data-stu-id="566f0-146">For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="566f0-147">Применяемое условие фильтра и where становится параметром свойства **Filter отчета.**</span><span class="sxs-lookup"><span data-stu-id="566f0-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="566f0-148">Действие **OpenReport** аналогично двойному щелчку отчета в области навигации или щелчку правой кнопкой мыши в области навигации и выбору представления или команды **"Печать".**</span><span class="sxs-lookup"><span data-stu-id="566f0-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="566f0-149">Чтобы распечатать похожие отчеты для различных наборов данных, используйте фильтр или предложение WHERE, чтобы ограничить записи, печатаные в отчете.</span><span class="sxs-lookup"><span data-stu-id="566f0-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="566f0-150">Затем измените макрос, чтобы применить другой фильтр, или измените аргумент Условия where.</span><span class="sxs-lookup"><span data-stu-id="566f0-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="566f0-151">Вы можете перетащить отчет из области навигации в строку макроса.</span><span class="sxs-lookup"><span data-stu-id="566f0-151">You can drag a report from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="566f0-152">При этом автоматически создается действие **OpenReport,** которое открывает отчет в представлении "Отчет".</span><span class="sxs-lookup"><span data-stu-id="566f0-152">This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="566f0-153">Пример</span><span class="sxs-lookup"><span data-stu-id="566f0-153">Example</span></span>

<span data-ttu-id="566f0-154">В следующем примере показано, как использовать действие OpenReport для передачи параметра, который фильтрует отчет по мере его открытия.</span><span class="sxs-lookup"><span data-stu-id="566f0-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="566f0-155">Отчет **rptChapters** отображает записи для указанного автора, передавая элемент, выбранный в поле со списоком **cboAuthors,** в параметр SelectedAuthor.</span><span class="sxs-lookup"><span data-stu-id="566f0-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="566f0-156">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="566f0-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
