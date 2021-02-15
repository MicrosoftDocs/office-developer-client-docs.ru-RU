---
title: Макрокоманда SetWarnings
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308661"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="35dab-102">Макрокоманда SetWarnings</span><span class="sxs-lookup"><span data-stu-id="35dab-102">SetWarnings macro action</span></span>

<span data-ttu-id="35dab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35dab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35dab-104">Вы можете использовать действие **SetWarnings,** чтобы включить или отключить системные сообщения.</span><span class="sxs-lookup"><span data-stu-id="35dab-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="35dab-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="35dab-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="35dab-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="35dab-106">Setting</span></span>

<span data-ttu-id="35dab-107">Действие **SetWarnings** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="35dab-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35dab-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="35dab-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="35dab-109">Описание</span><span class="sxs-lookup"><span data-stu-id="35dab-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35dab-110"><strong>Предупреждения в ветвях</strong></span><span class="sxs-lookup"><span data-stu-id="35dab-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="35dab-111">Указывает, отображаются ли системные сообщения.</span><span class="sxs-lookup"><span data-stu-id="35dab-111">Specifies whether system messages are displayed.</span></span> <span data-ttu-id="35dab-112">Нажмите <strong>кнопку</strong> "Да" (чтобы включить системные сообщения) или <strong></strong> "Нет" <strong>(для</strong> отключения системных сообщений) в поле "Предупреждения" в разделе "Аргументы действий" области построитель макроса. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="35dab-112">Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane.</span></span> <span data-ttu-id="35dab-113">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="35dab-113">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="35dab-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="35dab-114">Remarks</span></span>

<span data-ttu-id="35dab-115">Это действие можно использовать для предотвращения остановки макроса модальными предупреждениями и окнами сообщений.</span><span class="sxs-lookup"><span data-stu-id="35dab-115">You can use this action to prevent modal warnings and message boxes from stopping the macro.</span></span> <span data-ttu-id="35dab-116">Однако сообщения об ошибках всегда отображаются.</span><span class="sxs-lookup"><span data-stu-id="35dab-116">However, error messages are always displayed.</span></span> <span data-ttu-id="35dab-117">Кроме того, Microsoft Access отображает все диалоговые окна, которые требуют ввода, кроме простого нажатия кнопки (например, "ОК", "Отмена", **"Да"** или "Нет"), например любое диалоговое окно, в которое требуется ввести текст или выбрать один из нескольких параметров. </span><span class="sxs-lookup"><span data-stu-id="35dab-117">Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="35dab-118">Это действие с аргументом **Warnings On,** для которого установлено **"Нет",** имеет тот же эффект, что и нажатие на ввод при отображке предупреждения или окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="35dab-118">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed.</span></span> <span data-ttu-id="35dab-119">Обычно в **ответ**  на предупреждение или сообщение выбирается кнопка "ОК" или "Да".</span><span class="sxs-lookup"><span data-stu-id="35dab-119">Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="35dab-120">После завершения макроса Access автоматически включает отображение системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="35dab-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="35dab-121">Часто это действие используется с действием **Echo,** которое скрывает результаты макроса, пока оно не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="35dab-121">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished.</span></span> <span data-ttu-id="35dab-122">Действие **SetWarnings** также можно использовать для скрытие предупреждений и полей сообщений.</span><span class="sxs-lookup"><span data-stu-id="35dab-122">You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="35dab-123">Хотя действие **SetWarnings может** упростить взаимодействие с макросами, необходимо быть осторожным при отключлении системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="35dab-123">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off.</span></span> <span data-ttu-id="35dab-124">В некоторых случаях не нужно продолжать макрос, если отображается определенное предупреждение.</span><span class="sxs-lookup"><span data-stu-id="35dab-124">In some situations, you won't want to continue a macro if a certain warning message is displayed.</span></span> <span data-ttu-id="35dab-125">Если вы не уверены в результате всех макро действий, не следует использовать это действие.</span><span class="sxs-lookup"><span data-stu-id="35dab-125">Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="35dab-126">Чтобы запустить действие **SetWarnings** в модуле Visual Basic для приложений (VBA), используйте метод **SetWarnings** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="35dab-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

