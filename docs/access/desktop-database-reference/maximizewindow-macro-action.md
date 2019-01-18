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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715951"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="bc916-102">Макрокоманда MaximizeWindow</span><span class="sxs-lookup"><span data-stu-id="bc916-102">MaximizeWindow macro action</span></span>

<span data-ttu-id="bc916-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc916-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc916-104">Если доступа настроены на использование перекрывающиеся windows вместо вкладками, можно использовать действие **MaximizeWindow** увеличить размер активного окна, чтобы он заполняет окна клиента.</span><span class="sxs-lookup"><span data-stu-id="bc916-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="bc916-105">Это действие позволит увидеть столько объекта в активном окне ответов.</span><span class="sxs-lookup"><span data-stu-id="bc916-105">This action will allow you to see as much of the object in the active window as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="bc916-106">Это действие не может применяться к windows кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bc916-106">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="bc916-107">Для получения сведений о действиях с кодом windows приведены в разделе свойство **WindowState** .</span><span class="sxs-lookup"><span data-stu-id="bc916-107">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="bc916-108">Setting</span><span class="sxs-lookup"><span data-stu-id="bc916-108">Setting</span></span>

<span data-ttu-id="bc916-109">Действие **MaximizeWindow** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="bc916-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc916-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc916-110">Remarks</span></span>

<span data-ttu-id="bc916-111">Это действие имеет тот же эффект, нажав кнопку **Развернуть** в правом верхнем углу окна или нажав кнопку **Развернуть** в **элемент управления** меню.</span><span class="sxs-lookup"><span data-stu-id="bc916-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="bc916-112">Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого окна.</span><span class="sxs-lookup"><span data-stu-id="bc916-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

> [!TIP]
> - <span data-ttu-id="bc916-113">Может потребоваться **Макрокоманда Если окно, которое требуется развернуть, не является активным** .</span><span class="sxs-lookup"><span data-stu-id="bc916-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>
> - <span data-ttu-id="bc916-114">При развертывании окна в Access все остальные окна также будут развернуты при открытии или переключении на них.</span><span class="sxs-lookup"><span data-stu-id="bc916-114">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them.</span></span> <span data-ttu-id="bc916-115">Тем не менее не развертываются всплывающих форм.</span><span class="sxs-lookup"><span data-stu-id="bc916-115">However, pop-up forms aren't maximized.</span></span> <span data-ttu-id="bc916-116">Форма для сохранения его размер при развертывании других окон, установите его свойство **всплывающее окно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="bc916-116">If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="bc916-117">Чтобы выполнить действие **MaximizeWindow** в Visual Basic для приложений модуль, используйте метод **Развернуть** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="bc916-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

