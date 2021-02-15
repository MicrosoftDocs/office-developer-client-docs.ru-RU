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
# <a name="visual-c-ado-programming"></a><span data-ttu-id="ad87f-102">Программирование для ADO на Visual C++</span><span class="sxs-lookup"><span data-stu-id="ad87f-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="ad87f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad87f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad87f-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ad87f-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="ad87f-105">Хотя предполагаемая аудитория — все пользователи, программисты ADO используют различные языки, такие **\#** как Visual Basic, Visual C++ (с директивой импорта и без нее) и Visual J++ (с пакетом класса ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="ad87f-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="ad87f-106">Чтобы учесть такое разнообразие, синтаксис ADO для [Visual C++](using-ado-with-microsoft-visual-c.md) предоставляет синтаксис для языка Visual C++ со ссылками на общие описания функций, параметров, исключительных поведений и т. д. в справочнике по API.</span><span class="sxs-lookup"><span data-stu-id="ad87f-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="ad87f-107">ADO реализуется с помощью интерфейсов COM (объектной модели компонентов).</span><span class="sxs-lookup"><span data-stu-id="ad87f-107">ADO is implemented with COM (Component Object Model) interfaces.</span></span> <span data-ttu-id="ad87f-108">Однако программистам проще работать с COM на определенных языках программирования, чем с другими.</span><span class="sxs-lookup"><span data-stu-id="ad87f-108">However, it is easier for programmers to work with COM in certain programming languages than others.</span></span> <span data-ttu-id="ad87f-109">Например, почти все сведения об использовании COM обрабатываются неявно для Visual Basic программистов, тогда как программисты Visual C++ должны сами обращаться к этим сведениям.</span><span class="sxs-lookup"><span data-stu-id="ad87f-109">For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="ad87f-110">В следующих разделах приводится краткое руководство для программистов C и C++, использующих ADO и **\# директиву импорта.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="ad87f-111">В ней основное внимание уделяется типам данных, характерным для COM (**Variant,** **BSTR** и **SafeArray),** а также обработке ошибок \_ (ошибка \_ com).</span><span class="sxs-lookup"><span data-stu-id="ad87f-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="ad87f-112">Использование \# директивы компилятор импорта</span><span class="sxs-lookup"><span data-stu-id="ad87f-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="ad87f-113">Директива **\# компиляторов** Импорта Visual C++ упрощает работу с методами и свойствами ADO.</span><span class="sxs-lookup"><span data-stu-id="ad87f-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="ad87f-114">Директива принимает имя файла, содержащего библиотеку типов, например ADO DLL (Msado15.dll), и создает файлы заголовок, содержащие объявления typedef, интеллектуальные указатели для интерфейсов и нумерированные константы.</span><span class="sxs-lookup"><span data-stu-id="ad87f-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="ad87f-115">Каждый интерфейс инкапсулируется или оболочка в класс.</span><span class="sxs-lookup"><span data-stu-id="ad87f-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="ad87f-116">Для каждой операции в классе (то есть вызова метода или свойства) имеется объявление для прямого вызова операции (то есть "необработанные" формы операции) и объявление для вызова необработанных операций и вызова ошибки COM, если операция не удается выполнить успешно.</span><span class="sxs-lookup"><span data-stu-id="ad87f-116">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully.</span></span> <span data-ttu-id="ad87f-117">Если операция является свойством, обычно существует директива компиляторов, которая создает альтернативный синтаксис для операции с синтаксис, например Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ad87f-117">If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="ad87f-118">Операции, которые получают значение свойства, имеют имена формы, \**Get\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="ad87f-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="ad87f-119">Операции, которые устанавливают значение свойства, имеют имена формы, \**Put\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="ad87f-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="ad87f-120">Операции, которые устанавливают значение свойства с указателем на объект ADO, имеют имена формы, \**PutRef\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="ad87f-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="ad87f-121">Вы можете получить или настроить свойство с помощью вызовов этих форм:</span><span class="sxs-lookup"><span data-stu-id="ad87f-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="ad87f-122">Использование директив свойств</span><span class="sxs-lookup"><span data-stu-id="ad87f-122">Using property directives</span></span>

<span data-ttu-id="ad87f-123">Директива **\_ \_ компиляторов declspec(property...)** — это расширение языка C корпорации Майкрософт, которое объявляет функцию, используемую в качестве свойства для использования альтернативного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ad87f-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="ad87f-124">В результате вы можете установить или получить значения свойства так же, как Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ad87f-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="ad87f-125">Например, можно настроить и получить свойство таким образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="ad87f-126">Обратите внимание, что вам не нужно кодировать:</span><span class="sxs-lookup"><span data-stu-id="ad87f-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="ad87f-127">Компилятор создает соответствующий вызов \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* в зависимости от объявленного альтернативного синтаксиса и того, считывало ли свойство или оно было записано.</span><span class="sxs-lookup"><span data-stu-id="ad87f-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="ad87f-128">Директива **\_ \_ компиляторов declspec(property...)** может объявлять только **get,** **put,** or **get** and **put** alternative syntax for a function.</span><span class="sxs-lookup"><span data-stu-id="ad87f-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="ad87f-129">Операции только для чтения имеют только объявление **получения;** Операции только для записи имеют только объявление **put;** операции как для чтения, так и для записи имеют объявления **get** и **put.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="ad87f-130">С этой директивой можно сделать только два объявления; Однако каждое свойство может иметь три функции свойств: \**Get\*\*\*Property*, \**Put\*\*\*Property* и \**PutRef\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="ad87f-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="ad87f-131">В этом случае альтернативный синтаксис имеется только в двух формах свойства.</span><span class="sxs-lookup"><span data-stu-id="ad87f-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="ad87f-132">Например, свойство **ActiveConnection** объекта **Command** объявляется с альтернативным синтаксисом для \**Get\*\*\*ActiveConnection* и \**PutRef\*\*\*ActiveConnection.*</span><span class="sxs-lookup"><span data-stu-id="ad87f-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="ad87f-133">Синтаксис **PutRef**— хороший выбор, так как на практике в это свойство обычно нужно поместить открытый объект **Connection** (то есть указатель объекта **Connection).**</span><span class="sxs-lookup"><span data-stu-id="ad87f-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="ad87f-134">С другой стороны, объект **Recordset** имеет операции **Get-,** **Put**-и \**PutRef\*\*\*ActiveConnection,* но без альтернативного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ad87f-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="ad87f-135">Коллекции, метод GetItem и свойство Item</span><span class="sxs-lookup"><span data-stu-id="ad87f-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="ad87f-136">ADO определяет несколько коллекций, в том числе **Fields,** **Parameters,** **Properties** и **Errors.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="ad87f-137">В Visual C++ метод **GetItem(index)** возвращает член коллекции.</span><span class="sxs-lookup"><span data-stu-id="ad87f-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="ad87f-138">*Индекс* — **это variant,** значение которого — это либо числовой индекс члена коллекции, либо строка, содержащая имя члена.</span><span class="sxs-lookup"><span data-stu-id="ad87f-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="ad87f-139">Директива компиляторов **\_ \_ declspec(property...)** объявляет свойство **Item** в качестве альтернативного синтаксиса для основного метода **GetItem()** каждой коллекции.</span><span class="sxs-lookup"><span data-stu-id="ad87f-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="ad87f-140">Альтернативный синтаксис использует квадратные скобки и выглядит аналогично ссылке на массив.</span><span class="sxs-lookup"><span data-stu-id="ad87f-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="ad87f-141">Как правило, две формы выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="ad87f-142">Например, назначьте значение полю объекта **Recordset** с именем ***rs,*** производного от таблицы авторов базы **данных pubs.** </span><span class="sxs-lookup"><span data-stu-id="ad87f-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="ad87f-143">Используйте свойство **Item()** для  доступа к третьему  полю коллекции Полей объекта **Recordset** (коллекции индексются с нуля; предполагается, что третье поле называется ***au \_ fname).***</span><span class="sxs-lookup"><span data-stu-id="ad87f-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="ad87f-144">Затем вызовите **метод Value()** объекта **Field,** чтобы назначить строку.</span><span class="sxs-lookup"><span data-stu-id="ad87f-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="ad87f-145">Это может быть выражено Visual Basic следующими четырьмя способами (последние две формы уникальны для Visual Basic; другие языки не имеют эквивалентов):</span><span class="sxs-lookup"><span data-stu-id="ad87f-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="ad87f-146">Эквивалент в Visual C++ для первых двух вышеперечисленной формы:</span><span class="sxs-lookup"><span data-stu-id="ad87f-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="ad87f-147">\-or- (также показан альтернативный синтаксис для свойства **Value)**</span><span class="sxs-lookup"><span data-stu-id="ad87f-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="ad87f-148">Типы данных, специфики для COM</span><span class="sxs-lookup"><span data-stu-id="ad87f-148">COM-specific data types</span></span>

<span data-ttu-id="ad87f-149">Как правило, любой Visual Basic данных, который вы найдете в справочнике по ADO API, имеет эквивалент Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ad87f-149">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent.</span></span> <span data-ttu-id="ad87f-150">К ним относятся стандартные типы данных, такие как неподписаный символ для Visual Basic **Byte,** **short** for **Integer** и **long** for **Long.** </span><span class="sxs-lookup"><span data-stu-id="ad87f-150">These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**.</span></span> <span data-ttu-id="ad87f-151">Посмотрите в индексах синтаксиса, чтобы узнать, что именно требуется для операнд данного метода или свойства.</span><span class="sxs-lookup"><span data-stu-id="ad87f-151">Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="ad87f-152">Исключениями из этого правила являются типы данных, специфические для COM: **Variant,** **BSTR** и **SafeArray.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="ad87f-153">Variant</span><span class="sxs-lookup"><span data-stu-id="ad87f-153">Variant</span></span>

<span data-ttu-id="ad87f-154">Variant **—** это структурированный тип данных, содержащий член значения и тип данных.</span><span class="sxs-lookup"><span data-stu-id="ad87f-154">A **Variant** is a structured data type that contains a value member and a data type member.</span></span> <span data-ttu-id="ad87f-155">Variant  может содержать широкий диапазон других типов данных, включая другой указатель Variant, BSTR, Boolean, IDispatch или IUnknown, валюту, дату и т. д.</span><span class="sxs-lookup"><span data-stu-id="ad87f-155">A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</span></span> <span data-ttu-id="ad87f-156">COM также предоставляет методы, которые делают преобразование одного типа данных в другой.</span><span class="sxs-lookup"><span data-stu-id="ad87f-156">COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="ad87f-157">Класс **\_ variant \_ t** инкапсулирует тип данных **Variant** и управляет им.</span><span class="sxs-lookup"><span data-stu-id="ad87f-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="ad87f-158">Когда ссылка ADO API сообщает, что метод или операнд свойства принимает значение, обычно это означает, что значение передается в **\_ \_ варианте t**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="ad87f-159">Это правило явным образом  действует, если в разделе "Параметры" в разделах справочника по ADO API говорится, что операнд является **вариантом.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-159">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**.</span></span> <span data-ttu-id="ad87f-160">Одним из исключений является, когда в документации явно говорится, что операнд принимает стандартный тип данных, например **Long** или **Byte,** или enumeration.</span><span class="sxs-lookup"><span data-stu-id="ad87f-160">One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration.</span></span> <span data-ttu-id="ad87f-161">Еще одно исключение — когда операнд принимает **строку.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-161">Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="ad87f-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="ad87f-162">BSTR</span></span>

<span data-ttu-id="ad87f-163">**BSTR** (**B** asic **STR** ing) — это структурированный тип данных, содержащий строку символов и длину строки.</span><span class="sxs-lookup"><span data-stu-id="ad87f-163">A **BSTR** (**B** asic **STR** ing) is a structured data type that contains a character string and the string's length.</span></span> <span data-ttu-id="ad87f-164">COM предоставляет методы для выделения, управления и бесплатного **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-164">COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="ad87f-165">Класс **\_ bstr \_ t** инкапсулирует тип данных **BSTR** и управляет им.</span><span class="sxs-lookup"><span data-stu-id="ad87f-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="ad87f-166">Если ссылка ADO API сообщает, что  метод или свойство принимает строку, это означает, что значение имеет форму **\_ bstr \_ t**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a><span data-ttu-id="ad87f-167">Классы \_ variant \_ t и \_ bstr \_ t casting</span><span class="sxs-lookup"><span data-stu-id="ad87f-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="ad87f-168">Часто нет необходимости явно кодировать вариант **\_ \_ t** или **\_ bstr \_ t** в аргументе для операции.</span><span class="sxs-lookup"><span data-stu-id="ad87f-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="ad87f-169">Если класс **\_ variant \_ t** или **\_ bstr \_ t** имеет конструктор, соответствующий типу данных аргумента, компилятор создает соответствующий вариант **\_ \_ t** или **\_ bstr \_ t**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="ad87f-170">Однако если аргумент неоднозначн, то есть тип данных аргумента соответствует более чем одному конструктору, необходимо привести аргумент с соответствующим типом данных, чтобы вызвать правильный конструктор.</span><span class="sxs-lookup"><span data-stu-id="ad87f-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="ad87f-171">Например, для метода **Recordset::Open** используется объявление:</span><span class="sxs-lookup"><span data-stu-id="ad87f-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="ad87f-172">Аргумент ActiveConnection принимает ссылку на вариант **\_ \_ t,** который можно закодировать как строку подключения или указатель на открытый **объект Connection.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="ad87f-173">Правильный вариант **\_ \_ t** будет построен неявно, если передать строку, например "DSN=pubs;uid=sa;pwd=;", или указатель, например "(IDispatch \* ) pConn".</span><span class="sxs-lookup"><span data-stu-id="ad87f-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="ad87f-174">Или вы можете явно закодировать вариант, **\_ \_ не** содержащий указатель, например \_ "variant \_ t((IDispatch \* ) pConn, true)".</span><span class="sxs-lookup"><span data-stu-id="ad87f-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="ad87f-175">При этом (IDispatch) неоднозначность устраняется с помощью другого конструктора, который принимает указатель на интерфейс \* IUnknown.</span><span class="sxs-lookup"><span data-stu-id="ad87f-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="ad87f-176">Хотя этот факт редко упоминается, важно, чтобы ADO был интерфейсом IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ad87f-176">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface.</span></span> <span data-ttu-id="ad87f-177">Каждый раз, когда указатель на объект ADO должен передаваться в качестве **варианта,** этот указатель должен быть приведя в качестве указателя к интерфейсу IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ad87f-177">Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="ad87f-178">Последний случай явно кодирует второй boolean аргумент конструктора с необязательным значением по умолчанию, значением true.</span><span class="sxs-lookup"><span data-stu-id="ad87f-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="ad87f-179">Этот аргумент вызывает метод **AddRef**() **конструктора Variant,** который автоматически вызывает метод variant **\_ \_ t::Release**() при вызове метода ADO или свойства.</span><span class="sxs-lookup"><span data-stu-id="ad87f-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="ad87f-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="ad87f-180">SafeArray</span></span>

<span data-ttu-id="ad87f-181">**SafeArray** — это структурированный тип данных, содержащий массив других типов данных.</span><span class="sxs-lookup"><span data-stu-id="ad87f-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="ad87f-182">**SafeArray** называется  безопасным, так как он содержит сведения об границах каждого измерения массива и ограничивает доступ к элементам массива в этих границах.</span><span class="sxs-lookup"><span data-stu-id="ad87f-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="ad87f-183">Если ссылка ADO API сообщает, что метод или свойство принимает или возвращает массив, это означает, что метод или свойство принимает или возвращает **SafeArray,** а не массив C/C++.</span><span class="sxs-lookup"><span data-stu-id="ad87f-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="ad87f-184">Например, второй параметр метода **OpenSchema** объекта **Connection** требует массив значений **Variant.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-184">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values.</span></span> <span data-ttu-id="ad87f-185">Эти **значения Variant** должны быть переданы в качестве элементов **SafeArray,** и что **SafeArray** должен быть установлен в качестве значения другого **варианта**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-185">Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**.</span></span> <span data-ttu-id="ad87f-186">Это другой **вариант,** который передается в качестве второго аргумента **OpenSchema.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-186">It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="ad87f-187">В качестве дополнительных примеров первым аргументом метода **Find** является **Variant,** значением которого является одномерное **значение SafeArray;** каждый необязательный первый и второй аргумент **AddNew** является одномерным **SafeArray;** и возвращаемая величина метода **GetRows** — **это Variant,** значение которого является двумерным **safeArray.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="ad87f-188">Отсутствующие параметры и параметры по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad87f-188">Missing and default parameters</span></span>

<span data-ttu-id="ad87f-189">Visual Basic параметры в методах.</span><span class="sxs-lookup"><span data-stu-id="ad87f-189">Visual Basic allows missing parameters in methods.</span></span> <span data-ttu-id="ad87f-190">Например, метод **Recordset** object **Open** имеет пять параметров, но вы можете пропустить промежуточные параметры и не использовать последние параметры.</span><span class="sxs-lookup"><span data-stu-id="ad87f-190">For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters.</span></span> <span data-ttu-id="ad87f-191">BSTR или **Variant** **по** умолчанию будут заменены в зависимости от типа данных отсутствующих операндов.</span><span class="sxs-lookup"><span data-stu-id="ad87f-191">A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="ad87f-192">В C/C++ должны быть указаны все операнды.</span><span class="sxs-lookup"><span data-stu-id="ad87f-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="ad87f-193">Если необходимо указать отсутствующий параметр, тип данных которого является строкой, укажите **\_ строку bstr \_ t,** содержащую нулевую строку.</span><span class="sxs-lookup"><span data-stu-id="ad87f-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="ad87f-194">Если необходимо указать отсутствующий параметр, тип данных которого — **Variant,** укажите вариант **\_ \_ t** со значением DISP E PARAMNOTFOUND и типом \_ \_ ошибки \_ VT.</span><span class="sxs-lookup"><span data-stu-id="ad87f-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="ad87f-195">Кроме того, укажите эквивалентную константу **\_ variant \_ t,** **vtMissing,** которая предоставляется директивой **\# импорта.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="ad87f-196">Три метода являются исключениями из обычного использования **vtMissing.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-196">Three methods are exceptions to the typical use of **vtMissing**.</span></span> <span data-ttu-id="ad87f-197">Это методы **Execute** объектов **Connection** и **Command** и **метод NextRecordset** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-197">These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object.</span></span> <span data-ttu-id="ad87f-198">Их подписи:</span><span class="sxs-lookup"><span data-stu-id="ad87f-198">The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="ad87f-199">Параметры *RecordsAffected* и *Parameters*— это указатели на **variant.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-199">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**.</span></span> <span data-ttu-id="ad87f-200">*Параметры* — это входной параметр, который указывает адрес **Variant,** содержащий один параметр или массив параметров, который будет изменять команду, которая выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad87f-200">*Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed.</span></span> <span data-ttu-id="ad87f-201">*RecordsAffected* — это выходной параметр, который указывает адрес **variant,** где возвращается количество строк, затронутых методом.</span><span class="sxs-lookup"><span data-stu-id="ad87f-201">*RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="ad87f-202">В **методе Execute** объекта **Command** указать, что  параметры не заданы, задав для параметров значение \& vtMissing (рекомендуется) или нулевой указатель (то есть **NULL** или ноль (0)).</span><span class="sxs-lookup"><span data-stu-id="ad87f-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="ad87f-203">Если *параметры заданы* как указатель null, метод внутренне заменяет эквивалент **vtMissing,** а затем завершает операцию.</span><span class="sxs-lookup"><span data-stu-id="ad87f-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="ad87f-204">Во всех методах следует указать, что количество затронутых записей не должно возвращаться путем установки параметра *RecordsAffected* для указателя null.</span><span class="sxs-lookup"><span data-stu-id="ad87f-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="ad87f-205">В этом случае null-указатель — это не столько отсутствующий параметр, сколько указание на то, что метод должен отменить количество затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="ad87f-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="ad87f-206">Таким образом, для этих трех методов допустимо закодировать что-то, например:</span><span class="sxs-lookup"><span data-stu-id="ad87f-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="ad87f-207">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="ad87f-207">Error handling</span></span>

<span data-ttu-id="ad87f-208">В COM большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция.</span><span class="sxs-lookup"><span data-stu-id="ad87f-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="ad87f-209">Директива **\# импорта** создает код-оболочку для каждого "необработанных" метода или свойства и проверяет возвращенный HRESULT.</span><span class="sxs-lookup"><span data-stu-id="ad87f-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="ad87f-210">Если HRESULT указывает на сбой, код-оболочка вызывает ошибку COM, вызывая \_ com \_ issue errorex() с кодом возврата HRESULT в качестве \_ аргумента.</span><span class="sxs-lookup"><span data-stu-id="ad87f-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="ad87f-211">Объекты ошибки COM могут быть перехвачены в **блоке try** - **catch.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="ad87f-212">(Для повышения эффективности перехватить ссылку на объект **\_ ошибки \_ com.)**</span><span class="sxs-lookup"><span data-stu-id="ad87f-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="ad87f-213">Помните, что это ошибки ADO: они являются результатом сбоя операции ADO.</span><span class="sxs-lookup"><span data-stu-id="ad87f-213">Remember, these are ADO errors: they result from the ADO operation failing.</span></span> <span data-ttu-id="ad87f-214">Ошибки, возвращенные поставщиком, отображаются как **объекты Error** в коллекции **Errors** объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-214">Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="ad87f-215">Директива **\# импорта** создает только процедуры обработки ошибок для методов и свойств, объявленных в DLL ADO.</span><span class="sxs-lookup"><span data-stu-id="ad87f-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="ad87f-216">Тем не менее, вы можете воспользоваться этим же механизмом обработки ошибок, написав собственный макрос проверки ошибок или функцию.</span><span class="sxs-lookup"><span data-stu-id="ad87f-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="ad87f-217">Примеры см. в разделе [,Visual C++ Extensions](visual-c-extensions-for-ado.md)или коде в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="ad87f-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="ad87f-218">Visual C++ equivalents of Visual Basic conventions</span><span class="sxs-lookup"><span data-stu-id="ad87f-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="ad87f-219">Ниже приводится сводка по нескольким соглашениям в документации ADO, закодирование в Visual Basic, а также их эквиваленты в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ad87f-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="ad87f-220">Объявление объекта ADO</span><span class="sxs-lookup"><span data-stu-id="ad87f-220">Declaring an ADO object</span></span>

<span data-ttu-id="ad87f-221">В Visual Basic объектной переменной ADO (в данном случае для объекта **Recordset)** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="ad87f-222">Предложение "ADODB. Recordset" — это progID объекта **Recordset,** как определено в реестре.</span><span class="sxs-lookup"><span data-stu-id="ad87f-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="ad87f-223">Новый экземпляр объекта **Record** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="ad87f-224">\-or-</span><span class="sxs-lookup"><span data-stu-id="ad87f-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="ad87f-225">В Visual C++ директива **\# импорта** создает объявления типа интеллектуального указателя для всех объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="ad87f-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="ad87f-226">Например, переменная, которая указывает на объект **\_ Recordset,** имеет тип **\_ RecordsetPtr** и объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="ad87f-227">Переменная, которая указывает на новый экземпляр объекта **\_ Recordset,** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="ad87f-228">\-or-</span><span class="sxs-lookup"><span data-stu-id="ad87f-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="ad87f-229">\-or-</span><span class="sxs-lookup"><span data-stu-id="ad87f-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="ad87f-230">После того как будет вызван **метод CreateInstance,** переменную можно использовать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="ad87f-231">Обратите внимание, что в одном случае оператор "." используется так, как если бы переменная была экземпляром класса (rs). CreateInstance), а в другом случае оператор "- " используется, как если бы переменная была указателем на \> интерфейс (rs-Open). \></span><span class="sxs-lookup"><span data-stu-id="ad87f-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="ad87f-232">Одну переменную можно использовать двумя способами, так как оператор "-" перегружен, чтобы позволить экземпляру класса вести себя как указатель \> на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ad87f-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="ad87f-233">Частный член класса переменной экземпляра содержит указатель на интерфейс **\_ recordset;** оператор "-" возвращает этот указатель, а возвращенный указатель возвращает доступ к членам объекта \> **\_ Recordset.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="ad87f-234">Написание кода отсутствующих параметров</span><span class="sxs-lookup"><span data-stu-id="ad87f-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="ad87f-235">String</span><span class="sxs-lookup"><span data-stu-id="ad87f-235">String</span></span>

<span data-ttu-id="ad87f-236">Если вам нужно закодировать отсутствующий операнд строки в Visual Basic, просто опустить операнд. </span><span class="sxs-lookup"><span data-stu-id="ad87f-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="ad87f-237">Операнд необходимо указать в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ad87f-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="ad87f-238">Код **\_ bstr \_ t с** пустой строкой в качестве значения.</span><span class="sxs-lookup"><span data-stu-id="ad87f-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="ad87f-239">Variant</span><span class="sxs-lookup"><span data-stu-id="ad87f-239">Variant</span></span>

<span data-ttu-id="ad87f-240">Если вам нужно закодировать отсутствующий операнд **Variant** в Visual Basic, просто опустить операнд.</span><span class="sxs-lookup"><span data-stu-id="ad87f-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="ad87f-241">Необходимо указать все операнды в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ad87f-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="ad87f-242">Задайте код для **\_ \_** отсутствующих параметров **Variant,** для варианта не заданы специальные значения DISP \_ E \_ PARAMNOTFOUND и type, VT \_ ERROR.</span><span class="sxs-lookup"><span data-stu-id="ad87f-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="ad87f-243">Кроме того, укажите **vtMissing**— эквивалентную предопределенную константу, предоставленную директивой **\# импорта.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="ad87f-244">\-или использовать —</span><span class="sxs-lookup"><span data-stu-id="ad87f-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="ad87f-245">Объявление варианта</span><span class="sxs-lookup"><span data-stu-id="ad87f-245">Declaring a variant</span></span>

<span data-ttu-id="ad87f-246">В Visual Basic **variant** объявляется с помощью заявления **Dim** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad87f-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="ad87f-247">В Visual C++ объявите переменную как тип **\_ variant \_ t**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="ad87f-248">Ниже показано несколько **\_ схемных \_ вариантов t** объявлений.</span><span class="sxs-lookup"><span data-stu-id="ad87f-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="ad87f-249">Эти объявления просто дают приблизительное представление о том, что бы вы напрограмме в собственной программе.</span><span class="sxs-lookup"><span data-stu-id="ad87f-249">These declarations merely give a rough idea of what you would code in your own program.</span></span> <span data-ttu-id="ad87f-250">Дополнительные сведения см. в примерах ниже и документации по Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ad87f-250">For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="ad87f-251">Использование массивов вариантов</span><span class="sxs-lookup"><span data-stu-id="ad87f-251">Using arrays of variants</span></span>

<span data-ttu-id="ad87f-252">В Visual Basic массивы **Variant** можно закодировать с помощью заявления **Dim** или использовать функцию **Array,** как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="ad87f-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="ad87f-253">В следующем примере Visual C++ демонстрируется использование **SafeArray,** используемой с **\_ вариантом \_ t**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="ad87f-254">Следующие примечания соответствуют закомментным разделам в примере кода.</span><span class="sxs-lookup"><span data-stu-id="ad87f-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="ad87f-255">Опять же, в рамках функции TESTHR() определена возможность использования существующего механизма обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="ad87f-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="ad87f-256">Вам нужен только одномерный массив, поэтому вместо объявления **SAFEARRAYBOUND** общего назначения и функции **SafeArrayCreate** можно использовать **SafeArrayCreate.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-256">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function.</span></span> <span data-ttu-id="ad87f-257">Вот как будет выглядеть этот код с помощью **SafeArrayCreate:**</span><span class="sxs-lookup"><span data-stu-id="ad87f-257">The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="ad87f-258">Схема, обнаруженная по нумероватой константы **adSchemaColumns,** связана с четырьмя столбцами ограничений: TABLE \_ CATALOG, TABLE \_ SCHEMA, TABLE \_ NAME и COLUMN \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="ad87f-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="ad87f-259">Поэтому создается массив значений **Variant** с четырьмя элементами.</span><span class="sxs-lookup"><span data-stu-id="ad87f-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="ad87f-260">Затем указывается значение ограничения, соответствующее третьему столбце , TABLE \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="ad87f-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="ad87f-261">**Возвращаемая группа** записей состоит из нескольких столбцов, подмножество которых является столбцом ограничения.</span><span class="sxs-lookup"><span data-stu-id="ad87f-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="ad87f-262">Значения столбцов ограничений для каждой возвращаемой строки должны быть одинаковыми с соответствующими значениями ограничений.</span><span class="sxs-lookup"><span data-stu-id="ad87f-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="ad87f-263">Те, кто знаком **с SafeArrays,** могут быть удивлены тому, что **SafeArrayDestroy**() не вызван перед выходом.</span><span class="sxs-lookup"><span data-stu-id="ad87f-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="ad87f-264">Вызов **SafeArrayDestroy**() в данном случае приведет к исключению во время запуска.</span><span class="sxs-lookup"><span data-stu-id="ad87f-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="ad87f-265">Причина заключается в том, что деструктор для vtCriteria будет вызывать **VariantClear**(), когда вариант **\_ \_ t** выходит за пределы области, что освободит **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="ad87f-266">Вызов **SafeArrayDestroy** без очистки варианта **\_ \_ t** вручную приведет к тому, что деструктор попытается очистить недопустимый **указатель SafeArray.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="ad87f-267">Если **бы был вызван SafeArrayDestroy,** код выглядел бы так:</span><span class="sxs-lookup"><span data-stu-id="ad87f-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="ad87f-268">Однако гораздо проще позволить варианту **\_ \_** не управлять **SafeArray.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


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

### <a name="using-property-getputputref"></a><span data-ttu-id="ad87f-269">Использование свойства Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="ad87f-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="ad87f-270">В Visual Basic имя свойства не квалифицироваться по извлечению, назначению или назначению ссылки.</span><span class="sxs-lookup"><span data-stu-id="ad87f-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="ad87f-271">В этом примере Visual C++ демонстрируется / **свойство Get Put** /\* *PutRef\*\*\*Property.*</span><span class="sxs-lookup"><span data-stu-id="ad87f-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="ad87f-272">Следующие примечания соответствуют закомментным разделам в примере кода.</span><span class="sxs-lookup"><span data-stu-id="ad87f-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="ad87f-273">В этом примере используются две формы отсутствующих аргументов строки: явная константа, **strMissing** и строка, которую компилятор будет использовать для создания временной **\_ строки \_ t,** которая будет существовать для области метода **Open.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="ad87f-274">Нет необходимости привести операнд \> rs-PutRefActiveConnection(cn) к (IDispatch), так как тип операнда уже \* есть (IDispatch). \*</span><span class="sxs-lookup"><span data-stu-id="ad87f-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="ad87f-275">Использование GetItem(x) и Item \[ x\]</span><span class="sxs-lookup"><span data-stu-id="ad87f-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="ad87f-276">В Visual Basic примере демонстрируется стандартный и альтернативный синтаксис **для элемента**().</span><span class="sxs-lookup"><span data-stu-id="ad87f-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="ad87f-277">В этом примере Visual C++ **демонстрируется item.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="ad87f-278">Следующее примечание соответствует закомментным разделам в примере кода.</span><span class="sxs-lookup"><span data-stu-id="ad87f-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="ad87f-279">При доступе к коллекции с помощью **Item** индекс **2** должен быть приводиться к длинному, чтобы был вызван соответствующий конструктор. </span><span class="sxs-lookup"><span data-stu-id="ad87f-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="ad87f-280">Casting ADO object pointers with (IDispatch) \*</span><span class="sxs-lookup"><span data-stu-id="ad87f-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="ad87f-281">В следующем примере Visual C++ демонстрируется использование (IDispatch) для \* придаия указателям объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="ad87f-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="ad87f-282">Следующие примечания соответствуют закомментным разделам в примере кода.</span><span class="sxs-lookup"><span data-stu-id="ad87f-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="ad87f-283">Укажите открытый **объект Connection** в явно кодовом **варианте.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="ad87f-284">Привязим его с помощью (IDispatch), чтобы был вызван правильный \* конструктор.</span><span class="sxs-lookup"><span data-stu-id="ad87f-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="ad87f-285">Кроме того, явно установите для второго параметра **\_ variant \_ t** значение по умолчанию **true,** поэтому количество ссылок на объект будет правильным после окончания операции **Recordset::Open.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="ad87f-286">Выражение ( bstr t) не является оператором cast, а оператором \_ variant \_ **\_ \_ t,** который извлекает **\_ строку bstr \_ t** из **варианта,** возвращаемого **значением**.</span><span class="sxs-lookup"><span data-stu-id="ad87f-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="ad87f-287">Выражение (char) не является оператором cast, а \* **\_ оператором bstr \_ t,** который извлекает указатель на инкапсулированную строку в **\_ объекте bstr \_ t.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="ad87f-288">В этом разделе кода демонстрируются некоторые полезные поведения операторов **\_ variant \_ t** и **\_ bstr \_ t.**</span><span class="sxs-lookup"><span data-stu-id="ad87f-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

