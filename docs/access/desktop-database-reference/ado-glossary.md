---
title: Глоссарий ActiveX Data Objects (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9b9fd656aeda727cc829ab47ea4cb9fab8f2a169
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997793"
---
# <a name="ado-glossary"></a><span data-ttu-id="88d5b-102">Глоссарий ADO</span><span class="sxs-lookup"><span data-stu-id="88d5b-102">ADO glossary</span></span>

<span data-ttu-id="88d5b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88d5b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="a"></a><span data-ttu-id="88d5b-104">A</span><span class="sxs-lookup"><span data-stu-id="88d5b-104">A</span></span>

<span data-ttu-id="88d5b-105">**Абсолютный URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="88d5b-105">**absolute URL**</span></span>

<span data-ttu-id="88d5b-106">Полный URL-адрес, указывающий местоположение ресурс, который находится в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="88d5b-106">A fully qualified URL that specifies the location of a resource that resides on the Internet or an intranet.</span></span> <span data-ttu-id="88d5b-107">В разделе также **URL-адреса** и **относительный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-107">See also **URL** and **relative URL**.</span></span>

<span data-ttu-id="88d5b-108">**элемент ActiveX**</span><span class="sxs-lookup"><span data-stu-id="88d5b-108">**ActiveX control**</span></span>

<span data-ttu-id="88d5b-109">Самостоятельно регистрации в процессе COM-компонентом, часто имеется визуальный элемент во время разработки или во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-109">Self-registering, in-process COM component that often has a visual element either at design time or run time.</span></span> <span data-ttu-id="88d5b-110">Элементы управления ActiveX также могут получать для взаимодействия с контейнер активных документов, таких как Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="88d5b-110">ActiveX controls also have the ability to communicate with an Active Document container, such as Microsoft Internet Explorer.</span></span>

<span data-ttu-id="88d5b-111">**ADISAPI (Дополнительные данные Internet Server прикладной программный интерфейс)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-111">**ADISAPI (Advanced Data Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="88d5b-112">ISAPI DLL, которая предоставляет средства синтаксического анализа, управления автоматизации, маршалинга **записей** и упаковки MIME.</span><span class="sxs-lookup"><span data-stu-id="88d5b-112">An ISAPI DLL that provides parsing, Automation control, **Recordset** marshaling, and MIME packaging.</span></span> <span data-ttu-id="88d5b-113">Компонент ADISAPI работает через API, предоставленных Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="88d5b-113">The ADISAPI component works through the API provided by Internet Information Services (IIS).</span></span> <span data-ttu-id="88d5b-114">Смотрите также **ISAPI**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-114">See also **ISAPI**.</span></span>

<span data-ttu-id="88d5b-115">**статистические функции**</span><span class="sxs-lookup"><span data-stu-id="88d5b-115">**aggregate function**</span></span>

<span data-ttu-id="88d5b-116">В запросе, функции, такие как COUNT, AVG или STDEV, вычисляющий значение с помощью все строки в столбец таблицы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-116">In a query, a function such as COUNT, AVG, or STDEV that calculates a value using all the rows in a column of a table.</span></span> <span data-ttu-id="88d5b-117">В выражениях и при программировании на статистические функции SQL (включая трех перечисленных выше) и статистические функции можно использовать для определения различная Статистика.</span><span class="sxs-lookup"><span data-stu-id="88d5b-117">In writing expressions and in programming, you can use SQL aggregate functions (including the three listed above) and domain aggregate functions to determine various statistics.</span></span>

<span data-ttu-id="88d5b-118">**alias**</span><span class="sxs-lookup"><span data-stu-id="88d5b-118">**alias**</span></span>

<span data-ttu-id="88d5b-119">Альтернативное имя, присваиваемое столбец или выражение в инструкции SQL SELECT, часто меньшие или более удобной для восприятия.</span><span class="sxs-lookup"><span data-stu-id="88d5b-119">An alternate name you give to a column or expression in an SQL SELECT statement, often shorter or more meaningful.</span></span> <span data-ttu-id="88d5b-120">Например, BobSales — это псевдоним в следующей инструкции SELECT: «Выберите wr продаж в качестве BobSales из SalesDB».</span><span class="sxs-lookup"><span data-stu-id="88d5b-120">For example, BobSales is the alias in the following SELECT statement: "Select wr-Sales as BobSales from SalesDB".</span></span> <span data-ttu-id="88d5b-121">Псевдоним можно использовать для динамического назначения столбцы для управления привязками на объекте **DataControl** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-121">An alias can be used to dynamically assign columns to control bindings on the **DataControl** object.</span></span>

<span data-ttu-id="88d5b-122">**потоковое**</span><span class="sxs-lookup"><span data-stu-id="88d5b-122">**apartment threading**</span></span>

<span data-ttu-id="88d5b-123">COM, потоковой модели, где все вызовы объекта только на один поток.</span><span class="sxs-lookup"><span data-stu-id="88d5b-123">A COM threading model where all calls to an object occur on one thread.</span></span> <span data-ttu-id="88d5b-124">В потоковое, COM синхронизирует и передает вызовы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-124">In apartment threading, COM synchronizes and marshals calls.</span></span> <span data-ttu-id="88d5b-125">Смотрите также **COM**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-125">See also **COM**.</span></span>

<span data-ttu-id="88d5b-126">**асинхронной операции**</span><span class="sxs-lookup"><span data-stu-id="88d5b-126">**asynchronous operation**</span></span>

<span data-ttu-id="88d5b-127">Операция, которая возвращает элемент управления в вызывающую программу, не дожидаясь завершения операции.</span><span class="sxs-lookup"><span data-stu-id="88d5b-127">An operation that returns control to the calling program without waiting for the operation to complete.</span></span> <span data-ttu-id="88d5b-128">До завершения операции продолжает выполнение кода.</span><span class="sxs-lookup"><span data-stu-id="88d5b-128">Before the operation is complete, code execution continues.</span></span> <span data-ttu-id="88d5b-129">В разделе также **синхронный режим**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-129">See also **synchronous operation**.</span></span>

<span data-ttu-id="88d5b-130">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-130">Return to top</span></span>

## <a name="b"></a><span data-ttu-id="88d5b-131">B</span><span class="sxs-lookup"><span data-stu-id="88d5b-131">B</span></span>

<span data-ttu-id="88d5b-132">**Операция привязки**</span><span class="sxs-lookup"><span data-stu-id="88d5b-132">**binding entry**</span></span>

<span data-ttu-id="88d5b-133">Сопоставление полей в таблице и переменной.</span><span class="sxs-lookup"><span data-stu-id="88d5b-133">A mapping between a field in a table and a variable.</span></span> <span data-ttu-id="88d5b-134">В расширениях ADO Visual C++ полям **набора записей** , сопоставляются с переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="88d5b-134">In the ADO Visual C++ extensions, **Recordset** fields are mapped to C/C++ variables.</span></span>

<span data-ttu-id="88d5b-135">**Битовая маска**</span><span class="sxs-lookup"><span data-stu-id="88d5b-135">**bitmask**</span></span>

<span data-ttu-id="88d5b-136">Числовое значение, предназначенные для сравнения значения-с разрядная с других числовых значений обычно для пометки параметры в параметров или возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="88d5b-136">A numeric value intended for a bit-by-bit value comparison with other numeric values, typically to flag options in parameter or return values.</span></span> <span data-ttu-id="88d5b-137">Обычно это сравнение выполняется с помощью побитовое логические операторы, такие как **и** и **или** в Visual Basic, **&** и **|** в C++.</span><span class="sxs-lookup"><span data-stu-id="88d5b-137">Usually this comparison is done with bitwise logical operators, such as **And** and **Or** in Visual Basic, **&** and **|** in C++.</span></span>

<span data-ttu-id="88d5b-138">Например ADO **FieldAttributeEnum** значения можно использовать в качестве битовой маски для определения атрибуты поля.</span><span class="sxs-lookup"><span data-stu-id="88d5b-138">For example, the ADO **FieldAttributeEnum** values can be used as bitmasks to determine the attributes of a field.</span></span> <span data-ttu-id="88d5b-139">Предположим, что вы хотите определить, было ли поле получаться.</span><span class="sxs-lookup"><span data-stu-id="88d5b-139">Suppose you wanted to determine if a field was updateable.</span></span> <span data-ttu-id="88d5b-140">Для этого может проверить следующее выражение в Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="88d5b-140">You could test for this with the following expression in Visual Basic:</span></span>  
  

<span data-ttu-id="88d5b-141">Если результат имеет значение TRUE, это поле является обновляемым.</span><span class="sxs-lookup"><span data-stu-id="88d5b-141">If the result is TRUE, then the field is updateable.</span></span>

<span data-ttu-id="88d5b-142">**Закладка**</span><span class="sxs-lookup"><span data-stu-id="88d5b-142">**bookmark**</span></span>

<span data-ttu-id="88d5b-143">Маркер, который уникально идентифицирует строки в наборе строк, чтобы пользователь можно быстро перейти к нему.</span><span class="sxs-lookup"><span data-stu-id="88d5b-143">A marker that uniquely identifies a row within a set of rows so that a user can quickly navigate to it.</span></span>

<span data-ttu-id="88d5b-144">**бизнес-объект**</span><span class="sxs-lookup"><span data-stu-id="88d5b-144">**business object**</span></span>

<span data-ttu-id="88d5b-145">Объект, который выполняет определенный набор операций, таких как логика правила проверки или бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-145">An object that performs a defined set of operations, such as data validation or business rule logic.</span></span> <span data-ttu-id="88d5b-146">Бизнес-объекты обычно размещаются на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="88d5b-146">Business objects usually reside on the middle tier.</span></span>

<span data-ttu-id="88d5b-147">**бизнес-правила**</span><span class="sxs-lookup"><span data-stu-id="88d5b-147">**business rule**</span></span>

<span data-ttu-id="88d5b-148">Комбинация проверки изменения, проверки входа в систему, поиск в базе данных, политик и алгоритма преобразования, которые составляют способ организации ведения бизнеса.</span><span class="sxs-lookup"><span data-stu-id="88d5b-148">The combination of validation edits, logon verifications, database lookups, policies, and algorithmic transformations that constitute an enterprise's way of doing business.</span></span> <span data-ttu-id="88d5b-149">Также известной как *бизнес-логики*.</span><span class="sxs-lookup"><span data-stu-id="88d5b-149">Also known as *business logic*.</span></span>

<span data-ttu-id="88d5b-150">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-150">Return to top</span></span>

## <a name="c"></a><span data-ttu-id="88d5b-151">C</span><span class="sxs-lookup"><span data-stu-id="88d5b-151">C</span></span>

<span data-ttu-id="88d5b-152">**расчетного выражения**</span><span class="sxs-lookup"><span data-stu-id="88d5b-152">**calculated expression**</span></span>

<span data-ttu-id="88d5b-153">Выражение, которое не является постоянным, однако, значение которого зависит от других значений.</span><span class="sxs-lookup"><span data-stu-id="88d5b-153">An expression that is not constant, but whose value depends upon other values.</span></span> <span data-ttu-id="88d5b-154">Для оценки, расчетного выражения необходимо получить и вычисление значений из других источников, обычно в другие поля или строки.</span><span class="sxs-lookup"><span data-stu-id="88d5b-154">To be evaluated, a calculated expression must obtain and compute values from other sources, typically in other fields or rows.</span></span>

<span data-ttu-id="88d5b-155">**главы**</span><span class="sxs-lookup"><span data-stu-id="88d5b-155">**chapter**</span></span>

<span data-ttu-id="88d5b-156">Ссылка на диапазон строк из источника данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-156">A reference to a range of rows from a data source.</span></span> <span data-ttu-id="88d5b-157">В ADO главы обычно является ссылкой на другой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-157">In ADO, a chapter is typically a reference to another **Recordset**.</span></span>

<span data-ttu-id="88d5b-158">Глава столбцов позволяют Определение отношения *родительских и дочерних* где *родительский* — **набора записей** , содержащий столбец главы и *дочерние* — **набора записей** , представленный в главе.</span><span class="sxs-lookup"><span data-stu-id="88d5b-158">Chapter columns make it possible to define a *parent-child* relationship where the *parent* is the **Recordset** containing the chapter column and the *child* is the **Recordset** represented by the chapter.</span></span>

<span data-ttu-id="88d5b-159">**псевдоним главы**</span><span class="sxs-lookup"><span data-stu-id="88d5b-159">**chapter-alias**</span></span>

<span data-ttu-id="88d5b-160">Псевдоним, который ссылается на столбец, добавляемый в родительском.</span><span class="sxs-lookup"><span data-stu-id="88d5b-160">An alias that refers to the column appended to the parent.</span></span>

<span data-ttu-id="88d5b-161">**набор символов**</span><span class="sxs-lookup"><span data-stu-id="88d5b-161">**character set**</span></span>

<span data-ttu-id="88d5b-162">Сопоставление набора символов для их числовые значения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-162">A mapping of a set of characters to their numeric values.</span></span> <span data-ttu-id="88d5b-163">Например Юникод — символ 16-разрядной задайте для кодирования все известные символы и использовать в качестве по всему миру Стандартная кодировка символов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-163">For example, Unicode is a 16-bit character set capable of encoding all known characters and used as a worldwide character-encoding standard.</span></span>

<span data-ttu-id="88d5b-164">**дочерние**</span><span class="sxs-lookup"><span data-stu-id="88d5b-164">**child**</span></span>

<span data-ttu-id="88d5b-165">Зависимые стороны иерархическую связь.</span><span class="sxs-lookup"><span data-stu-id="88d5b-165">The dependent side of a hierarchical relationship.</span></span> <span data-ttu-id="88d5b-166">Является дочернего узла в иерархической структуры, имеющей другой узел над текстом (ближе к корню).</span><span class="sxs-lookup"><span data-stu-id="88d5b-166">A child is a node in a hierarchical structure that has another node above it (closer to the root).</span></span> <span data-ttu-id="88d5b-167">См. также **дочерние псевдоним**, **отношения родительских и дочерних**, **родительского**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-167">See also **child-alias**, **parent-child relationship**, **parent**.</span></span>

<span data-ttu-id="88d5b-168">**псевдоним дочерних**</span><span class="sxs-lookup"><span data-stu-id="88d5b-168">**child-alias**</span></span>

<span data-ttu-id="88d5b-169">Псевдоним, который относится к дочерним.</span><span class="sxs-lookup"><span data-stu-id="88d5b-169">An alias that refers to the child.</span></span> <span data-ttu-id="88d5b-170">В разделе также **псевдоним**, **дочерние**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-170">See also **alias**, **child**.</span></span>

<span data-ttu-id="88d5b-171">**CLSID (идентификатор класса)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-171">**CLSID (class identifier)**</span></span>

<span data-ttu-id="88d5b-172">Уникальный идентификатор (UUID), определяющий COM-компонентом.</span><span class="sxs-lookup"><span data-stu-id="88d5b-172">A universally unique identifier (UUID) that identifies a COM component.</span></span> <span data-ttu-id="88d5b-173">Каждый COM-компонент имеет свой идентификатор в реестре Windows, чтобы ее можно загрузить с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="88d5b-173">Each COM component has its CLSID in the Windows Registry so that it can be loaded by other applications.</span></span> <span data-ttu-id="88d5b-174">В разделе также **ProgID**, **COM**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-174">See also **ProgID**, **COM**.</span></span>

<span data-ttu-id="88d5b-175">**уровня клиента**</span><span class="sxs-lookup"><span data-stu-id="88d5b-175">**client tier**</span></span>

<span data-ttu-id="88d5b-176">Логический слой распределенных систем, который обычно представляет данные для и обрабатывает входные данные от пользователя, иногда называется *переднего плана*.</span><span class="sxs-lookup"><span data-stu-id="88d5b-176">A logical layer of a distributed system that typically presents data to and processes input from the user, sometimes referred to as the *front end*.</span></span> <span data-ttu-id="88d5b-177">Как правило на клиентском уровне запрашивает данные от сервера, на основе введенных данных и затем форматирует и отображает результат.</span><span class="sxs-lookup"><span data-stu-id="88d5b-177">Usually, the client tier requests data from a server based on input, and then formats and displays the result.</span></span> <span data-ttu-id="88d5b-178">Смотрите также **Средний уровень**, **уровень источника данных**, **распределенных приложений**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-178">See also **middle tier**, **data source tier**, **distributed application**.</span></span>

<span data-ttu-id="88d5b-179">**COM (объектная модель компонента)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-179">**COM (Component Object Model)**</span></span>

<span data-ttu-id="88d5b-180">Двоичный стандарт, который позволяет объектам взаимодействовать в сетевой среде независимо от языка, в котором они были разработаны или компьютеров, на которых они находятся.</span><span class="sxs-lookup"><span data-stu-id="88d5b-180">A binary standard that enables objects to interoperate in a networked environment regardless of the language in which they were developed or on which computers they reside.</span></span> <span data-ttu-id="88d5b-181">Технологии COM-включать элементы управления ActiveX, автоматизации и объект связывание и внедрение объектов (OLE).</span><span class="sxs-lookup"><span data-stu-id="88d5b-181">COM-based technologies include ActiveX Controls, Automation, and object linking and embedding (OLE).</span></span> <span data-ttu-id="88d5b-182">COM позволяет объекту предоставлять его функциональность другим компонентам и ведущие приложения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-182">COM allows an object to expose its functionality to other components and to host applications.</span></span> <span data-ttu-id="88d5b-183">Определяется как объект предоставляет самого и принципы работы этого воздействия процессов и по сетям.</span><span class="sxs-lookup"><span data-stu-id="88d5b-183">It defines both how the object exposes itself and how this exposure works across processes and across networks.</span></span> <span data-ttu-id="88d5b-184">COM также определяет объект жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="88d5b-184">COM also defines the object's life cycle.</span></span>

<span data-ttu-id="88d5b-185">**COM-компонент**</span><span class="sxs-lookup"><span data-stu-id="88d5b-185">**COM component**</span></span>

<span data-ttu-id="88d5b-186">Двоичный файл, такие как библиотеки DLL, соответствующий и некоторые файлы .exe —, который поддерживает стандарт COM для создания объектов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-186">Binary file — such as .dll, .ocx, and some .exe files — that supports the COM standard for providing objects.</span></span> <span data-ttu-id="88d5b-187">Этот файл содержит код для одного или нескольких фабрики классов, COM-классов, механизмов записи реестра, загрузки кода и т. д.</span><span class="sxs-lookup"><span data-stu-id="88d5b-187">Such a file contains code for one or more class factories, COM classes, registry-entry mechanisms, loading code, and so on.</span></span>

<span data-ttu-id="88d5b-188">**оператор сравнения**</span><span class="sxs-lookup"><span data-stu-id="88d5b-188">**comparison operator**</span></span>

<span data-ttu-id="88d5b-189">Оператор, который сравнивает два выражения и возвращает значение типа Boolean.</span><span class="sxs-lookup"><span data-stu-id="88d5b-189">An operator that compares two expressions and returns a Boolean value.</span></span>

<span data-ttu-id="88d5b-190">Условия, которые могут быть выражены как "\>«(больше),»\<«(меньше), «=» (равно),»\>=» (больше или равно),"\<=» (меньше или равно), "\<\>" (не равно) или «как и» (подстановочные знаки).</span><span class="sxs-lookup"><span data-stu-id="88d5b-190">A criteria parameter that may be expressed as "\>" (greater than), "\<" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="88d5b-191">**компонент**</span><span class="sxs-lookup"><span data-stu-id="88d5b-191">**component**</span></span>

<span data-ttu-id="88d5b-192">Объект, который инкапсулирует данные и код, а также хорошо указанный набор общедоступных служб.</span><span class="sxs-lookup"><span data-stu-id="88d5b-192">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

<span data-ttu-id="88d5b-193">**составной файл**</span><span class="sxs-lookup"><span data-stu-id="88d5b-193">**compound file**</span></span>

<span data-ttu-id="88d5b-194">Реализация COM структура хранилища файлов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-194">An implementation of COM structured storage for files.</span></span> <span data-ttu-id="88d5b-195">Составной файл сохраняет отдельные объекты в один структурированный файл, состоящий из двух основных элементов: хранилище объектов и объектов потока.</span><span class="sxs-lookup"><span data-stu-id="88d5b-195">A compound file stores separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="88d5b-196">Друг с другом они работают как в файловой системе в пределах файла.</span><span class="sxs-lookup"><span data-stu-id="88d5b-196">Together, they function like a file system within a file.</span></span> <span data-ttu-id="88d5b-197">Для получения дополнительных сведений см. составные файлы в пакете SDK платформы Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88d5b-197">For more information, see Compound Files in the Microsoft Platform SDK.</span></span>

<span data-ttu-id="88d5b-198">Количество отдельных файлов, связанных одного физического файла.</span><span class="sxs-lookup"><span data-stu-id="88d5b-198">A number of individual files bound together in one physical file.</span></span> <span data-ttu-id="88d5b-199">Можно получить доступ к каждого файла в составном файле, как если бы одного физического файла.</span><span class="sxs-lookup"><span data-stu-id="88d5b-199">Each individual file in a compound file can be accessed as if it were a single physical file.</span></span>

<span data-ttu-id="88d5b-200">**константы**</span><span class="sxs-lookup"><span data-stu-id="88d5b-200">**constant**</span></span>

<span data-ttu-id="88d5b-201">Числовое или строковое значение, которое не изменяется.</span><span class="sxs-lookup"><span data-stu-id="88d5b-201">A numeric or string value that does not change.</span></span> <span data-ttu-id="88d5b-202">Именованные ADO перечисления (перечисляемые константы) можно использовать в коде вместо фактических значений, например, **adUseClient** — это константа, значение которого равно 3.</span><span class="sxs-lookup"><span data-stu-id="88d5b-202">Named ADO enumerations (enumerated constants) can be used in your code instead of actual values, for example, **adUseClient** is a constant whose value is 3.</span></span> <span data-ttu-id="88d5b-203">(Const adUseClient = 3).</span><span class="sxs-lookup"><span data-stu-id="88d5b-203">(Const adUseClient = 3).</span></span> <span data-ttu-id="88d5b-204">В разделе также **перечисления**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-204">See also **enumeration**.</span></span>

<span data-ttu-id="88d5b-205">**cursor (указатель)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-205">**cursor**</span></span>

<span data-ttu-id="88d5b-206">Элемент базы данных, который управляет перехода по записям, обновлению данных и видимости изменений, внесенных в базу данных другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="88d5b-206">A database element that controls record navigation, updateability of data, and the visibility of changes made to the database by other users.</span></span>

<span data-ttu-id="88d5b-207">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-207">Return to top</span></span>

## <a name="d"></a><span data-ttu-id="88d5b-208">D</span><span class="sxs-lookup"><span data-stu-id="88d5b-208">D</span></span>

<span data-ttu-id="88d5b-209">**Привязка данных**</span><span class="sxs-lookup"><span data-stu-id="88d5b-209">**data binding**</span></span>

<span data-ttu-id="88d5b-210">Процесс привязки объекты и элементы управления приложения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-210">The process of associating the objects or controls of an application to a data source.</span></span> <span data-ttu-id="88d5b-211">Элемент управления, связанный с источником данных называется элемент *управления с привязкой к данным*.</span><span class="sxs-lookup"><span data-stu-id="88d5b-211">A control associated with a data source is called a *data-bound control*.</span></span>

<span data-ttu-id="88d5b-212">Содержимое элемента управления с привязкой к данным связаны со значениями из базы данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-212">The contents of a data-bound control are associated with values from a database.</span></span> <span data-ttu-id="88d5b-213">Например элемент управления сетки, связанный с объектом **набора записей** можно обновить при обновлении строк в **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-213">For example, a grid control that is bound to a **Recordset** object can be updated when the rows in the **Recordset** are updated.</span></span> <span data-ttu-id="88d5b-214">Если новые значения получаются путем **набора записей**, новые значения отображаются в сетке.</span><span class="sxs-lookup"><span data-stu-id="88d5b-214">When new values are retrieved by the **Recordset**, new values are displayed in the grid.</span></span>

<span data-ttu-id="88d5b-215">**Поставщик данных**</span><span class="sxs-lookup"><span data-stu-id="88d5b-215">**data provider**</span></span>

<span data-ttu-id="88d5b-216">Программное обеспечение, которое предоставляет доступ к данным в приложение ADO напрямую или через поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="88d5b-216">Software that exposes data to an ADO application either directly or via a service provider.</span></span> <span data-ttu-id="88d5b-217">Смотрите также **поставщика услуг**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-217">See also **service provider**.</span></span>

<span data-ttu-id="88d5b-218">**формирования данных**</span><span class="sxs-lookup"><span data-stu-id="88d5b-218">**data shaping**</span></span>

<span data-ttu-id="88d5b-219">Метод, использующий Формализованная синтаксис (называемые **фигуры язык**) для определения специализированных объекта **набора записей** (называемые **форме записей**), который содержит не только данные, но также ссылается на другие объекты **набора записей** и / или вычисляемые значения на основе этих других объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-219">A technique which makes use of a formalized syntax (called **Shape language**) to define a specialized **Recordset** object (called a **shaped Recordset**) that contains not just data, but also references to other **Recordset** objects and/or computed values based on those other **Recordset** objects.</span></span>

<span data-ttu-id="88d5b-220">**уровень источника данных**</span><span class="sxs-lookup"><span data-stu-id="88d5b-220">**data source tier**</span></span>

<span data-ttu-id="88d5b-221">Логический слой распределенных систем, который представляет компьютера под управлением СУБД, например базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88d5b-221">A logical layer of a distributed system that represents a computer running a DBMS, such as an SQL Server database.</span></span> <span data-ttu-id="88d5b-222">Смотрите также **уровня клиента**, **Средний уровень**, **распределенных приложений**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-222">See also **client tier**, **middle tier**, **distributed application**.</span></span>

<span data-ttu-id="88d5b-223">**DCOM**</span><span class="sxs-lookup"><span data-stu-id="88d5b-223">**DCOM**</span></span>

<span data-ttu-id="88d5b-224">Протокол связи, позволяющий COM-компонентов для взаимодействия напрямую друг с другом по сети.</span><span class="sxs-lookup"><span data-stu-id="88d5b-224">A wire protocol that enables COM components to communicate directly with each other across a network.</span></span> <span data-ttu-id="88d5b-225">В разделе также **COM**, **компонент**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-225">See also **COM**, **component**.</span></span>

<span data-ttu-id="88d5b-226">**DDL (язык описания данных)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-226">**DDL (Data Definition Language)**</span></span>

<span data-ttu-id="88d5b-227">Эти инструкции в SQL, которые определяют, в отличие от работы с данными.</span><span class="sxs-lookup"><span data-stu-id="88d5b-227">Those statements in SQL that define, as opposed to manipulate, data.</span></span> <span data-ttu-id="88d5b-228">Схема базы данных при создании или изменении с DDL.</span><span class="sxs-lookup"><span data-stu-id="88d5b-228">The schema of a database is created or modified with DDL.</span></span> <span data-ttu-id="88d5b-229">К примеру **CREATE TABLE**, **CREATE INDEX**, **Предоставление**и **ОТЗЫВ** , инструкции SQL DDL.</span><span class="sxs-lookup"><span data-stu-id="88d5b-229">For example, **CREATE TABLE**, **CREATE INDEX**, **GRANT**, and **REVOKE** are SQL DDL statements.</span></span>

<span data-ttu-id="88d5b-230">**поток по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="88d5b-230">**default stream**</span></span>

<span data-ttu-id="88d5b-231">Текст или двоичный поток (представленный объектом **потока** ), который связан с объектами **записи** или **набора записей** при использовании некоторых поставщики OLE DB, такие как поставщик Microsoft OLE DB для публикации Интернет.</span><span class="sxs-lookup"><span data-stu-id="88d5b-231">A text or binary stream (represented by a **Stream** object) that is associated with **Record** or **Recordset** objects when using certain OLE DB providers, such as the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="88d5b-232">Поток по умолчанию обычно содержит содержимое файла, такие как HTML-код для корневого веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="88d5b-232">The default stream typically contains the contents of a file such as the HTML code for the root of a website.</span></span>

<span data-ttu-id="88d5b-233">**распределенные приложения**</span><span class="sxs-lookup"><span data-stu-id="88d5b-233">**distributed application**</span></span>

<span data-ttu-id="88d5b-234">Программа, написанная, чтобы обработка можно разделить на нескольких компьютерах в сети.</span><span class="sxs-lookup"><span data-stu-id="88d5b-234">A program written so that the processing can be divided across multiple computers over a network.</span></span> <span data-ttu-id="88d5b-235">Как правило распределенных приложений состоит из презентации, бизнес-логики и уровни хранилища данных или *уровней*.</span><span class="sxs-lookup"><span data-stu-id="88d5b-235">Typically, a distributed application is divided into presentation, business logic, and data store layers, or *tiers*.</span></span> <span data-ttu-id="88d5b-236">Смотрите также **уровня клиента**, **Средний уровень**, **уровень источника данных**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-236">See also **client tier**, **middle tier**, **data source tier**.</span></span>

<span data-ttu-id="88d5b-237">**отключенный набор записей**</span><span class="sxs-lookup"><span data-stu-id="88d5b-237">**disconnected Recordset**</span></span>

<span data-ttu-id="88d5b-238">Объект **набора записей** в клиентском кэше, которое больше нет live подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="88d5b-238">A **Recordset** object in a client cache that no longer has a live connection to the server.</span></span> <span data-ttu-id="88d5b-239">Если исходный источник данных требуется предоставить доступ для какой-либо причине, такие как обновление данных, подключение необходимо быть восстановлены.</span><span class="sxs-lookup"><span data-stu-id="88d5b-239">If the original data source needs to be accessed again for some reason, such as updating data, the connection must be re-established.</span></span> <span data-ttu-id="88d5b-240">Тем не менее семейства сайтов, свойства и методы отключенного **набора записей** по-прежнему доступны.</span><span class="sxs-lookup"><span data-stu-id="88d5b-240">However, the collections, properties, and methods of a disconnected **Recordset** can still be accessed.</span></span>

<span data-ttu-id="88d5b-241">**DLL (библиотека динамической компоновки)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-241">**DLL (dynamic-link library)**</span></span>

<span data-ttu-id="88d5b-242">Файл, содержащий одну или несколько функций, которые компилируются, связанные и храниться отдельно от процессами, их использования.</span><span class="sxs-lookup"><span data-stu-id="88d5b-242">A file that contains one or more functions that are compiled, linked, and stored separately from the processes that use them.</span></span> <span data-ttu-id="88d5b-243">Операционная система сопоставляет библиотеки DLL в адресное пространство вызывающего процесса при запуске процесса или во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-243">The operating system maps the DLLs into the address space of the calling process when the process is starting, or while it is running.</span></span>

<span data-ttu-id="88d5b-244">**DML (языка обработки данных)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-244">**DML (Data Manipulation Language)**</span></span>

<span data-ttu-id="88d5b-245">Эти инструкции в SQL, работа с элементами управления, а не для определения данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-245">Those statements in SQL that manipulate, as opposed to define, data.</span></span> <span data-ttu-id="88d5b-246">Значения в базе данных выбраны и изменить с помощью DML.</span><span class="sxs-lookup"><span data-stu-id="88d5b-246">The values in a database are selected and modified with DML.</span></span> <span data-ttu-id="88d5b-247">Например **Вставка**, **обновление**, **Удаление**и **ВЫБЕРИТЕ** , инструкции SQL DML.</span><span class="sxs-lookup"><span data-stu-id="88d5b-247">For example, **INSERT**, **UPDATE**, **DELETE**, and **SELECT** are SQL DML statements.</span></span>

<span data-ttu-id="88d5b-248">**Поставщик источника документов**</span><span class="sxs-lookup"><span data-stu-id="88d5b-248">**document source provider**</span></span>

<span data-ttu-id="88d5b-249">Специальный класс поставщиков, которыми управляют папки и документы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-249">A special class of providers that manage folders and documents.</span></span> <span data-ttu-id="88d5b-250">Когда документ представлен объектом **записи** или папки документов, представленное объектом **набора записей** , поставщик источника документов заполняет объектам с уникальный набор полей, описывающих характеристики документов вместо фактических документа самого.</span><span class="sxs-lookup"><span data-stu-id="88d5b-250">When a document is represented by a **Record** object, or a folder of documents is represented by a **Recordset** object, the document source provider populates those objects with a unique set of fields that describe characteristics of the document, instead of the actual document itself.</span></span> <span data-ttu-id="88d5b-251">Просмотрите **записи ресурса**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-251">See also **resource record**.</span></span>

<span data-ttu-id="88d5b-252">**Уведомления о Доставке (имя источника данных)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-252">**DSN (data source name)**</span></span>

<span data-ttu-id="88d5b-253">Коллекция сведения, используемые для подключения приложения к определенной базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="88d5b-253">The collection of information used to connect your application to a particular ODBC database.</span></span> <span data-ttu-id="88d5b-254">Драйвера ODBC использует эти сведения для создания подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-254">The ODBC Driver Manager uses this information to create a connection to the database.</span></span> <span data-ttu-id="88d5b-255">Имя источника данных могут храниться в файл (DSN) или в реестре Windows (компьютер DSN).</span><span class="sxs-lookup"><span data-stu-id="88d5b-255">A DSN can be stored in a file (a file DSN) or in the Windows Registry (a machine DSN).</span></span>

<span data-ttu-id="88d5b-256">**динамические свойства**</span><span class="sxs-lookup"><span data-stu-id="88d5b-256">**dynamic property**</span></span>

<span data-ttu-id="88d5b-257">Свойства, относящиеся к поставщику данных или службы курсора.</span><span class="sxs-lookup"><span data-stu-id="88d5b-257">A property specific to a data provider or the cursor service.</span></span> <span data-ttu-id="88d5b-258">Коллекция **свойств** объекта автоматически заполняется с этими («динамически»).</span><span class="sxs-lookup"><span data-stu-id="88d5b-258">The **Properties** collection of an object is populated with these automatically ("dynamically").</span></span> <span data-ttu-id="88d5b-259">Объект не имеет динамических свойств только после подключения к источнику данных через поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-259">An object has no dynamic properties until it is connected to a data source through a particular data provider.</span></span> <span data-ttu-id="88d5b-260">Смотрите также **Поставщик данных**, **курсора**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-260">See also **data provider**, **cursor**.</span></span>

<span data-ttu-id="88d5b-261">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-261">Return to top</span></span>

## <a name="e-i"></a><span data-ttu-id="88d5b-262">E-I</span><span class="sxs-lookup"><span data-stu-id="88d5b-262">E-I</span></span>

<span data-ttu-id="88d5b-263">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="88d5b-263">**enumeration**</span></span>

<span data-ttu-id="88d5b-264">Список именованных констант.</span><span class="sxs-lookup"><span data-stu-id="88d5b-264">A list of named constants.</span></span> <span data-ttu-id="88d5b-265">Перечисляемые значения не должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="88d5b-265">Enumerated values need not be unique.</span></span> <span data-ttu-id="88d5b-266">Тем не менее имя каждое значение должно быть уникальным в пределах области, где перечисления задан.</span><span class="sxs-lookup"><span data-stu-id="88d5b-266">However the name of each value must be unique within the scope where the enumeration is defined.</span></span> <span data-ttu-id="88d5b-267">В ADO перечисления, используемые для числовой параметр и возвращаемые значения для добавления значение для кода, ADO и защищают разработчиков от числовых значений (которые может меняться от версии на другую).</span><span class="sxs-lookup"><span data-stu-id="88d5b-267">In ADO, enumerations are used for numeric parameter and return values, to add meaning to ADO code and to shield the developer from the numeric values (which may change from version to version).</span></span> <span data-ttu-id="88d5b-268">Например чтобы открыть статического **набора записей**, используйте **adOpenStatic** значение перечисления:</span><span class="sxs-lookup"><span data-stu-id="88d5b-268">For example, to open a static **Recordset**, use the **adOpenStatic** enumerated value:</span></span>  
  

<span data-ttu-id="88d5b-269">Также называют *перечисляемой константы*.</span><span class="sxs-lookup"><span data-stu-id="88d5b-269">Also referred to as *enumerated constant*.</span></span> <span data-ttu-id="88d5b-270">В разделе также **константу**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-270">See also **constant**.</span></span>

<span data-ttu-id="88d5b-271">**событие**</span><span class="sxs-lookup"><span data-stu-id="88d5b-271">**event**</span></span>

<span data-ttu-id="88d5b-272">Действие, распознаваемое объектом, для которого можно написать код для ответа.</span><span class="sxs-lookup"><span data-stu-id="88d5b-272">An action recognized by an object, for which you can write code to respond.</span></span> <span data-ttu-id="88d5b-273">События возникают в результате выполнения команды, выполнения транзакции, записей и обновления данных, среди других действий.</span><span class="sxs-lookup"><span data-stu-id="88d5b-273">Events can be generated by command execution, transaction completion, recordset navigation, and data updates, among other actions.</span></span> <span data-ttu-id="88d5b-274">В разделе также **обработчик событий**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-274">See also **event handler**.</span></span>

<span data-ttu-id="88d5b-275">**обработчик событий**</span><span class="sxs-lookup"><span data-stu-id="88d5b-275">**event handler**</span></span>

<span data-ttu-id="88d5b-276">Обработчик событий — код, который выполняется при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="88d5b-276">An event handler is the code that is executed when an event occurs.</span></span> <span data-ttu-id="88d5b-277">Просмотрите **события**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-277">See also **event**.</span></span>

<span data-ttu-id="88d5b-278">**handler**</span><span class="sxs-lookup"><span data-stu-id="88d5b-278">**handler**</span></span>

<span data-ttu-id="88d5b-279">Процедуры, который управляет общие и сравнительно легко условие или операции, такие как управление восстановления или данных об ошибках.</span><span class="sxs-lookup"><span data-stu-id="88d5b-279">A routine that manages a common and relatively simple condition or operation, such as error recovery or data management.</span></span>

<span data-ttu-id="88d5b-280">**Иерархическая записей**</span><span class="sxs-lookup"><span data-stu-id="88d5b-280">**hierarchical Recordset**</span></span>

<span data-ttu-id="88d5b-281">**Набор записей** , содержащий другого **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-281">A **Recordset** that contains another **Recordset**.</span></span> <span data-ttu-id="88d5b-282">В разделе также **формирования данных**, **главы**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-282">See also **data shaping**, **chapter**.</span></span>

<span data-ttu-id="88d5b-283">Для получения дополнительных сведений см. [Доступ к строк в иерархической записей](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="88d5b-283">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)</span></span>

<span data-ttu-id="88d5b-284">**Иерархия**</span><span class="sxs-lookup"><span data-stu-id="88d5b-284">**hierarchy**</span></span>

<span data-ttu-id="88d5b-285">В общем случае иерархия является ранжированных структура с сверху на уровне и подчиненные уровни.</span><span class="sxs-lookup"><span data-stu-id="88d5b-285">In general, a hierarchy is a ranked structure with a top level and subordinate levels.</span></span> <span data-ttu-id="88d5b-286">В ADO иерархические **наборы записей** используются для представления отношения родительских и дочерних между записи и главу.</span><span class="sxs-lookup"><span data-stu-id="88d5b-286">In ADO, hierarchical **Recordsets** are used to represent the parent-child relationship between a record and a chapter.</span></span> <span data-ttu-id="88d5b-287">Также в ADO, **записи** и **поток** объектов можно использовать для доступа к структурам иерархическую древовидную, таких как папки и документы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-287">Also in ADO, **Record** and **Stream** objects can be used to access hierarchical tree structures such as a folder and documents.</span></span> <span data-ttu-id="88d5b-288">ADO MD также включает в себя **Иерархия** объектов для представления отношения между уровнями измерения куба OLAP.</span><span class="sxs-lookup"><span data-stu-id="88d5b-288">ADO MD also includes **Hierarchy** objects to represent a relationship between the levels of a dimension in an OLAP cube.</span></span> <span data-ttu-id="88d5b-289">В разделе также **иерархические наборы записей**, **отношения родительских и дочерних**, **главы**, **дерева**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-289">See also **hierarchical Recordsets**, **parent-child relationship**, **chapter**, **tree**.</span></span>

<span data-ttu-id="88d5b-290">**ISAPI (Internet Server прикладной программный интерфейс)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-290">**ISAPI (Internet Server Application Programming Interface)**</span></span>

<span data-ttu-id="88d5b-291">Набор функций для серверов Интернета, например, Windows NT Server и Windows 2000 сервер под управлением Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="88d5b-291">A set of functions for Internet servers, such as a Windows NT Server/Windows 2000 Server running Microsoft Internet Information Services (IIS).</span></span>

<span data-ttu-id="88d5b-292">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-292">Return to top</span></span>

## <a name="k-m"></a><span data-ttu-id="88d5b-293">K-M</span><span class="sxs-lookup"><span data-stu-id="88d5b-293">K-M</span></span>

<span data-ttu-id="88d5b-294">**ключ**</span><span class="sxs-lookup"><span data-stu-id="88d5b-294">**key**</span></span>

<span data-ttu-id="88d5b-295">Столбец или столбцы в таблице, которые однозначно идентифицируют строку. часто используется для индексирования таблицы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-295">A column or columns in a table that uniquely identify a row; often used to index a table.</span></span>

<span data-ttu-id="88d5b-296">**маршалинга**</span><span class="sxs-lookup"><span data-stu-id="88d5b-296">**marshaling**</span></span>

<span data-ttu-id="88d5b-297">Процесс упаковки, отправляющим и распаковки параметры метода интерфейса пределы потока или процесса.</span><span class="sxs-lookup"><span data-stu-id="88d5b-297">The process of packaging, sending, and unpackaging interface method parameters across thread or process boundaries.</span></span>

<span data-ttu-id="88d5b-298">**Средний уровень**</span><span class="sxs-lookup"><span data-stu-id="88d5b-298">**middle tier**</span></span>

<span data-ttu-id="88d5b-299">Логический уровень в распределенных систем между пользовательского интерфейса или веб-клиента и базы данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-299">The logical layer in a distributed system between a user interface or web client and the database.</span></span> <span data-ttu-id="88d5b-300">Обычно это, где создаются бизнес-объектов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-300">This is typically where business objects are instantiated.</span></span> <span data-ttu-id="88d5b-301">Средний уровень — это набор бизнес-правил и функции, создать и использовать при получении сведений.</span><span class="sxs-lookup"><span data-stu-id="88d5b-301">The middle tier is a collection of business rules and functions that generate and operate upon receiving information.</span></span> <span data-ttu-id="88d5b-302">Они выполняют через бизнес-правил, которые часто можно изменить и таким образом, инкапсулируются в компоненты, которые могут физически отдельно от самого логики приложения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-302">They accomplish this through business rules, which can change frequently, and are thus encapsulated into components that are physically separate from the application logic itself.</span></span> <span data-ttu-id="88d5b-303">Также известной как *на уровне сервера приложений*.</span><span class="sxs-lookup"><span data-stu-id="88d5b-303">Also known as *application server tier*.</span></span> <span data-ttu-id="88d5b-304">См. также **распределенные приложения**, **уровня клиента**, **уровень источника данных**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-304">See also **distributed application**, **client tier**, **data source tier**.</span></span>

<span data-ttu-id="88d5b-305">**MIME (расширение почты Интернета несколькими назначения)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-305">**MIME (Multi-purpose Internet Mail Extension)**</span></span>

<span data-ttu-id="88d5b-306">Протокол Интернета, изначально разработанного разрешить обмен сообщениями электронной почты с Форматированный контент в разнородных сети, машины и среды электронной почты.</span><span class="sxs-lookup"><span data-stu-id="88d5b-306">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, machine, and email environments.</span></span> <span data-ttu-id="88d5b-307">На практике MIME также был частичного или полного перевода и расширить, кроме почтовых приложений.</span><span class="sxs-lookup"><span data-stu-id="88d5b-307">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

<span data-ttu-id="88d5b-308">MIME — это стандарт, обеспечивающий двоичных данных для публикации и чтение в Интернете.</span><span class="sxs-lookup"><span data-stu-id="88d5b-308">MIME is a standard that allows binary data to be published and read on the Internet.</span></span> <span data-ttu-id="88d5b-309">Заголовок файла с помощью двоичных данных содержит тип MIME данных. Эта информация указывает клиентских программ (веб-браузеры и пакеты почты, например) может применяться для обработки данных по-другому, чем они обработать открытого текста.</span><span class="sxs-lookup"><span data-stu-id="88d5b-309">The header of a file with binary data contains the MIME type of the data; this informs client programs (web browsers and mail packages, for instance) that they will need to handle the data in a different way than they handle straight text.</span></span> <span data-ttu-id="88d5b-310">Например заголовок веб-документ, содержащий изображения JPEG содержит тип MIME, определенных в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="88d5b-310">For example, the header of a web document containing a JPEG graphic contains the MIME type specific to the JPEG file format.</span></span> <span data-ttu-id="88d5b-311">Это позволяет браузера для отображения файла с помощью средства просмотра его JPEG, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="88d5b-311">This allows a browser to display the file with its JPEG viewer, if one is present.</span></span>

<span data-ttu-id="88d5b-312">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-312">Return to top</span></span>

## <a name="n-o"></a><span data-ttu-id="88d5b-313">N-O</span><span class="sxs-lookup"><span data-stu-id="88d5b-313">N-O</span></span>

<span data-ttu-id="88d5b-314">**node**</span><span class="sxs-lookup"><span data-stu-id="88d5b-314">**node**</span></span>

<span data-ttu-id="88d5b-315">Элемент в иерархическую древовидную структуру.</span><span class="sxs-lookup"><span data-stu-id="88d5b-315">An element in a hierarchical tree structure.</span></span> <span data-ttu-id="88d5b-316">Узел может быть корневой или дочерние еще одного узла.</span><span class="sxs-lookup"><span data-stu-id="88d5b-316">A node may be the root, or the child of another node.</span></span> <span data-ttu-id="88d5b-317">Узел также может быть родительской несколько дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-317">A node can also be the parent of multiple children.</span></span> <span data-ttu-id="88d5b-318">См в разделе также **иерархии**, **дерева**, **корневой**, **дочерние** **parent**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-318">See also **hierarchy**, **tree**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="88d5b-319">**объектная переменная**</span><span class="sxs-lookup"><span data-stu-id="88d5b-319">**object variable**</span></span>

<span data-ttu-id="88d5b-320">Переменная, содержащая ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="88d5b-320">A variable that contains a reference to an object.</span></span> <span data-ttu-id="88d5b-321">Например objCustomObject — это переменная, которая указывает на объект типа CustomObject:</span><span class="sxs-lookup"><span data-stu-id="88d5b-321">For example, objCustomObject is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="88d5b-322">— это переменная, которая указывает на объект типа CustomObject:</span><span class="sxs-lookup"><span data-stu-id="88d5b-322">is a variable that points to an object of type CustomObject:</span></span>  
  
<span data-ttu-id="88d5b-323">Задать objCustomObject = CreateObject (adodb. Набор записей)</span><span class="sxs-lookup"><span data-stu-id="88d5b-323">Set objCustomObject = CreateObject(adodb.Recordset)</span></span>

<span data-ttu-id="88d5b-324">**ODBC (Open Database Connectivity)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-324">**ODBC (Open Database Connectivity)**</span></span>

<span data-ttu-id="88d5b-325">Это стандартный язык интерфейс программирования для подключения к различным источникам данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-325">A standard programming language interface used to connect to a variety of data sources.</span></span> <span data-ttu-id="88d5b-326">Обычно это осуществляется с помощью панели управления, где можно назначить имена источников данных (DSN) для использования определенных драйверов ODBC.</span><span class="sxs-lookup"><span data-stu-id="88d5b-326">This is usually accessed through Control Panel, where data source names (DSNs) can be assigned to use specific ODBC drivers.</span></span>

<span data-ttu-id="88d5b-327">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="88d5b-327">**OLE DB**</span></span>

<span data-ttu-id="88d5b-328">Набор интерфейсов, которые предоставляют доступ к данным из различных источников использования COM.</span><span class="sxs-lookup"><span data-stu-id="88d5b-328">A set of interfaces that expose data from a variety of sources using COM.</span></span> <span data-ttu-id="88d5b-329">Интерфейсы OLE DB предоставляют приложений с помощью единообразный доступ к данным, хранящимся в различным источникам данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-329">OLE DB interfaces provide applications with uniform access to data stored in diverse information sources.</span></span> <span data-ttu-id="88d5b-330">Эти интерфейсы поддерживают объем функциональные возможности СУБД, соответствующий источнику данных, что позволяет совместно использовать данные.</span><span class="sxs-lookup"><span data-stu-id="88d5b-330">These interfaces support the amount of DBMS functionality appropriate to the data source, enabling it to share its data.</span></span> <span data-ttu-id="88d5b-331">Смотрите также **COM**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-331">See also **COM**.</span></span>

<span data-ttu-id="88d5b-332">**оптимистичный блокировки**</span><span class="sxs-lookup"><span data-stu-id="88d5b-332">**optimistic locking**</span></span>

<span data-ttu-id="88d5b-333">Тип блокировки, в которой — страница данных, содержащий одну или несколько записей, включая запись, становится недоступной для других пользователей только в том случае, когда запись обновляется с помощью метода **Update** , но недоступны до и после вызова **обновления** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-333">A type of locking in which the data page containing one or more records, including the record being edited, is unavailable to other users only while the record is being updated by the **Update** method, but is available before and after the call to **Update**.</span></span>

<span data-ttu-id="88d5b-334">Оптимистичный блокировка используется при открытии объекта **набора записей** с **LockType для** параметра или свойство, значение **adLockOptimistic** или **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-334">Optimistic locking is used when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockOptimistic** or **adLockBatchOptimistic**.</span></span> <span data-ttu-id="88d5b-335">В разделе также **жесткой блокировки**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-335">See also **pessimistic locking**.</span></span>

<span data-ttu-id="88d5b-336">**Порядковый номер**</span><span class="sxs-lookup"><span data-stu-id="88d5b-336">**ordinal value**</span></span>

<span data-ttu-id="88d5b-337">Числовой расположение элемента в порядке.</span><span class="sxs-lookup"><span data-stu-id="88d5b-337">The numeric location of an item within an order.</span></span> <span data-ttu-id="88d5b-338">В коллекции ADO порядковый номер первого элемента равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="88d5b-338">In an ADO collection, the ordinal value of the first item is zero (0).</span></span> <span data-ttu-id="88d5b-339">Следующий элемент имеет один (1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="88d5b-339">The next item is one (1), and so on.</span></span>

<span data-ttu-id="88d5b-340">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-340">Return to top</span></span>

## <a name="p"></a><span data-ttu-id="88d5b-341">P</span><span class="sxs-lookup"><span data-stu-id="88d5b-341">P</span></span>

<span data-ttu-id="88d5b-342">**параметризованные команды**</span><span class="sxs-lookup"><span data-stu-id="88d5b-342">**parameterized command**</span></span>

<span data-ttu-id="88d5b-343">Запрос или команду, которая позволяет задать значения параметров перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="88d5b-343">A query or command that allows you to set parameter values before the command is executed.</span></span> <span data-ttu-id="88d5b-344">Например, строка SQL задаются путем внедрения маркеры параметров в строке SQL (обозначенного "?" символ).</span><span class="sxs-lookup"><span data-stu-id="88d5b-344">For example, a SQL string can be parameterized by embedding parameter markers in the SQL string (designated by the '?' character).</span></span> <span data-ttu-id="88d5b-345">Затем приложение задает значения для каждого параметра и выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="88d5b-345">The application then specifies values for each parameter and executes the command.</span></span>

<span data-ttu-id="88d5b-346">**родительский**</span><span class="sxs-lookup"><span data-stu-id="88d5b-346">**parent**</span></span>

<span data-ttu-id="88d5b-347">Управление сторона иерархическую связь.</span><span class="sxs-lookup"><span data-stu-id="88d5b-347">The controlling side of a hierarchical relationship.</span></span> <span data-ttu-id="88d5b-348">В иерархической структуры родительский объект имеет один или несколько дочерних узлов непосредственно под ним в иерархии.</span><span class="sxs-lookup"><span data-stu-id="88d5b-348">In a hierarchical structure, a parent has one or more child nodes directly beneath it in the hierarchy.</span></span> <span data-ttu-id="88d5b-349">Смотрите также **родительский псевдоним**, **отношения родительских и дочерних**, **дочерние**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-349">See also **parent-alias**, **parent-child relationship**, **child**.</span></span>

<span data-ttu-id="88d5b-350">**родительский псевдоним**</span><span class="sxs-lookup"><span data-stu-id="88d5b-350">**parent-alias**</span></span>

<span data-ttu-id="88d5b-351">Псевдоним, который относится к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="88d5b-351">An alias that refers to the parent.</span></span> <span data-ttu-id="88d5b-352">В разделе также **псевдоним**, **parent**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-352">See also **alias**, **parent**.</span></span>

<span data-ttu-id="88d5b-353">**отношения родительских и дочерних**</span><span class="sxs-lookup"><span data-stu-id="88d5b-353">**parent-child relationship**</span></span>

<span data-ttu-id="88d5b-354">Отношения в иерархической структуры, в котором родительский объект на один уровень выше и напрямую, связанные с один или несколько дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-354">A relationship in a hierarchical structure in which the parent is one level higher and directly associated with one or more children.</span></span> <span data-ttu-id="88d5b-355">Дочерний является уровня и должен иметь один родительский.</span><span class="sxs-lookup"><span data-stu-id="88d5b-355">A child is one level lower and must have one parent.</span></span> <span data-ttu-id="88d5b-356">В разделе также **родительских**, **дочерних**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-356">See also **parent**, **child**.</span></span>

<span data-ttu-id="88d5b-357">**Сохранение**</span><span class="sxs-lookup"><span data-stu-id="88d5b-357">**persist**</span></span>

<span data-ttu-id="88d5b-358">Для сохранения данных в постоянное состоянии, например сохранения **записей** в файл.</span><span class="sxs-lookup"><span data-stu-id="88d5b-358">To save data in a permanent state, such as saving a **Recordset** to a file.</span></span>

<span data-ttu-id="88d5b-359">**жесткой блокировки**</span><span class="sxs-lookup"><span data-stu-id="88d5b-359">**pessimistic locking**</span></span>

<span data-ttu-id="88d5b-360">Тип блокировки, в котором на этой странице содержится один или несколько записей, включая запись, становится недоступной для других пользователей, чтобы убедиться, что будет выполнено обновление.</span><span class="sxs-lookup"><span data-stu-id="88d5b-360">A type of locking in which the page containing one or more records, including the record being edited, is unavailable to other users to ensure that an update will be made.</span></span> <span data-ttu-id="88d5b-361">Жесткой блокировки поведение определяется поставщик OLE DB.</span><span class="sxs-lookup"><span data-stu-id="88d5b-361">Pessimistic locking behavior is defined by the OLE DB provider.</span></span> <span data-ttu-id="88d5b-362">Как правило записи блокируется при изменении и останутся недоступными до завершения метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-362">Typically, records are locked upon editing and remain unavailable until the **Update** method has completed.</span></span>

<span data-ttu-id="88d5b-363">Жесткой блокировка включена при открытии объекта **набора записей** с **LockType для** параметра или набора **adLockPessimistic**свойств.</span><span class="sxs-lookup"><span data-stu-id="88d5b-363">Pessimistic locking is enabled when the **Recordset** object is opened with the **LockType** parameter or property set to **adLockPessimistic**.</span></span> <span data-ttu-id="88d5b-364">В разделе также **оптимистичный блокировки**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-364">See also **optimistic locking**.</span></span>

<span data-ttu-id="88d5b-365">**пул**</span><span class="sxs-lookup"><span data-stu-id="88d5b-365">**pooling**</span></span>

<span data-ttu-id="88d5b-366">Оптимизация производительности, основанная на использовании наборов предварительно выделенных ресурсов, таких как объекты или подключения к базам данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-366">A performance optimization based on using collections of pre-allocated resources, such as objects or database connections.</span></span> <span data-ttu-id="88d5b-367">Целесообразно извлечение существующего ресурса из пула, чем создание нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="88d5b-367">It is more efficient to draw an existing resource from the pool than to create a new resource.</span></span>

<span data-ttu-id="88d5b-368">**ProgID (программный идентификатор)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-368">**ProgID (programmatic identifier)**</span></span>

<span data-ttu-id="88d5b-369">Уникальное имя для сопоставления с реестра Windows COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-369">A unique name mapped to the Windows registry by a COM application.</span></span> <span data-ttu-id="88d5b-370">ProgID для ADO-подключение является «ADODB. Подключения».</span><span class="sxs-lookup"><span data-stu-id="88d5b-370">The ProgID for an ADO Connection is "ADODB.Connection".</span></span> <span data-ttu-id="88d5b-371">В разделе также **CLSID**, **COM**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-371">See also **CLSID**, **COM**.</span></span>

<span data-ttu-id="88d5b-372">**proxy**</span><span class="sxs-lookup"><span data-stu-id="88d5b-372">**proxy**</span></span>

<span data-ttu-id="88d5b-373">Интерфейс-объект, предоставляющий маршалинга параметров и связи, необходимые для клиента для вызова объект приложения, на котором работает в среде выполнения различных, таких как в потоке, или в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="88d5b-373">An interface-specific object that provides the parameter marshaling and communication required for a client to call an application object that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="88d5b-374">Прокси-сервер расположен с клиентом и взаимодействует с соответствующую заглушку, расположенный с помощью объекта приложения, которая вызывается.</span><span class="sxs-lookup"><span data-stu-id="88d5b-374">The proxy is located with the client and communicates with a corresponding stub that is located with the application object that is being called.</span></span> <span data-ttu-id="88d5b-375">В разделе также **заглушку**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-375">See also **stub**.</span></span>

<span data-ttu-id="88d5b-376">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-376">Return to top</span></span>

## <a name="r"></a><span data-ttu-id="88d5b-377">R</span><span class="sxs-lookup"><span data-stu-id="88d5b-377">R</span></span>

<span data-ttu-id="88d5b-378">**относительный URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="88d5b-378">**relative URL**</span></span>

<span data-ttu-id="88d5b-379">Частично полный URL-адрес, который задает ресурс в Интернете или интрасети, расположение которого является относительно отправной точки, указанного идентификатором абсолютный URL-адрес или эквивалентный объект ADO Connection.</span><span class="sxs-lookup"><span data-stu-id="88d5b-379">A partially qualified URL that specifies a resource on the Internet or an intranet whose location is relative to a starting point specified by an absolute URL or equivalent ADO Connection object.</span></span> <span data-ttu-id="88d5b-380">В силу, объединенные абсолютных и относительных URL-адресов consitute полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="88d5b-380">In effect, the concatenated absolute and relative URLs consitute a complete URL.</span></span> <span data-ttu-id="88d5b-381">В разделе также **URL-адреса** и **абсолютный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-381">See also **URL** and **absolute URL**.</span></span>

<span data-ttu-id="88d5b-382">**удаленному источнику данных**</span><span class="sxs-lookup"><span data-stu-id="88d5b-382">**remote data source**</span></span>

<span data-ttu-id="88d5b-383">Источник данных, который существует на другом компьютере, а не в локальной системе (где выполняется в клиентском приложении).</span><span class="sxs-lookup"><span data-stu-id="88d5b-383">A data source that exists on a another computer, rather than on the local system (where the client application runs).</span></span>

<span data-ttu-id="88d5b-384">**запись ресурса**</span><span class="sxs-lookup"><span data-stu-id="88d5b-384">**resource record**</span></span>

<span data-ttu-id="88d5b-385">Записи из поставщика источника документа, который содержит поля для определения и описания папки или документа.</span><span class="sxs-lookup"><span data-stu-id="88d5b-385">A record from a document source provider that contains fields for the definition and description of a folder or document.</span></span> <span data-ttu-id="88d5b-386">Сам документ не находится в записи ресурса, но обычно может осуществляться в потоке по умолчанию или поля в записи ресурса, содержащая URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="88d5b-386">The document itself is not contained in the resource record but typically can be accessed by the default stream or a field in the resource record containing a URL.</span></span> <span data-ttu-id="88d5b-387">Смотрите также **Поставщик источника документа**, **поток по умолчанию**, **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-387">See also **document source provider**, **default stream**, **URL**.</span></span>

<span data-ttu-id="88d5b-388">**root**</span><span class="sxs-lookup"><span data-stu-id="88d5b-388">**root**</span></span>

<span data-ttu-id="88d5b-389">Верхнего уровня в иерархическую древовидную структуру.</span><span class="sxs-lookup"><span data-stu-id="88d5b-389">The top level in a hierarchical tree structure.</span></span> <span data-ttu-id="88d5b-390">Корневой узел имеет родительский объект не, но могут быть дочерние узлы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-390">The root node has no parents, but may have children.</span></span> <span data-ttu-id="88d5b-391">Смотрите также **иерархии**, **дерева**, **parent**, **дочерние**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-391">See also **hierarchy**, **tree**, **parent**, **child**.</span></span>

<span data-ttu-id="88d5b-392">**набор строк**</span><span class="sxs-lookup"><span data-stu-id="88d5b-392">**rowset**</span></span>

<span data-ttu-id="88d5b-393">Набор строк из источника данных, все того же схеме полей.</span><span class="sxs-lookup"><span data-stu-id="88d5b-393">A set of rows from a data source, all having the same field schema.</span></span> <span data-ttu-id="88d5b-394">Набор строк может представлять некоторые или все поля из таблицы.</span><span class="sxs-lookup"><span data-stu-id="88d5b-394">A rowset can represent all or some fields from a table.</span></span> <span data-ttu-id="88d5b-395">Набор строк также может представлять виртуальную таблицу, созданный запрос или соединение двух или нескольких таблиц.</span><span class="sxs-lookup"><span data-stu-id="88d5b-395">A rowset can also represent a virtual table, created by a query or a join of two or more tables.</span></span> <span data-ttu-id="88d5b-396">В ADO наборы строк представленные объектами **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-396">In ADO, rowsets are represented by **Recordset** objects.</span></span>

<span data-ttu-id="88d5b-397">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-397">Return to top</span></span>

## <a name="s"></a><span data-ttu-id="88d5b-398">s</span><span class="sxs-lookup"><span data-stu-id="88d5b-398">S</span></span>

<span data-ttu-id="88d5b-399">**схемы**</span><span class="sxs-lookup"><span data-stu-id="88d5b-399">**schema**</span></span>

<span data-ttu-id="88d5b-400">Описание базу данных для система управления базами данных (СУБД), обычно создается с помощью языка определения данных, предоставленные СУБД.</span><span class="sxs-lookup"><span data-stu-id="88d5b-400">A description of a database to the database management system (DBMS), typically generated using the data definition language provided by the DBMS.</span></span> <span data-ttu-id="88d5b-401">Схема определяет атрибуты базы данных, например таблицы, столбцы и свойства.</span><span class="sxs-lookup"><span data-stu-id="88d5b-401">A schema defines attributes of the database, such as tables, columns, and properties.</span></span>

<span data-ttu-id="88d5b-402">**scope**</span><span class="sxs-lookup"><span data-stu-id="88d5b-402">**scope**</span></span>

<span data-ttu-id="88d5b-403">Диапазон ссылку для объекта или переменной или диапазон записей в представлении или таблице.</span><span class="sxs-lookup"><span data-stu-id="88d5b-403">The range of reference for an object or variable or a range of records in a view or table.</span></span> <span data-ttu-id="88d5b-404">Например локальные переменные можно ссылаться только в пределах процедуры, в котором они были определены.</span><span class="sxs-lookup"><span data-stu-id="88d5b-404">For example, local variables can be referenced only within the procedure in which they were defined.</span></span> <span data-ttu-id="88d5b-405">Переменных с атрибутом Public доступны в любом месте приложения.</span><span class="sxs-lookup"><span data-stu-id="88d5b-405">Public variables are accessible from anywhere in the application.</span></span> <span data-ttu-id="88d5b-406">Объекты, такие как текущей базы данных находятся в области действия, если они находятся в путь поиска.</span><span class="sxs-lookup"><span data-stu-id="88d5b-406">Objects, such as the current database, are in scope if they are in the defined search path.</span></span> <span data-ttu-id="88d5b-407">Запишите диапазонов может быть указан с предложением область в многие команды.</span><span class="sxs-lookup"><span data-stu-id="88d5b-407">Record ranges can be specified with a Scope clause in many commands.</span></span>

<span data-ttu-id="88d5b-408">**Поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="88d5b-408">**service provider**</span></span>

<span data-ttu-id="88d5b-409">Программное обеспечение, инкапсулирующий службы путем создания и использования данных, дополнения функции в приложениях ADO.</span><span class="sxs-lookup"><span data-stu-id="88d5b-409">Software that encapsulates a service by producing and consuming data, augmenting features in your ADO applications.</span></span> <span data-ttu-id="88d5b-410">Поставщик, непосредственно не предоставляют данные, а вместо предоставляет службы, такие как обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-410">It is a provider that does not directly expose data, rather it provides a service, such as query processing.</span></span> <span data-ttu-id="88d5b-411">Поставщик услуг может обработать данные, предоставляемые поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="88d5b-411">The service provider may process data provided by a data provider.</span></span> <span data-ttu-id="88d5b-412">Смотрите также **Поставщик данных**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-412">See also **data provider**.</span></span>

<span data-ttu-id="88d5b-413">**формы записей**</span><span class="sxs-lookup"><span data-stu-id="88d5b-413">**shaped Recordset**</span></span>

<span data-ttu-id="88d5b-414">Набор **записей** , столбцы определенных специально для хранения не только данные, но также и справочные материалы (называемые главы) для других объектов **наборов записей** и/или вычисляемые значения на основе других объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="88d5b-414">A **Recordset** whose columns have been specifically defined to contain not just data, but also references (called chapters) to other **Recordset** objects and/or computed values based on other **Recordset** objects.</span></span>

<span data-ttu-id="88d5b-415">**одноуровневый**</span><span class="sxs-lookup"><span data-stu-id="88d5b-415">**sibling**</span></span>

<span data-ttu-id="88d5b-416">Два или более узлы в виде иерархической структуры, расположенные на том же уровне иерархии.</span><span class="sxs-lookup"><span data-stu-id="88d5b-416">Any two or more nodes in a hierarchical structure that are on the same level in the hierarchy.</span></span> <span data-ttu-id="88d5b-417">Корневой узел в иерархии имеет не элементы одного уровня.</span><span class="sxs-lookup"><span data-stu-id="88d5b-417">The root node in a hierarchy has no siblings.</span></span>

<span data-ttu-id="88d5b-418">**хранимые процедуры**</span><span class="sxs-lookup"><span data-stu-id="88d5b-418">**stored procedure**</span></span>

<span data-ttu-id="88d5b-419">Набор скомпилированных кода, такие как инструкций SQL и необязательных инструкций управления потоком хранятся в разделе имя и обрабатывается как единое.</span><span class="sxs-lookup"><span data-stu-id="88d5b-419">A precompiled collection of code such as SQL statements and optional control-of-flow statements stored under a name and processed as a unit.</span></span> <span data-ttu-id="88d5b-420">Хранимые процедуры хранятся в базе данных; они могут быть выполнены с помощью одного вызова из приложения и Разрешить пользовательские переменные, условное выполнение и другие мощные возможности программирования.</span><span class="sxs-lookup"><span data-stu-id="88d5b-420">Stored procedures are stored within a database; they can be executed with one call from an application and allow user-declared variables, conditional execution, and other powerful programming features.</span></span>

<span data-ttu-id="88d5b-421">**заготовка**</span><span class="sxs-lookup"><span data-stu-id="88d5b-421">**stub**</span></span>

<span data-ttu-id="88d5b-422">Интерфейс-объект, предоставляющий маршалинга параметров и связи, необходимые для объекта приложения будут принимать звонки от клиента, на котором работает в среде выполнения различных, таких как в потоке, или в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="88d5b-422">An interface-specific object that provides the parameter marshaling and communication required for an application object to receive calls from a client that is running in a different execution environment, such as on a different thread or in another process.</span></span> <span data-ttu-id="88d5b-423">Заглушка находится с помощью объекта приложения и взаимодействует с соответствующей прокси-сервер, расположенный с клиента, который вызывает его.</span><span class="sxs-lookup"><span data-stu-id="88d5b-423">The stub is located with the application object and communicates with a corresponding proxy that is located with the client that calls it.</span></span> <span data-ttu-id="88d5b-424">В разделе также **прокси-сервера**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-424">See also **proxy**.</span></span>

<span data-ttu-id="88d5b-425">**вложенный узел**</span><span class="sxs-lookup"><span data-stu-id="88d5b-425">**sub-node**</span></span>

<span data-ttu-id="88d5b-426">В разделе **дочерние**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-426">See **child**.</span></span>

<span data-ttu-id="88d5b-427">**Синхронный режим**</span><span class="sxs-lookup"><span data-stu-id="88d5b-427">**synchronous operation**</span></span>

<span data-ttu-id="88d5b-428">Операция, инициированных код, который выполняется до следующей операции может запускаться.</span><span class="sxs-lookup"><span data-stu-id="88d5b-428">An operation initiated by code that completes before the next operation may start.</span></span> <span data-ttu-id="88d5b-429">В разделе также **асинхронной операции**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-429">See also **asynchronous operation**.</span></span>

<span data-ttu-id="88d5b-430">К началу страницы</span><span class="sxs-lookup"><span data-stu-id="88d5b-430">Return to top</span></span>

## <a name="t-w"></a><span data-ttu-id="88d5b-431">T-W</span><span class="sxs-lookup"><span data-stu-id="88d5b-431">T-W</span></span>

<span data-ttu-id="88d5b-432">**tree**</span><span class="sxs-lookup"><span data-stu-id="88d5b-432">**tree**</span></span>

<span data-ttu-id="88d5b-433">Структура, представляющая иерархическую связь между элементами (узлы).</span><span class="sxs-lookup"><span data-stu-id="88d5b-433">A structure representing a hierarchical relationship between elements (nodes).</span></span> <span data-ttu-id="88d5b-434">Имеется один узел верхнего уровня дерева (корень).</span><span class="sxs-lookup"><span data-stu-id="88d5b-434">There is one node at the top level of a tree (the root).</span></span> <span data-ttu-id="88d5b-435">Ниже корня может быть несколько дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="88d5b-435">Underneath the root, there can be multiple children.</span></span> <span data-ttu-id="88d5b-436">В свою очередь каждого дочернего объекта может быть родительской других дочерних элементов, таким образом ветвление как дерево.</span><span class="sxs-lookup"><span data-stu-id="88d5b-436">Each child may in turn be the parent of other children, thus branching like a tree.</span></span> <span data-ttu-id="88d5b-437">Папка, содержащая документы и другие папки — это типичный древовидной структуры.</span><span class="sxs-lookup"><span data-stu-id="88d5b-437">A folder containing documents and other folders is a typical example of a tree structure.</span></span> <span data-ttu-id="88d5b-438">См в разделе также **иерархии**, **узел**, **корневой**, **дочерние** **parent**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-438">See also **hierarchy**, **node**, **root**, **child**, **parent**.</span></span>

<span data-ttu-id="88d5b-439">**URL-адрес (унифицированный указатель ресурсов)**</span><span class="sxs-lookup"><span data-stu-id="88d5b-439">**URL (Uniform Resource Locator)**</span></span>

<span data-ttu-id="88d5b-440">Указывает расположение ресурса, находящегося в Интернете или интрасети.</span><span class="sxs-lookup"><span data-stu-id="88d5b-440">Specifies the location of a resource residing on the Internet or an intranet.</span></span> <span data-ttu-id="88d5b-441">Полный URL-адрес состоит из схемы (например, FTP, HTTP, mailto, файлов и т. д.), за которым следует двоеточие, имя сервера и полный путь к ресурсу (например, документ, рисунок или другой файл).</span><span class="sxs-lookup"><span data-stu-id="88d5b-441">A complete URL consists of a scheme (such as FTP, HTTP, mailto, file, and so on), followed by a colon, a server name, and the full path of a resource (such as a document, graphic, or other file).</span></span> <span data-ttu-id="88d5b-442">Некоторые примеры URL-адреса, являются:</span><span class="sxs-lookup"><span data-stu-id="88d5b-442">Some examples of URLs are:</span></span>  
  
- https://www.domain.com/default.html  
- <span data-ttu-id="88d5b-443">FTP://FTP.Server.somewhere/FTP.File</span><span class="sxs-lookup"><span data-stu-id="88d5b-443">ftp://ftp.server.somewhere/ftp.file</span></span>  
  
- <span data-ttu-id="88d5b-444">FTP://FTP.Server.somewhere/FTP.File</span><span class="sxs-lookup"><span data-stu-id="88d5b-444">ftp://ftp.server.somewhere/ftp.file</span></span>  
- <span data-ttu-id="88d5b-445">file://Server/Share/File.doc</span><span class="sxs-lookup"><span data-stu-id="88d5b-445">file://Server/Share/File.doc</span></span>

<span data-ttu-id="88d5b-446">В разделе также **абсолютный URL-адрес** и **относительный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="88d5b-446">See also **absolute URL** and **relative URL**.</span></span>

<span data-ttu-id="88d5b-447">**веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="88d5b-447">**web server**</span></span>

<span data-ttu-id="88d5b-448">Компьютер, который предоставляет веб-служб и страницы, предназначенные для пользователей Интернета и интрасети.</span><span class="sxs-lookup"><span data-stu-id="88d5b-448">A computer that provides web services and pages to intranet and Internet users.</span></span>



