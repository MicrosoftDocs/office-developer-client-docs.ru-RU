---
title: FindNextRecord Macro Action
TOCTitle: FindNextRecord Macro Action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b58478a67468fa7d00c348066459672bc31c52a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482356"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="c9d5d-102">FindNextRecord Macro Action</span><span class="sxs-lookup"><span data-stu-id="c9d5d-102">FindNextRecord Macro Action</span></span>


<span data-ttu-id="c9d5d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9d5d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9d5d-104">Действие **FindNextRecord** можно использовать для поиска следующую запись, которая соответствует условиям, указанным **предыдущей НайтиЗапись** или значение в диалоговом окне **Поиск и замена** (на вкладке **Главная** нажмите кнопку **Найти**).</span><span class="sxs-lookup"><span data-stu-id="c9d5d-104">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**).</span></span> <span data-ttu-id="c9d5d-105">Действие **FindNextRecord** можно использовать для поиска записей несколько раз.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-105">You can use the **FindNextRecord** action to search repeatedly for records.</span></span> <span data-ttu-id="c9d5d-106">Например можно последовательно по всем записям для конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-106">For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="c9d5d-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="c9d5d-107">Setting</span></span>

<span data-ttu-id="c9d5d-108">Действие **FindNextRecord** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-108">The **FindNextRecord** action doesn't have any arguments.</span></span> <span data-ttu-id="c9d5d-109">Действие **FindNextRecord** Поиск следующей записи, которая соответствует условиям, заданным с **НайтиЗапись** или в диалоговом окне **Найти и заменить** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-109">The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box.</span></span> <span data-ttu-id="c9d5d-110">Аргументы **НайтиЗапись** используются совместно с параметрами в диалоговом окне **Найти и заменить** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-110">The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="c9d5d-111">Чтобы задать условия поиска, используйте **НайтиЗапись** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-111">To set the search criteria, use the **FindRecord** action.</span></span> <span data-ttu-id="c9d5d-112">Как правило введите **НайтиЗапись** в макросе и затем использовать действие **FindNextRecord** для поиска записей, отвечающих тем же условиям.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-112">Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria.</span></span> <span data-ttu-id="c9d5d-113">Для поиска записей только при выполнении определенного условия выполнены, можно ввести условного выражения в столбце **условие** строки действие для действия **FindNextRecord** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-113">To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d5d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9d5d-114">Remarks</span></span>

<span data-ttu-id="c9d5d-115">Это действие имеет тот же эффект, что и использование кнопки **Найти далее** в диалоговом окне **Найти и заменить** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c9d5d-116">Несмотря на то, что <STRONG>НайтиЗапись</STRONG> соответствует команду <STRONG>Найти</STRONG> на вкладке <STRONG>Главная</STRONG> таблиц, запросов и форм, но не соответствует команду <STRONG>Найти</STRONG> в меню <STRONG>Правка</STRONG> в окне код.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-116">Although the <STRONG>FindRecord</STRONG> action corresponds to the <STRONG>Find</STRONG> command on the <STRONG>Home</STRONG> tab for tables, queries, and forms, it doesn't correspond to the <STRONG>Find</STRONG> command on the <STRONG>Edit</STRONG> menu in the Code window.</span></span> <span data-ttu-id="c9d5d-117"><STRONG>НайтиЗапись</STRONG> или <STRONG>FindNextRecord</STRONG> действие нельзя использовать для поиска текста в модулях.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-117">You can't use the <STRONG>FindRecord</STRONG> action or <STRONG>FindNextRecord</STRONG> action to search for text in modules.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="c9d5d-118">Если выбрать <STRONG>Только в текущем поле</STRONG> аргумент <STRONG>НайтиЗапись</STRONG> <STRONG>Да</STRONG>может потребоваться использовать <STRONG>КЭлементуУправления</STRONG> для перемещения фокуса на элемент управления, содержащий данные, которые вы ищете, прежде чем использовать <STRONG> FindNextRecord</STRONG> действие.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-118">If you've set the <STRONG>Only Current Field</STRONG> argument of the <STRONG>FindRecord</STRONG> action to <STRONG>Yes</STRONG>, you may need to use the <STRONG>GoToControl</STRONG> action to move the focus to the control containing the data you're searching for before you use the <STRONG>FindNextRecord</STRONG> action.</span></span></P>



<span data-ttu-id="c9d5d-119">Если выделенный в текущий момент текст — то же, что искомый текст во время выполняемые действия макроса **FindNextRecord** , поиск начинается сразу после выделенного в том же поле выбора и в той же записи.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-119">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record.</span></span> <span data-ttu-id="c9d5d-120">В противном случае поиск начинается с начала текущей записи.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-120">Otherwise, the search begins at the start of the current record.</span></span> <span data-ttu-id="c9d5d-121">Это позволяет найти нескольких экземпляров одного условия поиска, которые могут отображаться в одну запись.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-121">This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="c9d5d-122">Тем не менее Обратите внимание на то, что при использовании кнопки для запуска макроса, содержащего действие **FindNextRecord** будет постоянно находиться первый экземпляр условия поиска.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-122">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly.</span></span> <span data-ttu-id="c9d5d-123">Это происходит, потому что нажатия кнопки команды удаляет фокус из поля, содержащего соответствующего значения.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-123">This behavior occurs because clicking the command button removes the focus from the field containing the matching value.</span></span> <span data-ttu-id="c9d5d-124">Действие **FindNextRecord** начинают поиск с начала записи.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-124">The **FindNextRecord** action will then begin searching from the start of the record.</span></span> <span data-ttu-id="c9d5d-125">Чтобы избежать этой проблемы, запустите макрос с помощью метода, который не изменяется фокус, такие как настраиваемая кнопка панели инструментов или комбинацию клавиш, определенных в макрос AutoKeys для передачи.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-125">To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro.</span></span> <span data-ttu-id="c9d5d-126">Кроме того можно установите фокус в макрос для поля, содержащего условия поиска, прежде чем выполнять действия **FindNextRecord** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-126">Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="c9d5d-127">Это поведение также возникает при использовании кнопки для запуска макроса, содержащего **НайтиЗапись** с **Найдите первый** аргумент, значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="c9d5d-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="c9d5d-128">Чтобы выполнить действие **FindNextRecord** в Visual Basic для приложений модуль, используйте метод **FindNext** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="c9d5d-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

