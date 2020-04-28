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
# <a name="shape-append-clause"></a><span data-ttu-id="30d7a-102">Предложение Append команды Shape</span><span class="sxs-lookup"><span data-stu-id="30d7a-102">Shape Append clause</span></span>


<span data-ttu-id="30d7a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30d7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30d7a-104">Предложение APPEND команды Shape добавляет столбец или столбцы в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="30d7a-104">The shape command APPEND clause appends a column or columns to a **Recordset**.</span></span> <span data-ttu-id="30d7a-105">Часто эти столбцы являются столбцами главы, которые ссылаются на дочерний **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="30d7a-105">Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d7a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30d7a-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="30d7a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="30d7a-107">Description</span></span>

<span data-ttu-id="30d7a-108">Ниже приведен список частей этого предложения.</span><span class="sxs-lookup"><span data-stu-id="30d7a-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="30d7a-109">*родительская — команда*</span><span class="sxs-lookup"><span data-stu-id="30d7a-109">*parent-command*</span></span>

- <span data-ttu-id="30d7a-110">Ноль или один из следующих элементов ( *команда* может полностью пропускаться):</span><span class="sxs-lookup"><span data-stu-id="30d7a-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="30d7a-111">Команда поставщика в фигурных скобках ("{}"), которая возвращает объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="30d7a-111">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="30d7a-112">Команда выдается базовому поставщику данных, а его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="30d7a-112">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="30d7a-113">Как правило, это язык SQL, хотя для ADO не требуется определенный язык запросов.</span><span class="sxs-lookup"><span data-stu-id="30d7a-113">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="30d7a-114">Еще одна команда "Фигура", внедренная в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="30d7a-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="30d7a-115">Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="30d7a-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="30d7a-116">*псевдоним родителя*</span><span class="sxs-lookup"><span data-stu-id="30d7a-116">*parent-alias*</span></span>

  - <span data-ttu-id="30d7a-117">Необязательный псевдоним, ссылающийся на родительский **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="30d7a-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="30d7a-118">*Column (список)*</span><span class="sxs-lookup"><span data-stu-id="30d7a-118">*column-list*</span></span>

  - <span data-ttu-id="30d7a-119">Один или несколько из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="30d7a-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="30d7a-120">Сводный столбец.</span><span class="sxs-lookup"><span data-stu-id="30d7a-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="30d7a-121">Вычисляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="30d7a-121">A calculated column.</span></span>
    
    - <span data-ttu-id="30d7a-122">Новый столбец, созданный с помощью оператора NEW.</span><span class="sxs-lookup"><span data-stu-id="30d7a-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="30d7a-123">Столбец главы.</span><span class="sxs-lookup"><span data-stu-id="30d7a-123">A chapter column.</span></span> <span data-ttu-id="30d7a-124">Определение столбца главы заключено в круглые скобки ("()").</span><span class="sxs-lookup"><span data-stu-id="30d7a-124">A chapter column definition is enclosed in parentheses ("()").</span></span> <span data-ttu-id="30d7a-125">Ниже приведен синтаксис:</span><span class="sxs-lookup"><span data-stu-id="30d7a-125">See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="30d7a-126">*дочерний набор записей*</span><span class="sxs-lookup"><span data-stu-id="30d7a-126">*child-recordset*</span></span>

  - <span data-ttu-id="30d7a-127">Команда поставщика в фигурных скобках ("{}"), которая возвращает объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="30d7a-127">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="30d7a-128">Команда выдается базовому поставщику данных, а его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="30d7a-128">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="30d7a-129">Как правило, это язык SQL, хотя для ADO не требуется определенный язык запросов.</span><span class="sxs-lookup"><span data-stu-id="30d7a-129">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="30d7a-130">Еще одна команда "Фигура", внедренная в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="30d7a-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="30d7a-131">Имя существующего **набора записей**в форме.</span><span class="sxs-lookup"><span data-stu-id="30d7a-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="30d7a-132">Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="30d7a-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="30d7a-133">*дочерний псевдоним*</span><span class="sxs-lookup"><span data-stu-id="30d7a-133">*child-alias*</span></span>

  - <span data-ttu-id="30d7a-134">Псевдоним, ссылающийся на дочерний **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="30d7a-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="30d7a-135">*родительский столбец*</span><span class="sxs-lookup"><span data-stu-id="30d7a-135">*parent-column*</span></span>

  - <span data-ttu-id="30d7a-136">Столбец в **наборе записей** , возвращенный *родительской командой.*</span><span class="sxs-lookup"><span data-stu-id="30d7a-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="30d7a-137">*дочерний столбец*</span><span class="sxs-lookup"><span data-stu-id="30d7a-137">*child-column*</span></span>

  - <span data-ttu-id="30d7a-138">Столбец в **наборе записей** , возвращенный *дочерней командой*.</span><span class="sxs-lookup"><span data-stu-id="30d7a-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="30d7a-139">*Param — Number*</span><span class="sxs-lookup"><span data-stu-id="30d7a-139">*param-number*</span></span>

  - <span data-ttu-id="30d7a-140">Просмотр [действий с параметризованными командами](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="30d7a-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="30d7a-141">*Глава — псевдоним*</span><span class="sxs-lookup"><span data-stu-id="30d7a-141">*chapter-alias*</span></span>

  - <span data-ttu-id="30d7a-142">Псевдоним, ссылающийся на столбец Chapter, добавляемый к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="30d7a-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="30d7a-143">Предложение _"родительский столбец для дочернего столбца"_ фактически является списком, где каждое определенное отношение отделяется запятой.</span><span class="sxs-lookup"><span data-stu-id="30d7a-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="30d7a-144">В действительности предложение после ключевого слова APPEND представляет собой список, в котором каждое предложение отделяется запятой и определяет другой столбец, добавляемый к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="30d7a-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="30d7a-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="30d7a-145">Remarks</span></span>

<span data-ttu-id="30d7a-146">Когда вы создаете команды поставщика из входных данных пользователя в составе команды SHAPE, SHAPE будет рассматривать указанную пользователем команду поставщика как непрозрачную строку и передавать их в поставщике.</span><span class="sxs-lookup"><span data-stu-id="30d7a-146">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider.</span></span> <span data-ttu-id="30d7a-147">Например, в следующей команде SHAPE</span><span class="sxs-lookup"><span data-stu-id="30d7a-147">For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="30d7a-148">Фигура будет выполнять две команды: выбрать \* из T1 и (выбрать \* из T2 связать K1 с K2).</span><span class="sxs-lookup"><span data-stu-id="30d7a-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="30d7a-149">Если пользователь предоставляет составную команду, состоящую из нескольких команд поставщика, разделенных точкой с запятой, фигура не может различать различия.</span><span class="sxs-lookup"><span data-stu-id="30d7a-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="30d7a-150">Поэтому в следующей команде SHAPE</span><span class="sxs-lookup"><span data-stu-id="30d7a-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="30d7a-151">ФИГУРА выполняет SELECT \* из T1; Drop Table T1 и (Select \* from T2 K1 to K2), не зная, что инструкция DROP TABLE T1 является отдельным и в данном случае опасной команды поставщика.</span><span class="sxs-lookup"><span data-stu-id="30d7a-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="30d7a-152">Приложения всегда должны проверять входные данные пользователя, чтобы предотвратить возникновение подобных потенциальных атак хакеров.</span><span class="sxs-lookup"><span data-stu-id="30d7a-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="30d7a-153">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="30d7a-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="30d7a-154">Operation of Non-Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="30d7a-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="30d7a-155">Operation of Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="30d7a-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="30d7a-156">Hybrid Commands</span><span class="sxs-lookup"><span data-stu-id="30d7a-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="30d7a-157">Intervening Shape COMPUTE Clauses</span><span class="sxs-lookup"><span data-stu-id="30d7a-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)
