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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698164"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="c776b-102">Макрокоманда RunMenuCommand</span><span class="sxs-lookup"><span data-stu-id="c776b-102">RunMenuCommand macro action</span></span>

<span data-ttu-id="c776b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c776b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c776b-104">Действие **RunMenuCommand** можно использовать для выполнения встроенных команды Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c776b-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="c776b-105">Setting</span><span class="sxs-lookup"><span data-stu-id="c776b-105">Setting</span></span>

<span data-ttu-id="c776b-106">Действие **RunMenuCommand** имеет аргумент следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c776b-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c776b-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="c776b-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c776b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c776b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c776b-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="c776b-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="c776b-110">Имя команды, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="c776b-110">The name of the command you want to run.</span></span> <span data-ttu-id="c776b-111">Поле <strong>команда</strong> отображает доступные встроенными командами в клиенте в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="c776b-111">The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order.</span></span> <span data-ttu-id="c776b-112">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="c776b-112">This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="c776b-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c776b-113">Remarks</span></span>

<span data-ttu-id="c776b-114">Действие **RunMenuCommand** можно использовать для выполнения команды Microsoft Access из меню, глобальной строки меню, пользовательского контекстного меню или глобального контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="c776b-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="c776b-115">Действие **RunMenuCommand** можно использовать в макросе с условного выражения для выполнения команды в зависимости от определенных условий.</span><span class="sxs-lookup"><span data-stu-id="c776b-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>

> [!NOTE]
> <span data-ttu-id="c776b-116">Перейдите на вкладку **файл** и затем выбрав **последние** показывает недавно использованные базы данных.</span><span class="sxs-lookup"><span data-stu-id="c776b-116">Clicking the **File** tab and then clicking **Recent** shows the most recently used databases.</span></span> <span data-ttu-id="c776b-117">Можно щелкнуть один из этих баз данных, не нажимая **Open**.</span><span class="sxs-lookup"><span data-stu-id="c776b-117">You can click one of these databases instead of clicking **Open**.</span></span> <span data-ttu-id="c776b-118">Эти элементы базы данных в поле раскрывающегося списка для аргумента **команды** не отображаются и не доступны с помощью **RunMenuCommand** действия в макросе.</span><span class="sxs-lookup"><span data-stu-id="c776b-118">These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.</span></span>

<span data-ttu-id="c776b-119">При преобразовании базы данных Access из предыдущей версии Access некоторые команды могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="c776b-119">When you convert an Access database from a previous version of Access, some commands may no longer be available.</span></span> <span data-ttu-id="c776b-120">Команда может была переименована, перемещена в другое меню или больше не может быть доступно в клиенте.</span><span class="sxs-lookup"><span data-stu-id="c776b-120">A command may have been renamed, moved to a different menu, or may no longer be available in Access.</span></span> <span data-ttu-id="c776b-121">Действия **DoMenuItem** для таких команд невозможно привести к **RunMenuCommand** действия.</span><span class="sxs-lookup"><span data-stu-id="c776b-121">The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions.</span></span> <span data-ttu-id="c776b-122">При открытии макрос, будет показан действие **RunMenuCommand** с пустым аргумент **команды** для команды.</span><span class="sxs-lookup"><span data-stu-id="c776b-122">When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands.</span></span> <span data-ttu-id="c776b-123">Измените макрос и введите аргумент допустимой команды или удаление **RunMenuCommand** действия.</span><span class="sxs-lookup"><span data-stu-id="c776b-123">You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="c776b-124">Чтобы выполнить действие **RunMenuCommand** в Visual Basic для приложений (VBA) модуль, используйте метод **ВыполнитьКоманду** объекта **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c776b-124">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object.</span></span> <span data-ttu-id="c776b-125">(Это эквивалентно метод **ВыполнитьКоманду** **объекта** .)</span><span class="sxs-lookup"><span data-stu-id="c776b-125">(This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

