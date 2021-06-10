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
# <a name="singlestep-macro-action"></a><span data-ttu-id="2e1b7-102">Макрокоманда SingleStep</span><span class="sxs-lookup"><span data-stu-id="2e1b7-102">SingleStep macro action</span></span>

<span data-ttu-id="2e1b7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e1b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e1b7-104">Вы можете использовать **действие SingleStep** для приостановки выполнения макроса и открытия диалогового окна **Макрос** один шаг.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="2e1b7-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="2e1b7-105">Setting</span></span>

<span data-ttu-id="2e1b7-106">Действие **SingleStep** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e1b7-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e1b7-107">Remarks</span></span>

- <span data-ttu-id="2e1b7-108">Используйте действие **SingleStep** для устранения неполадок макроса, который не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-108">Use the **SingleStep** action to troubleshoot a macro that is not working properly.</span></span> <span data-ttu-id="2e1b7-109">Действие **SingleStep** можно добавить в макрос незадолго до предполагаемого действия, которое может стать причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-109">You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem.</span></span> <span data-ttu-id="2e1b7-110">Действие приостанавливовка макроса и открывает диалоговое окно **Макрос один** шаг.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-110">The action pauses the macro and opens the **Macro Single Step** dialog box.</span></span> <span data-ttu-id="2e1b7-111">В этом диалоговом окне отображаются сведения о текущем действии макроса, таких как имя макроса, любые заданные условия, имя действия, аргументы и номер ошибки, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-111">This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable.</span></span> <span data-ttu-id="2e1b7-112">В диалоговом окне  можно щелкнуть Шаг, чтобы ступить к следующему действию макроса,  остановить  все макрос, чтобы остановить текущий макрос и все остальные макрос, которые запущены, или Продолжить, чтобы остановить одну шагу и возобновить нормальную работу макроса.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-112">In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="2e1b7-113">Действие **SingleStep имеет** аналогичное действие, как щелкнуть один шаг в группе  **Инструментов** на вкладке **Design** в макростроителье.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-113">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder.</span></span> <span data-ttu-id="2e1b7-114">Разница между этим и запуском действия **SingleStep** заключается в том, что при запуске действия можно разместить действие на макросе точно там, где необходимо начать одноступенчатое действие.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-114">The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin.</span></span> <span data-ttu-id="2e1b7-115">Таким образом, вам не придется проходить все предыдущие действия, чтобы добраться до того, которое необходимо изучить.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-115">That way, you don't have to step through all the previous actions to get to the one you want to examine.</span></span> <span data-ttu-id="2e1b7-116">С другой стороны, при  нажатии единого шага в макросстроителье необходимо сделать это перед запуском макроса.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-116">On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro.</span></span> <span data-ttu-id="2e1b7-117">В этом случае при первом действии на макросе начинается одношаговая шаговая ступень.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-117">In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="2e1b7-118">Если вы один шаг до конца макроса без нажатия **Продолжить,** один шаг по-прежнему будет действовать, когда макрос закончится.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-118">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends.</span></span> <span data-ttu-id="2e1b7-119">Любой последующий макрос, который вы запустите, будет запускаться в режиме одного шага.</span><span class="sxs-lookup"><span data-stu-id="2e1b7-119">Any subsequent macro you run will start in single step mode.</span></span> <span data-ttu-id="2e1b7-120">Чтобы отключить один шаг,  нажмите кнопку Продолжить в диалоговом окне Макрос один шаг или, открыв макрос  в представлении Design, на вкладке Design в группе **Tools** нажмите кнопку Один шаг, чтобы она больше не была выбрана.  </span><span class="sxs-lookup"><span data-stu-id="2e1b7-120">To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>
