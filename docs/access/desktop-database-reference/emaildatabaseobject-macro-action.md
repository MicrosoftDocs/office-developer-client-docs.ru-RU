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
ms.openlocfilehash: f0c0ba73274d6f27a9e2a857aea1061416168f3a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922918"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="79885-102">Макрокоманда EMailDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="79885-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="79885-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="79885-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="79885-104">Действие **EMailDatabaseObject** можно использовать для включения указанного Microsoft Access таблицы, формы, отчета, модуль или данные доступа к странице в сообщение электронной почты, где его можно просматривать и пересылку.</span><span class="sxs-lookup"><span data-stu-id="79885-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="79885-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="79885-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="settings"></a><span data-ttu-id="79885-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79885-107">Settings</span></span>

<span data-ttu-id="79885-108">Действие **EMailDatabaseObject** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="79885-108">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79885-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="79885-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="79885-110">Описание</span><span class="sxs-lookup"><span data-stu-id="79885-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79885-111"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="79885-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-112">Тип объекта для включения в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-112">The type of object to include in the mail message.</span></span> <span data-ttu-id="79885-113">Нажмите кнопку <strong>таблицы</strong> (таблицы), <strong>запрос</strong> (для таблицы запросов), <strong>формы</strong> (для формы или формы таблицы), <strong>отчета</strong>, <strong>модуль</strong>или <strong>Страницы доступа к данным</strong>, <strong>Представление</strong>, <strong>Хранимые процедуры</strong>или <strong> Функция</strong> в поле <strong>Тип объекта</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="79885-113">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="79885-114">Не удается отправить макроса.</span><span class="sxs-lookup"><span data-stu-id="79885-114">You can't send a macro.</span></span> <span data-ttu-id="79885-115">Если вы хотите включить активного объекта, выберите его тип, но оставить пустым аргумента <strong>Имя объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="79885-115">If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79885-116"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="79885-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-117">Имя объекта, чтобы включить в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-117">The name of the object to include in the mail message.</span></span> <span data-ttu-id="79885-118">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="79885-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="79885-119">Если оставить <strong>Тип</strong> и <strong>Имя объекта</strong> аргументов, Access отправляет сообщение в не все объекты базы данных.</span><span class="sxs-lookup"><span data-stu-id="79885-119">If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object.</span></span> <span data-ttu-id="79885-120">Если макрос, содержащий действие <strong>EMailDatabaseObject</strong> в базе данных библиотеки, поиск объекта с указанным именем сначала в библиотеке базы данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="79885-120">If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79885-121"><strong>Формат выходных данных</strong></span><span class="sxs-lookup"><span data-stu-id="79885-121"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-122">Тип формата, в котором следует отправляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="79885-122">The type of format you want used for the included object.</span></span> <span data-ttu-id="79885-123">Список форматов, которые можно выбрать один из меняется в зависимости от того, установите для аргумента <strong>Тип объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="79885-123">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="79885-124">Форматы могут включать <strong>Excel 97 - 2003 книги Excel (*.xls)</strong>, <strong>Двоичная книга Excel (*.xlsb)</strong>, <strong>Книга Excel (XLSX)</strong> <strong>HTML (*.htm, \* .html)</strong>, <strong>Книга Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Формат PDF </strong>, <strong>Fomat текст в формате RTF (*.rtf)</strong>, <strong>текстовые файлы (*.txt)</strong>или <strong>формате XPS (\*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="79885-124">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="79885-125">в поле <strong>Формат выходных данных</strong> .</span><span class="sxs-lookup"><span data-stu-id="79885-125">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="79885-126">Модули передаются только в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="79885-126">Modules can be sent only in text format.</span></span> <span data-ttu-id="79885-127">Страницы доступа к данным могут отправляться только в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="79885-127">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="79885-128">Если оставить это аргумент, Access запрашивает выходной формат.</span><span class="sxs-lookup"><span data-stu-id="79885-128">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79885-129"><strong>Задача</strong></span><span class="sxs-lookup"><span data-stu-id="79885-129"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-130">Получатели сообщения, имена которых требуется включить в строке <strong>Кому</strong> сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-130">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message.</span></span> <span data-ttu-id="79885-131">Если оставить это аргумент, Access запрашивает имен получателей.</span><span class="sxs-lookup"><span data-stu-id="79885-131">If you leave this argument blank, Access prompts you for the recipients' names.</span></span> <span data-ttu-id="79885-132">Разделите получателей указываемые имена этот аргумент (и аргументы <strong>«копия»</strong> и <strong>«СК»</strong> ) точкой с запятой (;) или с разделителями списков на вкладке <strong>число</strong> диалогового окна <strong>Свойства региональных параметров</strong> в Microsoft <strong>Панель управления</strong>Windows.</span><span class="sxs-lookup"><span data-stu-id="79885-132">Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>.</span></span> <span data-ttu-id="79885-133">Если почтовое приложение не может определить имена получателей, сообщение не отправляется и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="79885-133">If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79885-134"><strong>«Копия»</strong></span><span class="sxs-lookup"><span data-stu-id="79885-134"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-135">Получатели сообщения, имена которых следует разместить на <strong>«копия»</strong> (&quot;копии&quot;) строки в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-135">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="79885-136">Если оставить это аргумент, в строке <strong>копия</strong> сообщения электронной почты не задан.</span><span class="sxs-lookup"><span data-stu-id="79885-136">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79885-137"><strong>Скрытой копии</strong></span><span class="sxs-lookup"><span data-stu-id="79885-137"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-138">Получатели сообщения, имена которых следует разместить на <strong>скрытой копии</strong> (&quot;скрытой копии&quot;) строки в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-138">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="79885-139">Если оставить это аргумент, строки <strong>Скрытая копия</strong> сообщения электронной почты не задан.</span><span class="sxs-lookup"><span data-stu-id="79885-139">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79885-140"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="79885-140"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-141">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="79885-141">The subject of the message.</span></span> <span data-ttu-id="79885-142">Этот текст отображается в строке <strong>темы</strong> сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-142">This text appears on the <strong>Subject</strong> line in the mail message.</span></span> <span data-ttu-id="79885-143">Если этот аргумент оставлен пустым, строка <strong>темы</strong> сообщения электронной почты не задан.</span><span class="sxs-lookup"><span data-stu-id="79885-143">If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79885-144"><strong>Текст сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="79885-144"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-145">Текст, который вы хотите включить в сообщение помимо объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="79885-145">Any text you want to include in the message in addition to the database object.</span></span> <span data-ttu-id="79885-146">Этот текст отображается в основном тексте сообщения электронной почты после объекта.</span><span class="sxs-lookup"><span data-stu-id="79885-146">This text appears in the main body of the mail message, after the object.</span></span> <span data-ttu-id="79885-147">Если оставить это аргумент, никакой текст включается в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="79885-147">If you leave this argument blank, no additional text is included in the mail message.</span></span> <span data-ttu-id="79885-148">Если оставить <strong>Тип</strong> и <strong>Имя объекта</strong> аргументов, чтобы отправить сообщение электронной почты без объекта базы данных можно использовать этот аргумент.</span><span class="sxs-lookup"><span data-stu-id="79885-148">If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79885-149"><strong>Изменение сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="79885-149"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-150">Указывает, можно ли изменить перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="79885-150">Specifies whether the message can be edited before it's sent.</span></span> <span data-ttu-id="79885-151">Если выбран вариант <strong>Да</strong>, автоматически запускается приложение электронной почты и сообщения можно изменить.</span><span class="sxs-lookup"><span data-stu-id="79885-151">If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited.</span></span> <span data-ttu-id="79885-152">Если выбран вариант <strong>Нет</strong>, сообщение отправляется без участия пользователя возможность изменять сообщение.</span><span class="sxs-lookup"><span data-stu-id="79885-152">If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message.</span></span> <span data-ttu-id="79885-153">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="79885-153">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79885-154"><strong>Файл шаблона</strong></span><span class="sxs-lookup"><span data-stu-id="79885-154"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="79885-155">Путь и имя файла, который будет использоваться как шаблон для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="79885-155">The path and file name of a file you want to use as a template for an HTML file.</span></span> <span data-ttu-id="79885-156">Файл шаблона представляет собой файл, содержащий теги HTML.</span><span class="sxs-lookup"><span data-stu-id="79885-156">The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="79885-157">Примечания</span><span class="sxs-lookup"><span data-stu-id="79885-157">Remarks</span></span>

<span data-ttu-id="79885-158">— Это объект в сообщение электронной почты в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="79885-158">The object in the mail message is in the selected output format.</span></span> <span data-ttu-id="79885-159">Дважды щелкните объект, соответствующее программное обеспечение начинается с объектом открыт.</span><span class="sxs-lookup"><span data-stu-id="79885-159">When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="79885-160">При использовании **EMailDatabaseObject** действия для включения объекта базы данных в сообщение электронной почты, применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="79885-160">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="79885-161">Можно отправить в таблице, запросов и формы в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="79885-161">You can send table, query, and form datasheets.</span></span> <span data-ttu-id="79885-162">В объекте включены все поля в таблице выглядеть, как это делается в Access, за исключением полей, содержащих объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="79885-162">In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects.</span></span> <span data-ttu-id="79885-163">Столбцы для этих полей, которые включаются в объекте, но полей являются пустыми.</span><span class="sxs-lookup"><span data-stu-id="79885-163">The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="79885-164">Элементов управления, связанных с полями Да/Нет (выключатель, переключатель или флажок), файл выходных данных отображает значение -1 (Да), либо 0 (нет).</span><span class="sxs-lookup"><span data-stu-id="79885-164">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="79885-165">Для текстового поля, привязанного к полю гиперссылки, файл выходных данных отображаются гиперссылки для всех выходных форматов, кроме текста MS-DOS (в этом случае гиперссылку просто отображается как обычный текст).</span><span class="sxs-lookup"><span data-stu-id="79885-165">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="79885-166">При отправке формы в режиме формы, включенный объект всегда содержит представления таблицы данных формы.</span><span class="sxs-lookup"><span data-stu-id="79885-166">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="79885-167">При отправке отчета, единственными элементами управления, которые включены в объекте, текстовые поля и (в некоторых случаях) метки.</span><span class="sxs-lookup"><span data-stu-id="79885-167">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels.</span></span> <span data-ttu-id="79885-168">Все другие элементы управления игнорируются.</span><span class="sxs-lookup"><span data-stu-id="79885-168">All other controls are ignored.</span></span> <span data-ttu-id="79885-169">Сведения о верхний и нижний колонтитулы не также включены.</span><span class="sxs-lookup"><span data-stu-id="79885-169">Header and footer information is also not included.</span></span> <span data-ttu-id="79885-170">Единственное исключение — при отправке отчета в формате Excel, текстовое поле в нижнем колонтитуле группы, содержащий выражение, с помощью функции **Sum** Включение в объекте.</span><span class="sxs-lookup"><span data-stu-id="79885-170">The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object.</span></span> <span data-ttu-id="79885-171">Никакие другие элементы управления в заголовок или нижний колонтитул (и статистические функции, отличный от **сумм**) включается в объекте.</span><span class="sxs-lookup"><span data-stu-id="79885-171">No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="79885-172">Подчиненные отчеты включаются в объекте.</span><span class="sxs-lookup"><span data-stu-id="79885-172">Subreports are included in the object.</span></span>

- <span data-ttu-id="79885-173">При отправке таблицы, формы или страницы доступа к данным в формате HTML создается один HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="79885-173">When you send a datasheet, form, or data access page in HTML format, one .html file is created.</span></span> <span data-ttu-id="79885-174">При отправке отчета в формате HTML, один HTML-файла, создается для каждой страницы в отчете.</span><span class="sxs-lookup"><span data-stu-id="79885-174">When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="79885-175">Чтобы выполнить действие **EMailDatabaseObject** в Visual Basic для приложений (VBA) модуль, используйте метод **ОтправитьОбъект** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="79885-175">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="79885-176">О участник</span><span class="sxs-lookup"><span data-stu-id="79885-176">About the contributor</span></span>

<span data-ttu-id="79885-177">**Автор ссылок** Люк Чанг, [FMS, Inc.](https://www.fmsinc.com/), основатель и президент компании FMS, Inc., ведущего поставщика решений настраиваемых баз данных и средств разработки.</span><span class="sxs-lookup"><span data-stu-id="79885-177">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

  - [<span data-ttu-id="79885-178">Возможности и ограничения для использования метода ОтправитьОбъект для отправки</span><span class="sxs-lookup"><span data-stu-id="79885-178">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





