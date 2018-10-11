---
title: RunMenuCommand Macro Action
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481665"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="b45af-102">RunMenuCommand Macro Action</span><span class="sxs-lookup"><span data-stu-id="b45af-102">RunMenuCommand Macro Action</span></span>


<span data-ttu-id="b45af-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b45af-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b45af-104">Действие **RunMenuCommand** можно использовать для выполнения встроенных команды Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b45af-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="b45af-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="b45af-105">Setting</span></span>

<span data-ttu-id="b45af-106">Действие **RunMenuCommand** имеет аргумент следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b45af-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b45af-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b45af-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b45af-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b45af-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b45af-109"><strong>Команда</strong></span><span class="sxs-lookup"><span data-stu-id="b45af-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="b45af-110">Имя команды, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b45af-110">The name of the command you want to run.</span></span> <span data-ttu-id="b45af-111">Поле <strong>команда</strong> отображает доступные встроенными командами в клиенте в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="b45af-111">The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order.</span></span> <span data-ttu-id="b45af-112">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b45af-112">This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b45af-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="b45af-113">Remarks</span></span>

<span data-ttu-id="b45af-114">Действие **RunMenuCommand** можно использовать для выполнения команды Microsoft Access из меню, глобальной строки меню, пользовательского контекстного меню или глобального контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="b45af-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="b45af-115">Действие **RunMenuCommand** можно использовать в макросе с условного выражения для выполнения команды в зависимости от определенных условий.</span><span class="sxs-lookup"><span data-stu-id="b45af-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b45af-116">Перейдите на вкладку <STRONG>файл</STRONG> и затем выбрав <STRONG>последние</STRONG> показывает недавно использованные базы данных.</span><span class="sxs-lookup"><span data-stu-id="b45af-116">Clicking the <STRONG>File</STRONG> tab and then clicking <STRONG>Recent</STRONG> shows the most recently used databases.</span></span> <span data-ttu-id="b45af-117">Можно щелкнуть один из этих баз данных, не нажимая <STRONG>Open</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b45af-117">You can click one of these databases instead of clicking <STRONG>Open</STRONG>.</span></span> <span data-ttu-id="b45af-118">Эти элементы базы данных в поле раскрывающегося списка для аргумента <STRONG>команды</STRONG> не отображаются и не доступны с помощью <STRONG>RunMenuCommand</STRONG> действия в макросе.</span><span class="sxs-lookup"><span data-stu-id="b45af-118">These database items don't appear in the drop-down list box for the <STRONG>Command</STRONG> argument, and aren't available by using the <STRONG>RunMenuCommand</STRONG> action in a macro.</span></span></P>



<span data-ttu-id="b45af-119">При преобразовании базы данных Access из предыдущей версии Access некоторые команды могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="b45af-119">When you convert an Access database from a previous version of Access, some commands may no longer be available.</span></span> <span data-ttu-id="b45af-120">Команда может была переименована, перемещена в другое меню или больше не может быть доступно в клиенте.</span><span class="sxs-lookup"><span data-stu-id="b45af-120">A command may have been renamed, moved to a different menu, or may no longer be available in Access.</span></span> <span data-ttu-id="b45af-121">Действия **DoMenuItem** для таких команд невозможно привести к **RunMenuCommand** действия.</span><span class="sxs-lookup"><span data-stu-id="b45af-121">The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions.</span></span> <span data-ttu-id="b45af-122">При открытии макрос, будет показан действие **RunMenuCommand** с пустым аргумент **команды** для команды.</span><span class="sxs-lookup"><span data-stu-id="b45af-122">When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands.</span></span> <span data-ttu-id="b45af-123">Измените макрос и введите аргумент допустимой команды или удаление **RunMenuCommand** действия.</span><span class="sxs-lookup"><span data-stu-id="b45af-123">You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="b45af-124">Чтобы выполнить действие **RunMenuCommand** в Visual Basic для приложений (VBA) модуль, используйте метод **ВыполнитьКоманду** объекта **приложения** .</span><span class="sxs-lookup"><span data-stu-id="b45af-124">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object.</span></span> <span data-ttu-id="b45af-125">(Это эквивалентно метод **ВыполнитьКоманду** **объекта** .)</span><span class="sxs-lookup"><span data-stu-id="b45af-125">(This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

