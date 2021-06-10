---
title: Использование расширений Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312063"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="81618-102">Использование расширений Visual C++</span><span class="sxs-lookup"><span data-stu-id="81618-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="81618-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81618-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="81618-104">Интерфейс IADORecordBinding</span><span class="sxs-lookup"><span data-stu-id="81618-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="81618-105">Поля Microsoft Visual C++ для партнеров ADO или привязки полей объекта [Recordset](recordset-object-ado.md) к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-105">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="81618-106">Всякий раз, когда меняется текущая строка связанного **recordset,** все связанные поля в **Наборе** записей копируется в переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-106">Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables.</span></span> <span data-ttu-id="81618-107">При необходимости копируемые данные преобразуются в объявленный тип данных переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-107">If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="81618-108">Метод **BindToRecordset** **интерфейса IADORecordBinding** связывает поля с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-108">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables.</span></span> <span data-ttu-id="81618-109">Метод **AddNew добавляет** новую строку в связанный **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="81618-109">The **AddNew** method adds a new row to the bound **Recordset**.</span></span> <span data-ttu-id="81618-110">Метод **Update** заполняет поля в новых строках **Recordset** или обновляет поля в существующих строках со значением переменных C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-110">The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="81618-111">Интерфейс **IADORecordBinding** реализуется объектом **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="81618-111">The **IADORecordBinding** interface is implemented by the **Recordset** object.</span></span> <span data-ttu-id="81618-112">Вы не кодировать реализацию самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="81618-112">You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="81618-113">Привязка записей</span><span class="sxs-lookup"><span data-stu-id="81618-113">Binding Entries</span></span>

<span data-ttu-id="81618-114">Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span><span class="sxs-lookup"><span data-stu-id="81618-114">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="81618-115">Определение сопоставления между полем и переменной называется *привязкой.*</span><span class="sxs-lookup"><span data-stu-id="81618-115">The definition of a mapping between a field and a variable is called a *binding entry*.</span></span> <span data-ttu-id="81618-116">Макрос обеспечивает привязку записей для числовой, фиксированной длины и переменной длины данных.</span><span class="sxs-lookup"><span data-stu-id="81618-116">Macros provide binding entries for numeric, fixed-length, and variable-length data.</span></span> <span data-ttu-id="81618-117">Записи привязки и переменные C/C++ объявляются в классе, полученном из класса Visual C++ Extensions, **CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="81618-117">The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**.</span></span> <span data-ttu-id="81618-118">Класс **CADORecordBinding** определяется внутренними макросами записи привязки.</span><span class="sxs-lookup"><span data-stu-id="81618-118">The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="81618-119">Внутренний объект ADO создает параметры в этих макросах в структуру **DBBINDING** OLE DB и создает объект OLE DB **Accessor** для управления перемещением и преобразованием данных между полями и переменными.</span><span class="sxs-lookup"><span data-stu-id="81618-119">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables.</span></span> <span data-ttu-id="81618-120">OLE DB определяет данные как состоящие  из трех частей: буфера, в котором хранятся данные; *состояние,* которое указывает, было ли поле успешно сохранено в буфере или как переменная должна быть восстановлена в поле; и *длина* данных.</span><span class="sxs-lookup"><span data-stu-id="81618-120">OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data.</span></span> <span data-ttu-id="81618-121">(См. справку *программиста OLE DB,* главу 6: получение и настройку данных для получения дополнительных сведений.)</span><span class="sxs-lookup"><span data-stu-id="81618-121">(See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="81618-122">Файл загона</span><span class="sxs-lookup"><span data-stu-id="81618-122">Header File</span></span>

<span data-ttu-id="81618-123">Включите в приложение следующий файл, чтобы использовать расширения Visual C++ для ADO:</span><span class="sxs-lookup"><span data-stu-id="81618-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="81618-124">Поля привязки recordset</span><span class="sxs-lookup"><span data-stu-id="81618-124">Binding Recordset Fields</span></span>

<span data-ttu-id="81618-125">**Привязка полей recordset к переменным C/C++**</span><span class="sxs-lookup"><span data-stu-id="81618-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="81618-126">Создание класса, полученного из **класса CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="81618-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="81618-127">Укажите обязательные записи и соответствующие переменные C/C++ в полученном классе.</span><span class="sxs-lookup"><span data-stu-id="81618-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="81618-128">Скобка привязки записей **между BEGIN \_ ADO \_ BINDING** и **END \_ ADO \_ BINDING** макрос.</span><span class="sxs-lookup"><span data-stu-id="81618-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="81618-129">Не прекращать макрос запятой или запятой.</span><span class="sxs-lookup"><span data-stu-id="81618-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="81618-130">Соответствующие делимитеры автоматически заданы каждым макросом.</span><span class="sxs-lookup"><span data-stu-id="81618-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="81618-131">Укажите одну привязку для каждого поля, который будет соеди-ться с переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="81618-132">Используйте соответствующий член из семейства макрос **ADO \_ FIXED LENGTH \_ \_ ENTRY,** **ADO \_ NUMERIC \_ ENTRY** или **ADO VARIABLE LENGTH \_ \_ \_ ENTRY.**</span><span class="sxs-lookup"><span data-stu-id="81618-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="81618-133">В приложении создайте экземпляр класса, полученный из **CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="81618-133">In your application, create an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="81618-134">Получите **интерфейс IADORecordBinding** из **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="81618-134">Get the **IADORecordBinding** interface from the **Recordset**.</span></span> <span data-ttu-id="81618-135">Затем позвоните **методу BindToRecordset,** чтобы привязать поля **Recordset** к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-135">Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="81618-136">Дополнительные сведения см. в примере Visual [C++ Extensions.](visual-c-extensions-example.md)</span><span class="sxs-lookup"><span data-stu-id="81618-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="81618-137">Методы интерфейса</span><span class="sxs-lookup"><span data-stu-id="81618-137">Interface Methods</span></span>

<span data-ttu-id="81618-138">Интерфейс **IADORecordBinding имеет** три метода: **BindToRecordset,** **AddNew** и **Update.**</span><span class="sxs-lookup"><span data-stu-id="81618-138">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**.</span></span> <span data-ttu-id="81618-139">Единственным аргументом для каждого метода является указатель экземпляра класса, полученного из **CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="81618-139">The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="81618-140">Поэтому методы **AddNew** и **Update** не могут указывать ни один из параметров тезки метода ADO.</span><span class="sxs-lookup"><span data-stu-id="81618-140">Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="81618-141">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="81618-141">**Syntax**</span></span>

<span data-ttu-id="81618-142">Метод **BindToRecordset связывает** поля **Recordset** с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="81618-143">Метод **AddNew вызывает** своего тезку, метод ADO [AddNew,](addnew-method-ado.md) чтобы добавить новую строку в **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="81618-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="81618-144">Метод **Update** вызывает своего тезку, метод ADO [Update,](update-method-ado.md) для обновления **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="81618-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="81618-145">Привязка Макрос входа</span><span class="sxs-lookup"><span data-stu-id="81618-145">Binding Entry Macros</span></span>

<span data-ttu-id="81618-146">Макрос привязки для записи определяет связь поля **Recordset** и переменной.</span><span class="sxs-lookup"><span data-stu-id="81618-146">Binding entry macros define the association of a **Recordset** field and a variable.</span></span> <span data-ttu-id="81618-147">Начало и окончание макроса делимитовывает набор обязательных записей.</span><span class="sxs-lookup"><span data-stu-id="81618-147">A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="81618-148">Семьи макрос предоставляются для данных фиксированной длины, таких как **adDate** или **adBoolean;** числовая информация, например **adTinyInt,** **adInteger** или **adDouble;** и данные переменной длины, такие как **adChar,** **adVarChar** или **adVarBinary.**</span><span class="sxs-lookup"><span data-stu-id="81618-148">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**.</span></span> <span data-ttu-id="81618-149">Все числимые типы, за исключением **adVarNumeric,** также являются типами фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="81618-149">All numeric types, except for **adVarNumeric**, are also fixed-length types.</span></span> <span data-ttu-id="81618-150">Каждая семья имеет различные наборы параметров, чтобы исключить связывающие сведения, которые не являются интересующими.</span><span class="sxs-lookup"><span data-stu-id="81618-150">Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="81618-151">Дополнительные сведения см. в справке программиста *OLE DB,* приложении A: Типы данных.</span><span class="sxs-lookup"><span data-stu-id="81618-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="81618-152">_**Начало обязательных записей**_</span><span class="sxs-lookup"><span data-stu-id="81618-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="81618-153">\**BEGIN \_ ПРИВЯЗКА \_ ADO\*\*\*(Класс)*</span><span class="sxs-lookup"><span data-stu-id="81618-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="81618-154">_**Данные фиксированной длины**_</span><span class="sxs-lookup"><span data-stu-id="81618-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="81618-155">\**ADO \_ ЗАПИСЬ \_ \_ ФИКСИРОВАННОЙ ДЛИНЫ\*\*\*(Ordinal, DataType, Buffer, Status, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="81618-156">\**ADO \_ FIXED \_ LENGTH \_ ENTRY2\*\*\*(Ordinal, DataType, Buffer, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="81618-157">_**Числовая информация**_</span><span class="sxs-lookup"><span data-stu-id="81618-157">_**Numeric Data**_</span></span>

<span data-ttu-id="81618-158">\**ADO \_ NUMERIC \_ ENTRY\*\*\*(Ordinal, DataType, Buffer, Precision, Scale, Status, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="81618-159">\**ADO \_ NUMERIC \_ ENTRY2\*\*\*(Ordinal, DataType, Buffer, Precision, Scale, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="81618-160">_**Данные переменной длины**_</span><span class="sxs-lookup"><span data-stu-id="81618-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="81618-161">\**ADO \_ ЗАПИСЬ \_ VARIABLE \_ LENGTH\*\*\*(Ordinal, DataType, Buffer, Size, Status, Length, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="81618-162">\**ADO \_ VARIABLE \_ LENGTH \_ ENTRY2\*\*\*(Ordinal, DataType, Buffer, Size, Status, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="81618-163">\**ADO \_ VARIABLE \_ LENGTH \_ ENTRY3\*\*\*(Ordinal, DataType, Buffer, Size, Length, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="81618-164">\**ADO \_ VARIABLE \_ LENGTH \_ ENTRY4\*\*\*(Ordinal, DataType, Buffer, Size, Modify)*</span><span class="sxs-lookup"><span data-stu-id="81618-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="81618-165">_**Конечные записи привязки**_</span><span class="sxs-lookup"><span data-stu-id="81618-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="81618-166">**END \_ ПРИВЯЗКА \_ ADO**()</span><span class="sxs-lookup"><span data-stu-id="81618-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81618-167">Параметр</span><span class="sxs-lookup"><span data-stu-id="81618-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="81618-168">Описание</span><span class="sxs-lookup"><span data-stu-id="81618-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81618-169"><em>Class</em></span><span class="sxs-lookup"><span data-stu-id="81618-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="81618-170">Класс, в котором определяются записи привязки и переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="81618-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="81618-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="81618-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span><span class="sxs-lookup"><span data-stu-id="81618-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="81618-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="81618-174">Эквивалентный тип данных ADO переменной C/C++ (см. <a href="datatypeenum.md">dataTypeEnum</a> для списка допустимых типов данных).</span><span class="sxs-lookup"><span data-stu-id="81618-174">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types).</span></span> <span data-ttu-id="81618-175">При необходимости значение поля <strong>Recordset</strong> будет преобразовано в этот тип данных.</span><span class="sxs-lookup"><span data-stu-id="81618-175">The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-176"><em>Буфер</em></span><span class="sxs-lookup"><span data-stu-id="81618-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="81618-177">Имя переменной C/C++, в которой будет храниться поле <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="81618-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-178"><em>Размер</em></span><span class="sxs-lookup"><span data-stu-id="81618-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="81618-179">Максимальный размер в bytes of <em>Buffer</em>.</span><span class="sxs-lookup"><span data-stu-id="81618-179">Maximum size in bytes of <em>Buffer</em>.</span></span> <span data-ttu-id="81618-180">Если <em>буфер</em> будет содержать строку переменной длины, упустим место для завершаемого нуля.</span><span class="sxs-lookup"><span data-stu-id="81618-180">If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-181"><em>Состояние</em></span><span class="sxs-lookup"><span data-stu-id="81618-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="81618-182">Имя переменной, которая будет указывать, допустимо ли содержимое <em>буфера</em> и успешно ли было преобразование поля <em>в DataType.</em></span><span class="sxs-lookup"><span data-stu-id="81618-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="81618-183">Двумя наиболее важными значениями для этой переменной являются <strong>adFldOK,</strong>что означает успешное преобразование; <strong>и adFldNull</strong>, что означает, что значение поля будет ВАРИАНТ типа VT_NULL а не просто пустой.</span><span class="sxs-lookup"><span data-stu-id="81618-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="81618-184">Возможные значения <em>состояния</em> перечислены в следующей таблице &quot; , Значения состояния.&quot;</span><span class="sxs-lookup"><span data-stu-id="81618-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-185"><em>Modify</em></span><span class="sxs-lookup"><span data-stu-id="81618-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="81618-186">флаг Boolean; если ЗНАЧЕНИЕ TRUE указывает, что ADO разрешено обновлять соответствующее поле <strong>Recordset</strong> со значением, содержащеся в <em>буфере.</em></span><span class="sxs-lookup"><span data-stu-id="81618-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="81618-187">Установите параметр Изменения <em></em> Boolean в TRUE, чтобы включить ADO для обновления связанного поля и FALSE, если вы хотите изучить поле, но не изменить его.</span><span class="sxs-lookup"><span data-stu-id="81618-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-188"><em>Точность</em></span><span class="sxs-lookup"><span data-stu-id="81618-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="81618-189">Количество цифр, которые могут быть представлены в числовом переменном.</span><span class="sxs-lookup"><span data-stu-id="81618-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-190"><em>Scale</em></span><span class="sxs-lookup"><span data-stu-id="81618-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="81618-191">Количество десятичных мест в числовом переменной.</span><span class="sxs-lookup"><span data-stu-id="81618-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="81618-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="81618-193">Имя переменной из четырех byte, которая будет содержать фактическую длину данных в <em>буфере.</em></span><span class="sxs-lookup"><span data-stu-id="81618-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="81618-194">Значения состояния</span><span class="sxs-lookup"><span data-stu-id="81618-194">Status Values</span></span>

<span data-ttu-id="81618-195">Значение переменной *Status* указывает, было ли поле успешно скопировано на переменную.</span><span class="sxs-lookup"><span data-stu-id="81618-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="81618-196">При настройке данных *состояние* может быть назначено **adFldNull,** чтобы указать, что поле **Recordset** должно быть настроено на null.</span><span class="sxs-lookup"><span data-stu-id="81618-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81618-197">Константа</span><span class="sxs-lookup"><span data-stu-id="81618-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="81618-198">Значение</span><span class="sxs-lookup"><span data-stu-id="81618-198">Value</span></span></p></th>
<th><p><span data-ttu-id="81618-199">Описание</span><span class="sxs-lookup"><span data-stu-id="81618-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81618-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="81618-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-201">0</span><span class="sxs-lookup"><span data-stu-id="81618-201">0</span></span></p></td>
<td><p><span data-ttu-id="81618-202">Было возвращено значение поля non-null.</span><span class="sxs-lookup"><span data-stu-id="81618-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="81618-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-204">1</span><span class="sxs-lookup"><span data-stu-id="81618-204">1</span></span></p></td>
<td><p><span data-ttu-id="81618-205">Привязка была недействительной.</span><span class="sxs-lookup"><span data-stu-id="81618-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="81618-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-207">2</span><span class="sxs-lookup"><span data-stu-id="81618-207">2</span></span></p></td>
<td><p><span data-ttu-id="81618-208">Значение не может быть преобразовано по другим причинам, кроме несоответствия знака или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="81618-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="81618-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-210">3</span><span class="sxs-lookup"><span data-stu-id="81618-210">3</span></span></p></td>
<td><p><span data-ttu-id="81618-211">При получении поля указывается, что было возвращено значение null.</span><span class="sxs-lookup"><span data-stu-id="81618-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="81618-212">При настройке поля указывается, что поле должно быть настроено на <strong>NULL,</strong> если поле не может кодировать <strong>сам NULL</strong> (например, массив символов или целый ряд).</span><span class="sxs-lookup"><span data-stu-id="81618-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="81618-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-214">4 </span><span class="sxs-lookup"><span data-stu-id="81618-214">4</span></span></p></td>
<td><p><span data-ttu-id="81618-215">Данные переменной длины или численные цифры были усечены.</span><span class="sxs-lookup"><span data-stu-id="81618-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="81618-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-217">5 </span><span class="sxs-lookup"><span data-stu-id="81618-217">5</span></span></p></td>
<td><p><span data-ttu-id="81618-218">Значение подписывало, а тип переменных данных не подписывался.</span><span class="sxs-lookup"><span data-stu-id="81618-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="81618-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-220">6 </span><span class="sxs-lookup"><span data-stu-id="81618-220">6</span></span></p></td>
<td><p><span data-ttu-id="81618-221">Значение больше, чем может храниться в переменном типе данных.</span><span class="sxs-lookup"><span data-stu-id="81618-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="81618-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-223">7 </span><span class="sxs-lookup"><span data-stu-id="81618-223">7</span></span></p></td>
<td><p><span data-ttu-id="81618-224">Неизвестный тип столбца и поле уже открыты.</span><span class="sxs-lookup"><span data-stu-id="81618-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="81618-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-226">8 </span><span class="sxs-lookup"><span data-stu-id="81618-226">8</span></span></p></td>
<td><p><span data-ttu-id="81618-227">Значение поля не удалось определить — например, в новом, не назначенном поле без значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81618-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="81618-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-229">9 </span><span class="sxs-lookup"><span data-stu-id="81618-229">9</span></span></p></td>
<td><p><span data-ttu-id="81618-230">При обновлении нет разрешения на написание данных.</span><span class="sxs-lookup"><span data-stu-id="81618-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="81618-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-232">10 </span><span class="sxs-lookup"><span data-stu-id="81618-232">10</span></span></p></td>
<td><p><span data-ttu-id="81618-233">При обновлении значение поля нарушает целостность столбцов.</span><span class="sxs-lookup"><span data-stu-id="81618-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="81618-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-235">11</span><span class="sxs-lookup"><span data-stu-id="81618-235">11</span></span></p></td>
<td><p><span data-ttu-id="81618-236">При обновлении значение поля нарушает схему столбца.</span><span class="sxs-lookup"><span data-stu-id="81618-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81618-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="81618-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-238">12 </span><span class="sxs-lookup"><span data-stu-id="81618-238">12</span></span></p></td>
<td><p><span data-ttu-id="81618-239">При обновлении недействительный параметр состояния.</span><span class="sxs-lookup"><span data-stu-id="81618-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81618-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="81618-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="81618-241">13</span><span class="sxs-lookup"><span data-stu-id="81618-241">13</span></span></p></td>
<td><p><span data-ttu-id="81618-242">При обновлении использовалось значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81618-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

