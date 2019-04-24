---
title: Макрокоманда ExportWithFormatting
TOCTitle: ExportWithFormatting macro action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb633977fcc1b39fc2a5c0bb69523bc93c193695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293212"
---
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="e63be-102">Макрокоманда ExportWithFormatting</span><span class="sxs-lookup"><span data-stu-id="e63be-102">ExportWithFormatting macro action</span></span>


<span data-ttu-id="e63be-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e63be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e63be-104">Вы можете использовать действие **ExportWithFormatting** для вывода данных в указанном объекте базы данных Microsoft Access (таблица, форма, отчет, модуль или страница доступа к данным) для нескольких форматов вывода.</span><span class="sxs-lookup"><span data-stu-id="e63be-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="e63be-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e63be-105">Settings</span></span>

<span data-ttu-id="e63be-106">Действие **ExportWithFormatting** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e63be-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e63be-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="e63be-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e63be-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e63be-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e63be-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-110">Тип объекта с данными для вывода.</span><span class="sxs-lookup"><span data-stu-id="e63be-110">The type of object containing the data to output.</span></span> <span data-ttu-id="e63be-111">Нажмите <strong>Таблицы</strong> (для рабочего листа таблицы), <strong>Запрос</strong> (для запроса рабочего лив режиме таблицы), <strong>формы</strong> (для формы или форме в режиме таблицы), <strong>отчет</strong>, <strong> Модуль</strong>, <strong>представление сервера</strong>, <strong>хранимая процедура</strong>, или <strong>функция</strong> в <strong>тип объекта</strong> поле в <strong> Аргументы макрокоманды</strong> области конструктора макросов.</span><span class="sxs-lookup"><span data-stu-id="e63be-111">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="e63be-112">Невозможно использовать макрос в качестве вывода.</span><span class="sxs-lookup"><span data-stu-id="e63be-112">You can't output a macro.</span></span> <span data-ttu-id="e63be-113">Если вы хотите вывести активный объект, выберите его тип для этого аргумента, но оставьте аргумент <strong>Object Name</strong> пустым.</span><span class="sxs-lookup"><span data-stu-id="e63be-113">If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span> <span data-ttu-id="e63be-114">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="e63be-114">This is a required argument.</span></span> <span data-ttu-id="e63be-115">Значение по умолчанию: <strong>Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="e63be-115">The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e63be-116"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-117">Имя объекта с данными для вывода.</span><span class="sxs-lookup"><span data-stu-id="e63be-117">The name of the object containing the data to output.</span></span> <span data-ttu-id="e63be-118">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="e63be-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="e63be-119">При выполнении макроса, содержащего макрокоманду <strong>ExportWithFormatting</strong> в базе данных библиотеки, Access сначала выполняет поиск объекта с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="e63be-119">If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e63be-120"><strong>Output Format</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-121">Тип формата, который вы хотите использовать для вывода данных.</span><span class="sxs-lookup"><span data-stu-id="e63be-121">The type of format you want to use to output the data.</span></span> <span data-ttu-id="e63be-122">Вы можете выбрать <strong>рабочая книга Excel 97 - Excel 2003 (*.xls)</strong>, <strong>двоичная книга Excel (*.xlsb)</strong>, <strong>рабочая книга Excel (.xlsx)</strong>, <strong>HTML (*.htm; \* .html)</strong>, <strong>рабочая книга Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>формат PDF (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>текстовые файлы (*.txt) </strong>, или <strong>формат XPS (*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="e63be-122">You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>.</span></span> <span data-ttu-id="e63be-123">Если оставить этот аргумент пустым, Access попросит вас определить выходной формат.</span><span class="sxs-lookup"><span data-stu-id="e63be-123">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e63be-124"><strong>Output File</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-125">Файл, в который вы хотите вывести данные, включая полный путь.</span><span class="sxs-lookup"><span data-stu-id="e63be-125">The file to which you want to output the data, including the full path.</span></span> <span data-ttu-id="e63be-126">Вы можете включить стандартное расширение имени файла для формата вывода, выбранного в аргументе <strong>Output Format</strong>, но это необязательно.</span><span class="sxs-lookup"><span data-stu-id="e63be-126">You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required.</span></span> <span data-ttu-id="e63be-127">Если оставить аргумент <strong>Output File</strong> пустым, Access попросит вас определить имя файла.</span><span class="sxs-lookup"><span data-stu-id="e63be-127">If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e63be-128"><strong>Auto Start</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-129">Указывает, должно ли соответствующее программное обеспечение запускаться сразу же после запуска макрокоманды <strong>ExportWithFormatting</strong> с файлом, заданным открытым аргументом <strong>Output File</strong>.</span><span class="sxs-lookup"><span data-stu-id="e63be-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e63be-130"><strong>Template File</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-131">Имя файла и путь файла, который вы хотите использовать в качестве шаблона для HTML-файлов.</span><span class="sxs-lookup"><span data-stu-id="e63be-131">The path and file name of a file you want to use as a template for HTML files.</span></span> <span data-ttu-id="e63be-132">Файл шаблона представляет собой текстовый файл, который содержит HTML-теги и маркеры, которые являются уникальными для Access.</span><span class="sxs-lookup"><span data-stu-id="e63be-132">The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e63be-133"><strong>Encoding</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-134">Тип формата кодировки символов, который вы хотите использовать для вывода текста или HTML-данных.</span><span class="sxs-lookup"><span data-stu-id="e63be-134">The type of character encoding format you want used to output the text or HTML data.</span></span> <span data-ttu-id="e63be-135">Вы можете использовать <strong>MS-DOS</strong>, <strong>Юникод</strong> или <strong>Юникод (UTF-8)</strong>.</span><span class="sxs-lookup"><span data-stu-id="e63be-135">You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>.</span></span> <span data-ttu-id="e63be-136">Значение аргумента <strong>MS-DOS</strong> доступно только для текстовых файлов.</span><span class="sxs-lookup"><span data-stu-id="e63be-136">The <strong>MS-DOS</strong> argument setting is available only for text files.</span></span> <span data-ttu-id="e63be-137">Если оставить этот аргумент пустым, Access выводит данные с помощью стандартной кодировки Windows для текстовых файлов и системной кодировки для HTML-файлов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e63be-137">If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e63be-138"><strong>Output Quality</strong></span><span class="sxs-lookup"><span data-stu-id="e63be-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="e63be-139">Выберите <strong>Print</strong>, чтобы оптимизировать вывод для печати, или <strong>Screen</strong>, чтобы оптимизировать вывод для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="e63be-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e63be-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e63be-140">Remarks</span></span>

<span data-ttu-id="e63be-141">Данные Access выводятся в выбранном формате и могут считываться любой программой, использующей такой же формат.</span><span class="sxs-lookup"><span data-stu-id="e63be-141">The Access data is output in the selected format and can be read by any program that uses the same format.</span></span> <span data-ttu-id="e63be-142">Например, вы можете вывести отчет Access с сохранением форматирования в формате документа RTF и затем открыть его в Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="e63be-142">For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="e63be-143">При выводе объекта базы данных в формате HTML Access создает файл в формате HTML, содержащий данные из объекта.</span><span class="sxs-lookup"><span data-stu-id="e63be-143">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object.</span></span> <span data-ttu-id="e63be-144">Вы можете использовать аргумент **Template File**, чтобы указать файл, который нужно будет использоваться в качестве шаблона для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="e63be-144">You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="e63be-145">Следующие правила применяются при использовании макрокоманды **ExportWithFormatting** для вывода объекта базы данных в любом из форматов вывода:</span><span class="sxs-lookup"><span data-stu-id="e63be-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="e63be-146">Можно выводить данные в виде таблиц, запросов и форм в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="e63be-146">You can output data in table, query, and form datasheets.</span></span> <span data-ttu-id="e63be-147">В выходном файле все поля в таблице отображаются так же, как и в Access, за исключением полей, содержащих объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="e63be-147">In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects.</span></span> <span data-ttu-id="e63be-148">Столбцы для полей объекта OLE включаются в выходной файл, но поля пусты.</span><span class="sxs-lookup"><span data-stu-id="e63be-148">The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="e63be-149">Для элемента управления, привязанного к логическому полю (выключатель, кнопка выбора или флажок) в выходном файле выводится значение -1 (Да) или 0 (нет).</span><span class="sxs-lookup"><span data-stu-id="e63be-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="e63be-150">Для текстового поля, привязанного к полю гиперссылки, в выходном файле выводится гиперссылка для всех выходных форматов, кроме текста MS-DOS (в этом случае ссылка будет отображаться как обычный текст).</span><span class="sxs-lookup"><span data-stu-id="e63be-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="e63be-151">При выводе данных в форме в режиме формы выходной файл всегда содержит форму в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="e63be-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="e63be-152">При выводе таблицы, формы или страницы доступа к данным в формате HTML создается один HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="e63be-152">When you output a datasheet, form, or data access page in HTML format, one .html file is created.</span></span> <span data-ttu-id="e63be-153">При выводе отчета в формате HTML для каждой его страницы создается отдельный HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="e63be-153">When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="e63be-154">Результат выполнения макрокоманды **ExportWithFormatting** повторяет выбор один из вариантов в группе **Export** на вкладке **External Data**. Аргументы макрокоманды соответствуют параметрам диалогового окна **Export**.</span><span class="sxs-lookup"><span data-stu-id="e63be-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="e63be-155">Чтобы выполнить макрокоманду **ExportWithFormatting** в модуле Visual Basic для приложений (VBA), используйте метод **OutputTo** объекта **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e63be-155">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>

