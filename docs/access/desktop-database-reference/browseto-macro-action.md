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
ms.openlocfilehash: 09e2b8238555a0d1b718f04c69f733039c1d8477
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483180"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="75e22-102">BrowseTo Macro Action</span><span class="sxs-lookup"><span data-stu-id="75e22-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="75e22-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75e22-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75e22-104">Действие **ВыбратьОбъект** можно использовать для перехода между объектами на месте.</span><span class="sxs-lookup"><span data-stu-id="75e22-104">You can use the **BrowseTo** action to navigate between objects in place.</span></span> <span data-ttu-id="75e22-105">Можно также изменить исходный объект подчиненной путем указания пути к подчиненной аргумент.</span><span class="sxs-lookup"><span data-stu-id="75e22-105">You can also change the source object of a subform control by specifying the Path to Subform Control argument.</span></span> <span data-ttu-id="75e22-106">Используйте **ВыбратьОбъект** для перехода от form1 form2, не открывая новое окно.</span><span class="sxs-lookup"><span data-stu-id="75e22-106">Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="75e22-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="75e22-107">Setting</span></span>

<span data-ttu-id="75e22-108">Действие **ВыбратьОбъект** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="75e22-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75e22-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="75e22-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="75e22-110">Описание</span><span class="sxs-lookup"><span data-stu-id="75e22-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75e22-111">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="75e22-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="75e22-112">Тип объекта, к которому следует обзор.</span><span class="sxs-lookup"><span data-stu-id="75e22-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e22-113">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="75e22-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="75e22-114">Объект, который загружает внутри элемента управления подчиненной формы, ссылается путь, который требуется аргумент управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="75e22-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e22-115">Путь к элементу управления подчиненной формы</span><span class="sxs-lookup"><span data-stu-id="75e22-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="75e22-116">Если указан, то путь из основной формы приложения, подчиненная форма конечного управления, загружает объект, указанный в аргументе имя объекта.</span><span class="sxs-lookup"><span data-stu-id="75e22-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e22-117">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="75e22-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="75e22-118">Если указано, заменяет условие источника записей объекта.</span><span class="sxs-lookup"><span data-stu-id="75e22-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e22-119">Page</span><span class="sxs-lookup"><span data-stu-id="75e22-119">Page</span></span></p></td>
<td><p><span data-ttu-id="75e22-120">Если указано, задает страницу непрерывного формы, в которой будет осуществляться текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="75e22-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="75e22-121">Этот аргумент представляет Web только.</span><span class="sxs-lookup"><span data-stu-id="75e22-121">This argument is Web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e22-122">Режим данных</span><span class="sxs-lookup"><span data-stu-id="75e22-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="75e22-123">Если указан, режим ввода данных формы.</span><span class="sxs-lookup"><span data-stu-id="75e22-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="75e22-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="75e22-124">Remarks</span></span>

<span data-ttu-id="75e22-125">Аргумент PathToSubFormControl должен быть указан с помощью синтаксиса в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="75e22-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="75e22-126">В этом примере форме основной — форма верхнего уровня в клиентском приложении Access.</span><span class="sxs-lookup"><span data-stu-id="75e22-126">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="75e22-127">Путь, который требуется аргумент Sub элемента управления формы можно также необходимо указать имена элементов управления формы и подчиненной формы начальные из главной формы к элементу управления подчиненной формы, который является контейнером объект, указанный в аргументе имя объекта.</span><span class="sxs-lookup"><span data-stu-id="75e22-127">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="75e22-128">Все элементы управления подчиненной формы, указанного значения элемента управления на форме, которая предшествует его.</span><span class="sxs-lookup"><span data-stu-id="75e22-128">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="75e22-129">Путь должен завершаться управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="75e22-129">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="75e22-130">Пример</span><span class="sxs-lookup"><span data-stu-id="75e22-130">Example</span></span>

<span data-ttu-id="75e22-131">Следующем примере показано, как использовать ВыбратьОбъект действия, чтобы открыть отчет в элементе управления подчиненной формы или в элементе управления навигации.</span><span class="sxs-lookup"><span data-stu-id="75e22-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="75e22-132">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="75e22-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



