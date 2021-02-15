---
title: Макрокоманда SetOrderBy
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 86834cd8b6132e8939067c0e34037ca1b0ef8bad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314611"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="8b220-102">Макрокоманда SetOrderBy</span><span class="sxs-lookup"><span data-stu-id="8b220-102">SetOrderBy macro action</span></span>


<span data-ttu-id="8b220-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b220-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b220-104">С помощью действия **SetOrderBy** можно указать, как нужно сортировать записи в форме, отчете, таблице или результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="8b220-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="8b220-105">Setting</span><span class="sxs-lookup"><span data-stu-id="8b220-105">Setting</span></span>

<span data-ttu-id="8b220-106">Действие **SetOrderBy** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8b220-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b220-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="8b220-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8b220-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8b220-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b220-109"><strong>Order By</strong></span><span class="sxs-lookup"><span data-stu-id="8b220-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="8b220-110">Строка выражения, которая включает имя поля или полей, по которым необходимо сортировать записи, и необязательные ключевые слова ASC или DESC.</span><span class="sxs-lookup"><span data-stu-id="8b220-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b220-111"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="8b220-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8b220-112">Если этот объект предоставлен, а активный объект является формой или отчетом, имя этого средства управления соответствует подформе или в подотряду, которые будут отсортироваться.</span><span class="sxs-lookup"><span data-stu-id="8b220-112">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted.</span></span> <span data-ttu-id="8b220-113">Если пустой объект и активный объект является формой или отчетом, родительская форма или отчет сортироваться.</span><span class="sxs-lookup"><span data-stu-id="8b220-113">If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8b220-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="8b220-114">Remarks</span></span>

<span data-ttu-id="8b220-115">При запуске этого макроса сортировка применяется к таблице, форме, отчету или таблице (результат запроса), которая активна и находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="8b220-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="8b220-116">Аргумент Order By — это имя поля или полей, по которым необходимо сортировать записи.</span><span class="sxs-lookup"><span data-stu-id="8b220-116">The Order By argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="8b220-117">При использовании более одного имени поля разделять их запятой (,).</span><span class="sxs-lookup"><span data-stu-id="8b220-117">When you use more than one field name, separate the names with a comma (,).</span></span> <span data-ttu-id="8b220-118">Свойство **OrderBy** активного объекта используется для сохранения упорядоченного значения и его применения позже.</span><span class="sxs-lookup"><span data-stu-id="8b220-118">The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time.</span></span> <span data-ttu-id="8b220-119">Значения OrderBy сохраняются вместе с объектами, в которых они создаются.</span><span class="sxs-lookup"><span data-stu-id="8b220-119">OrderBy values are saved with the objects in which they are created.</span></span> <span data-ttu-id="8b220-120">Они автоматически загружаются при открытом объекте, но не применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="8b220-120">They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="8b220-121">Когда вы установите аргумент Order By, введите одно или несколько имен полей, а затем запустите макрос, записи сортироваться по умолчанию в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="8b220-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="8b220-122">Чтобы отсортировать записи в порядке убывления, введите DESC в конце выражения аргумента Order By.</span><span class="sxs-lookup"><span data-stu-id="8b220-122">To sort records in descending order, type DESC at the end of the Order By argument expression.</span></span> <span data-ttu-id="8b220-123">Например, чтобы отсортировать записи клиентов по убываемой порядку по имени контакта, установите для аргумента Order By "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="8b220-123">For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC".</span></span> <span data-ttu-id="8b220-124">Чтобы отсортировать имена по убыванию LastName и FirstName по возрастанию, установите для аргумента Order By "LastName DESC, FirstName ASC".</span><span class="sxs-lookup"><span data-stu-id="8b220-124">To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

