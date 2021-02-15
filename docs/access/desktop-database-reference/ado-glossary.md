---
title: ActiveX data Objects (ADO) glossary
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284836"
---
# <a name="ado-glossary"></a><span data-ttu-id="4ea7f-102">Глоссарий ADO</span><span class="sxs-lookup"><span data-stu-id="4ea7f-102">ADO glossary</span></span>

<span data-ttu-id="4ea7f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ea7f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="a"></a><span data-ttu-id="4ea7f-104">A</span><span class="sxs-lookup"><span data-stu-id="4ea7f-104">A</span></span>

<span data-ttu-id="4ea7f-105">**абсолютный URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-105">**absolute URL**</span></span>

<span data-ttu-id="4ea7f-106">Полное URL-адрес, который указывает расположение ресурса, который находится в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-106">A fully qualified URL that specifies the location of a resource that resides on the Internet or an intranet.</span></span> <span data-ttu-id="4ea7f-107">См. также **URL-адрес** **и относительный URL-адрес.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-107">See also **URL** and **relative URL**.</span></span>

<span data-ttu-id="4ea7f-108">**Элемент ActiveX**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-108">**ActiveX control**</span></span>

<span data-ttu-id="4ea7f-109">Самозаверяющий in-process COM-компонент, который часто имеет визуальный элемент во время разработки или во время работы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-109">Self-registering, in-process COM component that often has a visual element either at design time or run time.</span></span> <span data-ttu-id="4ea7f-110">ActiveX элементы управления также могут взаимодействовать с контейнером Active Document, например Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-110">ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</span></span>

<span data-ttu-id="4ea7f-111">**ADISAPI (расширенный интерфейс программирования приложений Internet Server для данных)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="4ea7f-112">IsAPI DLL, которая обеспечивает разметку, управление автоматизацией, маршалинг **наборов** записей и упаковку MIME.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-112">An ISAPI DLL that provides parsing, Automation control, **Recordset** marshaling, and MIME packaging.</span></span> <span data-ttu-id="4ea7f-113">Компонент ADISAPI работает через API, предоставляемый службами IIS.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-113">The ADISAPI component works through the API provided by Internet Information Services (IIS).</span></span> <span data-ttu-id="4ea7f-114">См. также **ISAPI.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-114">See also **ISAPI**.</span></span>

<span data-ttu-id="4ea7f-115">**агрегатная функция**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-115">**aggregate function**</span></span>

<span data-ttu-id="4ea7f-116">В запросе функция, например COUNT, AVG или STDEV, которая вычисляет значение, используя все строки в столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-116">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table.</span></span> <span data-ttu-id="4ea7f-117">При написании выражений и программировании можно использовать SQL (включая три перечисленных выше) и агрегатные функции домена для определения различных статистических данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-117">In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</span></span>

<span data-ttu-id="4ea7f-118">**alias**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-118">**alias**</span></span>

<span data-ttu-id="4ea7f-119">Альтернативное имя, которое вы даете столбцу или выражению в SQL SELECT, часто короче или осмысленнее.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-119">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful.</span></span> <span data-ttu-id="4ea7f-120">Например, BobSales — это псевдоним в следующем заявлении SELECT: "Select wr-Sales as BobSales from SalesDB".</span><span class="sxs-lookup"><span data-stu-id="4ea7f-120">For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB".</span></span> <span data-ttu-id="4ea7f-121">Псевдоним можно использовать для динамического назначения столбцов для управления привязками объекта **DataControl.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-121">An alias can be used to dynamically assign columns to control bindings on the **DataControl** object.</span></span>

<span data-ttu-id="4ea7f-122">**потоковая цепочка apartment**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-122">**apartment threading**</span></span>

<span data-ttu-id="4ea7f-123">Модель потоков COM, в которой все вызовы объекта происходят в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-123">A COM threading model where all calls to an object occur on one thread.</span></span> <span data-ttu-id="4ea7f-124">В потоке в многоквартирных домах COM синхронизирует и маршалирует вызовы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-124">In apartment threading, COM synchronizes and marshals calls.</span></span> <span data-ttu-id="4ea7f-125">См. также **COM.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-125">See also **COM**.</span></span>

<span data-ttu-id="4ea7f-126">**асинхронная операция**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-126">**asynchronous operation**</span></span>

<span data-ttu-id="4ea7f-127">Операция, которая возвращает управление вызываемой программе, не дожидаясь завершения операции.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-127">An operation that returns control to the calling program without waiting for the operation to complete.</span></span> <span data-ttu-id="4ea7f-128">Перед завершением операции выполнение кода продолжается.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-128">Before the operation is complete, code execution continues.</span></span> <span data-ttu-id="4ea7f-129">См. также **синхронную операцию.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-129">See also **synchronous operation**.</span></span>

<span data-ttu-id="4ea7f-130">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-130">Return to top</span></span>

## <a name="b"></a><span data-ttu-id="4ea7f-131">B</span><span class="sxs-lookup"><span data-stu-id="4ea7f-131">B</span></span>

<span data-ttu-id="4ea7f-132">**запись привязки**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-132">**binding entry**</span></span>

<span data-ttu-id="4ea7f-133">Сопоставление между полем в таблице и переменной.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-133">A mapping between a field in a table and a variable.</span></span> <span data-ttu-id="4ea7f-134">В расширениях ADO Visual C++ поля **Recordset** соединит с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-134">In the ADO Visual C++ extensions, **Recordset** fields are mapped to C/C++ variables.</span></span>

<span data-ttu-id="4ea7f-135">**битоваяmask**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-135">**bitmask**</span></span>

<span data-ttu-id="4ea7f-136">Числовые значения, предназначенные для по битового сравнения значений с другими числовые значения, как правило, для пометки параметров в параметрах или возвращаемом значении.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-136">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</span></span> <span data-ttu-id="4ea7f-137">Обычно это сравнение происходит с помощью по битовой логики операторов, таких как **And** и **Or** в Visual Basic, а также **&** на **|** C++.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-137">Usually this comparison is done with bitwise logical operators, such as **And** and **Or** in Visual Basic, **&** and **|** in C++.</span></span>

<span data-ttu-id="4ea7f-138">Например, значения ADO **FieldAttributeEnum** можно использовать в качестве битовыхmasks для определения атрибутов поля.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-138">For example, the ADO **FieldAttributeEnum** values can be used as bitmasks to determine the attributes of a field.</span></span> <span data-ttu-id="4ea7f-139">Предположим, вы хотите определить, можно ли обновить поле.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-139">Suppose you wanted to determine if a field was updateable.</span></span> <span data-ttu-id="4ea7f-140">Вы можете проверить это с помощью следующего выражения в Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4ea7f-140">You could test for this with the following expression in Visual Basic:</span></span>  
  

<span data-ttu-id="4ea7f-141">Если результат имеет true, поле можно обновить.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-141">If the result is TRUE, then the field is updateable.</span></span>

<span data-ttu-id="4ea7f-142">**bookmark**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-142">**bookmark**</span></span>

<span data-ttu-id="4ea7f-143">Маркер, который уникальным образом идентифицирует строку в наборе строк, чтобы пользователь быстро переходить к ней.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-143">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</span></span>

<span data-ttu-id="4ea7f-144">**бизнес-объект**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-144">**business object**</span></span>

<span data-ttu-id="4ea7f-145">Объект, который выполняет определенный набор операций, например проверку данных или логику бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-145">An object that performs a defined set of operations, such as data validation or business rule logic.</span></span> <span data-ttu-id="4ea7f-146">Бизнес-объекты обычно находятся на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-146">Business objects usually reside on the middle tier.</span></span>

<span data-ttu-id="4ea7f-147">**бизнес-правило**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-147">**business rule**</span></span>

<span data-ttu-id="4ea7f-148">Сочетание проверочных изменений, проверок при выходе в систему, поиска базы данных, политик и алгоритмических преобразований, составляющих способ ведения бизнеса на предприятии.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-148">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</span></span> <span data-ttu-id="4ea7f-149">Также называется *бизнес-логикой.*</span><span class="sxs-lookup"><span data-stu-id="4ea7f-149">Also known as *business logic*.</span></span>

<span data-ttu-id="4ea7f-150">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-150">Return to top</span></span>

## <a name="c"></a><span data-ttu-id="4ea7f-151">C</span><span class="sxs-lookup"><span data-stu-id="4ea7f-151">C</span></span>

<span data-ttu-id="4ea7f-152">**вычисляемая выражение**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-152">**calculated expression**</span></span>

<span data-ttu-id="4ea7f-153">Выражение, которое не является постоянным, но значение которого зависит от других значений.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-153">An expression that is not constant, but whose value depends upon other values.</span></span> <span data-ttu-id="4ea7f-154">Для оценки вычисленное выражение должно получать и вычислять значения из других источников, как правило, в других полях или строках.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-154">To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</span></span>

<span data-ttu-id="4ea7f-155">**chapter**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-155">**chapter**</span></span>

<span data-ttu-id="4ea7f-156">Ссылка на диапазон строк из источника данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-156">A reference to a range of rows from a data source.</span></span> <span data-ttu-id="4ea7f-157">В ADO глава обычно является ссылкой на другой **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-157">In ADO, a chapter is typically a reference to another **Recordset**.</span></span>

<span data-ttu-id="4ea7f-158">Столбцы главы по возможности определяют отношение    "родитель-потомок", где родительским  является набор записей, содержащий столбец главы, а потомок — набор записей, представленный главой. </span><span class="sxs-lookup"><span data-stu-id="4ea7f-158">Chapter columns make it possible to define a *parent-child* relationship where the *parent* is the **Recordset** containing the chapter column and the *child* is the **Recordset** represented by the chapter.</span></span>

<span data-ttu-id="4ea7f-159">**chapter-alias**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-159">**chapter-alias**</span></span>

<span data-ttu-id="4ea7f-160">Псевдоним, который ссылается на столбец, который был придан родительскому столбце.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-160">An alias that refers to the column appended to the parent.</span></span>

<span data-ttu-id="4ea7f-161">**кодировка**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-161">**character set**</span></span>

<span data-ttu-id="4ea7f-162">Сопоставление набора символов с их числами.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-162">A mapping of a set of characters to their numeric values.</span></span> <span data-ttu-id="4ea7f-163">Например, Юникод — это 16-битный набор символов, способный кодировать все известные символы и использоваться в качестве всемирного стандарта кодирования символов.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-163">For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</span></span>

<span data-ttu-id="4ea7f-164">**child**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-164">**child**</span></span>

<span data-ttu-id="4ea7f-165">Зависимая сторона иерархической связи.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-165">The dependent side of a hierarchical relationship.</span></span> <span data-ttu-id="4ea7f-166">Child — это узел в иерархической структуре, который находится над другим узлом (ближе к корню).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-166">A child is a node in a hierarchical structure that has another node above it (closer to the root).</span></span> <span data-ttu-id="4ea7f-167">См. **также псевдоним "родитель-родитель",** **"родительский".** </span><span class="sxs-lookup"><span data-stu-id="4ea7f-167">See also **child-alias**, **parent-child relationship**, **parent**.</span></span>

<span data-ttu-id="4ea7f-168">**child-alias**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-168">**child-alias**</span></span>

<span data-ttu-id="4ea7f-169">Псевдоним, который ссылается на child.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-169">An alias that refers to the child.</span></span> <span data-ttu-id="4ea7f-170">См. **также псевдоним**, **child**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-170">See also **alias**, **child**.</span></span>

<span data-ttu-id="4ea7f-171">**CLSID (идентификатор класса)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-171">**CLSID (class identifier)**</span></span>

<span data-ttu-id="4ea7f-172">Универсальный уникальный идентификатор (UUID), определяющие com-компонент.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-172">A universally unique identifier (UUID) that identifies a COM component.</span></span> <span data-ttu-id="4ea7f-173">Каждый компонент COM имеет свой CLSID в реестре Windows, чтобы его могли загружать другие приложения.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-173">Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications.</span></span> <span data-ttu-id="4ea7f-174">См. также **ProgID**, **COM**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-174">See also **ProgID**, **COM**.</span></span>

<span data-ttu-id="4ea7f-175">**уровень клиента**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-175">**client tier**</span></span>

<span data-ttu-id="4ea7f-176">Логический уровень распределенной системы, которая обычно представляет данные пользователю и обрабатывает входные данные пользователя, иногда называется *интерфейсным.*</span><span class="sxs-lookup"><span data-stu-id="4ea7f-176">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the *front end*.</span></span> <span data-ttu-id="4ea7f-177">Обычно клиентский уровень запрашивает данные с сервера на основе входных данных, а затем форматирование и отображение результата.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-177">Usually, the client tier requests data from a server based on input, and then formats and displays the result.</span></span> <span data-ttu-id="4ea7f-178">См. также **средний уровень,** **уровень источника данных,** **распределенные приложения.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-178">See also **middle tier**, **data source tier**, **distributed application**.</span></span>

<span data-ttu-id="4ea7f-179">**COM (объектная модель компонента)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-179">**COM (Component Object Model)**</span></span>

<span data-ttu-id="4ea7f-180">Двоичный стандарт, позволяющий объектам вести межсеансовую среду независимо от языка, на котором они были разработаны или на каких компьютерах они находятся.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-180">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside.</span></span> <span data-ttu-id="4ea7f-181">Технологии на основе COM включают ActiveX элементы управления, автоматизацию и связывание объектов и их встраивку (OLE).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-181">COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE).</span></span> <span data-ttu-id="4ea7f-182">COM позволяет объекту раскрыть свои функции для других компонентов и для работы с приложениями.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-182">COM allows an object to expose its functionality to other components and to host applications.</span></span> <span data-ttu-id="4ea7f-183">Он определяет, как объект предоставляет себя и как это экспозиция работает в процессах и в сетях.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-183">It defines both how the object exposes itself and how this exposure works across processes and across networks.</span></span> <span data-ttu-id="4ea7f-184">COM также определяет жизненный цикл объекта.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-184">COM also defines the object's life cycle.</span></span>

<span data-ttu-id="4ea7f-185">**Компонент COM**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-185">**COM component**</span></span>

<span data-ttu-id="4ea7f-186">Двоичный файл , например DLL, OCX и некоторые EXE-файлы, который поддерживает стандарт COM для предоставления объектов.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-186">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects.</span></span> <span data-ttu-id="4ea7f-187">Такой файл содержит код для одного или нескольких фабрик классов, классов COM, механизмов записи реестра, загрузки кода и так далее.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-187">Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</span></span>

<span data-ttu-id="4ea7f-188">**оператор сравнения**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-188">**comparison operator**</span></span>

<span data-ttu-id="4ea7f-189">Оператор, который сравнивает два выражения и возвращает значение boolean.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-189">An operator that compares two expressions and returns a Boolean value.</span></span>

<span data-ttu-id="4ea7f-190">Параметр условия, который может быть выражен как \> " (больше), \< " " (меньше), "=" (равно), " \> =" (больше или равно), " \< =" (меньше или равно), \< \> " " (не равно) или "like" (соответствие шаблона).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-190">A criteria parameter that may be expressed as "\>" (greater than), "\<" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="4ea7f-191">**component**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-191">**component**</span></span>

<span data-ttu-id="4ea7f-192">Объект, который инкапсулирует данные и код и предоставляет хорошо определенный набор общедоступных служб.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-192">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

<span data-ttu-id="4ea7f-193">**составной файл**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-193">**compound file**</span></span>

<span data-ttu-id="4ea7f-194">Реализация структурированного хранилища COM для файлов.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-194">An implementation of COM structured storage for files.</span></span> <span data-ttu-id="4ea7f-195">Составной файл хранит отдельные объекты в одном структурированный файл, состоящий из двух основных элементов: объектов хранилища и потоковых объектов.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-195">A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="4ea7f-196">Вместе они функционируют как файловая система в файле.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-196">Together, they function like a file system within a file.</span></span> <span data-ttu-id="4ea7f-197">Дополнительные сведения см. в составных файлах в Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-197">For more information, see Compound Files in the Microsoft Platform SDK.</span></span>

<span data-ttu-id="4ea7f-198">Несколько отдельных файлов, связанных в одном физическом файле.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-198">A number of individual files bound together in one physical file.</span></span> <span data-ttu-id="4ea7f-199">К каждому отдельному файлу в составных файлах можно получить доступ как к одному физическому файлу.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-199">Each individual file in a compound file can be accessed as if it were a single physical file.</span></span>

<span data-ttu-id="4ea7f-200">**constant**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-200">**constant**</span></span>

<span data-ttu-id="4ea7f-201">Числовая или строковая строка, которая не меняется.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-201">A numeric or string value that does not change.</span></span> <span data-ttu-id="4ea7f-202">Именуемые enumerations ADO (enumerated constants) могут использоваться в коде вместо фактических значений, например **adUseClient** — это константа, значение которой 3.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-202">Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, **adUseClient** is a constant whose value is 3.</span></span> <span data-ttu-id="4ea7f-203">(Const adUseClient = 3).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-203">(Const adUseClient = 3).</span></span> <span data-ttu-id="4ea7f-204">См. **также enumeration**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-204">See also **enumeration**.</span></span>

<span data-ttu-id="4ea7f-205">**курсор**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-205">**cursor**</span></span>

<span data-ttu-id="4ea7f-206">Элемент базы данных, который управляет навигацией, возможностью обновления данных и видимостью изменений, внесенных в базу данных другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-206">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</span></span>

<span data-ttu-id="4ea7f-207">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-207">Return to top</span></span>

## <a name="d"></a><span data-ttu-id="4ea7f-208">D</span><span class="sxs-lookup"><span data-stu-id="4ea7f-208">D</span></span>

<span data-ttu-id="4ea7f-209">**привязка данных**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-209">**data binding**</span></span>

<span data-ttu-id="4ea7f-210">Процесс связывание объектов или элементов управления приложения с источником данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-210">The process of associating the objects or controls of an application to a data source.</span></span> <span data-ttu-id="4ea7f-211">Связанный с источником данных контроль называется привязанным *к данным.*</span><span class="sxs-lookup"><span data-stu-id="4ea7f-211">A control associated with a data source is called a *data-bound control*.</span></span>

<span data-ttu-id="4ea7f-212">Содержимое привязанного к данным управления связано со значениями из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-212">The contents of a data-bound control are associated with values from a database.</span></span> <span data-ttu-id="4ea7f-213">Например, при обновлении строк в объекте **Recordset** можно обновить сетку, привязанную к объекту **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-213">For example, a grid control that is bound to a **Recordset** object can be updated when the rows in the **Recordset** are updated.</span></span> <span data-ttu-id="4ea7f-214">Когда набор записей извлекает новые **значения,** в сетке отображаются новые значения.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-214">When new values are retrieved by the **Recordset**, new values are displayed in the grid.</span></span>

<span data-ttu-id="4ea7f-215">**поставщик данных**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-215">**data provider**</span></span>

<span data-ttu-id="4ea7f-216">Программное обеспечение, которое предоставляет данные приложению ADO напрямую или через поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-216">Software that exposes data to an ADO application either directly or via a service provider.</span></span> <span data-ttu-id="4ea7f-217">См. также **поставщик услуг.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-217">See also **service provider**.</span></span>

<span data-ttu-id="4ea7f-218">**формирование данных**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-218">**data shaping**</span></span>

<span data-ttu-id="4ea7f-219">Метод, который использует формализованный синтаксис (называемый языком **фигуры)** для определения специализированного объекта **Recordset** (называемого фигурным набором записей), который содержит не только данные, но и ссылки на другие объекты **Recordset** и/или вычисленные значения на основе этих других объектов **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-219">A technique which makes use of a formalized syntax (called **Shape language**) to define a specialized **Recordset** object (called a **shaped Recordset**) that contains not just data, but also references to other **Recordset** objects and/or computed values based on those other **Recordset** objects.</span></span>

<span data-ttu-id="4ea7f-220">**уровень источника данных**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-220">**data source tier**</span></span>

<span data-ttu-id="4ea7f-221">Логический уровень распределенной системы, который представляет компьютер под управлением DBMS, например SQL Server данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-221">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database.</span></span> <span data-ttu-id="4ea7f-222">См. также **уровень клиента,** **средний уровень,** **распределенные приложения.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-222">See also **client tier**, **middle tier**, **distributed application**.</span></span>

<span data-ttu-id="4ea7f-223">**DCOM**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-223">**DCOM**</span></span>

<span data-ttu-id="4ea7f-224">Проводной протокол, позволяющий com-компонентам напрямую взаимодействовать друг с другом по сети.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-224">A wire protocol that enables COM components to communicate directly with each other across a network.</span></span> <span data-ttu-id="4ea7f-225">См. также **COM**, **компонент**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-225">See also **COM**, **component**.</span></span>

<span data-ttu-id="4ea7f-226">**DDL (язык определения данных)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-226">**DDL (Data Definition Language)**</span></span>

<span data-ttu-id="4ea7f-227">Эти заявления в SQL, которые определяют, в отличие от управления данными.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-227">Those statements in SQL that define, as opposed to manipulate, data.</span></span> <span data-ttu-id="4ea7f-228">Схема базы данных создается или изменена с помощью DDL.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-228">The schema of a database is created or modified with DDL.</span></span> <span data-ttu-id="4ea7f-229">Например, **CREATE TABLE,** **CREATE INDEX,** **GRANT** и **REVOKE** SQL DDL.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-229">For example, **CREATE TABLE**, **CREATE INDEX**, **GRANT**, and **REVOKE** are SQL DDL statements.</span></span>

<span data-ttu-id="4ea7f-230">**поток по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-230">**default stream**</span></span>

<span data-ttu-id="4ea7f-231">Текстовый или двоичный поток (представленный объектом **Stream),** связанный с объектами **Record** или **Recordset** при использовании определенных поставщиков OLE DB, таких как поставщик Microsoft OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-231">A text or binary stream (represented by a **Stream** object) that is associated with **Record** or **Recordset** objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="4ea7f-232">Поток по умолчанию обычно содержит содержимое файла, например HTML-код для корня веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-232">The default stream typically contains the contents of a file such as the HTML code for the root of a website.</span></span>

<span data-ttu-id="4ea7f-233">**распределенные приложения**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-233">**distributed application**</span></span>

<span data-ttu-id="4ea7f-234">Программа, написанная для разделения обработки на несколько компьютеров по сети.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-234">A program written so that the processing can be divided across multiple computers over a network.</span></span> <span data-ttu-id="4ea7f-235">Как правило, распределенное приложение делится на уровни представления, бизнес-логики и хранения *данных.*</span><span class="sxs-lookup"><span data-stu-id="4ea7f-235">Typically, a distributed application is divided into presentation, business logic, and data store layers, or *tiers*.</span></span> <span data-ttu-id="4ea7f-236">См. также **уровень клиента,** **средний уровень,** **уровень источника данных.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-236">See also **client tier**, **middle tier**, **data source tier**.</span></span>

<span data-ttu-id="4ea7f-237">**disconnected Recordset**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-237">**disconnected Recordset**</span></span>

<span data-ttu-id="4ea7f-238">Объект **Recordset** в клиентском кэше, который больше не имеет прямого подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-238">A **Recordset** object in a client cache that no longer has a live connection to the server.</span></span> <span data-ttu-id="4ea7f-239">Если исходный источник данных по какой-либо причине требуется получить доступ к исходному источнику данных, например к обновлению данных, подключение необходимо повторно установить.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-239">If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established.</span></span> <span data-ttu-id="4ea7f-240">Однако доступ к коллекциям, свойствам и методам отключенного объекта **Recordset** по-прежнему можно получить.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-240">However, the collections, properties, and methods of a disconnected **Recordset** can still be accessed.</span></span>

<span data-ttu-id="4ea7f-241">**DLL (библиотека динамической ссылки)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-241">**DLL (dynamic-link library)**</span></span>

<span data-ttu-id="4ea7f-242">Файл, содержащий одну или несколько функций, которые компилются, связываются и хранятся отдельно от процессов, которые их используют.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-242">A file that contains one or more functions that are compiled, linked, and stored separately from the processes that use them.</span></span> <span data-ttu-id="4ea7f-243">Операционная система сопоирует DLL в адресное пространство вызываемого процесса при запуске процесса или во время его работы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-243">The operating system maps the DLLs into the address space of the calling process when the process is starting, or while it is running.</span></span>

<span data-ttu-id="4ea7f-244">**DML (язык обработки данных)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-244">**DML (Data Manipulation Language)**</span></span>

<span data-ttu-id="4ea7f-245">Эти заявления в SQL, которые изменяют данные, а не определяют их.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-245">Those statements in SQL that manipulate, as opposed to define, data.</span></span> <span data-ttu-id="4ea7f-246">Значения в базе данных выбираются и меняются с помощью DML.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-246">The values in a database are selected and modified with DML.</span></span> <span data-ttu-id="4ea7f-247">Например, **INSERT,** **UPDATE,** **DELETE** и **SELECT** SQL DML.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-247">For example, **INSERT**, **UPDATE**, **DELETE**, and **SELECT** are SQL DML statements.</span></span>

<span data-ttu-id="4ea7f-248">**поставщик источника документов**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-248">**document source provider**</span></span>

<span data-ttu-id="4ea7f-249">Особый класс поставщиков, которые управляют папками и документами.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-249">A special class of providers that manage folders and documents.</span></span> <span data-ttu-id="4ea7f-250">Когда документ представлен объектом **Record** или папка документов представлен объектом **Recordset,** поставщик источника документов заполняет эти объекты уникальным набором полей, описывая характеристики документа, а не сам документ.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-250">When a document is represented by a **Record** object, or a folder of documents is represented by a **Recordset** object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself.</span></span> <span data-ttu-id="4ea7f-251">См. также **запись ресурса.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-251">See also **resource record**.</span></span>

<span data-ttu-id="4ea7f-252">**DSN (имя источника данных)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-252">**DSN (data source name)**</span></span>

<span data-ttu-id="4ea7f-253">Коллекция сведений, используемых для подключения приложения к определенной базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-253">The collection of information used to connect your application to a particular ODBC database.</span></span> <span data-ttu-id="4ea7f-254">Диспетчер драйверов ODBC использует эти сведения для создания подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-254">The ODBC Driver Manager uses this information to create a connection to the database.</span></span> <span data-ttu-id="4ea7f-255">DSN может храниться в файле (DSN файла) или в реестре Windows (DSN компьютера).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-255">A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</span></span>

<span data-ttu-id="4ea7f-256">**динамическое свойство**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-256">**dynamic property**</span></span>

<span data-ttu-id="4ea7f-257">Свойство, специфиственное для поставщика данных или службы курсора.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-257">A property specific to a data provider or the cursor service.</span></span> <span data-ttu-id="4ea7f-258">Коллекция **свойств** объекта заполняется этими свойствами автоматически ("динамически").</span><span class="sxs-lookup"><span data-stu-id="4ea7f-258">The **Properties** collection of an object is populated with these automatically ("dynamically").</span></span> <span data-ttu-id="4ea7f-259">У объекта нет динамических свойств, пока он не будет подключен к источнику данных через определенного поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-259">An object has no dynamic properties until it is connected to a data source through a particular data provider.</span></span> <span data-ttu-id="4ea7f-260">См. **также поставщик данных**, **курсор**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-260">See also **data provider**, **cursor**.</span></span>

<span data-ttu-id="4ea7f-261">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-261">Return to top</span></span>

## <a name="e-i"></a><span data-ttu-id="4ea7f-262">E-I</span><span class="sxs-lookup"><span data-stu-id="4ea7f-262">E-I</span></span>

<span data-ttu-id="4ea7f-263">**enumeration**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-263">**enumeration**</span></span>

<span data-ttu-id="4ea7f-264">Список именуемой константы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-264">A list of named constants.</span></span> <span data-ttu-id="4ea7f-265">Enumerated values need not be unique.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-265">Enumerated values need not be unique.</span></span> <span data-ttu-id="4ea7f-266">Однако имя каждого значения должно быть уникальным в пределах области, в которой определено значение.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-266">However the name of each value must be unique within the scope where the enumeration is defined.</span></span> <span data-ttu-id="4ea7f-267">В ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-267">In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</span></span> <span data-ttu-id="4ea7f-268">Например, чтобы открыть статический **набор записей,** используйте **enumerated значение adOpenStatic:**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-268">For example, to open a static **Recordset**, use the **adOpenStatic** enumerated value:</span></span>  
  

<span data-ttu-id="4ea7f-269">Также называется *enumerated constant*.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-269">Also referred to as *enumerated constant*.</span></span> <span data-ttu-id="4ea7f-270">См. также **константы.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-270">See also **constant**.</span></span>

<span data-ttu-id="4ea7f-271">**event**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-271">**event**</span></span>

<span data-ttu-id="4ea7f-272">Действие, распознано объектом, для которого можно написать код для ответа.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-272">An action recognized by an object, for which you can write code to respond.</span></span> <span data-ttu-id="4ea7f-273">События могут быть созданы в результате выполнения команды, завершения транзакций, навигации по набору записей и обновления данных, помимо других действий.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-273">Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</span></span> <span data-ttu-id="4ea7f-274">См. также **обработок событий.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-274">See also **event handler**.</span></span>

<span data-ttu-id="4ea7f-275">**обработчик событий**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-275">**event handler**</span></span>

<span data-ttu-id="4ea7f-276">Обработок события — это код, который выполняется при выполнении события.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-276">An event handler is the code that is executed when an event occurs.</span></span> <span data-ttu-id="4ea7f-277">См. также **событие**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-277">See also **event**.</span></span>

<span data-ttu-id="4ea7f-278">**handler**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-278">**handler**</span></span>

<span data-ttu-id="4ea7f-279">Процедура, управляющая общим и относительно простым условием или операцией, например восстановлением ошибок или управлением данными.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-279">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</span></span>

<span data-ttu-id="4ea7f-280">**hierarchical Recordset**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-280">**hierarchical Recordset**</span></span>

<span data-ttu-id="4ea7f-281">Набор **записей,** содержащий другой **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-281">A **Recordset** that contains another **Recordset**.</span></span> <span data-ttu-id="4ea7f-282">См. также **формирование данных**, **глава**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-282">See also **data shaping**, **chapter**.</span></span>

<span data-ttu-id="4ea7f-283">Дополнительные сведения [см. в подсети "Доступ к строкам в иерархическом наборе записей".](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="4ea7f-283">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)</span></span>

<span data-ttu-id="4ea7f-284">**hierarchy**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-284">**hierarchy**</span></span>

<span data-ttu-id="4ea7f-285">В общем, иерархия — это ранжированные структуры с верхним и подчиненным уровнями.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-285">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</span></span> <span data-ttu-id="4ea7f-286">В ADO иерархические записи используются для представления родительско-родительской связи между записью и главой. </span><span class="sxs-lookup"><span data-stu-id="4ea7f-286">In ADO, hierarchical **Recordsets** are used to represent the parent-child relationship between a record and a chapter.</span></span> <span data-ttu-id="4ea7f-287">Кроме того, в ADO **объекты Record** и **Stream** можно использовать для доступа к иерархическим структурам дерева, таким как папка и документы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-287">Also in ADO, **Record** and **Stream** objects can be used to access hierarchical tree structures such as a folder and documents.</span></span> <span data-ttu-id="4ea7f-288">ADO MD также включает **объекты Иерархии,** которые представляют отношение между уровнями измерения в кубе OLAP.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-288">ADO MD also includes **Hierarchy** objects to represent a relationship between the levels of a dimension in an OLAP cube.</span></span> <span data-ttu-id="4ea7f-289">См. **также иерархические записи,** **родительские и родительские** отношения, **глава,** **дерево.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-289">See also **hierarchical Recordsets**, **parent-child relationship**, **chapter**, **tree**.</span></span>

<span data-ttu-id="4ea7f-290">**ISAPI (интерфейс программирования приложений Internet Server)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-290">**ISAPI (Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="4ea7f-291">Набор функций для интернет-серверов, таких как Windows NT Server/Windows 2000 Server с Microsoft IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-291">A set of functions for Internet servers, such as a Windows NT Server/Windows 2000 Server running Microsoft Internet Information Services (IIS).</span></span>

<span data-ttu-id="4ea7f-292">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-292">Return to top</span></span>

## <a name="k-m"></a><span data-ttu-id="4ea7f-293">K-M</span><span class="sxs-lookup"><span data-stu-id="4ea7f-293">K-M</span></span>

<span data-ttu-id="4ea7f-294">**key**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-294">**key**</span></span>

<span data-ttu-id="4ea7f-295">Столбец или столбцы в таблице, однозначно идентифицируют строку; часто используется для индексации таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-295">A column or columns in a table that uniquely identify a row; often used to index a table.</span></span>

<span data-ttu-id="4ea7f-296">**marshaling**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-296">**marshaling**</span></span>

<span data-ttu-id="4ea7f-297">Процесс упаковки, отправки и распаковки параметров метода интерфейса через границы потока или процесса.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-297">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</span></span>

<span data-ttu-id="4ea7f-298">**средний уровень**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-298">**middle tier**</span></span>

<span data-ttu-id="4ea7f-299">Логический уровень в распределенной системе между пользовательским интерфейсом или веб-клиентом и базой данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-299">The logical layer in a distributed system between a user interface or web client and the database.</span></span> <span data-ttu-id="4ea7f-300">В таких случаях обычно используются бизнес-объекты.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-300">This is typically where business objects are instantiated.</span></span> <span data-ttu-id="4ea7f-301">Средний уровень — это коллекция бизнес-правил и функций, которые создают и работают при получении информации.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-301">The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</span></span> <span data-ttu-id="4ea7f-302">Для этого используются бизнес-правила, которые могут меняться часто и поэтому инкапсулированы в компоненты, физически отделенные от самой логики приложения.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-302">They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</span></span> <span data-ttu-id="4ea7f-303">Также известный как *уровень сервера приложений.*</span><span class="sxs-lookup"><span data-stu-id="4ea7f-303">Also known as *application server tier*.</span></span> <span data-ttu-id="4ea7f-304">См. также **распределенные приложения,** **уровень клиента,** **уровень источника данных.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-304">See also **distributed application**, **client tier**, **data source tier**.</span></span>

<span data-ttu-id="4ea7f-305">**MIME (Multi-purpose Internet Mail Extension)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-305">**MIME (Multi-purpose Internet Mail Extension)**</span></span>

<span data-ttu-id="4ea7f-306">Протокол Интернета, изначально разработанный для обмена электронными сообщениями электронной почты с форматом содержимого в разнородных сетях, на компьютерах и в средах электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-306">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and email environments.</span></span> <span data-ttu-id="4ea7f-307">На практике MIME также был принят и расширен приложениями, не относяжимся к почте.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-307">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

<span data-ttu-id="4ea7f-308">MIME — это стандарт, позволяющий публиковать и считывать двоичные данные в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-308">MIME is a standard that allows binary data to be published and read on the Internet.</span></span> <span data-ttu-id="4ea7f-309">Заглавная папка файла с двоичными данными содержит тип MIME данных; Это сообщает клиентских программам (например, веб-браузерам и почтовым пакетам), что им потребуется обрабатывать данные не так, как при прямом тексте.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-309">The header of a file with binary data contains the MIME type of the data; this informs client programs (web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</span></span> <span data-ttu-id="4ea7f-310">Например, загон веб-документа, содержащего графику JPEG, содержит тип MIME, относящееся к формату файла JPEG.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-310">For example, the header of a web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</span></span> <span data-ttu-id="4ea7f-311">Это позволяет браузеру отобразить файл с помощью просмотра JPEG, если он присутствует.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-311">This allows a browser to display the file with its JPEG viewer, if one is present.</span></span>

<span data-ttu-id="4ea7f-312">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-312">Return to top</span></span>

## <a name="n-o"></a><span data-ttu-id="4ea7f-313">N-O</span><span class="sxs-lookup"><span data-stu-id="4ea7f-313">N-O</span></span>

<span data-ttu-id="4ea7f-314">**node**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-314">**node**</span></span>

<span data-ttu-id="4ea7f-315">Элемент в иерархической структуре дерева.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-315">An element in a hierarchical tree structure.</span></span> <span data-ttu-id="4ea7f-316">Узел может быть корневым или дитя другого узла.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-316">A node may be the root, or the child of another node.</span></span> <span data-ttu-id="4ea7f-317">Узел также может быть родительским для нескольких детей.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-317">A node can also be the parent of multiple children.</span></span> <span data-ttu-id="4ea7f-318">См. **также иерархию,** **дерево,** **корневой,** **родительский,** **родительский.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-318">See also **hierarchy**, **tree**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="4ea7f-319">**переменная объекта**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-319">**object variable**</span></span>

<span data-ttu-id="4ea7f-320">Переменная, которая содержит ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-320">A variable that contains a reference to an object.</span></span> <span data-ttu-id="4ea7f-321">Например, objCustomObject — это переменная, которая указывает на объект типа CustomObject:</span><span class="sxs-lookup"><span data-stu-id="4ea7f-321">For example, objCustomObject is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="4ea7f-322">— переменная, которая указывает на объект типа CustomObject:</span><span class="sxs-lookup"><span data-stu-id="4ea7f-322">is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="4ea7f-323">Set objCustomObject = CreateObject(adodb. Recordset)</span><span class="sxs-lookup"><span data-stu-id="4ea7f-323">Set objCustomObject = CreateObject(adodb.Recordset)</span></span>

<span data-ttu-id="4ea7f-324">**ODBC (Open Database Connectivity)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-324">**ODBC (Open Database Connectivity)**</span></span>

<span data-ttu-id="4ea7f-325">Стандартный интерфейс языка программирования, используемый для подключения к различным источникам данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-325">A standard programming language interface used to connect to a variety of data sources.</span></span> <span data-ttu-id="4ea7f-326">Обычно доступ к этой функции можно получить с помощью панели управления, где имена источников данных (DSNs) могут быть назначены для использования определенных драйверов ODBC.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-326">This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</span></span>

<span data-ttu-id="4ea7f-327">**OLE DB**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-327">**OLE DB**</span></span>

<span data-ttu-id="4ea7f-328">Набор интерфейсов, которые выставляют данные из различных источников с помощью COM.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-328">A set of interfaces that expose data from a variety of sources using COM.</span></span> <span data-ttu-id="4ea7f-329">Интерфейсы OLE DB предоставляют приложениям единый доступ к данным, хранимым в различных источниках информации.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-329">OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</span></span> <span data-ttu-id="4ea7f-330">Эти интерфейсы поддерживают функциональные возможности DBMS, соответствующие источнику данных, позволяя им обмениваться данными.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-330">These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</span></span> <span data-ttu-id="4ea7f-331">См. также **COM.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-331">See also **COM**.</span></span>

<span data-ttu-id="4ea7f-332">**оптимистическая блокировка**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-332">**optimistic locking**</span></span>

<span data-ttu-id="4ea7f-333">Тип блокировки, в котором страница данных, содержащая одну или несколько записей, в том числе редактируемую, недоступна другим пользователям только во время обновления записи с помощью метода **Update,** но доступна до и после вызова **update.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-333">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the **Update** method, but is available before and after the call to **Update**.</span></span>

<span data-ttu-id="4ea7f-334">Оптимистичная блокировка используется, когда объект **Recordset** открывается с параметром **LockType** или свойством **adLockOptimistic** или **adLockBatchOptimistic.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-334">Optimistic locking is used when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockOptimistic** or **adLockBatchOptimistic**.</span></span> <span data-ttu-id="4ea7f-335">См. **также пессимистическую блокировку.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-335">See also **pessimistic locking**.</span></span>

<span data-ttu-id="4ea7f-336">**порядковая величина**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-336">**ordinal value**</span></span>

<span data-ttu-id="4ea7f-337">Числовое расположение элемента в заказе.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-337">The numeric location of an item within an order.</span></span> <span data-ttu-id="4ea7f-338">В коллекции ADO порядковая величина первого элемента — ноль (0).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-338">In an ADO collection, the ordinal value of the first item is zero (0).</span></span> <span data-ttu-id="4ea7f-339">Следующий элемент — один (1) и так далее.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-339">The next item is one (1), and so on.</span></span>

<span data-ttu-id="4ea7f-340">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-340">Return to top</span></span>

## <a name="p"></a><span data-ttu-id="4ea7f-341">P</span><span class="sxs-lookup"><span data-stu-id="4ea7f-341">P</span></span>

<span data-ttu-id="4ea7f-342">**параметризованная команда**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-342">**parameterized command**</span></span>

<span data-ttu-id="4ea7f-343">Запрос или команда, которая позволяет установить значения параметров перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-343">A query or command that allows you to set parameter values before the command is executed.</span></span> <span data-ttu-id="4ea7f-344">Например, строку SQL можно задать с помощью встраив маркеры параметров в строку SQL (обозначенную символом "?").</span><span class="sxs-lookup"><span data-stu-id="4ea7f-344">For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</span></span> <span data-ttu-id="4ea7f-345">Затем приложение указывает значения для каждого параметра и выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-345">The application then specifies values for each parameter and executes the command.</span></span>

<span data-ttu-id="4ea7f-346">**родитель**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-346">**parent**</span></span>

<span data-ttu-id="4ea7f-347">Контрольная сторона иерархической связи.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-347">The controlling side of a hierarchical relationship.</span></span> <span data-ttu-id="4ea7f-348">В иерархической структуре родительский узел имеет один или несколько непосредственных узлов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-348">In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</span></span> <span data-ttu-id="4ea7f-349">См. **также псевдоним "родитель-псевдоним",** **"родительский-родительский",** **"child".**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-349">See also **parent-alias**, **parent-child relationship**, **child**.</span></span>

<span data-ttu-id="4ea7f-350">**parent-alias**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-350">**parent-alias**</span></span>

<span data-ttu-id="4ea7f-351">Псевдоним, который ссылается на родительский.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-351">An alias that refers to the parent.</span></span> <span data-ttu-id="4ea7f-352">См. **также псевдоним**, **родительский**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-352">See also **alias**, **parent**.</span></span>

<span data-ttu-id="4ea7f-353">**связь "родительский-родительский"**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-353">**parent-child relationship**</span></span>

<span data-ttu-id="4ea7f-354">Связь в иерархической структуре, в которой родительский уровень выше на один уровень и напрямую связан с одним или более потомком.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-354">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</span></span> <span data-ttu-id="4ea7f-355">Потомок на один уровень ниже и должен иметь один родительский уровень.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-355">A child is one level lower and must have one parent.</span></span> <span data-ttu-id="4ea7f-356">См. также **родительский**, **родительский**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-356">See also **parent**, **child**.</span></span>

<span data-ttu-id="4ea7f-357">**persist**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-357">**persist**</span></span>

<span data-ttu-id="4ea7f-358">Сохранение данных в постоянном состоянии, например сохранение **наборов записей** в файл.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-358">To save data in a permanent state, such as saving a **Recordset** to a file.</span></span>

<span data-ttu-id="4ea7f-359">**пессимистическая блокировка**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-359">**pessimistic locking**</span></span>

<span data-ttu-id="4ea7f-360">Тип блокировки, в которой страница, содержащая одну или несколько записей, в том числе редактируемую, недоступна другим пользователям для обновления.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-360">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</span></span> <span data-ttu-id="4ea7f-361">Пессимистическое поведение блокировки определяется поставщиком OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-361">Pessimistic locking behavior is defined by the OLE DB provider.</span></span> <span data-ttu-id="4ea7f-362">Как правило, записи блокированы при редактировании и остаются недоступными до завершения работы метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-362">Typically, records are locked upon editing and remain unavailable until the **Update** method has completed.</span></span>

<span data-ttu-id="4ea7f-363">Пессимистическая блокировка включена, когда объект **Recordset** открывается с помощью параметра **LockType** или свойства **adLockPessimistic.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-363">Pessimistic locking is enabled when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockPessimistic**.</span></span> <span data-ttu-id="4ea7f-364">См. также **оптимистичную блокировку.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-364">See also **optimistic locking**.</span></span>

<span data-ttu-id="4ea7f-365">**pooling**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-365">**pooling**</span></span>

<span data-ttu-id="4ea7f-366">Оптимизация производительности на основе использования коллекций предварительно выделенных ресурсов, таких как объекты или подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-366">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</span></span> <span data-ttu-id="4ea7f-367">Эффективнее отрисовка существующего ресурса из пула, чем создание нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-367">It is more efficient to draw an existing resource from the pool than to create a new resource.</span></span>

<span data-ttu-id="4ea7f-368">**ProgID (программный идентификатор)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-368">**ProgID (programmatic identifier)**</span></span>

<span data-ttu-id="4ea7f-369">Уникальное имя, которое приложение COM соедино реестру Windows.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-369">A unique name mapped to the Windows registry by a COM application.</span></span> <span data-ttu-id="4ea7f-370">ProgID для подключения ADO — "ADODB. Подключение".</span><span class="sxs-lookup"><span data-stu-id="4ea7f-370">The ProgID for an ADO Connection is "ADODB.Connection".</span></span> <span data-ttu-id="4ea7f-371">См. также **CLSID,** **COM.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-371">See also **CLSID**, **COM**.</span></span>

<span data-ttu-id="4ea7f-372">**proxy**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-372">**proxy**</span></span>

<span data-ttu-id="4ea7f-373">Объект для определенного интерфейса, который обеспечивает маршалинг параметров и связь, необходимые клиенту для вызова объекта приложения, запущенного в другой среде выполнения, например в другом потоке или другом процессе.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-373">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="4ea7f-374">Прокси-сервер находится с клиентом и взаимодействует с соответствующей загона, которая расположена с объектом приложения, который будет вызван.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-374">The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</span></span> <span data-ttu-id="4ea7f-375">См. также **загона.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-375">See also **stub**.</span></span>

<span data-ttu-id="4ea7f-376">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-376">Return to top</span></span>

## <a name="r"></a><span data-ttu-id="4ea7f-377">R</span><span class="sxs-lookup"><span data-stu-id="4ea7f-377">R</span></span>

<span data-ttu-id="4ea7f-378">**относительный URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-378">**relative URL**</span></span>

<span data-ttu-id="4ea7f-379">Частично соответствующий URL-адрес, который указывает ресурс в Интернете или интрасети, расположение которого относительно начальной точки, указанной абсолютным URL-адресом или эквивалентным объектом подключения ADO.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-379">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</span></span> <span data-ttu-id="4ea7f-380">По сути, совмещенные абсолютные и относительные URL-адреса являются полными URL-адресами.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-380">In effect, the concatenated absolute and relative URLs consitute a complete URL.</span></span> <span data-ttu-id="4ea7f-381">См. также **URL-адрес** **и абсолютный URL-адрес.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-381">See also **URL** and **absolute URL**.</span></span>

<span data-ttu-id="4ea7f-382">**удаленный источник данных**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-382">**remote data source**</span></span>

<span data-ttu-id="4ea7f-383">Источник данных, который существует на другом компьютере, а не в локальной системе (где выполняется клиентские приложения).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-383">A data source that exists on a another computer, rather than on the local system (where the client application runs).</span></span>

<span data-ttu-id="4ea7f-384">**запись ресурса**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-384">**resource record**</span></span>

<span data-ttu-id="4ea7f-385">Запись от поставщика источника документов, которая содержит поля для определения и описания папки или документа.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-385">A record from a document source provider that contains fields for the definition and description of a folder or document.</span></span> <span data-ttu-id="4ea7f-386">Сам документ не содержится в записи ресурса, но обычно к нему можно получить доступ с помощью потока по умолчанию или поля в записи ресурса, содержащей URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-386">The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</span></span> <span data-ttu-id="4ea7f-387">См. также **поставщик источника документов,** **поток по умолчанию,** **URL-адрес.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-387">See also **document source provider**, **default stream**, **URL**.</span></span>

<span data-ttu-id="4ea7f-388">**root**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-388">**root**</span></span>

<span data-ttu-id="4ea7f-389">Верхний уровень иерархической структуры дерева.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-389">The top level in a hierarchical tree structure.</span></span> <span data-ttu-id="4ea7f-390">Корневой узел не имеет родительских узлов, но может иметь детей.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-390">The root node has no parents, but may have children.</span></span> <span data-ttu-id="4ea7f-391">См. **также иерархию,** **дерево,** **родительский**, **child**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-391">See also **hierarchy**, **tree**, **parent**, **child**.</span></span>

<span data-ttu-id="4ea7f-392">**rowset**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-392">**rowset**</span></span>

<span data-ttu-id="4ea7f-393">Набор строк из источника данных с одинаковой схемой поля.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-393">A set of rows from a data source, all having the same field schema.</span></span> <span data-ttu-id="4ea7f-394">Набор строк может представлять все или некоторые поля из таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-394">A rowset can represent all or some fields from a table.</span></span> <span data-ttu-id="4ea7f-395">Набор строк также может представлять виртуальную таблицу, созданную запросом или присоединив две или более таблиц.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-395">A rowset can also represent a virtual table, created by a query or a join of two or more tables.</span></span> <span data-ttu-id="4ea7f-396">В ADO наборы строк представлены **объектами Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-396">In ADO, rowsets are represented by **Recordset** objects.</span></span>

<span data-ttu-id="4ea7f-397">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-397">Return to top</span></span>

## <a name="s"></a><span data-ttu-id="4ea7f-398">S</span><span class="sxs-lookup"><span data-stu-id="4ea7f-398">S</span></span>

<span data-ttu-id="4ea7f-399">**schema**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-399">**schema**</span></span>

<span data-ttu-id="4ea7f-400">Описание базы данных в системе управления базами данных (DBMS), которое обычно создается с использованием языка определения данных, предоставляемого DBMS.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-400">A description of a database to the database management system (DBMS), typically generated using the data definition language provided by the DBMS.</span></span> <span data-ttu-id="4ea7f-401">Схема определяет атрибуты базы данных, такие как таблицы, столбцы и свойства.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-401">A schema defines attributes of the database, such as tables, columns, and properties.</span></span>

<span data-ttu-id="4ea7f-402">**scope**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-402">**scope**</span></span>

<span data-ttu-id="4ea7f-403">Диапазон ссылок для объекта или переменной или диапазона записей в представлении или таблице.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-403">The range of reference for an object or variable or a range of records in a view or table.</span></span> <span data-ttu-id="4ea7f-404">Например, на локальные переменные можно ссылаться только в рамках процедуры, в которой они были определены.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-404">For example, local variables can be referenced only within the procedure in which they were defined.</span></span> <span data-ttu-id="4ea7f-405">Общедоступные переменные доступны из любого места приложения.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-405">Public variables are accessible from anywhere in the application.</span></span> <span data-ttu-id="4ea7f-406">Объекты, например текущая база данных, находятся в области, если они находятся в определенном пути поиска.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-406">Objects, such as the current database, are in scope if they are in the defined search path.</span></span> <span data-ttu-id="4ea7f-407">Диапазоны записей могут быть заданы с помощью предложения Scope во многих командах.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-407">Record ranges can be specified with a Scope clause in many commands.</span></span>

<span data-ttu-id="4ea7f-408">**поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-408">**service provider**</span></span>

<span data-ttu-id="4ea7f-409">Программное обеспечение, которое инкапсулирует службу, выдав и потребляя данные, дополнив функции в приложениях ADO.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-409">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="4ea7f-410">Это поставщик, который не предоставляет данные напрямую, а предоставляет службу, например обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-410">It is a provider that does not directly expose data, rather it provides a service, such as query processing.</span></span> <span data-ttu-id="4ea7f-411">Поставщик услуг может обрабатывать данные, предоставленные поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-411">The service provider may process data provided by a data provider.</span></span> <span data-ttu-id="4ea7f-412">См. также **поставщик данных.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-412">See also **data provider**.</span></span>

<span data-ttu-id="4ea7f-413">**shaped Recordset**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-413">**shaped Recordset**</span></span>

<span data-ttu-id="4ea7f-414">Набор **записей,** столбцы которого были специально определены как содержащие не только данные, но и ссылки (называемые главами) на другие объекты **Recordset** и/или вычисленные значения на основе других объектов **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-414">A **Recordset** whose columns have been specifically defined to contain not just data, but also references (called chapters) to other **Recordset** objects and/or computed values based on other **Recordset** objects.</span></span>

<span data-ttu-id="4ea7f-415">**sibling**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-415">**sibling**</span></span>

<span data-ttu-id="4ea7f-416">Любые два или более узлов в иерархической структуре, которые находятся на одном уровне иерархии.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-416">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</span></span> <span data-ttu-id="4ea7f-417">Корневой узел в иерархии не имеет ни одного уровня.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-417">The root node in a hierarchy has no siblings.</span></span>

<span data-ttu-id="4ea7f-418">**хранимая процедура**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-418">**stored procedure**</span></span>

<span data-ttu-id="4ea7f-419">Предварительно компилировать коллекцию кода, например SQL и необязательные утверждения управления потоком, хранимые под именем и обрабатываемых как единица.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-419">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</span></span> <span data-ttu-id="4ea7f-420">Хранимые процедуры хранятся в базе данных; их можно выполнять одним вызовом из приложения и разрешить объявленные пользователем переменные, условное выполнение и другие мощные функции программирования.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-420">Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</span></span>

<span data-ttu-id="4ea7f-421">**stub**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-421">**stub**</span></span>

<span data-ttu-id="4ea7f-422">Объект для определенного интерфейса, который обеспечивает маршалинг параметров и связь, необходимые объекту приложения для получения вызовов от клиента, запущенного в другой среде выполнения, например в другом потоке или другом процессе.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-422">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="4ea7f-423">Загона расположена с объектом приложения и взаимодействует с соответствующим прокси-сервером, который находится с клиентом, который его вызывает.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-423">The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</span></span> <span data-ttu-id="4ea7f-424">См. также **прокси-сервер.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-424">See also **proxy**.</span></span>

<span data-ttu-id="4ea7f-425">**sub-node**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-425">**sub-node**</span></span>

<span data-ttu-id="4ea7f-426">См. **child**.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-426">See **child**.</span></span>

<span data-ttu-id="4ea7f-427">**синхронная операция**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-427">**synchronous operation**</span></span>

<span data-ttu-id="4ea7f-428">Операция, инициированная кодом, которая завершается до запуска следующей операции.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-428">An operation initiated by code that completes before the next operation may start.</span></span> <span data-ttu-id="4ea7f-429">См. также **асинхронную операцию.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-429">See also **asynchronous operation**.</span></span>

<span data-ttu-id="4ea7f-430">В начало</span><span class="sxs-lookup"><span data-stu-id="4ea7f-430">Return to top</span></span>

## <a name="t-w"></a><span data-ttu-id="4ea7f-431">T-W</span><span class="sxs-lookup"><span data-stu-id="4ea7f-431">T-W</span></span>

<span data-ttu-id="4ea7f-432">**tree**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-432">**tree**</span></span>

<span data-ttu-id="4ea7f-433">Структура, представляющая иерархическую связь между элементами (узлами).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-433">A structure representing a hierarchical relationship between elements (nodes).</span></span> <span data-ttu-id="4ea7f-434">На верхнем уровне дерева (корневой) имеется один узел.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-434">There is one node at the top level of a tree (the root).</span></span> <span data-ttu-id="4ea7f-435">Под корнем может быть несколько детей.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-435">Underneath the root, there can be multiple children.</span></span> <span data-ttu-id="4ea7f-436">Каждый из них, в свою очередь, может быть родительским для других детей, поэтому ветвяется как дерево.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-436">Each child may in turn be the parent of other children, thus branching like a tree.</span></span> <span data-ttu-id="4ea7f-437">Папка, содержащая документы и другие папки, является типичным примером структуры дерева.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-437">A folder containing documents and other folders is a typical example of a tree structure.</span></span> <span data-ttu-id="4ea7f-438">См. **также иерархию,** **узел,** **корневой,** **родительский,** **родительский.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-438">See also **hierarchy**, **node**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="4ea7f-439">**URL-адрес (Унифицированный поиск ресурсов)**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-439">**URL (Uniform Resource Locator)**</span></span>

<span data-ttu-id="4ea7f-440">Указывает расположение ресурса, расположенного в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-440">Specifies the location of a resource residing on the Internet or an intranet.</span></span> <span data-ttu-id="4ea7f-441">Полный URL-адрес состоит из схемы (например, FTP, HTTP, mailto, file и так далее), двоеточия, имени сервера и полного пути к ресурсу (например, документу, графике или другому файлу).</span><span class="sxs-lookup"><span data-stu-id="4ea7f-441">A complete URL consists of a scheme (such as FTP, HTTP, mailto, file, and so on), followed by a colon, a server name, and the full path of a resource (such as a document, graphic, or other file).</span></span> <span data-ttu-id="4ea7f-442">Вот несколько примеров URL-адресов:</span><span class="sxs-lookup"><span data-stu-id="4ea7f-442">Some examples of URLs are:</span></span>  
  
- https://www.domain.com/default.html  
- <span data-ttu-id="4ea7f-443">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="4ea7f-443">ftp://ftp.server.somewhere/ftp.file</span></span>  
  
- <span data-ttu-id="4ea7f-444">ftp://ftp.server.somewhere/ftp.file</span><span class="sxs-lookup"><span data-stu-id="4ea7f-444">ftp://ftp.server.somewhere/ftp.file</span></span>  
- <span data-ttu-id="4ea7f-445">file://Server/Share/File.doc</span><span class="sxs-lookup"><span data-stu-id="4ea7f-445">file://Server/Share/File.doc</span></span>

<span data-ttu-id="4ea7f-446">См. также **абсолютный URL-адрес** **и относительный URL-адрес.**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-446">See also **absolute URL** and **relative URL**.</span></span>

<span data-ttu-id="4ea7f-447">**веб-сервер**</span><span class="sxs-lookup"><span data-stu-id="4ea7f-447">**web server**</span></span>

<span data-ttu-id="4ea7f-448">Компьютер, который предоставляет веб-службы и страницы пользователям интрасети и Интернета.</span><span class="sxs-lookup"><span data-stu-id="4ea7f-448">A computer that provides web services and pages to intranet and Internet users.</span></span>



