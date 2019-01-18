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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726276"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="d2930-102">Макрокоманда SingleStep</span><span class="sxs-lookup"><span data-stu-id="d2930-102">SingleStep macro action</span></span>

<span data-ttu-id="d2930-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2930-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2930-104">Действие **SingleStep** можно использовать для приостановки выполнения макроса и открыть диалоговое окно **Макроса одним действием** .</span><span class="sxs-lookup"><span data-stu-id="d2930-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="d2930-105">Setting</span><span class="sxs-lookup"><span data-stu-id="d2930-105">Setting</span></span>

<span data-ttu-id="d2930-106">Действие **SingleStep** не имеет каких-либо аргументов.</span><span class="sxs-lookup"><span data-stu-id="d2930-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2930-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2930-107">Remarks</span></span>

- <span data-ttu-id="d2930-108">Действие **SingleStep** используется для устранения неполадок макрос, не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="d2930-108">Use the **SingleStep** action to troubleshoot a macro that is not working properly.</span></span> <span data-ttu-id="d2930-109">Можно добавить действие **SingleStep** макрос перед действие, который может быть причина проблемы.</span><span class="sxs-lookup"><span data-stu-id="d2930-109">You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem.</span></span> <span data-ttu-id="d2930-110">Действие приостанавливает макрос и открывает диалоговое окно **Макроса одним действием** .</span><span class="sxs-lookup"><span data-stu-id="d2930-110">The action pauses the macro and opens the **Macro Single Step** dialog box.</span></span> <span data-ttu-id="d2930-111">Это диалоговое окно сведения о получена, такие как имя макроса, любого указанного условия, действие имя, аргументы и номер ошибки, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="d2930-111">This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable.</span></span> <span data-ttu-id="d2930-112">В диалоговом окне нажмите кнопку **Шаг** , чтобы перейти к следующей действия макроса, **Остановите все макросы** для остановки текущего макроса и другие макросы, работающих под управлением или **Продолжить** , чтобы остановить пошаговый и возобновления нормальной работы макроса.</span><span class="sxs-lookup"><span data-stu-id="d2930-112">In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="d2930-113">Действие **SingleStep** имеет следующий эффект, щелкнув **Один шаг** в группе **Работа** на вкладке **Конструктор** построения макросов.</span><span class="sxs-lookup"><span data-stu-id="d2930-113">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder.</span></span> <span data-ttu-id="d2930-114">Различие между это и выполнение действия **SingleStep** — это что, выполнив действия, вы можете разместить действие в макросе, точно место одного пошаговое выполнение, чтобы начать.</span><span class="sxs-lookup"><span data-stu-id="d2930-114">The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin.</span></span> <span data-ttu-id="d2930-115">Таким образом, у вас нет к действию через все предыдущие действия для перехода к вам нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="d2930-115">That way, you don't have to step through all the previous actions to get to the one you want to examine.</span></span> <span data-ttu-id="d2930-116">С другой стороны Если щелкнуть **Один шаг** в инструменте построения макросов, вам необходимо сделать перед выполнение макроса.</span><span class="sxs-lookup"><span data-stu-id="d2930-116">On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro.</span></span> <span data-ttu-id="d2930-117">В этом случае пошаговый начинается с первого действия в макрос.</span><span class="sxs-lookup"><span data-stu-id="d2930-117">In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="d2930-118">Если вы пошагово до конца макрос без нажав кнопку **Продолжить**, единого пошаговое выполнение будет по-прежнему быть фактически окончания макрос.</span><span class="sxs-lookup"><span data-stu-id="d2930-118">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends.</span></span> <span data-ttu-id="d2930-119">Все последующие макросов, при запуске будет запускаться в режиме одним действием.</span><span class="sxs-lookup"><span data-stu-id="d2930-119">Any subsequent macro you run will start in single step mode.</span></span> <span data-ttu-id="d2930-120">Чтобы отключить режим пошагового нажмите кнопку **Продолжить** в диалоговом окне **Макрос одним действием** или, с помощью макроса в режиме конструктора, на вкладке **Конструктор** в группе **Сервис** нажмите кнопку **Один шаг** , чтобы он больше не выбран.</span><span class="sxs-lookup"><span data-stu-id="d2930-120">To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>
