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
# <a name="openreport-macro-action"></a><span data-ttu-id="99f5c-102">Макрокоманда OpenReport</span><span class="sxs-lookup"><span data-stu-id="99f5c-102">OpenReport macro action</span></span>

<span data-ttu-id="99f5c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99f5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99f5c-104">С помощью макрокоманды **ОткрытьОтчет** можно открыть отчет в режиме конструктора или предварительный просмотр, а также отправить отчет непосредственно на принтер.</span><span class="sxs-lookup"><span data-stu-id="99f5c-104">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer.</span></span> <span data-ttu-id="99f5c-105">Кроме того, вы можете ограничить записи, которые будут печататься в отчете.</span><span class="sxs-lookup"><span data-stu-id="99f5c-105">You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="99f5c-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="99f5c-106">Setting</span></span>

<span data-ttu-id="99f5c-107">Макрокоманда **ОткрытьОтчет** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="99f5c-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99f5c-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="99f5c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="99f5c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="99f5c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99f5c-110">Имя отчета</span><span class="sxs-lookup"><span data-stu-id="99f5c-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="99f5c-111">Имя отчета, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="99f5c-111">The name of the report to open.</span></span> <span data-ttu-id="99f5c-112">В поле <strong>имя отчета</strong> в разделе <strong>аргументы макрокоманды</strong> области <strong>построителя макросов</strong> отображаются все отчеты в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="99f5c-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="99f5c-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="99f5c-113">This is a required argument.</span></span> <span data-ttu-id="99f5c-114">При запуске макроса, содержащего действие ОткрытьОтчет, в библиотечной базе данных Microsoft Access сначала ищет отчет с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="99f5c-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f5c-115">Просмотреть</span><span class="sxs-lookup"><span data-stu-id="99f5c-115">View</span></span></p></td>
<td><p><span data-ttu-id="99f5c-116">Представление, в котором будет открыт отчет.</span><span class="sxs-lookup"><span data-stu-id="99f5c-116">The view in which the report will open.</span></span> <span data-ttu-id="99f5c-117">В поле <strong>вид</strong> последовательно выберите пункты <strong>Печать</strong> (немедленное печать отчета), <strong>проектирование</strong>или <strong>Предварительный просмотр печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="99f5c-117">Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="99f5c-118">Значение по умолчанию — <strong>Printing</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f5c-118">The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f5c-119">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="99f5c-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="99f5c-120">Фильтр, который ограничит записи отчета.</span><span class="sxs-lookup"><span data-stu-id="99f5c-120">A filter that restricts the report's records.</span></span> <span data-ttu-id="99f5c-121">Можно ввести имя существующего запроса или фильтра, сохраненного в виде запроса.</span><span class="sxs-lookup"><span data-stu-id="99f5c-121">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="99f5c-122">Однако запрос должен включать все поля в отчете, которые вы открываете, или задать для свойства <strong>OutputAllFields</strong> значение <strong>"Да"</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f5c-122">However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99f5c-123">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="99f5c-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="99f5c-124">Допустимое предложение WHERE (без слова WHERE) или выражение, которое Access использует для выбора записей из базовой таблицы или запроса отчета.</span><span class="sxs-lookup"><span data-stu-id="99f5c-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="99f5c-125">Если выбран фильтр с аргументом имя фильтра, Access применяет это предложение WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="99f5c-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="99f5c-126">Чтобы открыть отчет и ограничить его записи записями, указанными в значении элемента управления в форме, используйте следующее выражение:</span><span class="sxs-lookup"><span data-stu-id="99f5c-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="99f5c-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong><em>FormName</em><strong>]! [</strong><em>контролнаме в форме</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="99f5c-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="99f5c-128">Замените <em>fieldname</em> именем поля в базовой таблице или запросе отчета, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="99f5c-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="99f5c-129">Замените <em>FormName</em> и <em>контролнаме в форме</em> , указав имя формы и элемент управления в форме, которая содержит значение, в котором будут сопоставлены записи в отчете.</span><span class="sxs-lookup"><span data-stu-id="99f5c-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="99f5c-130"><b>Note</b>: максимальная длина аргумента условия Where — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="99f5c-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="99f5c-131">Если вам нужно ввести более сложное предложение WHERE SQL, более длинное, используйте метод <b>ОткрытьОтчет</b> объекта <b>DoCmd</b> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="99f5c-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="99f5c-132">Вы можете ввести инструкции SQL WHERE, содержащие до 32 768 символов в VBA.</span><span class="sxs-lookup"><span data-stu-id="99f5c-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99f5c-133">Режим окна</span><span class="sxs-lookup"><span data-stu-id="99f5c-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="99f5c-134">Режим, в котором откроется отчет.</span><span class="sxs-lookup"><span data-stu-id="99f5c-134">The mode in which the report will open.</span></span> <span data-ttu-id="99f5c-135">Щелкните <strong>обычный</strong>, <strong>скрытый</strong>, <strong>значок</strong>или <strong>диалоговое окно</strong> в поле <strong>режим окна</strong> .</span><span class="sxs-lookup"><span data-stu-id="99f5c-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="99f5c-136">Значение по умолчанию — <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f5c-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="99f5c-137"><b>Note</b>: некоторые параметры аргументов режима окна не применяются при использовании документов с вкладками.</span><span class="sxs-lookup"><span data-stu-id="99f5c-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="99f5c-138">Чтобы переключиться на перекрывающиеся окна:</span><span class="sxs-lookup"><span data-stu-id="99f5c-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="99f5c-139">Нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f5c-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="99f5c-140">В диалоговом окне " <strong>Параметры Access</strong> " щелкните <strong>Текущая база данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f5c-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="99f5c-141">В разделе Параметры <strong>приложения</strong> в разделе <strong>Параметры окна документа</strong>щелкните <strong>перекрывающиеся окна</strong>.</span><span class="sxs-lookup"><span data-stu-id="99f5c-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="99f5c-142">Нажмите кнопку <strong>ОК</strong>, а затем закройте и снова откройте базу данных.</span><span class="sxs-lookup"><span data-stu-id="99f5c-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="99f5c-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="99f5c-143">Remarks</span></span>

<span data-ttu-id="99f5c-144">Параметр " **Печать** " для аргумента " **Просмотр** " отправляет отчет сразу с использованием текущих параметров принтера, не открывая диалоговое окно " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="99f5c-144">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box.</span></span> <span data-ttu-id="99f5c-145">Вы также можете использовать макрокоманду **ОткрытьОтчет (OpenReport** ), чтобы открыть и настроить отчет, а затем использовать действие печать для его печати.</span><span class="sxs-lookup"><span data-stu-id="99f5c-145">You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it.</span></span> <span data-ttu-id="99f5c-146">Например, может потребоваться изменить отчет или использовать действие **Печать** , чтобы изменить параметры принтера перед печатью.</span><span class="sxs-lookup"><span data-stu-id="99f5c-146">For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="99f5c-147">Фильтр и условие, где вы хотите применить, становятся значением свойства **Filter** отчета.</span><span class="sxs-lookup"><span data-stu-id="99f5c-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="99f5c-148">Действие **ОткрытьОтчет** аналогично двойному щелчку отчета в области навигации или щелчку правой кнопкой мыши отчета в области навигации и выбору представления или команды " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="99f5c-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="99f5c-149">Чтобы напечатать похожие отчеты для разных наборов данных, используйте фильтр или предложение WHERE, чтобы ограничить записи, печатаемые в отчете.</span><span class="sxs-lookup"><span data-stu-id="99f5c-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="99f5c-150">Затем измените макрос, чтобы применить другой фильтр или изменить аргумент условия отбора.</span><span class="sxs-lookup"><span data-stu-id="99f5c-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="99f5c-151">Отчет можно перетащить из области навигации в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="99f5c-151">You can drag a report from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="99f5c-152">При этом автоматически создается действие **ОткрытьОтчет** , которое открывает отчет в режиме отчета.</span><span class="sxs-lookup"><span data-stu-id="99f5c-152">This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="99f5c-153">Пример</span><span class="sxs-lookup"><span data-stu-id="99f5c-153">Example</span></span>

<span data-ttu-id="99f5c-154">В приведенном ниже примере показано, как с помощью макрокоманды ОткрытьОтчет передать параметр, который фильтрует отчет при его открытии.</span><span class="sxs-lookup"><span data-stu-id="99f5c-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="99f5c-155">В отчете **рптчаптерс** отображаются записи указанного автора путем передачи элемента, выбранного в поле со списком **кбоаусорс** , в параметр селектедаусор.</span><span class="sxs-lookup"><span data-stu-id="99f5c-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="99f5c-156">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="99f5c-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
