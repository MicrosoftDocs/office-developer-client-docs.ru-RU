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
# <a name="setorderby-macro-action"></a><span data-ttu-id="ddb16-102">Макрокоманда SetOrderBy</span><span class="sxs-lookup"><span data-stu-id="ddb16-102">SetOrderBy macro action</span></span>


<span data-ttu-id="ddb16-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ddb16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ddb16-104">Вы можете использовать действие **сетордерби** , чтобы указать, как следует сортировать записи в форме, отчете, таблице или результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="ddb16-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="ddb16-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="ddb16-105">Setting</span></span>

<span data-ttu-id="ddb16-106">Макрокоманда **сетордерби** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ddb16-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ddb16-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="ddb16-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ddb16-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ddb16-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddb16-109"><strong>ORDER BY</strong></span><span class="sxs-lookup"><span data-stu-id="ddb16-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="ddb16-110">Строковое выражение, включающее имя поля или полей, по которым сортируются записи, а также необязательные ключевые слова ASC и DESC.</span><span class="sxs-lookup"><span data-stu-id="ddb16-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddb16-111"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="ddb16-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ddb16-112">Если этот параметр указан и активный объект является формой или отчетом, имя элемента управления, соответствующего подформе или вложенному отчету, который будет отсортирован.</span><span class="sxs-lookup"><span data-stu-id="ddb16-112">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted.</span></span> <span data-ttu-id="ddb16-113">Если этот объект пуст, а активный объект является формой или отчетом, сортируется родительская форма или отчет...</span><span class="sxs-lookup"><span data-stu-id="ddb16-113">If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ddb16-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ddb16-114">Remarks</span></span>

<span data-ttu-id="ddb16-115">При выполнении этого макроса сортировка применяется к таблице, форме, отчету или таблице (результат запроса), которая активна и имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="ddb16-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="ddb16-116">Аргумент ORDER BY — это имя поля или полей, для которых требуется отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="ddb16-116">The Order By argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="ddb16-117">При использовании нескольких имен полей разделяйте их запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="ddb16-117">When you use more than one field name, separate the names with a comma (,).</span></span> <span data-ttu-id="ddb16-118">Свойство **OrderBy** активного объекта используется для сохранения значения упорядочения и его применения в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="ddb16-118">The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time.</span></span> <span data-ttu-id="ddb16-119">Значения OrderBy сохраняются вместе с объектами, в которых они созданы.</span><span class="sxs-lookup"><span data-stu-id="ddb16-119">OrderBy values are saved with the objects in which they are created.</span></span> <span data-ttu-id="ddb16-120">Они автоматически загружаются при открытии объекта, но не применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="ddb16-120">They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="ddb16-121">При задании аргумента ORDER BY путем ввода одного или нескольких имен полей и запуска макроса записи сортируются по умолчанию в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="ddb16-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="ddb16-122">Чтобы отсортировать записи в убывающем порядке, введите DESC в конце выражения ORDER BY аргумента ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="ddb16-122">To sort records in descending order, type DESC at the end of the Order By argument expression.</span></span> <span data-ttu-id="ddb16-123">Например, чтобы отсортировать записи клиентов по убыванию по имени контакта, задайте для аргумента ORDER BY значение "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="ddb16-123">For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC".</span></span> <span data-ttu-id="ddb16-124">Для сортировки имен по убыванию и по возрастанию задайте для аргумента ORDER BY значение "фамилия DESC, имя ASC".</span><span class="sxs-lookup"><span data-stu-id="ddb16-124">To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

