---
title: NavigateTo Macro Action
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9a6a59b6c84e9814aeb9b4709d27955f29fd9e1e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481435"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="1f486-102">NavigateTo Macro Action</span><span class="sxs-lookup"><span data-stu-id="1f486-102">NavigateTo Macro Action</span></span>


<span data-ttu-id="1f486-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f486-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1f486-104">Действие **NavigateTo** можно использовать для управления отображением объектов базы данных в области навигации.</span><span class="sxs-lookup"><span data-stu-id="1f486-104">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane.</span></span> <span data-ttu-id="1f486-105">Например можно изменить как классифицируются объекты базы данных и объекты можно отфильтровать так, чтобы отображались только некоторые из них.</span><span class="sxs-lookup"><span data-stu-id="1f486-105">For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="1f486-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="1f486-106">Setting</span></span>

<span data-ttu-id="1f486-107">Действие **NavigateTo** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="1f486-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f486-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1f486-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1f486-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1f486-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f486-110"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="1f486-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="1f486-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1f486-111">Required.</span></span> <span data-ttu-id="1f486-112">Категория, по которому требуется области навигации для отображения объектов.</span><span class="sxs-lookup"><span data-stu-id="1f486-112">The category by which you want the Navigation Pane to display objects.</span></span> <span data-ttu-id="1f486-113">Выберите <strong>Тип объекта</strong>, <strong>таблицы и представления</strong>, <strong>Дата изменения</strong>, <strong>Дата создания</strong>или <strong>Custom</strong> в поле <strong>категории</strong> .</span><span class="sxs-lookup"><span data-stu-id="1f486-113">Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f486-114"><strong>group</strong></span><span class="sxs-lookup"><span data-stu-id="1f486-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="1f486-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="1f486-115">Optional.</span></span> <span data-ttu-id="1f486-116">Ограничения аргумент для <strong>групп</strong> , которые объектов в категории, отображаются в области навигации.</span><span class="sxs-lookup"><span data-stu-id="1f486-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="1f486-117">Если <strong>Группа</strong> аргумента оставлено пустым, области навигации отображает все объекты базы данных, упорядоченные по условиям, указанным в аргументе <strong>категории</strong> .</span><span class="sxs-lookup"><span data-stu-id="1f486-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="1f486-118">В следующей таблице показаны примеры допустимых аргументов <strong>группы</strong> для различных <strong>категорий</strong> аргументов.</span><span class="sxs-lookup"><span data-stu-id="1f486-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1f486-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f486-119">Remarks</span></span>

  - <span data-ttu-id="1f486-120">Это действие аналогично Выбор категории и группы из строки заголовка в области переходов.</span><span class="sxs-lookup"><span data-stu-id="1f486-120">This action is similar to selecting categories and groups from the title bar of the Navigation Pane.</span></span>

  - <span data-ttu-id="1f486-121">Допустимые аргументы **группы** зависят от того, какие **категории** используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="1f486-121">Valid **Group** arguments depend on which **Category** argument is used.</span></span> <span data-ttu-id="1f486-122">Если указан недопустимый аргумент **группы** , появляется сообщение об ошибке. В следующей таблице приведены примеры допустимых аргументов **группы** для каждой **категории** аргумента.</span><span class="sxs-lookup"><span data-stu-id="1f486-122">If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="1f486-123">Аргумент категории</span><span class="sxs-lookup"><span data-stu-id="1f486-123">Category argument</span></span></p></th>
    <th><p><span data-ttu-id="1f486-124">Пример группового аргументов</span><span class="sxs-lookup"><span data-stu-id="1f486-124">Example Group arguments</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="1f486-125">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="1f486-125">Object Type</span></span></p></td>
    <td><p><span data-ttu-id="1f486-126">Таблиц; Форм; Запросы; Страницы; Макросы; Модули</span><span class="sxs-lookup"><span data-stu-id="1f486-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="1f486-127">Таблицы и представления</span><span class="sxs-lookup"><span data-stu-id="1f486-127">Tables and Views</span></span></p></td>
    <td><p><span data-ttu-id="1f486-128">Имена отдельных таблиц в базе данных</span><span class="sxs-lookup"><span data-stu-id="1f486-128">Names of specific tables in your database</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="1f486-129">Дата изменения</span><span class="sxs-lookup"><span data-stu-id="1f486-129">Modified Date</span></span></p></td>
    <td><p><span data-ttu-id="1f486-130">Текущая; Устаревшее; Последний месяц; Более старые</span><span class="sxs-lookup"><span data-stu-id="1f486-130">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="1f486-131">Created Date (дата создания)</span><span class="sxs-lookup"><span data-stu-id="1f486-131">Created Date</span></span></p></td>
    <td><p><span data-ttu-id="1f486-132">Текущая; Устаревшее; Последний месяц; Более старые</span><span class="sxs-lookup"><span data-stu-id="1f486-132">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="1f486-133">Настраиваемые категории</span><span class="sxs-lookup"><span data-stu-id="1f486-133">Custom category</span></span></p></td>
    <td><p><span data-ttu-id="1f486-134">Имена групп, созданные для указанного настраиваемые категории</span><span class="sxs-lookup"><span data-stu-id="1f486-134">Names of groups you have created for the specified custom category</span></span></p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="1f486-135">Чтобы выполнить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="1f486-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1f486-136">Чтобы перейти на верхний уровень категории (например, <STRONG>Все таблицы</STRONG>, <STRONG>Все объекты доступа</STRONG>или <STRONG>Все даты</STRONG>), аргумент группы необходимо оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="1f486-136">To navigate to the top level of a category (for example, <STRONG>All Tables</STRONG>, <STRONG>All Access Objects</STRONG>, or <STRONG>All Dates</STRONG>), you must leave the Group argument blank.</span></span> <span data-ttu-id="1f486-137">К примеру при аргумент <STRONG>категории</STRONG> — это <STRONG>Тип объекта</STRONG>, ввод <STRONG>Всех объектов доступа</STRONG> как аргумент <STRONG>группы</STRONG> , приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1f486-137">For example, when the <STRONG>Category</STRONG> argument is <STRONG>Object Type</STRONG>, entering <STRONG>All Access Objects</STRONG> as a <STRONG>Group</STRONG> argument results in an error.</span></span></P>


