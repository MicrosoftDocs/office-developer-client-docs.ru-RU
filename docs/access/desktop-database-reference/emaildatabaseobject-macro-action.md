---
title: Макрокоманда EMailDatabaseObject
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 15cb7d6c422a9d7b0fae17ab649b6cfbc1b497a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293569"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="caca6-102">Макрокоманда EMailDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="caca6-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="caca6-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="caca6-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="caca6-104">Вы можете использовать действие **EMailDatabaseObject,** чтобы включить указанную таблицу данных Microsoft Access, форму, отчет, модуль или страницу доступа к данным в электронном сообщении электронной почты, где его можно просмотреть и пересылать.</span><span class="sxs-lookup"><span data-stu-id="caca6-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="caca6-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="caca6-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="caca6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caca6-106">Settings</span></span>

<span data-ttu-id="caca6-107">Действие **EMailDatabaseObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="caca6-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caca6-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="caca6-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="caca6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="caca6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caca6-110"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-111">Тип объекта, включаемого в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caca6-111">The type of object to include in the mail message.</span></span> <span data-ttu-id="caca6-112">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report,</strong> <strong>Module</strong>, or Data <strong>Access Page</strong>, Server <strong>View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the Action <strong>Arguments</strong> section of the Macro Builder pane.</span><span class="sxs-lookup"><span data-stu-id="caca6-112">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="caca6-113">Вы не можете отправить макрос.</span><span class="sxs-lookup"><span data-stu-id="caca6-113">You can't send a macro.</span></span> <span data-ttu-id="caca6-114">Если вы хотите включить активный объект, выберите его тип с этим аргументом, но оставьте аргумент <strong>Object Name</strong> пустым.</span><span class="sxs-lookup"><span data-stu-id="caca6-114">If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caca6-115"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-116">Имя объекта, включаемого в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caca6-116">The name of the object to include in the mail message.</span></span> <span data-ttu-id="caca6-117">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="caca6-117">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="caca6-118">Если оставить аргументы <strong>Object Type</strong> и <strong>Object Name</strong> пустыми, Access отправляет сообщение почтовому приложению без объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="caca6-118">If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object.</span></span> <span data-ttu-id="caca6-119">При запуске макроса, содержащего действие <strong>EMailDatabaseObject</strong> в базе данных библиотеки, Access сначала ищет объект с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="caca6-119">If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caca6-120"><strong>Output Format</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-121">Тип формата, который требуется использовать для включенного объекта.</span><span class="sxs-lookup"><span data-stu-id="caca6-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="caca6-122">Список форматов, которые можно выбрать, будет изменяться в зависимости от выбранного аргумента <strong>типа</strong> объекта.</span><span class="sxs-lookup"><span data-stu-id="caca6-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="caca6-123">Доступные форматы могут включать книги <strong>Excel 97 – Excel 2003 (XLS),</strong>Двоичные книги <strong>Excel (XLSB)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, Rich <strong>Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="caca6-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="caca6-124">в поле <strong>"Формат выходных данных".</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="caca6-125">Модули можно отправить только в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="caca6-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="caca6-126">Страницы доступа к данным можно отправить только в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="caca6-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="caca6-127">Если оставить этот аргумент пустым, Access попросит вас определить выходной формат.</span><span class="sxs-lookup"><span data-stu-id="caca6-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caca6-128"><strong>Для</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-129">Получатели сообщения, имена которых вы хотите поместить в строку <strong>"Кому"</strong> в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caca6-129">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message.</span></span> <span data-ttu-id="caca6-130">Если оставить этот аргумент пустым, Access запросит имена получателей.</span><span class="sxs-lookup"><span data-stu-id="caca6-130">If you leave this argument blank, Access prompts you for the recipients' names.</span></span> <span data-ttu-id="caca6-131">Разделять имена получателей, задамые в <strong></strong> этом аргументе (а также в аргументах <strong>"Ск"</strong> и "СК"), с заданной четной точкаю (;) или со списком, установленным на вкладке <strong>"Номер"</strong> диалоговых окон "Свойства <strong>региональных</strong> параметров" панели управления Microsoft <strong>Windows.</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-131">Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>.</span></span> <span data-ttu-id="caca6-132">Если почтовому приложению не удалось определить имена получателей, сообщение не отправляется и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="caca6-132">If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caca6-133"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-134">Получатели сообщений, имена которых необходимо <strong></strong> поместить в строку "Копия" &quot; (копия) в &quot; сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caca6-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="caca6-135">Если оставить этот аргумент пустым, <strong>строка "Ск"</strong> в почтовом сообщении будет пустой.</span><span class="sxs-lookup"><span data-stu-id="caca6-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caca6-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-137">Получатели сообщений, имена которых нужно поместить в строку <strong>"СК"</strong> (жалюзийная &quot; &quot; копия) в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caca6-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="caca6-138">Если оставить этот аргумент пустым, <strong>строка</strong> "СК" в сообщении почты будет пустой.</span><span class="sxs-lookup"><span data-stu-id="caca6-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caca6-139"><strong>Тема</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-140">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="caca6-140">The subject of the message.</span></span> <span data-ttu-id="caca6-141">Этот текст отображается в <strong>строке темы</strong> в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caca6-141">This text appears on the <strong>Subject</strong> line in the mail message.</span></span> <span data-ttu-id="caca6-142">Если оставить этот аргумент пустым, <strong>строка темы</strong> в почтовом сообщении будет пустой.</span><span class="sxs-lookup"><span data-stu-id="caca6-142">If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caca6-143"><strong>Текст сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-144">Любой текст, который вы хотите включить в сообщение в дополнение к объекту базы данных.</span><span class="sxs-lookup"><span data-stu-id="caca6-144">Any text you want to include in the message in addition to the database object.</span></span> <span data-ttu-id="caca6-145">Этот текст отображается в основном тексте сообщения после объекта.</span><span class="sxs-lookup"><span data-stu-id="caca6-145">This text appears in the main body of the mail message, after the object.</span></span> <span data-ttu-id="caca6-146">Если оставить этот аргумент пустым, в сообщение электронной почты не будет включен дополнительный текст.</span><span class="sxs-lookup"><span data-stu-id="caca6-146">If you leave this argument blank, no additional text is included in the mail message.</span></span> <span data-ttu-id="caca6-147">Если оставить <strong>аргументы Object Type</strong> и <strong>Object Name</strong> пустыми, этот аргумент можно использовать для отправки сообщения электронной почты без объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="caca6-147">If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caca6-148"><strong>Изменение сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-149">Указывает, можно ли изменить сообщение перед его отправлением.</span><span class="sxs-lookup"><span data-stu-id="caca6-149">Specifies whether the message can be edited before it's sent.</span></span> <span data-ttu-id="caca6-150">Если выбрано <strong>"Да",</strong>приложение электронной почты запускается автоматически, и сообщение можно изменить.</span><span class="sxs-lookup"><span data-stu-id="caca6-150">If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited.</span></span> <span data-ttu-id="caca6-151">Если выбрано <strong>"Нет",</strong>сообщение отправляется без возможности редактирования сообщения пользователем.</span><span class="sxs-lookup"><span data-stu-id="caca6-151">If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message.</span></span> <span data-ttu-id="caca6-152">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-152">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caca6-153"><strong>Template File</strong></span><span class="sxs-lookup"><span data-stu-id="caca6-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="caca6-154">Путь и имя файла, который вы хотите использовать в качестве шаблона для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="caca6-154">The path and file name of a file you want to use as a template for an HTML file.</span></span> <span data-ttu-id="caca6-155">Файл шаблона — это файл, содержащий HTML-теги.</span><span class="sxs-lookup"><span data-stu-id="caca6-155">The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="caca6-156">Заметки</span><span class="sxs-lookup"><span data-stu-id="caca6-156">Remarks</span></span>

<span data-ttu-id="caca6-157">Объект в почтовом сообщении имеет выбранный формат выходных данных.</span><span class="sxs-lookup"><span data-stu-id="caca6-157">The object in the mail message is in the selected output format.</span></span> <span data-ttu-id="caca6-158">При двойном щелчке по объекту соответствующее программное обеспечение начинается с открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="caca6-158">When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="caca6-159">При использовании действия **EMailDatabaseObject** для включаем объекта базы данных в сообщение электронной почты применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="caca6-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="caca6-160">Можно отправлять таблицы, запросы и таблицы данных форм.</span><span class="sxs-lookup"><span data-stu-id="caca6-160">You can send table, query, and form datasheets.</span></span> <span data-ttu-id="caca6-161">В включенного объекта все поля в таблице выглядят так же, как в Access, за исключением полей, содержащих объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="caca6-161">In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects.</span></span> <span data-ttu-id="caca6-162">Столбцы для этих полей включены в объект, но поля пусты.</span><span class="sxs-lookup"><span data-stu-id="caca6-162">The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="caca6-163">Для управления, привязанного к полю "Да"/"Нет" (кнопка "Кнопка-кнопка", "Параметр" или "Check box"), в выходных файлах отображается значение –1 (Да) или 0 (Нет).</span><span class="sxs-lookup"><span data-stu-id="caca6-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="caca6-164">Для текстового поля, привязанного к полю гиперссылки, выходной файл отображает гиперссылку для всех форматов вывода, кроме текста MS-DOS (в этом случае гиперссылка отображается как обычный текст).</span><span class="sxs-lookup"><span data-stu-id="caca6-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="caca6-165">При отправке формы в представлении формы включенный объект всегда содержит представление таблицы формы.</span><span class="sxs-lookup"><span data-stu-id="caca6-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="caca6-166">При отправке отчета в объект включаются только текстовые поля и (в некоторых случаях) метки.</span><span class="sxs-lookup"><span data-stu-id="caca6-166">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels.</span></span> <span data-ttu-id="caca6-167">Все остальные элементы управления игнорируются.</span><span class="sxs-lookup"><span data-stu-id="caca6-167">All other controls are ignored.</span></span> <span data-ttu-id="caca6-168">Кроме того, не включаются сведения о том, как использовать его.</span><span class="sxs-lookup"><span data-stu-id="caca6-168">Header and footer information is also not included.</span></span> <span data-ttu-id="caca6-169">Единственным исключением является то, что при отправке отчета в формате Excel в объект включается текстовое поле в footer группы, содержащее выражение с функцией **Сумм.**</span><span class="sxs-lookup"><span data-stu-id="caca6-169">The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object.</span></span> <span data-ttu-id="caca6-170">Никакие другие средства управления в header или footer (и никакие агрегатные функции, кроме **Суммы)** не включены в объект.</span><span class="sxs-lookup"><span data-stu-id="caca6-170">No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="caca6-171">В объект включаются в субрепорты.</span><span class="sxs-lookup"><span data-stu-id="caca6-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="caca6-172">При отправке таблицы, формы или страницы доступа к данным в формате HTML создается один HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="caca6-172">When you send a datasheet, form, or data access page in HTML format, one .html file is created.</span></span> <span data-ttu-id="caca6-173">При отправке отчета в формате HTML создается один HTML-файл для каждой страницы в отчете.</span><span class="sxs-lookup"><span data-stu-id="caca6-173">When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="caca6-174">Чтобы запустить действие **EMailDatabaseObject** в модуле Visual Basic для приложений (VBA), используйте метод **SendObject** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="caca6-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="caca6-175">Об участнике</span><span class="sxs-lookup"><span data-stu-id="caca6-175">About the contributor</span></span>

<span data-ttu-id="caca6-176">**Ссылка, предоставленная** Брайан Chung [,FMS, Inc.,](https://www.fmsinc.com/)основатель и президент FMS, Inc., ведущий поставщик пользовательских решений для баз данных и средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="caca6-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="caca6-177">Функции и ограничения при использовании метода SendObject для отправки</span><span class="sxs-lookup"><span data-stu-id="caca6-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





