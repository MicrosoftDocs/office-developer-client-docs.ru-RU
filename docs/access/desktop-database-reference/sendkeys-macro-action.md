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
localization_priority: Normal
ms.openlocfilehash: f8c45cdf0d9cf588f61d1b51b728a8a15f6d7e12
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722377"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="3dee7-102">Макрокоманда SendKeys</span><span class="sxs-lookup"><span data-stu-id="3dee7-102">SendKeys macro action</span></span>

<span data-ttu-id="3dee7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3dee7-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Примечание по безопасности" alt="Security note" /><span data-ttu-id="3dee7-105"><strong>Примечание по безопасности</strong></span><span class="sxs-lookup"><span data-stu-id="3dee7-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dee7-p101">
			Избегайте использования инструкции <strong>SendKeys</strong> или макроса AutoKeys с конфиденциальной информацией. Злоумышленники могут перехватывать нажимаемые клавиши, чтобы скомпрометировать безопасность компьютера и данных.
</span><span class="sxs-lookup"><span data-stu-id="3dee7-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3dee7-108">Можно использовать действие **SendKeys** для отправки нажатия клавиш непосредственно к Microsoft Access или активного приложения на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="3dee7-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>

> [!NOTE]
> <span data-ttu-id="3dee7-109">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="3dee7-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="3dee7-110">Setting</span><span class="sxs-lookup"><span data-stu-id="3dee7-110">Setting</span></span>

<span data-ttu-id="3dee7-111">Действие **SendKeys** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="3dee7-111">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3dee7-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3dee7-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3dee7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3dee7-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3dee7-114"><strong>Коды клавиш</strong></span><span class="sxs-lookup"><span data-stu-id="3dee7-114"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="3dee7-115">Нажатия клавиш, нужно доступа или приложение для обработки.</span><span class="sxs-lookup"><span data-stu-id="3dee7-115">The keystrokes you want Access or the application to process.</span></span> <span data-ttu-id="3dee7-116">Клавиши вводятся в поле <strong>клавиатурных команд</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="3dee7-116">Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="3dee7-117">Можно ввести до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="3dee7-117">You can type up to 255 characters.</span></span> <span data-ttu-id="3dee7-118">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="3dee7-118">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3dee7-119"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="3dee7-119"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="3dee7-120">Указывает ли макрос останавливаться обработки нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="3dee7-120">Specifies whether the macro should pause until the keystrokes have been processed.</span></span> <span data-ttu-id="3dee7-121">Нажмите кнопку <strong>Да</strong> (Чтобы приостановить) или <strong>Нет</strong> (чтобы не приостановить).</span><span class="sxs-lookup"><span data-stu-id="3dee7-121">Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause).</span></span> <span data-ttu-id="3dee7-122">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="3dee7-122">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3dee7-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="3dee7-123">Remarks</span></span>

<span data-ttu-id="3dee7-124">Доступа обрабатывает нажатия клавиш, переданные с помощью действие **SendKeys** точно, как если бы был введен их непосредственно в окне Access.</span><span class="sxs-lookup"><span data-stu-id="3dee7-124">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="3dee7-125">Чтобы указать нажатия клавиш, используйте тот же синтаксис, как и для оператора **SendKeys** .</span><span class="sxs-lookup"><span data-stu-id="3dee7-125">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>

> [!NOTE]
> <span data-ttu-id="3dee7-126">Ошибка может возникать, если аргумент **клавиатурных команд** содержит неправильный синтаксис, ошибочным текст или другие значения, которые не подходит для нажатия клавиш, передаются в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="3dee7-126">An error can occur if the **Keystrokes** argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span>

<span data-ttu-id="3dee7-127">Это действие можно использовать для ввода сведений в диалоговом окне, особенно в том случае, если вы не хотите прерывать макроса в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3dee7-127">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box.</span></span> <span data-ttu-id="3dee7-128">Некоторые действия доступа, например **PrintOut** и **НайтиЗапись**автоматически выберите параметры, в некоторых часто используемых диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="3dee7-128">Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes.</span></span> <span data-ttu-id="3dee7-129">Можно использовать действие **SendKeys** для выбора параметров в менее часто используемых диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="3dee7-129">You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>

> [!NOTE]
> - <span data-ttu-id="3dee7-130">Так как диалоговое окно, как приостановить макрос, необходимо поместить действие **SendKeys** перед действие, которое вызывает диалоговое окно Открыть, и значение аргумента **ожидания** **Нет**.</span><span class="sxs-lookup"><span data-stu-id="3dee7-130">Because the dialog box suspends the macro, you must put the **SendKeys** action before the action that causes the dialog box to open and set the **Wait** argument to **No**.</span></span>
> - <span data-ttu-id="3dee7-131">Время нажатий доступа или другого приложения может быть сложнее.</span><span class="sxs-lookup"><span data-stu-id="3dee7-131">The timing of the keystrokes reaching Access or another application can be tricky.</span></span> <span data-ttu-id="3dee7-132">В результате рекомендуется, что если какой-либо другой метод (например, **НайтиЗапись)** можно использовать для достижения требуемой задачи, используйте этот метод, а не с помощью действие **SendKeys** для установки параметров в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3dee7-132">As a result, it's recommended that if there's some other method (such as the **FindRecord** action) you can use to achieve a desired task, use that method rather than using the **SendKeys** action to fill in the options in a dialog box.</span></span>

<span data-ttu-id="3dee7-133">Если вы хотите отправить более 255 знаков доступа или другого приложения на базе Windows, можно использовать несколько действий **SendKeys** последовательно в макрос.</span><span class="sxs-lookup"><span data-stu-id="3dee7-133">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="3dee7-134">Использование действие **SendKeys** для отправки соответствующих событий **KeyDown**и **KeyUp**, **KeyPress** нажатий клавиш.</span><span class="sxs-lookup"><span data-stu-id="3dee7-134">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events.</span></span> <span data-ttu-id="3dee7-135">Отправка клавиатурных команд не ANSI (такие как функциональная клавиша) не приводит к возникновению события **KeyPress** .</span><span class="sxs-lookup"><span data-stu-id="3dee7-135">Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="3dee7-136">Это действие недоступно из Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="3dee7-136">This action isn't available from a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="3dee7-137">Вместо этого используйте инструкцию **SendKeys** .</span><span class="sxs-lookup"><span data-stu-id="3dee7-137">Use the **SendKeys** statement instead.</span></span>

