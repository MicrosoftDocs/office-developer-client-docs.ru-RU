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
# <a name="shape-append-clause"></a><span data-ttu-id="49a12-102">Предложение Append команды Shape</span><span class="sxs-lookup"><span data-stu-id="49a12-102">Shape Append clause</span></span>


<span data-ttu-id="49a12-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49a12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49a12-104">Положение appEND команды фигуры примыкает столбец или столбцы к **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="49a12-104">The shape command APPEND clause appends a column or columns to a **Recordset**.</span></span> <span data-ttu-id="49a12-105">Часто эти столбцы являются столбцами глав, которые относятся к детскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="49a12-105">Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a12-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49a12-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="49a12-107">Описание</span><span class="sxs-lookup"><span data-stu-id="49a12-107">Description</span></span>

<span data-ttu-id="49a12-108">Части этого положения:</span><span class="sxs-lookup"><span data-stu-id="49a12-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="49a12-109">*родительская команда*</span><span class="sxs-lookup"><span data-stu-id="49a12-109">*parent-command*</span></span>

- <span data-ttu-id="49a12-110">Ноль или один из следующих (можно полностью отопустить *родительную* команду):</span><span class="sxs-lookup"><span data-stu-id="49a12-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="49a12-111">Команда поставщика в фигурных скобки ("), которая {} возвращает **объект Recordset.**</span><span class="sxs-lookup"><span data-stu-id="49a12-111">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="49a12-112">Команда выдана основному поставщику данных, и ее синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="49a12-112">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="49a12-113">Обычно это будет язык SQL, хотя ADO не требует какого-либо конкретного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="49a12-113">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="49a12-114">Еще одна команда фигуры, встроенная в скобки.</span><span class="sxs-lookup"><span data-stu-id="49a12-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="49a12-115">Ключевое слово TABLE с именем таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="49a12-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="49a12-116">*родительский псевдоним*</span><span class="sxs-lookup"><span data-stu-id="49a12-116">*parent-alias*</span></span>

  - <span data-ttu-id="49a12-117">Необязательный псевдоним, который относится к родительскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="49a12-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="49a12-118">*столбец-список*</span><span class="sxs-lookup"><span data-stu-id="49a12-118">*column-list*</span></span>

  - <span data-ttu-id="49a12-119">Один или несколько из следующих ниже.</span><span class="sxs-lookup"><span data-stu-id="49a12-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="49a12-120">Сводный столбец.</span><span class="sxs-lookup"><span data-stu-id="49a12-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="49a12-121">Вычислимый столбец.</span><span class="sxs-lookup"><span data-stu-id="49a12-121">A calculated column.</span></span>
    
    - <span data-ttu-id="49a12-122">Новый столбец, созданный с новым предложением.</span><span class="sxs-lookup"><span data-stu-id="49a12-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="49a12-123">Столбец главы.</span><span class="sxs-lookup"><span data-stu-id="49a12-123">A chapter column.</span></span> <span data-ttu-id="49a12-124">Определение столбца главы заключено в скобки ("()").</span><span class="sxs-lookup"><span data-stu-id="49a12-124">A chapter column definition is enclosed in parentheses ("()").</span></span> <span data-ttu-id="49a12-125">См. синтаксис ниже:</span><span class="sxs-lookup"><span data-stu-id="49a12-125">See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="49a12-126">*набор записей для детей*</span><span class="sxs-lookup"><span data-stu-id="49a12-126">*child-recordset*</span></span>

  - <span data-ttu-id="49a12-127">Команда поставщика в фигурных скобки ("), которая {} возвращает **объект Recordset.**</span><span class="sxs-lookup"><span data-stu-id="49a12-127">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="49a12-128">Команда выдана основному поставщику данных, и ее синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="49a12-128">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="49a12-129">Обычно это будет язык SQL, хотя ADO не требует какого-либо конкретного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="49a12-129">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="49a12-130">Еще одна команда фигуры, встроенная в скобки.</span><span class="sxs-lookup"><span data-stu-id="49a12-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="49a12-131">Имя существующего формы **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="49a12-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="49a12-132">Ключевое слово TABLE с именем таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="49a12-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="49a12-133">*псевдоним ребенка*</span><span class="sxs-lookup"><span data-stu-id="49a12-133">*child-alias*</span></span>

  - <span data-ttu-id="49a12-134">Псевдоним, который относится к детскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="49a12-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="49a12-135">*родитель-столбец*</span><span class="sxs-lookup"><span data-stu-id="49a12-135">*parent-column*</span></span>

  - <span data-ttu-id="49a12-136">Столбец в **наборе записей,** возвращаемом *родительской командой.*</span><span class="sxs-lookup"><span data-stu-id="49a12-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="49a12-137">*столбец child-column*</span><span class="sxs-lookup"><span data-stu-id="49a12-137">*child-column*</span></span>

  - <span data-ttu-id="49a12-138">Столбец в **Наборе записей,** возвращенный *детской командой.*</span><span class="sxs-lookup"><span data-stu-id="49a12-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="49a12-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="49a12-139">*param-number*</span></span>

  - <span data-ttu-id="49a12-140">См. [операцию параметризированных команд.](operation-of-parameterized-commands.md)</span><span class="sxs-lookup"><span data-stu-id="49a12-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="49a12-141">*псевдоним главы*</span><span class="sxs-lookup"><span data-stu-id="49a12-141">*chapter-alias*</span></span>

  - <span data-ttu-id="49a12-142">Псевдоним, который ссылается на столбец главы, приданный родительскому.</span><span class="sxs-lookup"><span data-stu-id="49a12-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="49a12-143">Положение _"родительский столбец для ребенка-столбца"_ на самом деле является списком, где каждое определенное отношение разделено запятой.</span><span class="sxs-lookup"><span data-stu-id="49a12-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="49a12-144">Пункт после ключевого слова APPEND фактически является списком, где каждый пункт разделяется запятой и определяет другой столбец, который должен быть придан родительскому.</span><span class="sxs-lookup"><span data-stu-id="49a12-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="49a12-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="49a12-145">Remarks</span></span>

<span data-ttu-id="49a12-146">При построении команд поставщика из входных данных пользователя в составе команды SHAPE SHAPE будет рассматривать команду поставщика, предоставленную пользователем, как непрозрачной строки, и передавать их поставщику.</span><span class="sxs-lookup"><span data-stu-id="49a12-146">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider.</span></span> <span data-ttu-id="49a12-147">Например, в следующей команде SHAPE</span><span class="sxs-lookup"><span data-stu-id="49a12-147">For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="49a12-148">SHAPE выполнит две команды: выберите из t1 и (выберите из \* \* t2 RELATE k1 TO k2).</span><span class="sxs-lookup"><span data-stu-id="49a12-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="49a12-149">Если пользователь поставляет комплексную команду, состоящую из нескольких команд поставщика, разделенных зайколонами, SHAPE не сможет различить разницу.</span><span class="sxs-lookup"><span data-stu-id="49a12-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="49a12-150">Итак, в следующей команде SHAPE</span><span class="sxs-lookup"><span data-stu-id="49a12-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="49a12-151">SHAPE выполняет выбор из t1; drop table t1 и (выберите из \* t2 RELATE k1 to k2), не понимая, что таблица drop table t1 является отдельной и в этом случае опасной \* командой поставщика.</span><span class="sxs-lookup"><span data-stu-id="49a12-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="49a12-152">Приложения всегда должны проверять вход пользователя, чтобы предотвратить такие потенциальные хакерские атаки.</span><span class="sxs-lookup"><span data-stu-id="49a12-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="49a12-153">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="49a12-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="49a12-154">Operation of Non-Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="49a12-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="49a12-155">Operation of Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="49a12-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="49a12-156">Hybrid Commands</span><span class="sxs-lookup"><span data-stu-id="49a12-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="49a12-157">Intervening Shape COMPUTE Clauses</span><span class="sxs-lookup"><span data-stu-id="49a12-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)
