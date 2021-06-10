---
title: Макрокоманда ShowToolbar
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306477"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="b88f0-102">Макрокоманда ShowToolbar</span><span class="sxs-lookup"><span data-stu-id="b88f0-102">ShowToolbar macro action</span></span>

<span data-ttu-id="b88f0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b88f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b88f0-104">Вы можете использовать **действие ShowToolbar** для отображения или сокрытия группы команд на вкладке **Надстройки.**</span><span class="sxs-lookup"><span data-stu-id="b88f0-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="b88f0-105">Действие **ShowToolbar** не влияет на меню ярлыков.</span><span class="sxs-lookup"><span data-stu-id="b88f0-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="b88f0-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="b88f0-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b88f0-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="b88f0-107">Setting</span></span>

<span data-ttu-id="b88f0-108">Действие **ShowToolbar** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b88f0-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b88f0-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b88f0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b88f0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b88f0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b88f0-111"><strong>Имя панели инструментов</strong></span><span class="sxs-lookup"><span data-stu-id="b88f0-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b88f0-112">Имя группы команд на <strong></strong> вкладке Надстройки, отобразить или скрыть.</span><span class="sxs-lookup"><span data-stu-id="b88f0-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="b88f0-113">Поле <strong>Имя панели инструментов</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder показывает все доступные группы, на которые может повлиять это действие.</span><span class="sxs-lookup"><span data-stu-id="b88f0-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="b88f0-114">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b88f0-114">This is a required argument.</span></span> <span data-ttu-id="b88f0-115">При запуске макроса, содержащего действие <strong>ShowToolbar</strong> в базе данных библиотеки, Access сначала ищет группу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="b88f0-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88f0-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="b88f0-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="b88f0-117">Указывает, следует ли отображать или скрывать группу и в каких представлениях ее отображать или скрывать.</span><span class="sxs-lookup"><span data-stu-id="b88f0-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="b88f0-118">По умолчанию — <strong>да</strong> (покажите группу всегда).</span><span class="sxs-lookup"><span data-stu-id="b88f0-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="b88f0-119">Вы можете выбрать <strong>Да</strong> для отображения группы в любой <strong>момент,</strong> если необходимо отображать группу <strong></strong> только при активной форме или отчете, или Нет, чтобы скрыть группу во все времена.</span><span class="sxs-lookup"><span data-stu-id="b88f0-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b88f0-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b88f0-120">Remarks</span></span>

<span data-ttu-id="b88f0-121">Это действие можно использовать в макросе с условными выражениями для отображения или сокрытия группы в зависимости от определенных условий.</span><span class="sxs-lookup"><span data-stu-id="b88f0-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="b88f0-122">Если вы хотите показать определенную группу только в одной форме или отчете, можно задать свойство **OnActivate** формы или отчет имени макроса, который содержит действие **ShowToolbar,** чтобы показать группу.</span><span class="sxs-lookup"><span data-stu-id="b88f0-122">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group.</span></span> <span data-ttu-id="b88f0-123">Затем установите **свойство OnDeactivate** формы или отчета на имя макроса, который содержит действие **ShowToolbar,** чтобы скрыть группу.</span><span class="sxs-lookup"><span data-stu-id="b88f0-123">Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="b88f0-124">Встроенные панели инструментов недоступны для отображения или сокрытия с помощью этого действия, если вы установите свойство **AllowBuiltInToolbars** false (0) в модуле Visual Basic для приложений (VBA) или если вы установите параметр **Allow Built-in Toolbars** false в VBA с помощью **метода SetOption.**  </span><span class="sxs-lookup"><span data-stu-id="b88f0-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="b88f0-125">Чтобы выполнить **действие ShowToolbar** в модуле VBA, используйте **метод ShowToolbar** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="b88f0-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

