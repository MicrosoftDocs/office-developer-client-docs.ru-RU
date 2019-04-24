---
title: Программирование для ADO на Visual C++
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a890b4906fb9f207f12ff17ef0d3ccf1a97a44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302774"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="49599-102">Программирование для ADO на Visual C++</span><span class="sxs-lookup"><span data-stu-id="49599-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="49599-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49599-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49599-104">Справочник по API ADO описывает функциональные возможности API-интерфейса ADO, используя синтаксис, похожий на Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="49599-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="49599-105">Хотя предполагаемая аудитория — это все пользователи, программисты ADO используют различные языки, такие как Visual Basic, Visual C++ (с директивой \*\* \#Import\*\* и без нее), и Visual J++ (с пакетом классов ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="49599-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="49599-106">В соответствии с этим разнообразием [индексы синтаксиса ADO для Visual c++](using-ado-with-microsoft-visual-c.md) предоставляют языковой синтаксис Visual c++ со ссылками на общие описания функций, параметров, исключительных поведений и т. д. в справочнике по API.</span><span class="sxs-lookup"><span data-stu-id="49599-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="49599-107">ADO реализован с помощью интерфейсов COM (компонентной объектной модели).</span><span class="sxs-lookup"><span data-stu-id="49599-107">ADO is implemented with COM (Component Object Model) interfaces.</span></span> <span data-ttu-id="49599-108">Однако программисты легче работают с COM на определенных языках программирования, чем другие.</span><span class="sxs-lookup"><span data-stu-id="49599-108">However, it is easier for programmers to work with COM in certain programming languages than others.</span></span> <span data-ttu-id="49599-109">Например, почти все детали использования COM неявно обрабатываются для программистов Visual Basic, а программисты Visual C++ должны присутствовать на этих сведениях.</span><span class="sxs-lookup"><span data-stu-id="49599-109">For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="49599-110">В следующих разделах приведена сводка сведений для программистов C и C++, использующих ADO и директиву \*\* \#Import\*\* .</span><span class="sxs-lookup"><span data-stu-id="49599-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="49599-111">Он посвящен типам данных, характерным для COM (**Variant**, **BSTR**и **SAFEARRAY**), а также обработке ошибок\_(\_ошибках com).</span><span class="sxs-lookup"><span data-stu-id="49599-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="49599-112">Использование директивы компилятора \#импорта</span><span class="sxs-lookup"><span data-stu-id="49599-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="49599-113">Директива компилятора \*\* \#Import\*\* Visual C++ упрощает работу с методами и свойствами ADO.</span><span class="sxs-lookup"><span data-stu-id="49599-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="49599-114">Директива принимает имя файла, содержащего библиотеку типов, например, ADO. dll (Msado15. dll), и создает файлы заголовков, содержащие объявления typedef, смарт-указатели для интерфейсов и перечислимые константы.</span><span class="sxs-lookup"><span data-stu-id="49599-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="49599-115">Каждый интерфейс инкапсулируется или упаковывается в классе.</span><span class="sxs-lookup"><span data-stu-id="49599-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="49599-116">Для каждой операции в классе (то есть при вызове метода или свойства) существует объявление, которое вызывает операцию напрямую (то есть "необработанная" форма операции), и объявление для вызова необработанной операции и выдачи ошибки COM, если операция не может выполнить сукк ессфулли.</span><span class="sxs-lookup"><span data-stu-id="49599-116">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully.</span></span> <span data-ttu-id="49599-117">Если операция является свойством, то обычно существует директива компилятора, которая создает альтернативный синтаксис для операции, которая имеет синтаксис, такой как Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="49599-117">If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="49599-118">Операции, извлекающие значение свойства, имеют имена формы, \**Get \* \* \* Property*.</span><span class="sxs-lookup"><span data-stu-id="49599-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="49599-119">Операции, которые задают значение свойства, имеют имена формы, \**Put \* \* \* Property*.</span><span class="sxs-lookup"><span data-stu-id="49599-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="49599-120">Операции, которые задают значение свойства с указателем на объект ADO, имеют имена вида \*\*путреф \* \* \*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="49599-121">Вы можете получить или задать свойство с помощью вызовов следующих форм:</span><span class="sxs-lookup"><span data-stu-id="49599-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="49599-122">Использование директив свойств</span><span class="sxs-lookup"><span data-stu-id="49599-122">Using property directives</span></span>

<span data-ttu-id="49599-123">Директива компилятора \*\* \_деклспек (Property...) — это расширение языка C, зависящее от Майкрософт, которое объявляет функцию, используемую в качестве свойства, альтернативным синтаксисом. \_\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="49599-124">В результате можно задать или получить значения свойства, как в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="49599-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="49599-125">Например, вы можете задать и получить свойство следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="49599-126">Обратите внимание, что нет необходимости в коде:</span><span class="sxs-lookup"><span data-stu-id="49599-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="49599-127">Компилятор создаст соответствующий метод \*\*Get \* \* *-*, **Put**-или \*\*путреф \* \* \*\* в зависимости от объявления альтернативного синтаксиса и того, является ли свойство прочитанным или записанным.</span><span class="sxs-lookup"><span data-stu-id="49599-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="49599-128">\*\*\*\* \*\*\*\* \*\*\*\* \*\*\*\* \*\* \_Директива компилятора деклспек (Property...) может объявлять только альтернативный синтаксис для функции Get, PUT или Get. \_\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="49599-129">Только операции чтения имеют только объявление **Get** ; операции только для записи содержат объявление **Put** ; операции, выполняемые как для чтения, так и для записи, имеют объявления **Get** и **Put** .</span><span class="sxs-lookup"><span data-stu-id="49599-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="49599-130">Эта директива может иметь только два объявления; Однако у каждого свойства могут быть три функции свойств: \**Get \* \* \* Property*, \**Put \* \* \* Property*и \*\*путреф \* \* \*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="49599-131">В этом случае только две формы свойства имеют альтернативный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="49599-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="49599-132">Например, свойство **Command** Object **ActiveConnection** объявляется с помощью альтернативного синтаксиса для \**Get \* \* \* ActiveConnection* и \**путреф \* \* \* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="49599-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="49599-133">**Путреф**-синтаксис является хорошим выбором, так как на практике, как правило, необходимо поместить в это свойство открытый объект **Connection** (то есть, указатель на объект **подключения** ).</span><span class="sxs-lookup"><span data-stu-id="49599-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="49599-134">С другой стороны, объект **Recordset** имеет операции **Get**–, **Put**и \**путреф \* \* \* ActiveConnection* , но без альтернативного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="49599-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="49599-135">Коллекции, метод GetItem и свойство Item</span><span class="sxs-lookup"><span data-stu-id="49599-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="49599-136">ADO определяет несколько коллекций, в том числе **поля**, **Параметры**, **Свойства**и **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="49599-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="49599-137">В Visual C++ метод **GetItem (***index***)** Возвращает элемент коллекции.</span><span class="sxs-lookup"><span data-stu-id="49599-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="49599-138">*Index* является **вариантом**, значением которого является числовой индекс элемента в коллекции или строка, содержащая имя члена.</span><span class="sxs-lookup"><span data-stu-id="49599-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="49599-139">Директива компилятора \*\*\*\* \*\* \_деклспек (Property...) объявляет свойство Item в качестве альтернативного синтаксиса для каждого основного метода GetItem () каждой \_\*\* коллекции. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="49599-140">Альтернативный синтаксис использует квадратные скобки и выглядит примерно так: ссылка на массив.</span><span class="sxs-lookup"><span data-stu-id="49599-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="49599-141">В общем случае две формы выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="49599-142">Например, назначьте значение полю объекта **Recordset** с именем ***RS***, производным от таблицы **authors** базы данных **pubs** .</span><span class="sxs-lookup"><span data-stu-id="49599-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="49599-143">Используйте свойство **Item ()** , чтобы получить доступ к третьему **полю** коллекции **Fields** Object Collection (коллекции индексируются из нуля; Предположим, что третье поле называется ***Au\_fname***). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="49599-144">Затем вызовите метод **value ()** для объекта **field** , чтобы назначить строковое значение.</span><span class="sxs-lookup"><span data-stu-id="49599-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="49599-145">Это может быть представлено в Visual Basic следующими четырьмя способами (последние две формы уникальны для Visual Basic; у других языков нет эквивалентов):</span><span class="sxs-lookup"><span data-stu-id="49599-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="49599-146">Эквивалент в Visual C++ для первых двух предыдущих форм:</span><span class="sxs-lookup"><span data-stu-id="49599-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="49599-147">\-Кроме того, показан альтернативный синтаксис для свойства **value** .</span><span class="sxs-lookup"><span data-stu-id="49599-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="49599-148">Типы данных, зависящие от модели COM</span><span class="sxs-lookup"><span data-stu-id="49599-148">COM-specific data types</span></span>

<span data-ttu-id="49599-149">Как правило, любой тип данных Visual Basic, который вы найдете в справочнике по API ADO, имеет эквивалент в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="49599-149">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent.</span></span> <span data-ttu-id="49599-150">К ним относятся стандартные типы данных, такие как неподписанный **символ** для **байта**Visual Basic, **Short** для **целого числа**и **Long** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-150">These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**.</span></span> <span data-ttu-id="49599-151">Просмотрите индексы синтаксиса, чтобы точно увидеть, что требуется для операндов данного метода или свойства.</span><span class="sxs-lookup"><span data-stu-id="49599-151">Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="49599-152">Исключениями из этого правила являются типы данных, характерные для COM: **Variant**, **BSTR**и **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="49599-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="49599-153">Variant</span><span class="sxs-lookup"><span data-stu-id="49599-153">Variant</span></span>

<span data-ttu-id="49599-154">**Variant** — это структурированный тип данных, который содержит элемент value и элемент типа данных.</span><span class="sxs-lookup"><span data-stu-id="49599-154">A **Variant** is a structured data type that contains a value member and a data type member.</span></span> <span data-ttu-id="49599-155">**Variant** может содержать широкий диапазон других типов данных, в том числе другой Variant, BSTR, Boolean, IDispatch или указатель IUnknown, Currency, Date и т. д.</span><span class="sxs-lookup"><span data-stu-id="49599-155">A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</span></span> <span data-ttu-id="49599-156">COM также предоставляет методы, упрощающие преобразование одного типа данных в другой.</span><span class="sxs-lookup"><span data-stu-id="49599-156">COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="49599-157">Класс \*\* \_Variant\_t\*\* инкапсулирует и управляет типом данных **Variant** .</span><span class="sxs-lookup"><span data-stu-id="49599-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="49599-158">Если ссылка на API ADO указывает, что в качестве операнда метода или свойства используется значение, обычно это означает, что значение передается в \*\* \_варианте\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="49599-159">Это правило явно задано, когда раздел **Parameters** в разделах справочника по API ADO указывает на то, что операнд является **вариантом**.</span><span class="sxs-lookup"><span data-stu-id="49599-159">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**.</span></span> <span data-ttu-id="49599-160">Одним исключением является то, что в документации явно говорится, что операнд принимает стандартный тип данных, например **Long** или **Byte**, или перечисление.</span><span class="sxs-lookup"><span data-stu-id="49599-160">One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration.</span></span> <span data-ttu-id="49599-161">Другое исключение — когда операнд принимает **строку**.</span><span class="sxs-lookup"><span data-stu-id="49599-161">Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="49599-162">СТРОКЕ</span><span class="sxs-lookup"><span data-stu-id="49599-162">BSTR</span></span>

<span data-ttu-id="49599-163">Тип данных **BSTR** (**B**ASIC) — это структурированный тип данных, который содержит строку символов и длину строки. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-163">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length.</span></span> <span data-ttu-id="49599-164">COM предоставляет методы для распределения, управления и освобождения **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="49599-164">COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="49599-165">Класс \*\* \_BSTR\_t\*\* инкапсулирует и управляет типом данных **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="49599-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="49599-166">Если ссылка на API ADO указывает на то, что метод или \*\*\*\* свойство принимает строковое значение, это означает, что значение имеет вид \*\* \_BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="49599-167">\_Приведение\_классов Variant \_t\_и BSTR t</span><span class="sxs-lookup"><span data-stu-id="49599-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="49599-168">Часто нет необходимости явно кодировать \*\* \_Variant\_t\*\* или \*\* \_BSTR\_t\*\* в аргументе для операции.</span><span class="sxs-lookup"><span data-stu-id="49599-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="49599-169">Если класс \*\* \_Variant\_t\*\* или \*\* \_BSTR\_t\*\* имеет конструктор, который соответствует типу данных аргумента, компилятор создаст соответствующий \*\* \_\_Variant t\*\* или \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="49599-170">Тем не менее, если аргумент является неоднозначным, то есть тип данных аргумента соответствует более чем одному конструктору, необходимо привести аргумент с соответствующим типом данных для вызова надлежащего конструктора.</span><span class="sxs-lookup"><span data-stu-id="49599-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="49599-171">Например, объявление для объекта **Recordset:: Open** является следующим:</span><span class="sxs-lookup"><span data-stu-id="49599-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="49599-172">Аргумент ActiveConnection принимает ссылку на \*\* \_\_вариант t\*\*, который можно закодировать как строку подключения или указатель на открытый объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="49599-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="49599-173">Правильный \*\* \_вариант\_t\*\* будет создан неявно, если вы передаете строку, такую как "DSN = Pubs; UID = SA; pwd =;", или указатель, такой как "(IDispatch \*) пконн".</span><span class="sxs-lookup"><span data-stu-id="49599-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="49599-174">Или вы можете явно закодировать \*\* \_объект\_Variant t\*\* , содержащий указатель, такой\_как\_"Variant t ( \*(IDispatch) пконн, true)".</span><span class="sxs-lookup"><span data-stu-id="49599-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="49599-175">Приведение (IDispatch \*) разрешает неоднозначность с другим конструктором, принимающим указатель на интерфейс IUnknown.</span><span class="sxs-lookup"><span data-stu-id="49599-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="49599-176">Это очень важный, хотя и часто упоминаемый факт, что ADO является интерфейсом IDispatch.</span><span class="sxs-lookup"><span data-stu-id="49599-176">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface.</span></span> <span data-ttu-id="49599-177">Всякий раз, когда указатель на объект ADO должен быть передан как **Variant**, этот указатель должен быть приведен как указатель на интерфейс IDispatch.</span><span class="sxs-lookup"><span data-stu-id="49599-177">Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="49599-178">В последнем случае явно кодирует второй логический аргумент конструктора с необязательным значением по умолчанию true.</span><span class="sxs-lookup"><span data-stu-id="49599-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="49599-179">Этот аргумент заставляет конструктор **Variant** вызывать метод **AddRef**(), который компенсирует ADO автоматический вызов метода " \*\* \_\_t:: Release\*\*()" при завершении вызова метода или свойства ADO.</span><span class="sxs-lookup"><span data-stu-id="49599-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="49599-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="49599-180">SafeArray</span></span>

<span data-ttu-id="49599-181">**SAFEARRAY** это структурированный тип данных, который содержит массив других типов данных.</span><span class="sxs-lookup"><span data-stu-id="49599-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="49599-182">**SAFEARRAY** называется *Safe* , так как содержит сведения о границах каждого измерения массива и ограничивает доступ к элементам массива в этих границах.</span><span class="sxs-lookup"><span data-stu-id="49599-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="49599-183">Если ссылка на API ADO указывает на то, что метод или свойство принимают или возвращают массив, это означает, что метод или свойство принимает или возвращает **SAFEARRAY**, а не собственный массив C/C++.</span><span class="sxs-lookup"><span data-stu-id="49599-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="49599-184">Например, второму параметру метода **подключения** объекта **OpenSchema** требуется массив значений **Variant** .</span><span class="sxs-lookup"><span data-stu-id="49599-184">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values.</span></span> <span data-ttu-id="49599-185">Эти значения **типа Variant** должны передаваться в виде элементов **SAFEARRAY**, и этот **SAFEARRAY** должен быть установлен в качестве значения другого **варианта**.</span><span class="sxs-lookup"><span data-stu-id="49599-185">Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**.</span></span> <span data-ttu-id="49599-186">Это то, что другой **вариант** , передаваемый в качестве второго аргумента **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="49599-186">It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="49599-187">В качестве дальнейших примеров первым аргументом метода **Find** является **Variant** , значение которого является одномерным **массивом SAFEARRAY**; Каждый необязательный первый и второй аргументы **AddNew** является одномерным **массивом SAFEARRAY**; Возвращаемое значение метода **GetRows** — это объект **Variant** , значение которого является двумерным **массивом SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="49599-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="49599-188">Отсутствующие параметры и параметры по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49599-188">Missing and default parameters</span></span>

<span data-ttu-id="49599-189">Visual Basic разрешает отсутствующие параметры в методах.</span><span class="sxs-lookup"><span data-stu-id="49599-189">Visual Basic allows missing parameters in methods.</span></span> <span data-ttu-id="49599-190">Например, метод **Open** объекта **Recordset** имеет пять параметров, но вы можете пропустить промежуточные параметры и оставить параметры в конце.</span><span class="sxs-lookup"><span data-stu-id="49599-190">For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters.</span></span> <span data-ttu-id="49599-191">Значение **BSTR** или **Variant** по умолчанию будет заменено в зависимости от типа данных отсутствующего операнда.</span><span class="sxs-lookup"><span data-stu-id="49599-191">A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="49599-192">В C/C++ необходимо указать все операнды.</span><span class="sxs-lookup"><span data-stu-id="49599-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="49599-193">Если вы хотите указать отсутствующий параметр, тип данных которого является строкой, укажите строку \*\* \_BSTR\_t\*\* , содержащую пустую строку.</span><span class="sxs-lookup"><span data-stu-id="49599-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="49599-194">Если вы хотите указать отсутствующий параметр, тип данных которого — **Variant**, укажите \*\* \_вариант\_t\*\* со значением отображения\_E\_парамнотфаунд и типом ошибки VT\_.</span><span class="sxs-lookup"><span data-stu-id="49599-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="49599-195">Кроме того, можно указать эквивалентную \*\* \#\*\* \*\*\*\* \*\* \_константу Variant\_t\*\* , втмиссинг, которая предоставляется директивой импорта.</span><span class="sxs-lookup"><span data-stu-id="49599-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="49599-196">Три метода — это исключения типичного использования **втмиссинг**.</span><span class="sxs-lookup"><span data-stu-id="49599-196">Three methods are exceptions to the typical use of **vtMissing**.</span></span> <span data-ttu-id="49599-197">Это методы **EXECUTE** для объектов **Connection** и **Command** , а также метод **NextRecordset** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="49599-197">These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object.</span></span> <span data-ttu-id="49599-198">Ниже приведены их подписи:</span><span class="sxs-lookup"><span data-stu-id="49599-198">The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="49599-199">Параметры, *рекордсаффектед* и *Parameters*— указатели на **Variant**.</span><span class="sxs-lookup"><span data-stu-id="49599-199">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**.</span></span> <span data-ttu-id="49599-200">\*\* Параметр является входным параметром, который задает адрес **Variant** , содержащий один параметр, или массив параметров, которые будут изменять выполняемую команду.</span><span class="sxs-lookup"><span data-stu-id="49599-200">*Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed.</span></span> <span data-ttu-id="49599-201">*Рекордсаффектед* — выходной параметр, указывающий адрес **Variant**, в котором возвращается количество строк, затрагиваемых методом.</span><span class="sxs-lookup"><span data-stu-id="49599-201">*RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="49599-202">В методе **EXECUTE** Object Object указывает, что никакие параметры не указываются с помощью установки *параметров* для \&втмиссинг (рекомендуется) или для указателя NULL (то есть, **null** или нуль (0)). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="49599-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="49599-203">Если *параметру* присвоено значение null, метод выполняет внутреннее замещение эквивалента **втмиссинг**, а затем завершает операцию.</span><span class="sxs-lookup"><span data-stu-id="49599-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="49599-204">Во всех методах указывается, что количество затронутых записей не должно возвращаться путем установки для *рекордсаффектед* указателя NULL.</span><span class="sxs-lookup"><span data-stu-id="49599-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="49599-205">В этом случае указатель null не настолько похож на отсутствующий параметр, что означает, что метод должен отбросить количество затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="49599-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="49599-206">Таким образом, для этих трех методов допустимым кодом может быть нечто подобное:</span><span class="sxs-lookup"><span data-stu-id="49599-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="49599-207">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="49599-207">Error handling</span></span>

<span data-ttu-id="49599-208">В COM большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция.</span><span class="sxs-lookup"><span data-stu-id="49599-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="49599-209">Директива \*\* \#импорта\*\* создает код обертки вокруг каждого "необработанного" метода или свойства и проверяет возвращаемое значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="49599-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="49599-210">Если HRESULT указывает на ошибку, код оболочки создает ошибку COM, вызывая \_com-\_ошибку\_еррорекс () с возвращаемым кодом возврата HRESULT в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="49599-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="49599-211">Объекты ошибок COM можно перехватывать в блоке **try**-**catch** .</span><span class="sxs-lookup"><span data-stu-id="49599-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="49599-212">(Чтобы обеспечить эффективность, перехватите ссылку на объект \*\* \_Error\_com\*\* .)</span><span class="sxs-lookup"><span data-stu-id="49599-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="49599-213">Помните, что это ошибки ADO: они возникают при неисправности операции ADO.</span><span class="sxs-lookup"><span data-stu-id="49599-213">Remember, these are ADO errors: they result from the ADO operation failing.</span></span> <span data-ttu-id="49599-214">Ошибки, возвращенные базовым поставщиком, отображаются как объекты **ошибок** в коллекции **ошибок** объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="49599-214">Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="49599-215">Директива \*\* \#импорта\*\* создает только процедуры обработки ошибок для методов и свойств, объявленных в ADO. dll.</span><span class="sxs-lookup"><span data-stu-id="49599-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="49599-216">Тем не менее, вы можете использовать такой же механизм обработки ошибок, написав собственный макрос или встроенную функцию проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="49599-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="49599-217">Примеры приведены в разделе, [расширениях Visual C++](visual-c-extensions-for-ado.md)или коде в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="49599-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="49599-218">Эквиваленты соглашений Visual Basic в Visual C++</span><span class="sxs-lookup"><span data-stu-id="49599-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="49599-219">Ниже приведена сводка по нескольким соглашениям в документации по ADO, кодированным в Visual Basic, а также их эквивалентам в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="49599-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="49599-220">Объявление объекта ADO</span><span class="sxs-lookup"><span data-stu-id="49599-220">Declaring an ADO object</span></span>

<span data-ttu-id="49599-221">В Visual Basic объектная переменная ADO (в данном случае для объекта **Recordset** ) объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="49599-222">Предложение "ADODB. Recordset "— это ProgID объекта **Recordset** , как определено в реестре.</span><span class="sxs-lookup"><span data-stu-id="49599-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="49599-223">Новый экземпляр объекта **Record** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="49599-224">\-также</span><span class="sxs-lookup"><span data-stu-id="49599-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="49599-225">В Visual C++ директива \*\* \#импорта\*\* создает объявления типов смарт-указателей для всех объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="49599-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="49599-226">Например, переменная, указывающая на объект \*\* \_Recordset\*\* , имеет тип \*\* \_рекордсетптр\*\*и объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="49599-227">Переменная, указывающая на новый экземпляр объекта \*\* \_Recordset\*\* , объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="49599-228">\-также</span><span class="sxs-lookup"><span data-stu-id="49599-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="49599-229">\-также</span><span class="sxs-lookup"><span data-stu-id="49599-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="49599-230">После вызова метода **CreateInstance** переменная может использоваться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="49599-231">Обратите внимание, что в одном случае оператор "." используется, как если бы переменная была экземпляром класса (RS. CreateInstance), а в другом случае оператор "-\>" используется так, как если бы переменная была указателем на интерфейс (RS-\>Open).</span><span class="sxs-lookup"><span data-stu-id="49599-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="49599-232">Одну переменную можно использовать двумя способами, так как оператор "\>-" перегружен, чтобы позволить экземпляру класса вести себя как указатель на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="49599-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="49599-233">Частный член класса переменной экземпляра содержит указатель на интерфейс \*\* \_Recordset\*\* ; оператор "–\>" возвращает этот указатель; Возвращаемый указатель получает доступ к членам объекта \*\* \_Recordset\*\* .</span><span class="sxs-lookup"><span data-stu-id="49599-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="49599-234">Написание кода отсутствующего параметра</span><span class="sxs-lookup"><span data-stu-id="49599-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="49599-235">Строка</span><span class="sxs-lookup"><span data-stu-id="49599-235">String</span></span>

<span data-ttu-id="49599-236">Если вам нужно закодировать пропущенный **строковый** операнд в Visual Basic, вы просто опустите операнд.</span><span class="sxs-lookup"><span data-stu-id="49599-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="49599-237">Необходимо указать операнд в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="49599-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="49599-238">Код — \*\* \_BSTR\_t\*\* , имеющий пустую строку в качестве значения.</span><span class="sxs-lookup"><span data-stu-id="49599-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="49599-239">Variant</span><span class="sxs-lookup"><span data-stu-id="49599-239">Variant</span></span>

<span data-ttu-id="49599-240">При необходимости кодирования пропущенного операнда **Variant** в Visual Basic вы просто опустите операнд.</span><span class="sxs-lookup"><span data-stu-id="49599-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="49599-241">Необходимо указать все операнды в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="49599-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="49599-242">Код — отсутствует параметр **Variant** со значением \*\* \_Variant\_t\*\* , равным специальному значению\_,\_отображаемой E парамнотфаунд и Type\_, Error VT.</span><span class="sxs-lookup"><span data-stu-id="49599-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="49599-243">Кроме того, можно указать **втмиссинг**, представляющий собой эквивалентную предварительно определенную константу, предоставляемую директивой \*\* \#импорта\*\* .</span><span class="sxs-lookup"><span data-stu-id="49599-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="49599-244">\-или используйте —</span><span class="sxs-lookup"><span data-stu-id="49599-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="49599-245">Объявление варианта</span><span class="sxs-lookup"><span data-stu-id="49599-245">Declaring a variant</span></span>

<span data-ttu-id="49599-246">В Visual Basic **переменная Variant** объявляется с помощью оператора **Dim** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="49599-247">В Visual C++ объявите переменную как тип \*\* \_Variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="49599-248">Ниже приведено несколько схематических \*\* \_объявлений вариантов\_t\*\* .</span><span class="sxs-lookup"><span data-stu-id="49599-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="49599-249">Эти объявления просто придают грубое представление о том, что можно сделать с кодом в собственной программе.</span><span class="sxs-lookup"><span data-stu-id="49599-249">These declarations merely give a rough idea of what you would code in your own program.</span></span> <span data-ttu-id="49599-250">Дополнительные сведения можно найти в приведенных ниже примерах и документации по Visual C++.</span><span class="sxs-lookup"><span data-stu-id="49599-250">For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="49599-251">Использование массивов вариантов</span><span class="sxs-lookup"><span data-stu-id="49599-251">Using arrays of variants</span></span>

<span data-ttu-id="49599-252">В Visual Basic массивы **Variant** можно закодировать с помощью оператора **Dim** или можно использовать функцию **Array** , как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="49599-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

<span data-ttu-id="49599-253">В следующем примере на Visual C++ показано использование **SAFEARRAY** , используемого с \*\* \_вариантом\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="49599-254">Следующие примечания соответствуют разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="49599-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="49599-255">В этом случае встроенная функция ТЕССР () используется для использования существующего механизма обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="49599-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="49599-256">Необходим только одномерный массив, поэтому вы можете использовать **сафеаррайкреатевектор**вместо объявления общего назначения **Сафеаррайбаунд** и функции **сафеаррайкреате** .</span><span class="sxs-lookup"><span data-stu-id="49599-256">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function.</span></span> <span data-ttu-id="49599-257">Ниже показано, как будет выглядеть код с помощью **сафеаррайкреате**:</span><span class="sxs-lookup"><span data-stu-id="49599-257">The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="49599-258">Схема, определенная с помощью перечислимой константы, **адсчемаколумнс**, связана с четырьмя столбцами ограничений\_: Каталог таблицы\_, таблица,\_имя таблицы и имя\_столбца.</span><span class="sxs-lookup"><span data-stu-id="49599-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="49599-259">Поэтому создается массив значений **Variant** с четырьмя элементами.</span><span class="sxs-lookup"><span data-stu-id="49599-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="49599-260">Затем указывается значение ограничения, соответствующее третьему столбцу, имя\_таблицы.</span><span class="sxs-lookup"><span data-stu-id="49599-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="49599-261">Возвращаемый объект **Recordset** состоит из нескольких столбцов, подмножества которых являются столбцами ограничений.</span><span class="sxs-lookup"><span data-stu-id="49599-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="49599-262">Значения столбцов ограничений для каждой возвращаемой строки должны совпадать со значениями соответствующих ограничений.</span><span class="sxs-lookup"><span data-stu-id="49599-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="49599-263">Хорошо знакомые с **SAFEARRAY** , могут быть удивлены тем, что **сафеаррайдестрой**() не вызывается перед выходом.</span><span class="sxs-lookup"><span data-stu-id="49599-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="49599-264">На самом деле вызов **сафеаррайдестрой**() в этом случае приведет к возникновению исключения времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="49599-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="49599-265">Причина в том, что деструктор для вткритериа будет вызывать **вариантклеар**(), когда \*\* \_Variant\_t\*\* выходит из области действия, что позволит освободить **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="49599-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="49599-266">Вызов **сафеаррайдестрой**без ручного очистки \*\* \_Variant\_t\*\*приведет к тому, что деструктор попытается очистить недопустимый указатель **SAFEARRAY** .</span><span class="sxs-lookup"><span data-stu-id="49599-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="49599-267">При вызове **сафеаррайдестрой** код будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49599-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="49599-268">Тем не менее, значительно проще позволить \*\* \_\_варианту\*\* управлять **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="49599-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a><span data-ttu-id="49599-269">Использование свойства get/put/Путреф</span><span class="sxs-lookup"><span data-stu-id="49599-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="49599-270">В Visual Basic имя свойства не определено при получении, назначении или назначении ссылки.</span><span class="sxs-lookup"><span data-stu-id="49599-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

<span data-ttu-id="49599-271">В этом примере в Visual C++ показано свойство **Get**/**Put**/\*\*путреф \* \* \*\*.</span><span class="sxs-lookup"><span data-stu-id="49599-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="49599-272">Следующие примечания соответствуют разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="49599-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="49599-273">В этом примере используются две формы отсутствующего строкового аргумента: явная константа, **стрмиссинг**и строка, которую компилятор будет использовать для создания временной \*\* \_строки BSTR\_t\*\* , которая будет существовать для области метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="49599-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="49599-274">Не требуется приведение операнда RS-\>путрефактивеконнектион (CN) к (IDispatch \*), так как тип операнда уже (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="49599-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="49599-275">Использование метода GetItem (x) и элемента\[x\]</span><span class="sxs-lookup"><span data-stu-id="49599-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="49599-276">В этом примере Visual Basic показан стандартный и альтернативный синтаксис для **Item**().</span><span class="sxs-lookup"><span data-stu-id="49599-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

<span data-ttu-id="49599-277">В этом примере в Visual C++ показано, как **элемент**.</span><span class="sxs-lookup"><span data-stu-id="49599-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="49599-278">Следующее примечание соответствует разделу с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="49599-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="49599-279">Когда доступ к коллекции осуществляется с помощью **элемента**, индекс, **2**, должен быть приведен к типу **Long** , поэтому будет вызван соответствующий конструктор.</span><span class="sxs-lookup"><span data-stu-id="49599-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="49599-280">ПриВедение указателей объектов ADO с \*(IDispatch)</span><span class="sxs-lookup"><span data-stu-id="49599-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="49599-281">В следующем примере на Visual C++ показано использование ( \*IDispatch) для приведения указателей объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="49599-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="49599-282">Следующие примечания соответствуют разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="49599-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="49599-283">Укажите открытый объект **Connection** в явно заданном коде **Variant**.</span><span class="sxs-lookup"><span data-stu-id="49599-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="49599-284">ПриВедите его к ( \*IDispatch), чтобы вызвать правильный конструктор.</span><span class="sxs-lookup"><span data-stu-id="49599-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="49599-285">Кроме того, необходимо явным образом задать для второго \*\* \_параметра Variant\_t\*\* значение по умолчанию **true**, поэтому счетчик ссылок на объекты будет правильным, когда заканчивается операция **Recordset:: Open** .</span><span class="sxs-lookup"><span data-stu-id="49599-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="49599-286">Выражение (\_\_BSTR t) не является приведением, а оператор \*\* \_Variant\_t\*\* , который извлекает строку \*\* \_BSTR\_t\*\* из **Variant** , возвращенного по **значению**.</span><span class="sxs-lookup"><span data-stu-id="49599-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="49599-287">Выражение (char\*) не является приведением, но оператор \*\* \_BSTR\_t\*\* , который извлекает указатель на инкапсулированную строку в объекте \*\* \_BSTR\_t\*\* .</span><span class="sxs-lookup"><span data-stu-id="49599-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="49599-288">В этом разделе кода показаны некоторые из наиболее эффективных вариантов поведения \*\* \_операторов\_Variant t\*\* и \*\* \_BSTR\_t\*\* .</span><span class="sxs-lookup"><span data-stu-id="49599-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

