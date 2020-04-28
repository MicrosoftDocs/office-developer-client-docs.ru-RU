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
# <a name="singlestep-macro-action"></a><span data-ttu-id="63f8e-102">Макрокоманда SingleStep</span><span class="sxs-lookup"><span data-stu-id="63f8e-102">SingleStep macro action</span></span>

<span data-ttu-id="63f8e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63f8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63f8e-104">Вы можете приостановить выполнение макроса с помощью действия **Макрокоманда singlestep** и открыть диалоговое окно **макроса с одним действием** .</span><span class="sxs-lookup"><span data-stu-id="63f8e-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="63f8e-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="63f8e-105">Setting</span></span>

<span data-ttu-id="63f8e-106">Действие **Макрокоманда singlestep** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="63f8e-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="63f8e-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="63f8e-107">Remarks</span></span>

- <span data-ttu-id="63f8e-108">Используйте действие **Макрокоманда singlestep** для устранения неполадок в макросе, который работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="63f8e-108">Use the **SingleStep** action to troubleshoot a macro that is not working properly.</span></span> <span data-ttu-id="63f8e-109">Вы можете добавить действие **Макрокоманда singlestep** в макрос непосредственно перед действием, которое может стать причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="63f8e-109">You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem.</span></span> <span data-ttu-id="63f8e-110">Действие приостанавливает выполнение макроса и открывает диалоговое окно **макроса с одним действием** .</span><span class="sxs-lookup"><span data-stu-id="63f8e-110">The action pauses the macro and opens the **Macro Single Step** dialog box.</span></span> <span data-ttu-id="63f8e-111">В этом диалоговом окне отображаются сведения о текущем действии макроса, такие как имя макроса, все указанные условия, имя действия, аргументы и номер ошибки (если это требуется).</span><span class="sxs-lookup"><span data-stu-id="63f8e-111">This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable.</span></span> <span data-ttu-id="63f8e-112">В диалоговом окне можно нажать кнопку **Step (шаг** ), чтобы перейти к следующему макрокоманде, **остановить все макросы** , чтобы остановить текущий макрос и другие выполняемые макросы, либо **продолжить** работу с одним степпингом и возобновить нормальную работу макроса.</span><span class="sxs-lookup"><span data-stu-id="63f8e-112">In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="63f8e-113">Действие **Макрокоманда singlestep** аналогично нажатию **одного шага** в группе " **инструменты** " на вкладке " **конструктор** " в построителе макросов.</span><span class="sxs-lookup"><span data-stu-id="63f8e-113">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder.</span></span> <span data-ttu-id="63f8e-114">Разница между выполнением этого действия и выполнением действия **Макрокоманда singlestep** заключается в том, что это действие можно выполнить в макросе именно в том месте, где необходимо начать с одной пошаговой отладки.</span><span class="sxs-lookup"><span data-stu-id="63f8e-114">The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin.</span></span> <span data-ttu-id="63f8e-115">Таким образом, вам не нужно будет выполнять все предыдущие действия, чтобы перейти к тому, которую вы хотите проверить.</span><span class="sxs-lookup"><span data-stu-id="63f8e-115">That way, you don't have to step through all the previous actions to get to the one you want to examine.</span></span> <span data-ttu-id="63f8e-116">С другой стороны, если щелкнуть **один шаг** в построителе макросов, необходимо сделать это до запуска макроса.</span><span class="sxs-lookup"><span data-stu-id="63f8e-116">On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro.</span></span> <span data-ttu-id="63f8e-117">В этом случае однократное выполнение начинается с первого действия в макросе.</span><span class="sxs-lookup"><span data-stu-id="63f8e-117">In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="63f8e-118">Если вы единственный шаг до конца макроса, не нажимая кнопку **продолжить**, по-прежнему будет действовать действие по одному степпингу при завершении макроса.</span><span class="sxs-lookup"><span data-stu-id="63f8e-118">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends.</span></span> <span data-ttu-id="63f8e-119">Все последующие выполняемые макросы будут запущены в режиме с одним шагом.</span><span class="sxs-lookup"><span data-stu-id="63f8e-119">Any subsequent macro you run will start in single step mode.</span></span> <span data-ttu-id="63f8e-120">Чтобы отключить пошаговое выполнение, нажмите кнопку **продолжить** в диалоговом окне **макрос одного этапа** или, если макрос открыт в режиме конструктора, на вкладке **конструктор** в группе **Сервис** выберите **один шаг** , чтобы он больше не выбирался.</span><span class="sxs-lookup"><span data-stu-id="63f8e-120">To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>
