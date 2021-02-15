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
# <a name="using-visual-c-extensions"></a><span data-ttu-id="f546c-102">Использование расширений Visual C++</span><span class="sxs-lookup"><span data-stu-id="f546c-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="f546c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f546c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="f546c-104">Интерфейс IADORecordBinding</span><span class="sxs-lookup"><span data-stu-id="f546c-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="f546c-105">Расширения Microsoft Visual C++ для ADO связывают поля объекта [Recordset](recordset-object-ado.md) с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-105">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="f546c-106">При внесении изменений в текущую строку привязанного наборов **записей** все связанные поля в наборе **записей** копируется в переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-106">Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables.</span></span> <span data-ttu-id="f546c-107">При необходимости скопированные данные преобразуются в объявленный тип данных переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-107">If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="f546c-108">Метод **BindToRecordset** интерфейса **IADORecordBinding** привязывает поля к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-108">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables.</span></span> <span data-ttu-id="f546c-109">Метод **AddNew** добавляет новую строку в привязанный **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="f546c-109">The **AddNew** method adds a new row to the bound **Recordset**.</span></span> <span data-ttu-id="f546c-110">Метод **Update** заполняет поля в новых строках наборов **записей** или обновляет поля в существующих строках значением переменных C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-110">The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="f546c-111">Интерфейс **IADORecordBinding** реализуется **объектом Recordset.**</span><span class="sxs-lookup"><span data-stu-id="f546c-111">The **IADORecordBinding** interface is implemented by the **Recordset** object.</span></span> <span data-ttu-id="f546c-112">Вы не кодировать реализацию самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="f546c-112">You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="f546c-113">Привязка записей</span><span class="sxs-lookup"><span data-stu-id="f546c-113">Binding Entries</span></span>

<span data-ttu-id="f546c-114">Поля карты Visual C++ для ADO объекта [Recordset](recordset-object-ado.md) с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-114">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="f546c-115">Определение сопоставления между полем и переменной называется *записью привязки.*</span><span class="sxs-lookup"><span data-stu-id="f546c-115">The definition of a mapping between a field and a variable is called a *binding entry*.</span></span> <span data-ttu-id="f546c-116">Макрос предоставляет записи привязки для числовой, фиксированной длины и переменной длины данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-116">Macros provide binding entries for numeric, fixed-length, and variable-length data.</span></span> <span data-ttu-id="f546c-117">Записи привязки и переменные C/C++ объявляются в классе, производном от класса Visual C++ **Extensions, CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="f546c-117">The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**.</span></span> <span data-ttu-id="f546c-118">Класс **CADORecordBinding** определяется внутренним образом макросами записи привязки.</span><span class="sxs-lookup"><span data-stu-id="f546c-118">The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="f546c-119">ADO внутренне соповедет параметры в этих макросах со структурой **DBBINDING** OLE DB и создает объект OLE DB **Accessor** для управления перемещением и преобразованием данных между полями и переменными.</span><span class="sxs-lookup"><span data-stu-id="f546c-119">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables.</span></span> <span data-ttu-id="f546c-120">OLE DB определяет данные как состоящие из трех частей: *буфера,* в котором хранятся данные; *состояние,* которое указывает, было ли поле успешно сохранено в буфере или как переменная должна быть восстановлена в поле; и *длина* данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-120">OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data.</span></span> <span data-ttu-id="f546c-121">(Дополнительные сведения см. в справочнике программиста *по OLE DB*, глава 6. Получение и настройка данных.)</span><span class="sxs-lookup"><span data-stu-id="f546c-121">(See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="f546c-122">Файл загона</span><span class="sxs-lookup"><span data-stu-id="f546c-122">Header File</span></span>

<span data-ttu-id="f546c-123">Включите в приложение следующий файл, чтобы использовать расширения Visual C++ для ADO:</span><span class="sxs-lookup"><span data-stu-id="f546c-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="f546c-124">Поля наборов записей привязки</span><span class="sxs-lookup"><span data-stu-id="f546c-124">Binding Recordset Fields</span></span>

<span data-ttu-id="f546c-125">**Привязка полей recordset к переменным C/C++**</span><span class="sxs-lookup"><span data-stu-id="f546c-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="f546c-126">Создайте класс, производный от **класса CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="f546c-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="f546c-127">Укажите записи привязки и соответствующие переменные C/C++ в производного класса.</span><span class="sxs-lookup"><span data-stu-id="f546c-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="f546c-128">Прикрепить записи привязки между **МАКРОСАМИ BEGIN \_ ADO \_ BINDING** и **END \_ ADO \_ BINDING.**</span><span class="sxs-lookup"><span data-stu-id="f546c-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="f546c-129">Не прерывать макрос запятой или запятой.</span><span class="sxs-lookup"><span data-stu-id="f546c-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="f546c-130">Соответствующие селитари автоматически заданы каждым макросом.</span><span class="sxs-lookup"><span data-stu-id="f546c-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="f546c-131">Укажите одну запись привязки для каждого поля, соедино с переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="f546c-132">Используйте соответствующий член из семейства макроса **ADO \_ FIXED LENGTH \_ \_ ENTRY,** **ADO \_ NUMERIC \_ ENTRY** или **ADO VARIABLE LENGTH \_ \_ \_ ENTRY.**</span><span class="sxs-lookup"><span data-stu-id="f546c-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="f546c-133">В приложении создайте экземпляр класса, производный от **CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="f546c-133">In your application, create an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="f546c-134">Получите интерфейс **IADORecordBinding** из **recordset.**</span><span class="sxs-lookup"><span data-stu-id="f546c-134">Get the **IADORecordBinding** interface from the **Recordset**.</span></span> <span data-ttu-id="f546c-135">Затем вызовите метод **BindToRecordset,** чтобы привязать поля **Recordset** к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-135">Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="f546c-136">Дополнительные сведения см. в примере расширений [Visual C++.](visual-c-extensions-example.md)</span><span class="sxs-lookup"><span data-stu-id="f546c-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="f546c-137">Методы интерфейса</span><span class="sxs-lookup"><span data-stu-id="f546c-137">Interface Methods</span></span>

<span data-ttu-id="f546c-138">Интерфейс **IADORecordBinding** имеет три метода: **BindToRecordset,** **AddNew** и **Update.**</span><span class="sxs-lookup"><span data-stu-id="f546c-138">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**.</span></span> <span data-ttu-id="f546c-139">Единственным аргументом для каждого метода является указатель на экземпляр класса, производный от **CADORecordBinding.**</span><span class="sxs-lookup"><span data-stu-id="f546c-139">The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="f546c-140">Поэтому методы **AddNew** и **Update** не могут указывать параметры имен методов ADO.</span><span class="sxs-lookup"><span data-stu-id="f546c-140">Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="f546c-141">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="f546c-141">**Syntax**</span></span>

<span data-ttu-id="f546c-142">Метод **BindToRecordset** связывает поля **Recordset** с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="f546c-143">Метод **AddNew** вызывает именовую строку, метод ADO [AddNew,](addnew-method-ado.md) чтобы добавить новую строку в **recordset.**</span><span class="sxs-lookup"><span data-stu-id="f546c-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="f546c-144">Метод **Update** вызывает имя , метод ADO [Update,](update-method-ado.md) для обновления **recordset**.</span><span class="sxs-lookup"><span data-stu-id="f546c-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="f546c-145">Макрос записи привязки</span><span class="sxs-lookup"><span data-stu-id="f546c-145">Binding Entry Macros</span></span>

<span data-ttu-id="f546c-146">Макрос записи привязки определяет связь поля **Recordset** и переменной.</span><span class="sxs-lookup"><span data-stu-id="f546c-146">Binding entry macros define the association of a **Recordset** field and a variable.</span></span> <span data-ttu-id="f546c-147">В начале и конце макроса набор записей привязки размесков.</span><span class="sxs-lookup"><span data-stu-id="f546c-147">A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="f546c-148">Семейства макроса предоставляются для данных фиксированной длины, таких как **adDate** или **adBoolean;** числовая информация, например **adTinyInt,** **adInteger** или **adDouble;** и данные переменной длины, такие как **adChar,** **adVarChar** или **adVarBinary.**</span><span class="sxs-lookup"><span data-stu-id="f546c-148">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**.</span></span> <span data-ttu-id="f546c-149">Все числимые типы, кроме **adVarNumeric,** также являются типами фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="f546c-149">All numeric types, except for **adVarNumeric**, are also fixed-length types.</span></span> <span data-ttu-id="f546c-150">Каждое семейство имеет разные наборы параметров, поэтому можно исключить не интересующие вас сведения о привязке.</span><span class="sxs-lookup"><span data-stu-id="f546c-150">Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="f546c-151">Дополнительные сведения см. в справочнике программиста *OLE DB,* приложении А. Типы данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="f546c-152">_**Начало записей привязки**_</span><span class="sxs-lookup"><span data-stu-id="f546c-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="f546c-153">**BEGIN \_ ADO \_ BINDING**(*Class)*</span><span class="sxs-lookup"><span data-stu-id="f546c-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="f546c-154">_**Данные фиксированной длины**_</span><span class="sxs-lookup"><span data-stu-id="f546c-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="f546c-155">**ADO \_ FIXED \_ LENGTH \_ ENTRY**(*Ordinal, DataType, Buffer, Status, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="f546c-156">**ADO \_ FIXED \_ LENGTH \_ ENTRY2**(*Ordinal, DataType, Buffer, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="f546c-157">_**Числовая информация**_</span><span class="sxs-lookup"><span data-stu-id="f546c-157">_**Numeric Data**_</span></span>

<span data-ttu-id="f546c-158">**ADO \_ NUMERIC \_ ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="f546c-159">**ADO \_ NUMERIC \_ ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="f546c-160">_**Данные переменной длины**_</span><span class="sxs-lookup"><span data-stu-id="f546c-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="f546c-161">**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ЗАПИСИ**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="f546c-162">**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="f546c-163">**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="f546c-164">**ADO \_ ПЕРЕМЕННАЯ \_ ДЛИНА \_ ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify)*</span><span class="sxs-lookup"><span data-stu-id="f546c-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="f546c-165">_**Конечные записи привязки**_</span><span class="sxs-lookup"><span data-stu-id="f546c-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="f546c-166">**END \_ ADO \_ BINDING**()</span><span class="sxs-lookup"><span data-stu-id="f546c-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f546c-167">Параметр</span><span class="sxs-lookup"><span data-stu-id="f546c-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="f546c-168">Описание</span><span class="sxs-lookup"><span data-stu-id="f546c-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f546c-169"><em>Class</em></span><span class="sxs-lookup"><span data-stu-id="f546c-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-170">Класс, в котором определены записи привязки и переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="f546c-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-172">Порядковая цифра, отсчитывая от одного поля <strong>Recordset,</strong> соответствующего переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="f546c-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="f546c-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-174">Эквивалентный тип данных ADO переменной C/C++ (список допустимых типов данных см. в <a href="datatypeenum.md">dataTypeEnum).</a></span><span class="sxs-lookup"><span data-stu-id="f546c-174">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types).</span></span> <span data-ttu-id="f546c-175">Значение поля <strong>Recordset</strong> при необходимости будет преобразовано в этот тип данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-175">The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-176"><em>Буфер</em></span><span class="sxs-lookup"><span data-stu-id="f546c-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-177">Имя переменной C/C++, в которой будет храниться поле <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-178"><em>Размер</em></span><span class="sxs-lookup"><span data-stu-id="f546c-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-179">Максимальный размер буфера в <em>ветвях.</em></span><span class="sxs-lookup"><span data-stu-id="f546c-179">Maximum size in bytes of <em>Buffer</em>.</span></span> <span data-ttu-id="f546c-180">Если <em>буфер</em> будет содержать строку переменной длины, опустоните ноль.</span><span class="sxs-lookup"><span data-stu-id="f546c-180">If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-181"><em>Состояние</em></span><span class="sxs-lookup"><span data-stu-id="f546c-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-182">Имя переменной, которая указывает, допустимо <em></em> ли содержимое буфера, и успешно ли преобразование поля <em>в DataType.</em></span><span class="sxs-lookup"><span data-stu-id="f546c-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="f546c-183">Два наиболее важных значения для этой переменной <strong>adFldOK</strong>, что означает успешное преобразование; и <strong>adFldNull</strong>, что означает, что значение поля будет вариантом типа VT_NULL а не просто пустым.</span><span class="sxs-lookup"><span data-stu-id="f546c-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="f546c-184">Возможные значения для <em>состояния</em> перечислены в следующей таблице, &quot; "Значения состояния".&quot;</span><span class="sxs-lookup"><span data-stu-id="f546c-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-185"><em>Modify</em></span><span class="sxs-lookup"><span data-stu-id="f546c-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-186">Boolean flag; Если задается значение TRUE, ADO разрешается обновлять соответствующее поле <strong>Recordset</strong> со значением в <em>буфере.</em></span><span class="sxs-lookup"><span data-stu-id="f546c-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="f546c-187">Задайте для параметра Boolean <em>modify</em> true, чтобы включить ADO для обновления привязанного поля, и FALSE, если вы хотите изучить поле, но не изменять его.</span><span class="sxs-lookup"><span data-stu-id="f546c-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-188"><em>Точность</em></span><span class="sxs-lookup"><span data-stu-id="f546c-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-189">Число цифр, которые могут быть представлены в числовой переменной.</span><span class="sxs-lookup"><span data-stu-id="f546c-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-190"><em>Масштабирование</em></span><span class="sxs-lookup"><span data-stu-id="f546c-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-191">Количество десятичных цифр в числовом переменных.</span><span class="sxs-lookup"><span data-stu-id="f546c-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="f546c-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="f546c-193">Имя четырех byte переменной, которая будет содержать фактическую длину данных в <em>буфере.</em></span><span class="sxs-lookup"><span data-stu-id="f546c-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="f546c-194">Значения состояния</span><span class="sxs-lookup"><span data-stu-id="f546c-194">Status Values</span></span>

<span data-ttu-id="f546c-195">Значение переменной *Status* указывает, было ли поле успешно скопировано в переменную.</span><span class="sxs-lookup"><span data-stu-id="f546c-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="f546c-196">При настройке данных *для параметра Status* может быть установлено состояние **adFldNull,** чтобы указать, что для поля **Recordset** должно быть установлено null.</span><span class="sxs-lookup"><span data-stu-id="f546c-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f546c-197">Константа</span><span class="sxs-lookup"><span data-stu-id="f546c-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="f546c-198">Значение</span><span class="sxs-lookup"><span data-stu-id="f546c-198">Value</span></span></p></th>
<th><p><span data-ttu-id="f546c-199">Описание</span><span class="sxs-lookup"><span data-stu-id="f546c-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f546c-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-201">0</span><span class="sxs-lookup"><span data-stu-id="f546c-201">0</span></span></p></td>
<td><p><span data-ttu-id="f546c-202">Возвращено ненулевом значение поля.</span><span class="sxs-lookup"><span data-stu-id="f546c-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-204">1 </span><span class="sxs-lookup"><span data-stu-id="f546c-204">1</span></span></p></td>
<td><p><span data-ttu-id="f546c-205">Привязка недействительна.</span><span class="sxs-lookup"><span data-stu-id="f546c-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-207">2 </span><span class="sxs-lookup"><span data-stu-id="f546c-207">2</span></span></p></td>
<td><p><span data-ttu-id="f546c-208">Значение не может быть преобразовано по другим причинам, кроме несоответствия подписи или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-210">3 </span><span class="sxs-lookup"><span data-stu-id="f546c-210">3</span></span></p></td>
<td><p><span data-ttu-id="f546c-211">При получении поля указывает, что возвращено значение null.</span><span class="sxs-lookup"><span data-stu-id="f546c-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="f546c-212">При настройке поля указывает, что для поля необходимо установить <strong>NULL,</strong> если это поле не может закодировать само <strong>NULL</strong> (например, массив символов или целый ряд).</span><span class="sxs-lookup"><span data-stu-id="f546c-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-214">4 </span><span class="sxs-lookup"><span data-stu-id="f546c-214">4</span></span></p></td>
<td><p><span data-ttu-id="f546c-215">Данные переменной длины или цифры были усечены.</span><span class="sxs-lookup"><span data-stu-id="f546c-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-217">5 </span><span class="sxs-lookup"><span data-stu-id="f546c-217">5</span></span></p></td>
<td><p><span data-ttu-id="f546c-218">Значение подписано, а тип данных переменной — нет.</span><span class="sxs-lookup"><span data-stu-id="f546c-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-220">6 </span><span class="sxs-lookup"><span data-stu-id="f546c-220">6</span></span></p></td>
<td><p><span data-ttu-id="f546c-221">Значение больше, чем может храниться в переменном типе данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-223">7 </span><span class="sxs-lookup"><span data-stu-id="f546c-223">7</span></span></p></td>
<td><p><span data-ttu-id="f546c-224">Неизвестный тип столбца и поле уже открыты.</span><span class="sxs-lookup"><span data-stu-id="f546c-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-226">8 </span><span class="sxs-lookup"><span data-stu-id="f546c-226">8</span></span></p></td>
<td><p><span data-ttu-id="f546c-227">Не удалось определить значение поля, например в новом ненаписаном поле без значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f546c-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-229">9 </span><span class="sxs-lookup"><span data-stu-id="f546c-229">9</span></span></p></td>
<td><p><span data-ttu-id="f546c-230">При обновлении нет разрешения на написание данных.</span><span class="sxs-lookup"><span data-stu-id="f546c-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-232">10 </span><span class="sxs-lookup"><span data-stu-id="f546c-232">10</span></span></p></td>
<td><p><span data-ttu-id="f546c-233">При обновлении значение поля нарушает целостность столбцов.</span><span class="sxs-lookup"><span data-stu-id="f546c-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-235">11</span><span class="sxs-lookup"><span data-stu-id="f546c-235">11</span></span></p></td>
<td><p><span data-ttu-id="f546c-236">При обновлении значение поля нарушает схему столбца.</span><span class="sxs-lookup"><span data-stu-id="f546c-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f546c-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-238">12 </span><span class="sxs-lookup"><span data-stu-id="f546c-238">12</span></span></p></td>
<td><p><span data-ttu-id="f546c-239">При обновлении недопустимый параметр состояния.</span><span class="sxs-lookup"><span data-stu-id="f546c-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f546c-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="f546c-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="f546c-241">13 </span><span class="sxs-lookup"><span data-stu-id="f546c-241">13</span></span></p></td>
<td><p><span data-ttu-id="f546c-242">При обновлении использовалось значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f546c-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

