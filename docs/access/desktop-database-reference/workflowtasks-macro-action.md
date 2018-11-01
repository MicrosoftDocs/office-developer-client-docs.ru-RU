---
title: Действия макроса WorkflowTasks
TOCTitle: WorkflowTasks Macro Action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1bbb04600dc6f7ecea4ce9084b146d3bf696cd6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878124"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="0c0ef-102">Действия макроса WorkflowTasks</span><span class="sxs-lookup"><span data-stu-id="0c0ef-102">WorkflowTasks Macro Action</span></span>


<span data-ttu-id="0c0ef-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c0ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c0ef-104">Чтобы открыть диалоговое окно **Задачи рабочего процесса** можно использовать действие **WorkflowTasks** .</span><span class="sxs-lookup"><span data-stu-id="0c0ef-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="0c0ef-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="0c0ef-105">Setting</span></span>

<span data-ttu-id="0c0ef-106">Действие **WorkflowTasks** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c0ef-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="0c0ef-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0c0ef-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0c0ef-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c0ef-109"><strong>Номер записи</strong></span><span class="sxs-lookup"><span data-stu-id="0c0ef-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="0c0ef-110">Положение элемента в списке Microsoft SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> — для второго элемента, и т. д.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="0c0ef-111">Можно также ввести выражение для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0c0ef-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="0c0ef-112">Remarks</span></span>

  - <span data-ttu-id="0c0ef-113">Действие **WorkflowTasks** открывает диалоговое окно **Задачи рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="0c0ef-113">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box.</span></span> <span data-ttu-id="0c0ef-114">Это диалоговое окно отображает все задачи, доступные для заданного элемента.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-114">This dialog box displays all tasks that are available for the specified item.</span></span> <span data-ttu-id="0c0ef-115">Рабочий процесс необходимо определить для списка в Windows SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-115">A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="0c0ef-116">Действие **WorkflowTasks** может использоваться только после того как связанный список SharePoint Foundation открывается и выбран.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-116">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected.</span></span> <span data-ttu-id="0c0ef-117">Чтобы открыть и выберите связанный список, используйте **ОткрытьТаблицу** .</span><span class="sxs-lookup"><span data-stu-id="0c0ef-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="0c0ef-118">**Если список open, макрокоманда выберите его.**</span><span class="sxs-lookup"><span data-stu-id="0c0ef-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="0c0ef-119">Действие **WorkflowTasks** имеет тот же эффект, как правой кнопкой мыши любую ячейку в связанном списке SharePoint Foundation, когда он открыт в представлении таблицы данных, с указанием **рабочего процесса**и затем выбрав **Задачи рабочего процесса**.</span><span class="sxs-lookup"><span data-stu-id="0c0ef-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="0c0ef-120">Чтобы выполнить действие **WorkflowTasks** в модуле VBA, используйте метод **WorkflowTasks** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="0c0ef-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

