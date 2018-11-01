---
title: Действия макроса MaximizeWindow
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 110262c9aee48fc24858150714194953136fa835
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867274"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="cd20a-102">Действия макроса MaximizeWindow</span><span class="sxs-lookup"><span data-stu-id="cd20a-102">MaximizeWindow Macro Action</span></span>


<span data-ttu-id="cd20a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd20a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd20a-104">Если доступа настроены на использование перекрывающиеся windows вместо вкладками, можно использовать действие **MaximizeWindow** увеличить размер активного окна, чтобы он заполняет окна клиента.</span><span class="sxs-lookup"><span data-stu-id="cd20a-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="cd20a-105">Это действие позволит увидеть столько объекта в активном окне ответов.</span><span class="sxs-lookup"><span data-stu-id="cd20a-105">This action will allow you to see as much of the object in the active window as possible.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cd20a-106">Это действие не может применяться к windows кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cd20a-106">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="cd20a-107">Для получения сведений о действиях с кодом windows приведены в разделе свойство <STRONG>WindowState</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="cd20a-107">For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="cd20a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="cd20a-108">Setting</span></span>

<span data-ttu-id="cd20a-109">Действие **MaximizeWindow** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="cd20a-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd20a-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="cd20a-110">Remarks</span></span>

<span data-ttu-id="cd20a-111">Это действие имеет тот же эффект, нажав кнопку **Развернуть** в правом верхнем углу окна или нажав кнопку **Развернуть** в **элемент управления** меню.</span><span class="sxs-lookup"><span data-stu-id="cd20a-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="cd20a-112">Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого окна.</span><span class="sxs-lookup"><span data-stu-id="cd20a-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

<span data-ttu-id="cd20a-113">\*\*Советы \*\*</span><span class="sxs-lookup"><span data-stu-id="cd20a-113">**Tips**</span></span>

  - <span data-ttu-id="cd20a-114">Может потребоваться **Макрокоманда Если окно, которое требуется развернуть, не является активным** .</span><span class="sxs-lookup"><span data-stu-id="cd20a-114">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>

  - <span data-ttu-id="cd20a-115">При развертывании окна в Access все остальные окна также будут развернуты при открытии или переключении на них.</span><span class="sxs-lookup"><span data-stu-id="cd20a-115">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them.</span></span> <span data-ttu-id="cd20a-116">Тем не менее не развертываются всплывающих форм.</span><span class="sxs-lookup"><span data-stu-id="cd20a-116">However, pop-up forms aren't maximized.</span></span> <span data-ttu-id="cd20a-117">Форма для сохранения его размер при развертывании других окон, установите его свойство **всплывающее окно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="cd20a-117">If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="cd20a-118">Чтобы выполнить действие **MaximizeWindow** в Visual Basic для приложений модуль, используйте метод **Развернуть** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="cd20a-118">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

