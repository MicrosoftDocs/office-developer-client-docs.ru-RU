---
title: Доступ к корпоративным настраиваемым полям Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online — это служба Office 365, компаний можно расширить для удовлетворения потребностей бизнеса. Одной области расширения — корпоративных настраиваемых полей (ECFs). ECFs, типизированное значение поля, которые можно добавить в проекты, ресурсы и задачи. В следующей таблице перечислены ECFs, связанные с проектами, ресурсы и задачи и обеспечивает пример значение для экземпляра, ECF:'
ms.openlocfilehash: 978fdfbf4ba75382ad85b9f92f8ac4df5c7f97c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401155"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="2572d-106">Доступ к корпоративным настраиваемым полям Project Online</span><span class="sxs-lookup"><span data-stu-id="2572d-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="2572d-107">Project Online — это служба Office 365, компаний можно расширить для удовлетворения потребностей бизнеса.</span><span class="sxs-lookup"><span data-stu-id="2572d-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="2572d-108">Одной области расширения — корпоративных настраиваемых полей (ECFs).</span><span class="sxs-lookup"><span data-stu-id="2572d-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="2572d-109">ECFs, типизированное значение поля, которые можно добавить в проекты, ресурсы и задачи.</span><span class="sxs-lookup"><span data-stu-id="2572d-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="2572d-110">В следующей таблице перечислены ECFs, связанные с проектами, ресурсы и задачи и обеспечивает пример значение для экземпляра, ECF:</span><span class="sxs-lookup"><span data-stu-id="2572d-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="2572d-111">Имя ECF</span><span class="sxs-lookup"><span data-stu-id="2572d-111">ECF Name</span></span>|<span data-ttu-id="2572d-112">Тип ECF</span><span class="sxs-lookup"><span data-stu-id="2572d-112">ECF Type</span></span>|<span data-ttu-id="2572d-113">Association</span><span class="sxs-lookup"><span data-stu-id="2572d-113">Association</span></span>|<span data-ttu-id="2572d-114">Пример значения</span><span class="sxs-lookup"><span data-stu-id="2572d-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2572d-115">Выравнивание</span><span class="sxs-lookup"><span data-stu-id="2572d-115">Justification</span></span>  <br/> |<span data-ttu-id="2572d-116">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="2572d-116">TEXT</span></span>  <br/> |<span data-ttu-id="2572d-117">Project</span><span class="sxs-lookup"><span data-stu-id="2572d-117">Project</span></span>  <br/> |<span data-ttu-id="2572d-118">Конечный пользователь записи основных статистических и данными о работоспособности, с результатами, которые включают в себя оценки работоспособности и конкретные действия плана достигло предельного лучше работоспособности.</span><span class="sxs-lookup"><span data-stu-id="2572d-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="2572d-119">Оценка риска</span><span class="sxs-lookup"><span data-stu-id="2572d-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="2572d-120">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="2572d-120">TEXT</span></span>  <br/> |<span data-ttu-id="2572d-121">Project</span><span class="sxs-lookup"><span data-stu-id="2572d-121">Project</span></span>  <br/> |<span data-ttu-id="2572d-122">Low</span><span class="sxs-lookup"><span data-stu-id="2572d-122">Low</span></span>  <br/> |
|<span data-ttu-id="2572d-123">РЕНТАБЕЛЬНОСТЬ ИНВЕСТИЦИЙ</span><span class="sxs-lookup"><span data-stu-id="2572d-123">ROI</span></span>  <br/> |<span data-ttu-id="2572d-124">НОМЕР</span><span class="sxs-lookup"><span data-stu-id="2572d-124">NUMBER</span></span>  <br/> |<span data-ttu-id="2572d-125">Project</span><span class="sxs-lookup"><span data-stu-id="2572d-125">Project</span></span>  <br/> |<span data-ttu-id="2572d-126">2.10</span><span class="sxs-lookup"><span data-stu-id="2572d-126">2.10</span></span>  <br/> |
|<span data-ttu-id="2572d-127">Общие расходы</span><span class="sxs-lookup"><span data-stu-id="2572d-127">Total Cost</span></span>  <br/> |<span data-ttu-id="2572d-128">СТОИМОСТЬ</span><span class="sxs-lookup"><span data-stu-id="2572d-128">COST</span></span>  <br/> |<span data-ttu-id="2572d-129">Project</span><span class="sxs-lookup"><span data-stu-id="2572d-129">Project</span></span>  <br/> |<span data-ttu-id="2572d-130">$1,031,514</span><span class="sxs-lookup"><span data-stu-id="2572d-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="2572d-131">Запуск команды</span><span class="sxs-lookup"><span data-stu-id="2572d-131">Launch Team</span></span>  <br/> |<span data-ttu-id="2572d-132">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="2572d-132">TEXT</span></span>  <br/> |<span data-ttu-id="2572d-133">Resources</span><span class="sxs-lookup"><span data-stu-id="2572d-133">Resources</span></span>  <br/> |<span data-ttu-id="2572d-134">Да</span><span class="sxs-lookup"><span data-stu-id="2572d-134">Yes</span></span>  <br/> |
|<span data-ttu-id="2572d-135">Положение роли</span><span class="sxs-lookup"><span data-stu-id="2572d-135">Position Role</span></span>  <br/> |<span data-ttu-id="2572d-136">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="2572d-136">TEXT</span></span>  <br/> |<span data-ttu-id="2572d-137">Resources</span><span class="sxs-lookup"><span data-stu-id="2572d-137">Resources</span></span>  <br/> |<span data-ttu-id="2572d-138">Инженер-испытатель</span><span class="sxs-lookup"><span data-stu-id="2572d-138">Tester</span></span>  <br/> |
|<span data-ttu-id="2572d-139">Состояние отметки</span><span class="sxs-lookup"><span data-stu-id="2572d-139">Flag Status</span></span>  <br/> |<span data-ttu-id="2572d-140">ФЛАГ</span><span class="sxs-lookup"><span data-stu-id="2572d-140">FLAG</span></span>  <br/> |<span data-ttu-id="2572d-141">Task</span><span class="sxs-lookup"><span data-stu-id="2572d-141">Task</span></span>  <br/> |<span data-ttu-id="2572d-142">Нет</span><span class="sxs-lookup"><span data-stu-id="2572d-142">No</span></span>  <br/> |
|<span data-ttu-id="2572d-143">Работоспособности</span><span class="sxs-lookup"><span data-stu-id="2572d-143">Health</span></span>  <br/> |<span data-ttu-id="2572d-144">ТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="2572d-144">TEXT</span></span>  <br/> |<span data-ttu-id="2572d-145">Task</span><span class="sxs-lookup"><span data-stu-id="2572d-145">Task</span></span>  <br/> |<span data-ttu-id="2572d-146">Не указан</span><span class="sxs-lookup"><span data-stu-id="2572d-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="2572d-147">ECFs определяются на экземпляр приложения Web Project (PWA), внешние из любого проекта, ресурсу или задаче.</span><span class="sxs-lookup"><span data-stu-id="2572d-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="2572d-148">Еще они могут стать связанный с проектом, ресурсов или задач.</span><span class="sxs-lookup"><span data-stu-id="2572d-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="2572d-149">В этой статье представлены вводные взгляд на настраиваемых полей, с помощью примера приложения и основное внимание уделяется извлечение значений ECF.</span><span class="sxs-lookup"><span data-stu-id="2572d-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="2572d-150">Вы можете загрузить полный пример в https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span><span class="sxs-lookup"><span data-stu-id="2572d-150">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="2572d-151">Кроме того Project Online поддерживает локальные настраиваемые поля как только для чтения объектов, относящихся к определенному проекту, ресурсу или задаче.</span><span class="sxs-lookup"><span data-stu-id="2572d-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="2572d-152">Дополнительные сведения о локальном настраиваемые поля, см https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="2572d-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="2572d-153">Фон материалы (en)</span><span class="sxs-lookup"><span data-stu-id="2572d-153">Background materials</span></span>

<span data-ttu-id="2572d-154">Предыдущая статья, [Разработка приложения Project Online с помощью клиентской объектной модели](developing-a-project-online-application-using-the-client-side-object-model.md), представлены основные сведения и начальную ориентацию для разработки приложений с помощью CSOM.</span><span class="sxs-lookup"><span data-stu-id="2572d-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="2572d-155">Обратитесь в этой статье для следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="2572d-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="2572d-156">Общие сведения о проекте, изолированной и облачная выпуски</span><span class="sxs-lookup"><span data-stu-id="2572d-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="2572d-157">Среда разработки (выпуски Visual Studio и библиотеки программного обеспечения)</span><span class="sxs-lookup"><span data-stu-id="2572d-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="2572d-158">Проекта установки Visual Studio для приложений .NET с помощью библиотеки CSOM</span><span class="sxs-lookup"><span data-stu-id="2572d-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="2572d-159">Подключение к службе Project Online</span><span class="sxs-lookup"><span data-stu-id="2572d-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="2572d-160">Начальные сведения (объявления на уровне класса)</span><span class="sxs-lookup"><span data-stu-id="2572d-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="2572d-161">Класс для этого приложения определяет два элемента данных: контекст проекта и pwaECF словаря.</span><span class="sxs-lookup"><span data-stu-id="2572d-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="2572d-162">Объект context проект является частью CSOM проекта и подключается приложение и экземпляр веб-клиента Project.</span><span class="sxs-lookup"><span data-stu-id="2572d-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="2572d-163">Все запросы к службе использовать контекст проекта.</span><span class="sxs-lookup"><span data-stu-id="2572d-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="2572d-164">Контекст должен конечную точку подключения для создания экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="2572d-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="2572d-165">Конечная точка подключения — это URL-адрес экземпляра веб-клиента Project.</span><span class="sxs-lookup"><span data-stu-id="2572d-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="2572d-166">Словарь pwaECF сохранение проекта, ECFs определенные на уровне веб-клиента Project.</span><span class="sxs-lookup"><span data-stu-id="2572d-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="2572d-167">Словарь использует ECF. Внутреннееимя как ключ и объект CustomField как значение.</span><span class="sxs-lookup"><span data-stu-id="2572d-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="2572d-168">Словарь появится в методе ListPWACustomFields и затем используется как ссылка в методе Main.</span><span class="sxs-lookup"><span data-stu-id="2572d-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="2572d-169">Метод Main</span><span class="sxs-lookup"><span data-stu-id="2572d-169">Main method</span></span>

<span data-ttu-id="2572d-170">Метод Main управляет потоком приложения.</span><span class="sxs-lookup"><span data-stu-id="2572d-170">The Main method manages the application flow.</span></span> <span data-ttu-id="2572d-171">Как с помощью других приложений, использующих Project Online CSOM Main инициализирует контекст проекта.</span><span class="sxs-lookup"><span data-stu-id="2572d-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="2572d-172">Получение и списка ECFs в Project Online веб-клиента Project.</span><span class="sxs-lookup"><span data-stu-id="2572d-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="2572d-173">В метод ListPWACustomFields реализовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2572d-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="2572d-174">Получение проектов с настраиваемыми полями и ненастраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="2572d-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="2572d-175">При получении проектов с ECFs запрос к службе Project Online необходимо включить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="2572d-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="2572d-176">**IncludeCustomFields** &ndash; Этот элемент запрашивает службу для возврата коллекции PublishedProjects, где каждый опубликованного проекта включает в себя расширение, который поддерживает настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="2572d-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="2572d-177">Если этот элемент не указан, Project Online возвращает объекты PublishedProject, не содержащих данных настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="2572d-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="2572d-178">**IncludeCustomFields.CustomFields** &ndash; этот элемент запрашивает службу для заполнения объектов PublishedProject с данными настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="2572d-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="2572d-179">Следующий запрос указывает код проекта и имя, а также расширение объекта для настраиваемых полей и значения настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="2572d-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="2572d-180">Проверьте каждый из проектов.</span><span class="sxs-lookup"><span data-stu-id="2572d-180">Examine each project.</span></span>
    
   <span data-ttu-id="2572d-181">Объекты проекта, которые используются в этом приложении являются PublishedProject тип, поскольку значения извлекаются и отображаются.</span><span class="sxs-lookup"><span data-stu-id="2572d-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="2572d-182">Если вам потребуется обновить значения данных в один или несколько проектов, выполняет обновление проекта будет извлечено и приложение будет использовать объект DraftProject для получения значения и обновлять проект.</span><span class="sxs-lookup"><span data-stu-id="2572d-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="2572d-183">Доступ к записи ECF для проекта</span><span class="sxs-lookup"><span data-stu-id="2572d-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="2572d-184">Каждый экземпляр ECF разделяет значения поля из оставшейся части ECF сведения.</span><span class="sxs-lookup"><span data-stu-id="2572d-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="2572d-185">Значение поля сохраняется как часть пары "ключ значение".</span><span class="sxs-lookup"><span data-stu-id="2572d-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="2572d-186">Остальные сведения хранятся в объекте CustomField.</span><span class="sxs-lookup"><span data-stu-id="2572d-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="2572d-187">Доступ к значениям ECF в проекте состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="2572d-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="2572d-188">Переход по коллекции настраиваемых полей</span><span class="sxs-lookup"><span data-stu-id="2572d-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="2572d-189">Доступ к надлежащему запись, с помощью двух конструкций.</span><span class="sxs-lookup"><span data-stu-id="2572d-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="2572d-190">Каждый из проектов хранятся связанные записи ECF в двух местах, перечисляемую коллекцию настраиваемых полей и и значения полей как часть пары "ключ значение".</span><span class="sxs-lookup"><span data-stu-id="2572d-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="2572d-191">В пары "ключ значение" внутреннееимя — ключ и значение поля — это значение.</span><span class="sxs-lookup"><span data-stu-id="2572d-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="2572d-192">Используйте словарь для хранения и доступа к значениям поля.</span><span class="sxs-lookup"><span data-stu-id="2572d-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="2572d-193">Свойства ECF, отличных от значений полей, хранятся в объекты CustomField один объект в проекте.</span><span class="sxs-lookup"><span data-stu-id="2572d-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="2572d-194">Используйте коллекцию настраиваемых полей для доступа к ECFs, связанный с отдельного проекта.</span><span class="sxs-lookup"><span data-stu-id="2572d-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="2572d-195">Каждый из проектов хранятся связанные ECFs в семействе сайтов, где каждой записи ECF состоит из ключа — внутреннее имя ECF--и объекта, который содержит значение ECF.</span><span class="sxs-lookup"><span data-stu-id="2572d-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="2572d-196">Перенос словаря для отдельных операций доступа к коллекции.</span><span class="sxs-lookup"><span data-stu-id="2572d-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="2572d-197">Объявление приводится ниже.</span><span class="sxs-lookup"><span data-stu-id="2572d-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="2572d-198">Значение в записи словаря соответствует типу данных ECF.</span><span class="sxs-lookup"><span data-stu-id="2572d-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="2572d-199">Объект для каждого ECF сопоставляется один из различных типов.</span><span class="sxs-lookup"><span data-stu-id="2572d-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="2572d-200">Большинство ECFs используйте простые типы, которые входят в стандартный переменных.</span><span class="sxs-lookup"><span data-stu-id="2572d-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="2572d-201">В следующем фрагменте показано, что минимальной обработки задействованных для нескольких типов:</span><span class="sxs-lookup"><span data-stu-id="2572d-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   <span data-ttu-id="2572d-202">В таблице подстановки ТЕКСТОВЫХ значений, тем не менее, требует дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="2572d-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="2572d-203">Приложение получает в таблице подстановки соответствующие из службы и выводит экземпляра ECF (с одним или несколькими значениями) путем обхода таблицы подстановки.</span><span class="sxs-lookup"><span data-stu-id="2572d-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="2572d-204">В следующем фрагменте кода показан обработки ECFs текста, включая простого значения и с помощью таблицы подстановки:</span><span class="sxs-lookup"><span data-stu-id="2572d-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   <span data-ttu-id="2572d-205">Это приложение выводит просто значения; Тем не менее можно получить дополнительные значения из значения данных.</span><span class="sxs-lookup"><span data-stu-id="2572d-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="2572d-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="2572d-206">ListPWACustomFields</span></span>

<span data-ttu-id="2572d-207">Метод ListPWACustomFields получает и перечислены ECFs, связанных с проектами.</span><span class="sxs-lookup"><span data-stu-id="2572d-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="2572d-208">Этот метод перечислены ECFs, зарегистрированные в экземпляре веб-клиента Project, который может быть связано с отдельные проекты.</span><span class="sxs-lookup"><span data-stu-id="2572d-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="2572d-209">Точка входа для доступа к ECFs используется элемент настраиваемых полей проекта контекста, как показано в следующем запросе:</span><span class="sxs-lookup"><span data-stu-id="2572d-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="2572d-210">Метод не проверяет, чтобы увидеть, использует ли проект конкретных ECF.</span><span class="sxs-lookup"><span data-stu-id="2572d-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2572d-211">См. также</span><span class="sxs-lookup"><span data-stu-id="2572d-211">See also</span></span>

- [<span data-ttu-id="2572d-212">Портал проекта разработки</span><span class="sxs-lookup"><span data-stu-id="2572d-212">Project Development Portal</span></span>](https://developer.microsoft.com/en-us/project)
- [<span data-ttu-id="2572d-213">Обзор: Корпоративные настраиваемые поля и таблицы подстановки</span><span class="sxs-lookup"><span data-stu-id="2572d-213">Overview: Enterprise custom fields and lookup tables</span></span>](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- <span data-ttu-id="2572d-214">[Локальные и корпоративные настраиваемые поля](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="2572d-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="2572d-215">Добавление и редактирование корпоративных настраиваемых полей в Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="2572d-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

