---
title: Макрокоманда NavigateTo
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288604"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="9762c-102">Макрокоманда NavigateTo</span><span class="sxs-lookup"><span data-stu-id="9762c-102">NavigateTo macro action</span></span>

<span data-ttu-id="9762c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9762c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9762c-104">Действие **NavigateTo** можно использовать для управления отображением объектов базы данных в области навигации.</span><span class="sxs-lookup"><span data-stu-id="9762c-104">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane.</span></span> <span data-ttu-id="9762c-105">Например, можно изменить категорию объектов базы данных и отфильтровать их таким образом, чтобы отображались только определенные объекты.</span><span class="sxs-lookup"><span data-stu-id="9762c-105">For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="9762c-106">Setting</span><span class="sxs-lookup"><span data-stu-id="9762c-106">Setting</span></span>

<span data-ttu-id="9762c-107">Действие **NavigateTo** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9762c-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9762c-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="9762c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9762c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9762c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9762c-110"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="9762c-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="9762c-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="9762c-111">Required.</span></span> <span data-ttu-id="9762c-112">Категория, по которой в области навигации должны отображаться объекты.</span><span class="sxs-lookup"><span data-stu-id="9762c-112">The category by which you want the Navigation Pane to display objects.</span></span> <span data-ttu-id="9762c-113">Щелкните <strong>"Тип объекта",</strong> <strong>"Таблицы и</strong> <strong>представления", "Дата изменения",</strong> <strong>"Дата создания"</strong>или <strong>"Настраиваемый"</strong> в поле <strong>"Категория".</strong></span><span class="sxs-lookup"><span data-stu-id="9762c-113">Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9762c-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="9762c-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="9762c-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="9762c-115">Optional.</span></span> <span data-ttu-id="9762c-116">Аргумент <strong>Group</strong> ограничивает, какие объекты в категории отображаются в области навигации.</span><span class="sxs-lookup"><span data-stu-id="9762c-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="9762c-117">Если оставить аргумент <strong>Group</strong> пустым, в области навигации отображаются все объекты базы данных, классифицируются по критериям, заданной в <strong>аргументе Category.</strong></span><span class="sxs-lookup"><span data-stu-id="9762c-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="9762c-118">Примеры допустимого <strong>аргумента Group</strong> для различных <strong>аргументов Category</strong> показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9762c-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9762c-119">Заметки</span><span class="sxs-lookup"><span data-stu-id="9762c-119">Remarks</span></span>

- <span data-ttu-id="9762c-120">Это действие аналогично выбору категорий и групп в заголовке панели навигации.</span><span class="sxs-lookup"><span data-stu-id="9762c-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="9762c-121">**Допустимые** аргументы группы зависят **от используемой категории** аргумента.</span><span class="sxs-lookup"><span data-stu-id="9762c-121">Valid **Group** arguments depend on which **Category** argument is used.</span></span> <span data-ttu-id="9762c-122">Если ввести недопустимый **аргумент Group,** появится сообщение об ошибке. В следующей таблице представлены примеры допустимого **аргумента Group** для каждого **аргумента Category.**</span><span class="sxs-lookup"><span data-stu-id="9762c-122">If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="9762c-123">Аргумент category</span><span class="sxs-lookup"><span data-stu-id="9762c-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="9762c-124">Примеры аргументов group</span><span class="sxs-lookup"><span data-stu-id="9762c-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="9762c-125">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="9762c-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="9762c-126">Таблицы; Forms; Запросы; Страницы; Макрос; Модули</span><span class="sxs-lookup"><span data-stu-id="9762c-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="9762c-127">Таблицы и представления</span><span class="sxs-lookup"><span data-stu-id="9762c-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="9762c-128">Имена определенных таблиц в базе данных</span><span class="sxs-lookup"><span data-stu-id="9762c-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="9762c-129">Дата изменения</span><span class="sxs-lookup"><span data-stu-id="9762c-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="9762c-130">Сегодня; Сегодня; Last Month; Более старые</span><span class="sxs-lookup"><span data-stu-id="9762c-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="9762c-131">Created Date (дата создания)</span><span class="sxs-lookup"><span data-stu-id="9762c-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="9762c-132">Сегодня; Сегодня; Last Month; Более старые</span><span class="sxs-lookup"><span data-stu-id="9762c-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="9762c-133">Настраиваемая категория</span><span class="sxs-lookup"><span data-stu-id="9762c-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="9762c-134">Имена групп, созданных для указанной настраиваемой категории</span><span class="sxs-lookup"><span data-stu-id="9762c-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="9762c-135">Чтобы запустить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="9762c-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="9762c-136">Чтобы перейти на верхний уровень категории **(например,**"Все таблицы", "Все объекты доступа" или **"Все** даты"), необходимо оставить аргумент Group пустым.</span><span class="sxs-lookup"><span data-stu-id="9762c-136">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank.</span></span> <span data-ttu-id="9762c-137">Например, если аргумент **category** имеет тип **объекта,** при  вводе всех объектов **Access** в качестве группового аргумента происходит ошибка.</span><span class="sxs-lookup"><span data-stu-id="9762c-137">For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


