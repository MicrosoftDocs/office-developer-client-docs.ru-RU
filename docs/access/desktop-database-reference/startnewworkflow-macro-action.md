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
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="70dd5-102">Макрокоманда StartNewWorkflow</span><span class="sxs-lookup"><span data-stu-id="70dd5-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="70dd5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70dd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70dd5-104">Вы можете использовать действие **Макрокоманда startnewworkflow** для запуска нового рабочего процесса для элемента в связанном списке Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="70dd5-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="70dd5-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="70dd5-105">Setting</span></span>

<span data-ttu-id="70dd5-106">Действие **Макрокоманда startnewworkflow** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="70dd5-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70dd5-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="70dd5-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="70dd5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="70dd5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70dd5-109"><strong>Номер записи</strong></span><span class="sxs-lookup"><span data-stu-id="70dd5-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="70dd5-110">Положение элемента в списке SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> для второго элемента и т. д.</span><span class="sxs-lookup"><span data-stu-id="70dd5-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="70dd5-111">Вы также можете ввести выражение для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="70dd5-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="70dd5-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="70dd5-112">Remarks</span></span>

  - <span data-ttu-id="70dd5-113">Действие **Макрокоманда startnewworkflow** открывает диалоговое окно " **запустить новый рабочий процесс** ".</span><span class="sxs-lookup"><span data-stu-id="70dd5-113">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box.</span></span> <span data-ttu-id="70dd5-114">В этом диалоговом окне отображаются все рабочие процессы, доступные для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="70dd5-114">This dialog box displays all workflows that are available for the specified item.</span></span> <span data-ttu-id="70dd5-115">Перед запуском этого действия в списке в SharePoint Foundation необходимо определить рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="70dd5-115">A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="70dd5-116">Действие **Макрокоманда startnewworkflow** можно использовать только после открытия и выбора связанного списка SharePoint.</span><span class="sxs-lookup"><span data-stu-id="70dd5-116">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected.</span></span> <span data-ttu-id="70dd5-117">Чтобы открыть и выбрать связанный список, используйте действие **опентабле** .</span><span class="sxs-lookup"><span data-stu-id="70dd5-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="70dd5-118">Если список уже открыт, используйте макрокоманду " **ВыделитьОбъект** " (ВыделитьОбъект), чтобы выбрать ее.</span><span class="sxs-lookup"><span data-stu-id="70dd5-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="70dd5-119">Действие **Макрокоманда startnewworkflow** имеет тот же результат, что и щелчок правой кнопкой мыши по любой ячейке в связанном списке SharePoint, когда она открыта в режиме таблицы, указывает на **Рабочий процесс**, а затем **запускает команду Запустить новый рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="70dd5-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="70dd5-120">Чтобы выполнить действие **Макрокоманда startnewworkflow** в модуле VBA, используйте метод **Макрокоманда startnewworkflow** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="70dd5-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

