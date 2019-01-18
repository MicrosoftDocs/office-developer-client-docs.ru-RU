---
title: Макрокоманда SetFilter
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698682"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="e5103-102">Макрокоманда SetFilter</span><span class="sxs-lookup"><span data-stu-id="e5103-102">SetFilter macro action</span></span>

<span data-ttu-id="e5103-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5103-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5103-104">Чтобы применить фильтр в записи в активной таблицы, формы, отчета или в таблице можно использовать действие **SetFilter** .</span><span class="sxs-lookup"><span data-stu-id="e5103-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="e5103-105">Setting</span><span class="sxs-lookup"><span data-stu-id="e5103-105">Setting</span></span>

<span data-ttu-id="e5103-106">Действие **SetFilter** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e5103-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5103-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="e5103-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e5103-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e5103-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5103-109">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="e5103-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="e5103-110">Если этот параметр указан, имя запроса или фильтра, сохраненный как запрос.</span><span class="sxs-lookup"><span data-stu-id="e5103-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="e5103-111">Этот аргумент или аргумент WhereCondition требуется в базе данных клиента.</span><span class="sxs-lookup"><span data-stu-id="e5103-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="e5103-112">В веб-база данных этот аргумент недоступен.</span><span class="sxs-lookup"><span data-stu-id="e5103-112">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5103-113">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="e5103-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="e5103-114">Если этот параметр указан, SQL предложения WHERE, которое ограничивает число записей в таблице данных, форме, отчете или таблице.</span><span class="sxs-lookup"><span data-stu-id="e5103-114">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="e5103-115">В веб-база данных этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e5103-115">In a web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5103-116">Контрольное имя</span><span class="sxs-lookup"><span data-stu-id="e5103-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="e5103-117">Если этот параметр указан, имя элемента управления, соответствующее подчиненной формы или отчета для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="e5103-117">If provided, the name of the control that corresponds to the subform or subreport to be filtered.</span></span> <span data-ttu-id="e5103-118">Если пустые, фильтруется текущий объект.</span><span class="sxs-lookup"><span data-stu-id="e5103-118">If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e5103-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="e5103-119">Remarks</span></span>

<span data-ttu-id="e5103-120">В веб-база данных где условие аргумент не может начинаться с знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="e5103-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="e5103-121">При выполнении этого действия, чтобы таблицы, формы, отчета или таблицы данных (например, результат запроса), который является активным и фокус находится на применяется фильтр.</span><span class="sxs-lookup"><span data-stu-id="e5103-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="e5103-122">Свойство **фильтра** активного объекта используется для сохранения WhereCondition аргумент, применять в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="e5103-122">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time.</span></span> <span data-ttu-id="e5103-123">Фильтры сохраняются вместе с объектами, в которых они созданы.</span><span class="sxs-lookup"><span data-stu-id="e5103-123">Filters are saved with the objects in which they are created.</span></span> <span data-ttu-id="e5103-124">Автоматически загружаются при открытии объекта, но они не применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="e5103-124">They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="e5103-125">В базе данных клиента чтобы автоматически применить фильтр при открытии объекта, присвойте свойству **FilterOnLoad** значение True.</span><span class="sxs-lookup"><span data-stu-id="e5103-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="e5103-126">В веб-база данных автоматически применить фильтр при открытии объекта, добавьте действие **SetFilter** макроса и добавить макрос для объекта события **OnLoad** .</span><span class="sxs-lookup"><span data-stu-id="e5103-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="e5103-127">Пример</span><span class="sxs-lookup"><span data-stu-id="e5103-127">Example</span></span>

<span data-ttu-id="e5103-128">Следующем примере показано, как использовать действие SetFilter для фильтрации формы, в котором определен макрос.</span><span class="sxs-lookup"><span data-stu-id="e5103-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="e5103-129">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e5103-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
