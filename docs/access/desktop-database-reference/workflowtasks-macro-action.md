---
title: Макрокоманда WorkflowTasks
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306008"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="4e76b-102">Макрокоманда WorkflowTasks</span><span class="sxs-lookup"><span data-stu-id="4e76b-102">WorkflowTasks macro action</span></span>


<span data-ttu-id="4e76b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e76b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e76b-104">Вы можете использовать **действие WorkflowTasks** для отображения **диалогового** окна задачи рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="4e76b-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="4e76b-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="4e76b-105">Setting</span></span>

<span data-ttu-id="4e76b-106">Действие **WorkflowTasks имеет** следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="4e76b-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e76b-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="4e76b-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4e76b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4e76b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e76b-109"><strong>Номер записи</strong></span><span class="sxs-lookup"><span data-stu-id="4e76b-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="4e76b-110">Положение элемента в списке Microsoft SharePoint, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> для второго элемента и так далее.</span><span class="sxs-lookup"><span data-stu-id="4e76b-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="4e76b-111">Вы также можете ввести выражение для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="4e76b-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4e76b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e76b-112">Remarks</span></span>

  - <span data-ttu-id="4e76b-113">Действие **WorkflowTasks** открывает диалоговое окно **Workflow Tasks.**</span><span class="sxs-lookup"><span data-stu-id="4e76b-113">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box.</span></span> <span data-ttu-id="4e76b-114">В этом диалоговом окне отображаются все задачи, доступные для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="4e76b-114">This dialog box displays all tasks that are available for the specified item.</span></span> <span data-ttu-id="4e76b-115">Рабочий процесс должен быть определен для списка в SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="4e76b-115">A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="4e76b-116">Действие **WorkflowTasks** можно использовать только после открытия и выбора связанного списка SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="4e76b-116">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected.</span></span> <span data-ttu-id="4e76b-117">Чтобы открыть и выбрать связанный список, используйте **действие OpenTable.**</span><span class="sxs-lookup"><span data-stu-id="4e76b-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="4e76b-118">Если список уже открыт, выберите действие **SelectObject.**</span><span class="sxs-lookup"><span data-stu-id="4e76b-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="4e76b-119">Действие **WorkflowTasks** имеет тот же эффект, что и щелкнуть правой кнопкой мыши любую ячейку в связанном списке SharePoint Foundation, пока она открыта в представлении таблицы данных, указав на рабочий **процесс,** а затем щелкнув задачи рабочего процесса **.**</span><span class="sxs-lookup"><span data-stu-id="4e76b-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="4e76b-120">Чтобы выполнить **действие WorkflowTasks** в модуле VBA, используйте метод **WorkflowTasks** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="4e76b-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

