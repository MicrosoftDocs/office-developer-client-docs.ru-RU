---
title: Программирование для ADO на Visual C++
TOCTitle: Visual C++ ADO Programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55e4bf1476112cc950b72e8bfd1659226704f991
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25890010"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="2e0be-102">Программирование для ADO на Visual C++</span><span class="sxs-lookup"><span data-stu-id="2e0be-102">Visual C++ ADO Programming</span></span>


<span data-ttu-id="2e0be-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e0be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e0be-104">Справочник по API ADO описывается функциональных возможностей ADO программный интерфейс (API) с помощью синтаксис, подобный в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2e0be-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="2e0be-105">То, что Предполагаемая аудитория всех пользователей, ADO с любым опытом использования различных языков, например Visual Basic, Visual C++ (с и без \*\* \#импорта\*\* директива) и Visual J ++ (с пакетом класс ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="2e0be-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="2e0be-106">Чтобы обеспечить этот плотности, [ADO для Visual C++ синтаксис индексов](using-ado-with-microsoft-visual-c.md) предоставляют синтаксис конкретного языка Visual C++ с помощью ссылки на общие описания функциональных возможностей, параметры, исключительных поведения и т. д в справочник по API.</span><span class="sxs-lookup"><span data-stu-id="2e0be-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="2e0be-107">ADO реализуется с помощью интерфейсов COM (объектная модель компонента).</span><span class="sxs-lookup"><span data-stu-id="2e0be-107">ADO is implemented with COM (Component Object Model) interfaces.</span></span> <span data-ttu-id="2e0be-108">Тем не менее проще для программистов для работы с COM на некоторых языках программирования, чем другие.</span><span class="sxs-lookup"><span data-stu-id="2e0be-108">However, it is easier for programmers to work with COM in certain programming languages than others.</span></span> <span data-ttu-id="2e0be-109">Например почти все дополнительные сведения об использовании COM осуществляется неявно для программистов Visual Basic программистов Visual C++ должны принять участие в этих сведений о себе.</span><span class="sxs-lookup"><span data-stu-id="2e0be-109">For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="2e0be-110">В следующих разделах приведены подробные сведения для программистов C и C++ с помощью ADO и \*\* \#импорта\*\* директивы.</span><span class="sxs-lookup"><span data-stu-id="2e0be-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="2e0be-111">В данном документе описываются типы данных, относящимся к COM (**Variant**, **BSTR**и **SafeArray**) и обработка ошибок (\_com\_ошибка).</span><span class="sxs-lookup"><span data-stu-id="2e0be-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="2e0be-112">С помощью \#импорта директива компилятора</span><span class="sxs-lookup"><span data-stu-id="2e0be-112">Using the \#import Compiler Directive</span></span>

<span data-ttu-id="2e0be-113">\*\* \#Импорта\*\* директивы компилятора Visual C++ упрощает работу с ADO методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="2e0be-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="2e0be-114">Директива принимает имя файла, содержащего библиотеку типов, таких как ADO библиотеки DLL (Msado15.dll) и создает файлы заголовков, содержащие объявления typedef, смарт-указатели интерфейсов и перечисляемые константы.</span><span class="sxs-lookup"><span data-stu-id="2e0be-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="2e0be-115">Каждого интерфейса инкапсулированную или заключены в классе.</span><span class="sxs-lookup"><span data-stu-id="2e0be-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="2e0be-116">Для каждой операции в классе (то есть, метод или свойство звонок) отсутствует объявление, чтобы вызвать операцию непосредственно (то есть, «необработанные» форма операции) и объявление, чтобы вызвать операцию необработанные и создавать COM-ошибки, если не удается выполнить операцию для выполнения succ essfully.</span><span class="sxs-lookup"><span data-stu-id="2e0be-116">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully.</span></span> <span data-ttu-id="2e0be-117">Если операция является свойством, есть обычно директива компилятора, который создает альтернативный синтаксис для операции, которая имеет синтаксис, аналогичный Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2e0be-117">If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="2e0be-118">Операции, которые извлекают значение свойства имеют имена формы, \**получения \*\*\* свойство*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="2e0be-119">Операции, задайте значение свойства имеют имена формы, \**поместить \*\*\* свойство*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="2e0be-120">Операции, задайте значение свойства с помощью указателя на объект ADO имеют имена формы, \**PutRef \*\*\* свойство*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="2e0be-121">Можно получить или задать свойство со звонками из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="2e0be-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="2e0be-122">Свойство директивы using</span><span class="sxs-lookup"><span data-stu-id="2e0be-122">Using Property Directives</span></span>

<span data-ttu-id="2e0be-123">\*\* \_ \_Declspec(property...)\*\* директивы компилятора является расширением языка C зависящие от корпорации Майкрософт, которая объявляет функцию, используемую как свойство иметь альтернативный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2e0be-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="2e0be-124">В результате можно задать или получить значения свойства в виде делается в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2e0be-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="2e0be-125">К примеру можно задать и получить свойство таким образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="2e0be-126">Обратите внимание на то, что нет необходимости кода:</span><span class="sxs-lookup"><span data-stu-id="2e0be-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="2e0be-127">Компилятор будет создавать соответствующий \*\*Get \*\**-*, **поместите**-, или \**PutRef \*\*\* свойство* звонок на основе объявлен какие альтернативный синтаксис и ли сейчас свойство чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="2e0be-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="2e0be-128">\*\* \_ \_Declspec(property...)\*\* директивы компилятора можно объявить только **Получение**, **поместить**или **get** и **put** альтернативный синтаксис для функции.</span><span class="sxs-lookup"><span data-stu-id="2e0be-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="2e0be-129">Только для чтения operations иметь только объявление **получения** ; операции только для записи только у объявление **поместить** ; операции, которые являются чтение и запись иметь как **get** и **put** объявлений.</span><span class="sxs-lookup"><span data-stu-id="2e0be-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="2e0be-130">Только два объявления, которые можно получить с этой директивы; Тем не менее, каждое свойство может иметь три функции свойств: \**получения \*\*\* свойство*, \**поместить \*\*\* свойство*, и \**PutRef \*\*\* свойство*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="2e0be-131">В этом случае только две формы свойства имеют альтернативный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2e0be-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="2e0be-132">Например, объект **команды** свойства **ActiveConnection** объявлен с альтернативный синтаксис \**получения \*\*\* ActiveConnection* и \**PutRef \*\*\* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="2e0be-133">**PutRef**- синтаксис является хорошим выбором, поскольку на практике обычно требуется поместить объект **подключения** open (указатель объекта **подключения** ), это свойство.</span><span class="sxs-lookup"><span data-stu-id="2e0be-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="2e0be-134">С другой стороны, имеет объекта **набора записей** **Get**-, **поместите**- и \**PutRef \*\*\* ActiveConnection* операций, но не альтернативный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2e0be-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="2e0be-135">Коллекции, метод GetItem и свойство Item</span><span class="sxs-lookup"><span data-stu-id="2e0be-135">Collections, the GetItem Method, and the Item Property</span></span>

<span data-ttu-id="2e0be-136">ADO определяет несколько семейств сайтов, включая **поля**, **Параметры**, **свойств**и **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-136">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**.</span></span> <span data-ttu-id="2e0be-137">В Visual C++ метод **GetItem (***индекс***)** возвращает элемент коллекции.</span><span class="sxs-lookup"><span data-stu-id="2e0be-137">In Visual C++, the **GetItem(***index***)** method returns a member of the collection.</span></span> <span data-ttu-id="2e0be-138">*Индекс* находится **Variant**, значение которого равно числовой индекс элемента в коллекции или строка, содержащая имя элемента.</span><span class="sxs-lookup"><span data-stu-id="2e0be-138">*Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="2e0be-139">\*\* \_ \_Declspec(property...)\*\* директивы компилятора объявляет свойство **Item** как альтернативный синтаксис для каждого семейства сайтов фундаментальные метод **GetItem() для удаленного элемента** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="2e0be-140">Альтернативный синтаксис использует квадратные скобки и выглядит ссылкой на массив.</span><span class="sxs-lookup"><span data-stu-id="2e0be-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="2e0be-141">В общем случае две формы иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="2e0be-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="2e0be-142">Например присвоить значение поля объекта **набора записей** , с именем ***rs***, полученных из таблицы **авторов** базы данных **pubs** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="2e0be-143">Используйте свойство **Item()** для доступа к третьего **поля** объекта **набора записей** коллекции **полей** (семейств сайтов, индексируются с нуля; возможно, с именем третьего поля ***au\_отображающее общие сведения***).</span><span class="sxs-lookup"><span data-stu-id="2e0be-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="2e0be-144">Затем вызовите метод **Value()** для объекта **поля** для присвоения строкового значения.</span><span class="sxs-lookup"><span data-stu-id="2e0be-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="2e0be-145">Это может быть выражено в Visual Basic следующие четыре способа (последние два формы являются уникальными для Visual Basic, другие языки, которые не имеют эквиваленты):</span><span class="sxs-lookup"><span data-stu-id="2e0be-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="2e0be-146">— Это эквивалент в Visual C++ выше первые две формы:</span><span class="sxs-lookup"><span data-stu-id="2e0be-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="2e0be-147">\-или -(альтернативный синтаксис для свойства **значение** также отображается)</span><span class="sxs-lookup"><span data-stu-id="2e0be-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="2e0be-148">Типы данных COM</span><span class="sxs-lookup"><span data-stu-id="2e0be-148">COM-Specific Data Types</span></span>

<span data-ttu-id="2e0be-149">В общем случае любой тип данных Visual Basic, поиск в справке API ADO имеет эквивалентом Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2e0be-149">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent.</span></span> <span data-ttu-id="2e0be-150">К ним относятся типов стандартных данных, таких как **неподписанные символов** для Visual Basic **Byte**, **короткий** для **целого числа**и **много** **времени**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-150">These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**.</span></span> <span data-ttu-id="2e0be-151">Просмотрите индексов синтаксис, чтобы увидеть именно то, что требуется для операндов данный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="2e0be-151">Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="2e0be-152">Исключения для этого правила — это типы данных, относящиеся к COM: **Variant**, **BSTR**и **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

## <a name="variant"></a><span data-ttu-id="2e0be-153">Variant</span><span class="sxs-lookup"><span data-stu-id="2e0be-153">Variant</span></span>

<span data-ttu-id="2e0be-154">**Variant** — это тип структурированных данных, который содержит элемент значение и член типа данных.</span><span class="sxs-lookup"><span data-stu-id="2e0be-154">A **Variant** is a structured data type that contains a value member and a data type member.</span></span> <span data-ttu-id="2e0be-155">**Variant** может содержать большое число других типов данных, включая другого типа Variant, BSTR, логическое значение, IDispatch или IUnknown указатель, валюты, даты и т. д.</span><span class="sxs-lookup"><span data-stu-id="2e0be-155">A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</span></span> <span data-ttu-id="2e0be-156">COM также предоставляет методы, которые позволяют легко преобразования одного типа данных в другой.</span><span class="sxs-lookup"><span data-stu-id="2e0be-156">COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="2e0be-157">\*\* \_Variant\_t\*\* класс инкапсулирует и управляет тип данных **Variant** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="2e0be-158">Справочник по API ADO сказано, метод или свойство операнд принимает значение, обычно означает значение передается в \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="2e0be-159">Это правило не явным образом значение true, если в разделе **Параметры** в разделах Справочник по API ADO говорит операнд **Variant**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-159">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**.</span></span> <span data-ttu-id="2e0be-160">Одно исключение — при документации явно сказано, что операнд принимает тип стандартных данных, таких как **длинный** или **байтов**или перечисление.</span><span class="sxs-lookup"><span data-stu-id="2e0be-160">One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration.</span></span> <span data-ttu-id="2e0be-161">Операнд принимает **строку**при еще одно исключение.</span><span class="sxs-lookup"><span data-stu-id="2e0be-161">Another exception is when the operand takes a **String**.</span></span>

## <a name="bstr"></a><span data-ttu-id="2e0be-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="2e0be-162">BSTR</span></span>

<span data-ttu-id="2e0be-163">**BSTR** (**B**asic **STR**ing) — это тип структурированных данных, который содержит строку символов и длина строки.</span><span class="sxs-lookup"><span data-stu-id="2e0be-163">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length.</span></span> <span data-ttu-id="2e0be-164">COM предоставляет методы для выделения, работы с и без **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-164">COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="2e0be-165">\*\* \_Bstr\_t\*\* класс инкапсулирует и управляет тип данных **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="2e0be-166">Справочник по API ADO сказано, метод или свойство принимает значение типа **String** , означает значение задается в виде \*\* \_bstr\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

## <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="2e0be-167">Приведение \_variant\_t и \_bstr\_классы t</span><span class="sxs-lookup"><span data-stu-id="2e0be-167">Casting \_variant\_t and \_bstr\_t Classes</span></span>

<span data-ttu-id="2e0be-168">Часто не требуется явно кода \*\* \_variant\_t\*\* или \*\* \_bstr\_t\*\* в аргумент для операции.</span><span class="sxs-lookup"><span data-stu-id="2e0be-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="2e0be-169">Если \*\* \_variant\_t\*\* или \*\* \_bstr\_t\*\* класс содержит конструктор, который соответствует типу данных аргумента, а затем компилятор будет создавать соответствующий \*\* \_variant\_t\*\* или \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="2e0be-170">Тем не менее если аргумент является неоднозначным, то есть, тип данных аргумента соответствует более одного конструктора, необходимо привести аргумент с соответствующий тип данных для вызова конструктора правильное.</span><span class="sxs-lookup"><span data-stu-id="2e0be-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="2e0be-171">Например объявление для метода **Recordset::Open** является:</span><span class="sxs-lookup"><span data-stu-id="2e0be-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="2e0be-172">Аргумент ActiveConnection принимает ссылку на \*\* \_variant\_t\*\*, которой может кода как строка подключения или указатель на открытый объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="2e0be-173">Правильный \*\* \_variant\_t\*\* будут созданы неявно, если передачи строки, например, «уведомления о Доставке = pubs; uid = sa; pwd =;», или указатель, такие как "(IDispatch \*) pConn».</span><span class="sxs-lookup"><span data-stu-id="2e0be-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="2e0be-174">Или может явно кода \*\* \_variant\_t\*\* содержащий указатель, таких как "\_variant\_t ((IDispatch \*) pConn true)».</span><span class="sxs-lookup"><span data-stu-id="2e0be-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="2e0be-175">Приведение (IDispatch \*), разрешает неопределенность с другой конструктор, который принимает указатель на интерфейс IUnknown.</span><span class="sxs-lookup"><span data-stu-id="2e0be-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="2e0be-176">Очень важно, хотя редко упомянутые факт, ADO интерфейс IDispatch.</span><span class="sxs-lookup"><span data-stu-id="2e0be-176">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface.</span></span> <span data-ttu-id="2e0be-177">Каждый раз, когда указатель на объект ADO должен передаваться в качестве **типа Variant**, этот указатель должны быть приведены как указатель на интерфейс IDispatch.</span><span class="sxs-lookup"><span data-stu-id="2e0be-177">Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="2e0be-178">Последний случай явно кодов второй аргумент boolean конструктора с его дополнительный параметр, по умолчанию значение true.</span><span class="sxs-lookup"><span data-stu-id="2e0be-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="2e0be-179">Этот аргумент вызывает конструктор **типа Variant** , чтобы вызвать метод **AddRef**(), который компенсация ADO автоматически вызов \*\* \_variant\_t::Release\*\*() метод при завершении вызова метод или свойство ADO.</span><span class="sxs-lookup"><span data-stu-id="2e0be-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

## <a name="safearray"></a><span data-ttu-id="2e0be-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="2e0be-180">SafeArray</span></span>

<span data-ttu-id="2e0be-181">**SafeArray** — это тип структурированных данных, который содержит массив из других типов данных.</span><span class="sxs-lookup"><span data-stu-id="2e0be-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="2e0be-182">**SafeArray** называется *безопасных* , так как он содержит сведения о границы каждого измерения массива и ограничения доступа к элементам массива в этих границах.</span><span class="sxs-lookup"><span data-stu-id="2e0be-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="2e0be-183">Справочник по API ADO сказано, метод или свойство принимает или возвращает массив, это означает, что метод или свойство принимает или возвращает **SafeArray**, не собственный массив C/C++.</span><span class="sxs-lookup"><span data-stu-id="2e0be-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="2e0be-184">Например второго параметра объект **подключения** **OpenSchema** метод требует массив значений **Variant** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-184">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values.</span></span> <span data-ttu-id="2e0be-185">Эти значения **Variant** передается как элементы **SafeArray**и этого **SafeArray** должно быть задано как значение другого **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-185">Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**.</span></span> <span data-ttu-id="2e0be-186">Это, другие **Variant** , которое передается в качестве аргумента второй **OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-186">It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="2e0be-187">В качестве примеров первый аргумент метода **поиска** является **Variant** , значение которого равно одномерный **массив SafeArray**; Каждый дополнительный первый и второй аргументы **AddNew** является одномерный **массив SafeArray**; а возвращаемое значение метода **получения строк** — **Variant** , значение которого равно двухмерных **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="2e0be-188">Отсутствует и параметры по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e0be-188">Missing and Default Parameters</span></span>

<span data-ttu-id="2e0be-189">Visual Basic позволяет отсутствуют параметры в методах.</span><span class="sxs-lookup"><span data-stu-id="2e0be-189">Visual Basic allows missing parameters in methods.</span></span> <span data-ttu-id="2e0be-190">К примеру метод **Open** объекта **набора записей** имеет пять параметров, но можно пропустить промежуточных параметров и не указывайте конечные параметры.</span><span class="sxs-lookup"><span data-stu-id="2e0be-190">For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters.</span></span> <span data-ttu-id="2e0be-191">В зависимости от типа операнд будет заменен по умолчанию **BSTR** или **Variant** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-191">A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="2e0be-192">В C/C++ необходимо указать все операндов.</span><span class="sxs-lookup"><span data-stu-id="2e0be-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="2e0be-193">Если вы хотите указать отсутствующий параметр типом данных — это строка, укажите \*\* \_bstr\_t\*\* содержащий пустую строку.</span><span class="sxs-lookup"><span data-stu-id="2e0be-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="2e0be-194">Если вы хотите отсутствующий параметр указан тип данных которого является значение **типа Variant**, укажите \*\* \_variant\_t\*\* со значением Отображать\_E\_PARAMNOTFOUND тип VT и\_ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e0be-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="2e0be-195">Кроме того, укажите эквивалент \*\* \_variant\_t\*\* константа, **vtMissing**, которая хранится в телефонном \*\* \#импорта\*\* директивы.</span><span class="sxs-lookup"><span data-stu-id="2e0be-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="2e0be-196">Три метода, исключения для типичного использования **vtMissing**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-196">Three methods are exceptions to the typical use of **vtMissing**.</span></span> <span data-ttu-id="2e0be-197">Это методов **Execute** объектов **подключения** и **команды** и метод **NextRecordset** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-197">These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object.</span></span> <span data-ttu-id="2e0be-198">Ниже приведены их подписей.</span><span class="sxs-lookup"><span data-stu-id="2e0be-198">The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="2e0be-199">Используются параметры, *Параметры*и *RecordsAffected* указатели на **Variant**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-199">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**.</span></span> <span data-ttu-id="2e0be-200">*Параметры* — это входного параметра, который определяет адрес **Variant** один параметр, содержащий или массив параметров, которые будет изменять выполняемой команды.</span><span class="sxs-lookup"><span data-stu-id="2e0be-200">*Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed.</span></span> <span data-ttu-id="2e0be-201">*RecordsAffected* — это выходной параметр, который указывает адрес **Variant**, где возвращается количество строк с помощью метода.</span><span class="sxs-lookup"><span data-stu-id="2e0be-201">*RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="2e0be-202">В объекте **команд** метода **Execute** указывает, что не указаны параметры путем установки *параметров* на любой \&vtMissing (что рекомендуется) или значение null, указатель (то есть, **значение NULL** или нуль (0)).</span><span class="sxs-lookup"><span data-stu-id="2e0be-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="2e0be-203">Если *Параметры* указателя null, метод внутренне заменяет эквивалент **vtMissing**и затем завершает операцию.</span><span class="sxs-lookup"><span data-stu-id="2e0be-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="2e0be-204">Все методы указывает, что количество записей не должны возвращаться путем установки для параметра *RecordsAffected* указатель null.</span><span class="sxs-lookup"><span data-stu-id="2e0be-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="2e0be-205">В этом случае указатель null не так отсутствующий параметр как это свидетельствует о том, что метод необходимо отменить количество записей.</span><span class="sxs-lookup"><span data-stu-id="2e0be-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="2e0be-206">Таким образом для этих трех методов является допустимым написать код таких как:</span><span class="sxs-lookup"><span data-stu-id="2e0be-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="2e0be-207">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="2e0be-207">Error Handling</span></span>

<span data-ttu-id="2e0be-208">В модели COM большинство операций возврата HRESULT кода возврата, которое указывает, будет ли функция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="2e0be-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="2e0be-209">\*\* \#Импорта\*\* директива создает код программы-оболочки вокруг каждого «необработанные» метод или свойство и проверяет возвращаемое значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2e0be-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="2e0be-210">Если значение HRESULT указывает на ошибку, кода программы-оболочки для вызывает ошибку COM путем вызова \_com\_проблему\_errorex() со значением HRESULT возвращают код в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="2e0be-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="2e0be-211">Ошибка COM-объектов может быть зафиксировано в **Попробуйте**-блок**catch** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="2e0be-212">(Ради повышения эффективности перехватывающей ссылку на \*\* \_com\_ошибка\*\* объект.)</span><span class="sxs-lookup"><span data-stu-id="2e0be-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="2e0be-213">Помните, что это ADO ошибки: они являются результатом сбоя операции ADO.</span><span class="sxs-lookup"><span data-stu-id="2e0be-213">Remember, these are ADO errors: they result from the ADO operation failing.</span></span> <span data-ttu-id="2e0be-214">Ошибок, возвращаемых основного поставщика отображаются в виде объектов **ошибок** в объект **подключения** семейства **Errors** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-214">Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="2e0be-215">\*\* \#Импорта\*\* директива создает только ошибки процедур обработки для методов и свойств, объявленных в ADO DLL-файл.</span><span class="sxs-lookup"><span data-stu-id="2e0be-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="2e0be-216">Тем не менее вы можете воспользоваться преимуществами эта же ошибка механизм обработки, создав собственный макрос или встроенной функции проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="2e0be-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="2e0be-217">Просмотрите раздел, [Расширений Visual C++](visual-c-extensions-for-ado.md)или код в следующих разделах приведены примеры.</span><span class="sxs-lookup"><span data-stu-id="2e0be-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="2e0be-218">Соглашения по Visual Basic, эквивалентные Visual C++</span><span class="sxs-lookup"><span data-stu-id="2e0be-218">Visual C++ Equivalents of Visual Basic Conventions</span></span>

<span data-ttu-id="2e0be-219">Ниже приводится сводка по несколько условные обозначения в документации по ADO, закодированный в Visual Basic, а также их эквивалентами в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2e0be-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

## <a name="declaring-an-ado-object"></a><span data-ttu-id="2e0be-220">Объявление объекта ADO</span><span class="sxs-lookup"><span data-stu-id="2e0be-220">Declaring an ADO Object</span></span>

<span data-ttu-id="2e0be-221">В Visual Basic ADO объектной переменной (в данном случае для объекта **набора записей** ) объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="2e0be-222">Предложение «ADODB. Записей» — это программный идентификатор объекта **набора записей** , как определено в реестре.</span><span class="sxs-lookup"><span data-stu-id="2e0be-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="2e0be-223">Новый экземпляр объекта **записи** объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="2e0be-224">\-или -</span><span class="sxs-lookup"><span data-stu-id="2e0be-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="2e0be-225">В Visual C++ \*\* \#импорта\*\* директива создает смарт-тип указателя объявления для всех объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="2e0be-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="2e0be-226">Например, переменную, которая указывает на \*\* \_записей\*\* — это объект типа \*\* \_RecordsetPtr\*\*и объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="2e0be-227">Переменная, указывающий на новый экземпляр объекта \*\* \_записей\*\* объект объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="2e0be-228">\-или -</span><span class="sxs-lookup"><span data-stu-id="2e0be-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="2e0be-229">\-или -</span><span class="sxs-lookup"><span data-stu-id="2e0be-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="2e0be-230">После вызова метода **CreateInstance** переменной можно использовать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="2e0be-231">Обратите внимание, что в одном случае «.» используется оператор, как если бы переменная экземпляра класса (rs. CreateInstance) и в другом случае «-\>"оператор используется, как если бы переменная указатель на интерфейс (rs -\>Open).</span><span class="sxs-lookup"><span data-stu-id="2e0be-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="2e0be-232">По одной переменной можно использовать двумя способами, так как «-\>"оператор перегрузить чтобы экземпляр класса для обрабатываются как указатель на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2e0be-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="2e0be-233">Закрытый класс элемент переменной экземпляра содержит указатель на \*\* \_записей\*\* интерфейса; «-\>"оператор возвращает этот указатель; и возвращенный указатель обращается к членов \*\* \_записей\*\* объекта.</span><span class="sxs-lookup"><span data-stu-id="2e0be-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

## <a name="coding-a-missing-parameter"></a><span data-ttu-id="2e0be-234">Создание кода отсутствующий параметр</span><span class="sxs-lookup"><span data-stu-id="2e0be-234">Coding a Missing Parameter</span></span>

<span data-ttu-id="2e0be-235">При необходимости кода операнд **строки** в Visual Basic, просто опустить операнд.</span><span class="sxs-lookup"><span data-stu-id="2e0be-235">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="2e0be-236">Необходимо указать операнд в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2e0be-236">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="2e0be-237">Код \*\* \_bstr\_t\*\* , которая имеет пустую строку как значение.</span><span class="sxs-lookup"><span data-stu-id="2e0be-237">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

## <a name="coding-a-missing-parameter"></a><span data-ttu-id="2e0be-238">Создание кода отсутствующий параметр</span><span class="sxs-lookup"><span data-stu-id="2e0be-238">Coding a Missing Parameter</span></span>

<span data-ttu-id="2e0be-239">При необходимости кода операнд **Variant** в Visual Basic, просто опустить операнд.</span><span class="sxs-lookup"><span data-stu-id="2e0be-239">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="2e0be-240">Необходимо указать все операнды в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2e0be-240">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="2e0be-241">Код отсутствующий параметр **типа Variant** с \*\* \_variant\_t\*\* специальные значение Отображать\_E\_PARAMNOTFOUND и тип, VT\_ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e0be-241">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="2e0be-242">Кроме того, укажите **vtMissing**, который является эквивалент предопределенные константы в телефонном \*\* \#импорта\*\* директивы.</span><span class="sxs-lookup"><span data-stu-id="2e0be-242">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="2e0be-243">\-или воспользуйтесь-</span><span class="sxs-lookup"><span data-stu-id="2e0be-243">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

## <a name="declaring-a-variant"></a><span data-ttu-id="2e0be-244">Объявление типа Variant</span><span class="sxs-lookup"><span data-stu-id="2e0be-244">Declaring a Variant</span></span>

<span data-ttu-id="2e0be-245">В Visual Basic **Variant** объявлен с помощью оператора **Dim** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-245">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="2e0be-246">В Visual C++ объявлении переменной в качестве типа \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-246">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="2e0be-247">Несколько схема \*\* \_variant\_t\*\* ниже показаны объявления.</span><span class="sxs-lookup"><span data-stu-id="2e0be-247">A few schematic **\_variant\_t** declarations are shown below.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2e0be-248">Эти объявления просто присвойте приблизительное представление об бы кода в собственную программу.</span><span class="sxs-lookup"><span data-stu-id="2e0be-248">These declarations merely give a rough idea of what you would code in your own program.</span></span> <span data-ttu-id="2e0be-249">Для получения дополнительных сведений см. в приведенных ниже примерах и документации по Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2e0be-249">For more information, see the examples below, and the Visual C++ documentation.</span></span></P>



```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

## <a name="using-arrays-of-variants"></a><span data-ttu-id="2e0be-250">Использование массивов вариантов</span><span class="sxs-lookup"><span data-stu-id="2e0be-250">Using Arrays of Variants</span></span>

<span data-ttu-id="2e0be-251">В Visual Basic массивов **вариантов** можно закодировать с помощью оператора **Dim** , или можно использовать функцию **массива** , как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="2e0be-251">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

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

<span data-ttu-id="2e0be-252">В следующем примере Visual C++ демонстрируется использование **SafeArray** используется с \*\* \_variant\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-252">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2e0be-253">Следующие замечания соответствуют закомментированного разделов в примере кода.</span><span class="sxs-lookup"><span data-stu-id="2e0be-253">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="2e0be-254">Еще раз чтобы воспользоваться преимуществами существующего механизм обработки ошибок определяется встроенная функция TESTHR().</span><span class="sxs-lookup"><span data-stu-id="2e0be-254">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2.  <span data-ttu-id="2e0be-255">Одномерный массив, требуется только в том случае, поэтому **SafeArrayCreateVector**, можно использовать вместо объявления **SAFEARRAYBOUND** общего назначения и функции **SafeArrayCreate** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-255">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function.</span></span> <span data-ttu-id="2e0be-256">Ниже приведен код будет выглядеть как с помощью **SafeArrayCreate**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-256">The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
    ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
    ```

3.  <span data-ttu-id="2e0be-257">Схемы, определяемую средством константа перечисления **adSchemaColumns**связан с четыре столбца ограничение: таблица\_КАТАЛОГА, в ТАБЛИЦЕ\_СХЕМЫ, таблица\_имя и столбец\_имя.</span><span class="sxs-lookup"><span data-stu-id="2e0be-257">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="2e0be-258">Таким образом создается массив значений **Variant** с четырьмя элементами.</span><span class="sxs-lookup"><span data-stu-id="2e0be-258">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="2e0be-259">Выберите ограничение по значению, соответствующий третьего столбца в ТАБЛИЦЕ\_имя, указано.</span><span class="sxs-lookup"><span data-stu-id="2e0be-259">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="2e0be-260">**Набор записей** , который возвращается состоит из нескольких столбцов, подмножество из которых представляет столбцы ограничений.</span><span class="sxs-lookup"><span data-stu-id="2e0be-260">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="2e0be-261">Значения столбцов ограничения для каждой строки набора должно совпадать с соответствующие значения ограничения.</span><span class="sxs-lookup"><span data-stu-id="2e0be-261">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4.  <span data-ttu-id="2e0be-262">Те, которые знакомы с **объекты SAFEARRAY** может получать уведомления, что ( **SafeArrayDestroy**) не вызывается до завершения.</span><span class="sxs-lookup"><span data-stu-id="2e0be-262">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="2e0be-263">На самом деле вызов ( **SafeArrayDestroy**) в этом случае вызовет исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2e0be-263">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="2e0be-264">Причина в том, что деструктор vtCriteria выполняется звонок ( **VariantClear**) при \*\* \_variant\_t\*\* выходит за область, в которой будет освободить **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-264">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="2e0be-265">Вызов **SafeArrayDestroy**без вручную очистка \*\* \_variant\_t\*\*, вызовет деструктор для снимите недопустимый указатель **SafeArray** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-265">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="2e0be-266">Если вызов **SafeArrayDestroy** , код будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2e0be-266">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
    ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
    ```
    
    <span data-ttu-id="2e0be-267">Тем не менее, гораздо проще let \*\* \_variant\_t\*\* управление **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-267">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>

<!-- end list -->

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

## <a name="using-property-getputputref"></a><span data-ttu-id="2e0be-268">С помощью свойства Get и Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="2e0be-268">Using Property Get/Put/PutRef</span></span>

<span data-ttu-id="2e0be-269">В Visual Basic имя свойства не дополняется ли его получить, назначенных или назначенных ссылку.</span><span class="sxs-lookup"><span data-stu-id="2e0be-269">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

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

<span data-ttu-id="2e0be-270">В этом примере Visual C++ демонстрируется **Начало**/**поместить**/\**PutRef \*\*\* свойство*.</span><span class="sxs-lookup"><span data-stu-id="2e0be-270">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2e0be-271">Следующие замечания соответствуют закомментированного разделов в примере кода.</span><span class="sxs-lookup"><span data-stu-id="2e0be-271">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="2e0be-272">В этом примере используется два вида отсутствует строковый аргумент: явные константа, **strMissing**и строку, компилятор будет использовать для создания временного \*\* \_bstr\_t\*\* , которая будет присутствовать для области метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-272">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2.  <span data-ttu-id="2e0be-273">Нет необходимости привести операнд rs -\>PutRefActiveConnection(cn) для (IDispatch \*), так как тип операнда уже (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="2e0be-273">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
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

## <a name="using-getitemx-and-itemx"></a><span data-ttu-id="2e0be-274">С помощью GetItem(x) и элемента\[x\]</span><span class="sxs-lookup"><span data-stu-id="2e0be-274">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="2e0be-275">В этом примере Visual Basic демонстрируется стандартный и альтернативный синтаксис ( **элемент**).</span><span class="sxs-lookup"><span data-stu-id="2e0be-275">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

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

<span data-ttu-id="2e0be-276">В этом примере Visual C++ **элемента**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-276">This Visual C++ example demonstrates **Item**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2e0be-277">Следующее примечание соответствует комментариев для разделов в примере кода.</span><span class="sxs-lookup"><span data-stu-id="2e0be-277">The following note corresponds to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="2e0be-278">При доступе к коллекции с помощью **элемента**, индекса, **2**, необходимо привести к **времени** , вызывается соответствующий конструктор.</span><span class="sxs-lookup"><span data-stu-id="2e0be-278">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
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

## <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="2e0be-279">Приведение указатели объект ADO с (IDispatch \*)</span><span class="sxs-lookup"><span data-stu-id="2e0be-279">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="2e0be-280">В следующем примере Visual C++ демонстрируется использование (IDispatch \*) для приведения указателей объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="2e0be-280">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2e0be-281">Следующие замечания соответствуют закомментированного разделов в примере кода.</span><span class="sxs-lookup"><span data-stu-id="2e0be-281">The following notes correspond to commented sections in the code example.</span></span></P>



1.  <span data-ttu-id="2e0be-282">Укажите open объекта **подключения** в явным образом закодированный **Variant**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-282">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="2e0be-283">Привести его с (IDispatch \*), будет вызываться надлежащий конструктор.</span><span class="sxs-lookup"><span data-stu-id="2e0be-283">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="2e0be-284">Также, необходимо явно задать второй \*\* \_variant\_t\*\* параметр со значением по умолчанию **значение true**, поэтому счетчик ссылок объекта будет правильный после завершения операции **Recordset::Open** .</span><span class="sxs-lookup"><span data-stu-id="2e0be-284">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2.  <span data-ttu-id="2e0be-285">Выражение (\_bstr\_t), не является приведения, но \*\* \_variant\_t\*\* оператор, который извлекает \*\* \_bstr\_t\*\* строку из **типа Variant** , возвращенное **значение**.</span><span class="sxs-lookup"><span data-stu-id="2e0be-285">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="2e0be-286">Выражение (символ\*), не является приведения, но \*\* \_bstr\_t\*\* оператор, который извлекает указатель инкапсулированное строку в \*\* \_bstr\_t\*\* объекта.</span><span class="sxs-lookup"><span data-stu-id="2e0be-286">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="2e0be-287">В этом разделе кода показаны некоторые полезные поведения \*\* \_variant\_t\*\* и \*\* \_bstr\_t\*\* операторы.</span><span class="sxs-lookup"><span data-stu-id="2e0be-287">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
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

