---
title: FindRecord Macro Action
TOCTitle: FindRecord Macro Action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d62c80c18ffd091d71c88fc64c9bd5c60c580101
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483220"
---
# <a name="findrecord-macro-action"></a><span data-ttu-id="fc75f-102">FindRecord Macro Action</span><span class="sxs-lookup"><span data-stu-id="fc75f-102">FindRecord Macro Action</span></span>


<span data-ttu-id="fc75f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc75f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc75f-104">Чтобы найти первую строку данных, который соответствует условиям, указанным аргументы **НайтиЗапись** можно использовать **НайтиЗапись** .</span><span class="sxs-lookup"><span data-stu-id="fc75f-104">You can use the **FindRecord** action to find the first instance of data that meets the criteria specified by the **FindRecord** arguments.</span></span> <span data-ttu-id="fc75f-105">Эти данные могут быть в текущей записи, в записи следующего или предыдущего или первой записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-105">This data can be in the current record, in a succeeding or prior record, or in the first record.</span></span> <span data-ttu-id="fc75f-106">Можно найти записи в активной таблица в режиме таблицы, запрос в режиме таблицы, формы или формы.</span><span class="sxs-lookup"><span data-stu-id="fc75f-106">You can find records in the active table datasheet, query datasheet, form datasheet, or form.</span></span>

## <a name="setting"></a><span data-ttu-id="fc75f-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="fc75f-107">Setting</span></span>

<span data-ttu-id="fc75f-108">**НайтиЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fc75f-108">The **FindRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc75f-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="fc75f-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fc75f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fc75f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc75f-111"><strong>Find What (Образец поиска)</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-111"><strong>Find What</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-112">Определяет данные, которые требуется найти в записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-112">Specifies the data you want to find in the record.</span></span> <span data-ttu-id="fc75f-113">Введите текст, число или дату, чтобы найти или введите выражение, которое будет стоять знак равенства (<strong>=</strong>), в поле <strong>Найти</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="fc75f-113">Enter the text, number, or date you want to find or type an expression, which is preceded by an equal sign (<strong>=</strong>), in the <strong>Find What</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="fc75f-114">Можно использовать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="fc75f-114">You can use wildcard characters.</span></span> <span data-ttu-id="fc75f-115">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="fc75f-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc75f-116"><strong>Соответствие</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-116"><strong>Match</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-117">Указывает расположение данных в поле.</span><span class="sxs-lookup"><span data-stu-id="fc75f-117">Specifies where the data is located in the field.</span></span> <span data-ttu-id="fc75f-118">Поиск данных в любой части поля (<strong>Любой части поля</strong>), можно указать для данных, которая заполняет всю поле (<strong>Поля целиком</strong>) или для данных, расположенного в начале поля (<strong>Начала поля</strong>).</span><span class="sxs-lookup"><span data-stu-id="fc75f-118">You can specify a search for data in any part of the field (<strong>Any Part of Field</strong>), for data that fills the entire field (<strong>Whole Field</strong>), or for data located at the beginning of the field (<strong>Start of Field</strong>).</span></span> <span data-ttu-id="fc75f-119">Значение по умолчанию — <strong>Поля целиком</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-119">The default is <strong>Whole Field</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc75f-120"><strong>Match Case (С учетом регистра)</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-120"><strong>Match Case</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-121">Указывает, является ли поиск с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="fc75f-121">Specifies whether the search is case-sensitive.</span></span> <span data-ttu-id="fc75f-122">Нажмите кнопку <strong>Да</strong> (поведения поиска с учетом регистра) или <strong>Нет</strong> (поиска без точно соответствующих прописных и строчных букв).</span><span class="sxs-lookup"><span data-stu-id="fc75f-122">Click <strong>Yes</strong> (conduct a case-sensitive search) or <strong>No</strong> (search without matching uppercase and lowercase letters exactly).</span></span> <span data-ttu-id="fc75f-123">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-123">The default is <strong>No</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc75f-124"><strong>Поиск</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-124"><strong>Search</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-125">Указывает, будет ли поиск продолжается из текущей записи первой записи (<strong>копирования</strong>); вниз до конца записей (<strong>вниз</strong>); или вниз до конца записей, а затем от начала записей для записи, так что все записи, поиск (<strong>все</strong>).</span><span class="sxs-lookup"><span data-stu-id="fc75f-125">Specifies whether the search proceeds from the current record up to the beginning of the records (<strong>Up</strong>); down to the end of the records (<strong>Down</strong>); or down to the end of the records and then from the beginning of the records to the current record, so all records are searched (<strong>All</strong>).</span></span> <span data-ttu-id="fc75f-126">Значение по умолчанию — <strong>все</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-126">The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc75f-127"><strong>Поиск, как форматирование</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-127"><strong>Search As Formatted</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-128">Указывает, будет ли в поиск включаются форматированными данными.</span><span class="sxs-lookup"><span data-stu-id="fc75f-128">Specifies whether the search includes formatted data.</span></span> <span data-ttu-id="fc75f-129">Нажмите кнопку <strong>Да</strong> (Microsoft Office Access 2007 выполняет поиск данных как формат и отображается в поле) или <strong>Нет</strong> (получить доступ к поисков для данных, хранимых в базе данных, которая не всегда же, как оно отображается).</span><span class="sxs-lookup"><span data-stu-id="fc75f-129">Click <strong>Yes</strong> (Microsoft Office Access 2007 searches for the data as it is formatted and displayed in the field) or <strong>No</strong> (Access searches for the data as it is stored in the database, which isn't always the same as it's displayed).</span></span> <span data-ttu-id="fc75f-130">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-130">The default is <strong>No</strong>.</span></span> <span data-ttu-id="fc75f-131">Этот компонент можно использовать для ограничения поиска данных в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="fc75f-131">You can use this feature to restrict the search to data in a particular format.</span></span> <span data-ttu-id="fc75f-132">Например нажмите кнопку <strong>Да</strong> и введите <strong>1234</strong> в качестве аргумента <strong>Найти</strong> поиск значения в поле Формат для включения их запятыми.</span><span class="sxs-lookup"><span data-stu-id="fc75f-132">For example, click <strong>Yes</strong> and type <strong>1,234</strong> in the <strong>Find What</strong> argument to find a value of 1,234 in a field formatted to include commas.</span></span> <span data-ttu-id="fc75f-133">Выберите <strong>Нет</strong> , если вы хотите введите <strong>1234</strong> для поиска данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="fc75f-133">Click <strong>No</strong> if you want to type <strong>1234</strong> to search for the data in this field.</span></span> <span data-ttu-id="fc75f-134">Чтобы найти даты, нажмите кнопку <strong>Да,</strong> чтобы найти даты именно так, как он имеет формат, например 08 июля 2003 г..</span><span class="sxs-lookup"><span data-stu-id="fc75f-134">To search for dates, click <strong>Yes</strong> to find a date exactly as it is formatted, such as 08-July-2003.</span></span> <span data-ttu-id="fc75f-135">Если нажать кнопку <strong>Нет</strong>, введите дату для аргумента <strong>Образец поиска</strong> в формате, которое задано в региональных параметрах в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="fc75f-135">If you click <strong>No</strong>, enter the date for the <strong>Find What</strong> argument in the format that is set in the regional settings in Windows Control Panel.</span></span> <span data-ttu-id="fc75f-136">В этом формате отображается в поле <strong>с кратким форматом даты</strong> , найденные на вкладке <strong>Дата</strong> в региональных параметрах.</span><span class="sxs-lookup"><span data-stu-id="fc75f-136">This format is shown in the <strong>Short date format</strong> box found on the <strong>Date</strong> tab in the regional settings.</span></span> <span data-ttu-id="fc75f-137">К примеру Если <strong>M/d/гг</strong>поле <strong>с кратким форматом даты</strong> , можно ввести 7 и 8/03 и Access найдет все записи в поле даты, соответствующие 8 июля 2003 г., независимо от того, как это поле имеет формат.</span><span class="sxs-lookup"><span data-stu-id="fc75f-137">For example, if the <strong>Short date format</strong> box is set to <strong>M/d/yy</strong>, you can enter 7/8/03, and Access will find all entries in a Date field that correspond to July 8, 2003, regardless of how this field is formatted.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="fc75f-138">Аргумент <STRONG>Формата</STRONG> вступает в силу только в том случае, если текущее поле является связанный элемент управления, аргумент <STRONG>совпадение</STRONG> задано значение <STRONG>Поля целиком</STRONG>, аргумент <STRONG>Только в текущем поле</STRONG> задано значение <STRONG>Да</STRONG>и аргумент <STRONG>Учитывать регистр</STRONG> задано значение <STRONG>No</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-138">The <STRONG>Search As Formatted</STRONG> argument takes effect only if the current field is a bound control, the <STRONG>Match</STRONG> argument is set to <STRONG>Whole Field</STRONG>, the <STRONG>Only Current Field</STRONG> argument is set to <STRONG>Yes</STRONG>, and the <STRONG>Match Case</STRONG> argument is set to <STRONG>No</STRONG>.</span></span></P>


<p><span data-ttu-id="fc75f-139">Если значение <strong>Да</strong> или <strong>Только в текущем поле</strong> , по которому <strong>Нет</strong>значение <strong>Учитывать регистр</strong> , необходимо также установить <strong>Формата</strong> значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-139">If you set <strong>Match Case</strong> to <strong>Yes</strong> or <strong>Only Current Field</strong> to <strong>No</strong>, you must also set <strong>Search As Formatted</strong> to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc75f-140"><strong>Только в текущем поле</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-140"><strong>Only Current Field</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-141">Указывает, ограничен текущего поля в каждой записи поиска или включает в себя всех полей в каждой записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-141">Specifies whether the search is confined to the current field in each record or includes all fields in each record.</span></span> <span data-ttu-id="fc75f-142">Поиск в текущем поле выполняется быстрее.</span><span class="sxs-lookup"><span data-stu-id="fc75f-142">Searching in the current field is faster.</span></span> <span data-ttu-id="fc75f-143">Нажмите кнопку <strong>Да</strong> (ограничивается только поиска для текущего поля) или <strong>Нет</strong> (поиск во всех полях в каждой записи).</span><span class="sxs-lookup"><span data-stu-id="fc75f-143">Click <strong>Yes</strong> (confine the search to the current field) or <strong>No</strong> (search in all fields in each record).</span></span> <span data-ttu-id="fc75f-144">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-144">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc75f-145"><strong>Найти первую</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-145"><strong>Find First</strong></span></span></p></td>
<td><p><span data-ttu-id="fc75f-146">Указывает, будет ли поиск начинается в первой записи или в текущей строке.</span><span class="sxs-lookup"><span data-stu-id="fc75f-146">Specifies whether the search starts at the first record or at the current record.</span></span> <span data-ttu-id="fc75f-147">Нажмите кнопку <strong>Да</strong> (начать с первой записи) или <strong>Нет</strong> (запустите задается по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="fc75f-147">Click <strong>Yes</strong> (start at the first record) or <strong>No</strong> (start at the current record).</span></span> <span data-ttu-id="fc75f-148">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc75f-148">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fc75f-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc75f-149">Remarks</span></span>

<span data-ttu-id="fc75f-150">После запуска макроса **НайтиЗапись** ищет указанные данные в записях (порядок поиска, определяется параметром аргумент **поиска** ).</span><span class="sxs-lookup"><span data-stu-id="fc75f-150">When a macro runs the **FindRecord** action, Access searches for the specified data in the records (the order of the search is determined by the setting of the **Search** argument).</span></span> <span data-ttu-id="fc75f-151">Когда Access находит указанные данные, данные будет установлен в записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-151">When Access finds the specified data, the data is selected in the record.</span></span>

<span data-ttu-id="fc75f-152">**НайтиЗапись** эквивалентен на вкладке **Главная** нажмите кнопку **Найти** и ее аргументы такие же, как параметры в диалоговом окне **Найти и заменить** .</span><span class="sxs-lookup"><span data-stu-id="fc75f-152">The **FindRecord** action is equivalent to clicking **Find** on the **Home** tab, and its arguments are the same as the options in the **Find and Replace** dialog box.</span></span> <span data-ttu-id="fc75f-153">Если задать аргументы **НайтиЗапись** в области построения макросов и запустите макрос, вы увидите соответствующие параметры, выбранные в диалоговом окне **Найти и заменить** при нажатии кнопки **Найти**.</span><span class="sxs-lookup"><span data-stu-id="fc75f-153">If you set the **FindRecord** arguments in the Macro Builder pane and then run the macro, you will see the corresponding options selected in the **Find and Replace** dialog box when you click **Find**.</span></span>

<span data-ttu-id="fc75f-154">Access сохраняет самыми последними **НайтиЗапись** аргументов во время сеанса базы данных, чтобы вам не нужно вводить тем же условиям несколько раз при выполнении последующих операций с **НайтиЗапись** .</span><span class="sxs-lookup"><span data-stu-id="fc75f-154">Access retains the most recent **FindRecord** arguments during a database session so that you don't need to enter the same criteria repeatedly as you perform subsequent operations with the **FindRecord** action.</span></span> <span data-ttu-id="fc75f-155">Если аргумент не заполнено, используются самые последние настройки для аргумента, как набор **одни** или в диалоговом окне **Найти и заменить** .</span><span class="sxs-lookup"><span data-stu-id="fc75f-155">If you leave an argument blank, Access uses the most recent setting for the argument, as set either by a previous **FindRecord** action or in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="fc75f-156">Для поиска записей с помощью макроса, необходимо используйте \*\*НайтиЗапись не **RunMenuCommand** действие с аргумента которого задано значение выполните команду **Найти** \*\* .</span><span class="sxs-lookup"><span data-stu-id="fc75f-156">When you want to find a record by using a macro, use the **FindRecord** action, not the **RunMenuCommand** action with its argument set to run the **Find** command.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fc75f-157">Во время <STRONG>НайтиЗапись</STRONG> соответствует команду <STRONG>Найти</STRONG> на вкладке <STRONG>Главная</STRONG> таблиц, запросов и форм, но не соответствует команду <STRONG>Найти</STRONG> в меню <STRONG>Правка</STRONG> в окне код.</span><span class="sxs-lookup"><span data-stu-id="fc75f-157">While the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window.</span></span> <span data-ttu-id="fc75f-158"><STRONG>НайтиЗапись</STRONG> нельзя использовать для поиска текста в модулях.</span><span class="sxs-lookup"><span data-stu-id="fc75f-158">You can't use the <STRONG>FindRecord</STRONG> action to search for text in modules.</span></span></P>



<span data-ttu-id="fc75f-159">Если выделенный в текущий момент текст — то же, что искомый текст во время выполняемые **НайтиЗапись** , поиск начинается сразу после выделенного в том же поле выбора и в той же записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-159">If the currently selected text is the same as the search text at the time the **FindRecord** action is carried out, the search begins immediately following the selection in the same field as the selection, and in the same record.</span></span> <span data-ttu-id="fc75f-160">В противном случае поиск начинается с начала текущей записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-160">Otherwise, the search begins at the start of the current record.</span></span> <span data-ttu-id="fc75f-161">Это позволяет найти нескольких экземпляров одного условия поиска, которые могут отображаться в одну запись.</span><span class="sxs-lookup"><span data-stu-id="fc75f-161">This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="fc75f-162">Тем не менее Обратите внимание на то, что при использовании кнопки для запуска макроса, содержащего **НайтиЗапись** будет постоянно находиться первый экземпляр условия поиска.</span><span class="sxs-lookup"><span data-stu-id="fc75f-162">However, note that if you use a command button to run a macro containing the **FindRecord** action, the first instance of the search criteria will be found repeatedly.</span></span> <span data-ttu-id="fc75f-163">Это происходит, потому что нажатия кнопки команды удаляет фокус из поля, содержащего соответствующего значения.</span><span class="sxs-lookup"><span data-stu-id="fc75f-163">This behavior occurs because clicking the command button removes the focus from the field containing the matching value.</span></span> <span data-ttu-id="fc75f-164">**НайтиЗапись** начинают поиск с начала записи.</span><span class="sxs-lookup"><span data-stu-id="fc75f-164">The **FindRecord** action will then begin searching from the start of the record.</span></span> <span data-ttu-id="fc75f-165">Чтобы избежать этой проблемы, запустите макрос с помощью метода, который не фокус, такие как настраиваемая кнопка панели инструментов или комбинацию клавиш, определенных в макросе AutoKeys или задать фокус в макрос для поля, содержащего условия поиска, прежде чем выполнять \*\* НайтиЗапись\*\* действие.</span><span class="sxs-lookup"><span data-stu-id="fc75f-165">To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro, or set the focus in the macro to the field containing the search criteria before you carry out the **FindRecord** action.</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Примечание по безопасности" alt="Security note" /><span data-ttu-id="fc75f-167"><strong>Примечание по безопасности</strong></span><span class="sxs-lookup"><span data-stu-id="fc75f-167"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc75f-p115">
			Избегайте использования инструкции <strong>SendKeys</strong> или макроса AutoKeys с конфиденциальной информацией. Злоумышленники могут перехватывать нажимаемые клавиши, чтобы скомпрометировать безопасность компьютера и данных.
</span><span class="sxs-lookup"><span data-stu-id="fc75f-p115">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc75f-170">Это поведение также возникает при использовании кнопки для запуска макроса, содержащего **СледующаяЗапись** .</span><span class="sxs-lookup"><span data-stu-id="fc75f-170">The same behavior also occurs if you use a command button to run a macro containing the **FindNext** action.</span></span>

<span data-ttu-id="fc75f-171">Чтобы запустить **НайтиЗапись** в Visual Basic для приложений (VBA) модуль, используйте метод **НайтиЗапись** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="fc75f-171">To run the **FindRecord** action in a Visual Basic for Applications (VBA) module, use the **FindRecord** method of the **DoCmd** object.</span></span>

<span data-ttu-id="fc75f-172">Для более сложного поиска можно использовать действие **ПоискЗаписи** макрос.</span><span class="sxs-lookup"><span data-stu-id="fc75f-172">For more complex searches, you may want to use the **SearchForRecord** macro action.</span></span>

