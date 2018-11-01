---
title: Использование расширений Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcfde7e343a37d65356e1f9ed8d879030913f5ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868786"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="0d21e-102">Использование расширений Visual C++</span><span class="sxs-lookup"><span data-stu-id="0d21e-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="0d21e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d21e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="0d21e-104">Интерфейс IADORecordBinding</span><span class="sxs-lookup"><span data-stu-id="0d21e-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="0d21e-105">Расширения Visual C++ Майкрософт для полей свяжите ADO или привязку объекта [набора записей](recordset-object-ado.md) переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-105">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="0d21e-106">При каждом изменении текущей строки связанных **записей** , привязанных полей в **записей** копируются переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-106">Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables.</span></span> <span data-ttu-id="0d21e-107">При необходимости, скопированные данные преобразуется в тип данных объявленные переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-107">If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="0d21e-108">Метод **BindToRecordset** интерфейса **IADORecordBinding** привязывает поля переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-108">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables.</span></span> <span data-ttu-id="0d21e-109">Метод **AddNew** добавляет новую строку в привязанной **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-109">The **AddNew** method adds a new row to the bound **Recordset**.</span></span> <span data-ttu-id="0d21e-110">Метод **Update** заполняет поля в новые строки **набора записей**или обновления поля в строках со значением переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-110">The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="0d21e-111">Интерфейс **IADORecordBinding** реализуется объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="0d21e-111">The **IADORecordBinding** interface is implemented by the **Recordset** object.</span></span> <span data-ttu-id="0d21e-112">Не кода реализации самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="0d21e-112">You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="0d21e-113">Привязка записей</span><span class="sxs-lookup"><span data-stu-id="0d21e-113">Binding Entries</span></span>

<span data-ttu-id="0d21e-114">Расширения Visual C++ для ADO сопоставление полей объекта [набора записей](recordset-object-ado.md) с переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-114">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="0d21e-115">Определения сопоставления между полем и переменной называется *записи привязки*.</span><span class="sxs-lookup"><span data-stu-id="0d21e-115">The definition of a mapping between a field and a variable is called a *binding entry*.</span></span> <span data-ttu-id="0d21e-116">Макросы предоставляют записи привязки для числовых, фиксированной длины и переменной длины данных.</span><span class="sxs-lookup"><span data-stu-id="0d21e-116">Macros provide binding entries for numeric, fixed-length, and variable-length data.</span></span> <span data-ttu-id="0d21e-117">Привязка записей и переменные C/C++ объявляются в класс, производный от класса расширения Visual C++ **CADORecordBinding**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-117">The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**.</span></span> <span data-ttu-id="0d21e-118">Класс **CADORecordBinding** определяется во внутренней сети в привязке записи макросов.</span><span class="sxs-lookup"><span data-stu-id="0d21e-118">The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="0d21e-119">ADO во внутренней сети сопоставляется структуру OLE DB **DBBINDING** параметров в этих макросов и создает объект OLE DB **доступа к данным** для управления перемещения и преобразования данных между полями и переменных.</span><span class="sxs-lookup"><span data-stu-id="0d21e-119">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables.</span></span> <span data-ttu-id="0d21e-120">OLE DB определяет данные, состоящий из трех частей: *буфера* , где хранятся данные; *состояние* , указывает ли поле было успешно сохранены в буфере или как восстановлены переменная поля; и *длину* данных.</span><span class="sxs-lookup"><span data-stu-id="0d21e-120">OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data.</span></span> <span data-ttu-id="0d21e-121">( *Справочник программиста OLE DB*, Глава 6: получение и установка данных для получения дополнительных сведений.)</span><span class="sxs-lookup"><span data-stu-id="0d21e-121">(See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="0d21e-122">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="0d21e-122">Header File</span></span>

<span data-ttu-id="0d21e-123">Добавьте следующий файл в приложении для использования расширений Visual C++ для ADO:</span><span class="sxs-lookup"><span data-stu-id="0d21e-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="0d21e-124">Привязка полей набора записей</span><span class="sxs-lookup"><span data-stu-id="0d21e-124">Binding Recordset Fields</span></span>

<span data-ttu-id="0d21e-125">**Привязка полей набора записей переменным C/C++**</span><span class="sxs-lookup"><span data-stu-id="0d21e-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="0d21e-126">Создайте класс, производный от класса **CADORecordBinding** .</span><span class="sxs-lookup"><span data-stu-id="0d21e-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="0d21e-127">Укажите привязку записей и соответствующие переменные C/C++ в производного класса.</span><span class="sxs-lookup"><span data-stu-id="0d21e-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="0d21e-128">Квадратная скобка записей привязки между **приступить к\_ADO\_ПРИВЯЗКИ** и **конечных\_ADO\_ПРИВЯЗКИ** макросы.</span><span class="sxs-lookup"><span data-stu-id="0d21e-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="0d21e-129">Не прерывания макросов с помощью запятой или точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="0d21e-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="0d21e-130">Каждый макрос автоматически задаются соответствующие разделители.</span><span class="sxs-lookup"><span data-stu-id="0d21e-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="0d21e-131">Укажите одной записи привязки для каждого поля для сопоставления с переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="0d21e-132">Используйте соответствующий элемент из **ADO\_ФИКСИРОВАННАЯ\_длина\_запись**, **ADO\_ЧИСЛОВОЕ\_запись**, или **ADO\_ПЕРЕМЕННЫХ\_длина\_запись** семейства макросов.</span><span class="sxs-lookup"><span data-stu-id="0d21e-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="0d21e-133">В приложении создайте экземпляр класса, производного от **CADORecordBinding**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-133">In your application, create an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="0d21e-134">Получите интерфейс **IADORecordBinding** из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-134">Get the **IADORecordBinding** interface from the **Recordset**.</span></span> <span data-ttu-id="0d21e-135">Затем вызовите метод **BindToRecordset** для привязки полей **набора записей** переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-135">Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="0d21e-136">[Пример расширения Visual C++](visual-c-extensions-example.md) для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0d21e-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="0d21e-137">Методы интерфейса</span><span class="sxs-lookup"><span data-stu-id="0d21e-137">Interface Methods</span></span>

<span data-ttu-id="0d21e-138">Этот интерфейс **IADORecordBinding** содержит три метода: **BindToRecordset**, **AddNew**и **обновления**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-138">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**.</span></span> <span data-ttu-id="0d21e-139">Единственный аргумент для каждого метода — указатель на экземпляр класса, производного от **CADORecordBinding**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-139">The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="0d21e-140">Таким образом методы **AddNew** и **обновление** нельзя указать параметры их namesakes метод ADO.</span><span class="sxs-lookup"><span data-stu-id="0d21e-140">Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="0d21e-141">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="0d21e-141">**Syntax**</span></span>

<span data-ttu-id="0d21e-142">Метод **BindToRecordset** связывает полей **набора записей** с помощью переменных C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="0d21e-143">Метод **AddNew** вызывает его namesake, метод ADO [AddNew](addnew-method-ado.md) , чтобы добавить новую строку **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="0d21e-144">Метод **Update** вызывает его namesake, метод ADO [обновления](update-method-ado.md) для обновления **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="0d21e-145">Привязка записи макросов</span><span class="sxs-lookup"><span data-stu-id="0d21e-145">Binding Entry Macros</span></span>

<span data-ttu-id="0d21e-146">Привязка записи макросов определение поля **набора записей** и переменной.</span><span class="sxs-lookup"><span data-stu-id="0d21e-146">Binding entry macros define the association of a **Recordset** field and a variable.</span></span> <span data-ttu-id="0d21e-147">Макрос начального и конечного отделяет набор привязки записей.</span><span class="sxs-lookup"><span data-stu-id="0d21e-147">A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="0d21e-148">Семейства операционных систем макросов предоставляются для данных фиксированной длины, например **adDate** или **adBoolean**; числовые данные, такие как **adTinyInt**, **adInteger**или **adDouble**; и данные переменной длины, например **adChar**, **adVarChar** или **adVarBinary**.</span><span class="sxs-lookup"><span data-stu-id="0d21e-148">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**.</span></span> <span data-ttu-id="0d21e-149">Все числовые типы, за исключением **adVarNumeric**, могут также типы фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="0d21e-149">All numeric types, except for **adVarNumeric**, are also fixed-length types.</span></span> <span data-ttu-id="0d21e-150">Каждое семейство имеет различные наборы параметров, поэтому можно исключить сведения о привязке, не представляют интереса.</span><span class="sxs-lookup"><span data-stu-id="0d21e-150">Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="0d21e-151">Типы данных приложение а: *Справочник программиста OLE DB* для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0d21e-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="0d21e-152">_**Приступить к привязке записей**_</span><span class="sxs-lookup"><span data-stu-id="0d21e-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="0d21e-153">**Приступить к\_ADO\_ПРИВЯЗКИ**(*класс*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="0d21e-154">_**Данные фиксированной длины**_</span><span class="sxs-lookup"><span data-stu-id="0d21e-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="0d21e-155">**ADO\_ФИКСИРОВАННАЯ\_длина\_запись**(*порядковый номер, тип данных, буфера, состояние, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="0d21e-156">**ADO\_ФИКСИРОВАННАЯ\_длина\_ENTRY2**(*порядковый номер, тип данных, буфера, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="0d21e-157">_**Числовые данные**_</span><span class="sxs-lookup"><span data-stu-id="0d21e-157">_**Numeric Data**_</span></span>

<span data-ttu-id="0d21e-158">**ADO\_ЧИСЛОВОЕ\_запись**(*порядковый номер, тип данных, буфера, точности, масштаба, состояние, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="0d21e-159">**ADO\_ЧИСЛОВОЕ\_ENTRY2**(*порядковый номер, тип данных, буфера, точность, масштаб, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="0d21e-160">_**Данные переменной длины**_</span><span class="sxs-lookup"><span data-stu-id="0d21e-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="0d21e-161">**ADO\_ПЕРЕМЕННЫХ\_длина\_запись**(*порядковый номер, тип данных, буфер, размер, состояние, длину, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="0d21e-162">**ADO\_ПЕРЕМЕННЫХ\_длина\_ENTRY2**(*порядковый номер, тип данных, буфер, размер, состояние, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="0d21e-163">**ADO\_ПЕРЕМЕННЫХ\_длина\_ENTRY3**(*порядковый номер, тип данных, буфер, размер, длины, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="0d21e-164">**ADO\_ПЕРЕМЕННЫХ\_длина\_ENTRY4**(*порядковый номер, тип данных, буфер, размер, изменение*)</span><span class="sxs-lookup"><span data-stu-id="0d21e-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="0d21e-165">_**Привязка записи плана**_</span><span class="sxs-lookup"><span data-stu-id="0d21e-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="0d21e-166">**Конец\_ADO\_ПРИВЯЗКИ** ()</span><span class="sxs-lookup"><span data-stu-id="0d21e-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d21e-167">Параметр</span><span class="sxs-lookup"><span data-stu-id="0d21e-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="0d21e-168">Описание</span><span class="sxs-lookup"><span data-stu-id="0d21e-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-169"><em>Class</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-170">Класс определенные операции привязки и переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-171"><em>Порядковый номер</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-172">Порядковый номер, начиная с одним из поля <strong>набора записей</strong> , соответствующего переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d21e-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-174">Эквивалентный тип данных ADO переменной C/C++ (см. <a href="datatypeenum.md">DataTypeEnum</a> список типов данных).</span><span class="sxs-lookup"><span data-stu-id="0d21e-174">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types).</span></span> <span data-ttu-id="0d21e-175">Значение поля <strong>набора записей</strong> будут преобразованы в этот тип данных, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="0d21e-175">The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-176"><em>Буфера</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-177">Имя переменной C/C++, где будут храниться в поле <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0d21e-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-178"><em>Размер</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-179">Максимальный размер <em>буфера</em>в байтах.</span><span class="sxs-lookup"><span data-stu-id="0d21e-179">Maximum size in bytes of <em>Buffer</em>.</span></span> <span data-ttu-id="0d21e-180">Если <em>буфер</em> будет содержать строку переменной длины, разрешить комнаты для выполнения определенного нулю.</span><span class="sxs-lookup"><span data-stu-id="0d21e-180">If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-181"><em>Состояние</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-182">Имя переменной, которая появится сообщение о том, является ли содержимое <em>буфера</em> являются допустимыми и ли преобразование поля в <em>типе данных</em> прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="0d21e-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="0d21e-183">Наиболее важные значения для этой переменной не <strong>adFldOK</strong>, что означает, что преобразование прошло успешно; и <strong>adFldNull</strong>, что означает значение поля будет иметь тип VARIANT типа VT_NULL и не просто пустой.</span><span class="sxs-lookup"><span data-stu-id="0d21e-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="0d21e-184">В следующей таблице перечислены возможные значения для <em>состояния</em> &quot;значения состояния.&quot;</span><span class="sxs-lookup"><span data-stu-id="0d21e-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-185"><em>Modify</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-186">Флаг типа Boolean; Если значение TRUE, указывает, что ADO может обновить соответствующее поле <strong>записей</strong> со значением, содержащихся в <em>буфере</em>.</span><span class="sxs-lookup"><span data-stu-id="0d21e-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="0d21e-187">Параметр типа Boolean, <em>Изменение</em> в значение true, чтобы включить ADO для обновления связанное поле и FALSE, если вы хотите изучить поля, но не меняйте его.</span><span class="sxs-lookup"><span data-stu-id="0d21e-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-188"><em>Точность</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-189">Число знаков, которые могут быть представлены в числовая переменная.</span><span class="sxs-lookup"><span data-stu-id="0d21e-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-190"><em>Масштаб</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-191">Число десятичных знаков в числовая переменная.</span><span class="sxs-lookup"><span data-stu-id="0d21e-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-192"><em>Длина</em></span><span class="sxs-lookup"><span data-stu-id="0d21e-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="0d21e-193">Имя переменной 4 байта, которая будет содержать длину данные в <em>буфер</em>.</span><span class="sxs-lookup"><span data-stu-id="0d21e-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="0d21e-194">Значения состояний</span><span class="sxs-lookup"><span data-stu-id="0d21e-194">Status Values</span></span>

<span data-ttu-id="0d21e-195">Значение переменной *состояние* указывает, является ли поле успешно скопирована в переменной.</span><span class="sxs-lookup"><span data-stu-id="0d21e-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="0d21e-196">При задании данных, *состояние* может быть присвоено **adFldNull** для указания поля **набора записей** необходимо задать значение null.</span><span class="sxs-lookup"><span data-stu-id="0d21e-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d21e-197">Константа</span><span class="sxs-lookup"><span data-stu-id="0d21e-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="0d21e-198">Значение</span><span class="sxs-lookup"><span data-stu-id="0d21e-198">Value</span></span></p></th>
<th><p><span data-ttu-id="0d21e-199">Описание</span><span class="sxs-lookup"><span data-stu-id="0d21e-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-201">0</span><span class="sxs-lookup"><span data-stu-id="0d21e-201">0</span></span></p></td>
<td><p><span data-ttu-id="0d21e-202">Возвращено значение поля не являющееся null.</span><span class="sxs-lookup"><span data-stu-id="0d21e-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-204">1</span><span class="sxs-lookup"><span data-stu-id="0d21e-204">1</span></span></p></td>
<td><p><span data-ttu-id="0d21e-205">Привязка недопустима.</span><span class="sxs-lookup"><span data-stu-id="0d21e-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-207">2</span><span class="sxs-lookup"><span data-stu-id="0d21e-207">2</span></span></p></td>
<td><p><span data-ttu-id="0d21e-208">Не удалось преобразовать значение по причине, отличной от несоответствия знака или данных переполнения.</span><span class="sxs-lookup"><span data-stu-id="0d21e-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-210">3</span><span class="sxs-lookup"><span data-stu-id="0d21e-210">3</span></span></p></td>
<td><p><span data-ttu-id="0d21e-211">При получении поле, указывает, что возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="0d21e-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="0d21e-212">При установке на поле, указывает, что поле должно быть присвоено <strong>значение NULL,</strong> Если поле не удалось зашифровать <strong>значение NULL,</strong> сам (например, массив символов или целое число).</span><span class="sxs-lookup"><span data-stu-id="0d21e-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-214">4</span><span class="sxs-lookup"><span data-stu-id="0d21e-214">4</span></span></p></td>
<td><p><span data-ttu-id="0d21e-215">Данные переменной длины или цифр были усечено.</span><span class="sxs-lookup"><span data-stu-id="0d21e-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-217">5</span><span class="sxs-lookup"><span data-stu-id="0d21e-217">5</span></span></p></td>
<td><p><span data-ttu-id="0d21e-218">Значение является подписью и является неподписанные переменной типа.</span><span class="sxs-lookup"><span data-stu-id="0d21e-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-220">6</span><span class="sxs-lookup"><span data-stu-id="0d21e-220">6</span></span></p></td>
<td><p><span data-ttu-id="0d21e-221">Значение больше, чем может храниться в типе данных переменной.</span><span class="sxs-lookup"><span data-stu-id="0d21e-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-223">7</span><span class="sxs-lookup"><span data-stu-id="0d21e-223">7</span></span></p></td>
<td><p><span data-ttu-id="0d21e-224">Неизвестный тип столбца и поле уже открыт.</span><span class="sxs-lookup"><span data-stu-id="0d21e-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-226">8</span><span class="sxs-lookup"><span data-stu-id="0d21e-226">8</span></span></p></td>
<td><p><span data-ttu-id="0d21e-227">Не удается определить значение поля — например, на новое поле неназначенных без значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d21e-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-229">9</span><span class="sxs-lookup"><span data-stu-id="0d21e-229">9</span></span></p></td>
<td><p><span data-ttu-id="0d21e-230">При обновлении, нет разрешения для записи данных.</span><span class="sxs-lookup"><span data-stu-id="0d21e-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-232">10</span><span class="sxs-lookup"><span data-stu-id="0d21e-232">10</span></span></p></td>
<td><p><span data-ttu-id="0d21e-233">При обновлении, значение поля может нарушить целостности столбца.</span><span class="sxs-lookup"><span data-stu-id="0d21e-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-235">11</span><span class="sxs-lookup"><span data-stu-id="0d21e-235">11</span></span></p></td>
<td><p><span data-ttu-id="0d21e-236">При обновлении, значение поля нарушит схемы столбца.</span><span class="sxs-lookup"><span data-stu-id="0d21e-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d21e-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-238">12</span><span class="sxs-lookup"><span data-stu-id="0d21e-238">12</span></span></p></td>
<td><p><span data-ttu-id="0d21e-239">При обновлении параметр недопустимое состояние.</span><span class="sxs-lookup"><span data-stu-id="0d21e-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d21e-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="0d21e-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="0d21e-241">13</span><span class="sxs-lookup"><span data-stu-id="0d21e-241">13</span></span></p></td>
<td><p><span data-ttu-id="0d21e-242">При обновлении, было использовано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0d21e-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

