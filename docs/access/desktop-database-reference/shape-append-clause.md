---
title: Предложение добавления фигуры
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb8e60c52ded359350adff737807c3e0f92cb7c4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862128"
---
# <a name="shape-append-clause"></a><span data-ttu-id="6c7ce-102">Предложение добавления фигуры</span><span class="sxs-lookup"><span data-stu-id="6c7ce-102">Shape Append Clause</span></span>


<span data-ttu-id="6c7ce-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c7ce-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6c7ce-104">Предложение APPEND фигуры команда добавляет столбец или столбцы **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-104">The shape command APPEND clause appends a column or columns to a **Recordset**.</span></span> <span data-ttu-id="6c7ce-105">Часто эти столбцы, главы столбцов, которые ссылаться на дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-105">Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c7ce-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="6c7ce-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6c7ce-107">Description</span></span>

<span data-ttu-id="6c7ce-108">Части это предложение, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c7ce-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="6c7ce-109">*родительский command*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-109">*parent-command*</span></span>

- <span data-ttu-id="6c7ce-110">Ноль или один из следующих значений (может опустить *родительского команда* полностью):</span><span class="sxs-lookup"><span data-stu-id="6c7ce-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="6c7ce-111">Команды поставщика в фигурные скобки (»{}«), которое возвращает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6c7ce-111">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="6c7ce-112">Команды для базового поставщика данных, и его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-112">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="6c7ce-113">Обычно это будет языка SQL, несмотря на то, что ADO не требуется любой язык, определенного запроса.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-113">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="6c7ce-114">Другую фигуру, команда внедренные в скобки.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="6c7ce-115">В ТАБЛИЦЕ ключевого слова, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="6c7ce-116">*родительский псевдоним*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-116">*parent-alias*</span></span>

  - <span data-ttu-id="6c7ce-117">Необязательный псевдоним, который относится к родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="6c7ce-118">*Список столбцов*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-118">*column-list*</span></span>

  - <span data-ttu-id="6c7ce-119">Одно или несколько из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="6c7ce-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="6c7ce-120">Составного столбца.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="6c7ce-121">Вычисляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-121">A calculated column.</span></span>
    
    - <span data-ttu-id="6c7ce-122">Новый столбец, созданных с помощью оператора NEW.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="6c7ce-123">Столбец.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-123">A chapter column.</span></span> <span data-ttu-id="6c7ce-124">Определение столбца главы заключается в круглые скобки («()»).</span><span class="sxs-lookup"><span data-stu-id="6c7ce-124">A chapter column definition is enclosed in parentheses ("()").</span></span> <span data-ttu-id="6c7ce-125">Можно найти описанных ниже:</span><span class="sxs-lookup"><span data-stu-id="6c7ce-125">See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="6c7ce-126">*дочерних наборов записей*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-126">*child-recordset*</span></span>

  - <span data-ttu-id="6c7ce-127">Команды поставщика в фигурные скобки (»{}«), которое возвращает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6c7ce-127">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="6c7ce-128">Команды для базового поставщика данных, и его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-128">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="6c7ce-129">Обычно это будет языка SQL, несмотря на то, что ADO не требуется любой язык, определенного запроса.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-129">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="6c7ce-130">Другую фигуру, команда внедренные в скобки.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="6c7ce-131">Имя существующего форме **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="6c7ce-132">В ТАБЛИЦЕ ключевого слова, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="6c7ce-133">*псевдоним дочерних*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-133">*child-alias*</span></span>

  - <span data-ttu-id="6c7ce-134">Псевдоним, который относится к дочерним **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="6c7ce-135">*родительский столбец*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-135">*parent-column*</span></span>

  - <span data-ttu-id="6c7ce-136">Столбец в **набор записей** , возвращаемых *родительский command.*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="6c7ce-137">*дочерний столбец*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-137">*child-column*</span></span>

  - <span data-ttu-id="6c7ce-138">Столбец в **набор записей** , возвращаемых *дочерних command*.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="6c7ce-139">*число параметров*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-139">*param-number*</span></span>

  - <span data-ttu-id="6c7ce-140">В разделе [операция параметризованные команды](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="6c7ce-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="6c7ce-141">*псевдоним главы*</span><span class="sxs-lookup"><span data-stu-id="6c7ce-141">*chapter-alias*</span></span>

  - <span data-ttu-id="6c7ce-142">Псевдоним, который относится к главе столбец, добавляемый в родительском.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="6c7ce-143">Предложение _«Кому родительского столбца дочерних столбца»_ является списком, где каждого отношения определенные разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="6c7ce-144">Предложение после ключевого слова APPEND является фактически список, где каждое предложение разделенных точкой с запятой и определяет другого столбца для добавления к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="6c7ce-145">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c7ce-145">Remarks</span></span>

<span data-ttu-id="6c7ce-146">При построении команды поставщика из введенных пользователем данных как часть команды ФИГУРЫ ФИГУРА считать пользовательские команды поставщика непрозрачную строку и передавайте их точно к поставщику.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-146">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider.</span></span> <span data-ttu-id="6c7ce-147">Например в следующую команду ФИГУРЫ</span><span class="sxs-lookup"><span data-stu-id="6c7ce-147">For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="6c7ce-148">ФИГУРА будет выполняться две команды: выберите \* из t1 и (выберите \* из t2 ссылка k1 кому k2).</span><span class="sxs-lookup"><span data-stu-id="6c7ce-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="6c7ce-149">Если пользователь указал составные команды, состоящий из нескольких команд поставщика, разделенных точкой с запятой, ФИГУРА не сможет понять разницу.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="6c7ce-150">В следующей командой с ФИГУРЫ</span><span class="sxs-lookup"><span data-stu-id="6c7ce-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="6c7ce-151">ФИГУРА выполняет выберите \* из t1; Поместите таблицы t1 и (выберите \* из t2 ссылка k1 кому k2), не осознавать, входящей в таблице t1 является отдельным и в этой команде делами, опасной, поставщика.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="6c7ce-152">Приложения всегда должны проверить пользователем данные, чтобы предотвратить такие потенциальных атак злоумышленников.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="6c7ce-153">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="6c7ce-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="6c7ce-154">Операция для команд без параметров</span><span class="sxs-lookup"><span data-stu-id="6c7ce-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="6c7ce-155">Операция для команд с параметрами</span><span class="sxs-lookup"><span data-stu-id="6c7ce-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="6c7ce-156">Гибридные команды</span><span class="sxs-lookup"><span data-stu-id="6c7ce-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="6c7ce-157">Предложения COMPUTE для промежуточных фигур</span><span class="sxs-lookup"><span data-stu-id="6c7ce-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)