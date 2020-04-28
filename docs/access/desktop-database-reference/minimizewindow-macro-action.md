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
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="81ead-102">Макрокоманда MinimizeWindow</span><span class="sxs-lookup"><span data-stu-id="81ead-102">MinimizeWindow macro action</span></span>

<span data-ttu-id="81ead-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81ead-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81ead-104">Если в Access настроено использование перекрывающихся окон вместо документов с вкладками, можно использовать действие **минимизевиндов** , чтобы уменьшить активное окно до маленькой строки заголовка в нижней части окна Access.</span><span class="sxs-lookup"><span data-stu-id="81ead-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>

> [!NOTE]
> <span data-ttu-id="81ead-105">Это действие невозможно применить к окнам кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="81ead-105">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="81ead-106">Сведения о том, как повлиять на окна кода, представлены в разделе свойство **WindowState** .</span><span class="sxs-lookup"><span data-stu-id="81ead-106">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="81ead-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="81ead-107">Setting</span></span>

<span data-ttu-id="81ead-108">Макрокоманда **минимизевиндов** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="81ead-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ead-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="81ead-109">Remarks</span></span>

<span data-ttu-id="81ead-110">С помощью этого действия можно удалить окно с экрана, оставив объект открытым.</span><span class="sxs-lookup"><span data-stu-id="81ead-110">You can use this action to remove a window from the screen while leaving the object open.</span></span> <span data-ttu-id="81ead-111">Вы также можете использовать это действие, чтобы открыть объект без отображения его окна.</span><span class="sxs-lookup"><span data-stu-id="81ead-111">You can also use this action to open an object without displaying its window.</span></span> <span data-ttu-id="81ead-112">Чтобы отобразить объект, используйте макрокоманду **ВыделитьОбъект** с действием **максимизевиндов** или **ресторевиндов** .</span><span class="sxs-lookup"><span data-stu-id="81ead-112">To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action.</span></span> <span data-ttu-id="81ead-113">Действие **ресторевиндов** Восстанавливает свернутое окно до его предыдущего размера.</span><span class="sxs-lookup"><span data-stu-id="81ead-113">The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="81ead-114">Действие **минимизевиндов** имеет тот же результат, что и нажатие кнопки **свертывания** в правом верхнем углу окна, или при нажатии кнопки **Свернуть** в **оконном меню окна** .</span><span class="sxs-lookup"><span data-stu-id="81ead-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="81ead-115">**Советы**</span><span class="sxs-lookup"><span data-stu-id="81ead-115">**Tips**</span></span>

- <span data-ttu-id="81ead-116">Если окно, которое нужно свернуть, не является активным, может потребоваться использовать макрокоманду "ВыделитьОбъект" ( **SelectObject** ).</span><span class="sxs-lookup"><span data-stu-id="81ead-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

- <span data-ttu-id="81ead-117">Чтобы скрыть область навигации, используйте макрокоманду "ВыделитьОбъект" ( **SelectObject** ) с параметром в разделе в области навигации, равным **Да** , а затем используйте действие **минимизевиндов** .</span><span class="sxs-lookup"><span data-stu-id="81ead-117">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action.</span></span> <span data-ttu-id="81ead-118">Объект, выбранный в действии **ВыделитьОбъект** , может быть любым объектом в базе данных.</span><span class="sxs-lookup"><span data-stu-id="81ead-118">The object you select in the **SelectObject** action can be any object in the database.</span></span>

- <span data-ttu-id="81ead-119">Чтобы скрыть активное окно, щелкните **Управление этим окном** в меню **вид** , а затем выберите команду **Скрыть**.</span><span class="sxs-lookup"><span data-stu-id="81ead-119">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**.</span></span> <span data-ttu-id="81ead-120">Вместо того чтобы уменьшаться до значка, окно становится невидимым.</span><span class="sxs-lookup"><span data-stu-id="81ead-120">Instead of being reduced to an icon, the window becomes invisible.</span></span> <span data-ttu-id="81ead-121">Чтобы вновь отобразить окно, используйте команду **отобразить** в том же меню.</span><span class="sxs-lookup"><span data-stu-id="81ead-121">Use the **Unhide** command on the same menu to make the window reappear.</span></span> <span data-ttu-id="81ead-122">Вы можете использовать действие **Макрокоманда runmenucommand** для выполнения любой из этих команд из макроса.</span><span class="sxs-lookup"><span data-stu-id="81ead-122">You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

- <span data-ttu-id="81ead-123">Вы также можете использовать действие **SetValue** , чтобы задать свойство **Visible** формы для скрытия или отображения окна формы.</span><span class="sxs-lookup"><span data-stu-id="81ead-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="81ead-124">Чтобы запустить действие **минимизевиндов** в модуле Visual Basic для приложений (VBA), используйте метод **сворачивания** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="81ead-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

