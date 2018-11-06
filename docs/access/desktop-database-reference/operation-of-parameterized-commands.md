---
title: Операция параметризованные команды
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1623b32a5ec52acd086bf028a5c1775daae989e8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997051"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="1404d-102">Операция параметризованные команды</span><span class="sxs-lookup"><span data-stu-id="1404d-102">Operation of parameterized commands</span></span>

<span data-ttu-id="1404d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1404d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1404d-104">Если работа с большой дочерних **записей**, особенно по сравнению с размерами родительского **набора записей**, но для доступа только несколько дочерних главы могут оказаться более эффективно использовать параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="1404d-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="1404d-105">*Без параметров командной* извлекает весь родительских и дочерних **наборов записей**, добавляет столбец с родительским и затем назначает ссылку на главы дочернюю для каждой строки родительского.</span><span class="sxs-lookup"><span data-stu-id="1404d-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="1404d-106">*Параметризованный команда* извлекает весь родительского **набора записей**, но извлекаются только главы **набора записей** при доступе к главе столбца.</span><span class="sxs-lookup"><span data-stu-id="1404d-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="1404d-107">Разницы в стратегии извлечения может привести к значительным производительность.</span><span class="sxs-lookup"><span data-stu-id="1404d-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="1404d-108">Например можно указать следующее:</span><span class="sxs-lookup"><span data-stu-id="1404d-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="1404d-109">Родительскими и дочерними таблицами иметь имя столбца в распространенных, клиент\_идентификатора *.*</span><span class="sxs-lookup"><span data-stu-id="1404d-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="1404d-110">*Команда дочерних* имеет заполнитель «?», на который указывает ссылка предложения (то есть, «... ПАРАМЕТР, 0").</span><span class="sxs-lookup"><span data-stu-id="1404d-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="1404d-111">Предложение параметр относится исключительно к синтаксис команды фигуры.</span><span class="sxs-lookup"><span data-stu-id="1404d-111">The PARAMETER clause pertains solely to the shape command syntax.</span></span> <span data-ttu-id="1404d-112">Не связан с объектом ADO [параметр](parameter-object-ado.md) или коллекцию [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1404d-112">It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="1404d-113">При выполнении команды параметризованный фигуры, происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="1404d-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="1404d-114">*Родительский команда* выполняется и возвращает родительский объект **набора записей** из таблицы Customers.</span><span class="sxs-lookup"><span data-stu-id="1404d-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="1404d-115">Столбец используется в качестве родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="1404d-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="1404d-116">При обращении к ним столбец главы родительской строки *дочерних команда* выполняется с использованием значения customer.cust\_код в качестве значения параметра.</span><span class="sxs-lookup"><span data-stu-id="1404d-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="1404d-117">Все строки в наборе строк поставщика данных, созданный на шаге 3 используются для заполнения дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="1404d-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="1404d-118">В этом примере, являющегося все строки в таблице Orders, в котором окно\_идентификатор равен значение customer.cust\_идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1404d-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="1404d-119">По умолчанию дочерних **записей**s будут кэшироваться на стороне клиента, пока не будут отпущены все ссылки на родительский **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="1404d-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="1404d-120">Чтобы изменить это поведение, установите **набор записей** [динамического свойства](ado-dynamic-property-index.md)**Кэша дочерних строк** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="1404d-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="1404d-121">Ссылку на извлеченных дочерних строк (то есть, главы дочерних **записей**) переводится в столбце главы текущей строки родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="1404d-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="1404d-122">Шаги 3 – 5 повторяются при доступе к главе столбец другой строки.</span><span class="sxs-lookup"><span data-stu-id="1404d-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="1404d-123">Свойство динамического **Кэша дочерние строки** имеет значение **True** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1404d-123">The **Cache Child Rows** dynamic property is set to **True** by default.</span></span> <span data-ttu-id="1404d-124">Поведение кэширования, может изменяться в зависимости от значения параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="1404d-124">The caching behavior varies depending upon the parameter values of the query.</span></span> <span data-ttu-id="1404d-125">В запросе с одним параметром дочерних **записей** значение данного параметра будут кэшироваться между запросами для дочерних с соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="1404d-125">In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value.</span></span> <span data-ttu-id="1404d-126">Это демонстрируется в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="1404d-126">The following code demonstrates this:</span></span>

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

<span data-ttu-id="1404d-127">В запросе с двумя или несколькими параметрами кэшированных дочерних используется только в том случае, если значение параметра соответствует кэшированных значений.</span><span class="sxs-lookup"><span data-stu-id="1404d-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="1404d-128">Параметризованные команды и сложных родительского дочерние отношения</span><span class="sxs-lookup"><span data-stu-id="1404d-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="1404d-129">Для повышения эффективности иерархии типа эквивалентное соединение с помощью параметризованные команды, параметризованные команды можно использовать для поддержки более сложных родительских и дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="1404d-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="1404d-130">Рассмотрим маленьким лига базы данных с двумя таблицами: один, состоящий из группы (группы\_код, группы\_имя), а другой игр (даты, домашняя страница\_группы, посетив\_группы).</span><span class="sxs-lookup"><span data-stu-id="1404d-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="1404d-131">С помощью иерархии без параметров, нет возможности для их связывания рабочих групп и игры таким образом, что дочерних **записей** для каждой группы содержит полный расписание.</span><span class="sxs-lookup"><span data-stu-id="1404d-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="1404d-132">Вы можете создать главы (en), которые содержат Домашняя страница расписание или расписание дорогу, но не оба.</span><span class="sxs-lookup"><span data-stu-id="1404d-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="1404d-133">Причина этого заключается в предложении ссылка ограничивается родительских и дочерних элементов формы (pc1 = cc1) AND (pc2 = pc2).</span><span class="sxs-lookup"><span data-stu-id="1404d-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="1404d-134">Таким образом, если команда включает «team ссылка\_идентификатор кому домашней\_группы, группы\_код на странице веб-узла\_группы», можно получить только игры где группы самой воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1404d-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="1404d-135">Необходимые является "(team\_идентификатор = Домашняя страница\_группы) или (группы\_идентификатор = посетив\_группы)», но поставщик фигура не поддерживает предложение OR.</span><span class="sxs-lookup"><span data-stu-id="1404d-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="1404d-136">Чтобы получить результат, можно использовать параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="1404d-136">To obtain the desired result, you can use a parameterized command.</span></span> <span data-ttu-id="1404d-137">Пример:</span><span class="sxs-lookup"><span data-stu-id="1404d-137">For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="1404d-138">В этом примере использует более высокий уровень гибкости предложения SQL WHERE для получения результатов.</span><span class="sxs-lookup"><span data-stu-id="1404d-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

