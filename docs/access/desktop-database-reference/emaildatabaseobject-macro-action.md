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
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="d97bc-102">Макрокоманда EMailDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d97bc-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="d97bc-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d97bc-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="d97bc-104">Действие **емаилдатабасеобжект** можно использовать для включения указанной таблицы, формы, отчета, модуля или страницы доступа к данным Microsoft Access в электронном письме, где их можно просматривать и пересылать.</span><span class="sxs-lookup"><span data-stu-id="d97bc-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="d97bc-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="d97bc-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="d97bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d97bc-106">Settings</span></span>

<span data-ttu-id="d97bc-107">Макрокоманда **емаилдатабасеобжект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="d97bc-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d97bc-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="d97bc-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d97bc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d97bc-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d97bc-110"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-111">Тип объекта, включаемого в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-111">The type of object to include in the mail message.</span></span> <span data-ttu-id="d97bc-112">Щелкните <strong>Таблица</strong> (для таблицы таблица), <strong>Query</strong> (для таблицы в запросе), <strong>форма</strong> (для формы или формы в режиме таблицы), <strong>отчет</strong>, <strong>модуль</strong>или <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>хранимые процедуры</strong>или <strong>функция</strong> в поле <strong>тип объекта</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="d97bc-112">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d97bc-113">Невозможно отправить макрос.</span><span class="sxs-lookup"><span data-stu-id="d97bc-113">You can't send a macro.</span></span> <span data-ttu-id="d97bc-114">Если вы хотите включить активный объект, выберите его тип с этим аргументом, но оставьте значение аргумента <strong>имя объекта</strong> пустым.</span><span class="sxs-lookup"><span data-stu-id="d97bc-114">If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d97bc-115"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-116">Имя объекта, включаемого в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-116">The name of the object to include in the mail message.</span></span> <span data-ttu-id="d97bc-117">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="d97bc-117">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="d97bc-118">Если вы оставляете аргументы " <strong>тип объекта</strong> " и " <strong>имя объекта</strong> " пустыми, Access отправляет сообщение в почтовое приложение без какого бы то ни было объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="d97bc-118">If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object.</span></span> <span data-ttu-id="d97bc-119">При запуске макроса, содержащего действие <strong>емаилдатабасеобжект</strong> , в библиотечной базе данных Access сначала ищет объект с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="d97bc-119">If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d97bc-120"><strong>Output Format</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-121">Тип формата, который будет использоваться для включенного объекта.</span><span class="sxs-lookup"><span data-stu-id="d97bc-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="d97bc-122">Список форматов, из которого можно выбирать элементы, будет изменяться в зависимости от того, что выбрано для аргумента <strong>тип объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="d97bc-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="d97bc-123">Доступные форматы могут включать <strong>книгу excel 97-Excel 2003 (*. xls)</strong>, <strong>Двоичная книга Excel (*. xlsb)</strong>, <strong>Книга Excel (*. xlsx)</strong>, <strong>HTML (*. htm, *. HTML)</strong>, <strong>книга Microsoft Excel 5.0/95 (*. xls)</strong>, <strong>Формат PDF</strong>, <strong>форматированный текст фомат (*. RTF)</strong>, <strong>текстовые файлы (*. txt</strong>) или <strong>Формат XPS (\*. XPS)</strong>.</span><span class="sxs-lookup"><span data-stu-id="d97bc-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="d97bc-124">в поле <strong>Формат вывода</strong> .</span><span class="sxs-lookup"><span data-stu-id="d97bc-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="d97bc-125">Модули можно отправлять только в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="d97bc-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="d97bc-126">Страницы доступа к данным можно отправлять только в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="d97bc-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="d97bc-127">Если оставить этот аргумент пустым, Access попросит вас определить выходной формат.</span><span class="sxs-lookup"><span data-stu-id="d97bc-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d97bc-128"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-129">Получатели сообщения, чьи имена вы хотите поместить в строку " <strong>Кому</strong> " в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-129">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message.</span></span> <span data-ttu-id="d97bc-130">Если оставить этот аргумент пустым, Access предложит ввести имена получателей.</span><span class="sxs-lookup"><span data-stu-id="d97bc-130">If you leave this argument blank, Access prompts you for the recipients' names.</span></span> <span data-ttu-id="d97bc-131">Разделяйте имена получателей, указанные в этом аргументе (а в аргументах <strong>"копия"</strong> и <strong>"СК</strong> "), точкой с запятой (;) или с помощью разделителя списков, установленного на вкладке <strong>число</strong> диалогового окна <strong>Свойства: региональные параметры</strong> на <strong>панели управления</strong>Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d97bc-131">Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>.</span></span> <span data-ttu-id="d97bc-132">Если почтовое приложение не может определить имена получателей, сообщение не отправляется и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d97bc-132">If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d97bc-133"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-134">Получатели сообщения, чьи имена вы хотите поместить в строку <strong>CC</strong> (&quot;копия&quot;) сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="d97bc-135">Если оставить этот аргумент пустым, строка <strong>"копия"</strong> в почтовом сообщении будет пустой.</span><span class="sxs-lookup"><span data-stu-id="d97bc-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d97bc-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-137">Получатели сообщения, чьи имена необходимо поместить в строку <strong>"СК"</strong> (&quot;Скрытая копия&quot;) в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="d97bc-138">Если оставить этот аргумент пустым, строка <strong>скрытой копии</strong> в почтовом сообщении будет пустой.</span><span class="sxs-lookup"><span data-stu-id="d97bc-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d97bc-139"><strong>Тема</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-140">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="d97bc-140">The subject of the message.</span></span> <span data-ttu-id="d97bc-141">Этот текст отображается в строке <strong>темы</strong> сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-141">This text appears on the <strong>Subject</strong> line in the mail message.</span></span> <span data-ttu-id="d97bc-142">Если оставить этот аргумент пустым, строка <strong>темы</strong> в почтовом сообщении будет пустой.</span><span class="sxs-lookup"><span data-stu-id="d97bc-142">If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d97bc-143"><strong>Текст сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-144">Текст, который необходимо включить в сообщение, кроме объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="d97bc-144">Any text you want to include in the message in addition to the database object.</span></span> <span data-ttu-id="d97bc-145">Этот текст отображается в основном тексте почтового сообщения после объекта.</span><span class="sxs-lookup"><span data-stu-id="d97bc-145">This text appears in the main body of the mail message, after the object.</span></span> <span data-ttu-id="d97bc-146">Если оставить этот аргумент пустым, в сообщение электронной почты не будет добавлен никакой дополнительный текст.</span><span class="sxs-lookup"><span data-stu-id="d97bc-146">If you leave this argument blank, no additional text is included in the mail message.</span></span> <span data-ttu-id="d97bc-147">Если оставить аргументы " <strong>тип объекта</strong> " и " <strong>имя объекта</strong> " пустыми, можно использовать этот аргумент для отправки почтового сообщения без объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="d97bc-147">If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d97bc-148"><strong>Изменение сообщения</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-149">Указывает, можно ли изменять сообщение перед его отправкой.</span><span class="sxs-lookup"><span data-stu-id="d97bc-149">Specifies whether the message can be edited before it's sent.</span></span> <span data-ttu-id="d97bc-150">Если выбрано <strong>значение Да</strong>, приложение электронной почты запускается автоматически, и сообщение может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="d97bc-150">If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited.</span></span> <span data-ttu-id="d97bc-151">Если выбрано значение <strong>нет</strong>, сообщение отправляется без возможности изменения сообщения пользователем.</span><span class="sxs-lookup"><span data-stu-id="d97bc-151">If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message.</span></span> <span data-ttu-id="d97bc-152">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="d97bc-152">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d97bc-153"><strong>Template File</strong></span><span class="sxs-lookup"><span data-stu-id="d97bc-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="d97bc-154">Путь и имя файла, который вы хотите использовать в качестве шаблона для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="d97bc-154">The path and file name of a file you want to use as a template for an HTML file.</span></span> <span data-ttu-id="d97bc-155">Файл шаблона — это файл, содержащий HTML-теги.</span><span class="sxs-lookup"><span data-stu-id="d97bc-155">The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d97bc-156">Примечания</span><span class="sxs-lookup"><span data-stu-id="d97bc-156">Remarks</span></span>

<span data-ttu-id="d97bc-157">Объект в сообщении электронной почты находится в выбранном выходном формате.</span><span class="sxs-lookup"><span data-stu-id="d97bc-157">The object in the mail message is in the selected output format.</span></span> <span data-ttu-id="d97bc-158">Если дважды щелкнуть объект, соответствующее программное обеспечение начинается с открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="d97bc-158">When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="d97bc-159">При использовании действия **емаилдатабасеобжект** для включения объекта базы данных в сообщение электронной почты применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="d97bc-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="d97bc-160">Таблицы, запросы и формы можно отправлять в таблицы, запросы и формы.</span><span class="sxs-lookup"><span data-stu-id="d97bc-160">You can send table, query, and form datasheets.</span></span> <span data-ttu-id="d97bc-161">В включенном объекте все поля в таблице выглядят так же, как и в Access, за исключением полей, содержащих объекты OLE.</span><span class="sxs-lookup"><span data-stu-id="d97bc-161">In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects.</span></span> <span data-ttu-id="d97bc-162">Столбцы для этих полей включены в объект, но поля пусты.</span><span class="sxs-lookup"><span data-stu-id="d97bc-162">The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="d97bc-163">Для элемента управления, привязанного к полю "да/нет" (выключатель, переключатель или флажок), выходной файл отображает значение – 1 (да) или 0 (нет).</span><span class="sxs-lookup"><span data-stu-id="d97bc-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="d97bc-164">Для текстового поля, привязанного к полю гиперссылки, в выходном файле отображается гиперссылка для всех форматов вывода, кроме текста MS-DOS (в данном случае гиперссылка просто отображается как обычный текст).</span><span class="sxs-lookup"><span data-stu-id="d97bc-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="d97bc-165">При отправке формы в режиме формы включенный объект всегда содержит представление таблицы данных формы.</span><span class="sxs-lookup"><span data-stu-id="d97bc-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="d97bc-166">Если вы отправляете отчет, единственными элементами управления, включенными в объект, являются текстовые поля и (в некоторых случаях) Метки.</span><span class="sxs-lookup"><span data-stu-id="d97bc-166">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels.</span></span> <span data-ttu-id="d97bc-167">Все остальные элементы управления игнорируются.</span><span class="sxs-lookup"><span data-stu-id="d97bc-167">All other controls are ignored.</span></span> <span data-ttu-id="d97bc-168">Сведения о верхнем и нижнем колонтитулах также не включаются.</span><span class="sxs-lookup"><span data-stu-id="d97bc-168">Header and footer information is also not included.</span></span> <span data-ttu-id="d97bc-169">Единственное исключение из этого параметра заключается в том, что при отправке отчета в формате Excel текстовое поле в нижнем колонтитуле группы, содержащее выражение с функцией **Sum** , включается в объект.</span><span class="sxs-lookup"><span data-stu-id="d97bc-169">The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object.</span></span> <span data-ttu-id="d97bc-170">В этом объекте нет другого элемента управления в верхнем или нижнем колонтитуле (а Статистическая функция, отличная от **Sum**), не включается в объект.</span><span class="sxs-lookup"><span data-stu-id="d97bc-170">No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="d97bc-171">Вложенные отчеты включаются в объект.</span><span class="sxs-lookup"><span data-stu-id="d97bc-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="d97bc-172">При отправке таблицы, формы или страницы доступа к данным в формате HTML создается один HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="d97bc-172">When you send a datasheet, form, or data access page in HTML format, one .html file is created.</span></span> <span data-ttu-id="d97bc-173">При отправке отчета в формате HTML для каждой страницы отчета создается один HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="d97bc-173">When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="d97bc-174">Чтобы запустить действие **емаилдатабасеобжект** в модуле Visual Basic для приложений (VBA), используйте метод **сендобжект** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="d97bc-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="d97bc-175">Об участнике</span><span class="sxs-lookup"><span data-stu-id="d97bc-175">About the contributor</span></span>

<span data-ttu-id="d97bc-176">**Ссылка, предоставляемая** Люк Чанг, [FMS, Inc.](https://www.fmsinc.com/), основатель компании и президента для FMS, Inc., ведущие поставщики пользовательских решений для баз данных и средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="d97bc-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="d97bc-177">Функции и пределы использования метода Сендобжект для отправки</span><span class="sxs-lookup"><span data-stu-id="d97bc-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





