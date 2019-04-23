---
title: Глоссарий объектов данных ActiveX (ADO)
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
# <a name="ado-glossary"></a><span data-ttu-id="5ed40-102">Глоссарий ADO</span><span class="sxs-lookup"><span data-stu-id="5ed40-102">ADO glossary</span></span>

<span data-ttu-id="5ed40-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ed40-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="a"></a><span data-ttu-id="5ed40-104">A</span><span class="sxs-lookup"><span data-stu-id="5ed40-104">A</span></span>

<span data-ttu-id="5ed40-105">**абсолютный URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="5ed40-105">**absolute URL**</span></span>

<span data-ttu-id="5ed40-106">Полный URL-адрес, указывающий расположение ресурса, находящегося в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="5ed40-106">A fully qualified URL that specifies the location of a resource that resides on the Internet or an intranet.</span></span> <span data-ttu-id="5ed40-107">См. также **URL-адрес** и отНОСИТЕЛЬНЫЙ **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-107">See also **URL** and **relative URL**.</span></span>

<span data-ttu-id="5ed40-108">**Элемент ActiveX**</span><span class="sxs-lookup"><span data-stu-id="5ed40-108">**ActiveX control**</span></span>

<span data-ttu-id="5ed40-109">Внутрипроцессный компонент COM, который часто содержит визуальный элемент во время конструирования или выполнения.</span><span class="sxs-lookup"><span data-stu-id="5ed40-109">Self-registering, in-process COM component that often has a visual element either at design time or run time.</span></span> <span data-ttu-id="5ed40-110">Элементы управления ActiveX также могут связываться с контейнером активного документа, таким как Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5ed40-110">ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</span></span>

<span data-ttu-id="5ed40-111">**АДИСАПИ (Расширенный интерфейсный интерфейс Интернет-серверных приложений)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="5ed40-112">Библиотека ISAPI ISAPI, обеспечивающая синтаксический анализ, управление автоматизацией, маршалинг **наборов записей** и упаковку MIME.</span><span class="sxs-lookup"><span data-stu-id="5ed40-112">An ISAPI DLL that provides parsing, Automation control, **Recordset** marshaling, and MIME packaging.</span></span> <span data-ttu-id="5ed40-113">Компонент АДИСАПИ работает через API, предоставляемый службами IIS.</span><span class="sxs-lookup"><span data-stu-id="5ed40-113">The ADISAPI component works through the API provided by Internet Information Services (IIS).</span></span> <span data-ttu-id="5ed40-114">См. также **ISAPI**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-114">See also **ISAPI**.</span></span>

<span data-ttu-id="5ed40-115">**агрегатная функция**</span><span class="sxs-lookup"><span data-stu-id="5ed40-115">**aggregate function**</span></span>

<span data-ttu-id="5ed40-116">В запросе это функция, такая как COUNT, AVG или STDEV, которая вычисляет значение с помощью всех строк в столбце таблицы.</span><span class="sxs-lookup"><span data-stu-id="5ed40-116">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table.</span></span> <span data-ttu-id="5ed40-117">При написании выражений и программировании можно использовать статистические функции SQL (в том числе три приведенные выше) и статистические функции по подмножеству для определения различных статистических показателей.</span><span class="sxs-lookup"><span data-stu-id="5ed40-117">In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</span></span>

<span data-ttu-id="5ed40-118">**alias**</span><span class="sxs-lookup"><span data-stu-id="5ed40-118">**alias**</span></span>

<span data-ttu-id="5ed40-119">Альтернативное имя, которое вы предоставляете столбцу или выражению в операторе SQL SELECT, часто короче или более осмысленно.</span><span class="sxs-lookup"><span data-stu-id="5ed40-119">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful.</span></span> <span data-ttu-id="5ed40-120">Например, Бобсалес является псевдонимом в следующей инструкции SELECT: "Select ВР-Sales AS Бобсалес from Салесдб".</span><span class="sxs-lookup"><span data-stu-id="5ed40-120">For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB".</span></span> <span data-ttu-id="5ed40-121">Псевдоним можно использовать для динамического назначения столбцов привязкам элементов управления в объекте DataObject. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5ed40-121">An alias can be used to dynamically assign columns to control bindings on the **DataControl** object.</span></span>

<span data-ttu-id="5ed40-122">**потоковое подразделение**</span><span class="sxs-lookup"><span data-stu-id="5ed40-122">**apartment threading**</span></span>

<span data-ttu-id="5ed40-123">Потоковая модель COM, в которой все вызовы объекта выполняются в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="5ed40-123">A COM threading model where all calls to an object occur on one thread.</span></span> <span data-ttu-id="5ed40-124">В потоковом подразделении COM выполняет синхронизацию и маршалирование вызовов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-124">In apartment threading, COM synchronizes and marshals calls.</span></span> <span data-ttu-id="5ed40-125">См. также **com**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-125">See also **COM**.</span></span>

<span data-ttu-id="5ed40-126">**асинхронная операция**</span><span class="sxs-lookup"><span data-stu-id="5ed40-126">**asynchronous operation**</span></span>

<span data-ttu-id="5ed40-127">Операция, которая возвращает управление вызывающей программе, не дожидаясь завершения операции.</span><span class="sxs-lookup"><span data-stu-id="5ed40-127">An operation that returns control to the calling program without waiting for the operation to complete.</span></span> <span data-ttu-id="5ed40-128">До завершения операции выполнение кода продолжается.</span><span class="sxs-lookup"><span data-stu-id="5ed40-128">Before the operation is complete, code execution continues.</span></span> <span data-ttu-id="5ed40-129">См. также **синхронные операции**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-129">See also **synchronous operation**.</span></span>

<span data-ttu-id="5ed40-130">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-130">Return to top</span></span>

## <a name="b"></a><span data-ttu-id="5ed40-131">B</span><span class="sxs-lookup"><span data-stu-id="5ed40-131">B</span></span>

<span data-ttu-id="5ed40-132">**запись привязки**</span><span class="sxs-lookup"><span data-stu-id="5ed40-132">**binding entry**</span></span>

<span data-ttu-id="5ed40-133">Сопоставление между полем в таблице и переменной.</span><span class="sxs-lookup"><span data-stu-id="5ed40-133">A mapping between a field in a table and a variable.</span></span> <span data-ttu-id="5ed40-134">В расширениях ADO для Visual C++ поля **набора записей** сопоставляются с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="5ed40-134">In the ADO Visual C++ extensions, **Recordset** fields are mapped to C/C++ variables.</span></span>

<span data-ttu-id="5ed40-135">**маски**</span><span class="sxs-lookup"><span data-stu-id="5ed40-135">**bitmask**</span></span>

<span data-ttu-id="5ed40-136">Числовое значение, предназначенное для сравнения поразрядных значений с другими числовыми значениями, обычно для отметки параметров в параметрах или возвращаемых значениях.</span><span class="sxs-lookup"><span data-stu-id="5ed40-136">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</span></span> <span data-ttu-id="5ed40-137">Обычно это сравнение выполняется с поразрядными логическими операторами, такими как **и** и или в **&** Visual **|** Basic, а **также** в C++.</span><span class="sxs-lookup"><span data-stu-id="5ed40-137">Usually this comparison is done with bitwise logical operators, such as **And** and **Or** in Visual Basic, **&** and **|** in C++.</span></span>

<span data-ttu-id="5ed40-138">Например, значения ADO **фиелдаттрибутинум** можно использовать в качестве масок для определения атрибутов поля.</span><span class="sxs-lookup"><span data-stu-id="5ed40-138">For example, the ADO **FieldAttributeEnum** values can be used as bitmasks to determine the attributes of a field.</span></span> <span data-ttu-id="5ed40-139">Предположим, вы решили определить, было ли поле обновляемым.</span><span class="sxs-lookup"><span data-stu-id="5ed40-139">Suppose you wanted to determine if a field was updateable.</span></span> <span data-ttu-id="5ed40-140">Это можно проверить с помощью следующего выражения в Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5ed40-140">You could test for this with the following expression in Visual Basic:</span></span>  
  

<span data-ttu-id="5ed40-141">Если результат имеет значение TRUE, то поле доступно для обновления.</span><span class="sxs-lookup"><span data-stu-id="5ed40-141">If the result is TRUE, then the field is updateable.</span></span>

<span data-ttu-id="5ed40-142">**bookmark**</span><span class="sxs-lookup"><span data-stu-id="5ed40-142">**bookmark**</span></span>

<span data-ttu-id="5ed40-143">Маркер, однозначно определяющий строку в наборе строк, чтобы пользователь мог быстро перейти к ней.</span><span class="sxs-lookup"><span data-stu-id="5ed40-143">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</span></span>

<span data-ttu-id="5ed40-144">**бизнес-объект**</span><span class="sxs-lookup"><span data-stu-id="5ed40-144">**business object**</span></span>

<span data-ttu-id="5ed40-145">Объект, который выполняет определенный набор операций, например проверку данных или логику бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="5ed40-145">An object that performs a defined set of operations, such as data validation or business rule logic.</span></span> <span data-ttu-id="5ed40-146">Бизнес-объекты обычно размещаются на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="5ed40-146">Business objects usually reside on the middle tier.</span></span>

<span data-ttu-id="5ed40-147">**Бизнес-правило**</span><span class="sxs-lookup"><span data-stu-id="5ed40-147">**business rule**</span></span>

<span data-ttu-id="5ed40-148">Сочетание изменений проверки, проверки входа, поиска в базе данных, политик и алгоритмов преобразования, которые представляют собой способ ведения бизнеса в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="5ed40-148">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</span></span> <span data-ttu-id="5ed40-149">Также называется *бизнес-логикой*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-149">Also known as *business logic*.</span></span>

<span data-ttu-id="5ed40-150">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-150">Return to top</span></span>

## <a name="c"></a><span data-ttu-id="5ed40-151">C</span><span class="sxs-lookup"><span data-stu-id="5ed40-151">C</span></span>

<span data-ttu-id="5ed40-152">**Вычисляемое выражение**</span><span class="sxs-lookup"><span data-stu-id="5ed40-152">**calculated expression**</span></span>

<span data-ttu-id="5ed40-153">Неконстантное выражение, значение которого зависит от других значений.</span><span class="sxs-lookup"><span data-stu-id="5ed40-153">An expression that is not constant, but whose value depends upon other values.</span></span> <span data-ttu-id="5ed40-154">Вычисляемое выражение должно получать и считывать значения из других источников, как правило, в других полях или строках.</span><span class="sxs-lookup"><span data-stu-id="5ed40-154">To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</span></span>

<span data-ttu-id="5ed40-155">**части**</span><span class="sxs-lookup"><span data-stu-id="5ed40-155">**chapter**</span></span>

<span data-ttu-id="5ed40-156">Ссылка на диапазон строк из источника данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-156">A reference to a range of rows from a data source.</span></span> <span data-ttu-id="5ed40-157">В ADO глава, как правило, представляет собой ссылку на другой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-157">In ADO, a chapter is typically a reference to another **Recordset**.</span></span>

<span data-ttu-id="5ed40-158">В столбцах главы можно определить связь типа " *родители-потомки* ", в которой *родитель* — это объект **Recordset** , содержащий столбец Chapter, а дочерний элемент — это **набор записей** , представленный главой. \*\*</span><span class="sxs-lookup"><span data-stu-id="5ed40-158">Chapter columns make it possible to define a *parent-child* relationship where the *parent* is the **Recordset** containing the chapter column and the *child* is the **Recordset** represented by the chapter.</span></span>

<span data-ttu-id="5ed40-159">**Глава — псевдоним**</span><span class="sxs-lookup"><span data-stu-id="5ed40-159">**chapter-alias**</span></span>

<span data-ttu-id="5ed40-160">Псевдоним, ссылающийся на столбец, добавленный к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="5ed40-160">An alias that refers to the column appended to the parent.</span></span>

<span data-ttu-id="5ed40-161">**кодировка**</span><span class="sxs-lookup"><span data-stu-id="5ed40-161">**character set**</span></span>

<span data-ttu-id="5ed40-162">Сопоставление набора символов с их числовыми значениями.</span><span class="sxs-lookup"><span data-stu-id="5ed40-162">A mapping of a set of characters to their numeric values.</span></span> <span data-ttu-id="5ed40-163">Например, Юникод — это 16-разрядный набор символов, поддерживающий кодирование всех известных символов и используемый в качестве стандарта кодировки символов мира.</span><span class="sxs-lookup"><span data-stu-id="5ed40-163">For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</span></span>

<span data-ttu-id="5ed40-164">**ребенка**</span><span class="sxs-lookup"><span data-stu-id="5ed40-164">**child**</span></span>

<span data-ttu-id="5ed40-165">Зависимая сторона иерархической связи.</span><span class="sxs-lookup"><span data-stu-id="5ed40-165">The dependent side of a hierarchical relationship.</span></span> <span data-ttu-id="5ed40-166">Дочерний элемент — это узел в иерархической структуре, имеющий другой узел над ним (ближе к корню).</span><span class="sxs-lookup"><span data-stu-id="5ed40-166">A child is a node in a hierarchical structure that has another node above it (closer to the root).</span></span> <span data-ttu-id="5ed40-167">Также **: дочерний псевдоним**, **связь "родитель — потомок**", "родитель". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5ed40-167">See also **child-alias**, **parent-child relationship**, **parent**.</span></span>

<span data-ttu-id="5ed40-168">**дочерний псевдоним**</span><span class="sxs-lookup"><span data-stu-id="5ed40-168">**child-alias**</span></span>

<span data-ttu-id="5ed40-169">Псевдоним, который относится к дочернему элементу.</span><span class="sxs-lookup"><span data-stu-id="5ed40-169">An alias that refers to the child.</span></span> <span data-ttu-id="5ed40-170">Кроме того, можно просмотреть **псевдоним**, дочерний **элемент**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-170">See also **alias**, **child**.</span></span>

<span data-ttu-id="5ed40-171">**CLSID (идентификатор класса)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-171">**CLSID (class identifier)**</span></span>

<span data-ttu-id="5ed40-172">Универсальный уникальный идентификатор (UUID), определяющий COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="5ed40-172">A universally unique identifier (UUID) that identifies a COM component.</span></span> <span data-ttu-id="5ed40-173">Каждый компонент COM имеет свой идентификатор CLSID в реестре Windows, чтобы его можно было загрузить из других приложений.</span><span class="sxs-lookup"><span data-stu-id="5ed40-173">Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications.</span></span> <span data-ttu-id="5ed40-174">См. также **ProgID**, **com**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-174">See also **ProgID**, **COM**.</span></span>

<span data-ttu-id="5ed40-175">**клиентский уровень**</span><span class="sxs-lookup"><span data-stu-id="5ed40-175">**client tier**</span></span>

<span data-ttu-id="5ed40-176">Логический уровень распределенной системы, который обычно представляет данные для и обрабатывает входные данные пользователя, иногда называемые *интерфейсным сервером*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-176">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the *front end*.</span></span> <span data-ttu-id="5ed40-177">Как правило, клиентский уровень запрашивает данные с сервера на основе входных данных, а затем форматирует и отображает результат.</span><span class="sxs-lookup"><span data-stu-id="5ed40-177">Usually, the client tier requests data from a server based on input, and then formats and displays the result.</span></span> <span data-ttu-id="5ed40-178">См. также **средний уровень**, **уровень источника данных**, **распределенное приложение**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-178">See also **middle tier**, **data source tier**, **distributed application**.</span></span>

<span data-ttu-id="5ed40-179">**COM (объектная модель компонента)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-179">**COM (Component Object Model)**</span></span>

<span data-ttu-id="5ed40-180">Двоичный стандарт, который позволяет объектам взаимодействовать в сетевой среде независимо от того, на каком языке они разрабатывались или на каких компьютерах они находятся.</span><span class="sxs-lookup"><span data-stu-id="5ed40-180">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside.</span></span> <span data-ttu-id="5ed40-181">Технологии на основе COM включают элементы управления ActiveX, автоматизацию, а также связывание и внедрение объектов (OLE).</span><span class="sxs-lookup"><span data-stu-id="5ed40-181">COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE).</span></span> <span data-ttu-id="5ed40-182">COM позволяет объекту предоставлять свои функциональные возможности другим компонентам и размещать приложения.</span><span class="sxs-lookup"><span data-stu-id="5ed40-182">COM allows an object to expose its functionality to other components and to host applications.</span></span> <span data-ttu-id="5ed40-183">Он определяет как объект представляет себя, так и то, как эта экспозиция работает в процессах и в сетях.</span><span class="sxs-lookup"><span data-stu-id="5ed40-183">It defines both how the object exposes itself and how this exposure works across processes and across networks.</span></span> <span data-ttu-id="5ed40-184">COM также определяет жизненный цикл объекта.</span><span class="sxs-lookup"><span data-stu-id="5ed40-184">COM also defines the object's life cycle.</span></span>

<span data-ttu-id="5ed40-185">**Компонент COM**</span><span class="sxs-lookup"><span data-stu-id="5ed40-185">**COM component**</span></span>

<span data-ttu-id="5ed40-186">Двоичный файл (например, DLL, OCX и некоторые exe-файлы), поддерживающий стандарт COM для предоставления объектов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-186">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects.</span></span> <span data-ttu-id="5ed40-187">Такой файл содержит код для одной или нескольких фабрик классов, COM-классов, механизмов записи реестра, загрузки кода и т. д.</span><span class="sxs-lookup"><span data-stu-id="5ed40-187">Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</span></span>

<span data-ttu-id="5ed40-188">**оператор сравнения**</span><span class="sxs-lookup"><span data-stu-id="5ed40-188">**comparison operator**</span></span>

<span data-ttu-id="5ed40-189">Оператор, который сравнивает два выражения и возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="5ed40-189">An operator that compares two expressions and returns a Boolean value.</span></span>

<span data-ttu-id="5ed40-190">Параметр условия, который может быть выражен как "\>" (больше),\<"" (меньше), "=" (равно), "\>=" (больше или равно), "\<=" (меньше или равно), "\<\>" (не равно) или "Like" (совпадение по шаблону).</span><span class="sxs-lookup"><span data-stu-id="5ed40-190">A criteria parameter that may be expressed as "\>" (greater than), "\<" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="5ed40-191">**component**</span><span class="sxs-lookup"><span data-stu-id="5ed40-191">**component**</span></span>

<span data-ttu-id="5ed40-192">Объект, который инкапсулирует данные и код и предоставляет строго указанный набор общедоступных служб.</span><span class="sxs-lookup"><span data-stu-id="5ed40-192">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

<span data-ttu-id="5ed40-193">**составной файл**</span><span class="sxs-lookup"><span data-stu-id="5ed40-193">**compound file**</span></span>

<span data-ttu-id="5ed40-194">Реализация структурированного хранилища COM для файлов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-194">An implementation of COM structured storage for files.</span></span> <span data-ttu-id="5ed40-195">Составной файл хранит отдельные объекты в один структурированный файл, состоящий из двух основных элементов: объектов хранилища и объектов потока.</span><span class="sxs-lookup"><span data-stu-id="5ed40-195">A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="5ed40-196">Вместе они работают так же, как файловая система в файле.</span><span class="sxs-lookup"><span data-stu-id="5ed40-196">Together, they function like a file system within a file.</span></span> <span data-ttu-id="5ed40-197">Дополнительные сведения содержатся в разделе составные файлы в пакете Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5ed40-197">For more information, see Compound Files in the Microsoft Platform SDK.</span></span>

<span data-ttu-id="5ed40-198">Несколько отдельных файлов, привязанных к одному физическому файлу.</span><span class="sxs-lookup"><span data-stu-id="5ed40-198">A number of individual files bound together in one physical file.</span></span> <span data-ttu-id="5ed40-199">К каждому отдельному файлу в составном файле можно получить доступ, как если бы это был один физический файл.</span><span class="sxs-lookup"><span data-stu-id="5ed40-199">Each individual file in a compound file can be accessed as if it were a single physical file.</span></span>

<span data-ttu-id="5ed40-200">**константа**</span><span class="sxs-lookup"><span data-stu-id="5ed40-200">**constant**</span></span>

<span data-ttu-id="5ed40-201">Числовое или строковое значение, которое не изменяется.</span><span class="sxs-lookup"><span data-stu-id="5ed40-201">A numeric or string value that does not change.</span></span> <span data-ttu-id="5ed40-202">Именованные перечисления ADO (перечислимые константы) можно использовать в коде вместо фактических значений, например, **адусеклиент** является константой, значение которой равно 3.</span><span class="sxs-lookup"><span data-stu-id="5ed40-202">Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, **adUseClient** is a constant whose value is 3.</span></span> <span data-ttu-id="5ed40-203">(Const Адусеклиент = 3).</span><span class="sxs-lookup"><span data-stu-id="5ed40-203">(Const adUseClient = 3).</span></span> <span data-ttu-id="5ed40-204">См. \*\*\*\* также перечисление.</span><span class="sxs-lookup"><span data-stu-id="5ed40-204">See also **enumeration**.</span></span>

<span data-ttu-id="5ed40-205">**установлен**</span><span class="sxs-lookup"><span data-stu-id="5ed40-205">**cursor**</span></span>

<span data-ttu-id="5ed40-206">Элемент Database, который управляет навигацией по записям, обновлением данных и отображением изменений, внесенных в базу данных другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="5ed40-206">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</span></span>

<span data-ttu-id="5ed40-207">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-207">Return to top</span></span>

## <a name="d"></a><span data-ttu-id="5ed40-208">D</span><span class="sxs-lookup"><span data-stu-id="5ed40-208">D</span></span>

<span data-ttu-id="5ed40-209">**Привязка данных**</span><span class="sxs-lookup"><span data-stu-id="5ed40-209">**data binding**</span></span>

<span data-ttu-id="5ed40-210">Процесс привязки объектов или элементов управления приложения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-210">The process of associating the objects or controls of an application to a data source.</span></span> <span data-ttu-id="5ed40-211">Элемент управления, связанный с источником данных, называется *элементом управления с привязкой к данным*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-211">A control associated with a data source is called a *data-bound control*.</span></span>

<span data-ttu-id="5ed40-212">Содержимое элемента управления с привязкой к данным связано со значениями из базы данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-212">The contents of a data-bound control are associated with values from a database.</span></span> <span data-ttu-id="5ed40-213">Например, элемент управления Grid, связанный с объектом **Recordset** , можно обновлять при обновлении строк в **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-213">For example, a grid control that is bound to a **Recordset** object can be updated when the rows in the **Recordset** are updated.</span></span> <span data-ttu-id="5ed40-214">Когда **набор записей**извлекает новые значения, новые значения отображаются в сетке.</span><span class="sxs-lookup"><span data-stu-id="5ed40-214">When new values are retrieved by the **Recordset**, new values are displayed in the grid.</span></span>

<span data-ttu-id="5ed40-215">**поставщик данных**</span><span class="sxs-lookup"><span data-stu-id="5ed40-215">**data provider**</span></span>

<span data-ttu-id="5ed40-216">Программное обеспечение, которое предоставляет доступ к данным для приложения ADO либо напрямую, либо через поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="5ed40-216">Software that exposes data to an ADO application either directly or via a service provider.</span></span> <span data-ttu-id="5ed40-217">Обратитесь к **поставщику услуг**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-217">See also **service provider**.</span></span>

<span data-ttu-id="5ed40-218">**формирование данных**</span><span class="sxs-lookup"><span data-stu-id="5ed40-218">**data shaping**</span></span>

<span data-ttu-id="5ed40-219">Метод, который использует формальный синтаксис (называемый **языком фигуры**), чтобы определить специализированный объект **Recordset** (который называется **набором записей в форме**), содержащий не только данные, но и ссылки на другие объекты **Recordset** и вычисляемые значения/ОР на основе этих объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-219">A technique which makes use of a formalized syntax (called **Shape language**) to define a specialized **Recordset** object (called a **shaped Recordset**) that contains not just data, but also references to other **Recordset** objects and/or computed values based on those other **Recordset** objects.</span></span>

<span data-ttu-id="5ed40-220">**уровень источника данных**</span><span class="sxs-lookup"><span data-stu-id="5ed40-220">**data source tier**</span></span>

<span data-ttu-id="5ed40-221">Логический уровень распределенной системы, представляющей компьютер, на котором выполняется СУБД, например база данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ed40-221">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database.</span></span> <span data-ttu-id="5ed40-222">См. также **уровень клиента**, **средний уровень**, **распределенное приложение**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-222">See also **client tier**, **middle tier**, **distributed application**.</span></span>

<span data-ttu-id="5ed40-223">**ТРАФИК**</span><span class="sxs-lookup"><span data-stu-id="5ed40-223">**DCOM**</span></span>

<span data-ttu-id="5ed40-224">Протокол связи, позволяющий COM-компонентам напрямую связываться друг с другом в сети.</span><span class="sxs-lookup"><span data-stu-id="5ed40-224">A wire protocol that enables COM components to communicate directly with each other across a network.</span></span> <span data-ttu-id="5ed40-225">См. также **com-** **компонент**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-225">See also **COM**, **component**.</span></span>

<span data-ttu-id="5ed40-226">**DDL (язык определения данных)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-226">**DDL (Data Definition Language)**</span></span>

<span data-ttu-id="5ed40-227">Эти операторы в SQL определяют, а не управляют данными.</span><span class="sxs-lookup"><span data-stu-id="5ed40-227">Those statements in SQL that define, as opposed to manipulate, data.</span></span> <span data-ttu-id="5ed40-228">Схема базы данных создается или изменяется с помощью DDL.</span><span class="sxs-lookup"><span data-stu-id="5ed40-228">The schema of a database is created or modified with DDL.</span></span> <span data-ttu-id="5ed40-229">Например, инструкции SQL DDL: **CREATE TABLE**, **CREATE INDEX**, **Grant**и **REVOKE** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-229">For example, **CREATE TABLE**, **CREATE INDEX**, **GRANT**, and **REVOKE** are SQL DDL statements.</span></span>

<span data-ttu-id="5ed40-230">**поток по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="5ed40-230">**default stream**</span></span>

<span data-ttu-id="5ed40-231">Текстовый или двоичный поток (представленный объектом **Stream** ), связанный с объектами **Record** или **RECORDSET** при использовании определенных поставщиков OLE DB, таких как поставщик Microsoft OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="5ed40-231">A text or binary stream (represented by a **Stream** object) that is associated with **Record** or **Recordset** objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="5ed40-232">Поток по умолчанию обычно содержит содержимое файла, например HTML-код для корня веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="5ed40-232">The default stream typically contains the contents of a file such as the HTML code for the root of a website.</span></span>

<span data-ttu-id="5ed40-233">**распределенное приложение**</span><span class="sxs-lookup"><span data-stu-id="5ed40-233">**distributed application**</span></span>

<span data-ttu-id="5ed40-234">Программа, написанная таким образом, что обработка может быть разделена на несколько компьютеров в сети.</span><span class="sxs-lookup"><span data-stu-id="5ed40-234">A program written so that the processing can be divided across multiple computers over a network.</span></span> <span data-ttu-id="5ed40-235">Как правило, распределенное приложение разделяется на представления, бизнес-логику и уровни хранилища данных или *уровни*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-235">Typically, a distributed application is divided into presentation, business logic, and data store layers, or *tiers*.</span></span> <span data-ttu-id="5ed40-236">См. также уровень **клиента**, **средний уровень**, **уровень источника данных**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-236">See also **client tier**, **middle tier**, **data source tier**.</span></span>

<span data-ttu-id="5ed40-237">**Отключенный набор записей**</span><span class="sxs-lookup"><span data-stu-id="5ed40-237">**disconnected Recordset**</span></span>

<span data-ttu-id="5ed40-238">Объект **Recordset** в кэше клиента, у которого больше нет действующего подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="5ed40-238">A **Recordset** object in a client cache that no longer has a live connection to the server.</span></span> <span data-ttu-id="5ed40-239">Если исходный источник данных необходим по некоторой причине, например обновление данных, необходимо повторно установить подключение.</span><span class="sxs-lookup"><span data-stu-id="5ed40-239">If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established.</span></span> <span data-ttu-id="5ed40-240">Тем не менее, можно получить доступ к коллекциям, свойствам и методам отключенного **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-240">However, the collections, properties, and methods of a disconnected **Recordset** can still be accessed.</span></span>

<span data-ttu-id="5ed40-241">**DLL (библиотека динамической компоновки)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-241">**DLL (dynamic-link library)**</span></span>

<span data-ttu-id="5ed40-242">Файл, содержащий одну или несколько функций, которые компилируются, связываются и хранятся отдельно от процессов, в которых они используются.</span><span class="sxs-lookup"><span data-stu-id="5ed40-242">A file that contains one or more functions that are compiled, linked, and stored separately from the processes that use them.</span></span> <span data-ttu-id="5ed40-243">Операционная система сопоставляет библиотеки DLL с адресным пространством процесса вызова при запуске процесса или во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="5ed40-243">The operating system maps the DLLs into the address space of the calling process when the process is starting, or while it is running.</span></span>

<span data-ttu-id="5ed40-244">**DML (язык обработки данных)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-244">**DML (Data Manipulation Language)**</span></span>

<span data-ttu-id="5ed40-245">Эти операторы в SQL управляют, а не определяют данные.</span><span class="sxs-lookup"><span data-stu-id="5ed40-245">Those statements in SQL that manipulate, as opposed to define, data.</span></span> <span data-ttu-id="5ed40-246">Значения в базе данных выбираются и изменяются с помощью DML.</span><span class="sxs-lookup"><span data-stu-id="5ed40-246">The values in a database are selected and modified with DML.</span></span> <span data-ttu-id="5ed40-247">Например, инструкции SQL DML: **INSERT**, **Update**, **Delete**и **SELECT** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-247">For example, **INSERT**, **UPDATE**, **DELETE**, and **SELECT** are SQL DML statements.</span></span>

<span data-ttu-id="5ed40-248">**Поставщик источника документов**</span><span class="sxs-lookup"><span data-stu-id="5ed40-248">**document source provider**</span></span>

<span data-ttu-id="5ed40-249">Особый класс поставщиков, управляющих папками и документами.</span><span class="sxs-lookup"><span data-stu-id="5ed40-249">A special class of providers that manage folders and documents.</span></span> <span data-ttu-id="5ed40-250">Если документ представлен объектом **Record** , или папка документов представлена объектом **Recordset** , то поставщик источника документа заполняет эти объекты уникальным набором полей, описывающих характеристики документа, вместо собственно собственно документа.</span><span class="sxs-lookup"><span data-stu-id="5ed40-250">When a document is represented by a **Record** object, or a folder of documents is represented by a **Recordset** object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself.</span></span> <span data-ttu-id="5ed40-251">Просмотреть также **запись ресурса**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-251">See also **resource record**.</span></span>

<span data-ttu-id="5ed40-252">**DSN (имя источника данных)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-252">**DSN (data source name)**</span></span>

<span data-ttu-id="5ed40-253">Коллекция данных, используемая для подключения приложения к определенной базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="5ed40-253">The collection of information used to connect your application to a particular ODBC database.</span></span> <span data-ttu-id="5ed40-254">Диспетчер драйверов ODBC использует эти сведения для создания подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-254">The ODBC Driver Manager uses this information to create a connection to the database.</span></span> <span data-ttu-id="5ed40-255">ИМЯ DSN может храниться в файле (DSN) или в реестре Windows (DSN компьютера).</span><span class="sxs-lookup"><span data-stu-id="5ed40-255">A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</span></span>

<span data-ttu-id="5ed40-256">**динамическое свойство**</span><span class="sxs-lookup"><span data-stu-id="5ed40-256">**dynamic property**</span></span>

<span data-ttu-id="5ed40-257">Свойство, относящееся к поставщику данных или службе курсора.</span><span class="sxs-lookup"><span data-stu-id="5ed40-257">A property specific to a data provider or the cursor service.</span></span> <span data-ttu-id="5ed40-258">Коллекция **свойств** объекта автоматически заполняется этими свойствами ("динамически").</span><span class="sxs-lookup"><span data-stu-id="5ed40-258">The **Properties** collection of an object is populated with these automatically ("dynamically").</span></span> <span data-ttu-id="5ed40-259">Объект не имеет динамических свойств до тех пор, пока он не будет подключен к источнику данных с помощью определенного поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-259">An object has no dynamic properties until it is connected to a data source through a particular data provider.</span></span> <span data-ttu-id="5ed40-260">Сведения о **поставщике данных**, **курсоре**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-260">See also **data provider**, **cursor**.</span></span>

<span data-ttu-id="5ed40-261">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-261">Return to top</span></span>

## <a name="e-i"></a><span data-ttu-id="5ed40-262">E – I</span><span class="sxs-lookup"><span data-stu-id="5ed40-262">E-I</span></span>

<span data-ttu-id="5ed40-263">**упорядочен**</span><span class="sxs-lookup"><span data-stu-id="5ed40-263">**enumeration**</span></span>

<span data-ttu-id="5ed40-264">Список именованных констант.</span><span class="sxs-lookup"><span data-stu-id="5ed40-264">A list of named constants.</span></span> <span data-ttu-id="5ed40-265">Перечисляемые значения не должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="5ed40-265">Enumerated values need not be unique.</span></span> <span data-ttu-id="5ed40-266">Однако имя каждого значения должно быть уникальным в пределах области, где определено перечисление.</span><span class="sxs-lookup"><span data-stu-id="5ed40-266">However the name of each value must be unique within the scope where the enumeration is defined.</span></span> <span data-ttu-id="5ed40-267">В ADO перечисления используются для числовых параметров и возвращаемых значений, чтобы добавить значение к коду ADO и защитить разработчика от числовых значений (которые могут изменяться от версии к версии).</span><span class="sxs-lookup"><span data-stu-id="5ed40-267">In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</span></span> <span data-ttu-id="5ed40-268">Например, чтобы открыть статический **набор записей**, используйте перечислимое значение **адопенстатик** :</span><span class="sxs-lookup"><span data-stu-id="5ed40-268">For example, to open a static **Recordset**, use the **adOpenStatic** enumerated value:</span></span>  
  

<span data-ttu-id="5ed40-269">Также называется перечислимой *константой*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-269">Also referred to as *enumerated constant*.</span></span> <span data-ttu-id="5ed40-270">Кроме того \*\*\*\*, можно просмотреть константу.</span><span class="sxs-lookup"><span data-stu-id="5ed40-270">See also **constant**.</span></span>

<span data-ttu-id="5ed40-271">**event**</span><span class="sxs-lookup"><span data-stu-id="5ed40-271">**event**</span></span>

<span data-ttu-id="5ed40-272">Действие, распознаваемое объектом, для которого можно написать код для ответа.</span><span class="sxs-lookup"><span data-stu-id="5ed40-272">An action recognized by an object, for which you can write code to respond.</span></span> <span data-ttu-id="5ed40-273">События могут создаваться при выполнении команд, завершении транзакций, навигации по набору записей и обновлении данных, среди других действий.</span><span class="sxs-lookup"><span data-stu-id="5ed40-273">Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</span></span> <span data-ttu-id="5ed40-274">См. также **обработчик событий**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-274">See also **event handler**.</span></span>

<span data-ttu-id="5ed40-275">**обработчик событий**</span><span class="sxs-lookup"><span data-stu-id="5ed40-275">**event handler**</span></span>

<span data-ttu-id="5ed40-276">Обработчик событий — это код, который выполняется при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="5ed40-276">An event handler is the code that is executed when an event occurs.</span></span> <span data-ttu-id="5ed40-277">См. также **событие**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-277">See also **event**.</span></span>

<span data-ttu-id="5ed40-278">**handler**</span><span class="sxs-lookup"><span data-stu-id="5ed40-278">**handler**</span></span>

<span data-ttu-id="5ed40-279">Процедура, которая управляет общим и относительно простым условием или операцией, например восстановлением ошибок или управлением данными.</span><span class="sxs-lookup"><span data-stu-id="5ed40-279">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</span></span>

<span data-ttu-id="5ed40-280">**иерархический набор записей**</span><span class="sxs-lookup"><span data-stu-id="5ed40-280">**hierarchical Recordset**</span></span>

<span data-ttu-id="5ed40-281">**Набор записей** , содержащий другой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-281">A **Recordset** that contains another **Recordset**.</span></span> <span data-ttu-id="5ed40-282">Сведения о процессе **формирования данных**, **глава**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-282">See also **data shaping**, **chapter**.</span></span>

<span data-ttu-id="5ed40-283">Дополнительные сведения см в разделе [доступ к строкам в иерархическом наборе записей](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="5ed40-283">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)</span></span>

<span data-ttu-id="5ed40-284">**иерархии**</span><span class="sxs-lookup"><span data-stu-id="5ed40-284">**hierarchy**</span></span>

<span data-ttu-id="5ed40-285">В общем случае иерархия — это ранжированная структура с верхним и подчиненными уровнями.</span><span class="sxs-lookup"><span data-stu-id="5ed40-285">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</span></span> <span data-ttu-id="5ed40-286">В ADO иерархические **наборы записей** используются для представления связи "родители — потомки" между записью и главой.</span><span class="sxs-lookup"><span data-stu-id="5ed40-286">In ADO, hierarchical **Recordsets** are used to represent the parent-child relationship between a record and a chapter.</span></span> <span data-ttu-id="5ed40-287">Кроме того, в ADO объекты **Record** и **Stream** можно использовать для доступа к иерархическим древовидным структурам, таким как папка и документы.</span><span class="sxs-lookup"><span data-stu-id="5ed40-287">Also in ADO, **Record** and **Stream** objects can be used to access hierarchical tree structures such as a folder and documents.</span></span> <span data-ttu-id="5ed40-288">Кроме того, ADO MD включает объекты **иерархии** для представления связи между уровнями измерения в кубе OLAP.</span><span class="sxs-lookup"><span data-stu-id="5ed40-288">ADO MD also includes **Hierarchy** objects to represent a relationship between the levels of a dimension in an OLAP cube.</span></span> <span data-ttu-id="5ed40-289">См. \*\*\*\* также иерархические записи, **связь "родители — потомки**", " **глава**" и " **дерево**".</span><span class="sxs-lookup"><span data-stu-id="5ed40-289">See also **hierarchical Recordsets**, **parent-child relationship**, **chapter**, **tree**.</span></span>

<span data-ttu-id="5ed40-290">**ISAPI (интерфейс программирования приложений для Интернет-сервера)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-290">**ISAPI (Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="5ed40-291">Набор функций для Интернет-серверов, например сервер Windows NT Server/Windows 2000, на котором запущены службы Microsoft IIS.</span><span class="sxs-lookup"><span data-stu-id="5ed40-291">A set of functions for Internet servers, such as a Windows NT Server/Windows 2000 Server running Microsoft Internet Information Services (IIS).</span></span>

<span data-ttu-id="5ed40-292">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-292">Return to top</span></span>

## <a name="k-m"></a><span data-ttu-id="5ed40-293">K – M</span><span class="sxs-lookup"><span data-stu-id="5ed40-293">K-M</span></span>

<span data-ttu-id="5ed40-294">**key**</span><span class="sxs-lookup"><span data-stu-id="5ed40-294">**key**</span></span>

<span data-ttu-id="5ed40-295">Столбец или столбцы в таблице, которые уникально идентифицируют строку; часто используется для индексирования таблицы.</span><span class="sxs-lookup"><span data-stu-id="5ed40-295">A column or columns in a table that uniquely identify a row; often used to index a table.</span></span>

<span data-ttu-id="5ed40-296">**маршалинга**</span><span class="sxs-lookup"><span data-stu-id="5ed40-296">**marshaling**</span></span>

<span data-ttu-id="5ed40-297">Процесс упаковки, отправки и распаковки параметров метода интерфейса для границ потоков или процессов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-297">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</span></span>

<span data-ttu-id="5ed40-298">**Средний уровень**</span><span class="sxs-lookup"><span data-stu-id="5ed40-298">**middle tier**</span></span>

<span data-ttu-id="5ed40-299">Логический уровень в распределенной системе между пользовательским интерфейсом или веб-клиентом и базой данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-299">The logical layer in a distributed system between a user interface or web client and the database.</span></span> <span data-ttu-id="5ed40-300">Обычно это место, в котором создаются экземпляры бизнес-объектов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-300">This is typically where business objects are instantiated.</span></span> <span data-ttu-id="5ed40-301">Средний уровень — это набор бизнес-правил и функций, которые создают и оперируют при получении информации.</span><span class="sxs-lookup"><span data-stu-id="5ed40-301">The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</span></span> <span data-ttu-id="5ed40-302">Это достигается с помощью бизнес-правил, которые могут изменяться часто, и поэтому инкапсулируются в компоненты, физически отделенные от самой логики приложения.</span><span class="sxs-lookup"><span data-stu-id="5ed40-302">They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</span></span> <span data-ttu-id="5ed40-303">Также называется *уровнем сервера приложений*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-303">Also known as *application server tier*.</span></span> <span data-ttu-id="5ed40-304">См. также **распределенное приложение**, **уровень клиента**и **уровень источника данных**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-304">See also **distributed application**, **client tier**, **data source tier**.</span></span>

<span data-ttu-id="5ed40-305">**MIME (поддержка многоцелевого расширения почты в Интернете)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-305">**MIME (Multi-purpose Internet Mail Extension)**</span></span>

<span data-ttu-id="5ed40-306">Изначально разработанный протокол Интернета, позволяющий обмениваться сообщениями электронной почты с форматированным содержимым в разнородной сети, компьютере и среде электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ed40-306">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and email environments.</span></span> <span data-ttu-id="5ed40-307">На практике MIME также были приняты и расширены приложениями, не являющимися почтой.</span><span class="sxs-lookup"><span data-stu-id="5ed40-307">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

<span data-ttu-id="5ed40-308">MIME — это стандарт, который позволяет публиковать и читать двоичные данные в Интернете.</span><span class="sxs-lookup"><span data-stu-id="5ed40-308">MIME is a standard that allows binary data to be published and read on the Internet.</span></span> <span data-ttu-id="5ed40-309">В заголовке файла с двоичными данными содержится тип MIME данных; Это информирует клиентские программы (например, веб-браузеры и почтовые пакеты) о том, что они должны обрабатывать данные иначе, чем при обработке прямого текста.</span><span class="sxs-lookup"><span data-stu-id="5ed40-309">The header of a file with binary data contains the MIME type of the data; this informs client programs (web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</span></span> <span data-ttu-id="5ed40-310">Например, заголовок веб-документа, содержащего изображение в формате JPEG, содержит тип MIME, относящийся к формату JPEG-файлов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-310">For example, the header of a web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</span></span> <span data-ttu-id="5ed40-311">Это позволяет браузеру отображать файл с помощью средства просмотра JPEG (если он есть).</span><span class="sxs-lookup"><span data-stu-id="5ed40-311">This allows a browser to display the file with its JPEG viewer, if one is present.</span></span>

<span data-ttu-id="5ed40-312">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-312">Return to top</span></span>

## <a name="n-o"></a><span data-ttu-id="5ed40-313">N – O</span><span class="sxs-lookup"><span data-stu-id="5ed40-313">N-O</span></span>

<span data-ttu-id="5ed40-314">**узлах**</span><span class="sxs-lookup"><span data-stu-id="5ed40-314">**node**</span></span>

<span data-ttu-id="5ed40-315">Элемент в иерархической структуре дерева.</span><span class="sxs-lookup"><span data-stu-id="5ed40-315">An element in a hierarchical tree structure.</span></span> <span data-ttu-id="5ed40-316">Узел может быть корневым или дочерним по отношению к другому узлу.</span><span class="sxs-lookup"><span data-stu-id="5ed40-316">A node may be the root, or the child of another node.</span></span> <span data-ttu-id="5ed40-317">Узел также может быть родителем нескольких дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-317">A node can also be the parent of multiple children.</span></span> <span data-ttu-id="5ed40-318">См. \*\*\*\* также иерархия, **дерево**, **корневой**, дочерний **элемент**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5ed40-318">See also **hierarchy**, **tree**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="5ed40-319">**переменная объекта**</span><span class="sxs-lookup"><span data-stu-id="5ed40-319">**object variable**</span></span>

<span data-ttu-id="5ed40-320">Переменная, которая содержит ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="5ed40-320">A variable that contains a reference to an object.</span></span> <span data-ttu-id="5ed40-321">Например, Обжкустомобжект — это переменная, указывающая на объект типа Кустомобжект:</span><span class="sxs-lookup"><span data-stu-id="5ed40-321">For example, objCustomObject is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="5ed40-322">— это переменная, указывающая на объект типа Кустомобжект:</span><span class="sxs-lookup"><span data-stu-id="5ed40-322">is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="5ed40-323">Set Обжкустомобжект = CreateObject (ADODB. Recordset</span><span class="sxs-lookup"><span data-stu-id="5ed40-323">Set objCustomObject = CreateObject(adodb.Recordset)</span></span>

<span data-ttu-id="5ed40-324">**ODBC (Open Database Connectivity)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-324">**ODBC (Open Database Connectivity)**</span></span>

<span data-ttu-id="5ed40-325">Стандартный языковой интерфейс программирования, используемый для подключения к различным источникам данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-325">A standard programming language interface used to connect to a variety of data sources.</span></span> <span data-ttu-id="5ed40-326">Доступ к нему обычно осуществляется с помощью панели управления, где имена источников данных (DSN) могут быть назначены для использования определенных драйверов ODBC.</span><span class="sxs-lookup"><span data-stu-id="5ed40-326">This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</span></span>

<span data-ttu-id="5ed40-327">\*\*OLE DB \*\*.</span><span class="sxs-lookup"><span data-stu-id="5ed40-327">**OLE DB**</span></span>

<span data-ttu-id="5ed40-328">Набор интерфейсов, которые предоставляют доступ к данным из различных источников с помощью COM.</span><span class="sxs-lookup"><span data-stu-id="5ed40-328">A set of interfaces that expose data from a variety of sources using COM.</span></span> <span data-ttu-id="5ed40-329">Интерфейсы OLE DB предоставляют приложениям единообразный доступ к данным, хранящимся в различных информационных источниках.</span><span class="sxs-lookup"><span data-stu-id="5ed40-329">OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</span></span> <span data-ttu-id="5ed40-330">Эти интерфейсы поддерживают функции СУБД, соответствующие источнику данных, что позволяет ему предоставлять общий доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="5ed40-330">These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</span></span> <span data-ttu-id="5ed40-331">См. также **com**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-331">See also **COM**.</span></span>

<span data-ttu-id="5ed40-332">**Оптимистическая блокировка**</span><span class="sxs-lookup"><span data-stu-id="5ed40-332">**optimistic locking**</span></span>

<span data-ttu-id="5ed40-333">Тип блокировки, в котором страница данных, содержащая одну или несколько записей, в том числе редактируемую запись, недоступна другим пользователям только при обновлении записи с помощью метода **Update** , но доступна до и после вызова **Update** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-333">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the **Update** method, but is available before and after the call to **Update**.</span></span>

<span data-ttu-id="5ed40-334">Оптимистическая блокировка используется при открытии объекта **Recordset** с параметром или свойством **LockType** , равным **адлоккоптимистик** или **адлоккбатчоптимистик**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-334">Optimistic locking is used when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockOptimistic** or **adLockBatchOptimistic**.</span></span> <span data-ttu-id="5ed40-335">См. также **Пессимистическая блокировка**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-335">See also **pessimistic locking**.</span></span>

<span data-ttu-id="5ed40-336">**Порядковое значение**</span><span class="sxs-lookup"><span data-stu-id="5ed40-336">**ordinal value**</span></span>

<span data-ttu-id="5ed40-337">Числовое расположение элемента в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="5ed40-337">The numeric location of an item within an order.</span></span> <span data-ttu-id="5ed40-338">В коллекции ADO порядковым значением первого элемента является ноль (0).</span><span class="sxs-lookup"><span data-stu-id="5ed40-338">In an ADO collection, the ordinal value of the first item is zero (0).</span></span> <span data-ttu-id="5ed40-339">Следующий элемент — один (1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="5ed40-339">The next item is one (1), and so on.</span></span>

<span data-ttu-id="5ed40-340">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-340">Return to top</span></span>

## <a name="p"></a><span data-ttu-id="5ed40-341">P</span><span class="sxs-lookup"><span data-stu-id="5ed40-341">P</span></span>

<span data-ttu-id="5ed40-342">**Параметризованная команда**</span><span class="sxs-lookup"><span data-stu-id="5ed40-342">**parameterized command**</span></span>

<span data-ttu-id="5ed40-343">Запрос или команда, позволяющие задать значения параметров перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="5ed40-343">A query or command that allows you to set parameter values before the command is executed.</span></span> <span data-ttu-id="5ed40-344">Например, строку SQL можно параметризованно путем встраивания маркеров параметров в строку SQL (с указанным символом "?").</span><span class="sxs-lookup"><span data-stu-id="5ed40-344">For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</span></span> <span data-ttu-id="5ed40-345">Затем приложение задает значения для каждого параметра и выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="5ed40-345">The application then specifies values for each parameter and executes the command.</span></span>

<span data-ttu-id="5ed40-346">**верхнего**</span><span class="sxs-lookup"><span data-stu-id="5ed40-346">**parent**</span></span>

<span data-ttu-id="5ed40-347">Управляемая сторона иерархической связи.</span><span class="sxs-lookup"><span data-stu-id="5ed40-347">The controlling side of a hierarchical relationship.</span></span> <span data-ttu-id="5ed40-348">В иерархической структуре родитель имеет один или несколько дочерних узлов, расположенных непосредственно под ним в иерархии.</span><span class="sxs-lookup"><span data-stu-id="5ed40-348">In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</span></span> <span data-ttu-id="5ed40-349">Также: **родитель — псевдоним**, **связь родители**и потомки \*\*\*\*, дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="5ed40-349">See also **parent-alias**, **parent-child relationship**, **child**.</span></span>

<span data-ttu-id="5ed40-350">**псевдоним родителя**</span><span class="sxs-lookup"><span data-stu-id="5ed40-350">**parent-alias**</span></span>

<span data-ttu-id="5ed40-351">Псевдоним, ссылающийся на родителя.</span><span class="sxs-lookup"><span data-stu-id="5ed40-351">An alias that refers to the parent.</span></span> <span data-ttu-id="5ed40-352">См. также **псевдоним**, **родительский элемент**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-352">See also **alias**, **parent**.</span></span>

<span data-ttu-id="5ed40-353">**связь "родители — потомки"**</span><span class="sxs-lookup"><span data-stu-id="5ed40-353">**parent-child relationship**</span></span>

<span data-ttu-id="5ed40-354">Связь в иерархической структуре, в которой родитель находится на один уровень выше и напрямую связан с одним или несколькими дочерними объектами.</span><span class="sxs-lookup"><span data-stu-id="5ed40-354">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</span></span> <span data-ttu-id="5ed40-355">Дочерний элемент на один уровень ниже и должен иметь один родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="5ed40-355">A child is one level lower and must have one parent.</span></span> <span data-ttu-id="5ed40-356">См. также **Parent**, **Child**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-356">See also **parent**, **child**.</span></span>

<span data-ttu-id="5ed40-357">**храним**</span><span class="sxs-lookup"><span data-stu-id="5ed40-357">**persist**</span></span>

<span data-ttu-id="5ed40-358">Для сохранения данных в постоянном состоянии, например для сохранения объекта **Recordset** в файле.</span><span class="sxs-lookup"><span data-stu-id="5ed40-358">To save data in a permanent state, such as saving a **Recordset** to a file.</span></span>

<span data-ttu-id="5ed40-359">**Пессимистическая блокировка**</span><span class="sxs-lookup"><span data-stu-id="5ed40-359">**pessimistic locking**</span></span>

<span data-ttu-id="5ed40-360">Тип блокировки, в котором страница, содержащая одну или несколько записей, в том числе редактируемую запись, становится недоступной для других пользователей, чтобы убедиться в том, что обновление будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="5ed40-360">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</span></span> <span data-ttu-id="5ed40-361">Пессимистическая блокировка определяется поставщиком OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5ed40-361">Pessimistic locking behavior is defined by the OLE DB provider.</span></span> <span data-ttu-id="5ed40-362">Как правило, записи блокируются при редактировании и оставались недоступными, пока не завершится метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-362">Typically, records are locked upon editing and remain unavailable until the **Update** method has completed.</span></span>

<span data-ttu-id="5ed40-363">Пессимистическая блокировка включается при открытии объекта **Recordset** с параметром или свойством **LockType** , равным **адлоккпессимистик**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-363">Pessimistic locking is enabled when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockPessimistic**.</span></span> <span data-ttu-id="5ed40-364">См. также **Оптимистическая блокировка**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-364">See also **optimistic locking**.</span></span>

<span data-ttu-id="5ed40-365">**группировкой**</span><span class="sxs-lookup"><span data-stu-id="5ed40-365">**pooling**</span></span>

<span data-ttu-id="5ed40-366">Оптимизация производительности на основе использования коллекций предварительно выделенных ресурсов, таких как объекты или подключения к базам данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-366">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</span></span> <span data-ttu-id="5ed40-367">Более эффективная прорисовка существующего ресурса из пула по сравнению с созданием нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="5ed40-367">It is more efficient to draw an existing resource from the pool than to create a new resource.</span></span>

<span data-ttu-id="5ed40-368">**ProgID (программный идентификатор)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-368">**ProgID (programmatic identifier)**</span></span>

<span data-ttu-id="5ed40-369">Уникальное имя, сопоставленное с реестром Windows приложением COM.</span><span class="sxs-lookup"><span data-stu-id="5ed40-369">A unique name mapped to the Windows registry by a COM application.</span></span> <span data-ttu-id="5ed40-370">ProgID для подключения ADO — "ADODB. Подключение ".</span><span class="sxs-lookup"><span data-stu-id="5ed40-370">The ProgID for an ADO Connection is "ADODB.Connection".</span></span> <span data-ttu-id="5ed40-371">См. также **CLSID**, **com**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-371">See also **CLSID**, **COM**.</span></span>

<span data-ttu-id="5ed40-372">**proxy**</span><span class="sxs-lookup"><span data-stu-id="5ed40-372">**proxy**</span></span>

<span data-ttu-id="5ed40-373">Зависящий от интерфейса объект, обеспечивающий маршалирование параметров и связь, необходимые клиенту для вызова объекта приложения, выполняющегося в другой среде выполнения, например в другом потоке или в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="5ed40-373">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="5ed40-374">Прокси-сервер размещается в клиенте и взаимодействуют с соответствующей заглушкой, расположенной с вызываемым объектом Application.</span><span class="sxs-lookup"><span data-stu-id="5ed40-374">The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</span></span> <span data-ttu-id="5ed40-375">См. \*\*\*\* также заглушка.</span><span class="sxs-lookup"><span data-stu-id="5ed40-375">See also **stub**.</span></span>

<span data-ttu-id="5ed40-376">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-376">Return to top</span></span>

## <a name="r"></a><span data-ttu-id="5ed40-377">R</span><span class="sxs-lookup"><span data-stu-id="5ed40-377">R</span></span>

<span data-ttu-id="5ed40-378">**относительный URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="5ed40-378">**relative URL**</span></span>

<span data-ttu-id="5ed40-379">Частично определенный URL-адрес, указывающий ресурс в Интернете или интрасети, расположение которого связано с отправной точкой, указанной абсолютным URL-АДРЕСом или эквивалентным объектом подключения ADO.</span><span class="sxs-lookup"><span data-stu-id="5ed40-379">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</span></span> <span data-ttu-id="5ed40-380">Фактически сцепленные абсолютные и относительные URL-адреса конситуте полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ed40-380">In effect, the concatenated absolute and relative URLs consitute a complete URL.</span></span> <span data-ttu-id="5ed40-381">См. также **URL-адрес** и **абсолютный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-381">See also **URL** and **absolute URL**.</span></span>

<span data-ttu-id="5ed40-382">**удаленный источник данных**</span><span class="sxs-lookup"><span data-stu-id="5ed40-382">**remote data source**</span></span>

<span data-ttu-id="5ed40-383">Источник данных, который существует на другом компьютере, а не в локальной системе (где выполняется клиентское приложение).</span><span class="sxs-lookup"><span data-stu-id="5ed40-383">A data source that exists on a another computer, rather than on the local system (where the client application runs).</span></span>

<span data-ttu-id="5ed40-384">**запись ресурса**</span><span class="sxs-lookup"><span data-stu-id="5ed40-384">**resource record**</span></span>

<span data-ttu-id="5ed40-385">Запись из поставщика источника документов, содержащая поля для определения и описания папки или документа.</span><span class="sxs-lookup"><span data-stu-id="5ed40-385">A record from a document source provider that contains fields for the definition and description of a folder or document.</span></span> <span data-ttu-id="5ed40-386">Сам документ не содержится в записи ресурса, но обычно к нему можно получить доступ с помощью потока по умолчанию или поля в записи ресурса, содержащей URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ed40-386">The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</span></span> <span data-ttu-id="5ed40-387">В разделе также содержится **поставщик источника документов**, **поток по умолчанию**, **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-387">See also **document source provider**, **default stream**, **URL**.</span></span>

<span data-ttu-id="5ed40-388">**root**</span><span class="sxs-lookup"><span data-stu-id="5ed40-388">**root**</span></span>

<span data-ttu-id="5ed40-389">Уровень верхнего уровня в иерархической структуре дерева.</span><span class="sxs-lookup"><span data-stu-id="5ed40-389">The top level in a hierarchical tree structure.</span></span> <span data-ttu-id="5ed40-390">Корневой узел не имеет родителей, но может иметь дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="5ed40-390">The root node has no parents, but may have children.</span></span> <span data-ttu-id="5ed40-391">См. \*\*\*\* также иерархия, **дерево**, **родитель**, дочерний **элемент**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-391">See also **hierarchy**, **tree**, **parent**, **child**.</span></span>

<span data-ttu-id="5ed40-392">**возвращаем**</span><span class="sxs-lookup"><span data-stu-id="5ed40-392">**rowset**</span></span>

<span data-ttu-id="5ed40-393">Набор строк из источника данных, каждая из которых имеет одну и ту же схему поля.</span><span class="sxs-lookup"><span data-stu-id="5ed40-393">A set of rows from a data source, all having the same field schema.</span></span> <span data-ttu-id="5ed40-394">Набор строк может представлять все или некоторые поля из таблицы.</span><span class="sxs-lookup"><span data-stu-id="5ed40-394">A rowset can represent all or some fields from a table.</span></span> <span data-ttu-id="5ed40-395">Набор строк также может представлять виртуальную таблицу, созданную запросом или соединением двух или более таблиц.</span><span class="sxs-lookup"><span data-stu-id="5ed40-395">A rowset can also represent a virtual table, created by a query or a join of two or more tables.</span></span> <span data-ttu-id="5ed40-396">В ADO наборы строк представлены объектами **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-396">In ADO, rowsets are represented by **Recordset** objects.</span></span>

<span data-ttu-id="5ed40-397">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-397">Return to top</span></span>

## <a name="s"></a><span data-ttu-id="5ed40-398">S</span><span class="sxs-lookup"><span data-stu-id="5ed40-398">S</span></span>

<span data-ttu-id="5ed40-399">**схемы**</span><span class="sxs-lookup"><span data-stu-id="5ed40-399">**schema**</span></span>

<span data-ttu-id="5ed40-400">Описание базы данных для системы управления базами данных (СУБД), обычно создаваемой с помощью языка определения данных, предоставляемого СУБД.</span><span class="sxs-lookup"><span data-stu-id="5ed40-400">A description of a database to the database management system (DBMS), typically generated using the data definition language provided by the DBMS.</span></span> <span data-ttu-id="5ed40-401">Схема определяет атрибуты базы данных, такие как таблицы, столбцы и свойства.</span><span class="sxs-lookup"><span data-stu-id="5ed40-401">A schema defines attributes of the database, such as tables, columns, and properties.</span></span>

<span data-ttu-id="5ed40-402">**scope**</span><span class="sxs-lookup"><span data-stu-id="5ed40-402">**scope**</span></span>

<span data-ttu-id="5ed40-403">Диапазон ссылок для объекта или переменной или диапазона записей в представлении или таблице.</span><span class="sxs-lookup"><span data-stu-id="5ed40-403">The range of reference for an object or variable or a range of records in a view or table.</span></span> <span data-ttu-id="5ed40-404">Например, ссылаться на локальные переменные можно только в той процедуре, в которой они были определены.</span><span class="sxs-lookup"><span data-stu-id="5ed40-404">For example, local variables can be referenced only within the procedure in which they were defined.</span></span> <span data-ttu-id="5ed40-405">Доступ к общеДоступным переменным можно получить из любого места в приложении.</span><span class="sxs-lookup"><span data-stu-id="5ed40-405">Public variables are accessible from anywhere in the application.</span></span> <span data-ttu-id="5ed40-406">Объекты, такие как текущая база данных, находятся в области действия, если они находятся в определенном пути поиска.</span><span class="sxs-lookup"><span data-stu-id="5ed40-406">Objects, such as the current database, are in scope if they are in the defined search path.</span></span> <span data-ttu-id="5ed40-407">Диапазоны записей можно указать с помощью предложения Scope во многих командах.</span><span class="sxs-lookup"><span data-stu-id="5ed40-407">Record ranges can be specified with a Scope clause in many commands.</span></span>

<span data-ttu-id="5ed40-408">**поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="5ed40-408">**service provider**</span></span>

<span data-ttu-id="5ed40-409">Программное обеспечение, которое инкапсулирует службу, создавая и используя данные, расширяя возможности приложений ADO.</span><span class="sxs-lookup"><span data-stu-id="5ed40-409">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="5ed40-410">Это поставщик, который не предоставляет данные напрямую, а предоставляет службу, например обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-410">It is a provider that does not directly expose data, rather it provides a service, such as query processing.</span></span> <span data-ttu-id="5ed40-411">Поставщик услуг может обрабатывать данные, предоставляемые поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="5ed40-411">The service provider may process data provided by a data provider.</span></span> <span data-ttu-id="5ed40-412">См. также **поставщик данных**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-412">See also **data provider**.</span></span>

<span data-ttu-id="5ed40-413">**Набор записей в форме**</span><span class="sxs-lookup"><span data-stu-id="5ed40-413">**shaped Recordset**</span></span>

<span data-ttu-id="5ed40-414">**Набор записей** , столбцы которого были специально определены как содержащие данные, но также ссылки (называемые главы) на другие объекты **Recordset** и/или вычисляемые значения на основе других объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5ed40-414">A **Recordset** whose columns have been specifically defined to contain not just data, but also references (called chapters) to other **Recordset** objects and/or computed values based on other **Recordset** objects.</span></span>

<span data-ttu-id="5ed40-415">**узлом**</span><span class="sxs-lookup"><span data-stu-id="5ed40-415">**sibling**</span></span>

<span data-ttu-id="5ed40-416">Все два или более узла в иерархической структуре, расположенные на одном уровне иерархии.</span><span class="sxs-lookup"><span data-stu-id="5ed40-416">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</span></span> <span data-ttu-id="5ed40-417">Корневой узел в иерархии не имеет родственных элементов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-417">The root node in a hierarchy has no siblings.</span></span>

<span data-ttu-id="5ed40-418">**хранимая процедура**</span><span class="sxs-lookup"><span data-stu-id="5ed40-418">**stored procedure**</span></span>

<span data-ttu-id="5ed40-419">Предкомпилированная коллекция кода, например инструкции SQL и необязательные операторы управления выполнением, которые хранятся под именем и обрабатываются как единое целое.</span><span class="sxs-lookup"><span data-stu-id="5ed40-419">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</span></span> <span data-ttu-id="5ed40-420">Хранимые процедуры хранятся в базе данных; они могут выполняться с одним вызовом из приложения и разрешать объявляемые пользователями переменные, условное выполнение и другие мощные функциональные возможности программирования.</span><span class="sxs-lookup"><span data-stu-id="5ed40-420">Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</span></span>

<span data-ttu-id="5ed40-421">**@**</span><span class="sxs-lookup"><span data-stu-id="5ed40-421">**stub**</span></span>

<span data-ttu-id="5ed40-422">Объект, зависящий от интерфейса, который обеспечивает маршалинг параметров и связь, необходимые для объекта Application для получения вызовов от клиента, выполняющегося в другой среде выполнения, например в другом потоке или в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="5ed40-422">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="5ed40-423">Заглушка размещается с помощью объекта Application и связывается с соответствующим прокси-сервером, расположенным с клиентом, который его вызывает.</span><span class="sxs-lookup"><span data-stu-id="5ed40-423">The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</span></span> <span data-ttu-id="5ed40-424">См. также **proxy**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-424">See also **proxy**.</span></span>

<span data-ttu-id="5ed40-425">**вложенный узел**</span><span class="sxs-lookup"><span data-stu-id="5ed40-425">**sub-node**</span></span>

<span data-ttu-id="5ed40-426">Просмотр **дочерних элементов**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-426">See **child**.</span></span>

<span data-ttu-id="5ed40-427">**синхронная операция**</span><span class="sxs-lookup"><span data-stu-id="5ed40-427">**synchronous operation**</span></span>

<span data-ttu-id="5ed40-428">Операция, инициированная кодом, который завершается до того, как может начаться следующая операция.</span><span class="sxs-lookup"><span data-stu-id="5ed40-428">An operation initiated by code that completes before the next operation may start.</span></span> <span data-ttu-id="5ed40-429">См. также **асинхронные операции**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-429">See also **asynchronous operation**.</span></span>

<span data-ttu-id="5ed40-430">В начало</span><span class="sxs-lookup"><span data-stu-id="5ed40-430">Return to top</span></span>

## <a name="t-w"></a><span data-ttu-id="5ed40-431">T ВТ</span><span class="sxs-lookup"><span data-stu-id="5ed40-431">T-W</span></span>

<span data-ttu-id="5ed40-432">**объектов**</span><span class="sxs-lookup"><span data-stu-id="5ed40-432">**tree**</span></span>

<span data-ttu-id="5ed40-433">Структура, представляющая иерархические отношения между элементами (узлами).</span><span class="sxs-lookup"><span data-stu-id="5ed40-433">A structure representing a hierarchical relationship between elements (nodes).</span></span> <span data-ttu-id="5ed40-434">Существует один узел на верхнем уровне дерева (корень).</span><span class="sxs-lookup"><span data-stu-id="5ed40-434">There is one node at the top level of a tree (the root).</span></span> <span data-ttu-id="5ed40-435">Под корневым каталогом может быть несколько дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-435">Underneath the root, there can be multiple children.</span></span> <span data-ttu-id="5ed40-436">Все дочерние элементы могут быть родительскими для других дочерних элементов, поэтому ветвление аналогично дереву.</span><span class="sxs-lookup"><span data-stu-id="5ed40-436">Each child may in turn be the parent of other children, thus branching like a tree.</span></span> <span data-ttu-id="5ed40-437">Папка, содержащая документы и другие папки, представляет собой типичный пример древовидной структуры.</span><span class="sxs-lookup"><span data-stu-id="5ed40-437">A folder containing documents and other folders is a typical example of a tree structure.</span></span> <span data-ttu-id="5ed40-438">См. \*\*\*\* также иерархия, **узел**, **корень**, дочерний **элемент**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5ed40-438">See also **hierarchy**, **node**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="5ed40-439">**URL-адрес (унифицированный указатель ресурсов)**</span><span class="sxs-lookup"><span data-stu-id="5ed40-439">**URL (Uniform Resource Locator)**</span></span>

<span data-ttu-id="5ed40-440">Указывает расположение ресурса, находящегося в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="5ed40-440">Specifies the location of a resource residing on the Internet or an intranet.</span></span> <span data-ttu-id="5ed40-441">Полный URL-адрес состоит из схемы (например, FTP, HTTP, mailto, File и т. д.), за которым следует двоеточие, имя сервера и полный путь к ресурсу (например, документ, графический объект или другой файл).</span><span class="sxs-lookup"><span data-stu-id="5ed40-441">A complete URL consists of a scheme (such as FTP, HTTP, mailto, file, and so on), followed by a colon, a server name, and the full path of a resource (such as a document, graphic, or other file).</span></span> <span data-ttu-id="5ed40-442">Ниже приведены примеры URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="5ed40-442">Some examples of URLs are:</span></span>  
  
- https://www.domain.com/default.html  
- <span data-ttu-id="5ed40-443">FTP://FTP.Server.Somewhere/FTP.File</span><span class="sxs-lookup"><span data-stu-id="5ed40-443">ftp://ftp.server.somewhere/ftp.file</span></span>  
  
- <span data-ttu-id="5ed40-444">FTP://FTP.Server.Somewhere/FTP.File</span><span class="sxs-lookup"><span data-stu-id="5ed40-444">ftp://ftp.server.somewhere/ftp.file</span></span>  
- <span data-ttu-id="5ed40-445">file://Server/Share/File.doc</span><span class="sxs-lookup"><span data-stu-id="5ed40-445">file://Server/Share/File.doc</span></span>

<span data-ttu-id="5ed40-446">См. также **абсолютНЫЙ URL-адрес** и отНОСИТЕЛЬНЫЙ **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="5ed40-446">See also **absolute URL** and **relative URL**.</span></span>

<span data-ttu-id="5ed40-447">**веб-сервер**</span><span class="sxs-lookup"><span data-stu-id="5ed40-447">**web server**</span></span>

<span data-ttu-id="5ed40-448">Компьютер, предоставляющий веб-службы и страницы пользователям интрасети и Интернета.</span><span class="sxs-lookup"><span data-stu-id="5ed40-448">A computer that provides web services and pages to intranet and Internet users.</span></span>



