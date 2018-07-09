---
title: Фильтрация представления с помощью макроса в приложение Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: db4dbb71-1b22-4dfd-bc07-5f7d694fc038
description: Узнайте, как для фильтрации представления в приложение Access с помощью действия макроса RequeryRecords и макрос данных.
ms.openlocfilehash: 9cd8c74b3949a0bb496798df663b1b42fb2868d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806998"
---
# <a name="filter-a-view-by-using-a-macro-in-an-access-app"></a><span data-ttu-id="94228-103">Фильтрация представления с помощью макроса в приложение Access</span><span class="sxs-lookup"><span data-stu-id="94228-103">Filter a view by using a macro in an Access app</span></span>

<span data-ttu-id="94228-104">Узнайте, как для фильтрации представления в приложение Access с помощью действия макроса RequeryRecords и макрос данных.</span><span class="sxs-lookup"><span data-stu-id="94228-104">Learn how to filter a view in an Access app by using the RequeryRecords macro action and a data macro.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="94228-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="94228-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="94228-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="94228-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 

<span data-ttu-id="94228-107">Представление списка по умолчанию в приложение Access позволяет фильтровать проблемы на значения, содержащиеся в полях.</span><span class="sxs-lookup"><span data-stu-id="94228-107">The default list view in an Access app enables you to filter the issues on values that are contained in the fields.</span></span> <span data-ttu-id="94228-108">Возможны случаи, где требуется отфильтровать представлении, основываясь на набор условий, а не с сопоставления значения.</span><span class="sxs-lookup"><span data-stu-id="94228-108">There may be instances where you'd like to filter a view based on a set of conditions instead of by matching a value.</span></span> <span data-ttu-id="94228-109">Для этого необходимо создать макрос.</span><span class="sxs-lookup"><span data-stu-id="94228-109">To do that you must create a macro.</span></span> <span data-ttu-id="94228-110">В этой статье показано, как создать макрос, позволяющие фильтровать представления для отображения задач, для выполнения или из-за в следующие 7 дней.</span><span class="sxs-lookup"><span data-stu-id="94228-110">This article shows you how to create a macro that filter a view to display tasks that are past due or due in the next 7 days.</span></span>
  
## <a name="prerequisites-for-building-an-app-with-access"></a><span data-ttu-id="94228-111">Предварительные требования для создания приложения с помощью Access</span><span class="sxs-lookup"><span data-stu-id="94228-111">Prerequisites for building an app with Access</span></span>
<span data-ttu-id="94228-112"><a name="Access2013FilterViewByUsingMacro_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="94228-112"></span></span>

<span data-ttu-id="94228-113">Для выполнения действия, описанные в этом примере, вам потребуются:</span><span class="sxs-lookup"><span data-stu-id="94228-113">To follow the steps in this example, you need:</span></span>
  
- <span data-ttu-id="94228-114">Access 2013</span><span class="sxs-lookup"><span data-stu-id="94228-114">Access 2013</span></span>
- <span data-ttu-id="94228-115">Среда разработки SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="94228-115">A SharePoint 2013 development environment</span></span>
    
> [!NOTE]
> <span data-ttu-id="94228-116">Дополнительные сведения о настройке среды разработки SharePoint видеть [настроить среду разработки, общие для SharePoint 2013](http://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="94228-116">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint 2013](http://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span></span> <span data-ttu-id="94228-117">> Для получения дополнительных сведений о получении Access 2013 и SharePoint 2013 видеть [файлы для загрузки](http://msdn.microsoft.com/ru-ru/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="94228-117">>  For more information about obtaining Access 2013 and SharePoint 2013, see [Downloads](http://msdn.microsoft.com/ru-ru/office/apps/fp123627).</span></span> 
  
## <a name="create-the-app"></a><span data-ttu-id="94228-118">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="94228-118">Create the app</span></span>
<span data-ttu-id="94228-119"><a name="Access2013FilterViewByUsingMacro_CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="94228-119"></span></span>

<span data-ttu-id="94228-120">Предположим, что вы хотите создать приложение Access, который отслеживает задачи для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="94228-120">Suppose you want to create an Access app that tracks tasks for your business.</span></span> <span data-ttu-id="94228-121">Прежде чем приступить к созданию таблицы и представления, необходимо найти шаблона схемы.</span><span class="sxs-lookup"><span data-stu-id="94228-121">Before you start creating the tables and view, you should search for a schema template.</span></span>
  
### <a name="to-create-the-task-tracking-app"></a><span data-ttu-id="94228-122">Для создания приложения отслеживания задач</span><span class="sxs-lookup"><span data-stu-id="94228-122">To create the task tracking app</span></span>

1. <span data-ttu-id="94228-123">Откройте доступ и выберите пункт **настраиваемых веб-приложения**.</span><span class="sxs-lookup"><span data-stu-id="94228-123">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="94228-124">Введите имя и расположение веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="94228-124">Enter a name and the web location for your app.</span></span> <span data-ttu-id="94228-125">Можно выбрать расположение из **списка** и выберите команду **Создать**.</span><span class="sxs-lookup"><span data-stu-id="94228-125">You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="94228-126">В поле « **Поиск** » введите **задачи** и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="94228-126">Type **tasks** into the **Search** box and then press ENTER.</span></span> 
    
    <span data-ttu-id="94228-127">Шаблоны, которые могут оказаться полезными для отслеживания задач отображаются на рисунке 1.</span><span class="sxs-lookup"><span data-stu-id="94228-127">A list of templates that might be useful for tracking tasks is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="94228-128">**На рисунке 1. Шаблоны, соответствующие поиск задач**</span><span class="sxs-lookup"><span data-stu-id="94228-128">**Figure 1. Templates that match the search for tasks**</span></span>

   <span data-ttu-id="94228-129">![Шаблоны, соответствующие поиску проблем] (media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Шаблоны, соответствующие поиску проблем")</span><span class="sxs-lookup"><span data-stu-id="94228-129">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="94228-130">Выберите **задачи**.</span><span class="sxs-lookup"><span data-stu-id="94228-130">Choose **Tasks**.</span></span>
    
<span data-ttu-id="94228-131">Access создает набор таблиц и представлений.</span><span class="sxs-lookup"><span data-stu-id="94228-131">Access creates a set of tables and views.</span></span>
  
<span data-ttu-id="94228-132">Введите некоторые примеры задач и сотрудников в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="94228-132">Enter several sample tasks and employees in your app.</span></span> <span data-ttu-id="94228-133">Для этого выберите **Запуск приложения** , чтобы открыть его в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="94228-133">To do this, choose **Launch App** to open the app in your web browser.</span></span> <span data-ttu-id="94228-134">Введите значение в поле **Дата завершения** для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="94228-134">Enter a value in the **Due Date** field for each task.</span></span> <span data-ttu-id="94228-135">Вернуться к доступа, после завершения.</span><span class="sxs-lookup"><span data-stu-id="94228-135">Return to Access when you're done.</span></span> 
  
## <a name="plan-the-customizations"></a><span data-ttu-id="94228-136">Планирование настроек</span><span class="sxs-lookup"><span data-stu-id="94228-136">Plan the customizations</span></span>
<span data-ttu-id="94228-137"><a name="Access2013FilterViewByUsingMacro_PlanCustomizations"> </a></span><span class="sxs-lookup"><span data-stu-id="94228-137"></span></span>

<span data-ttu-id="94228-138">Теперь у вас есть приложения, которое содержит несколько задач.</span><span class="sxs-lookup"><span data-stu-id="94228-138">You now have an app that contains several tasks.</span></span> <span data-ttu-id="94228-139">Представление по умолчанию позволяет найти все задачи, с помощью элементов, которые хранятся в поля, отображаемые в представлении.</span><span class="sxs-lookup"><span data-stu-id="94228-139">The default view enables you to search for any tasks using items that are stored in the fields displayed in the view.</span></span> <span data-ttu-id="94228-140">Например, можно выполнить поиск важных проблем и проблем в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="94228-140">For example, you can search for high-priority issues or issues in progress.</span></span> <span data-ttu-id="94228-141">Предположим, что требуется определить приоритеты работу, отображая активные вопросы, которые срок выполнения в течение нескольких недель.</span><span class="sxs-lookup"><span data-stu-id="94228-141">Suppose you want to prioritize your work by displaying active issues that are due in the coming week.</span></span> <span data-ttu-id="94228-142">Для этого необходимо создать макрос пользовательского интерфейса (UI).</span><span class="sxs-lookup"><span data-stu-id="94228-142">To do this, you should create a user interface (UI) macro.</span></span>
  
<span data-ttu-id="94228-143">Команда макрос пользовательского интерфейса, которые можно использовать для фильтрации представлений — [Действия макроса RequeryRecords (приложение настраиваемых web Access)](requeryrecords-macro-action-access-custom-web-app.md).</span><span class="sxs-lookup"><span data-stu-id="94228-143">The UI macro command that you can use to filter the view is the [RequeryRecords Macro Action (Access custom web app)](requeryrecords-macro-action-access-custom-web-app.md).</span></span> <span data-ttu-id="94228-144">Действия макроса **RequeryRecords** фильтр представлении, основываясь на *где* аргумент, который предоставляется в виде предложения SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="94228-144">The **RequeryRecords** macro action filters the view based on the  *Where*  argument, which is provided in the form of a SQL WHERE clause.</span></span> <span data-ttu-id="94228-145">Для фильтрации представлений, необходимо указать несколько факты в определенный формат для фильтрации представления.</span><span class="sxs-lookup"><span data-stu-id="94228-145">To filter the view, you must supply several facts in a specific format to filter the view.</span></span> 
  
<span data-ttu-id="94228-146">Соответствующие факты являются:</span><span class="sxs-lookup"><span data-stu-id="94228-146">The relevant facts are:</span></span>
  
- <span data-ttu-id="94228-147">Одно или несколько полей для сравнения</span><span class="sxs-lookup"><span data-stu-id="94228-147">The field or fields to compare</span></span>
    
- <span data-ttu-id="94228-148">Обращение к текущей дате</span><span class="sxs-lookup"><span data-stu-id="94228-148">How to refer to today's date</span></span>
    
- <span data-ttu-id="94228-149">Как ссылаться на конкретный день относительно текущей даты</span><span class="sxs-lookup"><span data-stu-id="94228-149">How to refer to a particular day relative to today's date</span></span>
    
- <span data-ttu-id="94228-150">Как определить, который на задачи находятся в процессе выполнения</span><span class="sxs-lookup"><span data-stu-id="94228-150">How to determine which on tasks are in progress</span></span>
    
<span data-ttu-id="94228-151">Поле **Дата выполнения** предоставляет сведения о задача — срок выполнения.</span><span class="sxs-lookup"><span data-stu-id="94228-151">The **Due Date** field provides information about when a task is due.</span></span> <span data-ttu-id="94228-152">Поле **состояние** предоставляет сведения о состоянии о каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="94228-152">The **Status** field provides status information about each task.</span></span> <span data-ttu-id="94228-153">Для ссылки на поля в макросе, используйте формат **[*имя_таблицы*]. [ *FieldName*]**.</span><span class="sxs-lookup"><span data-stu-id="94228-153">To refer to a field in a macro, use the format **[*TableName*].[*FieldName*]**.</span></span> <span data-ttu-id="94228-154">Использование **[задачи]. [ Дата завершения]** для ссылки на поля **Дату завершения** и **[задачи]. [ Состояние]** для ссылки на поле **состояние** .</span><span class="sxs-lookup"><span data-stu-id="94228-154">Use **[Tasks].[Due Date]** to refer to the **Due Date** field and **[Tasks].[Status]** to refer to the **Status** field.</span></span> 
  
<span data-ttu-id="94228-155">Функция [Сегодня функции (приложение настраиваемых web Access)](today-function-access-custom-web-app.md) возвращает текущую дату.</span><span class="sxs-lookup"><span data-stu-id="94228-155">The [Today Function (Access custom web app)](today-function-access-custom-web-app.md) function returns today's date.</span></span> <span data-ttu-id="94228-156">Функция [Функции DateAdd (приложение настраиваемых web Access)](dateadd-function-access-custom-web-app.md) можно использовать для вычисления даты, определенного количества дней после определенной даты.</span><span class="sxs-lookup"><span data-stu-id="94228-156">The [DateAdd Function (Access custom web app)](dateadd-function-access-custom-web-app.md) function can be used to calculate a date that's a certain number of days after a specified date.</span></span> 
  
<span data-ttu-id="94228-157">Поле **состояния** содержит несколько возможных значений.</span><span class="sxs-lookup"><span data-stu-id="94228-157">The **Status** field contains several possible values.</span></span> <span data-ttu-id="94228-158">Значение **завершено** указывает, что задача больше не активен.</span><span class="sxs-lookup"><span data-stu-id="94228-158">A value of **Completed** indicates that the task is no longer active.</span></span> 
  
<span data-ttu-id="94228-159">Эти данные могут быть объединены в следующие предложения SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="94228-159">These facts can be combined into the following SQL WHERE clause.</span></span>
  
```sql
[Tasks].[Due Date]<DateAdd(Day,7,Today()) AND [Tasks].[Status]<>"Completed"
```

<span data-ttu-id="94228-160">В этом предложения SQL WHERE используется в макросе для фильтрации представления для отображения активные вопросы, срок выполнения в течение 7 дней, или просроченных.</span><span class="sxs-lookup"><span data-stu-id="94228-160">This SQL WHERE clause is used in the macro to filter the view to display active issues that are due in the next 7 days or are past due.</span></span>
  
<span data-ttu-id="94228-161">Чтобы запустить макрос пользовательского интерфейса, его необходимо подключенного к элемента или событий, возникающих в представлении в.</span><span class="sxs-lookup"><span data-stu-id="94228-161">To run the UI macro, it must be attached to an item or an event that occurs in the view.</span></span> <span data-ttu-id="94228-162">Добавление пользовательской команды в представление удобно в **Панель действий** .</span><span class="sxs-lookup"><span data-stu-id="94228-162">The **Action Bar** is a convenient place to add a custom command to the view.</span></span> <span data-ttu-id="94228-163">**Панель действий** — настраиваемая панель инструментов, который отображается в верхней части каждого представления.</span><span class="sxs-lookup"><span data-stu-id="94228-163">The **Action Bar** is a customizable toolbar that appears at the top of each view.</span></span> <span data-ttu-id="94228-164">По умолчанию **Панель действий** содержит кнопки для добавления, изменения, сохранение, удаление и отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="94228-164">By default, the **Action Bar** contains buttons to add, edit, save, delete, and cancel edits.</span></span> <span data-ttu-id="94228-165">Можно добавить кнопки для выполнения настраиваемых действий, например фильтрации представления.</span><span class="sxs-lookup"><span data-stu-id="94228-165">You can add buttons that perform custom actions, such as filtering the view.</span></span> 
  
<span data-ttu-id="94228-166">Если представление содержит записи, которые соответствуют заданным критериям, **RequeryRecords** фильтр представления.</span><span class="sxs-lookup"><span data-stu-id="94228-166">If the view contains records that meet the specified criteria, then **RequeryRecords** filters the view.</span></span> <span data-ttu-id="94228-167">Тем не менее если в представлении нет записей, которые соответствуют критериям, чем новые, отображается пустую запись.</span><span class="sxs-lookup"><span data-stu-id="94228-167">However, if the view doesn't contain any records that meet the criteria, than a new, blank record is displayed.</span></span> <span data-ttu-id="94228-168">Если вы не хотите пустую запись будет отображаться, если отсутствуют задачи, срок выполнения следующей недели, необходимо найти метод для проверки задачи, прежде чем вызывать действия макроса **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="94228-168">If you don't want a blank record to be displayed if no tasks are due in the next week, then you must find a method to check the tasks before you call the **RequeryRecords** macro action.</span></span> <span data-ttu-id="94228-169">Для этого создайте макрос данных на наличие записей, которые соответствуют критериям.</span><span class="sxs-lookup"><span data-stu-id="94228-169">To do this, create a data macro to check for records that meet the criteria.</span></span> 
  
<span data-ttu-id="94228-170">Макрос пользовательского интерфейса, можно вызвать макрос данных попытается найти задание, которое должно быть выполнено следующей недели.</span><span class="sxs-lookup"><span data-stu-id="94228-170">The UI macro will call the data macro, which will try to find a task that's due in the next week.</span></span> <span data-ttu-id="94228-171">Если макрос данных находит задачи настройки приложения.</span><span class="sxs-lookup"><span data-stu-id="94228-171">If the data macro finds the task then customize the app.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="94228-172">Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="94228-172">Customize the app</span></span>
<span data-ttu-id="94228-173"><a name="Access2013FilterViewByUsingMacro_CustomizeApp"> </a></span><span class="sxs-lookup"><span data-stu-id="94228-173"></span></span>

<span data-ttu-id="94228-174">Теперь, когда вы определили настроек, их реализации.</span><span class="sxs-lookup"><span data-stu-id="94228-174">Now that you've determined the customizations, implement them.</span></span> <span data-ttu-id="94228-175">Сначала необходимо создать макрос данных.</span><span class="sxs-lookup"><span data-stu-id="94228-175">The data macro should be created first.</span></span> <span data-ttu-id="94228-176">Некоторые макросы данных присоединяются напрямую с таблицами.</span><span class="sxs-lookup"><span data-stu-id="94228-176">Some data macros are attached directly to tables.</span></span> <span data-ttu-id="94228-177">Тем не менее этот макрос данных является отдельной макрос.</span><span class="sxs-lookup"><span data-stu-id="94228-177">However, this data macro is a stand-alone data macro.</span></span>
  
### <a name="to-create-the-data-macro"></a><span data-ttu-id="94228-178">Чтобы создать макрос данных</span><span class="sxs-lookup"><span data-stu-id="94228-178">To create the data macro</span></span>

1. <span data-ttu-id="94228-179">Откройте приложение в Access.</span><span class="sxs-lookup"><span data-stu-id="94228-179">Open the app in Access.</span></span>
    
2. <span data-ttu-id="94228-180">В группе **Создание** нажмите кнопку **Дополнительно**и выберите **Макрос данных**.</span><span class="sxs-lookup"><span data-stu-id="94228-180">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
    <span data-ttu-id="94228-181">Макрос данных открывается в режиме конструктора макросов.</span><span class="sxs-lookup"><span data-stu-id="94228-181">A blank data macro is opened in macro Design View.</span></span>
    
3. <span data-ttu-id="94228-182">В списке **Добавить новое действие** выберите команду **макрокомандой НайтиЗапись, после**.</span><span class="sxs-lookup"><span data-stu-id="94228-182">From the **Add New Action** list box, choose **LookupRecord**.</span></span>
    
4. <span data-ttu-id="94228-183">В поле **Поиск копирование записи в** списке выберите **задачи**.</span><span class="sxs-lookup"><span data-stu-id="94228-183">In the **Look Up A Record In** list box, choose **Tasks**.</span></span>
    
5. <span data-ttu-id="94228-184">В поле **Условие отбора** введите **[задачи]. [ Дата завершения]\<DateAdd(Day,7,Today()) и [задачи]. [Состояние] \< \>«Завершена»**.</span><span class="sxs-lookup"><span data-stu-id="94228-184">In the **Where Condition** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
6. <span data-ttu-id="94228-185">Выберите **SetReturnVar** в списке **Добавить действие** .</span><span class="sxs-lookup"><span data-stu-id="94228-185">Choose **SetReturnVar** from the **Add New Action** list box.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="94228-186">Вы увидите два поля списка **Добавить действие** , один внутри блока **макрокомандой НайтиЗапись, после** и другой вне блока **макрокомандой НайтиЗапись, после** .</span><span class="sxs-lookup"><span data-stu-id="94228-186">You'll see two **Add New Action** list boxes, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="94228-187">Следует выбрать список **Добавить действие** в блоке **макрокомандой НайтиЗапись, после** , как показано на рисунке 1.</span><span class="sxs-lookup"><span data-stu-id="94228-187">You should choose the **Add New Action** list box within the **LookupRecord** block, as shown in Figure 1.</span></span> 
  
   <span data-ttu-id="94228-188">**На рисунке 1. Добавьте поле со списком новое действие**</span><span class="sxs-lookup"><span data-stu-id="94228-188">**Figure 1. Add New Action list box**</span></span>

   <span data-ttu-id="94228-189">![Добавление нового действия раскрывающийся список] (media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Добавление нового действия раскрывающийся список")</span><span class="sxs-lookup"><span data-stu-id="94228-189">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="94228-190">В поле **имя** введите **TaskFound**.</span><span class="sxs-lookup"><span data-stu-id="94228-190">In the **Name** box, enter **TaskFound**.</span></span> 
    
8. <span data-ttu-id="94228-191">В поле **выражение** введите **«Да»**.</span><span class="sxs-lookup"><span data-stu-id="94228-191">In the **Expression** box, enter **"Yes"**.</span></span> 
    
9. <span data-ttu-id="94228-192">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="94228-192">Choose **Save**.</span></span> <span data-ttu-id="94228-193">В поле **Имя** введите **TasksDueSoon** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="94228-193">Enter **TasksDueSoon** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="94228-194">Макрос должен выглядеть макрос, показано на рисунке 2.</span><span class="sxs-lookup"><span data-stu-id="94228-194">The macro should resemble the macro shown in Figure 2.</span></span>
    
   <span data-ttu-id="94228-195">**На рисунке 2. Макрос данных tasksduesoon**</span><span class="sxs-lookup"><span data-stu-id="94228-195">**Figure 2. TasksDueSoon data macro**</span></span>

   <span data-ttu-id="94228-196">![Макрос данных tasksduesoon] (media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "Макрос данных tasksduesoon")</span><span class="sxs-lookup"><span data-stu-id="94228-196">![TasksDueSoon data macro](media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "TasksDueSoon data macro")</span></span>
  
10. <span data-ttu-id="94228-197">Закрытие конструктора макроса.</span><span class="sxs-lookup"><span data-stu-id="94228-197">Close macro Design View.</span></span>
    
<span data-ttu-id="94228-198">Теперь мы готовы для добавления настраиваемой кнопке панели действий.</span><span class="sxs-lookup"><span data-stu-id="94228-198">Now, we're ready to add a custom button to the Action Bar.</span></span>
  
### <a name="to-add-a-custom-button-to-the-action-bar"></a><span data-ttu-id="94228-199">Добавление настраиваемой кнопки на панель действий</span><span class="sxs-lookup"><span data-stu-id="94228-199">To add a custom button to the Action Bar</span></span>

1. <span data-ttu-id="94228-200">Выберите таблицу **задачи** .</span><span class="sxs-lookup"><span data-stu-id="94228-200">Choose the **Tasks** table.</span></span> <span data-ttu-id="94228-201">Это выбирает формы списка задач.</span><span class="sxs-lookup"><span data-stu-id="94228-201">This chooses the Tasks List form.</span></span> 
    
2. <span data-ttu-id="94228-202">Выбор представления в выберите **список**, выберите значок **Параметры и действия** и выберите команду **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="94228-202">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
    <span data-ttu-id="94228-203">Представление открывается в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="94228-203">The view is opened in Design View.</span></span>
    
3. <span data-ttu-id="94228-204">Теперь мы готовы для добавления настраиваемой кнопке панели действий.</span><span class="sxs-lookup"><span data-stu-id="94228-204">Now, we're ready to add a custom button to the Action Bar.</span></span> <span data-ttu-id="94228-205">Для этого нажмите кнопку **Добавить настраиваемое действие** , как показано на рисунке 3.</span><span class="sxs-lookup"><span data-stu-id="94228-205">To do this, choose **Add custom action** as shown in Figure 3.</span></span> 
    
   <span data-ttu-id="94228-206">**На рисунке 3. Кнопка добавления настраиваемого действия**</span><span class="sxs-lookup"><span data-stu-id="94228-206">**Figure 3. Add custom action button**</span></span>

   <span data-ttu-id="94228-207">![Кнопку Добавить настраиваемое действие] (media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Кнопку Добавить настраиваемое действие")</span><span class="sxs-lookup"><span data-stu-id="94228-207">![Add custom action button](media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Add custom action button")</span></span>
  
    <span data-ttu-id="94228-208">Новое действие отображается как кнопка со значком звезда, как показано на рисунке 4.</span><span class="sxs-lookup"><span data-stu-id="94228-208">The new action is displayed as a button with a star icon as shown in Figure 4.</span></span>
    
   <span data-ttu-id="94228-209">**На рисунке 4. Кнопка панели новых действий**</span><span class="sxs-lookup"><span data-stu-id="94228-209">**Figure 4. New Action Bar button**</span></span>

   <span data-ttu-id="94228-210">![Кнопка Создать панель действий] (media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "Кнопка Создать панель действий")</span><span class="sxs-lookup"><span data-stu-id="94228-210">![New Action Bar button](media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "New Action Bar button")</span></span>
  
4. <span data-ttu-id="94228-211">Нажмите кнопку панели настраиваемые действия и выберите значок **данных** .</span><span class="sxs-lookup"><span data-stu-id="94228-211">Choose the custom Action Bar Button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="94228-212">Откроется диалоговое окно **данных** .</span><span class="sxs-lookup"><span data-stu-id="94228-212">The **Data** dialog box appears.</span></span> 
    
5. <span data-ttu-id="94228-213">В поле **Имя элемента управления** введите **FilterTasks**.</span><span class="sxs-lookup"><span data-stu-id="94228-213">In the **Control Name** box, enter **FilterTasks**.</span></span> 
    
6. <span data-ttu-id="94228-214">В поле **всплывающая подсказка** введите **отображаемое обзор задач после выполнения или из-за следующей недели**.</span><span class="sxs-lookup"><span data-stu-id="94228-214">In the **Tooltip** box, enter **Display tasks past due or due in the next week**.</span></span> 
    
<span data-ttu-id="94228-215">Теперь мы готовы создать макрос пользовательского интерфейса, чтобы отфильтровать представление.</span><span class="sxs-lookup"><span data-stu-id="94228-215">Now, we're ready to create the UI macro that will filter the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-filter-the-view"></a><span data-ttu-id="94228-216">Чтобы создать макрос пользовательского интерфейса для фильтрации представлений</span><span class="sxs-lookup"><span data-stu-id="94228-216">To create the UI macro to filter the view</span></span>

1. <span data-ttu-id="94228-217">В диалоговом окне **данных** выберите **На выберите** , как показано на рисунке 5.</span><span class="sxs-lookup"><span data-stu-id="94228-217">In the **Data** dialog box, choose **On Click** as shown in Figure 5.</span></span> 
    
   <span data-ttu-id="94228-218">**На рисунке 5. Диалоговое окно "данные"**</span><span class="sxs-lookup"><span data-stu-id="94228-218">**Figure 5. Data dialog box**</span></span>

   <span data-ttu-id="94228-219">![Диалоговое окно "данные"] (media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Диалоговое окно \"данные\"")</span><span class="sxs-lookup"><span data-stu-id="94228-219">![Data dialog box](media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Data dialog box")</span></span>
  
    <span data-ttu-id="94228-220">Пустой макрос пользовательского интерфейса открывается в режиме конструктора макросов.</span><span class="sxs-lookup"><span data-stu-id="94228-220">A blank UI macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="94228-221">В списке **Добавить новое действие** выберите команду **ЗапускМакросаДанных**.</span><span class="sxs-lookup"><span data-stu-id="94228-221">From the **Add New Action** list box, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="94228-222">В поле Имя введите **TasksDueSoon**.</span><span class="sxs-lookup"><span data-stu-id="94228-222">In the Macro Name box, enter **TasksDueSoon**.</span></span> 
    
    <span data-ttu-id="94228-223">В поле **SetLocalVar** введите **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="94228-223">In the **SetLocalVar** box, enter **FilterRecords**.</span></span> 
    
    <span data-ttu-id="94228-224">**ЗапускМакросаДанных** вызывает **макрос данных tasksduesoon, которые мы создали раньше** и сохраняет ее результатов в переменной с именем **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="94228-224">The **RunDataMacro** action calls the **TasksDueSoon** data macro we created earlier and stores its result in a variable named **FilterRecords**.</span></span> 
    
4. <span data-ttu-id="94228-225">В списке **Добавить новое действие** выберите, **если**.</span><span class="sxs-lookup"><span data-stu-id="94228-225">From the **Add New Action** list box, choose **If**.</span></span> 
    
5. <span data-ttu-id="94228-226">Введите в поле **Если** **[FilterRecords] = «Yes»**.</span><span class="sxs-lookup"><span data-stu-id="94228-226">In the **If** box, enter **[FilterRecords]="Yes"**.</span></span> 
    
6. <span data-ttu-id="94228-227">В списке **Добавить новое действие** выберите команду **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="94228-227">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="94228-228">Вы увидите два поля списка **Добавить действие** , один в блок **If** , а другой за пределами блок **If** .</span><span class="sxs-lookup"><span data-stu-id="94228-228">You'll see two **Add New Action** list boxes, one within the **If** block, and another outside the **If** block.</span></span> <span data-ttu-id="94228-229">Поле со списком **Добавлять новые действия** в пределах блок **If** должен выбрать, как показано на рисунке 6.</span><span class="sxs-lookup"><span data-stu-id="94228-229">You should choose the **Add New Action** list box within the **If** block, as shown in Figure 6.</span></span> 
  
   <span data-ttu-id="94228-230">**На рисунке 6. Добавьте поле со списком новое действие**</span><span class="sxs-lookup"><span data-stu-id="94228-230">**Figure 6. Add New Action list box**</span></span>

   <span data-ttu-id="94228-231">![Добавление нового действия раскрывающийся список] (media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Добавление нового действия раскрывающийся список")</span><span class="sxs-lookup"><span data-stu-id="94228-231">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="94228-232">В поле **где** введите \<.</span><span class="sxs-lookup"><span data-stu-id="94228-232">In the **Where** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
8. <span data-ttu-id="94228-233">В поле **Order By** введите **[Дата завершения]**.</span><span class="sxs-lookup"><span data-stu-id="94228-233">In the **Order By** box, enter **[Due Date]**.</span></span> 
    
9. <span data-ttu-id="94228-234">Выберите ссылку **Добавить человеку** , который отображается в правой части в поле **Добавить действие** , как показано на рисунке 7.</span><span class="sxs-lookup"><span data-stu-id="94228-234">Choose the **Add Else** link that appears to the right side of the **Add New Action** box as shown in Figure 7.</span></span> 
    
   <span data-ttu-id="94228-235">**На рисунке 7. Добавление ссылки Else**</span><span class="sxs-lookup"><span data-stu-id="94228-235">**Figure 7. Add Else link**</span></span>

   <span data-ttu-id="94228-236">![Добавьте еще ссылок] (media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Добавьте еще ссылок")</span><span class="sxs-lookup"><span data-stu-id="94228-236">![Add Else link](media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Add Else link")</span></span>
  
    <span data-ttu-id="94228-237">Предложение Else добавляется в том случае, если блокировки.</span><span class="sxs-lookup"><span data-stu-id="94228-237">An Else clause is added to the If block.</span></span>
    
10. <span data-ttu-id="94228-238">В списке **Добавить новое действие** выберите команду **MessageBox**.</span><span class="sxs-lookup"><span data-stu-id="94228-238">From the **Add New Action** list box, choose **MessageBox**.</span></span> 
    
11. <span data-ttu-id="94228-239">В поле **сообщение** введите **отсутствуют задачи, просроченные или завершающиеся в следующие 7 дней!**.</span><span class="sxs-lookup"><span data-stu-id="94228-239">In the **Message** box, enter **No tasks are overdue or due in the next 7 days!**.</span></span> 
    
12. <span data-ttu-id="94228-240">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="94228-240">Choose **Save**.</span></span>
    
    <span data-ttu-id="94228-241">Макрос должен выглядеть макрос, показано на рисунке 8.</span><span class="sxs-lookup"><span data-stu-id="94228-241">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="94228-242">**На рисунке 8. Макрос пользовательского интерфейса для фильтрации представлений**</span><span class="sxs-lookup"><span data-stu-id="94228-242">**Figure 8. UI macro to filter the view**</span></span>

    <span data-ttu-id="94228-243">![Макрос пользовательского интерфейса для фильтрации представлений] (media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "Макрос пользовательского интерфейса для фильтрации представлений")</span><span class="sxs-lookup"><span data-stu-id="94228-243">![UI macro to filter the view](media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "UI macro to filter the view")</span></span>
  
13. <span data-ttu-id="94228-244">Закрытие конструктора макроса.</span><span class="sxs-lookup"><span data-stu-id="94228-244">Close macro Design View.</span></span>
    
<span data-ttu-id="94228-245">На этом этапе мы создали макрос пользовательского интерфейса, которая фильтрует представления списка задач для отображения срочных задач.</span><span class="sxs-lookup"><span data-stu-id="94228-245">At this point, we've created the UI macro that filters the Tasks List view to display the urgent tasks.</span></span> <span data-ttu-id="94228-246">Не будет вежливы из представления в отфильтрованные состоянии не предоставление метода для удаления фильтра.</span><span class="sxs-lookup"><span data-stu-id="94228-246">It wouldn't be polite to leave the view in a filtered state without providing a method to remove the filter.</span></span> <span data-ttu-id="94228-247">Для этого добавьте другой кнопки панель действий и макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="94228-247">To do this, add another Action Bar button and UI Macro.</span></span>
  
### <a name="to-add-an-action-bar-button-to-remove-the-filter"></a><span data-ttu-id="94228-248">Чтобы добавить кнопку панели действия для удаления фильтра</span><span class="sxs-lookup"><span data-stu-id="94228-248">To add an Action Bar Button to remove the filter</span></span>

1. <span data-ttu-id="94228-249">Нажмите кнопку **Добавить настраиваемое действие**.</span><span class="sxs-lookup"><span data-stu-id="94228-249">Choose **Add custom action**.</span></span>
    
    <span data-ttu-id="94228-250">Новое действие отображается как кнопка со значком звезда</span><span class="sxs-lookup"><span data-stu-id="94228-250">The new action is displayed as a button with a star icon</span></span>
    
2. <span data-ttu-id="94228-251">Нажмите кнопку настраиваемые панель действий и выберите значок **данных** .</span><span class="sxs-lookup"><span data-stu-id="94228-251">Choose the custom Action Bar button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="94228-252">Откроется диалоговое окно **данных** .</span><span class="sxs-lookup"><span data-stu-id="94228-252">The **Data** dialog box appears.</span></span> 
    
3. <span data-ttu-id="94228-253">В поле **Имя элемента управления** введите **RemoveFilter**.</span><span class="sxs-lookup"><span data-stu-id="94228-253">In the **Control Name** box, enter **RemoveFilter**.</span></span> 
    
4. <span data-ttu-id="94228-254">В поле **всплывающая подсказка** введите **Удалить все фильтр в представление**.</span><span class="sxs-lookup"><span data-stu-id="94228-254">In the **Tooltip** box, enter **Remove all filter applied to the view**.</span></span> 
    
<span data-ttu-id="94228-255">Теперь мы готовы создать макрос пользовательского интерфейса, который будет удалить форму фильтр представления.</span><span class="sxs-lookup"><span data-stu-id="94228-255">Now, we're ready to create the UI macro that will remove the filter form the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-remove-the-filter-from-the-view"></a><span data-ttu-id="94228-256">Чтобы создать макрос пользовательского интерфейса, чтобы удалить фильтр из представления</span><span class="sxs-lookup"><span data-stu-id="94228-256">To create the UI macro to remove the filter from the view</span></span>

1. <span data-ttu-id="94228-257">В диалоговом окне **данных** выберите **Пункт**.</span><span class="sxs-lookup"><span data-stu-id="94228-257">In the **Data** dialog box, choose **On Click**.</span></span>
    
    <span data-ttu-id="94228-258">Пустой макрос пользовательского интерфейса открывается в режиме конструктора макросов.</span><span class="sxs-lookup"><span data-stu-id="94228-258">A blank UI macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="94228-259">В списке **Добавить новое действие** выберите команду **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="94228-259">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    <span data-ttu-id="94228-260">Настоящее время мы будет оставьте **Where** и **Order By** поля пустыми.</span><span class="sxs-lookup"><span data-stu-id="94228-260">This time, we'll leave the **Where** and **Order By** boxes empty.</span></span> <span data-ttu-id="94228-261">Действие **RequeryRecords** вызывается без параметров, а затем удаляются все фильтры из представления.</span><span class="sxs-lookup"><span data-stu-id="94228-261">Then the **RequeryRecords** action is called without any parameters, all filters are removed from the view.</span></span> 
    
3. <span data-ttu-id="94228-262">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="94228-262">Choose **Save**.</span></span>
    
4. <span data-ttu-id="94228-263">Закрытие конструктора макроса.</span><span class="sxs-lookup"><span data-stu-id="94228-263">Close macro Design View.</span></span>
    
5. <span data-ttu-id="94228-264">Закройте представление списка задач.</span><span class="sxs-lookup"><span data-stu-id="94228-264">Close the Tasks List view.</span></span> <span data-ttu-id="94228-265">Когда вам будет предложено сохранить изменения, нажмите кнопку **Да** .</span><span class="sxs-lookup"><span data-stu-id="94228-265">Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="94228-266">Теперь мы готовы к тексту настройки.</span><span class="sxs-lookup"><span data-stu-id="94228-266">Now, we're ready to text the customization.</span></span> <span data-ttu-id="94228-267">Нажмите кнопку **Запуск приложения** откройте приложение в веб-браузере и нажмите кнопку настраиваемые FilterTasks панель действий.</span><span class="sxs-lookup"><span data-stu-id="94228-267">Choose **Launch App** to open the app in your web browser and then choose the custom FilterTasks Action Bar button.</span></span> <span data-ttu-id="94228-268">Задачи после завершения или завершающиеся в следующие 7 дней, отображаются.</span><span class="sxs-lookup"><span data-stu-id="94228-268">Any tasks past due or due in the next 7 days are displayed.</span></span> <span data-ttu-id="94228-269">Если приложение не содержит срочных задач отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="94228-269">A message is displayed if the app contains no urgent tasks.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="94228-270">Заключение</span><span class="sxs-lookup"><span data-stu-id="94228-270">Conclusion</span></span>

<span data-ttu-id="94228-271">Действия макроса **RequeryRecords** можно использовать в макросе пользовательского интерфейса для фильтрации представления на основе критериев, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="94228-271">You can use the **RequeryRecords** macro action in a UI macro to filter the view based on the criteria that you choose.</span></span> <span data-ttu-id="94228-272">В зависимости от желаемое поведение может потребоваться создать макрос данных, чтобы убедиться, что запись соответствует критерии, прежде чем использовать действия макроса **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="94228-272">Depending on the behavior that you want, you may want to create a data macro to verify that a record meets the criteria before you use the **RequeryRecords** macro action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94228-273">См. также</span><span class="sxs-lookup"><span data-stu-id="94228-273">See also</span></span>

- [<span data-ttu-id="94228-274">Новые возможности для разработчиков Access 2013</span><span class="sxs-lookup"><span data-stu-id="94228-274">What's new for Access 2013 developers</span></span>](http://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx)
    

