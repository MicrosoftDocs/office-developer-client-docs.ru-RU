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
# <a name="visual-c-ado-programming"></a><span data-ttu-id="a2761-102">Программирование для ADO на Visual C++</span><span class="sxs-lookup"><span data-stu-id="a2761-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="a2761-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2761-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2761-104">Ссылка ADO API описывает функциональность интерфейса программирования приложений ADO (API) с помощью синтаксиса, аналогичного Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2761-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="a2761-105">Хотя целевой аудиторией являются все пользователи, программисты ADO используют различные языки, такие **\#** как Visual Basic, Visual C++ (с директивой импорта и без нее) и Visual J++ (с пакетом классов ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="a2761-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="a2761-106">Чтобы обеспечить такое разнообразие, индексы синтаксиса ADO для visual [C++](using-ado-with-microsoft-visual-c.md) предоставляют синтаксис visual C++ с языковым синтаксисом со ссылками на общие описания функциональных возможностей, параметров, исключительных поведений и т. д. в справке API.</span><span class="sxs-lookup"><span data-stu-id="a2761-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="a2761-107">ADO реализуется с интерфейсами COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="a2761-107">ADO is implemented with COM (Component Object Model) interfaces.</span></span> <span data-ttu-id="a2761-108">Однако для программистов проще работать с COM на определенных языках программирования, чем с другими.</span><span class="sxs-lookup"><span data-stu-id="a2761-108">However, it is easier for programmers to work with COM in certain programming languages than others.</span></span> <span data-ttu-id="a2761-109">Например, почти все сведения об использовании COM обрабатываются неявно для Visual Basic, в то время как программисты Visual C++ должны сами ходить к этим сведениям.</span><span class="sxs-lookup"><span data-stu-id="a2761-109">For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="a2761-110">В следующих разделах обобщены сведения о программистах C и C++ с помощью ADO и **\# директивы импорта.**</span><span class="sxs-lookup"><span data-stu-id="a2761-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="a2761-111">Основное внимание уделяется типам данных, определенным com **(Variant,** **BSTR** и **SafeArray),** а также обработке ошибок \_ (ошибка \_ com).</span><span class="sxs-lookup"><span data-stu-id="a2761-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="a2761-112">Использование \# директивы компилятор импорта</span><span class="sxs-lookup"><span data-stu-id="a2761-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="a2761-113">Директива **\# по** импорту visual C++ упрощает работу с методами и свойствами ADO.</span><span class="sxs-lookup"><span data-stu-id="a2761-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="a2761-114">Директива принимает имя файла, содержащего библиотеку типов, например ADO .dll (Msado15.dll), и создает файлы заголовки, содержащие декларации типа, интеллектуальные указатели для интерфейсов и переумежаемые константы.</span><span class="sxs-lookup"><span data-stu-id="a2761-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="a2761-115">Каждый интерфейс инкапсулируется или завернут в класс.</span><span class="sxs-lookup"><span data-stu-id="a2761-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="a2761-116">Для каждой операции в классе (то есть вызова метода или свойства) имеется объявление о вызове операции напрямую (то есть "необработанные" формы операции), а также объявление об вызове необработанных операций и вызове ошибки com, если операция не выполняется успешно.</span><span class="sxs-lookup"><span data-stu-id="a2761-116">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully.</span></span> <span data-ttu-id="a2761-117">Если операция является свойством, обычно существует директива компиляторов, которая создает альтернативный синтаксис для операции с синтаксисом, как Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2761-117">If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="a2761-118">Операции, которые получают значение свойства, имеют имена формы\**Get\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="a2761-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="a2761-119">Операции, которые устанавливают значение свойства, имеют имена формы\**Put\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="a2761-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="a2761-120">Операции, задав значение свойства с указателем на объект ADO, имеют имена формы\**PutRef\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="a2761-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="a2761-121">Вы можете получить или установить свойство с вызовами этих форм:</span><span class="sxs-lookup"><span data-stu-id="a2761-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="a2761-122">Использование директив свойств</span><span class="sxs-lookup"><span data-stu-id="a2761-122">Using property directives</span></span>

<span data-ttu-id="a2761-123">Директива компиляторов **\_ \_ declspec(property...)** — это языковой расширение C для Microsoft, которое объявляет функцию, используемую в качестве свойства для альтернативного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="a2761-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="a2761-124">В результате вы можете установить или получить значения свойства таким образом, как Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2761-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="a2761-125">Например, можно установить и получить свойство таким образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="a2761-126">Обратите внимание, что вам не нужно кодировать:</span><span class="sxs-lookup"><span data-stu-id="a2761-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="a2761-127">Компилятор будет создавать соответствующий вызов \**Get\*\*\*-,* **Put**-или \**PutRef\*\*\*Property* на основе того, какой альтернативный синтаксис объявлен и читается ли свойство или написано.</span><span class="sxs-lookup"><span data-stu-id="a2761-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="a2761-128">Директива компилятор **\_ \_ declspec(property...)** может объявлять только **get,** **put**, or **get** and **put** alternative syntax for a function.</span><span class="sxs-lookup"><span data-stu-id="a2761-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="a2761-129">Операции только для чтения имеют только **объявление получения;** Операции только для записи имеют только объявление **пут;** операции, которые являются одновременно чтением и написанием, имеют как **получать, так** **и ставить** объявления.</span><span class="sxs-lookup"><span data-stu-id="a2761-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="a2761-130">С этой директивой можно сделать только две декларации; однако каждое свойство может иметь три свойства: \**Get\*\*\*Property*, \**Put\*\*\*Property* и \**PutRef\*\*\*Property*.</span><span class="sxs-lookup"><span data-stu-id="a2761-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="a2761-131">В этом случае альтернативный синтаксис имеется только в двух формах свойства.</span><span class="sxs-lookup"><span data-stu-id="a2761-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="a2761-132">Например, свойство **Объекта** **Команды ActiveConnection** объявляется с альтернативным синтаксисом для \**Get\*\*\*ActiveConnection* и \**PutRef\*\*\*ActiveConnection.*</span><span class="sxs-lookup"><span data-stu-id="a2761-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="a2761-133">Синтаксис **PutRef**— это хороший выбор, так как на  практике обычно необходимо поместить  в это свойство открытый объект Connection (то есть указатель объекта Подключения).</span><span class="sxs-lookup"><span data-stu-id="a2761-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="a2761-134">С другой стороны, объект **Recordset** имеет операции **Get-,** **Put**-и \**PutRef\*\*\*ActiveConnection,* но нет альтернативного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="a2761-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="a2761-135">Коллекции, метод GetItem и свойство Item</span><span class="sxs-lookup"><span data-stu-id="a2761-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="a2761-136">ADO определяет несколько коллекций, в том числе **Fields,** **Parameters,** **Properties** и **Errors.**</span><span class="sxs-lookup"><span data-stu-id="a2761-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="a2761-137">В Visual C++метод \*\*GetItem \*\*\*(index)\*\*\*\*\* возвращает участника коллекции.</span><span class="sxs-lookup"><span data-stu-id="a2761-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="a2761-138">*Index* — **это вариант,** значение которого — это либо числовой индекс участника в коллекции, либо строка, содержащая имя участника.</span><span class="sxs-lookup"><span data-stu-id="a2761-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="a2761-139">Директива компиляторов **\_ \_ declspec(property...)** объявляет свойство **Item** альтернативным синтаксисом для основного метода **GetItem()** каждой коллекции.</span><span class="sxs-lookup"><span data-stu-id="a2761-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="a2761-140">Альтернативный синтаксис использует квадратные скобки и похож на ссылку массива.</span><span class="sxs-lookup"><span data-stu-id="a2761-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="a2761-141">В общем, эти две формы выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="a2761-142">Например, назначьте значение для поля объекта **Recordset** с именем  ***rs,*** полученное из таблицы авторов базы **данных пабов.**</span><span class="sxs-lookup"><span data-stu-id="a2761-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="a2761-143">Используйте свойство **Item()** для  доступа к третьему  полю коллекции полей объектов **Recordset** (коллекции индексироваться с нуля; предположим, что третье поле называется ***au \_ fname).***</span><span class="sxs-lookup"><span data-stu-id="a2761-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="a2761-144">Затем вызовите **метод Value()** на **объекте Field,** чтобы назначить значение строки.</span><span class="sxs-lookup"><span data-stu-id="a2761-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="a2761-145">Это может быть выражено Visual Basic в следующих четырех способах (последние две формы уникальны для Visual Basic, другие языки не имеют эквивалентов):</span><span class="sxs-lookup"><span data-stu-id="a2761-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="a2761-146">Эквивалент visual C++ для первых двух форм выше:</span><span class="sxs-lookup"><span data-stu-id="a2761-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="a2761-147">\-or- (также показан альтернативный синтаксис для свойства **Value)**</span><span class="sxs-lookup"><span data-stu-id="a2761-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="a2761-148">Типы данных, специфические для COM</span><span class="sxs-lookup"><span data-stu-id="a2761-148">COM-specific data types</span></span>

<span data-ttu-id="a2761-149">Как правило, любой тип Visual Basic, который вы найдете в ссылке ADO API, имеет эквивалент Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a2761-149">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent.</span></span> <span data-ttu-id="a2761-150">К ним относятся стандартные типы данных, такие как **неподписаный** шар для Visual Basic **byte,** краткое **для** **Integer** и **long** for **Long**.</span><span class="sxs-lookup"><span data-stu-id="a2761-150">These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**.</span></span> <span data-ttu-id="a2761-151">Посмотрите в индексах синтаксиса, чтобы точно узнать, что требуется для операндов данного метода или свойства.</span><span class="sxs-lookup"><span data-stu-id="a2761-151">Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="a2761-152">Исключениями из этого правила являются типы данных, специфические для COM: **Variant,** **BSTR** и **SafeArray.**</span><span class="sxs-lookup"><span data-stu-id="a2761-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="a2761-153">Variant</span><span class="sxs-lookup"><span data-stu-id="a2761-153">Variant</span></span>

<span data-ttu-id="a2761-154">**Variant —** это структурированный тип данных, содержащий член значения и тип данных.</span><span class="sxs-lookup"><span data-stu-id="a2761-154">A **Variant** is a structured data type that contains a value member and a data type member.</span></span> <span data-ttu-id="a2761-155">Вариант **может** содержать широкий диапазон других типов данных, включая другой Вариант, BSTR, Boolean, указатель IDispatch или IUnknown, валюту, дату и т. д.</span><span class="sxs-lookup"><span data-stu-id="a2761-155">A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</span></span> <span data-ttu-id="a2761-156">COM также предоставляет методы, которые устроит преобразование одного типа данных в другой.</span><span class="sxs-lookup"><span data-stu-id="a2761-156">COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="a2761-157">Вариант **\_ \_ t** class инкапсулирует и управляет типом **данных Variant.**</span><span class="sxs-lookup"><span data-stu-id="a2761-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="a2761-158">Когда ссылка ADO API говорит, что операнд метода или свойства принимает значение, это обычно означает, что значение передается в **\_ \_ варианте t**.</span><span class="sxs-lookup"><span data-stu-id="a2761-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="a2761-159">Это правило явно верно, когда в разделе **Параметры** в разделах ADO API Reference говорится, что operand является **вариантом**.</span><span class="sxs-lookup"><span data-stu-id="a2761-159">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**.</span></span> <span data-ttu-id="a2761-160">Одним из исключений является то, что в документации явно говорится, что операнд принимает стандартный тип данных, например **Long** или **Byte,** или переуметив.</span><span class="sxs-lookup"><span data-stu-id="a2761-160">One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration.</span></span> <span data-ttu-id="a2761-161">Другим исключением является то, что операнд принимает **строку**.</span><span class="sxs-lookup"><span data-stu-id="a2761-161">Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="a2761-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="a2761-162">BSTR</span></span>

<span data-ttu-id="a2761-163">**BSTR** **(B** asic **STR** ing) — структурированный тип данных, содержащий строку символов и длину строки.</span><span class="sxs-lookup"><span data-stu-id="a2761-163">A **BSTR** (**B** asic **STR** ing) is a structured data type that contains a character string and the string's length.</span></span> <span data-ttu-id="a2761-164">COM предоставляет методы выделения, управления и **бесплатного BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a2761-164">COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="a2761-165">Класс **\_ bstr \_ t** инкапсулирует и управляет типом **данных BSTR.**</span><span class="sxs-lookup"><span data-stu-id="a2761-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="a2761-166">Когда ссылка ADO API говорит, что метод или свойство принимает значение **String,** это означает, что значение находится в виде **\_ bstr \_ t**.</span><span class="sxs-lookup"><span data-stu-id="a2761-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a><span data-ttu-id="a2761-167">\_Литье вариант t и \_ \_ bstr t \_ классов</span><span class="sxs-lookup"><span data-stu-id="a2761-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="a2761-168">Часто не требуется явно кодировать вариант **\_ \_ t или** **\_ bstr \_ t** в аргументе для операции.</span><span class="sxs-lookup"><span data-stu-id="a2761-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="a2761-169">Если в **\_ классе вариант \_ t** или **\_ bstr \_ t** есть конструктор, соответствующий типу данных аргумента, компилятор будет создавать соответствующий вариант **\_ \_ t** или **\_ bstr \_ t**.</span><span class="sxs-lookup"><span data-stu-id="a2761-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="a2761-170">Однако если аргумент неоднозначный, то есть тип данных аргумента соответствует более чем одному конструктору, необходимо ввести аргумент с соответствующим типом данных, чтобы вызвать правильного конструктора.</span><span class="sxs-lookup"><span data-stu-id="a2761-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="a2761-171">Например, объявление для метода **Recordset::Open:**</span><span class="sxs-lookup"><span data-stu-id="a2761-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="a2761-172">Аргумент ActiveConnection ссылается на вариант **\_ \_ t,** который можно кодировать как строку подключения или указатель на открытый объект **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="a2761-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="a2761-173">Правильный вариант **\_ \_ t** будет построен неявно, если вы передаете строку, например "DSN=pubs;uid=sa;pwd=;", или указатель, например "(IDispatch) \* pConn".</span><span class="sxs-lookup"><span data-stu-id="a2761-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="a2761-174">Или вы можете явно кодировать вариант **\_ \_ t,** содержащий указатель, например \_ "variant \_ t((IDispatch) \* pConn, true)".</span><span class="sxs-lookup"><span data-stu-id="a2761-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="a2761-175">В гипсе (IDispatch) устраняется двусмысленность с помощью другого конструктора, который принимает указатель на \* интерфейс IUnknown.</span><span class="sxs-lookup"><span data-stu-id="a2761-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="a2761-176">Важно, хотя и редко упоминалось, что ADO — это интерфейс IDispatch.</span><span class="sxs-lookup"><span data-stu-id="a2761-176">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface.</span></span> <span data-ttu-id="a2761-177">Всякий раз, когда указатель на объект ADO должен быть передан в качестве **варианта,** этот указатель должен быть отлит в качестве указателя для интерфейса IDispatch.</span><span class="sxs-lookup"><span data-stu-id="a2761-177">Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="a2761-178">Последний случай явно кодирует второй аргумент boolean конструктора с его необязательным значением по умолчанию true.</span><span class="sxs-lookup"><span data-stu-id="a2761-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="a2761-179">В этом аргументе конструктор **Variant** вызывает метод **AddRef**(), который компенсирует автоматический вызов метода **\_ \_ вариантов t::Release**() при завершении вызова метода ADO или свойства.</span><span class="sxs-lookup"><span data-stu-id="a2761-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="a2761-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="a2761-180">SafeArray</span></span>

<span data-ttu-id="a2761-181">**SafeArray** — это структурированный тип данных, содержащий массив других типов данных.</span><span class="sxs-lookup"><span data-stu-id="a2761-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="a2761-182">**SafeArray** называется  безопасным, так как содержит сведения о границах каждого измерения массива и ограничивает доступ к элементам массива в этих границах.</span><span class="sxs-lookup"><span data-stu-id="a2761-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="a2761-183">Если в ссылке ADO API говорится, что метод или свойство принимает или возвращает массив, это означает, что метод или свойство принимает или возвращает массив **SafeArray,** а не массив C/C++.</span><span class="sxs-lookup"><span data-stu-id="a2761-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="a2761-184">Например, для второго параметра метода **OpenSchema объекта Подключения** требуется массив значений  **Variant.**</span><span class="sxs-lookup"><span data-stu-id="a2761-184">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values.</span></span> <span data-ttu-id="a2761-185">Эти **значения Variant** должны быть переданы в качестве элементов **SafeArray,** и что **SafeArray** должен быть задат как значение другого **варианта**.</span><span class="sxs-lookup"><span data-stu-id="a2761-185">Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**.</span></span> <span data-ttu-id="a2761-186">Это то, что другой **вариант,** который передается в качестве второго аргумента **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="a2761-186">It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="a2761-187">В качестве дополнительных примеров первым аргументом метода **Find** является **вариант,** значение которого — одномерный **SafeArray;** каждый из необязательных первого и второго аргументов **AddNew** является одномерным **SafeArray;** и возвращаемая величина метода **GetRows** — это **вариант,** значение которого — двухмерный **SafeArray.**</span><span class="sxs-lookup"><span data-stu-id="a2761-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="a2761-188">Отсутствующие и невыполнение параметров</span><span class="sxs-lookup"><span data-stu-id="a2761-188">Missing and default parameters</span></span>

<span data-ttu-id="a2761-189">Visual Basic позволяет пропускать параметры в методах.</span><span class="sxs-lookup"><span data-stu-id="a2761-189">Visual Basic allows missing parameters in methods.</span></span> <span data-ttu-id="a2761-190">Например, метод Open  **объекта Recordset** имеет пять параметров, но можно пропустить промежуточные параметры и не использовать параметры trailing.</span><span class="sxs-lookup"><span data-stu-id="a2761-190">For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters.</span></span> <span data-ttu-id="a2761-191">BSTR **или** **Variant** по умолчанию будут заменены в зависимости от типа данных отсутствующих operand.</span><span class="sxs-lookup"><span data-stu-id="a2761-191">A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="a2761-192">В C/C++все операнды должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="a2761-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="a2761-193">Если необходимо указать отсутствующий параметр, тип данных которого — строка, укажите **\_ bstr \_ t,** содержащий строку null.</span><span class="sxs-lookup"><span data-stu-id="a2761-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="a2761-194">Если необходимо указать отсутствующий параметр, тип данных которого является **Вариантом,** укажите вариант **\_ \_ t** со значением DISP \_ E \_ PARAMNOTFOUND и типом ошибки \_ VT.</span><span class="sxs-lookup"><span data-stu-id="a2761-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="a2761-195">Кроме того, укажите эквивалентный вариант **\_ \_ t** **constant, vtMissing,** который поставляется директивой **\# импорта.**</span><span class="sxs-lookup"><span data-stu-id="a2761-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="a2761-196">Три метода являются исключениями из обычного использования **vtMissing.**</span><span class="sxs-lookup"><span data-stu-id="a2761-196">Three methods are exceptions to the typical use of **vtMissing**.</span></span> <span data-ttu-id="a2761-197">Это методы **выполнения** объектов **Подключения** и **Команды,** а также метод **NextRecordset** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="a2761-197">These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object.</span></span> <span data-ttu-id="a2761-198">Следующие подписи:</span><span class="sxs-lookup"><span data-stu-id="a2761-198">The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="a2761-199">Параметры, *RecordsAffected* и *Parameters*, являются указателями на **вариант**.</span><span class="sxs-lookup"><span data-stu-id="a2761-199">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**.</span></span> <span data-ttu-id="a2761-200">*Параметры* — это параметр ввода, который  указывает адрес варианта, содержащего один параметр или массив параметров, который изменит выполненную команду.</span><span class="sxs-lookup"><span data-stu-id="a2761-200">*Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed.</span></span> <span data-ttu-id="a2761-201">*RecordsAffected* — это выходной параметр, который указывает адрес **варианта,** где возвращается количество строк, затронутых методом.</span><span class="sxs-lookup"><span data-stu-id="a2761-201">*RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="a2761-202">В методе **Командный** объект **Выполнить** указать, что  параметры не заданы, задав параметры либо к vtMissing (что рекомендуется), либо к указателю null (т. е. NULL или zero \&  (0)).</span><span class="sxs-lookup"><span data-stu-id="a2761-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="a2761-203">Если *параметры* заданы в указателе null, метод внутренне заменяет эквивалент **vtMissing,** а затем завершает операцию.</span><span class="sxs-lookup"><span data-stu-id="a2761-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="a2761-204">Во всех методах указать, что количество затронутых записей не следует возвращать, установив *RecordsAffected* в указатель null.</span><span class="sxs-lookup"><span data-stu-id="a2761-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="a2761-205">В этом случае указатель null — это не столько отсутствующий параметр, сколько указание на то, что метод должен отменить количество затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="a2761-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="a2761-206">Таким образом, для этих трех методов допустимо кодировать что-то, например:</span><span class="sxs-lookup"><span data-stu-id="a2761-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="a2761-207">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="a2761-207">Error handling</span></span>

<span data-ttu-id="a2761-208">В com большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция.</span><span class="sxs-lookup"><span data-stu-id="a2761-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="a2761-209">Директива **\# импорта** создает код оболочки вокруг каждого "необработанных" метода или свойства и проверяет возвращаемую HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a2761-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="a2761-210">Если HRESULT указывает на сбой, код оболочки вызывает ошибку COM, вызывая ошибку com issue errorex() с кодом возврата \_ \_ HRESULT в качестве \_ аргумента.</span><span class="sxs-lookup"><span data-stu-id="a2761-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="a2761-211">Объекты ошибки COM могут быть пойманы в **блоке try** - **catch.**</span><span class="sxs-lookup"><span data-stu-id="a2761-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="a2761-212">(Для обеспечения эффективности ловите ссылку на объект **\_ ошибки \_ com.)**</span><span class="sxs-lookup"><span data-stu-id="a2761-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="a2761-213">Помните, что это ошибки ADO: они являются результатом сбоя операции ADO.</span><span class="sxs-lookup"><span data-stu-id="a2761-213">Remember, these are ADO errors: they result from the ADO operation failing.</span></span> <span data-ttu-id="a2761-214">Ошибки, возвращаемые поставщиком, отображаются как **объекты ошибки** в коллекции **Ошибки** **объекта** Подключения.</span><span class="sxs-lookup"><span data-stu-id="a2761-214">Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="a2761-215">Директива **\# импорта** создает только процедуры обработки ошибок для методов и свойств, объявленных в ADO .dll.</span><span class="sxs-lookup"><span data-stu-id="a2761-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="a2761-216">Тем не менее, вы можете воспользоваться этим же механизмом обработки ошибок, написав собственную функцию проверки ошибок макроса или inline.</span><span class="sxs-lookup"><span data-stu-id="a2761-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="a2761-217">Примеры см. в разделе [Visual C++ Extensions](visual-c-extensions-for-ado.md)или код в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a2761-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="a2761-218">Visual C++ эквиваленты Visual Basic конвенций</span><span class="sxs-lookup"><span data-stu-id="a2761-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="a2761-219">Ниже приводится сводка нескольких конвенций в документации ADO, закодирования в Visual Basic, а также их эквивалентов в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a2761-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="a2761-220">Объявление объекта ADO</span><span class="sxs-lookup"><span data-stu-id="a2761-220">Declaring an ADO object</span></span>

<span data-ttu-id="a2761-221">В Visual Basic объектной переменной ADO (в данном случае для объекта **Recordset)** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="a2761-222">Пункт "ADODB. Recordset", является progID объекта **Recordset,** как определено в реестре.</span><span class="sxs-lookup"><span data-stu-id="a2761-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="a2761-223">Новый экземпляр объекта **Record** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="a2761-224">\-or-</span><span class="sxs-lookup"><span data-stu-id="a2761-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="a2761-225">В Visual C++директива **\# импорта** создает интеллектуальные объявления типа указателей для всех объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="a2761-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="a2761-226">Например, переменная, которая указывает на объект **\_ Recordset,** имеет тип **\_ RecordsetPtr** и объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="a2761-227">Переменная, которая указывает на новый экземпляр объекта **\_ Recordset,** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="a2761-228">\-or-</span><span class="sxs-lookup"><span data-stu-id="a2761-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="a2761-229">\-or-</span><span class="sxs-lookup"><span data-stu-id="a2761-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="a2761-230">После того как будет вызван метод **CreateInstance,** переменную можно использовать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="a2761-231">Обратите внимание, что в одном случае оператор "." используется так, как если бы переменная была экземпляром класса (rs. CreateInstance), а в другом случае оператор "- " используется так, как если бы переменная была указателем на интерфейс \> (rs-Open). \></span><span class="sxs-lookup"><span data-stu-id="a2761-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="a2761-232">Одна переменная может использоваться двумя способами, так как оператор "-" перегружен, чтобы позволить экземпляру класса вести себя как указатель \> на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a2761-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="a2761-233">Частный член класса переменной экземпляра содержит указатель на интерфейс **\_ Recordset;** оператор "-" возвращает этот указатель, а возвращаемая указатель имеет доступ к участникам объекта \> **\_ Recordset.**</span><span class="sxs-lookup"><span data-stu-id="a2761-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="a2761-234">Кодирование отсутствующих параметров</span><span class="sxs-lookup"><span data-stu-id="a2761-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="a2761-235">String</span><span class="sxs-lookup"><span data-stu-id="a2761-235">String</span></span>

<span data-ttu-id="a2761-236">Если вам нужно кодировать отсутствующий операнд **String** в Visual Basic, вы просто опустить operand.</span><span class="sxs-lookup"><span data-stu-id="a2761-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="a2761-237">Необходимо указать операнд в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a2761-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="a2761-238">Код **\_ bstr \_ t** с пустой строкой в качестве значения.</span><span class="sxs-lookup"><span data-stu-id="a2761-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="a2761-239">Variant</span><span class="sxs-lookup"><span data-stu-id="a2761-239">Variant</span></span>

<span data-ttu-id="a2761-240">При необходимости кодировать недостающий операнд **Variant** в Visual Basic, вы просто опустить operand.</span><span class="sxs-lookup"><span data-stu-id="a2761-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="a2761-241">Необходимо указать все операнды в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a2761-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="a2761-242">Код отсутствует **параметр Variant** с вариантом **\_ \_ t,** заданным для специального значения, DISP E \_ \_ PARAMNOTFOUND и типа, VT \_ ERROR.</span><span class="sxs-lookup"><span data-stu-id="a2761-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="a2761-243">Кроме того, укажите **vtMissing**, эквивалентную заранее определенной константе, предоставленной директивой **\# импорта.**</span><span class="sxs-lookup"><span data-stu-id="a2761-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="a2761-244">\-или использование —</span><span class="sxs-lookup"><span data-stu-id="a2761-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="a2761-245">Объявление варианта</span><span class="sxs-lookup"><span data-stu-id="a2761-245">Declaring a variant</span></span>

<span data-ttu-id="a2761-246">В Visual Basic **вариант** объявляется с заявлением **Dim** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2761-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="a2761-247">В Visual C++объявите переменную как вариант **\_ \_ типа t**.</span><span class="sxs-lookup"><span data-stu-id="a2761-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="a2761-248">Ниже показано несколько **\_ схемных \_** объявлений t вариантов.</span><span class="sxs-lookup"><span data-stu-id="a2761-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="a2761-249">Эти объявления просто дают приблизительное представление о том, что вы будете кодировать в собственной программе.</span><span class="sxs-lookup"><span data-stu-id="a2761-249">These declarations merely give a rough idea of what you would code in your own program.</span></span> <span data-ttu-id="a2761-250">Дополнительные сведения см. в примерах ниже и документации Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a2761-250">For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="a2761-251">Использование массивов вариантов</span><span class="sxs-lookup"><span data-stu-id="a2761-251">Using arrays of variants</span></span>

<span data-ttu-id="a2761-252">В Visual Basic массивы **Вариантов** можно закодировать с помощью заявления **Dim** или использовать функцию **Array,** как показано в следующем коде примера:</span><span class="sxs-lookup"><span data-stu-id="a2761-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="a2761-253">В следующем примере Visual C++ показано использование **SafeArray,** используемой с **\_ вариантом \_ t**.</span><span class="sxs-lookup"><span data-stu-id="a2761-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="a2761-254">Следующие заметки соответствуют разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="a2761-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="a2761-255">В очередной раз установлена функция inline TESTHR() для использования существующего механизма обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="a2761-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="a2761-256">Вам нужен только одномерный массив, поэтому вы можете использовать **SafeArrayCreateVector** вместо общего объявления **SAFEARRAYBOUND** и **функции SafeArrayCreate.**</span><span class="sxs-lookup"><span data-stu-id="a2761-256">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function.</span></span> <span data-ttu-id="a2761-257">Ниже приводится пример того, как будет выглядеть этот код с помощью **SafeArrayCreate:**</span><span class="sxs-lookup"><span data-stu-id="a2761-257">The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="a2761-258">Схема, идентифицированная константой, **adSchemaColumns,** связана с четырьмя столбцами ограничений: TABLE \_ CATALOG, \_ TABLE SCHEMA, TABLE \_ NAME и COLUMN \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="a2761-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="a2761-259">Поэтому создается массив значений **Variant** с четырьмя элементами.</span><span class="sxs-lookup"><span data-stu-id="a2761-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="a2761-260">Затем задано значение ограничения, соответствующее третьему столбце, TABLE \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="a2761-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="a2761-261">Возвращенный **набор** записей состоит из нескольких столбцов, подмножество которых — столбцы ограничений.</span><span class="sxs-lookup"><span data-stu-id="a2761-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="a2761-262">Значения столбцов ограничений для каждой возвращаемой строки должны быть одинаковыми с соответствующими значениями ограничения.</span><span class="sxs-lookup"><span data-stu-id="a2761-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="a2761-263">Те, кто знаком с **SafeArrays,** могут быть удивлены, что **SafeArrayDestroy**() не вызван перед выходом.</span><span class="sxs-lookup"><span data-stu-id="a2761-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="a2761-264">На самом деле вызов **SafeArrayDestroy**() в этом случае приведет к исключению времени запуска.</span><span class="sxs-lookup"><span data-stu-id="a2761-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="a2761-265">Причина в том, что деструктор для vtCriteria будет вызывать **VariantClear**(), когда вариант **\_ \_ t** выходит из области, что освободит **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="a2761-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="a2761-266">Вызов **SafeArrayDestroy** без вручную очистки варианта **\_ \_ t** приведет к деструктору, чтобы попытаться очистить недействительный **указатель SafeArray.**</span><span class="sxs-lookup"><span data-stu-id="a2761-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="a2761-267">Если **бы был вызван SafeArrayDestroy,** код выглядел бы так:</span><span class="sxs-lookup"><span data-stu-id="a2761-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="a2761-268">Тем не менее, гораздо проще позволить **\_ \_ варианту t управлять** **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="a2761-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


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

### <a name="using-property-getputputref"></a><span data-ttu-id="a2761-269">Использование свойства Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="a2761-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="a2761-270">В Visual Basic, имя свойства не может быть квалифицировано, будет ли оно извлечено, назначено или назначено ссылку.</span><span class="sxs-lookup"><span data-stu-id="a2761-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="a2761-271">В этом примере Visual C++ показано свойство **Get** /  /\* *Put PutRef\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="a2761-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="a2761-272">Следующие заметки соответствуют разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="a2761-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="a2761-273">В этом примере используются две формы отсутствующих аргументов строк: явная константа, **strMissing** и строка, которую компилятор будет использовать для создания временной **\_ bstr \_ t,** которая будет существовать для области метода **Open.**</span><span class="sxs-lookup"><span data-stu-id="a2761-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="a2761-274">Нет необходимости ставить операнд rs-PutRefActiveConnection (cn) в (IDispatch), так как тип операнда уже \> \* есть (IDispatch). \*</span><span class="sxs-lookup"><span data-stu-id="a2761-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="a2761-275">Использование GetItem (x) и Item \[ x\]</span><span class="sxs-lookup"><span data-stu-id="a2761-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="a2761-276">В Visual Basic примере демонстрируется стандартный и альтернативный синтаксис **для Item**().</span><span class="sxs-lookup"><span data-stu-id="a2761-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="a2761-277">В этом примере Visual C++ **демонстрируется Item**.</span><span class="sxs-lookup"><span data-stu-id="a2761-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="a2761-278">Следующая заметка соответствует разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="a2761-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="a2761-279">При доступе к коллекции **с элементом** индекс **2**  должен быть отлит до долгого времени, чтобы был вызван соответствующий конструктор.</span><span class="sxs-lookup"><span data-stu-id="a2761-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="a2761-280">Кастинг указателей объектов ADO с (IDispatch) \*</span><span class="sxs-lookup"><span data-stu-id="a2761-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="a2761-281">В следующем примере Visual C++ показано использование (IDispatch) для \* отбраковки указателей объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="a2761-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="a2761-282">Следующие заметки соответствуют разделам с комментариями в примере кода.</span><span class="sxs-lookup"><span data-stu-id="a2761-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="a2761-283">Укажите объект **open Connection** в явно закодировать **вариант**.</span><span class="sxs-lookup"><span data-stu-id="a2761-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="a2761-284">Отдай его (IDispatch), чтобы был вызван правильный \* конструктор.</span><span class="sxs-lookup"><span data-stu-id="a2761-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="a2761-285">Кроме того, явно задан параметр **\_ \_ t** второго варианта к значению true по **умолчанию,** поэтому количество ссылок на объект будет правильным после окончания операции **Recordset::Open.**</span><span class="sxs-lookup"><span data-stu-id="a2761-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="a2761-286">Выражение (bstr t) — это не литье, а оператор \_ \_  **\_ \_ вариантов t,** который извлекает строку **\_ bstr \_ t** из варианта, возвращенного **значением**.</span><span class="sxs-lookup"><span data-stu-id="a2761-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="a2761-287">Выражение (char) — это не литье, а оператор \* **\_ bstr \_ t,** который извлекает указатель на инкапсулированную строку в **\_ объекте bstr \_ t.**</span><span class="sxs-lookup"><span data-stu-id="a2761-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="a2761-288">В этом разделе кода демонстрируются некоторые полезные действия операторов **\_ \_ вариантов t** и **\_ bstr \_ t.**</span><span class="sxs-lookup"><span data-stu-id="a2761-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

