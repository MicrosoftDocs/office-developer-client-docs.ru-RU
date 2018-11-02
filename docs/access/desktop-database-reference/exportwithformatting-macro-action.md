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
ms.openlocfilehash: ae03262489b707257a4aee93e4380aa70329856a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924437"
---
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="7c41f-102">Макрокоманда ExportWithFormatting</span><span class="sxs-lookup"><span data-stu-id="7c41f-102">ExportWithFormatting macro action</span></span>


<span data-ttu-id="7c41f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c41f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c41f-104">Действие **ExportWithFormatting** можно использовать для вывода данных в указанном Microsoft Access объект базы данных (таблицы, формы, отчета, модуль или страницы доступа к данным) в нескольких форматах.</span><span class="sxs-lookup"><span data-stu-id="7c41f-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="7c41f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c41f-105">Settings</span></span>

<span data-ttu-id="7c41f-106">Действие **ExportWithFormatting** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="7c41f-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c41f-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="7c41f-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7c41f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7c41f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c41f-109"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-110">Тип object, содержащий данные для вывода.</span><span class="sxs-lookup"><span data-stu-id="7c41f-110">The type of object containing the data to output.</span></span> <span data-ttu-id="7c41f-111">Нажмите кнопку <strong>таблицы</strong> (таблицы), <strong>запрос</strong> (для таблицы запросов), <strong>формы</strong> (для формы или формы таблицы), <strong>отчет</strong>, <strong>модуль</strong>, <strong>Представление</strong>, <strong>Хранимую процедуру</strong>или <strong>функцию</strong> в <strong>объект Тип</strong> флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="7c41f-111">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="7c41f-112">Не удается вывода макроса.</span><span class="sxs-lookup"><span data-stu-id="7c41f-112">You can't output a macro.</span></span> <span data-ttu-id="7c41f-113">Если вы хотите вывода активного объекта, выберите его тип, но оставить пустым аргумента <strong>Имя объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="7c41f-113">If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span> <span data-ttu-id="7c41f-114">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="7c41f-114">This is a required argument.</span></span> <span data-ttu-id="7c41f-115">Значение по умолчанию — <strong>в таблице</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c41f-115">The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c41f-116"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-117">Имя объекта, содержащего данные для вывода.</span><span class="sxs-lookup"><span data-stu-id="7c41f-117">The name of the object containing the data to output.</span></span> <span data-ttu-id="7c41f-118">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="7c41f-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="7c41f-119">Если макрос, содержащий действие <strong>ExportWithFormatting</strong> в базе данных библиотеки, сначала поиск объекта с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="7c41f-119">If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c41f-120"><strong>Формат выходных данных</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-121">Тип формата, который будет использоваться для вывода данных.</span><span class="sxs-lookup"><span data-stu-id="7c41f-121">The type of format you want to use to output the data.</span></span> <span data-ttu-id="7c41f-122">Можно выбрать <strong>Excel 97 - 2003 книги Excel (*.xls)</strong>, <strong>Двоичная книга Excel (*.xlsb)</strong>, <strong>Книга Excel (XLSX)</strong> <strong>HTML (*.htm; \* .html)</strong>, <strong>Книга Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Формат PDF (*.pdf)</strong>, <strong> Текст в формате RTF (*.rtf)</strong>, <strong>текстовые файлы (*.txt)</strong>или в <strong>формате XPS (*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c41f-122">You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>.</span></span> <span data-ttu-id="7c41f-123">Если оставить это аргумент, Access запрашивает выходной формат.</span><span class="sxs-lookup"><span data-stu-id="7c41f-123">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c41f-124"><strong>Выходной файл</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-125">Файл, который будет использоваться для вывода данных, включая полный путь.</span><span class="sxs-lookup"><span data-stu-id="7c41f-125">The file to which you want to output the data, including the full path.</span></span> <span data-ttu-id="7c41f-126">Может включать стандартное расширение имени файла для выходной формат, выбранный вами с аргументом <strong>Выходной формат</strong> , но не требуется.</span><span class="sxs-lookup"><span data-stu-id="7c41f-126">You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required.</span></span> <span data-ttu-id="7c41f-127">Если аргумент <strong>Выходного файла</strong> оставить пустым, приглашение ввести имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7c41f-127">If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c41f-128"><strong>Автоматический запуск</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-129">Указывает, следует ли соответствующее программное обеспечение для запуска сразу после выполнения действия <strong>ExportWithFormatting</strong> с файлом, указанным в аргументе <strong>Выходной файл</strong> открыт.</span><span class="sxs-lookup"><span data-stu-id="7c41f-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c41f-130"><strong>Файл шаблона</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-131">Путь и имя файла, который будет использоваться как шаблон для файлов HTML.</span><span class="sxs-lookup"><span data-stu-id="7c41f-131">The path and file name of a file you want to use as a template for HTML files.</span></span> <span data-ttu-id="7c41f-132">Файл шаблона — это текстовый файл, который включает в себя теги HTML и маркеры, которые являются уникальными для Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7c41f-132">The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c41f-133"><strong>Кодировка</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-134">Тип формата кодировки, который будет использовать для вывода текста или данных HTML.</span><span class="sxs-lookup"><span data-stu-id="7c41f-134">The type of character encoding format you want used to output the text or HTML data.</span></span> <span data-ttu-id="7c41f-135">Можно выбрать <strong>MS-DOS</strong>, <strong>Unicode</strong>или <strong>Юникод (UTF-8)</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c41f-135">You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>.</span></span> <span data-ttu-id="7c41f-136">Значение аргумента <strong>MS-DOS</strong> доступен только для текстовых файлов.</span><span class="sxs-lookup"><span data-stu-id="7c41f-136">The <strong>MS-DOS</strong> argument setting is available only for text files.</span></span> <span data-ttu-id="7c41f-137">Если оставить это аргумент, Access выводит данные с помощью Windows кодировка по умолчанию для текстовых файлов и системы по умолчанию, кодировка HTML-файлы.</span><span class="sxs-lookup"><span data-stu-id="7c41f-137">If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c41f-138"><strong>Качество вывода</strong></span><span class="sxs-lookup"><span data-stu-id="7c41f-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="7c41f-139">Выберите <strong>Print</strong> для оптимизации выходные данные для печати или <strong>экрана</strong> , чтобы оптимизировать выходных данных для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="7c41f-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7c41f-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c41f-140">Remarks</span></span>

<span data-ttu-id="7c41f-141">Доступ к данным — это выходные данные в выбранном формате и доступны для чтения, все программы, которая использует тот же формат.</span><span class="sxs-lookup"><span data-stu-id="7c41f-141">The Access data is output in the selected format and can be read by any program that uses the same format.</span></span> <span data-ttu-id="7c41f-142">Например можно отчет с форматированием в формате RTF документ Microsoft Access и затем откройте документ в Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="7c41f-142">For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="7c41f-143">При выводе объекта базы данных в формат HTML создается файл в формате HTML, содержащие данные из объекта.</span><span class="sxs-lookup"><span data-stu-id="7c41f-143">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object.</span></span> <span data-ttu-id="7c41f-144">Аргумент **Файл шаблона** можно использовать для указания файла для использования в качестве шаблона для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="7c41f-144">You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="7c41f-145">При использовании **ExportWithFormatting** действие для вывода объекта базы данных на любой из форматов вывода, применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="7c41f-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="7c41f-146">При выводе данных в таблице, запросов и формы в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="7c41f-146">You can output data in table, query, and form datasheets.</span></span> <span data-ttu-id="7c41f-147">В выходной файл как в клиенте, за исключением полей, содержащих объекты OLE отображаются все поля в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="7c41f-147">In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects.</span></span> <span data-ttu-id="7c41f-148">Столбцы для полей объектов OLE, которые включаются в выходной файл, но полей являются пустыми.</span><span class="sxs-lookup"><span data-stu-id="7c41f-148">The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="7c41f-149">Для элемента управления, присоединенного к полю Да/Нет (выключатель, переключатель или флажок), файл выходных данных отображает значение -1 (Да), либо 0 (нет).</span><span class="sxs-lookup"><span data-stu-id="7c41f-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="7c41f-150">Для текстового поля, привязанного к полю гиперссылки, файл выходных данных отображает гиперссылку для всех выходных форматов, за исключением текста MS-DOS (в этом случае отображается гиперссылка как обычный текст).</span><span class="sxs-lookup"><span data-stu-id="7c41f-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="7c41f-151">При выводе данных формы в режиме формы выходного файла всегда содержит представление таблицы данных формы.</span><span class="sxs-lookup"><span data-stu-id="7c41f-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="7c41f-152">При выводе таблицы, формы или страницы доступа к данным в формате HTML создается один HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="7c41f-152">When you output a datasheet, form, or data access page in HTML format, one .html file is created.</span></span> <span data-ttu-id="7c41f-153">При выводе отчета в формате HTML для каждой страницы в отчете создается один файл .html.</span><span class="sxs-lookup"><span data-stu-id="7c41f-153">When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="7c41f-154">В результате выполнения действия **ExportWithFormatting** аналогична щелкнув один из вариантов в группе **Экспорт** на вкладке **Внешних данных** . Аргументы действие соответствуют параметрам в диалоговом окне " **Экспорт** ".</span><span class="sxs-lookup"><span data-stu-id="7c41f-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="7c41f-155">Чтобы выполнить действие **ExportWithFormatting** в Visual Basic для приложений (VBA) модуль, используйте метод **OutputTo** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="7c41f-155">To run the **ExportWithFormatting** action in a Visual Basic for Applications (VBA) module, use the **OutputTo** method of the **DoCmd** object.</span></span>

