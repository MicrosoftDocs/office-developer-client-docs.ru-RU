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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721215"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="64d87-102">Макрокоманда MinimizeWindow</span><span class="sxs-lookup"><span data-stu-id="64d87-102">MinimizeWindow macro action</span></span>

<span data-ttu-id="64d87-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64d87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64d87-104">Если доступа настроены на использование перекрывающиеся windows вместо вкладками, можно использовать действие **MinimizeWindow** для уменьшения активного окна малого заголовка в нижней части окна клиента.</span><span class="sxs-lookup"><span data-stu-id="64d87-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>

> [!NOTE]
> <span data-ttu-id="64d87-105">Это действие не может применяться к windows кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="64d87-105">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="64d87-106">Для получения сведений о действиях с кодом windows приведены в разделе свойство **WindowState** .</span><span class="sxs-lookup"><span data-stu-id="64d87-106">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="64d87-107">Setting</span><span class="sxs-lookup"><span data-stu-id="64d87-107">Setting</span></span>

<span data-ttu-id="64d87-108">Действие **MinimizeWindow** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="64d87-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d87-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="64d87-109">Remarks</span></span>

<span data-ttu-id="64d87-110">Это действие можно использовать для удаления окна на экране, не закрывая объекта.</span><span class="sxs-lookup"><span data-stu-id="64d87-110">You can use this action to remove a window from the screen while leaving the object open.</span></span> <span data-ttu-id="64d87-111">Это действие также можно использовать для открытия объекта без отображения окна.</span><span class="sxs-lookup"><span data-stu-id="64d87-111">You can also use this action to open an object without displaying its window.</span></span> <span data-ttu-id="64d87-112">**Чтобы отобразить объект макрокоманда с действием либо **MaximizeWindow** , либо **RestoreWindow** .**</span><span class="sxs-lookup"><span data-stu-id="64d87-112">To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action.</span></span> <span data-ttu-id="64d87-113">Действие **RestoreWindow** восстанавливает свернутого окна предыдущих размеров.</span><span class="sxs-lookup"><span data-stu-id="64d87-113">The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="64d87-114">Действие **MinimizeWindow** имеет тот же эффект, нажав кнопку « **Свернуть** » в правом верхнем углу окна или нажав кнопку **Свернуть** в **элемент управления** меню.</span><span class="sxs-lookup"><span data-stu-id="64d87-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="64d87-115">\*\*Советы \*\*</span><span class="sxs-lookup"><span data-stu-id="64d87-115">**Tips**</span></span>

- <span data-ttu-id="64d87-116">Вам может потребоваться **Макрокоманда Если окно, которое нужно свернуть, не является активным** .</span><span class="sxs-lookup"><span data-stu-id="64d87-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

- <span data-ttu-id="64d87-117">**Чтобы скрыть область навигации, макрокоманда с в области навигации аргумент значение **Да** и затем использовать действие **MinimizeWindow** .**</span><span class="sxs-lookup"><span data-stu-id="64d87-117">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action.</span></span> <span data-ttu-id="64d87-118">Объект, который вы выбираете в **ВыделитьОбъект** может быть любой объект в базе данных.</span><span class="sxs-lookup"><span data-stu-id="64d87-118">The object you select in the **SelectObject** action can be any object in the database.</span></span>

- <span data-ttu-id="64d87-119">Можно скрыть активного окна, выбрав в меню " **Вид** " **Управление это окно** , выберите команду **Скрыть**.</span><span class="sxs-lookup"><span data-stu-id="64d87-119">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**.</span></span> <span data-ttu-id="64d87-120">Вместо уменьшен до размеров значка окна становится невидимым.</span><span class="sxs-lookup"><span data-stu-id="64d87-120">Instead of being reduced to an icon, the window becomes invisible.</span></span> <span data-ttu-id="64d87-121">Команда **Показать** в меню для убедитесь, что окно снова.</span><span class="sxs-lookup"><span data-stu-id="64d87-121">Use the **Unhide** command on the same menu to make the window reappear.</span></span> <span data-ttu-id="64d87-122">Действие **RunMenuCommand** можно использовать для выполнения любой из этих команд из макроса.</span><span class="sxs-lookup"><span data-stu-id="64d87-122">You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

- <span data-ttu-id="64d87-123">Можно также использовать **ЗадатьЗначение** для установки свойства **Visible** формы, чтобы скрыть или отобразить окна формы.</span><span class="sxs-lookup"><span data-stu-id="64d87-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="64d87-124">Чтобы выполнить действие **MinimizeWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **Свернуть** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="64d87-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

