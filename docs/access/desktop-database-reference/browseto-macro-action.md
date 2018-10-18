---
title: BrowseTo Macro Action
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15009ca039d5df06bc732f4b58c066ad8f8d67c9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603765"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="210fa-102">BrowseTo Macro Action</span><span class="sxs-lookup"><span data-stu-id="210fa-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="210fa-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="210fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="210fa-104">Действие **ВыбратьОбъект** можно использовать для перехода между объектами на месте.</span><span class="sxs-lookup"><span data-stu-id="210fa-104">You can use the **BrowseTo** action to navigate between objects in place.</span></span> <span data-ttu-id="210fa-105">Можно также изменить исходный объект подчиненной путем указания пути к подчиненной аргумент.</span><span class="sxs-lookup"><span data-stu-id="210fa-105">You can also change the source object of a subform control by specifying the Path to Subform Control argument.</span></span> <span data-ttu-id="210fa-106">Используйте **ВыбратьОбъект** для перехода от form1 form2, не открывая новое окно.</span><span class="sxs-lookup"><span data-stu-id="210fa-106">Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="210fa-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="210fa-107">Setting</span></span>

<span data-ttu-id="210fa-108">Действие **ВыбратьОбъект** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="210fa-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="210fa-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="210fa-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="210fa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="210fa-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="210fa-111">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="210fa-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="210fa-112">Тип объекта, к которому следует обзор.</span><span class="sxs-lookup"><span data-stu-id="210fa-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="210fa-113">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="210fa-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="210fa-114">Объект, который загружает внутри элемента управления подчиненной формы, ссылается путь, который требуется аргумент управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="210fa-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210fa-115">Путь к элементу управления подчиненной формы</span><span class="sxs-lookup"><span data-stu-id="210fa-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="210fa-116">Если указан, то путь из основной формы приложения, подчиненная форма конечного управления, загружает объект, указанный в аргументе имя объекта.</span><span class="sxs-lookup"><span data-stu-id="210fa-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="210fa-117">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="210fa-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="210fa-118">Если указано, заменяет условие источника записей объекта.</span><span class="sxs-lookup"><span data-stu-id="210fa-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210fa-119">Page</span><span class="sxs-lookup"><span data-stu-id="210fa-119">Page</span></span></p></td>
<span data-ttu-id="210fa-120"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="210fa-120"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="210fa-121">Если указано, задает страницу непрерывного формы, в которой будет осуществляться текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="210fa-121">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="210fa-122">Этот аргумент представляет Web только.</span><span class="sxs-lookup"><span data-stu-id="210fa-122">This argument is Web only.</span></span></p></td>
=======
<td><p><span data-ttu-id="210fa-123">Если указано, задает страницу непрерывного формы, в которой будет осуществляться текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="210fa-123">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="210fa-124">Этот аргумент представляет веб-узла только.</span><span class="sxs-lookup"><span data-stu-id="210fa-124">This argument is web only.</span></span></p></td><span data-ttu-id="210fa-125">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="210fa-125">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="210fa-126">Режим данных</span><span class="sxs-lookup"><span data-stu-id="210fa-126">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="210fa-127">Если указан, режим ввода данных формы.</span><span class="sxs-lookup"><span data-stu-id="210fa-127">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="210fa-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="210fa-128">Remarks</span></span>

<span data-ttu-id="210fa-129">Аргумент PathToSubFormControl должен быть указан с помощью синтаксиса в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="210fa-129">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="210fa-130">В этом примере форме основной — форма верхнего уровня в клиентском приложении Access.</span><span class="sxs-lookup"><span data-stu-id="210fa-130">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="210fa-131">Путь, который требуется аргумент Sub элемента управления формы можно также необходимо указать имена элементов управления формы и подчиненной формы начальные из главной формы к элементу управления подчиненной формы, который является контейнером объект, указанный в аргументе имя объекта.</span><span class="sxs-lookup"><span data-stu-id="210fa-131">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="210fa-132">Все элементы управления подчиненной формы, указанного значения элемента управления на форме, которая предшествует его.</span><span class="sxs-lookup"><span data-stu-id="210fa-132">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="210fa-133">Путь должен завершаться управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="210fa-133">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="210fa-134">Пример</span><span class="sxs-lookup"><span data-stu-id="210fa-134">Example</span></span>

<span data-ttu-id="210fa-135">Следующем примере показано, как использовать ВыбратьОбъект действия, чтобы открыть отчет в элементе управления подчиненной формы или в элементе управления навигации.</span><span class="sxs-lookup"><span data-stu-id="210fa-135">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="210fa-136">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="210fa-136">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



