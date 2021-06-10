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
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="a8391-102">Макрокоманда EMailDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a8391-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="a8391-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8391-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="a8391-104">Вы можете использовать действие **EMailDatabaseObject,** чтобы включить указанную таблицу данных Microsoft Access, форму, отчет, модуль или страницу доступа к данным в электронном почтовом сообщении, где его можно просматривать и пересылать.</span><span class="sxs-lookup"><span data-stu-id="a8391-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="a8391-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="a8391-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="a8391-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8391-106">Settings</span></span>

<span data-ttu-id="a8391-107">Действие **EMailDatabaseObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a8391-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8391-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a8391-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a8391-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a8391-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8391-110"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-111">Тип объекта, который необходимо включить в почтовое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8391-111">The type of object to include in the mail message.</span></span> <span data-ttu-id="a8391-112">Щелкните Таблица <strong>(для</strong> таблицы <strong>данных),</strong> Запрос (для таблицы данных запроса), Форма (для таблицы данных формы или формы), Отчет, <strong>Модуль</strong> <strong></strong> или Страница <strong></strong> доступа к <strong></strong> <strong>данным,</strong>Просмотр <strong>сервера,</strong>сохраненные процедуры или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="a8391-112">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a8391-113">Вы не можете отправить макрос.</span><span class="sxs-lookup"><span data-stu-id="a8391-113">You can't send a macro.</span></span> <span data-ttu-id="a8391-114">Если вы хотите включить активный объект, выберите его тип с помощью этого аргумента, но оставьте аргумент <strong>Object Name</strong> пустым.</span><span class="sxs-lookup"><span data-stu-id="a8391-114">If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8391-115"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-116">Имя объекта, включаемого в почтовое сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8391-116">The name of the object to include in the mail message.</span></span> <span data-ttu-id="a8391-117">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8391-117">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="a8391-118">Если аргументы <strong>типа</strong> объекта <strong></strong> и имени объектов будут пустыми, Access отправляет сообщение в почтовое приложение без объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="a8391-118">If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object.</span></span> <span data-ttu-id="a8391-119">Если вы запустите макрос, содержащий действие <strong>EMailDatabaseObject</strong> в базе данных библиотеки, Access сначала ищет объект с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a8391-119">If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8391-120"><strong>Output Format</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-121">Тип формата, который требуется использовать для включенного объекта.</span><span class="sxs-lookup"><span data-stu-id="a8391-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="a8391-122">Список форматов, которые можно выбрать, будет изменяться в зависимости от выбранного аргумента <strong>типа</strong> объекта.</span><span class="sxs-lookup"><span data-stu-id="a8391-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="a8391-123">Доступные форматы могут включать <strong>книги Excel 97 — Excel 2003 (*.xls),</strong>Excel Двоичные книги <strong>(*.xlsb),</strong> <strong>Excel Книги (*.xlsx),</strong> <strong>HTML (*.htm, *.html)</strong> <strong>, Microsoft Excel 5.0/95 Книги (*.xls),</strong> <strong>ФОРМАТ PDF,</strong>богатый текстовый <strong>фомат (*.rtf),</strong>текстовые файлы <strong>(*.txt)</strong>или <strong>ФОРМАТ XPS (\*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8391-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="a8391-124">в поле <strong>Формат вывода.</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="a8391-125">Модули можно отправить только в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="a8391-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="a8391-126">Страницы доступа к данным можно отправить только в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="a8391-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="a8391-127">Если оставить этот аргумент пустым, Access попросит вас определить выходной формат.</span><span class="sxs-lookup"><span data-stu-id="a8391-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8391-128"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-129">Получатели сообщения, имена которых необходимо поместить в строку <strong>To</strong> в почтовом сообщении.</span><span class="sxs-lookup"><span data-stu-id="a8391-129">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message.</span></span> <span data-ttu-id="a8391-130">Если оставить этот аргумент пустым, Access подсказывит вам имена получателей.</span><span class="sxs-lookup"><span data-stu-id="a8391-130">If you leave this argument blank, Access prompts you for the recipients' names.</span></span> <span data-ttu-id="a8391-131">Разделять имена получателей, которые указаны в этом аргументе (и в аргументах <strong>Cc</strong> и <strong>Bcc)</strong> с полуколоном (;) или с набором сепаратора списков на вкладке <strong>Номер</strong> диалоговой Параметры <strong>Properties</strong> в панели управления Microsoft <strong>Windows.</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-131">Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>.</span></span> <span data-ttu-id="a8391-132">Если почтовое приложение не может идентифицировать имена получателей, сообщение не отправляется и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a8391-132">If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8391-133"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-134">Получатели сообщений, имена которых необходимо поместить в строку <strong>Cc</strong> &quot; (копия &quot; углерода) в почтовом сообщении.</span><span class="sxs-lookup"><span data-stu-id="a8391-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="a8391-135">Если оставить этот аргумент пустым, строка <strong>Cc</strong> в почтовом сообщении пуста.</span><span class="sxs-lookup"><span data-stu-id="a8391-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8391-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-137">Получатели сообщений, имена которых необходимо поместить на строку <strong>Bcc</strong> &quot; (слепая копия &quot; углерода) в почтовом сообщении.</span><span class="sxs-lookup"><span data-stu-id="a8391-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="a8391-138">Если оставить этот аргумент пустым, <strong>строка Bcc</strong> в почтовом сообщении пуста.</span><span class="sxs-lookup"><span data-stu-id="a8391-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8391-139"><strong>Тема</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-140">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8391-140">The subject of the message.</span></span> <span data-ttu-id="a8391-141">Этот текст отображается в <strong>строке Subject</strong> в почтовом сообщении.</span><span class="sxs-lookup"><span data-stu-id="a8391-141">This text appears on the <strong>Subject</strong> line in the mail message.</span></span> <span data-ttu-id="a8391-142">Если оставить этот аргумент пустым, строка <strong>Subject</strong> в почтовом сообщении пуста.</span><span class="sxs-lookup"><span data-stu-id="a8391-142">If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8391-143"><strong>Текст сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-144">Любой текст, который необходимо включить в сообщение в дополнение к объекту базы данных.</span><span class="sxs-lookup"><span data-stu-id="a8391-144">Any text you want to include in the message in addition to the database object.</span></span> <span data-ttu-id="a8391-145">Этот текст отображается в основном тексте почтового сообщения после объекта.</span><span class="sxs-lookup"><span data-stu-id="a8391-145">This text appears in the main body of the mail message, after the object.</span></span> <span data-ttu-id="a8391-146">Если оставить этот аргумент пустым, в почтовое сообщение не будет включен дополнительный текст.</span><span class="sxs-lookup"><span data-stu-id="a8391-146">If you leave this argument blank, no additional text is included in the mail message.</span></span> <span data-ttu-id="a8391-147">Если аргументы <strong>типа</strong> <strong></strong> объекта и имени объектов пусты, этот аргумент можно использовать для отправки сообщения почты без объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="a8391-147">If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8391-148"><strong>Изменение сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-149">Указывает, можно ли изменить сообщение перед его отправлением.</span><span class="sxs-lookup"><span data-stu-id="a8391-149">Specifies whether the message can be edited before it's sent.</span></span> <span data-ttu-id="a8391-150">Если вы выберите <strong>Да,</strong>приложение электронной почты запускается автоматически, и сообщение может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="a8391-150">If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited.</span></span> <span data-ttu-id="a8391-151">Если <strong>выбрано нет,</strong>сообщение отправляется без возможности пользователя изменить сообщение.</span><span class="sxs-lookup"><span data-stu-id="a8391-151">If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message.</span></span> <span data-ttu-id="a8391-152">По умолчанию — <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-152">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8391-153"><strong>Template File</strong></span><span class="sxs-lookup"><span data-stu-id="a8391-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="a8391-154">Путь и имя файла файла, который необходимо использовать в качестве шаблона для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="a8391-154">The path and file name of a file you want to use as a template for an HTML file.</span></span> <span data-ttu-id="a8391-155">Файл шаблона — это файл, содержащий HTML-теги.</span><span class="sxs-lookup"><span data-stu-id="a8391-155">The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a8391-156">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8391-156">Remarks</span></span>

<span data-ttu-id="a8391-157">Объект в почтовом сообщении находится в выбранном формате вывода.</span><span class="sxs-lookup"><span data-stu-id="a8391-157">The object in the mail message is in the selected output format.</span></span> <span data-ttu-id="a8391-158">При дважды нажатии на объект соответствующее программное обеспечение начинается с открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a8391-158">When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="a8391-159">При использовании действия **EMailDatabaseObject** для включательного объекта базы данных в почтовое сообщение применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="a8391-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="a8391-160">Можно отправлять таблицы, запросы и таблицы данных форм.</span><span class="sxs-lookup"><span data-stu-id="a8391-160">You can send table, query, and form datasheets.</span></span> <span data-ttu-id="a8391-161">В включеном объекте все поля в таблице данных выглядят так же, как и в Access, за исключением полей, содержащих объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="a8391-161">In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects.</span></span> <span data-ttu-id="a8391-162">Столбцы для этих полей включены в объект, но поля пустые.</span><span class="sxs-lookup"><span data-stu-id="a8391-162">The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="a8391-163">Для управления, связанного с полем Yes/No (кнопка toggle, кнопка параметра или контрольное окно), в файле вывода отображается значение :1 (Да) или 0 (Нет).</span><span class="sxs-lookup"><span data-stu-id="a8391-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="a8391-164">Для текстового поля, связанного с полем гиперссылки, в выходном файле отображается гиперссылка для всех форматов выходных данных, за исключением текста MS-DOS (в этом случае гиперссылка отображается как обычный текст).</span><span class="sxs-lookup"><span data-stu-id="a8391-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="a8391-165">Если вы отправляете форму в представлении Form, включенный объект всегда содержит представление таблицы данных формы.</span><span class="sxs-lookup"><span data-stu-id="a8391-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="a8391-166">При отправке отчета единственными средствами управления, включенными в объект, являются текстовые поля и (в некоторых случаях) метки.</span><span class="sxs-lookup"><span data-stu-id="a8391-166">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels.</span></span> <span data-ttu-id="a8391-167">Все остальные элементы управления игнорируются.</span><span class="sxs-lookup"><span data-stu-id="a8391-167">All other controls are ignored.</span></span> <span data-ttu-id="a8391-168">Сведения о загонах и подножке также не включаются.</span><span class="sxs-lookup"><span data-stu-id="a8391-168">Header and footer information is also not included.</span></span> <span data-ttu-id="a8391-169">Единственным исключением является то, что при отправке отчета в Excel формате в объект включается текстовое поле в подножке группы, содержащее выражение с функцией **Sum.**</span><span class="sxs-lookup"><span data-stu-id="a8391-169">The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object.</span></span> <span data-ttu-id="a8391-170">Никакой другой контроль в загоне или подножке (а также не совокупная функция, кроме **Sum)** не включается в объект.</span><span class="sxs-lookup"><span data-stu-id="a8391-170">No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="a8391-171">В объект включены подэкспорты.</span><span class="sxs-lookup"><span data-stu-id="a8391-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="a8391-172">При отправке таблицы данных, формы или страницы доступа к данным в формате HTML создается один .html файл.</span><span class="sxs-lookup"><span data-stu-id="a8391-172">When you send a datasheet, form, or data access page in HTML format, one .html file is created.</span></span> <span data-ttu-id="a8391-173">При отправке отчета в формате HTML создается один .html для каждой страницы отчета.</span><span class="sxs-lookup"><span data-stu-id="a8391-173">When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="a8391-174">Чтобы выполнить **действие EMailDatabaseObject** в модуле Visual Basic для приложений (VBA), используйте метод **SendObject** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="a8391-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="a8391-175">Об участнике</span><span class="sxs-lookup"><span data-stu-id="a8391-175">About the contributor</span></span>

<span data-ttu-id="a8391-176">**Ссылка, предоставленная** Luke Chung, [FMS, Inc.,](https://www.fmsinc.com/)основатель и президент FMS, Inc., ведущего поставщика пользовательских решений базы данных и средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="a8391-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="a8391-177">Возможности и ограничения использования метода SendObject для отправки</span><span class="sxs-lookup"><span data-stu-id="a8391-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





