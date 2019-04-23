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
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="75dc9-102">Выполнение параметризованных команд</span><span class="sxs-lookup"><span data-stu-id="75dc9-102">Operation of parameterized commands</span></span>

<span data-ttu-id="75dc9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75dc9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75dc9-104">При работе с большим дочерним **наборОм записей**, особенно по сравнению с размером родительского объекта **Recordset**, но при необходимости можно получить доступ только к нескольким дочерним главам, может оказаться более эффективным использовать параметризованную команду.</span><span class="sxs-lookup"><span data-stu-id="75dc9-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="75dc9-105">Непараметризованная *команда* извлекает и все родительские и доЧерние **наборы записей**, добавляет столбец главы к родительскому элементу, а затем назначает ссылку на соответствующую дочернюю главу для каждой родительской строки.</span><span class="sxs-lookup"><span data-stu-id="75dc9-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="75dc9-106">*Параметризованная команда* извлекает весь родительский **набор записей**, но при обращении к столбцу главы извлекается только **набор записей** Chapter.</span><span class="sxs-lookup"><span data-stu-id="75dc9-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="75dc9-107">Эта разница в стратегии извлечения может значительно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="75dc9-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="75dc9-108">Например, вы можете указать следующее:</span><span class="sxs-lookup"><span data-stu-id="75dc9-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="75dc9-109">Родительская и дочерняя таблицы имеют имя столбца Common ID,\_идентификатор Cust *.*</span><span class="sxs-lookup"><span data-stu-id="75dc9-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="75dc9-110">Дочерняя *команда* имеет заполнитель "_км_", к которому относится предложение Relate (то есть "... ПАРАМЕТР 0 ").</span><span class="sxs-lookup"><span data-stu-id="75dc9-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="75dc9-111">Предложение PARAMETER относится только к синтаксису команды Shape.</span><span class="sxs-lookup"><span data-stu-id="75dc9-111">The PARAMETER clause pertains solely to the shape command syntax.</span></span> <span data-ttu-id="75dc9-112">Он не связан ни с одним объектом [параметров](parameter-object-ado.md) ADO, ни с коллекцией [Parameters](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="75dc9-112">It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="75dc9-113">При выполнении команды с параметризованной фигурой происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="75dc9-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="75dc9-114">Выполняется *родительская команда* , которая возвращает родительский **набор записей** из таблицы Customers.</span><span class="sxs-lookup"><span data-stu-id="75dc9-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="75dc9-115">Столбец Chapter добавляется к родительскому набору **записей**.</span><span class="sxs-lookup"><span data-stu-id="75dc9-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="75dc9-116">При доступе к столбцу раздела в родительской строке выполняется *дочерняя команда* с использованием значения идентификатора Customer. cust\_в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="75dc9-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="75dc9-117">Все строки в наборе строк поставщика данных, созданном на шаге 3, используются для заполнения дочернего объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="75dc9-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="75dc9-118">В этом примере это все строки в таблице Orders, в которых идентификатор Cust\_равен значению идентификатора Customer. cust.\_</span><span class="sxs-lookup"><span data-stu-id="75dc9-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="75dc9-119">По умолчанию Дочерний **набор записей**кэшируется в клиенте до тех пор, пока не будут сняты все ссылки на родительский **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="75dc9-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="75dc9-120">Чтобы изменить это поведение, задайте для**дочерних строк в кэше** [динамических свойств](ado-dynamic-property-index.md) **Recordset** **значение false**.</span><span class="sxs-lookup"><span data-stu-id="75dc9-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="75dc9-121">Ссылка на извлеченные дочерние строки (то есть главу дочернего объекта **Recordset**) помещается в столбец Chapter текущей строки родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="75dc9-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="75dc9-122">Шаги 3 – 5 повторяются при доступе к столбцу Chapter другой строки.</span><span class="sxs-lookup"><span data-stu-id="75dc9-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="75dc9-123">Динамическое свойство **Cache ДочернИе строки** по умолчанию имеет значение **true** .</span><span class="sxs-lookup"><span data-stu-id="75dc9-123">The **Cache Child Rows** dynamic property is set to **True** by default.</span></span> <span data-ttu-id="75dc9-124">Поведение кэширования зависит от значений параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="75dc9-124">The caching behavior varies depending upon the parameter values of the query.</span></span> <span data-ttu-id="75dc9-125">В запросе с одним параметром дочерний **набор записей** для данного значения параметра кэшируется между запросами для дочернего элемента с таким значением.</span><span class="sxs-lookup"><span data-stu-id="75dc9-125">In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value.</span></span> <span data-ttu-id="75dc9-126">Это показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="75dc9-126">The following code demonstrates this:</span></span>

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

<span data-ttu-id="75dc9-127">В запросе с двумя или более параметрами кэшированный дочерний объект используется только в том случае, если все значения параметров совпадают с кэшированными значениями.</span><span class="sxs-lookup"><span data-stu-id="75dc9-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="75dc9-128">Параметризованные команды и сложные родительские дочерние связи</span><span class="sxs-lookup"><span data-stu-id="75dc9-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="75dc9-129">В дополнение к использованию параметризованных команд для улучшения производительности иерархии типов с эквивалентным присоединением, параметризованные команды можно использовать для поддержки более сложных отношений "родитель — потомок".</span><span class="sxs-lookup"><span data-stu-id="75dc9-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="75dc9-130">Например, рассмотрим несколько баз данных League с двумя таблицами: одна из которых состоит из групп (идентификатор\_группы, имя\_группы) и других игр (Дата, домашняя\_группа, посещение\_команды).</span><span class="sxs-lookup"><span data-stu-id="75dc9-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="75dc9-131">При использовании непараметризованной иерархии невозможно связать таблицы Teams и Games таким образом, чтобы дочерний **набор записей** для каждой команды содержал полное расписание.</span><span class="sxs-lookup"><span data-stu-id="75dc9-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="75dc9-132">Вы можете создавать главы, содержащие расписание для домашнего или дорогого, но не оба.</span><span class="sxs-lookup"><span data-stu-id="75dc9-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="75dc9-133">Это связано с тем, что предложение СВЯЗЫВАНИЯ позволяет ограничить связи между родительскими и дочерними элементами формы (PC1 = CC1) и (PC2 = PC2).</span><span class="sxs-lookup"><span data-stu-id="75dc9-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="75dc9-134">Таким образом, если команда соОТНЕСЕНия идентификатора\_группы с домашней\_командой, идентификатор\_группы для посещения\_команды, вы получите только те игры, в которых команда воспроизводила себя.</span><span class="sxs-lookup"><span data-stu-id="75dc9-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="75dc9-135">Вы хотите: "(идентификатор группы\_= Домашняя\_группа) или (код\_группы = посещение\_команды)", но поставщик фигур не поддерживает предложение OR.</span><span class="sxs-lookup"><span data-stu-id="75dc9-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="75dc9-136">Чтобы получить требуемый результат, можно использовать параметризованную команду.</span><span class="sxs-lookup"><span data-stu-id="75dc9-136">To obtain the desired result, you can use a parameterized command.</span></span> <span data-ttu-id="75dc9-137">Пример:</span><span class="sxs-lookup"><span data-stu-id="75dc9-137">For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="75dc9-138">В этом примере показано, как использовать большую гибкость предложения WHERE в SQL, чтобы получить необходимый результат.</span><span class="sxs-lookup"><span data-stu-id="75dc9-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

