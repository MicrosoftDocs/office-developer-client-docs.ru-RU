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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308752"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="02ee8-102">Макрокоманда SendKeys</span><span class="sxs-lookup"><span data-stu-id="02ee8-102">SendKeys macro action</span></span>

<span data-ttu-id="02ee8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02ee8-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Заметка о безопасности" alt="Security note" /><span data-ttu-id="02ee8-105"><strong>Заметка о безопасности</strong></span><span class="sxs-lookup"><span data-stu-id="02ee8-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02ee8-p101">Избегайте использования оператора <strong>SendKeys</strong> или макроса AutoKeys с конфиденциальной или секретной информацией. Злоумышленники могут выполнить перехват нажатий клавиш и нарушить безопасность компьютера и данных.</span><span class="sxs-lookup"><span data-stu-id="02ee8-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="02ee8-108">С помощью макрокоманды **SendKeys** можно отправлять сообщения о нажатиях клавиш непосредственно в Microsoft Access или в активное приложение на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="02ee8-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>

> [!NOTE]
> <span data-ttu-id="02ee8-109">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="02ee8-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="02ee8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="02ee8-110">Setting</span></span>

<span data-ttu-id="02ee8-111">Макрокоманда **SendKeys** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="02ee8-111">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02ee8-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="02ee8-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="02ee8-113">Описание</span><span class="sxs-lookup"><span data-stu-id="02ee8-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02ee8-114"><strong>Кодов клавиш</strong></span><span class="sxs-lookup"><span data-stu-id="02ee8-114"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="02ee8-115">Клавиши, которые вы хотите использовать для доступа или приложения.</span><span class="sxs-lookup"><span data-stu-id="02ee8-115">The keystrokes you want Access or the application to process.</span></span> <span data-ttu-id="02ee8-116">Введите клавиши в поле нажатия <strong>клавиш</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="02ee8-116">Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="02ee8-117">Можно ввести до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="02ee8-117">You can type up to 255 characters.</span></span> <span data-ttu-id="02ee8-118">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="02ee8-118">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02ee8-119"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="02ee8-119"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="02ee8-120">Указывает, должен ли макрос приостанавливаться до тех пор, пока не будут обработаны нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="02ee8-120">Specifies whether the macro should pause until the keystrokes have been processed.</span></span> <span data-ttu-id="02ee8-121">Нажмите кнопку <strong>Да</strong> (приостановить) или <strong>нет</strong> (не приостанавливать).</span><span class="sxs-lookup"><span data-stu-id="02ee8-121">Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause).</span></span> <span data-ttu-id="02ee8-122">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="02ee8-122">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="02ee8-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="02ee8-123">Remarks</span></span>

<span data-ttu-id="02ee8-124">Access обрабатывает нажатия клавиш, которые он получает через действие **SendKeys** , точно так же, как если бы вы ввели их непосредственно в окне Access.</span><span class="sxs-lookup"><span data-stu-id="02ee8-124">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="02ee8-125">Чтобы указать нажатия клавиш, используйте тот же синтаксис, что и для оператора **SendKeys** .</span><span class="sxs-lookup"><span data-stu-id="02ee8-125">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>

> [!NOTE]
> <span data-ttu-id="02ee8-126">Ошибка может возникнуть, если аргумент " **клавиши** " содержит неверный синтаксис, неправильно написанный текст или другие значения, которые не подходят для окна, в которое отправляются нажатия клавиш.</span><span class="sxs-lookup"><span data-stu-id="02ee8-126">An error can occur if the **Keystrokes** argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span>

<span data-ttu-id="02ee8-127">Это действие можно использовать для ввода сведений в диалоговом окне, в частности, если вы не хотите прерывать выполнение макроса вручную в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="02ee8-127">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box.</span></span> <span data-ttu-id="02ee8-128">Некоторые действия доступа, такие как **Printing** и **НайтиЗапись**, автоматически выбирают параметры в некоторых часто используемых диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="02ee8-128">Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes.</span></span> <span data-ttu-id="02ee8-129">Макрокоманда "КомандыКлавиатуры" ( **SendKeys** ) позволяет выбрать нужные параметры в диалоговом окне "менее часто используемые".</span><span class="sxs-lookup"><span data-stu-id="02ee8-129">You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>

> [!NOTE]
> - <span data-ttu-id="02ee8-130">Так как диалоговое окно приостанавливает работу макроса, необходимо поместить действие **SendKeys** перед действием, которое вызывает открытие диалогового окна и присвоить аргументу **Wait** значение **No**.</span><span class="sxs-lookup"><span data-stu-id="02ee8-130">Because the dialog box suspends the macro, you must put the **SendKeys** action before the action that causes the dialog box to open and set the **Wait** argument to **No**.</span></span>
> - <span data-ttu-id="02ee8-131">Время, в течение которого клавиши, обращающиеся к доступу или другому приложению, могут быть сложными.</span><span class="sxs-lookup"><span data-stu-id="02ee8-131">The timing of the keystrokes reaching Access or another application can be tricky.</span></span> <span data-ttu-id="02ee8-132">В результате рекомендуется, чтобы при достижении нужной задачи (например, макрокоманды "НайтиЗапись" (FindRecord) "( **НайтиЗапись** )) использовать этот метод, а не использовать макрокоманду **SendKeys** для заполнения параметров в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="02ee8-132">As a result, it's recommended that if there's some other method (such as the **FindRecord** action) you can use to achieve a desired task, use that method rather than using the **SendKeys** action to fill in the options in a dialog box.</span></span>

<span data-ttu-id="02ee8-133">Если вы хотите отправить более 255 символов для доступа к другому приложению Windows, можно использовать несколько действий **SendKeys** в макросе.</span><span class="sxs-lookup"><span data-stu-id="02ee8-133">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="02ee8-134">Использование макрокоманды **SendKeys** для отправки нажатий клавиш вызывает соответствующие события **KeyDown**, **KeyUp**и **KeyPress** .</span><span class="sxs-lookup"><span data-stu-id="02ee8-134">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events.</span></span> <span data-ttu-id="02ee8-135">При отПравке нажатий клавиш, отличных от ANSI (таких как клавиша функции) событие **KeyPress** не вызывается.</span><span class="sxs-lookup"><span data-stu-id="02ee8-135">Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="02ee8-136">Это действие недоступно в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="02ee8-136">This action isn't available from a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="02ee8-137">Вместо этого используйте инструкцию **SendKeys** .</span><span class="sxs-lookup"><span data-stu-id="02ee8-137">Use the **SendKeys** statement instead.</span></span>

