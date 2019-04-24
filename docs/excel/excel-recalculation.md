---
title: Пересчет в Excel
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 07deec5ad104c59074567725d6abf9b66711e351
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304118"
---
# <a name="excel-recalculation"></a><span data-ttu-id="a2dc6-104">Пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="a2dc6-104">Excel Recalculation</span></span>

<span data-ttu-id="a2dc6-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a2dc6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a2dc6-106">Пользователь может вызывать пересчет в Microsoft Excel несколькими способами, например:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="a2dc6-107">путем ввода новых данных (если Excel находится в режиме автоматического пересчета, описанном далее в этой статье);</span><span class="sxs-lookup"><span data-stu-id="a2dc6-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="a2dc6-108">явным указанием Excel пересчитать всю книгу или ее часть;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="a2dc6-109">путем удаления или вставки строки или столбца;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="a2dc6-110">путем сохранения книги при заданном параметре **Пересчет перед сохранением**;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="a2dc6-111">путем выполнения некоторых действий автофильтра;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="a2dc6-112">двойным щелчком по разделителю строк или столбцов (в режиме автоматического вычисления);</span><span class="sxs-lookup"><span data-stu-id="a2dc6-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="a2dc6-113">путем добавления, редактирования или удаления заданного имени;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="a2dc6-114">путем переименования листа;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="a2dc6-115">путем изменения позиции листа относительно других листов;</span><span class="sxs-lookup"><span data-stu-id="a2dc6-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="a2dc6-116">путем скрытия или отображения строк (не столбцов).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a2dc6-p101">В этой статье не делается различий между непосредственным нажатием клавиши или кнопки мыши пользователем и выполнением этих задач командой или макросом. Пользователь запускает команду или делает что-либо, чтобы она запустилась, поэтому это также считается действием пользователя. Таким образом, слово "пользователь" также означает "пользователь либо команда или процесс, запущенные пользователем".</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="a2dc6-120">Зависимость, "грязные" ячейки и пересчитанные ячейки</span><span class="sxs-lookup"><span data-stu-id="a2dc6-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="a2dc6-121">Вычисление листов в Excel можно рассматривать как процесс из трех этапов:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="a2dc6-122">Создание дерева зависимостей</span><span class="sxs-lookup"><span data-stu-id="a2dc6-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="a2dc6-123">Создание цепочки вычислений</span><span class="sxs-lookup"><span data-stu-id="a2dc6-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="a2dc6-124">Пересчет ячеек</span><span class="sxs-lookup"><span data-stu-id="a2dc6-124">Recalculation of cells</span></span>
    
<span data-ttu-id="a2dc6-p102">Дерево зависимостей сообщает Excel, какие ячейки зависят от других ячеек или, аналогично, какие ячейки являются прецедентами для других. Из этого дерева Excel составляет цепочку вычислений. В ней перечисляются все ячейки, которые содержат формулы, в том порядке, в котором их необходимо вычислять. Во время пересчета Excel изменяет эту цепочку, если обнаруживается формула, которая зависит от еще не вычисленной ячейки. В этом случае вычисляемая ячейка и зависящие от нее ячейки перемещаются вниз по цепочке. По этой причине время вычисления в первых нескольких циклах часто сокращается на листах, которые были только что открыты.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="a2dc6-p103">При структурном изменении книги, например при вводе новой формулы, Excel заново создает дерево зависимостей и цепочку вычислений. При вводе новых данных или новых формул Excel помечает все ячейки, которые зависят от новых данных, как требующие пересчета. Помеченные таким образом ячейки называются *"грязными"*. Все прямые и косвенные зависимые ячейки помечаются как "грязные", поэтому если ячейка B1 зависит от ячейки A1, а ячейка C1 — от B1, то при изменении ячейки A1 ячейки B1 и C1 помечаются как "грязные".</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p103">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="a2dc6-p104">Если ячейка зависит, прямо или косвенно, от себя, то Excel обнаруживает циклическую ссылку и предупреждает пользователя. Как правило, это приводит к ошибке, которую пользователь должен исправить, а Excel предоставляет полезные графические и навигационные средства, которые помогут пользователю найти источник циклической зависимости. В некоторых случаях это условие создается намеренно. К примеру, вам нужно выполнить итеративное вычисление, где начальной точкой для следующей итерации является результат предыдущей. Excel поддерживает управление итеративными вычислениями с помощью диалогового окна параметров вычислений.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="a2dc6-p105">Отметив ячейки как "грязные" при следующем пересчете, Excel повторно оценивает содержимое каждой "грязной" ячейки в порядке, определяемом цепочкой вычислений. В приведенном выше примере это означает, что сначала оценивается ячейка B1, а затем — C1. Пересчет происходит сразу после того, как Excel закончит отмечать ячейки как "грязные", если выбран автоматический режим пересчета. В противном случае это происходит позже.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="a2dc6-p106">Начиная с Microsoft Excel 2002, объект **Range** в Microsoft Visual Basic для приложений (VBA) поддерживает метод **Range.Dirty**, который отмечает ячейки как требующие подсчета. Когда он используется совместно с методом **Range.Calculate** (см. следующий раздел), он включает принудительный пересчет ячеек в заданном диапазоне. Это удобно при выполнении ограниченного вычисления в макросе, где установлен ручной режим подсчета (для избежания избытка вычисляемых ячеек, не относящихся к функции макроса). Методы подсчета диапазонов недоступны через API C.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="a2dc6-p107">В Excel 2002 и более ранних версиях Excel составлял цепочку вычислений для каждого листа в каждой открытой книге. Это несколько усложняло обработку ссылок между листами и требовало осторожности для обеспечения эффективного пересчета. В частности, в Excel 2000 необходимо сводить к минимуму зависимости между листами и присваивать листам имена в алфавитном порядке, чтобы листы, зависящие от других листов, следовали по алфавиту за листами, от которых они зависят.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="a2dc6-p108">В Excel 2007 логика была улучшена для поддержки пересчета в нескольких потоках, чтобы разделы цепочки вычислений не зависели друг от друга и для них можно было проводить подсчеты одновременно. Вы можете настроить Excel для использования нескольких потоков на компьютере с одним процессором или одного потока на многопроцессорном или многоядерном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p108">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="a2dc6-152">Асинхронные пользовательские функции</span><span class="sxs-lookup"><span data-stu-id="a2dc6-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="a2dc6-p109">Когда вычисление обнаруживает асинхронную пользовательскую функцию, оно сохраняет состояние текущей формулы, запускает пользовательскую функцию и продолжает оценивать остальные ячейки. Когда вычисление завершает оценку ячеек, Excel ждет завершения асинхронных функций, если они еще выполняются. По мере того как каждая асинхронная функция сообщает о результатах, Excel завершает формулу, а затем запускает новую передачу вычисления, чтобы пересчитать ячейки, которые используют ячейку со ссылкой на асинхронную функцию.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="a2dc6-156">Переменные и постоянные функции</span><span class="sxs-lookup"><span data-stu-id="a2dc6-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="a2dc6-p110">Excel поддерживает переменные функции, то есть функции, значения которых в разные моменты могут отличаться, даже если ни один из аргументов (если они принимаются) не изменился. Excel повторно оценивает ячейки, которые содержат переменные функции, вместе со всеми зависимыми функциями при каждом пересчете. По этой причине чрезмерное использование переменных функций может замедлить пересчет. Используйте их экономно.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="a2dc6-161">Переменными являются следующие функции Excel:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="a2dc6-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-162">**NOW**</span></span>
    
- <span data-ttu-id="a2dc6-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-163">**TODAY**</span></span>
    
- <span data-ttu-id="a2dc6-164">**RANDBETWEEN**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="a2dc6-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-165">**OFFSET**</span></span>
    
- <span data-ttu-id="a2dc6-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="a2dc6-167">**INFO** (в зависимости от аргументов)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="a2dc6-168">**CELL** (в зависимости от аргументов)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="a2dc6-169">**SUMIF** (в зависимости от аргументов)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="a2dc6-p111">Интерфейсы API VBA и C поддерживают способы сообщить Excel, что пользовательскую функцию следует обрабатывать как переменную. В VBA пользовательская функция объявляется переменной следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="a2dc6-p112">По умолчанию Excel предполагает, что пользовательские функции VBA не являются переменными. Excel узнает, что пользовательская функция является переменной, только при ее первом вызове. Переменную пользовательскую функцию можно сделать постоянной, как в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="a2dc6-p113">С помощью API C можно зарегистрировать функцию XLL как переменную до ее первого вызова. Он также позволяет включать и отключать переменное состояние функции листа.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="a2dc6-p114">По умолчанию Excel обрабатывает пользовательские функции XLL, которые принимают диапазоны в качестве аргументов и объявлены как эквиваленты листа макросов (изменчивые). Вы можете отключить это состояние по умолчанию с помощью функции **xlfVolatile** при первом вызове пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="a2dc6-179">Режимы вычисления, команды, выборочный пересчет и таблицы данных</span><span class="sxs-lookup"><span data-stu-id="a2dc6-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="a2dc6-180">В Excel есть три режима вычисления:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="a2dc6-181">Automatic</span><span class="sxs-lookup"><span data-stu-id="a2dc6-181">Automatic</span></span>
    
- <span data-ttu-id="a2dc6-182">Автоматический, кроме таблиц</span><span class="sxs-lookup"><span data-stu-id="a2dc6-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="a2dc6-183">Manual</span><span class="sxs-lookup"><span data-stu-id="a2dc6-183">Manual</span></span>
    
<span data-ttu-id="a2dc6-p115">В автоматическом режиме вычисления пересчет происходит только после каждого ввода данных и после определенных событий, таких как примеры в предыдущем разделе. В очень больших книгах пересчет может занимать так много времени, что пользователям необходимо ограничивать эти условия, чтобы пересчет происходил только при необходимости. Для этого Excel поддерживает ручной режим. Пользователь может выбрать режим в системе меню Excel или программным способом с помощью API VBA, COM или C.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="a2dc6-p116">Таблицы данных — это специальные структуры на листе. Сначала пользователь настраивает вычисление результата на листе. Это зависит от одного или двух изменяемых наборов данных, введенных с клавиатуры, и других параметров. Затем пользователь может создать таблицу результатов для значений одного или обоих вводов с клавиатуры. Таблица создается с помощью **мастера таблиц данных**. После настройки таблицы Excel по одному отправляет наборы введенных данных в вычисление и копирует полученное значение в таблицу. Так как можно использовать один или два набора введенных данных, таблицы данных могут быть одномерными или двумерными.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="a2dc6-195">Пересчет таблиц данных обрабатывается немного по-другому:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="a2dc6-196">Пересчет обрабатывается асинхронно в отличие от обычного пересчета книг, поэтому пересчет больших таблиц может занимать больше времени, чем пересчет остальных элементов книги.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="a2dc6-p117">Циклические ссылки допускаются. Если вычисление, используемое для получения результата, зависит от одного или нескольких значений из таблицы данных, то Excel не возвращает ошибку циклической зависимости.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 

- <span data-ttu-id="a2dc6-199">Таблицы данных не используют многопоточные вычисления.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-199">Data tables do not use multi-threaded calculation.</span></span>
    
<span data-ttu-id="a2dc6-p118">Учитывая, что Excel по-другому обрабатывает пересчет таблиц данных, а вычисление больших таблиц, зависящих от сложных или длинных вычислений, может занимать много времени, Excel позволяет отключить автоматическое вычисление таблиц данных. Для этого выберите режим вычисления "Автоматический, кроме таблиц". В этом режиме пользователь может пересчитывать данные, нажав клавишу F9 или выполнив эквивалентную программную операцию.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="a2dc6-p119">Excel предоставляет методы, с помощью которых можно изменять режим пересчета и управлять им. Эти методы улучшались от версии к версии, чтобы обеспечить возможность более точного управления. Возможности API C в этом отношении отражают возможности, доступные в Excel версии 5, поэтому не предоставляют такого управления, как при использовании VBA в более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="a2dc6-206">Эти методы чаще всего используются, когда Excel находится в ручном режиме вычисления, и позволяют выборочно вычислять книги, листы и диапазоны, полностью пересчитывать все открытые книги и даже полностью перестраивать дерево зависимостей и цепочку вычислений.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-206">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="a2dc6-207">Вычисление диапазонов</span><span class="sxs-lookup"><span data-stu-id="a2dc6-207">Range Calculation</span></span>

<span data-ttu-id="a2dc6-208">Клавиша: нет</span><span class="sxs-lookup"><span data-stu-id="a2dc6-208">Keystroke: None</span></span>
  
<span data-ttu-id="a2dc6-209">VBA: **Range.Calculate** (представлен в Excel 2000, изменен в Excel 2007) и **Range.CalculateRowMajorOrder** (представлен в Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-209">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="a2dc6-210">API C: не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a2dc6-210">C API: Not supported</span></span>
  
- <span data-ttu-id="a2dc6-211">**Ручной режим**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-211">**Manual mode**</span></span>
    
    <span data-ttu-id="a2dc6-p120">Пересчитывает только ячейки в заданном диапазоне независимо от того, "грязные" ли они. Поведение метода **Range.Calculate** изменилось в Excel 2007. Но предыдущее поведение по-прежнему поддерживается методом **Range.CalculateRowMajorOrder**.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="a2dc6-214">**Режим "Автоматически" или "Автоматически, кроме таблиц"**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-214">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="a2dc6-215">Пересчитывает книгу, но не выполняет принудительный пересчет диапазона или каких-либо ячеек в нем.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-215">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="a2dc6-216">Активное вычисление листов</span><span class="sxs-lookup"><span data-stu-id="a2dc6-216">Active Worksheet Calculation</span></span>

<span data-ttu-id="a2dc6-217">Клавиши: SHIFT+F9</span><span class="sxs-lookup"><span data-stu-id="a2dc6-217">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="a2dc6-218">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-218">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="a2dc6-219">API C: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-219">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="a2dc6-220">**Все режимы**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-220">**All modes**</span></span>
    
    <span data-ttu-id="a2dc6-221">Пересчитывает ячейки, отмеченные для вычисления, только на активном листе.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-221">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="a2dc6-222">Вычисление указанных листов</span><span class="sxs-lookup"><span data-stu-id="a2dc6-222">Specified Worksheet Calculation</span></span>

<span data-ttu-id="a2dc6-223">Клавиша: нет</span><span class="sxs-lookup"><span data-stu-id="a2dc6-223">Keystroke: None</span></span>
  
<span data-ttu-id="a2dc6-224">VBA: **Worksheets(** reference **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-224">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="a2dc6-225">API C: не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a2dc6-225">C API: Not supported</span></span>
  
- <span data-ttu-id="a2dc6-226">**Все режимы**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-226">**All modes**</span></span>
    
    <span data-ttu-id="a2dc6-p121">Пересчитывает "грязные" ячейки и их зависимости только на указанном листе. Ссылка — это имя листа как строка или номер индекса в соответствующей книге.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="a2dc6-p122">Excel 2000 и более поздних версий предоставляет свойство листа **Boolean** (**EnableCalculation**). Если задать для него значение **True** вместо **False**, все ячейки на указанном листе будут помечены как "грязные". В автоматических режимах это вызывает пересчет всей книги.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="a2dc6-232">В ручном режиме следующий код вызывает пересчет только активного листа.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-232">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="a2dc6-233">Повторное создание и принудительный пересчет дерева книги</span><span class="sxs-lookup"><span data-stu-id="a2dc6-233">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="a2dc6-234">Клавиши: CTRL+ALT+SHIFT+F9 (появились в Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-234">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="a2dc6-235">VBA: **Workbooks(** reference **).ForceFullCalculation** (представлен в Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-235">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="a2dc6-236">API C: не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a2dc6-236">C API: Not supported</span></span>
  
- <span data-ttu-id="a2dc6-237">**Все режимы**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-237">**All modes**</span></span>
    
    <span data-ttu-id="a2dc6-238">Указывает Excel заново создать дерево зависимостей и цепочку вычислений для определенной книги и вызывает пересчет всех ячеек, содержащих формулы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-238">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="a2dc6-239">Все открытые книги</span><span class="sxs-lookup"><span data-stu-id="a2dc6-239">All Open Workbooks</span></span>

<span data-ttu-id="a2dc6-240">Клавиша: F9</span><span class="sxs-lookup"><span data-stu-id="a2dc6-240">Keystroke: F9</span></span>
  
<span data-ttu-id="a2dc6-241">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-241">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="a2dc6-242">API C: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-242">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="a2dc6-243">**Все режимы**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-243">**All modes**</span></span>
    
    <span data-ttu-id="a2dc6-p123">Пересчитывает все ячейки, которые Excel отметил как "грязные", то есть зависящие от переменных или измененных данных, и ячейки, программно отмеченные как "грязные". Если выбран режим вычисления "Автоматический, кроме таблиц", этот метод вычисляет таблицы, которые требуют обновления, а также все переменные функции и их зависимости.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="a2dc6-246">Повторное создание и принудительное вычисление дерева всех открытых книг</span><span class="sxs-lookup"><span data-stu-id="a2dc6-246">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="a2dc6-247">Клавиши: CTRL+ALT+F9</span><span class="sxs-lookup"><span data-stu-id="a2dc6-247">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="a2dc6-248">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-248">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="a2dc6-249">API C: не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a2dc6-249">C API: Not supported</span></span>
  
- <span data-ttu-id="a2dc6-250">**Все режимы**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-250">**All modes**</span></span>
    
    <span data-ttu-id="a2dc6-p124">Пересчитывает все ячейки во всех открытых книгах. Если выбран режим вычисления "Автоматический, кроме таблиц", выполняется принудительный пересчет таблиц.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2dc6-253">См. также</span><span class="sxs-lookup"><span data-stu-id="a2dc6-253">See also</span></span>



[<span data-ttu-id="a2dc6-254">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="a2dc6-254">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="a2dc6-255">Типы данных, используемые в Excel</span><span class="sxs-lookup"><span data-stu-id="a2dc6-255">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="a2dc6-256">Управление памятью в Excel</span><span class="sxs-lookup"><span data-stu-id="a2dc6-256">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="a2dc6-257">Понятия, связанные с программированием, для Excel</span><span class="sxs-lookup"><span data-stu-id="a2dc6-257">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

