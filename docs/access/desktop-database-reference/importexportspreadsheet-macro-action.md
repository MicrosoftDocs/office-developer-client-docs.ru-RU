---
title: ImportExportSpreadsheet Macro Action
TOCTitle: ImportExportSpreadsheet Macro Action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4693cbe643ab34431f7920564e704808c1b0f73b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480394"
---
# <a name="importexportspreadsheet-macro-action"></a><span data-ttu-id="dd2d6-102">ImportExportSpreadsheet Macro Action</span><span class="sxs-lookup"><span data-stu-id="dd2d6-102">ImportExportSpreadsheet Macro Action</span></span>


<span data-ttu-id="dd2d6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd2d6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd2d6-104">Действие **ImportExportSpreadsheet** можно использовать для импорта или экспорта данных между текущей базы данных Access (MDB- или .accdb) или проект Microsoft Access (файлы с расширением ADP) и файла электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-104">You can use the **ImportExportSpreadsheet** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and a spreadsheet file.</span></span> <span data-ttu-id="dd2d6-105">Также можно связать данные в электронную таблицу Microsoft Excel для текущей базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-105">You can also link the data in a Microsoft Excel spreadsheet to the current Microsoft Access database.</span></span> <span data-ttu-id="dd2d6-106">Связывания электронной таблицы можно просматривать и изменять данные электронной таблицы с доступом по-прежнему предоставляя полный доступ к данным из программы электронной таблицы Excel.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-106">With a linked spreadsheet, you can view and edit the spreadsheet data with Access while still allowing complete access to the data from your Excel spreadsheet program.</span></span> <span data-ttu-id="dd2d6-107">Также можно связать с данным в файл электронной таблицы Lotus 1-2-3, но эти данные в доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-107">You can also link to data in a Lotus 1-2-3 spreadsheet file, but this data is read-only in Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dd2d6-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="dd2d6-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="dd2d6-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="dd2d6-110">Setting</span></span>

<span data-ttu-id="dd2d6-111">**ПреобразоватьЭлектроннуюТаблицу** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-111">The **TransferSpreadsheet** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd2d6-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="dd2d6-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dd2d6-113">Описание</span><span class="sxs-lookup"><span data-stu-id="dd2d6-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd2d6-114"><strong>Тип передачи</strong></span><span class="sxs-lookup"><span data-stu-id="dd2d6-114"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="dd2d6-115">Тип переноса, который требуется сделать.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-115">The type of transfer you want to make.</span></span> <span data-ttu-id="dd2d6-116">Выберите <strong>Импорт</strong>, <strong>Экспорт</strong>или <strong>ссылку</strong> в поле <strong>Тип преобразования</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-116">Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="dd2d6-117">Значение по умолчанию — <strong>Импорт</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-117">The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="dd2d6-118">Тип передачи <STRONG>связи</STRONG> не поддерживается для проектов Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="dd2d6-118">The <STRONG>Link</STRONG> transfer type is not supported for Access projects (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd2d6-119"><strong>Тип электронной таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="dd2d6-119"><strong>Spreadsheet Type</strong></span></span></p></td>
<td><p><span data-ttu-id="dd2d6-120">Тип электронной таблицы для импорта, экспорта или ссылка на.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-120">The type of spreadsheet to import from, export to, or link to.</span></span> <span data-ttu-id="dd2d6-121">В поле можно выбрать один из нескольких типов электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-121">You can select one of a number of spreadsheet types in the box.</span></span> <span data-ttu-id="dd2d6-122">Значение по умолчанию — <strong>Книги Excel</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-122">The default is <strong>Excel Workbook</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="dd2d6-123">Можно импортировать из и ссылка на Lotus (только для чтения). Файлы WK4, но не может экспортировать доступ к данным в данном формате электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-123">You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format.</span></span> <span data-ttu-id="dd2d6-124">Access больше не поддерживает импорт, экспорт или связывание данных из Lotus. WKS или электронные таблицы Excel версии 2.0 с помощью этого действия.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-124">Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action.</span></span> <span data-ttu-id="dd2d6-125">Если вы хотите импортировать из или ссылка на данные электронной таблицы в Excel версии 2.0 или Lotus. WKS форматирование, преобразование данных электронных таблиц в более поздней версии Excel или Lotus 1-2-3 перед Импорт или связывание данных в Access.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-125">If you want to import from or link to spreadsheet data in Excel version 2.0 or Lotus .WKS format, convert the spreadsheet data to a later version of Excel or Lotus 1-2-3 before importing or linking the data into Access.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd2d6-126"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="dd2d6-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dd2d6-127">Имя таблицы Access Импорт данных электронных таблиц для экспорта данных электронной таблицы из или связывание данных электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-127">The name of the Access table to import spreadsheet data to, export spreadsheet data from, or link spreadsheet data to.</span></span> <span data-ttu-id="dd2d6-128">Также можно ввести имя доступа выберите запрос, который необходимо экспортировать данные из.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-128">You can also type the name of the Access select query you want to export data from.</span></span> <span data-ttu-id="dd2d6-129">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-129">This is a required argument.</span></span> <span data-ttu-id="dd2d6-130">При выборе <strong>импорта</strong> в аргументе <strong>Тип</strong> доступа добавляет данным электронных таблиц в этой таблице, если таблица уже существует.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-130">If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument, Access appends the spreadsheet data to this table if the table already exists.</span></span> <span data-ttu-id="dd2d6-131">В противном случае создается новая таблица с данными электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-131">Otherwise, Access creates a new table containing the spreadsheet data.</span></span> <span data-ttu-id="dd2d6-132">В клиенте нельзя использовать инструкции SQL для указания данных для экспорта при использовании <strong>ImportExportSpreadsheet</strong> действие.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-132">In Access, you can't use an SQL statement to specify data to export when you are using the <strong>ImportExportSpreadsheet</strong> action.</span></span> <span data-ttu-id="dd2d6-133">Вместо использования инструкции SQL, необходимо сначала создать запрос и затем указать имя запроса в качестве аргумента <strong>Имя таблицы</strong> .</span><span class="sxs-lookup"><span data-stu-id="dd2d6-133">Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd2d6-134"><strong>Имя файла</strong></span><span class="sxs-lookup"><span data-stu-id="dd2d6-134"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dd2d6-135">Имя файла электронной таблицы для импорта, экспорта или ссылка на.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-135">The name of the spreadsheet file to import from, export to, or link to.</span></span> <span data-ttu-id="dd2d6-136">Включите полный путь.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-136">Include the full path.</span></span> <span data-ttu-id="dd2d6-137">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-137">This is a required argument.</span></span> <span data-ttu-id="dd2d6-138">Access создает новую таблицу при экспорте данных из Access.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-138">Access creates a new spreadsheet when you export data from Access.</span></span> <span data-ttu-id="dd2d6-139">Если имя файла совпадает с именем существующей электронной таблицы, Access заменяет существующей электронной таблицы, если не экспорте книги 5.0 или более поздней версии Excel.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-139">If the file name is the same as the name of an existing spreadsheet, Access replaces the existing spreadsheet, unless you're exporting to an Excel version 5.0 or later workbook.</span></span> <span data-ttu-id="dd2d6-140">В этом случае Access копирует экспортируемых данных доступен следующий нового листа в книге.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-140">In that case, Access copies the exported data to the next available new worksheet in the workbook.</span></span> <span data-ttu-id="dd2d6-141">При импорте из или ссылки на Excel версий 5.0 или более поздних версий, определенного рабочего листа можно указать с помощью аргумент <strong>диапазон</strong> .</span><span class="sxs-lookup"><span data-stu-id="dd2d6-141">If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can specify a particular worksheet by using the <strong>Range</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd2d6-142"><strong>Содержит имена полей</strong></span><span class="sxs-lookup"><span data-stu-id="dd2d6-142"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="dd2d6-143">Указывает, содержит ли первой строки электронной таблицы имена полей.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-143">Specifies whether the first row of the spreadsheet contains the names of the fields.</span></span> <span data-ttu-id="dd2d6-144">Если выбран вариант <strong>Да</strong>, Access использует имена в этой строке как имена полей таблицы Microsoft Access при Импорт или связывание данных электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-144">If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the spreadsheet data.</span></span> <span data-ttu-id="dd2d6-145">Если выбран вариант <strong>Нет</strong>, Access рассматривается как обычная строка данных первой строки.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-145">If you select <strong>No</strong>, Access treats the first row as a normal row of data.</span></span> <span data-ttu-id="dd2d6-146">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-146">The default is <strong>No</strong>.</span></span> <span data-ttu-id="dd2d6-147">При экспорте таблицы Microsoft Access или выборку в электронную таблицу имена полей вставляется в первую строку электронной таблицы независимо от того, вы выбираете в этот аргумент.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-147">When you export an Access table or select query to a spreadsheet, the field names are inserted into the first row of the spreadsheet no matter what you select in this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd2d6-148"><strong>Range</strong></span><span class="sxs-lookup"><span data-stu-id="dd2d6-148"><strong>Range</strong></span></span></p></td>
<td><p><span data-ttu-id="dd2d6-149">Диапазон ячеек для импорта.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-149">The range of cells to import or link.</span></span> <span data-ttu-id="dd2d6-150">Оставьте данный аргумент пустым, чтобы импортировать или связать всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-150">Leave this argument blank to import or link the entire spreadsheet.</span></span> <span data-ttu-id="dd2d6-151">Можно ввести имя диапазона в электронной таблице или указать диапазон ячеек для импорта, такие как A1:E25 (Обратите внимание, что A1.. Синтаксис E25 не работает в Microsoft Access 97 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="dd2d6-151">You can type the name of a range in the spreadsheet or specify the range of cells to import or link, such as A1:E25 (note that the A1..E25 syntax does not work in Access 97 or later).</span></span> <span data-ttu-id="dd2d6-152">При импорте из или ссылки на Excel версий 5.0 или более поздних версий, можно перед именем диапазона имя листа и восклицательный знак; Например, бюджет! A1:C7.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-152">If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can prefix the range with the name of the worksheet and an exclamation point; for example, Budget!A1:C7.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="dd2d6-153">При экспорте в электронную таблицу, этот аргумент необходимо оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-153">When you export to a spreadsheet, you must leave this argument blank.</span></span> <span data-ttu-id="dd2d6-154">Если ввести диапазон, экспорт завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-154">If you enter a range, the export will fail.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dd2d6-155">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd2d6-155">Remarks</span></span>

<span data-ttu-id="dd2d6-156">Можно экспортировать данные в запросах доступа электронных таблиц.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-156">You can export the data in Access select queries to spreadsheets.</span></span> <span data-ttu-id="dd2d6-157">Microsoft Access экспортирует набор результатов запроса в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-157">Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="dd2d6-158">Данные электронной таблицы, добавляемые в существующую таблицу Access должны быть совместимы со структурой таблицы.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-158">Spreadsheet data that you append to an existing Access table must be compatible with the table's structure.</span></span>

  - <span data-ttu-id="dd2d6-159">Каждое поле в таблице должен быть типу данных, то соответствующее поле в таблице.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-159">Each field in the spreadsheet must be of the same data type as the corresponding field in the table.</span></span>

  - <span data-ttu-id="dd2d6-160">Поля должны быть в том же порядке (Если аргумент **Содержит имена полей** задано значение **Да**, в этом случае поле имена в электронной таблице должны совпадать имена полей в таблице).</span><span class="sxs-lookup"><span data-stu-id="dd2d6-160">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the spreadsheet must match the field names in the table).</span></span>

<span data-ttu-id="dd2d6-161">Это действие аналогично выбрав вкладку **Внешних данных** и и выбрав пункты **Excel** в **Импорт** или **Экспорт** группу или **несколько** в группе **Импорт** или **Экспорт** и щелкнув **Файл Lotus 1-2-3**.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-161">This action is similar to clicking the **External Data** tab and clicking **Excel** in the **Import** or **Export** group, or clicking **More** in the **Import** or **Export** group and clicking **Lotus 1-2-3 File**.</span></span> <span data-ttu-id="dd2d6-162">Эти команды можно использовать для выбора источника данных, например Access или тип базы данных, электронную таблицу или текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-162">You can use these commands to select a source of data, such as Access or a type of database, spreadsheet, or text file.</span></span> <span data-ttu-id="dd2d6-163">При выборе электронной таблице отображается ряд диалоговых окон или запускается мастер Microsoft Access, в котором выберите имя электронной таблицы и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-163">If you select a spreadsheet, a series of dialog boxes appear, or an Access wizard runs, in which you select the name of the spreadsheet and other options.</span></span> <span data-ttu-id="dd2d6-164">Аргументы действие **ImportExportSpreadsheet** соответствуют параметрам этих диалоговых окон или мастера.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-164">The arguments of the **ImportExportSpreadsheet** action reflect the options in these dialog boxes or in the wizards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dd2d6-165">Запроса и фильтрации связанной электронной таблице запроса или фильтра с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-165">If you query or filter a linked spreadsheet, the query or filter is case-sensitive.</span></span></P>



<span data-ttu-id="dd2d6-166">При связывании таблицы Excel, которая открыта в режиме редактирования Access будет ждать в электронной таблице Excel — режим редактирования перед завершением ссылок; нет тайм-аут.</span><span class="sxs-lookup"><span data-stu-id="dd2d6-166">If you link to an Excel spreadsheet that is open in Edit mode, Access will wait until the Excel spreadsheet is out of Edit mode before completing the link; there's no time-out.</span></span>

<span data-ttu-id="dd2d6-167">Чтобы выполнить действие **ImportExportSpreadsheet** в Visual Basic для приложений (VBA) модуль, используйте метод **ПреобразоватьЭлектроннуюТаблицу** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="dd2d6-167">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>

