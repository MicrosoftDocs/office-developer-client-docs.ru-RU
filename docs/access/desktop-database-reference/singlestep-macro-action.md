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
ms.openlocfilehash: c3944b82e656bae7f35ecef89d2e30083832a65b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925130"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="7d0ee-102">Макрокоманда SingleStep</span><span class="sxs-lookup"><span data-stu-id="7d0ee-102">SingleStep macro action</span></span>


<span data-ttu-id="7d0ee-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d0ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d0ee-104">Действие **SingleStep** можно использовать для приостановки выполнения макроса и открыть диалоговое окно **Макроса одним действием** .</span><span class="sxs-lookup"><span data-stu-id="7d0ee-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="7d0ee-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="7d0ee-105">Setting</span></span>

<span data-ttu-id="7d0ee-106">Действие **SingleStep** не имеет каких-либо аргументов.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d0ee-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d0ee-107">Remarks</span></span>

  - <span data-ttu-id="7d0ee-108">Действие **SingleStep** используется для устранения неполадок макрос, не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-108">Use the **SingleStep** action to troubleshoot a macro that is not working properly.</span></span> <span data-ttu-id="7d0ee-109">Можно добавить действие **SingleStep** макрос перед действие, который может быть причина проблемы.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-109">You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem.</span></span> <span data-ttu-id="7d0ee-110">Действие приостанавливает макрос и открывает диалоговое окно **Макроса одним действием** .</span><span class="sxs-lookup"><span data-stu-id="7d0ee-110">The action pauses the macro and opens the **Macro Single Step** dialog box.</span></span> <span data-ttu-id="7d0ee-111">Это диалоговое окно сведения о получена, такие как имя макроса, любого указанного условия, действие имя, аргументы и номер ошибки, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-111">This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable.</span></span> <span data-ttu-id="7d0ee-112">В диалоговом окне нажмите кнопку **Шаг** , чтобы перейти к следующей действия макроса, **Остановите все макросы** для остановки текущего макроса и другие макросы, работающих под управлением или **Продолжить** , чтобы остановить пошаговый и возобновления нормальной работы макроса.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-112">In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

  - <span data-ttu-id="7d0ee-113">Действие **SingleStep** имеет следующий эффект, щелкнув **Один шаг** в группе **Работа** на вкладке **Конструктор** построения макросов.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-113">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder.</span></span> <span data-ttu-id="7d0ee-114">Различие между это и выполнение действия **SingleStep** — это что, выполнив действия, вы можете разместить действие в макросе, точно место одного пошаговое выполнение, чтобы начать.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-114">The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin.</span></span> <span data-ttu-id="7d0ee-115">Таким образом, у вас нет к действию через все предыдущие действия для перехода к вам нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-115">That way, you don't have to step through all the previous actions to get to the one you want to examine.</span></span> <span data-ttu-id="7d0ee-116">С другой стороны Если щелкнуть **Один шаг** в инструменте построения макросов, вам необходимо сделать перед выполнение макроса.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-116">On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro.</span></span> <span data-ttu-id="7d0ee-117">В этом случае пошаговый начинается с первого действия в макрос.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-117">In that case, single stepping begins at the first action in the macro.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7d0ee-118">Если вы пошагово до конца макрос без нажав кнопку <STRONG>Продолжить</STRONG>, единого пошаговое выполнение будет по-прежнему быть фактически окончания макрос.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-118">If you single-step all the way to the end of a macro without clicking <STRONG>Continue</STRONG>, single stepping will still be in effect when the macro ends.</span></span> <span data-ttu-id="7d0ee-119">Все последующие макросов, при запуске будет запускаться в режиме одним действием.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-119">Any subsequent macro you run will start in single step mode.</span></span> <span data-ttu-id="7d0ee-120">Чтобы отключить режим пошагового нажмите кнопку <STRONG>Продолжить</STRONG> в диалоговом окне <STRONG>Макрос одним действием</STRONG> или, с помощью макроса в режиме конструктора, на вкладке <STRONG>Конструктор</STRONG> в группе <STRONG>Сервис</STRONG> нажмите кнопку <STRONG>Один шаг</STRONG> , чтобы он больше не выбран.</span><span class="sxs-lookup"><span data-stu-id="7d0ee-120">To turn off single stepping, either click <STRONG>Continue</STRONG> in the <STRONG>Macro Single Step</STRONG> dialog box, or, with a macro open in Design view, on the <STRONG>Design</STRONG> tab, in the <STRONG>Tools</STRONG> group, click <STRONG>Single Step</STRONG> so that it is no longer selected.</span></span></P>


