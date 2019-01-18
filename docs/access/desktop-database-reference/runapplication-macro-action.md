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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721789"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="4368d-102">Макрокоманда RunApplication</span><span class="sxs-lookup"><span data-stu-id="4368d-102">RunApplication macro action</span></span>

<span data-ttu-id="4368d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4368d-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Примечание по безопасности" alt="Security note" /><span data-ttu-id="4368d-105"><strong>Примечание по безопасности</strong></span><span class="sxs-lookup"><span data-stu-id="4368d-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4368d-p101">Будьте осторожны при запуске исполняемых файлов или кода в макросах и приложениях. Исполняемые файлы или код могут использоваться для выполнения действий, которые могут скомпрометировать безопасность компьютера и данных.</span><span class="sxs-lookup"><span data-stu-id="4368d-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4368d-108">Действие **RunApplication** позволяет выполнять Microsoft Windows и основе MS-DOS приложения, например Microsoft Excel, Microsoft Word или Microsoft PowerPoint в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4368d-108">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access.</span></span> <span data-ttu-id="4368d-109">Например можно вставить данные электронных таблиц Excel в базы данных Access.</span><span class="sxs-lookup"><span data-stu-id="4368d-109">For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="4368d-110">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="4368d-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="4368d-111">Setting</span><span class="sxs-lookup"><span data-stu-id="4368d-111">Setting</span></span>

<span data-ttu-id="4368d-112">Действие **RunApplication** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="4368d-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4368d-113">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="4368d-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4368d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4368d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4368d-115"><strong>Командной строки</strong></span><span class="sxs-lookup"><span data-stu-id="4368d-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="4368d-116">Командная строка, используемая для запуска приложения (включая путь и другие необходимые параметры, такие как коммутаторы, запустите приложение в определенный режим).</span><span class="sxs-lookup"><span data-stu-id="4368d-116">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode).</span></span> <span data-ttu-id="4368d-117">Введите в командной строке в поле <strong>Командная строка</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="4368d-117">Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="4368d-118">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="4368d-118">This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4368d-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="4368d-119">Remarks</span></span>

<span data-ttu-id="4368d-120">Приложения, выбранных с помощью этого действия загружает и выполняется на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="4368d-120">The application selected with this action loads and runs in the foreground.</span></span> <span data-ttu-id="4368d-121">Макрос, содержащий это действие по-прежнему производится после запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="4368d-121">The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="4368d-122">Можно перенести данные между приложением и доступа с помощью средства Microsoft Windows динамический обмен данными (DDE) exchange или в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="4368d-122">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard.</span></span> <span data-ttu-id="4368d-123">Можно использовать действие **SendKeys** для отправки нажатия клавиш для других приложений (хотя DDE является более эффективный способ передачи данных).</span><span class="sxs-lookup"><span data-stu-id="4368d-123">You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data).</span></span> <span data-ttu-id="4368d-124">Также можно обмениваться данными между приложениями с помощью автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4368d-124">You can also share data among applications by using automation.</span></span>

<span data-ttu-id="4368d-125">Приложения на основе MS-DOS выполните в окне MS-DOS в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="4368d-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="4368d-126">В операционных системах Windows существует несколько способов запуска приложения, в том числе запуск программы в проводнике Windows, с помощью команды **выполнить** в меню **Пуск** и дважды щелкните значок программы на рабочем столе Windows.</span><span class="sxs-lookup"><span data-stu-id="4368d-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="4368d-127">Не удается выполнить действие **RunApplication** в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="4368d-127">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="4368d-128">Вместо этого используйте функцию VBA **командной консоли** .</span><span class="sxs-lookup"><span data-stu-id="4368d-128">Use the VBA **Shell** function instead.</span></span>

