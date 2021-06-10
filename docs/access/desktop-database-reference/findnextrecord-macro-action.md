---
title: Макрокоманда FindNextRecord
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c92a43ce2f4417fde83a544022a90cfca572bf60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292351"
---
# <a name="findnextrecord-macro-action"></a><span data-ttu-id="aa91d-102">Макрокоманда FindNextRecord</span><span class="sxs-lookup"><span data-stu-id="aa91d-102">FindNextRecord macro action</span></span>


<span data-ttu-id="aa91d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa91d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa91d-104">Вы можете использовать действие **FindNextRecord,** чтобы найти следующую запись, которая соответствует критериям, заданным предыдущим действием **FindRecord** или значением в диалоговом окне Найти и заменить (на вкладке Главная нажмите кнопку **Найти).**  </span><span class="sxs-lookup"><span data-stu-id="aa91d-104">You can use the **FindNextRecord** action to find the next record that meets the criteria specified by the previous **FindRecord** action or the value in the **Find and Replace** dialog box (on the **Home** tab, click **Find**).</span></span> <span data-ttu-id="aa91d-105">Вы можете использовать **действие FindNextRecord** для многократного поиска записей.</span><span class="sxs-lookup"><span data-stu-id="aa91d-105">You can use the **FindNextRecord** action to search repeatedly for records.</span></span> <span data-ttu-id="aa91d-106">Например, можно последовательно перемещать все записи для конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="aa91d-106">For example, you can move successively through all the records for a specific customer.</span></span>

## <a name="setting"></a><span data-ttu-id="aa91d-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="aa91d-107">Setting</span></span>

<span data-ttu-id="aa91d-108">Действие **FindNextRecord** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="aa91d-108">The **FindNextRecord** action doesn't have any arguments.</span></span> <span data-ttu-id="aa91d-109">Действие **FindNextRecord** находит следующую запись, которая соответствует критериям, установленным действием **FindRecord** или диалоговом окне **Find and Replace.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-109">The **FindNextRecord** action finds the next record that meets the criteria set either by the **FindRecord** action or in the **Find and Replace** dialog box.</span></span> <span data-ttu-id="aa91d-110">Аргументы для действия **FindRecord** делятся с вариантами в диалоговом окне Найти и **заменить.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-110">The arguments for the **FindRecord** action are shared with the options in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="aa91d-111">Чтобы установить критерии поиска, используйте **действие FindRecord.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-111">To set the search criteria, use the **FindRecord** action.</span></span> <span data-ttu-id="aa91d-112">Как правило, вы вводите действие **FindRecord** в макросе, а затем используете **действие FindNextRecord,** чтобы найти последующие записи, которые соответствуют тем же критериям.</span><span class="sxs-lookup"><span data-stu-id="aa91d-112">Typically, you enter a **FindRecord** action in a macro and then use the **FindNextRecord** action to find succeeding records that meet the same criteria.</span></span> <span data-ttu-id="aa91d-113">Чтобы искать записи только при определенном условии, можно ввести условное выражение в столбце **Condition** строки действий для действия **FindNextRecord.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-113">To search for records only when a certain condition is met, you can enter a conditional expression in the **Condition** column of the action row for the **FindNextRecord** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa91d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa91d-114">Remarks</span></span>

<span data-ttu-id="aa91d-115">Это действие имеет тот же эффект, что и использование кнопки **Find Next** в диалоговом окне Найти и **заменить.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-115">This action has the same effect as using the **Find Next** button in the **Find and Replace** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="aa91d-116">Хотя действие **FindRecord** соответствует команде **Find** на вкладке **Главная** для таблиц, запросов и форм,  оно не соответствует команде Find в меню **Edit** в окне Code.</span><span class="sxs-lookup"><span data-stu-id="aa91d-116">Although the **FindRecord** action corresponds to the **Find** command on the **Home** tab for tables, queries, and forms, it doesn't correspond to the **Find** command on the **Edit** menu in the Code window.</span></span> <span data-ttu-id="aa91d-117">Вы не можете использовать действие **FindRecord** или **FindNextRecord** для поиска текста в модулях.</span><span class="sxs-lookup"><span data-stu-id="aa91d-117">You can't use the **FindRecord** action or **FindNextRecord** action to search for text in modules.</span></span>

> [!TIP]
> <span data-ttu-id="aa91d-118">Если для действия  **FindRecord** задавалось только текущее **поле,** может потребоваться использовать действие **GoToControl,** чтобы переместить фокус на управление, содержащее данные, которые вы ищете, прежде чем использовать действие **FindNextRecord.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-118">If you've set the **Only Current Field** argument of the **FindRecord** action to **Yes**, you may need to use the **GoToControl** action to move the focus to the control containing the data you're searching for before you use the **FindNextRecord** action.</span></span>

<span data-ttu-id="aa91d-119">Если выбранный в настоящее время текст является таким же, как текст поиска во время действия **макрос FindNextRecord,** поиск начинается сразу после выбора, в том же поле, что и выбор, и в той же записи.</span><span class="sxs-lookup"><span data-stu-id="aa91d-119">If the currently selected text is the same as the search text at the time the **FindNextRecord** macro action is carried out, the search begins immediately following the selection, in the same field as the selection, and in the same record.</span></span> <span data-ttu-id="aa91d-120">В противном случае поиск начинается в начале текущей записи.</span><span class="sxs-lookup"><span data-stu-id="aa91d-120">Otherwise, the search begins at the start of the current record.</span></span> <span data-ttu-id="aa91d-121">Это позволяет находить несколько экземпляров тех же критериев поиска, которые могут отображаться в одной записи.</span><span class="sxs-lookup"><span data-stu-id="aa91d-121">This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="aa91d-122">Однако обратите внимание, что при использовании кнопки команды для запуска макроса, содержащего действие **FindNextRecord,** первый экземпляр критериев поиска будет найден повторно.</span><span class="sxs-lookup"><span data-stu-id="aa91d-122">However, note that if you use a command button to run a macro containing the **FindNextRecord** action, the first instance of the search criteria will be found repeatedly.</span></span> <span data-ttu-id="aa91d-123">Такое поведение возникает из-за того, что нажатие кнопки команды удаляет фокус из поля, содержащего совпадающее значение.</span><span class="sxs-lookup"><span data-stu-id="aa91d-123">This behavior occurs because clicking the command button removes the focus from the field containing the matching value.</span></span> <span data-ttu-id="aa91d-124">После **этого действие FindNextRecord** начнет поиск с самого начала записи.</span><span class="sxs-lookup"><span data-stu-id="aa91d-124">The **FindNextRecord** action will then begin searching from the start of the record.</span></span> <span data-ttu-id="aa91d-125">Чтобы избежать этой проблемы, запустите макрос с помощью метода, который не меняет фокус, например настраиваемой кнопки панели инструментов или сочетания ключей, определенных в макрос AutoKeys.</span><span class="sxs-lookup"><span data-stu-id="aa91d-125">To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro.</span></span> <span data-ttu-id="aa91d-126">Кроме того, перед проведением действия **FindNextRecord** установите фокус в макросе на поле, содержащее критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="aa91d-126">Alternatively, set the focus in the macro to the field containing the search criteria before you carry out the **FindNextRecord** action.</span></span>

<span data-ttu-id="aa91d-127">Такое же поведение также происходит, если вы используете кнопку команды для запуска макроса, содержащего действие **FindRecord** с набором аргумента **Find First** для **No**.</span><span class="sxs-lookup"><span data-stu-id="aa91d-127">The same behavior also occurs if you use a command button to run a macro containing the **FindRecord** action with the **Find First** argument set to **No**.</span></span>

<span data-ttu-id="aa91d-128">Чтобы выполнить **действие FindNextRecord** в Visual Basic для приложений, используйте метод **FindNext** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="aa91d-128">To run the **FindNextRecord** action in a Visual Basic for Applications module, use the **FindNext** method of the **DoCmd** object.</span></span>

