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
# <a name="browseto-macro-action"></a><span data-ttu-id="2d637-102">Макрокоманда BrowseTo</span><span class="sxs-lookup"><span data-stu-id="2d637-102">BrowseTo macro action</span></span>

<span data-ttu-id="2d637-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d637-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d637-104">Вы можете использовать действие **бровсето** для перехода между объектами на месте.</span><span class="sxs-lookup"><span data-stu-id="2d637-104">You can use the **BrowseTo** action to navigate between objects in place.</span></span> <span data-ttu-id="2d637-105">Кроме того, можно изменить исходный объект элемента управления подчиненной формы, указав аргумент путь к элементу управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="2d637-105">You can also change the source object of a subform control by specifying the Path to Subform Control argument.</span></span> <span data-ttu-id="2d637-106">С помощью **бровсето** можно переходить с Form1 на Form2, не открывая новое окно.</span><span class="sxs-lookup"><span data-stu-id="2d637-106">Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="2d637-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="2d637-107">Setting</span></span>

<span data-ttu-id="2d637-108">Действие **бровсето** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="2d637-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d637-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2d637-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2d637-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2d637-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d637-111">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="2d637-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="2d637-112">Тип объекта, в котором необходимо выполнить обзор.</span><span class="sxs-lookup"><span data-stu-id="2d637-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d637-113">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="2d637-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="2d637-114">Объект, который загружается в элемент управления подчиненной формы, на который ссылается аргумент элемента управления "путь к подчиненной форме".</span><span class="sxs-lookup"><span data-stu-id="2d637-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d637-115">Путь к элементу управления подчиненной формы</span><span class="sxs-lookup"><span data-stu-id="2d637-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="2d637-116">Если этот параметр указан, то путь из основной формы приложения к целевому элементу управления подчиненной формы, который загружает объект, заданный аргументом "имя объекта".</span><span class="sxs-lookup"><span data-stu-id="2d637-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d637-117">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="2d637-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="2d637-118">Если этот параметр указан, заменяется условие WHERE источника записей объекта.</span><span class="sxs-lookup"><span data-stu-id="2d637-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d637-119">Page</span><span class="sxs-lookup"><span data-stu-id="2d637-119">Page</span></span></p></td>
<td><p><span data-ttu-id="2d637-120">Если этот параметр указан, задает страницу ленточной формы, которая будет сделана на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="2d637-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="2d637-121">Этот аргумент относится только к веб-сайтам.</span><span class="sxs-lookup"><span data-stu-id="2d637-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d637-122">Режим данных</span><span class="sxs-lookup"><span data-stu-id="2d637-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="2d637-123">Если этот параметр указан, то режим ввода данных в форме.</span><span class="sxs-lookup"><span data-stu-id="2d637-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2d637-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="2d637-124">Remarks</span></span>

<span data-ttu-id="2d637-125">Аргумент Пастосубформконтрол должен быть указан с помощью синтаксиса в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="2d637-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="2d637-126">В этом примере Главная форма является формой верхнего уровня в клиентском приложении Access.</span><span class="sxs-lookup"><span data-stu-id="2d637-126">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="2d637-127">Аргумент элемента управления "путь к подчиненной форме" должен указывать имена элементов управления формы и подчиненной формы, ведущие от главной формы к элементу управления подчиненной формы, который является контейнером объекта, указанного аргументом "имя объекта".</span><span class="sxs-lookup"><span data-stu-id="2d637-127">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="2d637-128">Каждый указанный элемент управления подчиненной формы должен быть элементом управления в форме, предшествующей ему.</span><span class="sxs-lookup"><span data-stu-id="2d637-128">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="2d637-129">Путь должен заканчиваться элементом управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="2d637-129">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="2d637-130">Пример</span><span class="sxs-lookup"><span data-stu-id="2d637-130">Example</span></span>

<span data-ttu-id="2d637-131">В приведенном ниже примере показано, как использовать действие Бровсето для открытия отчета в элементе управления подчиненной формы или в элементе управления навигацией.</span><span class="sxs-lookup"><span data-stu-id="2d637-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="2d637-132">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2d637-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



