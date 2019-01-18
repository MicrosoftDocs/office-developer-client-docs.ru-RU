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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704422"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="3449f-102">Макрокоманда SetOrderBy</span><span class="sxs-lookup"><span data-stu-id="3449f-102">SetOrderBy macro action</span></span>


<span data-ttu-id="3449f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3449f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3449f-104">Действие **ЗадатьПорядокСортировки** можно использовать для указания способа сортировки записей формы, отчета, таблицы или результата запроса.</span><span class="sxs-lookup"><span data-stu-id="3449f-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="3449f-105">Setting</span><span class="sxs-lookup"><span data-stu-id="3449f-105">Setting</span></span>

<span data-ttu-id="3449f-106">Действие **ЗадатьПорядокСортировки** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="3449f-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3449f-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3449f-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3449f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3449f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3449f-109"><strong>Order By</strong></span><span class="sxs-lookup"><span data-stu-id="3449f-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="3449f-110">Строковое выражение, которое включает в себя имя поля или полей, по которому выполняется сортировка записей и необязательные ASC или DESC ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="3449f-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3449f-111"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="3449f-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3449f-112">Если этот параметр указан и активный объект является форму или отчет, имя элемента управления, соответствующее подчиненной формы или отчета, который будут отсортированы.</span><span class="sxs-lookup"><span data-stu-id="3449f-112">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted.</span></span> <span data-ttu-id="3449f-113">Если empty и активного объекта в форму или отчет, сортироваться родительского форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="3449f-113">If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3449f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3449f-114">Remarks</span></span>

<span data-ttu-id="3449f-115">При выполнении этого действия макроса сортировки применяется к таблице, форме, отчете или таблицы данных (результат запроса), который является активным и фокус находится на.</span><span class="sxs-lookup"><span data-stu-id="3449f-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="3449f-116">Аргумент Order By — это имя в поле или поля, в которых используется для сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="3449f-116">The Order By argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="3449f-117">При использовании более одного имени поля, разделяйте имена запятыми (,).</span><span class="sxs-lookup"><span data-stu-id="3449f-117">When you use more than one field name, separate the names with a comma (,).</span></span> <span data-ttu-id="3449f-118">Свойство **OrderBy** активного объекта используется чтобы сохранить порядок сортировки и применять в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="3449f-118">The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time.</span></span> <span data-ttu-id="3449f-119">Значения OrderBy сохраняются с объектами, в которых они созданы.</span><span class="sxs-lookup"><span data-stu-id="3449f-119">OrderBy values are saved with the objects in which they are created.</span></span> <span data-ttu-id="3449f-120">Автоматически загружаются при открытии объекта, но при этом не применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="3449f-120">They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="3449f-121">Если значение аргумента Order By, указав один или несколько имен полей и запустите макрос, записи сортируются в порядке возрастания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3449f-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="3449f-122">Чтобы отсортировать записи в убывающем порядке, введите DESC в конце выражения аргумента Order By.</span><span class="sxs-lookup"><span data-stu-id="3449f-122">To sort records in descending order, type DESC at the end of the Order By argument expression.</span></span> <span data-ttu-id="3449f-123">Например для сортировки записей клиентов в порядке убывания имя контакта, задайте Order By для «ContactName DESC».</span><span class="sxs-lookup"><span data-stu-id="3449f-123">For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC".</span></span> <span data-ttu-id="3449f-124">Чтобы отсортировать имена, LastName по убыванию и FirstName по возрастанию, значение аргумента Order By «Фамилия DESC, имя ASC».</span><span class="sxs-lookup"><span data-stu-id="3449f-124">To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

