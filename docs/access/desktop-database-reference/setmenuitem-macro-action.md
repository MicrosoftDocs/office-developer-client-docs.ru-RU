---
title: Макрокоманда SetMenuItem
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fe61a3368813ba3420920909f818beee2029d993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308682"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="63111-102">Макрокоманда SetMenuItem</span><span class="sxs-lookup"><span data-stu-id="63111-102">SetMenuItem macro action</span></span>

<span data-ttu-id="63111-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63111-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63111-104">С помощью действия **SetMenuItem** можно настроить состояние элементов меню (включенных, отключенных, выбранных или невыбранных) в настраиваемом или глобальном меню на вкладке "Надстройки". </span><span class="sxs-lookup"><span data-stu-id="63111-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="63111-105">Действие **SetMenuItem** работает только с пользовательскими и глобальными меню, созданными с помощью макроса меню.</span><span class="sxs-lookup"><span data-stu-id="63111-105">The **SetMenuItem** action works only with custom and global menus created by using menu macros.</span></span> <span data-ttu-id="63111-106">Действие **SetMenuItem** включено в Microsoft Access только для совместимости с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="63111-106">The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions.</span></span> <span data-ttu-id="63111-107">Он не работает с функциями панели команд.</span><span class="sxs-lookup"><span data-stu-id="63111-107">It does not work with the command bar functionality.</span></span> <span data-ttu-id="63111-108">Однако свойства Enabled  и **State** в модуле Visual Basic для приложений (VBA) можно использовать для отключения, включения и выбора или отключения элементов в ярлыках или настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="63111-108">However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span>

## <a name="setting"></a><span data-ttu-id="63111-109">Setting</span><span class="sxs-lookup"><span data-stu-id="63111-109">Setting</span></span>

<span data-ttu-id="63111-110">Действие **SetMenuItem** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="63111-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63111-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="63111-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="63111-112">Описание</span><span class="sxs-lookup"><span data-stu-id="63111-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63111-113"><strong>Индекс меню</strong></span><span class="sxs-lookup"><span data-stu-id="63111-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="63111-114">Индекс меню, содержащий команду, для которой необходимо установить состояние.</span><span class="sxs-lookup"><span data-stu-id="63111-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="63111-115">Введите в настраиваемом или глобальном меню значение, начиная с 0, в индекс нужного меню.</span><span class="sxs-lookup"><span data-stu-id="63111-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="63111-116">Введите значение индекса в поле <strong>"Индекс</strong> меню" в разделе <strong>"Аргументы действий"</strong> области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="63111-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="63111-117">Индекс относительно позиции меню в макросах меню для настраиваемого или глобального меню (позиция действия <strong>AddMenu</strong> этого меню в макросе меню, подсчет от 0).</span><span class="sxs-lookup"><span data-stu-id="63111-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="63111-118">Отображение меню может быть немного другим, так как вы можете использовать условные выражения в макросах меню, чтобы скрыть или отобразить настраиваемые элементы меню.</span><span class="sxs-lookup"><span data-stu-id="63111-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="63111-119">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="63111-119">This is a required argument.</span></span> <span data-ttu-id="63111-120">Если выбрать меню с этим аргументом и оставить аргументы <strong>Command Index</strong> и <strong>Subcommand Index</strong> пустыми, можно включить или отключить само имя меню.</span><span class="sxs-lookup"><span data-stu-id="63111-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="63111-121">Однако нельзя выбрать или отобрать имя меню (Access <strong></strong> игнорирует параметры <strong>"Проверить"</strong> и "Отклоировать" для аргумента <strong>Flag</strong> для имен меню).</span><span class="sxs-lookup"><span data-stu-id="63111-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63111-122"><strong>Индекс команд</strong></span><span class="sxs-lookup"><span data-stu-id="63111-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="63111-123">Индекс команды, для которой необходимо установить состояние.</span><span class="sxs-lookup"><span data-stu-id="63111-123">The index of the command for which you want to set the state.</span></span> <span data-ttu-id="63111-124">Введите в меню, выбранном аргументом <strong>"Индекс</strong> меню", значение, начиная с 0, начиная с 0, в качестве индекса нужной команды.</span><span class="sxs-lookup"><span data-stu-id="63111-124">Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument.</span></span> <span data-ttu-id="63111-125">Индекс относительно позиции команды в группе макроса, которая определяет выбранное меню для настраиваемого или глобального меню (позиция макроса этой команды в группе макроса, отсчитка от 0).</span><span class="sxs-lookup"><span data-stu-id="63111-125">The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0).</span></span> <span data-ttu-id="63111-126">Отображение меню может немного по-другому, так как вы можете использовать условные выражения в группе макроса меню, чтобы скрыть или отобразить пользовательские команды меню.</span><span class="sxs-lookup"><span data-stu-id="63111-126">The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63111-127"><strong>Индекс подкоманда</strong></span><span class="sxs-lookup"><span data-stu-id="63111-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="63111-128">Индекс подкоманда, для которого необходимо установить состояние.</span><span class="sxs-lookup"><span data-stu-id="63111-128">The index of the subcommand for which you want to set the state.</span></span> <span data-ttu-id="63111-129">Это применимо только в том случае, если в нужной команде есть подменю.</span><span class="sxs-lookup"><span data-stu-id="63111-129">This applies only if the desired command has a submenu.</span></span> <span data-ttu-id="63111-130">Введите в качестве индекса нужного подкоманда в подменю, выбранном аргументом <strong>Command Index,</strong> значение, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="63111-130">Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument.</span></span> <span data-ttu-id="63111-131">Индекс является относительным положением подкоманда в группе макроса, которая определяет выбранное подменю для настраиваемого или глобального меню (позиция макроса этого подкоманда в группе макроса, при подсчете от 0).</span><span class="sxs-lookup"><span data-stu-id="63111-131">The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63111-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="63111-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="63111-133">Состояние, в который необходимо установить команду или подкоманда.</span><span class="sxs-lookup"><span data-stu-id="63111-133">The state you want to set the command or subcommand to.</span></span> <span data-ttu-id="63111-134">Нажмите "Серый" <strong>(чтобы</strong> отключить команду — она отображается неанимательно), <strong></strong> неавстранимая (чтобы включить <strong>ее),</strong> проверьте (чтобы <strong></strong> сделать проверку с помощью команды , обычно указывая, что она была выбрана или переключена) или снимите (чтобы удалить проверку).</span><span class="sxs-lookup"><span data-stu-id="63111-134">Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check).</span></span> <span data-ttu-id="63111-135">Значение по умолчанию : <strong>Ungray</strong>.</span><span class="sxs-lookup"><span data-stu-id="63111-135">The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="63111-136">Заметки</span><span class="sxs-lookup"><span data-stu-id="63111-136">Remarks</span></span>

<span data-ttu-id="63111-137">Действие **SetMenuItem** работает только в настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="63111-137">The **SetMenuItem** action works only on a custom or global menu.</span></span> <span data-ttu-id="63111-138">Если в активном окне нет настраиваемого или глобального меню, запуск макроса, содержащего действие **SetMenuItem,** приводит к ошибке во время работы.</span><span class="sxs-lookup"><span data-stu-id="63111-138">If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="63111-139">Это действие можно использовать для настройки состояния команд меню и подкомандах, но не подкомандах подкомандах.</span><span class="sxs-lookup"><span data-stu-id="63111-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="63111-140">Чтобы запустить действие **SetMenuItem** в модуле Visual Basic для приложений (VBA), используйте метод **SetMenuItem** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="63111-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

