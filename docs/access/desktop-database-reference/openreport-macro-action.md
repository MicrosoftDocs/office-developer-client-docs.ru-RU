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
# <a name="openreport-macro-action"></a><span data-ttu-id="df7ef-102">Макрокоманда OpenReport</span><span class="sxs-lookup"><span data-stu-id="df7ef-102">OpenReport macro action</span></span>

<span data-ttu-id="df7ef-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df7ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df7ef-104">Вы можете использовать **действие OpenReport,** чтобы открыть отчет в представлении Design или Print Preview или отправить отчет непосредственно на принтер.</span><span class="sxs-lookup"><span data-stu-id="df7ef-104">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer.</span></span> <span data-ttu-id="df7ef-105">Кроме того, вы можете ограничить записи, которые будут печататься в отчете.</span><span class="sxs-lookup"><span data-stu-id="df7ef-105">You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="df7ef-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="df7ef-106">Setting</span></span>

<span data-ttu-id="df7ef-107">Действие **OpenReport** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="df7ef-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df7ef-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="df7ef-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="df7ef-109">Описание</span><span class="sxs-lookup"><span data-stu-id="df7ef-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df7ef-110">Имя отчета</span><span class="sxs-lookup"><span data-stu-id="df7ef-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="df7ef-111">Имя открываемого отчета.</span><span class="sxs-lookup"><span data-stu-id="df7ef-111">The name of the report to open.</span></span> <span data-ttu-id="df7ef-112">Поле <strong>Имя отчета</strong> в разделе <strong>Аргументы</strong> действий области <strong>Macro Builder</strong> отображает все отчеты в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="df7ef-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="df7ef-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="df7ef-113">This is a required argument.</span></span> <span data-ttu-id="df7ef-114">Если вы запустите макрос, содержащий действие OpenReport в базе данных библиотеки, Microsoft Access сначала ищет отчет с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="df7ef-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df7ef-115">Просмотреть</span><span class="sxs-lookup"><span data-stu-id="df7ef-115">View</span></span></p></td>
<td><p><span data-ttu-id="df7ef-116">Представление, в котором откроется отчет.</span><span class="sxs-lookup"><span data-stu-id="df7ef-116">The view in which the report will open.</span></span> <span data-ttu-id="df7ef-117">Нажмите <strong>кнопку Печать</strong> (немедленно <strong>распечатайте</strong>отчет), Дизайн или <strong>Распечатайте предварительный</strong> просмотр в <strong>поле Просмотр.</strong></span><span class="sxs-lookup"><span data-stu-id="df7ef-117">Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="df7ef-118">По умолчанию значение <strong>Print</strong>.</span><span class="sxs-lookup"><span data-stu-id="df7ef-118">The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df7ef-119">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="df7ef-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="df7ef-120">Фильтр, ограничивающий записи отчета.</span><span class="sxs-lookup"><span data-stu-id="df7ef-120">A filter that restricts the report's records.</span></span> <span data-ttu-id="df7ef-121">Можно ввести имя существующего запроса или фильтра, сохраненного в качестве запроса.</span><span class="sxs-lookup"><span data-stu-id="df7ef-121">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="df7ef-122">Однако запрос должен включать все поля в открываемом отчете или иметь свойство <strong>OutputAllFields</strong> для <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="df7ef-122">However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df7ef-123">Где состояние</span><span class="sxs-lookup"><span data-stu-id="df7ef-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="df7ef-124">Допустимый SQL where (без слова WHERE) или выражение, которое Access использует для выбора записей из таблицы или запроса отчета.</span><span class="sxs-lookup"><span data-stu-id="df7ef-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="df7ef-125">Если выбрать фильтр с аргументом Имя фильтра, Access применяет этот пункт WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="df7ef-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="df7ef-126">Чтобы открыть отчет и ограничить его записи теми, которые указаны значением управления в форме, используйте следующее выражение:</span><span class="sxs-lookup"><span data-stu-id="df7ef-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="df7ef-127">
<strong>[имя</strong><em>поля]</em><strong>= Формы! [</strong><em>имя формы</em><strong>]! [</strong><em>имя управления в форме</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="df7ef-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="df7ef-128">Замените <em>имя поля</em> и имя поля в таблице или запросе отчета, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="df7ef-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="df7ef-129">Замените имя <em></em> <em>формы</em> и имя управления в форме с именем формы и управлением в форме, которая содержит необходимое значение записей в отчете.</span><span class="sxs-lookup"><span data-stu-id="df7ef-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="df7ef-130"><b>ПРИМЕЧАНИЕ.</b>Максимальная длина аргумента Where Condition — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="df7ef-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="df7ef-131">Если требуется ввести более сложный пункт SQL WHERE дольше, используйте метод <b>OpenReport</b> объекта <b>DoCmd</b> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="df7ef-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="df7ef-132">Вы можете ввести SQL, где в VBA можно ввести утверждения о клаузулах до 32 768 знаков.</span><span class="sxs-lookup"><span data-stu-id="df7ef-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df7ef-133">Режим окна</span><span class="sxs-lookup"><span data-stu-id="df7ef-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="df7ef-134">Режим, в котором откроется отчет.</span><span class="sxs-lookup"><span data-stu-id="df7ef-134">The mode in which the report will open.</span></span> <span data-ttu-id="df7ef-135">Щелкните <strong>нормальный,</strong> <strong>скрытый,</strong> <strong>значок</strong>или <strong>диалоговое окно</strong> <strong>в окне Режим</strong> окна.</span><span class="sxs-lookup"><span data-stu-id="df7ef-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="df7ef-136">По умолчанию является <strong>нормальным</strong>.</span><span class="sxs-lookup"><span data-stu-id="df7ef-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="df7ef-137"><b>ПРИМЕЧАНИЕ.</b>Некоторые параметры аргумента в режиме окна не применяются при использовании документов на вкладке.</span><span class="sxs-lookup"><span data-stu-id="df7ef-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="df7ef-138">Чтобы перейти на перекрывающиеся окна:</span><span class="sxs-lookup"><span data-stu-id="df7ef-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="df7ef-139">Нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="df7ef-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="df7ef-140">В <strong>диалоговом окне Параметры</strong> доступа щелкните <strong>Текущая база данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="df7ef-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="df7ef-141">В разделе <strong>Параметры приложений</strong> в <strong>разделе Параметры окна документов</strong>нажмите <strong>кнопку Перекрытие Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="df7ef-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="df7ef-142">Нажмите <strong>кнопку ОК,</strong>а затем закрыть и открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="df7ef-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="df7ef-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="df7ef-143">Remarks</span></span>

<span data-ttu-id="df7ef-144">Параметр **Print** для аргумента **View** немедленно печатает отчет с помощью текущих параметров принтера, не выведя диалоговое окно **Print.**</span><span class="sxs-lookup"><span data-stu-id="df7ef-144">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box.</span></span> <span data-ttu-id="df7ef-145">Вы также можете использовать **действие OpenReport** для открытия и настроить отчет, а затем использовать действие PrintOut для его печати.</span><span class="sxs-lookup"><span data-stu-id="df7ef-145">You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it.</span></span> <span data-ttu-id="df7ef-146">Например, перед печатью может потребоваться изменить отчет или использовать действие **PrintOut** для изменения параметров принтера.</span><span class="sxs-lookup"><span data-stu-id="df7ef-146">For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="df7ef-147">Фильтр и условия WHERE, которые вы применяли, становятся параметром свойства **Фильтр отчетов.**</span><span class="sxs-lookup"><span data-stu-id="df7ef-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="df7ef-148">Действие **OpenReport** аналогично дважды щелкнуть отчет в области навигации или щелкнуть правой кнопкой мыши отчет в области навигации и выбрать представление или команду **Печать.**</span><span class="sxs-lookup"><span data-stu-id="df7ef-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="df7ef-149">Чтобы напечатать аналогичные отчеты для различных наборов данных, используйте фильтр или пункт WHERE, чтобы ограничить записи, напечатанные в отчете.</span><span class="sxs-lookup"><span data-stu-id="df7ef-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="df7ef-150">Затем измените макрос, чтобы применить другой фильтр или изменить аргумент Where Condition.</span><span class="sxs-lookup"><span data-stu-id="df7ef-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="df7ef-151">Отчет можно перетаскивать из области навигации в строку действий макроса.</span><span class="sxs-lookup"><span data-stu-id="df7ef-151">You can drag a report from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="df7ef-152">Это автоматически создает действие **OpenReport,** которое открывает отчет в представлении Report.</span><span class="sxs-lookup"><span data-stu-id="df7ef-152">This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="df7ef-153">Пример</span><span class="sxs-lookup"><span data-stu-id="df7ef-153">Example</span></span>

<span data-ttu-id="df7ef-154">В следующем примере показано, как использовать действие OpenReport для передачи параметра, который фильтрует отчет при его открытиях.</span><span class="sxs-lookup"><span data-stu-id="df7ef-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="df7ef-155">Отчет **rptChapters** отображает записи для указанного автора, передав элемент, выбранный в комбо-окне **cboAuthors,** параметру SelectedAuthor.</span><span class="sxs-lookup"><span data-stu-id="df7ef-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="df7ef-156">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="df7ef-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
