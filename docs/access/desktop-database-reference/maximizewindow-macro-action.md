---
title: Макрокоманда MaximizeWindow
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289751"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="36791-102">Макрокоманда MaximizeWindow</span><span class="sxs-lookup"><span data-stu-id="36791-102">MaximizeWindow macro action</span></span>

<span data-ttu-id="36791-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36791-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36791-104">Если приложение Access настроено на использование перекрывающихся окон вместо документов с вкладками, можно использовать действие **максимизевиндов** , чтобы увеличить активное окно, чтобы оно заполнило окно Access.</span><span class="sxs-lookup"><span data-stu-id="36791-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="36791-105">Это действие позволит увидеть максимально возможный объем объекта в активном окне.</span><span class="sxs-lookup"><span data-stu-id="36791-105">This action will allow you to see as much of the object in the active window as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="36791-106">Это действие невозможно применить к окнам кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="36791-106">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="36791-107">Сведения о том, как повлиять на окна кода, представлены в разделе свойство **WindowState** .</span><span class="sxs-lookup"><span data-stu-id="36791-107">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="36791-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="36791-108">Setting</span></span>

<span data-ttu-id="36791-109">Макрокоманда **максимизевиндов** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="36791-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="36791-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="36791-110">Remarks</span></span>

<span data-ttu-id="36791-111">Это действие имеет тот же результат, что и нажатие кнопки **развернуть** в правом верхнем углу окна, или с помощью команды **развернуть** **в меню оконного** меню.</span><span class="sxs-lookup"><span data-stu-id="36791-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="36791-112">Вы можете использовать действие **ресторевиндов** для восстановления предыдущего размера развернутого окна.</span><span class="sxs-lookup"><span data-stu-id="36791-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

> [!TIP]
> - <span data-ttu-id="36791-113">Если окно, которое вы хотите развернуть, не является активным, может потребоваться использовать макрокоманду "ВыделитьОбъект" ( **SelectObject** ).</span><span class="sxs-lookup"><span data-stu-id="36791-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>
> - <span data-ttu-id="36791-114">При развертывании окна в Access все остальные окна также размещаются в развернутом состоянии при открытии или переключении на них.</span><span class="sxs-lookup"><span data-stu-id="36791-114">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them.</span></span> <span data-ttu-id="36791-115">Однако всплывающие формы не развернуты.</span><span class="sxs-lookup"><span data-stu-id="36791-115">However, pop-up forms aren't maximized.</span></span> <span data-ttu-id="36791-116">Если вы хотите, чтобы форма состроила свой размер при разворачивании других окон, задайте для свойства **Popup свойство Popup** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="36791-116">If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="36791-117">Чтобы запустить действие **максимизевиндов** в модуле Visual Basic для приложений, используйте метод **Maximize** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="36791-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

