---
title: Макрокоманда SingleStep
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e934b290472dc4bb0ad8619b2ada6992b4215c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308633"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="b6beb-102">Макрокоманда SingleStep</span><span class="sxs-lookup"><span data-stu-id="b6beb-102">SingleStep macro action</span></span>

<span data-ttu-id="b6beb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6beb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6beb-104">С помощью действия **SingleStep можно** приостановить  выполнение макроса и открыть диалоговое окно "Один шаг макроса".</span><span class="sxs-lookup"><span data-stu-id="b6beb-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="b6beb-105">Setting</span><span class="sxs-lookup"><span data-stu-id="b6beb-105">Setting</span></span>

<span data-ttu-id="b6beb-106">Действие **SingleStep** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="b6beb-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6beb-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="b6beb-107">Remarks</span></span>

- <span data-ttu-id="b6beb-108">Используйте действие **SingleStep** для устранения неполадок макроса, который работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b6beb-108">Use the **SingleStep** action to troubleshoot a macro that is not working properly.</span></span> <span data-ttu-id="b6beb-109">Действие **SingleStep можно** добавить в макрос сразу перед действием, которое, как вы подозреваете, может стать причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="b6beb-109">You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem.</span></span> <span data-ttu-id="b6beb-110">Действие приостановит макрос и откроет диалоговое окно **"Один** шаг макроса".</span><span class="sxs-lookup"><span data-stu-id="b6beb-110">The action pauses the macro and opens the **Macro Single Step** dialog box.</span></span> <span data-ttu-id="b6beb-111">В этом диалоговом окне отображаются сведения о текущем макрокомене, например имя макроса, все указанные условия, имя действия, аргументы и номер ошибки, если применимо.</span><span class="sxs-lookup"><span data-stu-id="b6beb-111">This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable.</span></span> <span data-ttu-id="b6beb-112">В диалоговом окне  можно щелкнуть "Шаг", чтобы ступить к следующему макроу действию,   остановить все макрос, чтобы остановить текущий макрос и все остальные запущенные макрос, или продолжить пошаговое действие и возобновить обычную работу макроса.</span><span class="sxs-lookup"><span data-stu-id="b6beb-112">In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="b6beb-113">Действие **SingleStep** аналогично нажатию кнопки **"Один** шаг"  в группе "Инструменты" на вкладке "Конструктор" построитель макроса. </span><span class="sxs-lookup"><span data-stu-id="b6beb-113">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder.</span></span> <span data-ttu-id="b6beb-114">Разница между этим и запуском действия **SingleStep** заключается в том, что при запуске действия можно разместить действие в макросе именно там, где нужно начать одну пошаговую работу.</span><span class="sxs-lookup"><span data-stu-id="b6beb-114">The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin.</span></span> <span data-ttu-id="b6beb-115">Таким образом, вам не придется пошаговую проверку всех предыдущих действий, чтобы ступить к нужному действию.</span><span class="sxs-lookup"><span data-stu-id="b6beb-115">That way, you don't have to step through all the previous actions to get to the one you want to examine.</span></span> <span data-ttu-id="b6beb-116">С другой стороны, при нажатии кнопки **"Один** шаг" в построителье макроса это необходимо сделать перед запуском макроса.</span><span class="sxs-lookup"><span data-stu-id="b6beb-116">On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro.</span></span> <span data-ttu-id="b6beb-117">В этом случае одна пошаговая</span><span class="sxs-lookup"><span data-stu-id="b6beb-117">In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="b6beb-118">Если вы на один шаг до конца макроса без нажатия кнопки "Продолжить", пошаговая по-прежнему будет действовать после окончания макроса.</span><span class="sxs-lookup"><span data-stu-id="b6beb-118">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends.</span></span> <span data-ttu-id="b6beb-119">Любой последующий макрос будет запускаться в режиме одного шага.</span><span class="sxs-lookup"><span data-stu-id="b6beb-119">Any subsequent macro you run will start in single step mode.</span></span> <span data-ttu-id="b6beb-120">Чтобы отключить одну пошаговую  пошаговую пошаговую работу, нажмите кнопку "Продолжить"  в диалоговом окне "Один шаг макроса" или, открыв макрос в представлении конструктора, на вкладке "Конструктор" в группе "Инструменты" щелкните "Один шаг", чтобы он больше не был выбран.   </span><span class="sxs-lookup"><span data-stu-id="b6beb-120">To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>
