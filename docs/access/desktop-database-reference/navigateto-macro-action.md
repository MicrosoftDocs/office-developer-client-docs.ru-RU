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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704142"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="9163b-102">Макрокоманда NavigateTo</span><span class="sxs-lookup"><span data-stu-id="9163b-102">NavigateTo macro action</span></span>

<span data-ttu-id="9163b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9163b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9163b-104">Действие **NavigateTo** можно использовать для управления отображением объектов базы данных в области навигации.</span><span class="sxs-lookup"><span data-stu-id="9163b-104">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane.</span></span> <span data-ttu-id="9163b-105">Например можно изменить как классифицируются объекты базы данных и объекты можно отфильтровать так, чтобы отображались только некоторые из них.</span><span class="sxs-lookup"><span data-stu-id="9163b-105">For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="9163b-106">Setting</span><span class="sxs-lookup"><span data-stu-id="9163b-106">Setting</span></span>

<span data-ttu-id="9163b-107">Действие **NavigateTo** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="9163b-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9163b-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="9163b-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9163b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9163b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9163b-110"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="9163b-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="9163b-111">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="9163b-111">Required.</span></span> <span data-ttu-id="9163b-112">Категория, по которому требуется области навигации для отображения объектов.</span><span class="sxs-lookup"><span data-stu-id="9163b-112">The category by which you want the Navigation Pane to display objects.</span></span> <span data-ttu-id="9163b-113">Выберите <strong>Тип объекта</strong>, <strong>таблицы и представления</strong>, <strong>Дата изменения</strong>, <strong>Дата создания</strong>или <strong>Custom</strong> в поле <strong>категории</strong> .</span><span class="sxs-lookup"><span data-stu-id="9163b-113">Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9163b-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="9163b-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="9163b-115">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="9163b-115">Optional.</span></span> <span data-ttu-id="9163b-116">Ограничения аргумент для <strong>групп</strong> , которые объектов в категории, отображаются в области навигации.</span><span class="sxs-lookup"><span data-stu-id="9163b-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="9163b-117">Если <strong>Группа</strong> аргумента оставлено пустым, области навигации отображает все объекты базы данных, упорядоченные по условиям, указанным в аргументе <strong>категории</strong> .</span><span class="sxs-lookup"><span data-stu-id="9163b-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="9163b-118">В следующей таблице показаны примеры допустимых аргументов <strong>группы</strong> для различных <strong>категорий</strong> аргументов.</span><span class="sxs-lookup"><span data-stu-id="9163b-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9163b-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="9163b-119">Remarks</span></span>

- <span data-ttu-id="9163b-120">Это действие аналогично Выбор категории и группы из строки заголовка в области переходов.</span><span class="sxs-lookup"><span data-stu-id="9163b-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="9163b-121">Допустимые аргументы **группы** зависят от того, какие **категории** используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="9163b-121">Valid **Group** arguments depend on which **Category** argument is used.</span></span> <span data-ttu-id="9163b-122">Если указан недопустимый аргумент **группы** , появляется сообщение об ошибке. В следующей таблице приведены примеры допустимых аргументов **группы** для каждой **категории** аргумента.</span><span class="sxs-lookup"><span data-stu-id="9163b-122">If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="9163b-123">Аргумент категории</span><span class="sxs-lookup"><span data-stu-id="9163b-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="9163b-124">Пример группового аргументов</span><span class="sxs-lookup"><span data-stu-id="9163b-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="9163b-125">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="9163b-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="9163b-126">Таблиц; Форм; Запросы; Страницы; Макросы; Модули</span><span class="sxs-lookup"><span data-stu-id="9163b-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="9163b-127">Таблицы и представления</span><span class="sxs-lookup"><span data-stu-id="9163b-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="9163b-128">Имена отдельных таблиц в базе данных</span><span class="sxs-lookup"><span data-stu-id="9163b-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="9163b-129">Дата изменения</span><span class="sxs-lookup"><span data-stu-id="9163b-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="9163b-130">Текущая; Устаревшее; Последний месяц; Более старые</span><span class="sxs-lookup"><span data-stu-id="9163b-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="9163b-131">Created Date (дата создания)</span><span class="sxs-lookup"><span data-stu-id="9163b-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="9163b-132">Текущая; Устаревшее; Последний месяц; Более старые</span><span class="sxs-lookup"><span data-stu-id="9163b-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="9163b-133">Настраиваемые категории</span><span class="sxs-lookup"><span data-stu-id="9163b-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="9163b-134">Имена групп, созданные для указанного настраиваемые категории</span><span class="sxs-lookup"><span data-stu-id="9163b-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="9163b-135">Чтобы выполнить действие **NavigateTo** в модуле VBA, используйте метод **NavigateTo** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="9163b-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="9163b-136">Чтобы перейти на верхний уровень категории (например, **Все таблицы**, **Все объекты доступа**или **Все даты**), аргумент группы необходимо оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="9163b-136">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank.</span></span> <span data-ttu-id="9163b-137">К примеру при аргумент **категории** — это **Тип объекта**, ввод **Всех объектов доступа** как аргумент **группы** , приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="9163b-137">For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


