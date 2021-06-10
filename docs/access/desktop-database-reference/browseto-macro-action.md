---
title: Макрокоманда BrowseTo
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296775"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="dfab0-102">Макрокоманда BrowseTo</span><span class="sxs-lookup"><span data-stu-id="dfab0-102">BrowseTo macro action</span></span>

<span data-ttu-id="dfab0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfab0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfab0-104">Вы можете использовать действие **BrowseTo для** перемещения между объектами на месте.</span><span class="sxs-lookup"><span data-stu-id="dfab0-104">You can use the **BrowseTo** action to navigate between objects in place.</span></span> <span data-ttu-id="dfab0-105">Кроме того, можно изменить исходный объект управления подформами, указав аргумент Path to Subform Control.</span><span class="sxs-lookup"><span data-stu-id="dfab0-105">You can also change the source object of a subform control by specifying the Path to Subform Control argument.</span></span> <span data-ttu-id="dfab0-106">Используйте **BrowseTo** для перемещения из form1 в form2 без открытия нового окна.</span><span class="sxs-lookup"><span data-stu-id="dfab0-106">Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="dfab0-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="dfab0-107">Setting</span></span>

<span data-ttu-id="dfab0-108">Действие **BrowseTo** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="dfab0-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dfab0-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="dfab0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dfab0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dfab0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfab0-111">Object Type</span><span class="sxs-lookup"><span data-stu-id="dfab0-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="dfab0-112">Тип объекта, для которого необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="dfab0-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfab0-113">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="dfab0-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="dfab0-114">Объект, загружаемый внутри управления подформами, ссылаясь на аргумент Path to Subform Control.</span><span class="sxs-lookup"><span data-stu-id="dfab0-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfab0-115">Путь к контролю subform</span><span class="sxs-lookup"><span data-stu-id="dfab0-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="dfab0-116">Если указано, путь от основной формы приложения до целевого управления подформами, загружаемого объектом, указанным аргументом Object Name.</span><span class="sxs-lookup"><span data-stu-id="dfab0-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfab0-117">Где состояние</span><span class="sxs-lookup"><span data-stu-id="dfab0-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="dfab0-118">Если задано, заменит состояние Where источника записи объекта.</span><span class="sxs-lookup"><span data-stu-id="dfab0-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfab0-119">Page</span><span class="sxs-lookup"><span data-stu-id="dfab0-119">Page</span></span></p></td>
<td><p><span data-ttu-id="dfab0-120">Если указано, задана страница непрерывной формы, которая будет выполнена на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="dfab0-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="dfab0-121">Этот аргумент является веб-только.</span><span class="sxs-lookup"><span data-stu-id="dfab0-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfab0-122">Режим данных</span><span class="sxs-lookup"><span data-stu-id="dfab0-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="dfab0-123">Если указано, режим ввода данных формы.</span><span class="sxs-lookup"><span data-stu-id="dfab0-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dfab0-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="dfab0-124">Remarks</span></span>

<span data-ttu-id="dfab0-125">Аргумент PathToSubFormControl должен быть указан с помощью синтаксиса в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="dfab0-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="dfab0-126">В этом примере основная форма — это форма верхнего уровня в клиентских приложениях Access.</span><span class="sxs-lookup"><span data-stu-id="dfab0-126">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="dfab0-127">Аргумент Path to Sub Form Control должен поочередно указывать имена управления формами и подформами, ведущие из основной формы в подформу, которая является контейнером объекта, указанного аргументом Object Name.</span><span class="sxs-lookup"><span data-stu-id="dfab0-127">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="dfab0-128">Каждый указанный контроль подформы должен быть управлением в форме, предшествуемой ему.</span><span class="sxs-lookup"><span data-stu-id="dfab0-128">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="dfab0-129">Путь должен закончиться управлением подформ.</span><span class="sxs-lookup"><span data-stu-id="dfab0-129">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="dfab0-130">Пример</span><span class="sxs-lookup"><span data-stu-id="dfab0-130">Example</span></span>

<span data-ttu-id="dfab0-131">В следующем примере показано, как использовать действие BrowseTo для открытия отчета в подформ-контроле или в области управления навигацией.</span><span class="sxs-lookup"><span data-stu-id="dfab0-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="dfab0-132">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="dfab0-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



