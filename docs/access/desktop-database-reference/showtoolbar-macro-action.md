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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700341"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="520b0-102">Макрокоманда ShowToolbar</span><span class="sxs-lookup"><span data-stu-id="520b0-102">ShowToolbar macro action</span></span>

<span data-ttu-id="520b0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="520b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="520b0-104">**ПанельИнструментов** можно использовать для отображения или скрытия группы команд на вкладке **Надстройки** .</span><span class="sxs-lookup"><span data-stu-id="520b0-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="520b0-105">**ПанельИнструментов** не влияет на контекстные меню.</span><span class="sxs-lookup"><span data-stu-id="520b0-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="520b0-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="520b0-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="520b0-107">Setting</span><span class="sxs-lookup"><span data-stu-id="520b0-107">Setting</span></span>

<span data-ttu-id="520b0-108">**ПанельИнструментов** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="520b0-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="520b0-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="520b0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="520b0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="520b0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="520b0-111"><strong>Имя панели инструментов</strong></span><span class="sxs-lookup"><span data-stu-id="520b0-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="520b0-112">Имя группы команд на вкладке <strong>Надстройки</strong> требуется отобразить или скрыть.</span><span class="sxs-lookup"><span data-stu-id="520b0-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="520b0-113">В поле <strong>Имя панели инструментов</strong> в разделе <strong>Действие аргументы</strong> области конструктор макросов показаны все доступные группы, которые могут повлиять это действие.</span><span class="sxs-lookup"><span data-stu-id="520b0-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="520b0-114">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="520b0-114">This is a required argument.</span></span> <span data-ttu-id="520b0-115">Если макрос, содержащий <strong>ПанельИнструментов в базе данных библиотеки</strong> , сначала поиск группу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="520b0-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="520b0-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="520b0-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="520b0-117">Указывает на отображение или скрытие группы и в представлений для отображения или скрытия его.</span><span class="sxs-lookup"><span data-stu-id="520b0-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="520b0-118">Значение по умолчанию — <strong>Да</strong> (Показать группы в любое время).</span><span class="sxs-lookup"><span data-stu-id="520b0-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="520b0-119"><strong>Да,</strong> можно выбрать для отображения в группу на всех время, <strong>Где соответствующие</strong> для отображения в группу только в том случае, если соответствующий форму или отчет является активным, или <strong>не</strong> для скрытия группы в любое время.</span><span class="sxs-lookup"><span data-stu-id="520b0-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="520b0-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="520b0-120">Remarks</span></span>

<span data-ttu-id="520b0-121">Это действие можно использовать в макросе с условного выражения для отображения или скрытия группы в зависимости от определенных условий.</span><span class="sxs-lookup"><span data-stu-id="520b0-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="520b0-122">Если вы хотите отобразить определенную группу на форме или отчета, свойству **OnActivate** форму или отчет можно присвоить имя макроса, содержащего **ПанельИнструментов для отображения группы** .</span><span class="sxs-lookup"><span data-stu-id="520b0-122">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group.</span></span> <span data-ttu-id="520b0-123">Имя макроса, содержащего **ПанельИнструментов, чтобы скрыть группу** установите свойство **OnDeactivate** форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="520b0-123">Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="520b0-124">Встроенные панели инструментов, недоступны для отображения или скрытия с помощью этого действия, если свойству **AllowBuiltInToolbars** присвоено значение **False** (0 в Visual Basic для приложений (VBA) модуля) или установить параметр **Встроенные панели инструментов** **Значение false** в VBA с помощью метода **SetOption** .</span><span class="sxs-lookup"><span data-stu-id="520b0-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="520b0-125">Чтобы запустить **ПанельИнструментов** в модуль VBA, используйте метод **ПанельИнструментов** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="520b0-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

