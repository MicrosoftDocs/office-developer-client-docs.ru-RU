---
title: Выполнение параметризованных команд
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288289"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="b430f-102">Выполнение параметризованных команд</span><span class="sxs-lookup"><span data-stu-id="b430f-102">Operation of parameterized commands</span></span>

<span data-ttu-id="b430f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b430f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b430f-104">Если вы работаете с большим ребенком **Recordset**, особенно по сравнению с размером родительского **recordset,** но вам необходимо получить доступ только к нескольким детским главам, возможно, будет эффективнее использовать параметризованную команду.</span><span class="sxs-lookup"><span data-stu-id="b430f-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="b430f-105">*Непараметровная* команда извлекает все родительские и детские записи, придает столбец главы родительскому, а затем назначает ссылку на связанную детскую главу для каждой родительской строки. </span><span class="sxs-lookup"><span data-stu-id="b430f-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="b430f-106">*Параметризованная команда* извлекает весь родительский набор **записей,** но извлекает только главу **Recordset** при доступе к столбце главы.</span><span class="sxs-lookup"><span data-stu-id="b430f-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="b430f-107">Это различие в стратегии ирисовки может принести значительные преимущества производительности.</span><span class="sxs-lookup"><span data-stu-id="b430f-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="b430f-108">Например, можно указать следующее:</span><span class="sxs-lookup"><span data-stu-id="b430f-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="b430f-109">Родительские и детские таблицы имеют общее имя столбца, cust \_ *id.*</span><span class="sxs-lookup"><span data-stu-id="b430f-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="b430f-110">В *детской команде* есть местоодатель "?" , на который ссылается пункт RELATE (то есть "... PARAMETER 0").</span><span class="sxs-lookup"><span data-stu-id="b430f-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="b430f-111">Пункт PARAMETER относится исключительно к синтаксису командной фигуры.</span><span class="sxs-lookup"><span data-stu-id="b430f-111">The PARAMETER clause pertains solely to the shape command syntax.</span></span> <span data-ttu-id="b430f-112">Он не связан ни с объектом ADO [Parameter,](parameter-object-ado.md) ни с коллекцией [Параметры.](parameters-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b430f-112">It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="b430f-113">При выполнении команды заданной фигуры возникает следующее:</span><span class="sxs-lookup"><span data-stu-id="b430f-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="b430f-114">Родительская *команда* выполняется и возвращает родительский **набор записей** из таблицы Клиенты.</span><span class="sxs-lookup"><span data-stu-id="b430f-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="b430f-115">Столбец главы примыкает к родительскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="b430f-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="b430f-116">При доступе к столбцу главы родительской строки детская команда выполняется с использованием значения customer.cust id в качестве значения  \_ параметра.</span><span class="sxs-lookup"><span data-stu-id="b430f-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="b430f-117">Все строки в строке поставщика данных, созданной в шаге 3, используются для заполнения детского **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="b430f-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="b430f-118">В этом примере это все строки в таблице Orders, в которой cust id равен значению \_ customer.cust \_ id.</span><span class="sxs-lookup"><span data-stu-id="b430f-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="b430f-119">По умолчанию ребенок **Recordset** s будет кэшироваться на клиенте до тех пор, пока не будут выпущены все ссылки на родительский **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="b430f-119">By default, the child **Recordset** s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="b430f-120">Чтобы изменить это поведение, установите динамическое свойство **Recordset** [](ado-dynamic-property-index.md)**Cache Child Rows** **false**.</span><span class="sxs-lookup"><span data-stu-id="b430f-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="b430f-121">Ссылка на извлеченные детские строки (то есть главу детского набора записей) помещается в столбец главы текущего строки родительского **recordset**.</span><span class="sxs-lookup"><span data-stu-id="b430f-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="b430f-122">Действия 3-5 повторяются при доступе к столбце главы другой строки.</span><span class="sxs-lookup"><span data-stu-id="b430f-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="b430f-123">Динамическое **свойство "Детские строки кэша"** по умолчанию настроено на **Значение True.**</span><span class="sxs-lookup"><span data-stu-id="b430f-123">The **Cache Child Rows** dynamic property is set to **True** by default.</span></span> <span data-ttu-id="b430f-124">Поведение кэшинга зависит от значений параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="b430f-124">The caching behavior varies depending upon the parameter values of the query.</span></span> <span data-ttu-id="b430f-125">В запросе с одним параметром ребенок **Recordset** для заданного значения параметра будет кэшироваться между запросами для ребенка с этим значением.</span><span class="sxs-lookup"><span data-stu-id="b430f-125">In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value.</span></span> <span data-ttu-id="b430f-126">Следующий код демонстрирует следующее:</span><span class="sxs-lookup"><span data-stu-id="b430f-126">The following code demonstrates this:</span></span>

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

<span data-ttu-id="b430f-127">В запросе с двумя или несколькими параметрами кэшный ребенок используется только в том случае, если все значения параметров соответствуют кэшным значениям.</span><span class="sxs-lookup"><span data-stu-id="b430f-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="b430f-128">Параметризированные команды и сложные родительские отношения с детьми</span><span class="sxs-lookup"><span data-stu-id="b430f-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="b430f-129">Помимо использования параметризированных команд для повышения производительности иерархии типов equi-join можно использовать параметризированные команды для поддержки более сложных отношений между родителями и детьми.</span><span class="sxs-lookup"><span data-stu-id="b430f-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="b430f-130">Например, рассмотрим базу данных Little League с двумя таблицами: одну из команд (ид команды, имя команды) и другую из игр (дата, домашняя команда, команда \_ \_ \_ \_ посещения).</span><span class="sxs-lookup"><span data-stu-id="b430f-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="b430f-131">С помощью непараметровизированной иерархии не существует способа связать команды и таблицы  игр таким образом, чтобы детский набор записей для каждой команды содержит полное расписание.</span><span class="sxs-lookup"><span data-stu-id="b430f-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="b430f-132">Можно создать главы, содержащие домашнее расписание или расписание дорог, но не оба.</span><span class="sxs-lookup"><span data-stu-id="b430f-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="b430f-133">Это связано с тем, что пункт RELATE ограничивает отношения между родителями и детьми формы (pc1=cc1) и (pc2=pc2).</span><span class="sxs-lookup"><span data-stu-id="b430f-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="b430f-134">Таким образом, если ваша команда включала "RELATE team \_ id TO home \_ team, team \_ id TO visiting team", вы получите только игры, в которых команда играла \_ сама.</span><span class="sxs-lookup"><span data-stu-id="b430f-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="b430f-135">Требуется "(team \_ id=home \_ team) OR (team \_ id=visiting team)", но поставщик shape не поддерживает пункт \_ OR.</span><span class="sxs-lookup"><span data-stu-id="b430f-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="b430f-136">Чтобы получить нужный результат, можно использовать параметризованную команду.</span><span class="sxs-lookup"><span data-stu-id="b430f-136">To obtain the desired result, you can use a parameterized command.</span></span> <span data-ttu-id="b430f-137">Пример.</span><span class="sxs-lookup"><span data-stu-id="b430f-137">For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="b430f-138">В этом примере используются более гибкие положения SQL WHERE, чтобы получить необходимый результат.</span><span class="sxs-lookup"><span data-stu-id="b430f-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

