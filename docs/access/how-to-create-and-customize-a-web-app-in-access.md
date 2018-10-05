---
title: Создание и настройка веб-приложения в Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
ms.openlocfilehash: d837a83ea8773018033a27ec894375a22c15c8a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391124"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="71f9b-102">Создание и настройка веб-приложения в Access</span><span class="sxs-lookup"><span data-stu-id="71f9b-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71f9b-103">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="71f9b-103">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="71f9b-104">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="71f9b-104">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="71f9b-105">Access 2013 компонентов новая модель приложения, которая позволяет экспертов для быстрого создания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-105">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications.</span></span> <span data-ttu-id="71f9b-106">Входит в состав доступа — это набор шаблонов, которые можно использовать для перехода приступить к созданию приложения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-106">Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="71f9b-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="71f9b-107"></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="71f9b-108">Предварительные требования для создания приложения с помощью Access 2013</span><span class="sxs-lookup"><span data-stu-id="71f9b-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="71f9b-109">Для выполнения действий, описанных в этом примере, вам потребуется следующее:</span><span class="sxs-lookup"><span data-stu-id="71f9b-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="71f9b-110">Access</span><span class="sxs-lookup"><span data-stu-id="71f9b-110">Access</span></span>
    
- <span data-ttu-id="71f9b-111">Среда разработки SharePoint</span><span class="sxs-lookup"><span data-stu-id="71f9b-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="71f9b-112">Дополнительные сведения о настройке среды разработки SharePoint видеть [настроить среду разработки, общие для SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span><span class="sxs-lookup"><span data-stu-id="71f9b-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="71f9b-113">Дополнительные сведения о получении доступа и SharePoint в разделе [файлов для загрузки](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="71f9b-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="71f9b-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="71f9b-114"></span></span>

## <a name="create-the-app"></a><span data-ttu-id="71f9b-115">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="71f9b-115">Create the app</span></span>

<span data-ttu-id="71f9b-116">Предположим, что вы хотите создать приложение Access, который отслеживает проблемы в бизнесе.</span><span class="sxs-lookup"><span data-stu-id="71f9b-116">Suppose you want to create an Access app that tracks issues for your business.</span></span> <span data-ttu-id="71f9b-117">Прежде чем начинать создание таблиц и представление «с нуля», необходимо найти шаблона схемы, который соответствует потребностям.</span><span class="sxs-lookup"><span data-stu-id="71f9b-117">Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="71f9b-118">Чтобы создать приложение отслеживания вопросов</span><span class="sxs-lookup"><span data-stu-id="71f9b-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="71f9b-119">Откройте доступ и выберите пункт **настраиваемых веб-приложения**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="71f9b-120">Введите имя и расположение веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-120">Enter a name and the web location for your app.</span></span> <span data-ttu-id="71f9b-121">Можно выбрать расположение из **списка** и выберите команду **Создать**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-121">You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="71f9b-122">**Проблемы** в **как для отслеживания?** поле и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="71f9b-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="71f9b-123">На рисунке 1 отображается список шаблонов, которые могут оказаться полезными для отслеживания проблем.</span><span class="sxs-lookup"><span data-stu-id="71f9b-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="71f9b-124">**На рисунке 1. Шаблоны, соответствующие поиску проблем**</span><span class="sxs-lookup"><span data-stu-id="71f9b-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="71f9b-125">![Шаблоны, соответствующие поиску проблем] (media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Шаблоны, соответствующие поиску проблем")</span><span class="sxs-lookup"><span data-stu-id="71f9b-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="71f9b-126">Выберите **проблемы**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="71f9b-127">Access создает набор таблиц и представлений.</span><span class="sxs-lookup"><span data-stu-id="71f9b-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="71f9b-128">Изучение приложения</span><span class="sxs-lookup"><span data-stu-id="71f9b-128">Explore the app</span></span>
<span data-ttu-id="71f9b-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="71f9b-129"></span></span>

<span data-ttu-id="71f9b-130">Чтобы понять, будет ли схемы и представления соответствии со своими потребностями, их следует проверить.</span><span class="sxs-lookup"><span data-stu-id="71f9b-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="71f9b-131">Таблицы, созданные путем выбора схемы "проблемы" отображаются в области заголовков.</span><span class="sxs-lookup"><span data-stu-id="71f9b-131">The tables created by selecting the Issues schema are displayed in the Tile Pane.</span></span> <span data-ttu-id="71f9b-132">В таблицах проблемы, клиентов и сотрудников — это основное внимание приложения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-132">The Issues, Customer, and Employees tables are the main focus of the app.</span></span> <span data-ttu-id="71f9b-133">В таблице ошибок хранятся сведения о каждой проблемы.</span><span class="sxs-lookup"><span data-stu-id="71f9b-133">The Issues table stores information about each issue.</span></span> <span data-ttu-id="71f9b-134">Каждая проблема открыто с и сотруднику от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="71f9b-134">Each issue is opened by and assigned to an employee on behalf of a customer.</span></span> <span data-ttu-id="71f9b-135">В таблицах связанные вопросы и комментарии проблему играют вспомогательные роль в приложении.</span><span class="sxs-lookup"><span data-stu-id="71f9b-135">The Related Issues and Issue Comments tables play a supporting role in the app.</span></span> <span data-ttu-id="71f9b-136">В таблице проблем, связанных с ними позволяет связать одна проблема в другую.</span><span class="sxs-lookup"><span data-stu-id="71f9b-136">The Related Issues table enables you to link one issue to another.</span></span> <span data-ttu-id="71f9b-137">В таблице комментариев проблему сохранение нескольких комментариев для одного проблемы.</span><span class="sxs-lookup"><span data-stu-id="71f9b-137">The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="71f9b-138">В базе данных Microsoft Access рабочего стола (.accdb) связи между таблицами осуществляется в окне **схемы** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-138">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window.</span></span> <span data-ttu-id="71f9b-139">Приложения Access 2013 управление отношениями с помощью поля, установите тип данных **подстановки** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-139">Access 2013 apps manage relationships by using fields set to the **Lookup** data type.</span></span> <span data-ttu-id="71f9b-140">Давайте рассмотрим связи для таблицы проблемы, щелкнув правой кнопкой мыши плитку **проблемы** и выбрав пункт **Изменение таблицы**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-140">Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="71f9b-141">Поле « **клиент** » относится к таблице **Customers** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-141">The **Customer** field is related to the **Customers** table.</span></span> <span data-ttu-id="71f9b-142">Для проверки связи, выберите поле **клиента** и затем выберите **Изменить операции поиска**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-142">To examine the relationship, select the **Customer** field and then select **Modify Lookups**.</span></span> <span data-ttu-id="71f9b-143">Появится **Мастер подстановок** , как показано на рисунке 2.</span><span class="sxs-lookup"><span data-stu-id="71f9b-143">The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="71f9b-144">**На рисунке 2. Мастер подстановок, отображающий отношение к таблице Customers**</span><span class="sxs-lookup"><span data-stu-id="71f9b-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="71f9b-145">![Мастер подстановок, отображающий связь] (media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Мастер подстановок, отображающий связь")</span><span class="sxs-lookup"><span data-stu-id="71f9b-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="71f9b-146">Диалоговое окно Мастер подстановок показывает, поле **клиента** связана к таблице **Customers** и возвращает **Отображаемое имя и фамилия** поля из таблицы **Customers** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="71f9b-147">**Открывается**, **Назначено**и **Кем изменено** относятся к таблице **Employees** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-147">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table.</span></span> <span data-ttu-id="71f9b-148">Несколько полей, также присваивается тип данных **поиска** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-148">Several other fields are also set to the **Lookup** data type.</span></span> <span data-ttu-id="71f9b-149">В таких случаях тип данных поиска используется для указания конкретного значения о предоставлении в соответствующем поле.</span><span class="sxs-lookup"><span data-stu-id="71f9b-149">In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="71f9b-150">Закройте таблица **вопросов** и просмотрите область плиток.</span><span class="sxs-lookup"><span data-stu-id="71f9b-150">Close the **Issues** table and examine the Tile Pane.</span></span> <span data-ttu-id="71f9b-151">Верхняя трех плиток для **проблемы**, **клиентами**и таблицы **сотрудников** , отображаются иначе, чем двух заголовков нижней для таблицы **Связанные вопросы** и **Комментарии проблему** , как показано на рисунке 3.</span><span class="sxs-lookup"><span data-stu-id="71f9b-151">The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="71f9b-152">**На рисунке 3. Область плиток для схемы "проблемы"**</span><span class="sxs-lookup"><span data-stu-id="71f9b-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="71f9b-153">![Область плиток для схемы проблем] (media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Область плиток для схемы проблем")</span><span class="sxs-lookup"><span data-stu-id="71f9b-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="71f9b-154">В таблицах **Связанные вопросы** и **Комментарии проблему** недоступны, поскольку они, должны быть скрыты от пользователя в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="71f9b-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="71f9b-155">Для отслеживания некоторые проблемы воспользуемся приложения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-155">Let's use the app to track some issues.</span></span> <span data-ttu-id="71f9b-156">Для этого нажмите кнопку **Запуск приложения** , чтобы открыть его в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="71f9b-156">To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="71f9b-157">Приложение откроется представление **Списка проблем** в таблице проблемы.</span><span class="sxs-lookup"><span data-stu-id="71f9b-157">The app opens the **Issues List** view of the Issues table.</span></span> <span data-ttu-id="71f9b-158">Перед добавлением проблему, будет полезно определить для добавления некоторых клиентов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="71f9b-158">Before adding an issue, it would be a good idea to add some customers and employees.</span></span> <span data-ttu-id="71f9b-159">Щелкните плитку **клиентов** , чтобы начать добавление клиентов.</span><span class="sxs-lookup"><span data-stu-id="71f9b-159">Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="71f9b-160">Выбор представления используйте для выберите один из трех представления, доступные в таблице **Customers** , обозначенный **списка**, **таблицы**и **группы** , как показано на рисунке 4.</span><span class="sxs-lookup"><span data-stu-id="71f9b-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="71f9b-161">**На рисунке 4. Выбор представления**</span><span class="sxs-lookup"><span data-stu-id="71f9b-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="71f9b-162">![Выбор представления] (media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Выбор представления")</span><span class="sxs-lookup"><span data-stu-id="71f9b-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="71f9b-163">Выбор **списка** активирует представления **Списка клиентов** , который является представлением списка сведений.</span><span class="sxs-lookup"><span data-stu-id="71f9b-163">Choosing **List** activates the **Customers List** view, which is a List Details view.</span></span> <span data-ttu-id="71f9b-164">Сведения о списке является одним из представлений, которые автоматически создается при создании таблицы.</span><span class="sxs-lookup"><span data-stu-id="71f9b-164">List Details is one of the views Access automatically generates when you create a table.</span></span> <span data-ttu-id="71f9b-165">Основной компонент, который отличает Просмотр сведений о списке является области списка, который отображается в левой части представления.</span><span class="sxs-lookup"><span data-stu-id="71f9b-165">The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view.</span></span> <span data-ttu-id="71f9b-166">В области списка используется для фильтрации и перемещаться по записям, содержащихся в представлении.</span><span class="sxs-lookup"><span data-stu-id="71f9b-166">The list pane is used to filter and navigate the records contained in the view.</span></span> <span data-ttu-id="71f9b-167">Базы данных доступа к рабочему столу реализация представления списка для поиска требуется написании пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="71f9b-167">In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="71f9b-168">Выбор **таблицы** откроется представление **Таблицы данных клиентов** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-168">Choosing **Datasheet** opens the **Customers Datasheet** view.</span></span> <span data-ttu-id="71f9b-169">Таблицы данных является другой тип представления, которое автоматически создается при создании таблицы.</span><span class="sxs-lookup"><span data-stu-id="71f9b-169">Datasheet is the other kind of view Access automatically generates when you create a table.</span></span> <span data-ttu-id="71f9b-170">Представления таблицы данных полезны для тех, кому удобным для ввода, отсортировать, и фильтрация данных в виде наподобие электронных таблиц.</span><span class="sxs-lookup"><span data-stu-id="71f9b-170">Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="71f9b-171">Выбор групп откроется представление сводки.</span><span class="sxs-lookup"><span data-stu-id="71f9b-171">Choosing Groups opens a Summary view.</span></span> <span data-ttu-id="71f9b-172">Сводного представления можно использовать для группировки записей на основе поля и при необходимости вычисление суммы или среднего.</span><span class="sxs-lookup"><span data-stu-id="71f9b-172">Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="71f9b-173">При добавлении пользователей, используйте панель действий для добавления записей, изменение записей, сохраните записей, удалить записи и отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-173">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits.</span></span> <span data-ttu-id="71f9b-174">Панель действий — настраиваемая панель инструментов, который отображается в верхней части каждого представления, как показано на рисунке 5.</span><span class="sxs-lookup"><span data-stu-id="71f9b-174">The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="71f9b-175">**На рисунке 5. Панель действий**</span><span class="sxs-lookup"><span data-stu-id="71f9b-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="71f9b-176">![Панель действий] (media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Панель действий")</span><span class="sxs-lookup"><span data-stu-id="71f9b-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="71f9b-177">Один раз вы добавили некоторые клиенты и сотрудники открыть представление списка проблем и начать добавление проблемы.</span><span class="sxs-lookup"><span data-stu-id="71f9b-177">Once you've added some customers and employees open the Issues List view and start adding an issue.</span></span> <span data-ttu-id="71f9b-178">При вводе имени клиента в в поле клиента одно или несколько имен клиентов будет отображаться, как показано на рисунке 6.</span><span class="sxs-lookup"><span data-stu-id="71f9b-178">As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="71f9b-179">**На рисунке 6. Элемент управления AutoComplete**</span><span class="sxs-lookup"><span data-stu-id="71f9b-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="71f9b-180">![Элемент управления AutoComplete] (media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Элемент управления AutoComplete")</span><span class="sxs-lookup"><span data-stu-id="71f9b-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="71f9b-181">В поле клиентов — это элемент управления AutoComplete.</span><span class="sxs-lookup"><span data-stu-id="71f9b-181">The Customer box is an AutoComplete control.</span></span> <span data-ttu-id="71f9b-182">Элемент управления AutoComplete отображается список записей, которые соответствуют заполнять вводимые в поле.</span><span class="sxs-lookup"><span data-stu-id="71f9b-182">The AutoComplete control displays a list of records that match what you're typing into the box.</span></span> <span data-ttu-id="71f9b-183">Это позволяет обеспечить точность ввода данных.</span><span class="sxs-lookup"><span data-stu-id="71f9b-183">This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="71f9b-184">Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="71f9b-184">Customize the app</span></span>
<span data-ttu-id="71f9b-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="71f9b-185"></span></span>

<span data-ttu-id="71f9b-186">Теперь, когда вы извлекли тур приложения, вы Обратите внимание на то, что представление списка проблемы не содержит контактные данные для клиента.</span><span class="sxs-lookup"><span data-stu-id="71f9b-186">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer.</span></span> <span data-ttu-id="71f9b-187">Настроим приложение, чтобы добавить рабочий телефон клиента в таблицу проблемы при создании проблему.</span><span class="sxs-lookup"><span data-stu-id="71f9b-187">Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="71f9b-188">Добавление поля в таблице проблемы</span><span class="sxs-lookup"><span data-stu-id="71f9b-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="71f9b-189">Откройте приложение в Access.</span><span class="sxs-lookup"><span data-stu-id="71f9b-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="71f9b-190">Выберите плитку **проблемы** , выберите значок **Параметры и действия** и выберите **Изменение таблицы**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="71f9b-191">Введите **Номер контакта** в ячейку в столбце **Имя поля** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="71f9b-192">Выберите **Короткий текст** в столбце **Тип данных** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="71f9b-193">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="71f9b-194">Закройте таблица вопросов.</span><span class="sxs-lookup"><span data-stu-id="71f9b-194">Close the Issues table.</span></span>
    
<span data-ttu-id="71f9b-195">Теперь, когда у нас есть поля, в которых хранятся номер телефона, давайте создадим макрос данных, чтобы найти контактные сведения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="71f9b-196">Чтобы создать макрос данных, чтобы найти контактные сведения</span><span class="sxs-lookup"><span data-stu-id="71f9b-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="71f9b-197">В группе **Создание** нажмите кнопку **Дополнительно**и выберите **Макрос данных**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="71f9b-198">Выберите **параметр Создать**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="71f9b-199">В поле **имя** введите **CustID**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-199">In the **Name** box, enter **CustID**.</span></span> <span data-ttu-id="71f9b-200">В раскрывающемся списке **Тип** выберите **(с плавающей десятичных знаков).**</span><span class="sxs-lookup"><span data-stu-id="71f9b-200">In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="71f9b-201">В раскрывающемся списке **Добавить действие** выберите **макрокомандой НайтиЗапись, после**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="71f9b-202">В раскрывающемся списке **Поиск копирование записи в** выберите **клиентов**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="71f9b-203">В поле **Условие отбора** введите **[клиенты]. [ Идентификатор] = [CustID]**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="71f9b-204">Выберите **SetReturnVar** из раскрывающегося списка **Добавить действие** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="71f9b-205">Вы увидите два **Добавления нового действия** раскрывающихся списков, один внутри блока **макрокомандой НайтиЗапись, после** и другой вне блока **макрокомандой НайтиЗапись, после** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-205">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="71f9b-206">Следует выбрать в раскрывающемся списке **Добавить действие** в блоке **макрокомандой НайтиЗапись, после** , как показано на рисунке 7.</span><span class="sxs-lookup"><span data-stu-id="71f9b-206">You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="71f9b-207">**На рисунке 7. Добавление нового действия раскрывающийся список**</span><span class="sxs-lookup"><span data-stu-id="71f9b-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="71f9b-208">![Добавление нового действия раскрывающийся список] (media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Добавление нового действия раскрывающийся список")</span><span class="sxs-lookup"><span data-stu-id="71f9b-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="71f9b-209">В поле **имя** введите **ContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="71f9b-210">Введите в поле **выражение** **[клиенты]. [ Номер рабочего телефона]**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="71f9b-211">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-211">Choose **Save**.</span></span> <span data-ttu-id="71f9b-212">В поле **Имя** введите **GetContactPhone** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-212">Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="71f9b-213">Макрос должен выглядеть макрос, показано на рисунке 8.</span><span class="sxs-lookup"><span data-stu-id="71f9b-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="71f9b-214">**На рисунке 8. Макрос данных getcontactphone**</span><span class="sxs-lookup"><span data-stu-id="71f9b-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="71f9b-215">![Макрос данных getcontactphone] (media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Макрос данных getcontactphone")</span><span class="sxs-lookup"><span data-stu-id="71f9b-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="71f9b-216">Закрытие конструктора макроса.</span><span class="sxs-lookup"><span data-stu-id="71f9b-216">Close macro Design View.</span></span>
    
<span data-ttu-id="71f9b-217">Теперь мы готовы для добавления в поле **Номер контакта** к форме списка вопросов.</span><span class="sxs-lookup"><span data-stu-id="71f9b-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="71f9b-218">Чтобы добавить поле номер контакта к форме списка вопросов</span><span class="sxs-lookup"><span data-stu-id="71f9b-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="71f9b-219">Выберите таблицу **проблемы** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-219">Choose the **Issues** table.</span></span> <span data-ttu-id="71f9b-220">Это выбирает формы списка проблем.</span><span class="sxs-lookup"><span data-stu-id="71f9b-220">This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="71f9b-221">Выбор представления в выберите **список**, выберите значок **Параметры и действия** и выберите команду **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="71f9b-222">Перетащите элемент **Контактов номер** поля формы области **Список полей** расположения в форме место номер контакта для отображения.</span><span class="sxs-lookup"><span data-stu-id="71f9b-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="71f9b-223">Выберите **Номер контакта** текстовое поле и нажмите кнопку **данных**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="71f9b-224">В поле **Имя элемента управления** ввода **CustomerContact** , а затем закройте меню " **данные** ".</span><span class="sxs-lookup"><span data-stu-id="71f9b-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="71f9b-225">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-225">Choose **Save**.</span></span>
    
<span data-ttu-id="71f9b-226">Теперь следует написать макрос пользовательского интерфейса пользователя, который копируется в поле **Рабочий телефон** из таблицы **Customers** в поле **Телефон контакта** таблицы **проблемы** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-226">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table.</span></span> <span data-ttu-id="71f9b-227">**После обновления** события элемента управления **CustomerAutocomplete** — это удобное место для макроса.</span><span class="sxs-lookup"><span data-stu-id="71f9b-227">The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="71f9b-228">Чтобы создать макрос после обновления</span><span class="sxs-lookup"><span data-stu-id="71f9b-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="71f9b-229">Выберите элемент управления **CustomerAutocomplete** , нажмите кнопку **действия** и выберите **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="71f9b-230">Пустой макрос открывается в режиме конструктора макросов.</span><span class="sxs-lookup"><span data-stu-id="71f9b-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="71f9b-231">В раскрывающемся списке **Добавить действие** выберите **ЗапускМакросаДанных**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="71f9b-232">Выберите в раскрывающемся списке **Имя макроса** **GetContactPhone**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="71f9b-233">В поле **CustID** введите **[CustomerAutocomplete]**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="71f9b-234">В поле **SetLocalVar** введите **Телефон**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="71f9b-235">При выборе данных getcontactphone, который был создан ранее, Access автоматически введено имя параметра и возврат переменной для макроса.</span><span class="sxs-lookup"><span data-stu-id="71f9b-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="71f9b-236">Номер телефона для клиента, хранящиеся в переменной с именем телефона.</span><span class="sxs-lookup"><span data-stu-id="71f9b-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="71f9b-237">В раскрывающемся списке **Добавить действие** выберите **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="71f9b-238">В поле **Имя элемента управления** введите **CustomerContact**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="71f9b-239">В раскрывающемся списке **Свойства** выберите **значение**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="71f9b-240">В поле **значение** введите **= [Телефон]**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="71f9b-241">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="71f9b-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="71f9b-242">Макрос должен выглядеть макрос, показано на рисунке 9.</span><span class="sxs-lookup"><span data-stu-id="71f9b-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="71f9b-243">**На рисунке 9. Макрос после обновления**</span><span class="sxs-lookup"><span data-stu-id="71f9b-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="71f9b-244">![Макрос после обновления] (media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Макрос после обновления")</span><span class="sxs-lookup"><span data-stu-id="71f9b-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="71f9b-245">Закрытие конструктора макроса.</span><span class="sxs-lookup"><span data-stu-id="71f9b-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="71f9b-246">Закройте представление списка проблем.</span><span class="sxs-lookup"><span data-stu-id="71f9b-246">Close the Issues List view.</span></span> <span data-ttu-id="71f9b-247">Когда вам будет предложено сохранить изменения, нажмите кнопку **Да** .</span><span class="sxs-lookup"><span data-stu-id="71f9b-247">Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="71f9b-248">Теперь мы готовы к тексту настройки.</span><span class="sxs-lookup"><span data-stu-id="71f9b-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="71f9b-249">Нажмите кнопку **Запуск приложения** откройте приложение в веб-браузере и добавьте новый вопрос.</span><span class="sxs-lookup"><span data-stu-id="71f9b-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="71f9b-250">Обновления поля **Номер контакта** , автоматически после того, как введено имя клиента, как показано на рисунке 10.</span><span class="sxs-lookup"><span data-stu-id="71f9b-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="71f9b-251">**На рисунке 10. Представление проблем с обновленным номером телефона**</span><span class="sxs-lookup"><span data-stu-id="71f9b-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="71f9b-252">![Представление проблем с обновленным номером телефона] (media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Представление проблем с обновленным номером телефона")</span><span class="sxs-lookup"><span data-stu-id="71f9b-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="71f9b-253">Заключение</span><span class="sxs-lookup"><span data-stu-id="71f9b-253">Conclusion</span></span>

<span data-ttu-id="71f9b-254">С помощью одного из шаблонов схемы, входящих в состав — это удобный способ перехода начать создание приложение web Access.</span><span class="sxs-lookup"><span data-stu-id="71f9b-254">Using one of the schema templates included with is a good way to jump start the creation of an Access web app.</span></span> <span data-ttu-id="71f9b-255">Представления, которые автоматически создаются для вы содержать функционально Дополнительно, которые требуется пользовательский код для реализации в базе данных доступа к рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="71f9b-255">The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71f9b-256">См. также</span><span class="sxs-lookup"><span data-stu-id="71f9b-256">See also</span></span>

- [<span data-ttu-id="71f9b-257">Новые возможности для разработчиков Access 2013</span><span class="sxs-lookup"><span data-stu-id="71f9b-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="71f9b-258">Access custom web app reference</span><span class="sxs-lookup"><span data-stu-id="71f9b-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

