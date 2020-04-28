---
title: Макрокоманда RunApplication
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306841"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="1cdf4-102">Макрокоманда RunApplication</span><span class="sxs-lookup"><span data-stu-id="1cdf4-102">RunApplication macro action</span></span>

<span data-ttu-id="1cdf4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cdf4-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Заметка о безопасности" alt="Security note" /><span data-ttu-id="1cdf4-105"><strong>Заметка о безопасности</strong></span><span class="sxs-lookup"><span data-stu-id="1cdf4-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1cdf4-p101">Будьте осторожны при запуске исполняемых файлов или кода в макросах и приложениях. Исполняемые файлы или код могут использоваться для выполнения действий, которые могут скомпрометировать безопасность компьютера и данных.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1cdf4-108">Вы можете использовать действие **рунаппликатион** для запуска приложений на основе Microsoft Windows или MS DOS, таких как Microsoft Excel, Microsoft Word или Microsoft PowerPoint, в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-108">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access.</span></span> <span data-ttu-id="1cdf4-109">Например, вам может потребоваться вставить данные электронной таблицы Excel в базу данных Access.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-109">For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="1cdf4-110">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="1cdf4-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="1cdf4-111">Setting</span></span>

<span data-ttu-id="1cdf4-112">Действие **рунаппликатион** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cdf4-113">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1cdf4-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1cdf4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1cdf4-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cdf4-115"><strong>Командная строка</strong></span><span class="sxs-lookup"><span data-stu-id="1cdf4-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="1cdf4-116">Командная строка, используемая для запуска приложения (включая путь и другие необходимые параметры, такие как параметры, которые запускают приложение в определенном режиме).</span><span class="sxs-lookup"><span data-stu-id="1cdf4-116">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode).</span></span> <span data-ttu-id="1cdf4-117">Введите командную строку в поле <strong>Командная строка</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-117">Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="1cdf4-118">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-118">This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1cdf4-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="1cdf4-119">Remarks</span></span>

<span data-ttu-id="1cdf4-120">Приложение, выбранное с этим действием, загружается и выполняется на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-120">The application selected with this action loads and runs in the foreground.</span></span> <span data-ttu-id="1cdf4-121">Макрос, содержащий это действие, продолжает работу после запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-121">The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="1cdf4-122">Вы можете передавать данные между другим приложением и Access с помощью средства Microsoft Windows Dynamic Data Exchange (DDE) или буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-122">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard.</span></span> <span data-ttu-id="1cdf4-123">Вы можете использовать макрокоманду **SendKeys** для отправки нажатий клавиш в другое приложение (хотя DDE является более эффективным способом передачи данных).</span><span class="sxs-lookup"><span data-stu-id="1cdf4-123">You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data).</span></span> <span data-ttu-id="1cdf4-124">Вы также можете обмениваться данными между приложениями с помощью автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-124">You can also share data among applications by using automation.</span></span>

<span data-ttu-id="1cdf4-125">Приложения, работающие под управлением MS DOS, выполняются в окне MS-DOS в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="1cdf4-126">В операционных системах Windows существует несколько способов запуска приложения, в том числе запуска программы из проводника Windows, с помощью команды **выполнить** в меню " **Пуск** " и двойным нажатием значка программы на рабочем столе Windows.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="1cdf4-127">Вы не можете выполнить действие **рунаппликатион** в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="1cdf4-127">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="1cdf4-128">Вместо этого используйте функцию **оболочки** VBA.</span><span class="sxs-lookup"><span data-stu-id="1cdf4-128">Use the VBA **Shell** function instead.</span></span>

