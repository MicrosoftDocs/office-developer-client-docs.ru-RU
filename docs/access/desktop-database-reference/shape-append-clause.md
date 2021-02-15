---
title: Предложение Append команды Shape
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306449"
---
# <a name="shape-append-clause"></a><span data-ttu-id="75070-102">Предложение Append команды Shape</span><span class="sxs-lookup"><span data-stu-id="75070-102">Shape Append clause</span></span>


<span data-ttu-id="75070-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75070-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75070-104">Предложение APPEND команды фигуры привяжает столбец или столбцы к **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="75070-104">The shape command APPEND clause appends a column or columns to a **Recordset**.</span></span> <span data-ttu-id="75070-105">Часто эти столбцы являются столбцами глав, которые ссылаются на набор **записей.**</span><span class="sxs-lookup"><span data-stu-id="75070-105">Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="75070-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75070-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="75070-107">Описание</span><span class="sxs-lookup"><span data-stu-id="75070-107">Description</span></span>

<span data-ttu-id="75070-108">Часть этого предложения:</span><span class="sxs-lookup"><span data-stu-id="75070-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="75070-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="75070-109">*parent-command*</span></span>

- <span data-ttu-id="75070-110">Ноль или одно из следующих *(родительская* команда может полностью опуститься):</span><span class="sxs-lookup"><span data-stu-id="75070-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="75070-111">Команда поставщика в фигурных скобках (" "), которая возвращает {} объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="75070-111">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="75070-112">Команда передается основному поставщику данных, и ее синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="75070-112">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="75070-113">Обычно это язык SQL, хотя ADO не требует определенного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="75070-113">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="75070-114">Другая команда фигуры, встроенная в скобки.</span><span class="sxs-lookup"><span data-stu-id="75070-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="75070-115">Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="75070-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="75070-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="75070-116">*parent-alias*</span></span>

  - <span data-ttu-id="75070-117">Необязательный псевдоним, который ссылается на родительский **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="75070-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="75070-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="75070-118">*column-list*</span></span>

  - <span data-ttu-id="75070-119">Один или несколько из следующих следующую:</span><span class="sxs-lookup"><span data-stu-id="75070-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="75070-120">Сводный столбец.</span><span class="sxs-lookup"><span data-stu-id="75070-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="75070-121">Вычисляется столбец.</span><span class="sxs-lookup"><span data-stu-id="75070-121">A calculated column.</span></span>
    
    - <span data-ttu-id="75070-122">Новый столбец, созданный с помощью предложения NEW.</span><span class="sxs-lookup"><span data-stu-id="75070-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="75070-123">Столбец главы.</span><span class="sxs-lookup"><span data-stu-id="75070-123">A chapter column.</span></span> <span data-ttu-id="75070-124">Определение столбца главы заключено в скобки ("()").</span><span class="sxs-lookup"><span data-stu-id="75070-124">A chapter column definition is enclosed in parentheses ("()").</span></span> <span data-ttu-id="75070-125">См. синтаксис ниже:</span><span class="sxs-lookup"><span data-stu-id="75070-125">See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="75070-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="75070-126">*child-recordset*</span></span>

  - <span data-ttu-id="75070-127">Команда поставщика в фигурных скобках (" "), которая возвращает {} объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="75070-127">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="75070-128">Команда передается основному поставщику данных, и ее синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="75070-128">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="75070-129">Обычно это язык SQL, хотя ADO не требует определенного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="75070-129">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="75070-130">Другая команда фигуры, встроенная в скобки.</span><span class="sxs-lookup"><span data-stu-id="75070-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="75070-131">Имя существующего фигурного **recordset.**</span><span class="sxs-lookup"><span data-stu-id="75070-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="75070-132">Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="75070-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="75070-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="75070-133">*child-alias*</span></span>

  - <span data-ttu-id="75070-134">Псевдоним, который ссылается на набор **записей.**</span><span class="sxs-lookup"><span data-stu-id="75070-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="75070-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="75070-135">*parent-column*</span></span>

  - <span data-ttu-id="75070-136">Столбец в **наборе записей,** возвращаемом *родительской командой.*</span><span class="sxs-lookup"><span data-stu-id="75070-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="75070-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="75070-137">*child-column*</span></span>

  - <span data-ttu-id="75070-138">Столбец в **наборе записей,** возвращаемом *командой child-command.*</span><span class="sxs-lookup"><span data-stu-id="75070-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="75070-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="75070-139">*param-number*</span></span>

  - <span data-ttu-id="75070-140">См. ["Операция параметровизированных команд".](operation-of-parameterized-commands.md)</span><span class="sxs-lookup"><span data-stu-id="75070-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="75070-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="75070-141">*chapter-alias*</span></span>

  - <span data-ttu-id="75070-142">Псевдоним, который ссылается на столбец главы, который был придан родительскому.</span><span class="sxs-lookup"><span data-stu-id="75070-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="75070-143">Предложение "родительский столбец к столбцу _-child-column"_ фактически является списком, где каждое определенное отношение отделяется запятой.</span><span class="sxs-lookup"><span data-stu-id="75070-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="75070-144">Предложение после ключевого слова APPEND фактически является списком, где каждое предложение отделяется запятой и определяет другой столбец, который необходимо примедить к родительскому.</span><span class="sxs-lookup"><span data-stu-id="75070-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="75070-145">Заметки</span><span class="sxs-lookup"><span data-stu-id="75070-145">Remarks</span></span>

<span data-ttu-id="75070-146">При построении команд поставщика из пользовательского ввода в рамках команды SHAPE shape обрабатывает предоставленную пользователем команду поставщика как непрозрачной строкой и передает их поставщику.</span><span class="sxs-lookup"><span data-stu-id="75070-146">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider.</span></span> <span data-ttu-id="75070-147">Например, в следующей команде SHAPE</span><span class="sxs-lookup"><span data-stu-id="75070-147">For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="75070-148">SHAPE выполнит две команды: выберите из t1 и \* (выберите \* из t2 RELATE k1 TO k2).</span><span class="sxs-lookup"><span data-stu-id="75070-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="75070-149">Если пользователь передает составную команду, состоящую из нескольких команд поставщика, разделенных точкими с заточки, SHAPE не сможет определить разницу.</span><span class="sxs-lookup"><span data-stu-id="75070-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="75070-150">Поэтому в следующей команде SHAPE:</span><span class="sxs-lookup"><span data-stu-id="75070-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="75070-151">SHAPE выполняется из t1; выпадая таблицу t1 и (выберите из \* t2 RELATE k1 TO k2), не понимая, что таблица drop t1 является отдельной и, в данном случае, опасной \* командой поставщика.</span><span class="sxs-lookup"><span data-stu-id="75070-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="75070-152">Приложения всегда должны проверять входные данные пользователя, чтобы предотвратить такие потенциальные атаки злоумышленников.</span><span class="sxs-lookup"><span data-stu-id="75070-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="75070-153">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="75070-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="75070-154">Operation of Non-Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="75070-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="75070-155">Operation of Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="75070-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="75070-156">Hybrid Commands</span><span class="sxs-lookup"><span data-stu-id="75070-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="75070-157">Intervening Shape COMPUTE Clauses</span><span class="sxs-lookup"><span data-stu-id="75070-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)
