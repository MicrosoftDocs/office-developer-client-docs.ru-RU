---
title: Макрокоманда MinimizeWindow
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9f7c4ab535010dc0329673fd04721615f6eb3cd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288885"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="770ca-102">Макрокоманда MinimizeWindow</span><span class="sxs-lookup"><span data-stu-id="770ca-102">MinimizeWindow macro action</span></span>

<span data-ttu-id="770ca-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="770ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="770ca-104">Если Access настроен на использование перекрывающихся окон вместо документов с вкладками, с помощью действия **MinimizeWindow** можно уменьшить активное окно до небольшой строки заголовка в нижней части окна Access.</span><span class="sxs-lookup"><span data-stu-id="770ca-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>

> [!NOTE]
> <span data-ttu-id="770ca-105">Это действие нельзя применить к окнам кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="770ca-105">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="770ca-106">Сведения о том, как повлиять на окна кода, см. в разделе о **свойстве WindowState.**</span><span class="sxs-lookup"><span data-stu-id="770ca-106">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="770ca-107">Setting</span><span class="sxs-lookup"><span data-stu-id="770ca-107">Setting</span></span>

<span data-ttu-id="770ca-108">Действие **MinimizeWindow** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="770ca-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="770ca-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="770ca-109">Remarks</span></span>

<span data-ttu-id="770ca-110">Это действие можно использовать для удаления окна с экрана, оставив объект открытым.</span><span class="sxs-lookup"><span data-stu-id="770ca-110">You can use this action to remove a window from the screen while leaving the object open.</span></span> <span data-ttu-id="770ca-111">Это действие также можно использовать для открытия объекта без отображения его окна.</span><span class="sxs-lookup"><span data-stu-id="770ca-111">You can also use this action to open an object without displaying its window.</span></span> <span data-ttu-id="770ca-112">Чтобы отобразить объект, используйте **действие SelectObject** с действием **MaximizeWindow** или **RestoreWindow.**</span><span class="sxs-lookup"><span data-stu-id="770ca-112">To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action.</span></span> <span data-ttu-id="770ca-113">Действие **RestoreWindow** восстанавливает свернутое окно до предыдущего размера.</span><span class="sxs-lookup"><span data-stu-id="770ca-113">The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="770ca-114">Действие **MinimizeWindow** имеет тот же эффект, что и нажатие кнопки  **"Свернуть"** в правом верхнем углу окна или "Свернуть" в меню "Управление" окна. </span><span class="sxs-lookup"><span data-stu-id="770ca-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="770ca-115">**Советы**</span><span class="sxs-lookup"><span data-stu-id="770ca-115">**Tips**</span></span>

- <span data-ttu-id="770ca-116">Сначала может потребоваться использовать действие **SelectObject,** если нужно свести к минимуму окно, не является активным окном.</span><span class="sxs-lookup"><span data-stu-id="770ca-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

- <span data-ttu-id="770ca-117">Чтобы скрыть области навигации, используйте действие **SelectObject** с аргументом  "Да" в области навигации, а затем используйте действие **MinimizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="770ca-117">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action.</span></span> <span data-ttu-id="770ca-118">Объект, выбранный в **действии SelectObject,** может быть любым объектом в базе данных.</span><span class="sxs-lookup"><span data-stu-id="770ca-118">The object you select in the **SelectObject** action can be any object in the database.</span></span>

- <span data-ttu-id="770ca-119">Вы можете скрыть активное окно, щелкнув   "Управление этим окном" в меню "Вид", а затем щелкнув **"Скрыть".**</span><span class="sxs-lookup"><span data-stu-id="770ca-119">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**.</span></span> <span data-ttu-id="770ca-120">Окно становится невидимым, а не уменьшается до значка.</span><span class="sxs-lookup"><span data-stu-id="770ca-120">Instead of being reduced to an icon, the window becomes invisible.</span></span> <span data-ttu-id="770ca-121">Используйте команду **"Открепить"** в том же меню, чтобы снова появиться окно.</span><span class="sxs-lookup"><span data-stu-id="770ca-121">Use the **Unhide** command on the same menu to make the window reappear.</span></span> <span data-ttu-id="770ca-122">Вы можете использовать действие **RunMenuCommand** для выполнения любой из этих команд из макроса.</span><span class="sxs-lookup"><span data-stu-id="770ca-122">You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

- <span data-ttu-id="770ca-123">Вы также можете использовать **действие SetValue,** чтобы установить свойство **Visible** формы, чтобы скрыть или показать окно формы.</span><span class="sxs-lookup"><span data-stu-id="770ca-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="770ca-124">Чтобы выполнить действие **MinimizeWindow** в модуле Visual Basic для приложений VBA, используйте метод **Minimize** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="770ca-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

