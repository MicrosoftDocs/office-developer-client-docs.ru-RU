---
title: Создание и настройка веб-приложения в Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
localization_priority: Priority
ms.openlocfilehash: d7d27e98189a5b6784e4db48c81a545b85f01fc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306139"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="fdae4-102">Создание и настройка веб-приложения в Access</span><span class="sxs-lookup"><span data-stu-id="fdae4-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdae4-103">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fdae4-103">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="fdae4-104">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-RU/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="fdae4-104">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-RU/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="fdae4-105">Access 2013 содержит новую модель приложения, позволяющую экспертам быстро создавать веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-105">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications.</span></span> <span data-ttu-id="fdae4-106">В состав Access включен набор шаблонов, которые можно использовать для быстрого создания приложения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-106">Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="fdae4-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="fdae4-107"></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="fdae4-108">Предварительные требования для создания приложения с помощью Access 2013</span><span class="sxs-lookup"><span data-stu-id="fdae4-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="fdae4-109">Для выполнения действий, описанных в этом примере, вам потребуется следующее:</span><span class="sxs-lookup"><span data-stu-id="fdae4-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="fdae4-110">Access</span><span class="sxs-lookup"><span data-stu-id="fdae4-110">Access</span></span>
    
- <span data-ttu-id="fdae4-111">Среда разработки SharePoint</span><span class="sxs-lookup"><span data-stu-id="fdae4-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="fdae4-112">Дополнительные сведения о настройке среды разработки SharePoint см. в статье [Настройка общей среды разработки для SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span><span class="sxs-lookup"><span data-stu-id="fdae4-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="fdae4-113">Дополнительные сведения о получении Access и SharePoint см. в [Загрузках](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="fdae4-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="fdae4-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="fdae4-114"></span></span>

## <a name="create-the-app"></a><span data-ttu-id="fdae4-115">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="fdae4-115">Create the app</span></span>

<span data-ttu-id="fdae4-116">Предположим, что вы хотите создать приложение Access, отслеживающее проблемы в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fdae4-116">Suppose you want to create an Access app that tracks issues for your business.</span></span> <span data-ttu-id="fdae4-117">Перед созданием таблиц и представлений с нуля следует выполнить поиск шаблона схемы, соответствующего вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="fdae4-117">Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="fdae4-118">Создание приложения, отслеживающего проблемы</span><span class="sxs-lookup"><span data-stu-id="fdae4-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="fdae4-119">Запустите Access и выберите вариант **Пользовательское веб-приложение**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="fdae4-120">Введите имя и веб-адрес вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-120">Enter a name and the web location for your app.</span></span> <span data-ttu-id="fdae4-121">Либо выберите расположение из списка **Доступные места** и нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-121">You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="fdae4-122">Введите **Проблемы** в поле **Что нужно отслеживать?** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="fdae4-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="fdae4-123">Список шаблонов, которые могут помочь с отслеживанием проблем, показан на рисунке 1.</span><span class="sxs-lookup"><span data-stu-id="fdae4-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="fdae4-124">**Рисунок 1. Шаблоны, с помощью которых выполняется поиск проблем**</span><span class="sxs-lookup"><span data-stu-id="fdae4-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="fdae4-125">![Шаблоны, с помощью которых выполняется поиск проблем](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Шаблоны, с помощью которых выполняется поиск проблем")</span><span class="sxs-lookup"><span data-stu-id="fdae4-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="fdae4-126">Выберите **Проблемы**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="fdae4-127">Access создает набор таблиц и представлений.</span><span class="sxs-lookup"><span data-stu-id="fdae4-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="fdae4-128">Обзор приложения</span><span class="sxs-lookup"><span data-stu-id="fdae4-128">Explore the app</span></span>
<span data-ttu-id="fdae4-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="fdae4-129"></span></span>

<span data-ttu-id="fdae4-130">Чтобы понять, соответствует ли схема и представления вашим требованиям, следует их рассмотреть подробнее.</span><span class="sxs-lookup"><span data-stu-id="fdae4-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="fdae4-131">Таблицы, созданные при выборе схемы "Проблемы", отображаются в панели плиток.</span><span class="sxs-lookup"><span data-stu-id="fdae4-131">The tables created by selecting the Issues schema are displayed in the Tile Pane.</span></span> <span data-ttu-id="fdae4-132">Таблицы "Проблемы", "Клиент" и "Сотрудники" являются основными для приложения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-132">The Issues, Customer, and Employees tables are the main focus of the app.</span></span> <span data-ttu-id="fdae4-133">В таблице "Проблемы" хранятся сведения о каждой проблеме.</span><span class="sxs-lookup"><span data-stu-id="fdae4-133">The Issues table stores information about each issue.</span></span> <span data-ttu-id="fdae4-134">Каждая проблема открывается и назначается сотруднику от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="fdae4-134">Each issue is opened by and assigned to an employee on behalf of a customer.</span></span> <span data-ttu-id="fdae4-135">Таблицы "Связанные проблемы" и "Комментарии к проблеме" играют вспомогательную роль в приложении.</span><span class="sxs-lookup"><span data-stu-id="fdae4-135">The Related Issues and Issue Comments tables play a supporting role in the app.</span></span> <span data-ttu-id="fdae4-136">Таблица "Связанные проблемы" позволяет связывать одну проблему с другой.</span><span class="sxs-lookup"><span data-stu-id="fdae4-136">The Related Issues table enables you to link one issue to another.</span></span> <span data-ttu-id="fdae4-137">Таблица "Комментарии к проблеме" хранит несколько примечаний к одной проблеме.</span><span class="sxs-lookup"><span data-stu-id="fdae4-137">The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="fdae4-138">В базе данных Access на компьютере (ACCDB) связи между таблицами управляются в окне **Связи**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-138">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window.</span></span> <span data-ttu-id="fdae4-139">Приложение Access 2013 управляет связями с помощью полей с присвоенным типом данных **Lookup**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-139">Access 2013 apps manage relationships by using fields set to the **Lookup** data type.</span></span> <span data-ttu-id="fdae4-140">Проверить связи таблицы "Проблемы" можно, щелкнув правой кнопки мыши плитку **Проблемы** и выбрав пункт **Изменить таблицу**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-140">Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="fdae4-141">Поле **Клиент** связано с таблицей **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-141">The **Customer** field is related to the **Customers** table.</span></span> <span data-ttu-id="fdae4-142">Чтобы проверить связь, выберите поле **Клиент** и нажмите кнопку **Изменить подстановку**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-142">To examine the relationship, select the **Customer** field and then select **Modify Lookups**.</span></span> <span data-ttu-id="fdae4-143">Отобразится **Мастер подстановок**, как показано на рисунке 2.</span><span class="sxs-lookup"><span data-stu-id="fdae4-143">The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="fdae4-144">**Рисунок 2. Мастер подстановок, отображающий связь с таблицей "Клиенты"**</span><span class="sxs-lookup"><span data-stu-id="fdae4-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="fdae4-145">![Мастер подстановок, отображающий связь](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Мастер подстановок, отображающий связь")</span><span class="sxs-lookup"><span data-stu-id="fdae4-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="fdae4-146">Диалоговое окно мастера подстановок показывает, что поле **Клиент** связано с таблицей **Клиенты** и должно возвращаться поле **Отображаемое имя: Имя Фамилия** из таблицы **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="fdae4-147">Поля **Создано**, **Назначено** и **Изменено** относятся к таблице **Сотрудники**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-147">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table.</span></span> <span data-ttu-id="fdae4-148">Нескольким другим полям также присвоен тип данных **Lookup**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-148">Several other fields are also set to the **Lookup** data type.</span></span> <span data-ttu-id="fdae4-149">В этих случаях тип данных Lookup используется для указания конкретных значений, допустимых в поле.</span><span class="sxs-lookup"><span data-stu-id="fdae4-149">In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="fdae4-150">Закройте таблицу **Проблемы** и просмотрите панель плиток.</span><span class="sxs-lookup"><span data-stu-id="fdae4-150">Close the **Issues** table and examine the Tile Pane.</span></span> <span data-ttu-id="fdae4-151">Отображение верхних трех плиток для таблиц **Проблемы**, **Клиенты** и **Сотрудники** отличается от нижних двух плиток для таблиц **Связанные проблемы** и **Комментарии о проблеме**, как показано на рисунке 3.</span><span class="sxs-lookup"><span data-stu-id="fdae4-151">The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="fdae4-152">**Рисунок 3. Панель плиток для схемы "Проблемы"**</span><span class="sxs-lookup"><span data-stu-id="fdae4-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="fdae4-153">![Панель плиток для схемы "Проблемы"](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Панель плиток для схемы \"Проблемы\"")</span><span class="sxs-lookup"><span data-stu-id="fdae4-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="fdae4-154">Таблицы **Связанные проблемы** и **Комментарии о проблеме** затемнены, так как они скрыты от пользователей в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="fdae4-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="fdae4-155">Воспользуемся приложением для отслеживания некоторых проблем.</span><span class="sxs-lookup"><span data-stu-id="fdae4-155">Let's use the app to track some issues.</span></span> <span data-ttu-id="fdae4-156">Для этого щелкните пункт **Запустить приложение**, чтобы открыть приложение в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="fdae4-156">To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="fdae4-157">Приложение откроет представление **Список проблем** таблицы "Проблемы".</span><span class="sxs-lookup"><span data-stu-id="fdae4-157">The app opens the **Issues List** view of the Issues table.</span></span> <span data-ttu-id="fdae4-158">Прежде чем добавить проблему рекомендуется добавить несколько клиентов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="fdae4-158">Before adding an issue, it would be a good idea to add some customers and employees.</span></span> <span data-ttu-id="fdae4-159">Щелкните плитку **Клиенты**, чтобы начать добавление клиентов.</span><span class="sxs-lookup"><span data-stu-id="fdae4-159">Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="fdae4-160">С помощью средства выбора представления выберите одно из трех представлений, доступных для таблицы **Клиенты**, с именами **Список**, **Таблица** и **Группы**, как показано на рисунке 4.</span><span class="sxs-lookup"><span data-stu-id="fdae4-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="fdae4-161">**Рисунок 4. Выбор представления**</span><span class="sxs-lookup"><span data-stu-id="fdae4-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="fdae4-162">![Выбор представления](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Выбор представления")</span><span class="sxs-lookup"><span data-stu-id="fdae4-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="fdae4-163">Выбор варианта **Список** активирует представление **Список клиентов**, являющееся представлением со сведениями о списке.</span><span class="sxs-lookup"><span data-stu-id="fdae4-163">Choosing **List** activates the **Customers List** view, which is a List Details view.</span></span> <span data-ttu-id="fdae4-164">Сведения о списке — одно из представлений, которое Access автоматически создает при создании таблицы.</span><span class="sxs-lookup"><span data-stu-id="fdae4-164">List Details is one of the views Access automatically generates when you create a table.</span></span> <span data-ttu-id="fdae4-165">Основной функцией, отличающей представление "Сведения о списке", является область списка, отображающаяся в левой части представления.</span><span class="sxs-lookup"><span data-stu-id="fdae4-165">The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view.</span></span> <span data-ttu-id="fdae4-166">Область списка используется для фильтрации и перехода к записям, содержащимся в представлении.</span><span class="sxs-lookup"><span data-stu-id="fdae4-166">The list pane is used to filter and navigate the records contained in the view.</span></span> <span data-ttu-id="fdae4-167">В базе данных Access на компьютере реализация представления списка с возможностью поиска потребует написания пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="fdae4-167">In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="fdae4-168">При выборе варианта **Таблица** откроется представление **Таблица клиентов**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-168">Choosing **Datasheet** opens the **Customers Datasheet** view.</span></span> <span data-ttu-id="fdae4-169">Таблица — это другой тип представления, которое Access автоматически создает при создании таблицы.</span><span class="sxs-lookup"><span data-stu-id="fdae4-169">Datasheet is the other kind of view Access automatically generates when you create a table.</span></span> <span data-ttu-id="fdae4-170">Табличные представления удобны для тех, кому проще вводить, сортировать и фильтровать данные в электронной таблице.</span><span class="sxs-lookup"><span data-stu-id="fdae4-170">Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="fdae4-171">При выборе варианта "Группы" откроется сводное представление.</span><span class="sxs-lookup"><span data-stu-id="fdae4-171">Choosing Groups opens a Summary view.</span></span> <span data-ttu-id="fdae4-172">Сводные представления можно использовать для группировки записей на основе поля и выбора вычисления суммы или среднего значения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-172">Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="fdae4-173">Если вы добавляете клиентов, используйте панель действий, чтобы добавлять, изменять, сохранять и удалять записи, а также отменять изменения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-173">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits.</span></span> <span data-ttu-id="fdae4-174">Панель действий — это настраиваемая панель инструментов, которая отображается в верхней части каждого представления, как показано на рисунке 5.</span><span class="sxs-lookup"><span data-stu-id="fdae4-174">The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="fdae4-175">**Рисунок 5. Панель действий**</span><span class="sxs-lookup"><span data-stu-id="fdae4-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="fdae4-176">![Панель действий](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Панель действий")</span><span class="sxs-lookup"><span data-stu-id="fdae4-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="fdae4-177">После добавления нескольких клиентов и сотрудников откройте представление "Список проблем" и начните добавление проблемы.</span><span class="sxs-lookup"><span data-stu-id="fdae4-177">Once you've added some customers and employees open the Issues List view and start adding an issue.</span></span> <span data-ttu-id="fdae4-178">При вводе имени клиента в поле "Клиент" появится одно или несколько имен клиентов, как показано на рисунке 6.</span><span class="sxs-lookup"><span data-stu-id="fdae4-178">As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="fdae4-179">**Рисунок 6. Элемент управления AutoComplete**</span><span class="sxs-lookup"><span data-stu-id="fdae4-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="fdae4-180">![Элемент управления AutoComplete](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Элемент управления AutoComplete")</span><span class="sxs-lookup"><span data-stu-id="fdae4-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="fdae4-181">Поле "Клиент" — это элемент управления AutoComplete.</span><span class="sxs-lookup"><span data-stu-id="fdae4-181">The Customer box is an AutoComplete control.</span></span> <span data-ttu-id="fdae4-182">Элемент управления AutoComplete отображает список записей, соответствующих вводимому в поле тексту.</span><span class="sxs-lookup"><span data-stu-id="fdae4-182">The AutoComplete control displays a list of records that match what you're typing into the box.</span></span> <span data-ttu-id="fdae4-183">Это помогает обеспечить точность ввода данных.</span><span class="sxs-lookup"><span data-stu-id="fdae4-183">This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="fdae4-184">Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="fdae4-184">Customize the app</span></span>
<span data-ttu-id="fdae4-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="fdae4-185"></span></span>

<span data-ttu-id="fdae4-186">После обзора приложения вы можете заметить, что в представлении "Список проблем" нет контактных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="fdae4-186">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer.</span></span> <span data-ttu-id="fdae4-187">Настроим приложение, чтобы добавлять рабочий телефон клиента в таблицу "Проблемы" при создании проблемы.</span><span class="sxs-lookup"><span data-stu-id="fdae4-187">Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="fdae4-188">Добавление поля в таблицу "Проблемы"</span><span class="sxs-lookup"><span data-stu-id="fdae4-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="fdae4-189">Откройте приложение в Access.</span><span class="sxs-lookup"><span data-stu-id="fdae4-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="fdae4-190">Выберите плитку **Проблемы**, щелкните значок **Параметры/действие** и нажмите кнопку **Изменить таблицу**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="fdae4-191">Введите **Номер контакта** в первой пустой ячейке столбца **Имя поля**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="fdae4-192">Выберите вариант **Короткий текст** в столбце **Тип данных**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="fdae4-193">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="fdae4-194">Закройте таблицу "Проблемы".</span><span class="sxs-lookup"><span data-stu-id="fdae4-194">Close the Issues table.</span></span>
    
<span data-ttu-id="fdae4-195">Теперь, когда есть поле для сохранения номера телефона, создадим макрос данных для поиска контактных данных.</span><span class="sxs-lookup"><span data-stu-id="fdae4-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="fdae4-196">Создание макроса данных для поиска контактных данных</span><span class="sxs-lookup"><span data-stu-id="fdae4-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="fdae4-197">В группе **Создание** выберите **Дополнительно**, а затем **Макрос данных**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="fdae4-198">Выберите **Создать параметр**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="fdae4-199">В поле **Имя** введите **CustID**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-199">In the **Name** box, enter **CustID**.</span></span> <span data-ttu-id="fdae4-200">В раскрывающемся списке **Тип** выберите **Число (десятичное с плавающей запятой).**</span><span class="sxs-lookup"><span data-stu-id="fdae4-200">In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="fdae4-201">В раскрывающемся списке **Добавить новую макрокоманду** выберите пункт **НайтиЗапись**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="fdae4-202">В раскрывающемся списке **Найти запись в** выберите пункт **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="fdae4-203">В поле **Условие отбора** введите **[Клиенты].[ID]=[CustID]**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="fdae4-204">Выберите **SetReturnVar** в раскрывающемся списке **Добавить новую макрокоманду**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="fdae4-205">Появится два раскрывающихся списка **Добавить новую макрокоманду**: один в блоке **НайтиЗапись**, а другой за его пределами.</span><span class="sxs-lookup"><span data-stu-id="fdae4-205">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="fdae4-206">Следует выбрать раскрывающийся список **Добавить новую макрокоманду** в блоке **НайтиЗапись**, как показано на рисунке 7.</span><span class="sxs-lookup"><span data-stu-id="fdae4-206">You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="fdae4-207">**Рисунок 7. Раскрывающееся меню "Добавить новую макрокоманду"**</span><span class="sxs-lookup"><span data-stu-id="fdae4-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="fdae4-208">![Раскрывающееся меню "Добавить новую макрокоманду"](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Раскрывающееся меню \"Добавить новую макрокоманду\"")</span><span class="sxs-lookup"><span data-stu-id="fdae4-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="fdae4-209">В поле **Имя** введите **ContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="fdae4-210">В поле **Выражение** введите **[Клиенты].[Рабочий телефон]**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="fdae4-211">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-211">Choose **Save**.</span></span> <span data-ttu-id="fdae4-212">Введите **GetContactPhone** в поле **Имя макроса** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-212">Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="fdae4-213">Макрос должен выглядеть примерно как на рисунке 8.</span><span class="sxs-lookup"><span data-stu-id="fdae4-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="fdae4-214">**Рисунок 8. Макрос данных GetContactPhone**</span><span class="sxs-lookup"><span data-stu-id="fdae4-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="fdae4-215">![Макрос данных GetContactPhone](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Макрос данных GetContactPhone")</span><span class="sxs-lookup"><span data-stu-id="fdae4-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="fdae4-216">Закройте представление "Конструктор" макроса.</span><span class="sxs-lookup"><span data-stu-id="fdae4-216">Close macro Design View.</span></span>
    
<span data-ttu-id="fdae4-217">Теперь можно добавить поле **Номер контакта** в форму "Список проблем".</span><span class="sxs-lookup"><span data-stu-id="fdae4-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="fdae4-218">Добавление поля "Номер контакта" в форму "Список проблем"</span><span class="sxs-lookup"><span data-stu-id="fdae4-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="fdae4-219">Откройте таблицу **Проблемы**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-219">Choose the **Issues** table.</span></span> <span data-ttu-id="fdae4-220">При этом будет выбрана форма "Список проблем".</span><span class="sxs-lookup"><span data-stu-id="fdae4-220">This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="fdae4-221">В средстве выбора представления выберите **Список**, щелкните значок **Параметры/действие** и нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="fdae4-222">Перетащите поле **Номер контакта** из области **Список полей** в нужное место отображения номера контакта.</span><span class="sxs-lookup"><span data-stu-id="fdae4-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="fdae4-223">Выберите поле **Номер контакта** и щелкните **Данные**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="fdae4-224">В поле **Имя элемента** введите **CustomerContact** и закройте всплывающее окно **Данные**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="fdae4-225">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-225">Choose **Save**.</span></span>
    
<span data-ttu-id="fdae4-226">Теперь нужно создать макрос пользовательского интерфейса, который копирует поле **Рабочий телефон** из таблицы **Клиенты** в поле **Телефон контакта** таблицы **Проблемы**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-226">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table.</span></span> <span data-ttu-id="fdae4-227">Событие **После обновления** элемента управления **CustomerAutocomplete** является хорошим расположением для макроса.</span><span class="sxs-lookup"><span data-stu-id="fdae4-227">The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="fdae4-228">Создание макроса "После обновления"</span><span class="sxs-lookup"><span data-stu-id="fdae4-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="fdae4-229">Выберите элемент управления **CustomerAutocomplete**, нажмите кнопку **Действия** и выберите **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="fdae4-230">Откроется пустой макрос в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="fdae4-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="fdae4-231">В раскрывающемся списке **Добавить новую макрокоманду** выберите пункт **ЗапускМакросаДанных**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="fdae4-232">В раскрывающемся списке **Имя макроса** выберите **GetContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="fdae4-233">В поле **CustID** введите **[CustomerAutocomplete]**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="fdae4-234">В поле **ЗадатьЛокПеременную** введите **Телефон**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="fdae4-235">Если вы выбрали макрос данных GetContactPhone, созданный ранее, Access автоматически заполнит параметр имени и вернет переменную для макроса.</span><span class="sxs-lookup"><span data-stu-id="fdae4-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="fdae4-236">Номер телефона клиента хранится в переменной с именем "Телефон".</span><span class="sxs-lookup"><span data-stu-id="fdae4-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="fdae4-237">В раскрывающемся списке **Добавить новую макрокоманду** выберите пункт **ЗадатьСвойство**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="fdae4-238">В поле **Имя элемента** введите **CustomerContact**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="fdae4-239">В раскрывающемся списке **Свойство** выберите **Значение**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="fdae4-240">В поле **Значение** введите **=[Телефон]**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="fdae4-241">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fdae4-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="fdae4-242">Макрос должен выглядеть примерно как на рисунке 9.</span><span class="sxs-lookup"><span data-stu-id="fdae4-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="fdae4-243">**Рисунок 9. Макрос "После обновления"**</span><span class="sxs-lookup"><span data-stu-id="fdae4-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="fdae4-244">![Макрос "После обновления"](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Макрос \"После обновления\"")</span><span class="sxs-lookup"><span data-stu-id="fdae4-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="fdae4-245">Закройте представление "Конструктор" макроса.</span><span class="sxs-lookup"><span data-stu-id="fdae4-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="fdae4-246">Закройте представление "Список проблем".</span><span class="sxs-lookup"><span data-stu-id="fdae4-246">Close the Issues List view.</span></span> <span data-ttu-id="fdae4-247">Выберите **Да**, когда будет предложено сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="fdae4-247">Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="fdae4-248">Теперь все готово для проверки настроек.</span><span class="sxs-lookup"><span data-stu-id="fdae4-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="fdae4-249">Щелкните пункт **Запустить приложение**, чтобы открыть приложение в веб-браузере, и добавьте новую проблему.</span><span class="sxs-lookup"><span data-stu-id="fdae4-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="fdae4-250">Поле **Номер контакта** автоматически обновляется после ввода имени клиента, как показано на рисунке 10.</span><span class="sxs-lookup"><span data-stu-id="fdae4-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="fdae4-251">**Рисунок 10. Представление "Проблемы", в которое добавлен номер телефона**</span><span class="sxs-lookup"><span data-stu-id="fdae4-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="fdae4-252">![Представление "Проблемы", в которое добавлен номер телефона](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Представление \"Проблемы\", в которое добавлен номер телефона")</span><span class="sxs-lookup"><span data-stu-id="fdae4-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="fdae4-253">Заключение</span><span class="sxs-lookup"><span data-stu-id="fdae4-253">Conclusion</span></span>

<span data-ttu-id="fdae4-254">Использование одного из имеющихся шаблонов схемы — это отличный способ быстро перейти к созданию веб-приложения Access.</span><span class="sxs-lookup"><span data-stu-id="fdae4-254">Using one of the schema templates included with is a good way to jump start the creation of an Access web app.</span></span> <span data-ttu-id="fdae4-255">Автоматически создаваемые представления содержат расширенные функции, требующие использования пользовательского кода для реализации в базе данных Access на компьютере.</span><span class="sxs-lookup"><span data-stu-id="fdae4-255">The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fdae4-256">См. также</span><span class="sxs-lookup"><span data-stu-id="fdae4-256">See also</span></span>

- [<span data-ttu-id="fdae4-257">Новые возможности для разработчиков Access 2013</span><span class="sxs-lookup"><span data-stu-id="fdae4-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="fdae4-258">Справочник по пользовательским веб-приложениям для Access</span><span class="sxs-lookup"><span data-stu-id="fdae4-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

