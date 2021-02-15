---
title: Макрокоманда QuitAccess
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 424b2b2cab9bc4272052a201350a0cc2ab297b8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302816"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="63ea2-102">Макрокоманда QuitAccess</span><span class="sxs-lookup"><span data-stu-id="63ea2-102">QuitAccess macro action</span></span>

<span data-ttu-id="63ea2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63ea2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63ea2-104">Вы можете использовать действие **QuitAccess** для выхода из Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="63ea2-104">You can use the **QuitAccess** action to exit Microsoft Access.</span></span> <span data-ttu-id="63ea2-105">Действие **QuitAccess** также может указать один из нескольких вариантов сохранения объектов базы данных перед выходом из Access.</span><span class="sxs-lookup"><span data-stu-id="63ea2-105">The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>

> [!NOTE]
> <span data-ttu-id="63ea2-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="63ea2-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="63ea2-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="63ea2-107">Setting</span></span>

<span data-ttu-id="63ea2-108">Действие **QuitAccess** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="63ea2-108">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63ea2-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="63ea2-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="63ea2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="63ea2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63ea2-111"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="63ea2-111"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="63ea2-112">Указывает, что происходит с несравняемой объектами при выходе из Access.</span><span class="sxs-lookup"><span data-stu-id="63ea2-112">Specifies what happens to unsaved objects when you quit Access.</span></span> <span data-ttu-id="63ea2-113">Нажмите кнопку "Подсказка" <strong>(чтобы</strong> отобразить диалоговые окна с запросом на сохранение каждого <strong>объекта),</strong> "Сохранить все" (чтобы сохранить все <strong></strong> объекты без запроса по диалоговым окнам) или "Выйти" <strong>(чтобы</strong> выйти без сохранения объектов) в поле <strong>"Параметры"</strong> в разделе "Аргументы действий" области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="63ea2-113">Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="63ea2-114">Значение по умолчанию — <strong>"Сохранить все".</strong></span><span class="sxs-lookup"><span data-stu-id="63ea2-114">The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="63ea2-115">Заметки</span><span class="sxs-lookup"><span data-stu-id="63ea2-115">Remarks</span></span>

<span data-ttu-id="63ea2-116">Access не выполнит никаких действий, которые следуют действию **QuitAccess** в макросе.</span><span class="sxs-lookup"><span data-stu-id="63ea2-116">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="63ea2-117">Это действие можно использовать для выхода  из Access без подсказок из диалогов сохранения с помощью настраиваемой команды меню или кнопки на форме.</span><span class="sxs-lookup"><span data-stu-id="63ea2-117">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form.</span></span> <span data-ttu-id="63ea2-118">Например, у вас может быть этаголовая форма, используемая для отображения объектов в настраиваемой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="63ea2-118">For example, you might have a master form that you use to display the objects in your custom workspace.</span></span> <span data-ttu-id="63ea2-119">Эта форма может иметь кнопку **Quit,** которая запускает макрос, содержащий действие **QuitAccess** с аргументом **Options,** установленным как **"Сохранить все"**.</span><span class="sxs-lookup"><span data-stu-id="63ea2-119">This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="63ea2-120">Это действие имеет тот же  эффект, что и при нажатии на вкладку "Файл" и нажатии кнопки **"Выход".**</span><span class="sxs-lookup"><span data-stu-id="63ea2-120">This action has the same effect as clicking the **File** tab and then clicking **Exit**.</span></span> <span data-ttu-id="63ea2-121">Если при нажатии этой команды имеются какие-либо несжатые объекты, отображаются  те же диалоговые окна, что и при использовании запроса аргумента **Options** действия **QuitAccess.**</span><span class="sxs-lookup"><span data-stu-id="63ea2-121">If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="63ea2-122">Вы можете использовать действие **SaveObject** в макросах, чтобы сохранить указанный объект без выхода из Access или закрытия объекта.</span><span class="sxs-lookup"><span data-stu-id="63ea2-122">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="63ea2-123">Чтобы запустить действие **QuitAccess** в модуле Visual Basic для приложений (VBA), используйте метод **Quit** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="63ea2-123">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

