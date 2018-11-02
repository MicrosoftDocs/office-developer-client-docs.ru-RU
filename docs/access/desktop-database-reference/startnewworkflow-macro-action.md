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
ms.openlocfilehash: ed3c508f4799b2ef1f9939de8ce212ab11833353
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925494"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="6d0aa-102">Макрокоманда StartNewWorkflow</span><span class="sxs-lookup"><span data-stu-id="6d0aa-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="6d0aa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d0aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d0aa-104">Действие **StartNewWorkflow** можно использовать для запуска нового рабочего процесса для элемента в связанном списке Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="6d0aa-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="6d0aa-105">Setting</span></span>

<span data-ttu-id="6d0aa-106">Действие **StartNewWorkflow** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d0aa-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6d0aa-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6d0aa-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6d0aa-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d0aa-109"><strong>Номер записи</strong></span><span class="sxs-lookup"><span data-stu-id="6d0aa-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="6d0aa-110">Положение элемента в списке SharePoint Foundation, начиная с <strong>1</strong> для первого элемента в списке, <strong>2</strong> — для второго элемента, и т. д.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="6d0aa-111">Можно также ввести выражение для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6d0aa-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d0aa-112">Remarks</span></span>

  - <span data-ttu-id="6d0aa-113">Действие **StartNewWorkflow** открывает диалоговое окно **Запуск нового рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="6d0aa-113">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box.</span></span> <span data-ttu-id="6d0aa-114">Это диалоговое окно отображает все рабочие процессы, доступные для заданного элемента.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-114">This dialog box displays all workflows that are available for the specified item.</span></span> <span data-ttu-id="6d0aa-115">Необходимо определить рабочего процесса для списка в Windows SharePoint Services, перед тем как начать с помощью этого действия.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-115">A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="6d0aa-116">Действие **StartNewWorkflow** может использоваться только после того как связанный список SharePoint открыт и выбрано.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-116">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected.</span></span> <span data-ttu-id="6d0aa-117">Чтобы открыть и выберите связанный список, используйте **ОткрытьТаблицу** .</span><span class="sxs-lookup"><span data-stu-id="6d0aa-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="6d0aa-118">**Если список open, макрокоманда выберите его.**</span><span class="sxs-lookup"><span data-stu-id="6d0aa-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="6d0aa-119">Действие **StartNewWorkflow** имеет тот же эффект, что правой кнопкой мыши любую ячейку в связанном списке SharePoint, когда он открыт в представлении таблицы данных, с указанием **рабочего процесса**и затем выбрав **Запуск нового рабочего процесса**.</span><span class="sxs-lookup"><span data-stu-id="6d0aa-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="6d0aa-120">Чтобы выполнить действие **StartNewWorkflow** в модуле VBA, используйте метод **StartNewWorkflow** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="6d0aa-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

