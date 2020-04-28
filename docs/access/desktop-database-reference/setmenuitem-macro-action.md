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
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="5d0b4-102">Макрокоманда SetMenuItem</span><span class="sxs-lookup"><span data-stu-id="5d0b4-102">SetMenuItem macro action</span></span>

<span data-ttu-id="5d0b4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d0b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d0b4-104">Вы можете использовать действие **сетменуитем** , чтобы задать состояние пунктов меню (включено или отключено, выбрано или не выбрано) в настраиваемых или глобальных меню на **вкладке "надстройки** ".</span><span class="sxs-lookup"><span data-stu-id="5d0b4-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="5d0b4-105">Действие **сетменуитем** работает только с настраиваемыми и глобальными меню, созданными с помощью макросов меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-105">The **SetMenuItem** action works only with custom and global menus created by using menu macros.</span></span> <span data-ttu-id="5d0b4-106">Действие **сетменуитем** включено в Microsoft Access только для совместимости с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-106">The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions.</span></span> <span data-ttu-id="5d0b4-107">Она не работает с функциональными возможностями панели команд.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-107">It does not work with the command bar functionality.</span></span> <span data-ttu-id="5d0b4-108">Однако можно использовать свойства **Enabled** и **State** в модуле Visual Basic для приложений (VBA) для включения или отключения, а также для выбора или отмены выбора элементов в контекстных меню или в настраиваемых или глобальных меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-108">However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span>

## <a name="setting"></a><span data-ttu-id="5d0b4-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d0b4-109">Setting</span></span>

<span data-ttu-id="5d0b4-110">Макрокоманда **сетменуитем** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d0b4-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="5d0b4-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5d0b4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5d0b4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d0b4-113"><strong>Индекс меню</strong></span><span class="sxs-lookup"><span data-stu-id="5d0b4-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="5d0b4-114">Индекс меню, содержащего команду, для которой нужно задать состояние.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="5d0b4-115">Введите целое значение, начиная с 0, для индекса требуемого меню в настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="5d0b4-116">Введите значение индекса в поле <strong>индекс меню</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="5d0b4-117">Индекс задается относительно положения меню в макросе меню для настраиваемого или глобального меню (положение этого меню в макросе меню, <strong>AddMenu</strong> считая от 0).</span><span class="sxs-lookup"><span data-stu-id="5d0b4-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="5d0b4-118">Отображение меню может быть несколько другим, так как вы можете использовать условные выражения в макросе меню, чтобы скрыть или отобразить настраиваемые элементы меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="5d0b4-119">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-119">This is a required argument.</span></span> <span data-ttu-id="5d0b4-120">Если выбрано меню с этим аргументом и не заданы аргументы индекса <strong>команд</strong> и <strong>подкоманды</strong> , можно включить или отключить само имя меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="5d0b4-121">Вы не можете выбрать или отменить выбор имени меню (Access игнорирует параметры <strong>флажков и снять</strong> <strong>флажки</strong> для аргумента <strong>Flag</strong> для названий меню).</span><span class="sxs-lookup"><span data-stu-id="5d0b4-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d0b4-122"><strong>Индекс команды</strong></span><span class="sxs-lookup"><span data-stu-id="5d0b4-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="5d0b4-123">Индекс команды, для которой необходимо задать состояние.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-123">The index of the command for which you want to set the state.</span></span> <span data-ttu-id="5d0b4-124">Введите целое значение, начиная с 0, для индекса нужной команды в меню, выбранном аргументом <strong>индекса меню</strong> .</span><span class="sxs-lookup"><span data-stu-id="5d0b4-124">Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument.</span></span> <span data-ttu-id="5d0b4-125">Индекс задается относительно положения команды в группе макросов, которое определяет выбранное меню для настраиваемого или глобального меню (положение макроса этой команды в группе макросов, считая от 0).</span><span class="sxs-lookup"><span data-stu-id="5d0b4-125">The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0).</span></span> <span data-ttu-id="5d0b4-126">Отображение меню может быть несколько другим, так как вы можете использовать условные выражения в группе макросов меню для скрытия или отображения пользовательских команд меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-126">The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d0b4-127"><strong>Индекс подкоманды</strong></span><span class="sxs-lookup"><span data-stu-id="5d0b4-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="5d0b4-128">Индекс подкоманды, для которой нужно задать состояние.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-128">The index of the subcommand for which you want to set the state.</span></span> <span data-ttu-id="5d0b4-129">Это применимо только в том случае, если требуемая команда имеет подменю.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-129">This applies only if the desired command has a submenu.</span></span> <span data-ttu-id="5d0b4-130">Введите целое значение, начиная с 0, для индекса нужной подкоманды в подменю, выбранном аргументом <strong>индекс команды</strong> .</span><span class="sxs-lookup"><span data-stu-id="5d0b4-130">Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument.</span></span> <span data-ttu-id="5d0b4-131">Индекс задается относительно положения подкоманды в группе макросов, которое определяет выбранное подменю для настраиваемого или глобального меню (положения макроса этой подкоманды в группе макросов, считая от 0).</span><span class="sxs-lookup"><span data-stu-id="5d0b4-131">The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d0b4-132"><strong>Флаг</strong></span><span class="sxs-lookup"><span data-stu-id="5d0b4-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="5d0b4-133">Состояние, в котором нужно задать команду или подкоманду.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-133">The state you want to set the command or subcommand to.</span></span> <span data-ttu-id="5d0b4-134">Щелкните <strong>серый</strong> (чтобы отключить команду — она отображается серым цветом), не является <strong>серым</strong> (чтобы включить ее), <strong>установите флажок</strong> (чтобы выполнить проверку с помощью команды, как правило, она была выбрана или переключена) или снимите <strong>флажок</strong> (чтобы удалить проверку).</span><span class="sxs-lookup"><span data-stu-id="5d0b4-134">Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check).</span></span> <span data-ttu-id="5d0b4-135">Значение по умолчанию — " <strong>серый</strong>".</span><span class="sxs-lookup"><span data-stu-id="5d0b4-135">The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5d0b4-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d0b4-136">Remarks</span></span>

<span data-ttu-id="5d0b4-137">Действие **сетменуитем** работает только в настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-137">The **SetMenuItem** action works only on a custom or global menu.</span></span> <span data-ttu-id="5d0b4-138">Если в активном окне нет настраиваемого или глобального меню, то при запуске макроса, содержащего действие **сетменуитем** , возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-138">If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="5d0b4-139">Это действие можно использовать для задания состояния команд меню и подкоманд, но не подкоманд для подкоманд.</span><span class="sxs-lookup"><span data-stu-id="5d0b4-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="5d0b4-140">Чтобы запустить действие **сетменуитем** в модуле Visual Basic для приложений (VBA), используйте метод **сетменуитем** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="5d0b4-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

