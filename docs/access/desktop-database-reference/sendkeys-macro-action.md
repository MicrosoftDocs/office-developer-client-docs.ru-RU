---
title: Макрокоманда SendKeys
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: aa029e3a81670746cdc467ddf7578c5900b58b29
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929036"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="715b0-102">Макрокоманда SendKeys</span><span class="sxs-lookup"><span data-stu-id="715b0-102">SendKeys macro action</span></span>


<span data-ttu-id="715b0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="715b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Примечание по безопасности" alt="Security note" /><span data-ttu-id="715b0-105"><strong>Примечание по безопасности</strong></span><span class="sxs-lookup"><span data-stu-id="715b0-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="715b0-p101">
			Избегайте использования инструкции <strong>SendKeys</strong> или макроса AutoKeys с конфиденциальной информацией. Злоумышленники могут перехватывать нажимаемые клавиши, чтобы скомпрометировать безопасность компьютера и данных.
</span><span class="sxs-lookup"><span data-stu-id="715b0-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="715b0-108">Можно использовать действие **SendKeys** для отправки нажатия клавиш непосредственно к Microsoft Access или активного приложения на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="715b0-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>


> [!NOTE]
> <P><span data-ttu-id="715b0-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="715b0-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="715b0-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="715b0-111">Setting</span></span>

<span data-ttu-id="715b0-112">Действие **SendKeys** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="715b0-112">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="715b0-113">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="715b0-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="715b0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="715b0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="715b0-115"><strong>Коды клавиш</strong></span><span class="sxs-lookup"><span data-stu-id="715b0-115"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="715b0-116">Нажатия клавиш, нужно доступа или приложение для обработки.</span><span class="sxs-lookup"><span data-stu-id="715b0-116">The keystrokes you want Access or the application to process.</span></span> <span data-ttu-id="715b0-117">Клавиши вводятся в поле <strong>клавиатурных команд</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="715b0-117">Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="715b0-118">Можно ввести до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="715b0-118">You can type up to 255 characters.</span></span> <span data-ttu-id="715b0-119">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="715b0-119">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="715b0-120"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="715b0-120"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="715b0-121">Указывает ли макрос останавливаться обработки нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="715b0-121">Specifies whether the macro should pause until the keystrokes have been processed.</span></span> <span data-ttu-id="715b0-122">Нажмите кнопку <strong>Да</strong> (Чтобы приостановить) или <strong>Нет</strong> (чтобы не приостановить).</span><span class="sxs-lookup"><span data-stu-id="715b0-122">Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause).</span></span> <span data-ttu-id="715b0-123">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="715b0-123">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="715b0-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="715b0-124">Remarks</span></span>

<span data-ttu-id="715b0-125">Доступа обрабатывает нажатия клавиш, переданные с помощью действие **SendKeys** точно, как если бы был введен их непосредственно в окне Access.</span><span class="sxs-lookup"><span data-stu-id="715b0-125">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="715b0-126">Чтобы указать нажатия клавиш, используйте тот же синтаксис, как и для оператора **SendKeys** .</span><span class="sxs-lookup"><span data-stu-id="715b0-126">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="715b0-127">Ошибка может возникать, если аргумент <STRONG>клавиатурных команд</STRONG> содержит неправильный синтаксис, ошибочным текст или другие значения, которые не подходит для нажатия клавиш, передаются в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="715b0-127">An error can occur if the <STRONG>Keystrokes</STRONG> argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span></P>



<span data-ttu-id="715b0-128">Это действие можно использовать для ввода сведений в диалоговом окне, особенно в том случае, если вы не хотите прерывать макроса в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="715b0-128">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box.</span></span> <span data-ttu-id="715b0-129">Некоторые действия доступа, например **PrintOut** и **НайтиЗапись**автоматически выберите параметры, в некоторых часто используемых диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="715b0-129">Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes.</span></span> <span data-ttu-id="715b0-130">Можно использовать действие **SendKeys** для выбора параметров в менее часто используемых диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="715b0-130">You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="715b0-131">Так как диалоговое окно, как приостановить макрос, необходимо поместить действие <STRONG>SendKeys</STRONG> перед действие, которое вызывает диалоговое окно Открыть, и значение аргумента <STRONG>ожидания</STRONG> <STRONG>Нет</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="715b0-131">Because the dialog box suspends the macro, you must put the <STRONG>SendKeys</STRONG> action before the action that causes the dialog box to open and set the <STRONG>Wait</STRONG> argument to <STRONG>No</STRONG>.</span></span></P>
> <LI>
> <P><span data-ttu-id="715b0-132">Время нажатий доступа или другого приложения может быть сложнее.</span><span class="sxs-lookup"><span data-stu-id="715b0-132">The timing of the keystrokes reaching Access or another application can be tricky.</span></span> <span data-ttu-id="715b0-133">В результате рекомендуется, что если какой-либо другой метод (например, <STRONG>НайтиЗапись)</STRONG> можно использовать для достижения требуемой задачи, используйте этот метод, а не с помощью действие <STRONG>SendKeys</STRONG> для установки параметров в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="715b0-133">As a result, it's recommended that if there's some other method (such as the <STRONG>FindRecord</STRONG> action) you can use to achieve a desired task, use that method rather than using the <STRONG>SendKeys</STRONG> action to fill in the options in a dialog box.</span></span></P></LI></UL>



<span data-ttu-id="715b0-134">Если вы хотите отправить более 255 знаков доступа или другого приложения на базе Windows, можно использовать несколько действий **SendKeys** последовательно в макрос.</span><span class="sxs-lookup"><span data-stu-id="715b0-134">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="715b0-135">Использование действие **SendKeys** для отправки соответствующих событий **KeyDown**и **KeyUp**, **KeyPress** нажатий клавиш.</span><span class="sxs-lookup"><span data-stu-id="715b0-135">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events.</span></span> <span data-ttu-id="715b0-136">Отправка клавиатурных команд не ANSI (такие как функциональная клавиша) не приводит к возникновению события **KeyPress** .</span><span class="sxs-lookup"><span data-stu-id="715b0-136">Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="715b0-137">Это действие недоступно из Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="715b0-137">This action isn't available from a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="715b0-138">Вместо этого используйте инструкцию **SendKeys** .</span><span class="sxs-lookup"><span data-stu-id="715b0-138">Use the **SendKeys** statement instead.</span></span>

