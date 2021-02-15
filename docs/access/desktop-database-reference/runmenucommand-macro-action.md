---
title: Макрокоманда RunMenuCommand
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306505"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="2927d-102">Макрокоманда RunMenuCommand</span><span class="sxs-lookup"><span data-stu-id="2927d-102">RunMenuCommand macro action</span></span>

<span data-ttu-id="2927d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2927d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2927d-104">Вы можете использовать действие **RunMenuCommand** для запуска встроенной команды Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2927d-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="2927d-105">Setting</span><span class="sxs-lookup"><span data-stu-id="2927d-105">Setting</span></span>

<span data-ttu-id="2927d-106">Действие **RunMenuCommand** имеет следующий аргумент действия.</span><span class="sxs-lookup"><span data-stu-id="2927d-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2927d-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2927d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2927d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2927d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2927d-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="2927d-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="2927d-110">Имя команды, которая будет запускаться.</span><span class="sxs-lookup"><span data-stu-id="2927d-110">The name of the command you want to run.</span></span> <span data-ttu-id="2927d-111">В <strong>поле</strong> команд показаны доступные встроенные команды в Access в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="2927d-111">The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order.</span></span> <span data-ttu-id="2927d-112">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="2927d-112">This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="2927d-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="2927d-113">Remarks</span></span>

<span data-ttu-id="2927d-114">С помощью действия **RunMenuCommand** можно выполнить команду Access из настраиваемой панели меню, глобальной панели меню, настраиваемой команды или глобального меню.</span><span class="sxs-lookup"><span data-stu-id="2927d-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="2927d-115">Вы можете использовать действие **RunMenuCommand** в макросах с условными выражениями для запуска команды в зависимости от определенных условий.</span><span class="sxs-lookup"><span data-stu-id="2927d-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>

> [!NOTE]
> <span data-ttu-id="2927d-116">Если **щелкнуть вкладку** "Файл", а затем щелкнуть "Последние", будут показаны последние использованные базы данных. </span><span class="sxs-lookup"><span data-stu-id="2927d-116">Clicking the **File** tab and then clicking **Recent** shows the most recently used databases.</span></span> <span data-ttu-id="2927d-117">Вы можете щелкнуть одну из этих баз данных, а не нажать кнопку **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="2927d-117">You can click one of these databases instead of clicking **Open**.</span></span> <span data-ttu-id="2927d-118">Эти элементы базы данных не отображаются в поле  выпадаемого списка для аргумента Command и недоступны с помощью действия **RunMenuCommand** в макросах.</span><span class="sxs-lookup"><span data-stu-id="2927d-118">These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.</span></span>

<span data-ttu-id="2927d-119">При преобразовании базы данных Access из предыдущей версии Access некоторые команды могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="2927d-119">When you convert an Access database from a previous version of Access, some commands may no longer be available.</span></span> <span data-ttu-id="2927d-120">Команда может быть переименована, перемещена в другое меню или больше недоступна в Access.</span><span class="sxs-lookup"><span data-stu-id="2927d-120">A command may have been renamed, moved to a different menu, or may no longer be available in Access.</span></span> <span data-ttu-id="2927d-121">Действия **DoMenuItem** для таких команд нельзя преобразовать в **действия RunMenuCommand.**</span><span class="sxs-lookup"><span data-stu-id="2927d-121">The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions.</span></span> <span data-ttu-id="2927d-122">При запуске макроса Access отобразит действие **RunMenuCommand** с пустым **аргументом Command** для таких команд.</span><span class="sxs-lookup"><span data-stu-id="2927d-122">When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands.</span></span> <span data-ttu-id="2927d-123">Необходимо изменить макрос и ввести допустимый аргумент команды или удалить действие **RunMenuCommand.**</span><span class="sxs-lookup"><span data-stu-id="2927d-123">You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="2927d-124">Чтобы запустить действие **RunMenuCommand** в модуле Visual Basic для приложений (VBA), используйте метод **RunCommand** объекта **Application.**</span><span class="sxs-lookup"><span data-stu-id="2927d-124">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object.</span></span> <span data-ttu-id="2927d-125">(Это эквивалентно **методу RunCommand** объекта **DoCmd.)**</span><span class="sxs-lookup"><span data-stu-id="2927d-125">(This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

