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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308696"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="6f47e-102">Макрокоманда SetFilter</span><span class="sxs-lookup"><span data-stu-id="6f47e-102">SetFilter macro action</span></span>

<span data-ttu-id="6f47e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f47e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f47e-104">Вы можете использовать действие **SetFilter** , чтобы применить фильтр к записям в активной таблице, форме, отчете или таблице.</span><span class="sxs-lookup"><span data-stu-id="6f47e-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="6f47e-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="6f47e-105">Setting</span></span>

<span data-ttu-id="6f47e-106">Макрокоманда **SetFilter** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6f47e-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f47e-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6f47e-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6f47e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6f47e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f47e-109">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="6f47e-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="6f47e-110">Если этот параметр указан, имя запроса или фильтра сохраняется как запрос.</span><span class="sxs-lookup"><span data-stu-id="6f47e-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="6f47e-111">Этот аргумент или аргумент WhereCondition является обязательным в клиентской базе данных.</span><span class="sxs-lookup"><span data-stu-id="6f47e-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="6f47e-112">В веб-базе данных этот аргумент недоступен.</span><span class="sxs-lookup"><span data-stu-id="6f47e-112">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f47e-113">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="6f47e-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="6f47e-114">Если этот параметр указан, предложение WHERE (SQL), которое ограничит записи в таблице, форме, отчете или таблице.</span><span class="sxs-lookup"><span data-stu-id="6f47e-114">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="6f47e-115">В веб-базе данных этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6f47e-115">In a web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f47e-116">Контрольное имя</span><span class="sxs-lookup"><span data-stu-id="6f47e-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="6f47e-117">Если этот параметр указан, то имя элемента управления, соответствующего подчиненной форме или подчиненному отчету, который будет фильтроваться.</span><span class="sxs-lookup"><span data-stu-id="6f47e-117">If provided, the name of the control that corresponds to the subform or subreport to be filtered.</span></span> <span data-ttu-id="6f47e-118">Если этот параметр не задан, то фильтруется текущий объект.</span><span class="sxs-lookup"><span data-stu-id="6f47e-118">If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6f47e-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f47e-119">Remarks</span></span>

<span data-ttu-id="6f47e-120">В веб-базе данных аргумент условия WHERE не может начинаться со знака равенства (=).</span><span class="sxs-lookup"><span data-stu-id="6f47e-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="6f47e-121">При выполнении этого действия фильтр применяется к таблице, форме, отчету или таблице (например, результату запроса), которая активна и находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="6f47e-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="6f47e-122">Свойство **Filter** активного объекта используется для сохранения аргумента WhereCondition и его применения в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="6f47e-122">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time.</span></span> <span data-ttu-id="6f47e-123">Фильтры сохраняются с объектами, в которых они созданы.</span><span class="sxs-lookup"><span data-stu-id="6f47e-123">Filters are saved with the objects in which they are created.</span></span> <span data-ttu-id="6f47e-124">Они автоматически загружаются при открытии объекта, но не применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="6f47e-124">They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="6f47e-125">В клиентской базе данных для автоматического применения фильтра при открытии объекта задайте для свойства **Филтеронлоад** значение true.</span><span class="sxs-lookup"><span data-stu-id="6f47e-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="6f47e-126">В веб-базе данных для автоматического применения фильтра при открытии объекта добавьте действие **SetFilter** в макрос и добавьте макрос в событие OnLoad объекта. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6f47e-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="6f47e-127">Пример</span><span class="sxs-lookup"><span data-stu-id="6f47e-127">Example</span></span>

<span data-ttu-id="6f47e-128">В приведенном ниже примере показано, как использовать действие SetFilter для фильтрации формы, в которой определен макрос.</span><span class="sxs-lookup"><span data-stu-id="6f47e-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="6f47e-129">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6f47e-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
