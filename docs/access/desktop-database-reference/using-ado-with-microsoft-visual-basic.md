---
title: Использование ADO с Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26eaa93a1abbb3778a2735d50dd5022edb3023d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306225"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="b677c-102">Использование ADO с Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b677c-102">Using ADO with Microsoft Visual Basic</span></span>

<span data-ttu-id="b677c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b677c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b677c-104">Настройка проекта ADO и написание кода ADO аналогичны, независимо от того, используете ли вы Visual Basic или Visual Basic для приложений.</span><span class="sxs-lookup"><span data-stu-id="b677c-104">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications.</span></span> <span data-ttu-id="b677c-105">В этом разделе рассматривается использование ADO вместе с Visual Basic и Visual Basic для приложений, а также заметок о различиях.</span><span class="sxs-lookup"><span data-stu-id="b677c-105">This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="b677c-106">Создание ссылок на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="b677c-106">Referencing the ADO library</span></span>

<span data-ttu-id="b677c-107">Проект ADO должен ссылаться на библиотеку ADO.</span><span class="sxs-lookup"><span data-stu-id="b677c-107">The ADO library must be referenced by your project.</span></span>

### <a name="to-reference-ado-from-microsoft-visual-basic"></a><span data-ttu-id="b677c-108">Ссылка на ADO из Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b677c-108">To reference ADO from Microsoft Visual Basic</span></span>

1. <span data-ttu-id="b677c-109">В Visual Basic в меню **проект** выберите **ссылки...**.</span><span class="sxs-lookup"><span data-stu-id="b677c-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2. <span data-ttu-id="b677c-110">Выберите **библиотеку Microsoft ActiveX Data Objects x. x** из списка.</span><span class="sxs-lookup"><span data-stu-id="b677c-110">Select **Microsoft ActiveX Data Objects x.x Library** from the list.</span></span> <span data-ttu-id="b677c-111">Убедитесь, что также выбраны по крайней мере следующие библиотеки:</span><span class="sxs-lookup"><span data-stu-id="b677c-111">Verify that at least the following libraries are also selected:</span></span>
   
   - <span data-ttu-id="b677c-112">Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="b677c-112">Visual Basic for Applications</span></span>
   - <span data-ttu-id="b677c-113">Объекты и процедуры среды выполнения Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b677c-113">Visual Basic runtime objects and procedures</span></span>
   - <span data-ttu-id="b677c-114">Объекты и процедуры Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b677c-114">Visual Basic objects and procedures</span></span>
   - <span data-ttu-id="b677c-115">OLE Automation</span><span class="sxs-lookup"><span data-stu-id="b677c-115">OLE Automation</span></span>

3. <span data-ttu-id="b677c-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b677c-116">Click **OK**.</span></span>

<span data-ttu-id="b677c-117">Вы можете использовать ADO так же, как и в Visual Basic для приложений, например, с помощью Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b677c-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

### <a name="to-reference-ado-from-microsoft-access"></a><span data-ttu-id="b677c-118">Ссылка на ADO из Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="b677c-118">To reference ADO from Microsoft Access</span></span>

1. <span data-ttu-id="b677c-119">В Microsoft Access выберите или создайте модуль на вкладке **модули** окна **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="b677c-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2. <span data-ttu-id="b677c-120">В меню **Сервис** выберите пункт **ссылки..**..</span><span class="sxs-lookup"><span data-stu-id="b677c-120">From the **Tools** menu, select **References...**.</span></span>

3. <span data-ttu-id="b677c-121">Выберите **библиотеку Microsoft ActiveX Data Objects x. x** из списка.</span><span class="sxs-lookup"><span data-stu-id="b677c-121">Select **Microsoft ActiveX Data Objects x.x Library** from the list.</span></span> <span data-ttu-id="b677c-122">Убедитесь, что также выбраны по крайней мере следующие библиотеки:</span><span class="sxs-lookup"><span data-stu-id="b677c-122">Verify that at least the following libraries are also selected:</span></span>
    
   - <span data-ttu-id="b677c-123">Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="b677c-123">Visual Basic for Applications</span></span>
   - <span data-ttu-id="b677c-124">Библиотека объектов Microsoft Access 11,0 (или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="b677c-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4. <span data-ttu-id="b677c-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b677c-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="b677c-126">Создание объектов ADO в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b677c-126">Creating ADO objects in Visual Basic</span></span>

<span data-ttu-id="b677c-127">Чтобы создать переменную автоматизации и экземпляр объекта для этой переменной, можно использовать два метода: **Dim** или **CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="b677c-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

### <a name="dim"></a><span data-ttu-id="b677c-128">Dim</span><span class="sxs-lookup"><span data-stu-id="b677c-128">Dim</span></span>

<span data-ttu-id="b677c-129">Вы можете использовать ключевое слово **New** с **Dim** для объявления и создания экземпляров объектов ADO за один шаг:</span><span class="sxs-lookup"><span data-stu-id="b677c-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="b677c-130">Кроме того, объявление оператора **Dim** и создание экземпляра объекта также могут быть двумя этапами:</span><span class="sxs-lookup"><span data-stu-id="b677c-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> <span data-ttu-id="b677c-131">Нет необходимости явно использовать ProgID ADODB с оператором **Dim** , предполагая, что вы правильно ссылались на библиотеку ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="b677c-131">It is not required to explicitly use the ADODB progid with the **Dim** statement, assuming you have properly referenced the ADO library in your project.</span></span> <span data-ttu-id="b677c-132">Тем не менее, использование этого параметра гарантирует, что конфликты имен с другими библиотеками не будут.</span><span class="sxs-lookup"><span data-stu-id="b677c-132">However, using it ensures that you won't have naming conflicts with other libraries.</span></span>
> 
> <span data-ttu-id="b677c-133">Например, если вы включили в один проект ссылки на ADO и DAO, необходимо добавить квалификатор, указывающий, какую объектную модель использовать при создании экземпляров объектов **Recordset** , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="b677c-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a><span data-ttu-id="b677c-134">CreateObject</span><span class="sxs-lookup"><span data-stu-id="b677c-134">CreateObject</span></span>

<span data-ttu-id="b677c-135">При использовании метода **CreateObject** объявление и создание экземпляра объекта должны быть выполнены в два отдельных этапа:</span><span class="sxs-lookup"><span data-stu-id="b677c-135">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="b677c-136">Объекты, создаваемые с помощью **CreateObject** , имеют тип с поздней привязкой, что означает, что они не являются строго типизированными, а завершение командной строки отключено.</span><span class="sxs-lookup"><span data-stu-id="b677c-136">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled.</span></span> <span data-ttu-id="b677c-137">Тем не менее, это позволяет пропустить ссылку на библиотеку ADO из проекта и создать экземпляры определенных версий объектов.</span><span class="sxs-lookup"><span data-stu-id="b677c-137">However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects.</span></span> <span data-ttu-id="b677c-138">Пример:</span><span class="sxs-lookup"><span data-stu-id="b677c-138">For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="b677c-139">Это также можно сделать, специально создав ссылку на библиотеку типов ADO версии 2,0 и создав объект.</span><span class="sxs-lookup"><span data-stu-id="b677c-139">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="b677c-140">Создание экземпляров объектов с помощью метода **CreateObject** обычно выполняется медленнее, чем при использовании оператора **Dim** .</span><span class="sxs-lookup"><span data-stu-id="b677c-140">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="b677c-141">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="b677c-141">Handling events</span></span>

<span data-ttu-id="b677c-142">Для обработки событий ADO в Microsoft Visual Basic необходимо объявить переменную на уровне модуля с помощью ключевого слова **WithEvents** .</span><span class="sxs-lookup"><span data-stu-id="b677c-142">To handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword.</span></span> <span data-ttu-id="b677c-143">Переменная может быть объявлена только как часть модуля класса и должна быть объявлена на уровне модуля.</span><span class="sxs-lookup"><span data-stu-id="b677c-143">The variable can be declared only as part of a class module and must be declared at the module level.</span></span> <span data-ttu-id="b677c-144">Более подробное описание обработки событий ADO приведено в [главе 7: обработка событий ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="b677c-144">For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="b677c-145">Примеры Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b677c-145">Visual Basic examples</span></span>

<span data-ttu-id="b677c-146">Многие примеры Visual Basic включены в документацию по ADO.</span><span class="sxs-lookup"><span data-stu-id="b677c-146">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="b677c-147">Дополнительные сведения приведены [в статье примеры кода ADO в Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="b677c-147">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>

