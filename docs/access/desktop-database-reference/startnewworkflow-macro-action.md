---
title: Макрокоманда StartNewWorkflow
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1e37d72754531fc4dd51427eefb355a057d08073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306400"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="04057-102">Макрокоманда StartNewWorkflow</span><span class="sxs-lookup"><span data-stu-id="04057-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="04057-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04057-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04057-104">С помощью действия **StartNewWorkflow** можно запустить новый рабочий процесс для элемента в связанном списке Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="04057-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="04057-105">Setting</span><span class="sxs-lookup"><span data-stu-id="04057-105">Setting</span></span>

<span data-ttu-id="04057-106">Действие **StartNewWorkflow** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="04057-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04057-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="04057-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="04057-108">Описание</span><span class="sxs-lookup"><span data-stu-id="04057-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04057-109"><strong>Номер записи</strong></span><span class="sxs-lookup"><span data-stu-id="04057-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="04057-110">Положение элемента в списке SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> для второго элемента и так далее.</span><span class="sxs-lookup"><span data-stu-id="04057-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="04057-111">Вы также можете ввести выражение для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="04057-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="04057-112">Заметки</span><span class="sxs-lookup"><span data-stu-id="04057-112">Remarks</span></span>

  - <span data-ttu-id="04057-113">Действие **StartNewWorkflow** открывает диалоговое окно **"Начать** новый рабочий процесс".</span><span class="sxs-lookup"><span data-stu-id="04057-113">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box.</span></span> <span data-ttu-id="04057-114">В этом диалоговом окне отображаются все доступные для указанного элемента процессы.</span><span class="sxs-lookup"><span data-stu-id="04057-114">This dialog box displays all workflows that are available for the specified item.</span></span> <span data-ttu-id="04057-115">Рабочий процесс должен быть определен для списка в SharePoint Foundation, прежде чем можно будет запустить его с помощью этого действия.</span><span class="sxs-lookup"><span data-stu-id="04057-115">A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="04057-116">Действие **StartNewWorkflow** можно использовать только после открытия и выбора связанного списка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="04057-116">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected.</span></span> <span data-ttu-id="04057-117">Чтобы открыть и выбрать связанный список, используйте действие **OpenTable.**</span><span class="sxs-lookup"><span data-stu-id="04057-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="04057-118">Если список уже открыт, выберите его с помощью действия **SelectObject.**</span><span class="sxs-lookup"><span data-stu-id="04057-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="04057-119">Действие **StartNewWorkflow** имеет тот же эффект, что и щелчок правой кнопкой мыши любую ячейку в связанном списке SharePoint, когда она открыта в представлении таблицы, указывая на рабочий **процесс,** а затем щелкнув "Начать новый рабочий процесс". </span><span class="sxs-lookup"><span data-stu-id="04057-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="04057-120">Чтобы запустить действие **StartNewWorkflow** в модуле VBA, используйте метод **StartNewWorkflow** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="04057-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

