---
title: Использование ADO с Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8644bd4f5b1a19848689adf92dca91ba30f324c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889849"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="2d7ee-102">Использование ADO с Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2d7ee-102">Using ADO with Microsoft Visual Basic</span></span>


<span data-ttu-id="2d7ee-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d7ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d7ee-104">Подготовка проекта ADO и написания кода ADO аналогичен использование Visual Basic или Visual Basic для приложений.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-104">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications.</span></span> <span data-ttu-id="2d7ee-105">Этот раздел описывает использование ADO в Visual Basic и Visual Basic для приложений и заметки о все различия.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-105">This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="2d7ee-106">Создание ссылок на библиотеку ADO</span><span class="sxs-lookup"><span data-stu-id="2d7ee-106">Referencing the ADO Library</span></span>

<span data-ttu-id="2d7ee-107">Должна быть указана библиотека ADO файлов проекта.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-107">The ADO library must be referenced by your project.</span></span>

<span data-ttu-id="2d7ee-108">**Для ссылки ADO из Microsoft Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="2d7ee-108">**To reference ADO from Microsoft Visual Basic**</span></span>

1.  <span data-ttu-id="2d7ee-109">В Visual Basic в меню **проект** выберите **ссылки...**.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2.  <span data-ttu-id="2d7ee-110">Выберите в списке **Microsoft ActiveX Data Objects x.x библиотеки** .</span><span class="sxs-lookup"><span data-stu-id="2d7ee-110">Select **Microsoft ActiveX Data Objects x.x Library** from the list.</span></span> <span data-ttu-id="2d7ee-111">Убедитесь, что по крайней мере следующие библиотеки также выбраны:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-111">Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="2d7ee-112">Visual Basic для приложений</span><span class="sxs-lookup"><span data-stu-id="2d7ee-112">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="2d7ee-113">Объекты среды выполнения Visual Basic и процедуры</span><span class="sxs-lookup"><span data-stu-id="2d7ee-113">Visual Basic runtime objects and procedures</span></span>
    
    - <span data-ttu-id="2d7ee-114">Visual Basic объекты и процедуры</span><span class="sxs-lookup"><span data-stu-id="2d7ee-114">Visual Basic objects and procedures</span></span>
    
    - <span data-ttu-id="2d7ee-115">OLE-автоматизации</span><span class="sxs-lookup"><span data-stu-id="2d7ee-115">OLE Automation</span></span>

3.  <span data-ttu-id="2d7ee-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-116">Click **OK**.</span></span>

<span data-ttu-id="2d7ee-117">Можно использовать ADO так же легко, с помощью Visual Basic для приложений, например с помощью Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

<span data-ttu-id="2d7ee-118">**Для ссылки ADO из Microsoft Access**</span><span class="sxs-lookup"><span data-stu-id="2d7ee-118">**To reference ADO from Microsoft Access**</span></span>

1.  <span data-ttu-id="2d7ee-119">В Microsoft Access выберите или создайте модуль из вкладки **модулей** в окне **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="2d7ee-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2.  <span data-ttu-id="2d7ee-120">В меню **Сервис** выберите пункт **ссылки...**.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-120">From the **Tools** menu, select **References...**.</span></span>

3.  <span data-ttu-id="2d7ee-121">Выберите в списке **Microsoft ActiveX Data Objects x.x библиотеки** .</span><span class="sxs-lookup"><span data-stu-id="2d7ee-121">Select **Microsoft ActiveX Data Objects x.x Library** from the list.</span></span> <span data-ttu-id="2d7ee-122">Убедитесь, что по крайней мере следующие библиотеки также выбраны:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-122">Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="2d7ee-123">Visual Basic для приложений</span><span class="sxs-lookup"><span data-stu-id="2d7ee-123">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="2d7ee-124">Библиотека объектов Microsoft Access 11.0 (или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="2d7ee-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4.  <span data-ttu-id="2d7ee-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="2d7ee-126">Создание объектов ADO в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2d7ee-126">Creating ADO Objects in Visual Basic</span></span>

<span data-ttu-id="2d7ee-127">Чтобы создать переменную автоматизации и экземпляр объекта для этой переменной, можно использовать два метода: **Dim** или **CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

## <a name="dim"></a><span data-ttu-id="2d7ee-128">Dim</span><span class="sxs-lookup"><span data-stu-id="2d7ee-128">Dim</span></span>

<span data-ttu-id="2d7ee-129">Можно использовать ключевое слово **New** с **Dim** для объявите и создайте объекты ADO в один шаг:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="2d7ee-130">Кроме того **Dim** оператор объявления и создания экземпляра объекта также может быть два действия:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```


> [!NOTE]
> <P><span data-ttu-id="2d7ee-131">Не требуется явно использовать ADODB progid с помощью оператора <STRONG>Dim</STRONG> , при условии, что правильно ссылка на библиотеку ADO в проекте.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-131">It is not required to explicitly use the ADODB progid with the <STRONG>Dim</STRONG> statement, assuming you have properly referenced the ADO library in your project.</span></span> <span data-ttu-id="2d7ee-132">Тем не менее с его помощью гарантирует, что не будут иметь конфликтов с другими библиотеками имен.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-132">However, using it ensures that you won't have naming conflicts with other libraries.</span></span></P>



<span data-ttu-id="2d7ee-133">Например справочные материалы, которые ADO и DAO включается в одном проекте, необходимо включить квалификатор, чтобы указать, какие объектной модели для использования при создании объектов **наборов записей** , как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
<span data-ttu-id="2d7ee-134">Dim adoRS как ADODB. Набор записей</span><span class="sxs-lookup"><span data-stu-id="2d7ee-134">Dim adoRS As ADODB.Recordset</span></span>  
  
<span data-ttu-id="2d7ee-135">Dim daoRS как DAO. Набор записей</span><span class="sxs-lookup"><span data-stu-id="2d7ee-135">Dim daoRS As DAO.Recordset</span></span>

## <a name="createobject"></a><span data-ttu-id="2d7ee-136">Функция CreateObject</span><span class="sxs-lookup"><span data-stu-id="2d7ee-136">CreateObject</span></span>

<span data-ttu-id="2d7ee-137">С помощью **CreateObject** метод, объявления и создания экземпляра объекта должно быть два отдельных действий:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-137">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="2d7ee-138">Объекты с **CreateObject** экземпляр позднего связывания, что означает, что они не являются строго типизированным и отключается командной строки завершения.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-138">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled.</span></span> <span data-ttu-id="2d7ee-139">Тем не менее он позволяет пропустить ссылки на библиотеку ADO из проекта и позволяет создавать экземпляры определенных версий объектов.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-139">However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects.</span></span> <span data-ttu-id="2d7ee-140">Пример:</span><span class="sxs-lookup"><span data-stu-id="2d7ee-140">For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="2d7ee-141">Может также этого, а именно создание ссылки на библиотеку ADO версии 2.0 тип и создания объекта.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-141">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="2d7ee-142">Создание экземпляров объектов с помощью метода **CreateObject** обычно более медленными, чем с помощью оператора **Dim** .</span><span class="sxs-lookup"><span data-stu-id="2d7ee-142">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="2d7ee-143">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="2d7ee-143">Handling Events</span></span>

<span data-ttu-id="2d7ee-144">Для обработки событий ADO в Microsoft Visual Basic, необходимо объявить переменную уровня модуля, с помощью ключевое слово **WithEvents** .</span><span class="sxs-lookup"><span data-stu-id="2d7ee-144">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword.</span></span> <span data-ttu-id="2d7ee-145">Переменная может быть объявлен только как часть модуль класса и должны быть объявлены на уровне модуля.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-145">The variable can be declared only as part of a class module and must be declared at the module level.</span></span> <span data-ttu-id="2d7ee-146">Более подробные сведения об обработке событий ADO, в разделе [Глава 7: обработка событий ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="2d7ee-146">For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="2d7ee-147">Примеры Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2d7ee-147">Visual Basic Examples</span></span>

<span data-ttu-id="2d7ee-148">Многие примеры Visual Basic включены в документации по ADO.</span><span class="sxs-lookup"><span data-stu-id="2d7ee-148">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="2d7ee-149">Для получения дополнительных сведений см [ADO в Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="2d7ee-149">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>

