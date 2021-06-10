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
# <a name="navigateto-macro-action"></a><span data-ttu-id="7fd0f-102">Макрокоманда NavigateTo</span><span class="sxs-lookup"><span data-stu-id="7fd0f-102">NavigateTo macro action</span></span>

<span data-ttu-id="7fd0f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fd0f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7fd0f-104">Вы можете использовать **действие NavigateTo** для управления отображением объектов базы данных в области навигации.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-104">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane.</span></span> <span data-ttu-id="7fd0f-105">Например, можно изменить категорию объектов базы данных и отфильтровать их таким образом, чтобы отображались только определенные объекты.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-105">For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="7fd0f-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="7fd0f-106">Setting</span></span>

<span data-ttu-id="7fd0f-107">Действие **NavigateTo** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7fd0f-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="7fd0f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7fd0f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7fd0f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fd0f-110"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="7fd0f-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd0f-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-111">Required.</span></span> <span data-ttu-id="7fd0f-112">Категория, по которой необходимо, чтобы в области навигации отображались объекты.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-112">The category by which you want the Navigation Pane to display objects.</span></span> <span data-ttu-id="7fd0f-113">Нажмите <strong>кнопку Тип</strong>объекта, <strong>Таблицы</strong>и Представления, <strong>Измененная дата,</strong>Созданная <strong>дата</strong>или <strong>настраиваемая</strong> в <strong>поле Category.</strong></span><span class="sxs-lookup"><span data-stu-id="7fd0f-113">Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd0f-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="7fd0f-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd0f-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-115">Optional.</span></span> <span data-ttu-id="7fd0f-116">Аргумент <strong>Group</strong> ограничивает, какие объекты в категории отображаются в области навигации.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="7fd0f-117">Если оставить аргумент <strong>Group</strong> пустым, в области навигации отображаются все объекты базы данных, классифицируются по критериям, которые указаны в <strong>аргументе Category.</strong></span><span class="sxs-lookup"><span data-stu-id="7fd0f-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="7fd0f-118">Примеры допустимого <strong>группового</strong> аргумента для <strong>различных</strong> аргументов категории показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7fd0f-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="7fd0f-119">Remarks</span></span>

- <span data-ttu-id="7fd0f-120">Это действие аналогично выбору категорий и групп из панели заголовков панели навигации.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="7fd0f-121">Аргументы **допустимой** группы зависят от **того, какой аргумент** категории используется.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-121">Valid **Group** arguments depend on which **Category** argument is used.</span></span> <span data-ttu-id="7fd0f-122">Если ввести недействительный **групповой** аргумент, появится сообщение об ошибке. В следующей таблице представлены примеры допустимого **аргумента Group** для каждого **аргумента Категории.**</span><span class="sxs-lookup"><span data-stu-id="7fd0f-122">If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="7fd0f-123">Аргумент category</span><span class="sxs-lookup"><span data-stu-id="7fd0f-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="7fd0f-124">Примеры групповых аргументов</span><span class="sxs-lookup"><span data-stu-id="7fd0f-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="7fd0f-125">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="7fd0f-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="7fd0f-126">Таблицы; Формы; Запросы; Страницы; Макрос; Модули</span><span class="sxs-lookup"><span data-stu-id="7fd0f-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="7fd0f-127">Таблицы и представления</span><span class="sxs-lookup"><span data-stu-id="7fd0f-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="7fd0f-128">Имена определенных таблиц в базе данных</span><span class="sxs-lookup"><span data-stu-id="7fd0f-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="7fd0f-129">Измененная дата</span><span class="sxs-lookup"><span data-stu-id="7fd0f-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="7fd0f-130">Сегодня; Вчера; В прошлом месяце; Более старые</span><span class="sxs-lookup"><span data-stu-id="7fd0f-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="7fd0f-131">Created Date (дата создания)</span><span class="sxs-lookup"><span data-stu-id="7fd0f-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="7fd0f-132">Сегодня; Вчера; В прошлом месяце; Более старые</span><span class="sxs-lookup"><span data-stu-id="7fd0f-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="7fd0f-133">Настраиваемая категория</span><span class="sxs-lookup"><span data-stu-id="7fd0f-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="7fd0f-134">Имена групп, созданных для указанной настраиваемой категории</span><span class="sxs-lookup"><span data-stu-id="7fd0f-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="7fd0f-135">Чтобы выполнить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="7fd0f-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="7fd0f-136">Чтобы перейти на верхний уровень категории **(например,**"Все таблицы", "Все объекты доступа" или "Все даты"), необходимо оставить аргумент Group пустым.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-136">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank.</span></span> <span data-ttu-id="7fd0f-137">Например, если аргумент **category** — тип  **объекта,** ввод  всех объектов доступа в качестве группового аргумента приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="7fd0f-137">For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


