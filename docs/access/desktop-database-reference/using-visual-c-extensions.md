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
# <a name="using-visual-c-extensions"></a><span data-ttu-id="ee99a-102">Использование расширений Visual C++</span><span class="sxs-lookup"><span data-stu-id="ee99a-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="ee99a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee99a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="ee99a-104">Интерфейс Иадорекордбиндинг</span><span class="sxs-lookup"><span data-stu-id="ee99a-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="ee99a-105">Расширения Microsoft Visual C++ для ADO связывают или привязывают поля объекта [Recordset](recordset-object-ado.md) к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-105">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="ee99a-106">При изменении текущей строки в связанном **наборе записей** все связанные поля в **наборе записей** копируются в переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-106">Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables.</span></span> <span data-ttu-id="ee99a-107">При необходимости скопированные данные преобразуются в объявленный тип данных переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-107">If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="ee99a-108">Метод **биндторекордсет** интерфейса **иадорекордбиндинг** привязывают поля к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-108">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables.</span></span> <span data-ttu-id="ee99a-109">Метод **AddNew** добавляет новую строку в связанный **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-109">The **AddNew** method adds a new row to the bound **Recordset**.</span></span> <span data-ttu-id="ee99a-110">Метод **Update** заполняет поля в новых строках **набора записей**или обновляет поля в существующих строках, используя значения переменных C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-110">The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="ee99a-111">Интерфейс **иадорекордбиндинг** реализуется с помощью объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ee99a-111">The **IADORecordBinding** interface is implemented by the **Recordset** object.</span></span> <span data-ttu-id="ee99a-112">Вы не можете самостоятельно кодировать реализацию.</span><span class="sxs-lookup"><span data-stu-id="ee99a-112">You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="ee99a-113">Записи привязки</span><span class="sxs-lookup"><span data-stu-id="ee99a-113">Binding Entries</span></span>

<span data-ttu-id="ee99a-114">Расширения Visual C++ для полей сопоставления ADO объекта [Recordset](recordset-object-ado.md) с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-114">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables.</span></span> <span data-ttu-id="ee99a-115">Определение сопоставления между полем и переменной называется *записью привязки*.</span><span class="sxs-lookup"><span data-stu-id="ee99a-115">The definition of a mapping between a field and a variable is called a *binding entry*.</span></span> <span data-ttu-id="ee99a-116">Макросы предоставляют записи привязки для числовых, фиксированной длины и данных переменной длины.</span><span class="sxs-lookup"><span data-stu-id="ee99a-116">Macros provide binding entries for numeric, fixed-length, and variable-length data.</span></span> <span data-ttu-id="ee99a-117">Записи привязки и переменные C/C++ объявляются в классе, производном от класса расширений Visual C++, **кадорекордбиндинг**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-117">The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**.</span></span> <span data-ttu-id="ee99a-118">Класс **кадорекордбиндинг** определяется внутренним образом с помощью макросов записи привязки.</span><span class="sxs-lookup"><span data-stu-id="ee99a-118">The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="ee99a-119">ADO внутренне сопоставляет параметры в этих макросах с структурой **ДББИНДИНГ** OLE DB и создает объект средства **доступа** OLE DB для управления перемещением и преобразованием данных между полями и переменными.</span><span class="sxs-lookup"><span data-stu-id="ee99a-119">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables.</span></span> <span data-ttu-id="ee99a-120">OLE DB определяет данные, состоящие из трех частей: *буфера* , в котором хранятся данные; *состояние* , указывающее, успешно ли сохранено поле в буфере или как переменная должна быть восстановлена в поле; и *Длина* данных.</span><span class="sxs-lookup"><span data-stu-id="ee99a-120">OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data.</span></span> <span data-ttu-id="ee99a-121">(См. *Справочник по программированию OLE DB*, глава 6: извлечение и Настройка данных для получения дополнительных сведений.)</span><span class="sxs-lookup"><span data-stu-id="ee99a-121">(See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="ee99a-122">Заголовочный файл</span><span class="sxs-lookup"><span data-stu-id="ee99a-122">Header File</span></span>

<span data-ttu-id="ee99a-123">Добавьте следующий файл в приложение, чтобы использовать расширения Visual C++ для ADO:</span><span class="sxs-lookup"><span data-stu-id="ee99a-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="ee99a-124">Привязка полей Recordset</span><span class="sxs-lookup"><span data-stu-id="ee99a-124">Binding Recordset Fields</span></span>

<span data-ttu-id="ee99a-125">**Привязка полей Recordset к переменным C/C++**</span><span class="sxs-lookup"><span data-stu-id="ee99a-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="ee99a-126">Создайте класс, производный от класса **кадорекордбиндинг** .</span><span class="sxs-lookup"><span data-stu-id="ee99a-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="ee99a-127">Укажите записи привязки и соответствующие переменные C/C++ в производном классе.</span><span class="sxs-lookup"><span data-stu-id="ee99a-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="ee99a-128">Разделять записи привязки между макросами **\_Begin привязки ADO\_** и **End\_привязки ADO\_** .</span><span class="sxs-lookup"><span data-stu-id="ee99a-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="ee99a-129">Не прерывать макросы запятыми или точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="ee99a-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="ee99a-130">Соответствующие разделители задаются автоматически каждым макросом.</span><span class="sxs-lookup"><span data-stu-id="ee99a-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="ee99a-131">Укажите одну запись привязки для каждого поля, которое необходимо сопоставить с переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="ee99a-132">Используйте соответствующий член из **записи фиксированной\_\_\_длины ADO**, **цифровой\_\_записи ADO**или семейства макросов с **записью\_переменной\_длины\_ADO** .</span><span class="sxs-lookup"><span data-stu-id="ee99a-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="ee99a-133">В приложении создайте экземпляр класса, производного от **кадорекордбиндинг**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-133">In your application, create an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="ee99a-134">Получение интерфейса **иадорекордбиндинг** из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-134">Get the **IADORecordBinding** interface from the **Recordset**.</span></span> <span data-ttu-id="ee99a-135">Затем вызовите метод **биндторекордсет** , чтобы присоединить поля **Recordset** к переменным C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-135">Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="ee99a-136">Дополнительные сведения см. в [примере расширений Visual C++](visual-c-extensions-example.md) .</span><span class="sxs-lookup"><span data-stu-id="ee99a-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="ee99a-137">Методы интерфейса</span><span class="sxs-lookup"><span data-stu-id="ee99a-137">Interface Methods</span></span>

<span data-ttu-id="ee99a-138">Интерфейс **иадорекордбиндинг** содержит три метода: **биндторекордсет**, **AddNew**и **Update**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-138">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**.</span></span> <span data-ttu-id="ee99a-139">Единственный аргумент для каждого метода является указателем на экземпляр класса, производного от **кадорекордбиндинг**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-139">The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**.</span></span> <span data-ttu-id="ee99a-140">Таким образом, методы **AddNew** и **Update** не могут указывать ни один из параметров метода ADO намесакес.</span><span class="sxs-lookup"><span data-stu-id="ee99a-140">Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="ee99a-141">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ee99a-141">**Syntax**</span></span>

<span data-ttu-id="ee99a-142">Метод **биндторекордсет** связывает поля **набора записей** с переменными C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="ee99a-143">Метод **AddNew** вызывает метод намесаке, метод ADO [AddNew](addnew-method-ado.md) , чтобы добавить новую строку в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="ee99a-144">Метод **Update** вызывает метод намесаке, способ [обновления](update-method-ado.md) ADO, для обновления объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="ee99a-145">Привязка макросов записи</span><span class="sxs-lookup"><span data-stu-id="ee99a-145">Binding Entry Macros</span></span>

<span data-ttu-id="ee99a-146">Привязывание макросов записи определяет связь поля **набора записей** и переменной.</span><span class="sxs-lookup"><span data-stu-id="ee99a-146">Binding entry macros define the association of a **Recordset** field and a variable.</span></span> <span data-ttu-id="ee99a-147">Начальный и конечный макросы ограничивают набор записей привязки.</span><span class="sxs-lookup"><span data-stu-id="ee99a-147">A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="ee99a-148">Для данных фиксированной длины, таких как **аддате** или **адбулеан**, предусмотрены семейства макросов; числовые данные, например **адтининт**, **адинтежер**или **аддаубле**; и данные переменной длины, такие как **адчар**, **адварчар** или **адварбинари**.</span><span class="sxs-lookup"><span data-stu-id="ee99a-148">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**.</span></span> <span data-ttu-id="ee99a-149">Все числовые типы, кроме **адварнумерик**, также являются типами фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="ee99a-149">All numeric types, except for **adVarNumeric**, are also fixed-length types.</span></span> <span data-ttu-id="ee99a-150">Каждое семейство имеет разные наборы параметров, чтобы можно было исключить информацию о привязке, не представляющую интереса.</span><span class="sxs-lookup"><span data-stu-id="ee99a-150">Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="ee99a-151">В *справочных материалах программиста OLE DB,* приложение а: типы данных для дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="ee99a-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="ee99a-152">_**Начало записи привязки**_</span><span class="sxs-lookup"><span data-stu-id="ee99a-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="ee99a-153">**Начало\_привязки\_ADO**(*класс*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="ee99a-154">_**Данные фиксированной длины**_</span><span class="sxs-lookup"><span data-stu-id="ee99a-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="ee99a-155">**Запись\_\_фиксированной\_длины ADO**(*порядковый номер, тип данных, буфер, состояние, изменение*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="ee99a-156">**\_Фиксированная\_длина\_ADO ENTRY2**(*Ordinal, DataType, buffer, Modify*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="ee99a-157">_**Числовые данные**_</span><span class="sxs-lookup"><span data-stu-id="ee99a-157">_**Numeric Data**_</span></span>

<span data-ttu-id="ee99a-158">**\_Числовая\_запись ADO**(*Ordinal, DataType, buffer, Precision, Scale, Status, Modify*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="ee99a-159">**\_Числовой\_ENTRY2 ADO**(*порядковый, тип данных, буфер, точность, масштаб, изменение*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="ee99a-160">_**Данные переменной длины**_</span><span class="sxs-lookup"><span data-stu-id="ee99a-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="ee99a-161">**Запись\_переменной\_длины\_ADO**(*порядковый номер, тип данных, буфер, размер, состояние, длина, изменение*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="ee99a-162">**\_ПЕРЕМЕННАЯ\_длина\_ADO ENTRY2**(*Ordinal, DataType, buffer, Size, Status, Modify*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="ee99a-163">**\_ПЕРЕМЕННАЯ\_длина\_ADO ENTRY3**(*Ordinal, DataType, buffer, Size, Length, Modify*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="ee99a-164">**\_ПЕРЕМЕННАЯ\_длина\_ADO ENTRY4**(*Ordinal, DataType, buffer, Size, Modify*)</span><span class="sxs-lookup"><span data-stu-id="ee99a-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="ee99a-165">_**Закончить записи привязки**_</span><span class="sxs-lookup"><span data-stu-id="ee99a-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="ee99a-166">**Завершение\_привязки\_ADO**()</span><span class="sxs-lookup"><span data-stu-id="ee99a-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee99a-167">Параметр</span><span class="sxs-lookup"><span data-stu-id="ee99a-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="ee99a-168">Описание</span><span class="sxs-lookup"><span data-stu-id="ee99a-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-169"><em>Класс</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-170">Класс, в котором определены записи привязки и переменные C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-172">Порядковый номер, подсчитывающий из одного из поля <strong>Recordset</strong> , соответствующего переменной C/C++.</span><span class="sxs-lookup"><span data-stu-id="ee99a-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-174">Эквивалентный тип данных ADO для переменной C/C++ (обратитесь к разделу <a href="datatypeenum.md">DataTypeEnum</a> для получения списка допустимых типов данных).</span><span class="sxs-lookup"><span data-stu-id="ee99a-174">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types).</span></span> <span data-ttu-id="ee99a-175">Если необходимо, значение поля <strong>Recordset</strong> будет преобразовано в этот тип данных.</span><span class="sxs-lookup"><span data-stu-id="ee99a-175">The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-176"><em>Буферизовать</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-177">Имя переменной C/C++, в которой будет храниться поле <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee99a-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-178"><em>Размер</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-179">Максимальный размер <em>буфера</em>в байтах.</span><span class="sxs-lookup"><span data-stu-id="ee99a-179">Maximum size in bytes of <em>Buffer</em>.</span></span> <span data-ttu-id="ee99a-180">Если <em>буфер</em> будет содержать строку переменной длины, разрешите место для нулевого значения.</span><span class="sxs-lookup"><span data-stu-id="ee99a-180">If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-181"><em>Состояние</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-182">Имя переменной, указывающей, является ли содержимое <em>буфера</em> допустимым и было ли преобразование поля в <em>тип данных</em> успешным.</span><span class="sxs-lookup"><span data-stu-id="ee99a-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="ee99a-183">Два наиболее важных значения этой переменной — <strong>адфлдок</strong>, что означает, что преобразование выполнено успешно; и <strong>адфлднулл</strong>, что означает, что значение поля является вариантом типа VT_NULL, а не просто пустым.</span><span class="sxs-lookup"><span data-stu-id="ee99a-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="ee99a-184">Возможные значения <em>Status</em> указаны в следующей таблице: &quot;значения состояния.&quot;</span><span class="sxs-lookup"><span data-stu-id="ee99a-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-185"><em>Modify</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-186">Логический флаг; Если этот параметр имеет значение TRUE, то для ADO разрешено обновление соответствующего поля <strong>Recordset</strong> с использованием значения, содержащегося в <em>буфере</em>.</span><span class="sxs-lookup"><span data-stu-id="ee99a-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="ee99a-187">Установите для параметра логического <em>изменения</em> значение true, чтобы функция ADO обновляла связанное поле, и значение false, если нужно проверить поле, но не изменять его.</span><span class="sxs-lookup"><span data-stu-id="ee99a-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-188"><em>Точности</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-189">Количество цифр, которое может быть представлено в числовой переменной.</span><span class="sxs-lookup"><span data-stu-id="ee99a-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-190"><em>Масштабирование</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-191">Количество десятичных разрядов в числовой переменной.</span><span class="sxs-lookup"><span data-stu-id="ee99a-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="ee99a-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="ee99a-193">Имя переменной из четырех байтов, которая будет содержать фактическую длину данных в <em>буфере</em>.</span><span class="sxs-lookup"><span data-stu-id="ee99a-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="ee99a-194">Значения состояния</span><span class="sxs-lookup"><span data-stu-id="ee99a-194">Status Values</span></span>

<span data-ttu-id="ee99a-195">Значение переменной *Status* указывает, было ли поле успешно скопировано в переменную.</span><span class="sxs-lookup"><span data-stu-id="ee99a-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="ee99a-196">При задании данных параметру *Status* может быть присвоено значение **адфлднулл** , чтобы указать, что поле **Recordset** должно иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="ee99a-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee99a-197">Константа</span><span class="sxs-lookup"><span data-stu-id="ee99a-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="ee99a-198">Значение</span><span class="sxs-lookup"><span data-stu-id="ee99a-198">Value</span></span></p></th>
<th><p><span data-ttu-id="ee99a-199">Описание</span><span class="sxs-lookup"><span data-stu-id="ee99a-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-200"><strong>адфлдок</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-201">нуль</span><span class="sxs-lookup"><span data-stu-id="ee99a-201">0</span></span></p></td>
<td><p><span data-ttu-id="ee99a-202">Возвращено значение поля, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="ee99a-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-203"><strong>адфлдбадакцессор</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-204">1,1</span><span class="sxs-lookup"><span data-stu-id="ee99a-204">1</span></span></p></td>
<td><p><span data-ttu-id="ee99a-205">Недопустимая привязка.</span><span class="sxs-lookup"><span data-stu-id="ee99a-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-206"><strong>адфлдкантконвертвалуе</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-207">2</span><span class="sxs-lookup"><span data-stu-id="ee99a-207">2</span></span></p></td>
<td><p><span data-ttu-id="ee99a-208">Не удалось преобразовать значение по причине, отличной от несоответствия знака или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="ee99a-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-209"><strong>адфлднулл</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-210">4</span><span class="sxs-lookup"><span data-stu-id="ee99a-210">3</span></span></p></td>
<td><p><span data-ttu-id="ee99a-211">При возврате поля показывается, что было возвращено значение null.</span><span class="sxs-lookup"><span data-stu-id="ee99a-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="ee99a-212">При установке поля указывает, что для поля должно быть задано <strong>значение NULL</strong> , если поле не может закодировать само <strong>значение NULL</strong> (например, массив символов или целое число).</span><span class="sxs-lookup"><span data-stu-id="ee99a-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-213"><strong>адфлдтрункатед</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-214">4 </span><span class="sxs-lookup"><span data-stu-id="ee99a-214">4</span></span></p></td>
<td><p><span data-ttu-id="ee99a-215">Данные переменной длины или цифры были усечены.</span><span class="sxs-lookup"><span data-stu-id="ee99a-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-216"><strong>адфлдсигнмисматч</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-217">5 </span><span class="sxs-lookup"><span data-stu-id="ee99a-217">5</span></span></p></td>
<td><p><span data-ttu-id="ee99a-218">Значение имеет подпись и тип данных переменной не подписан.</span><span class="sxs-lookup"><span data-stu-id="ee99a-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-219"><strong>адфлддатаоверфлов</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-220">6 </span><span class="sxs-lookup"><span data-stu-id="ee99a-220">6</span></span></p></td>
<td><p><span data-ttu-id="ee99a-221">Значение больше, чем может храниться в типе данных переменной.</span><span class="sxs-lookup"><span data-stu-id="ee99a-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-222"><strong>адфлдканткреате</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-223">7 </span><span class="sxs-lookup"><span data-stu-id="ee99a-223">7</span></span></p></td>
<td><p><span data-ttu-id="ee99a-224">Неизвестный тип столбца и поле уже открыто.</span><span class="sxs-lookup"><span data-stu-id="ee99a-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-225"><strong>адфлдунаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-226">8 </span><span class="sxs-lookup"><span data-stu-id="ee99a-226">8</span></span></p></td>
<td><p><span data-ttu-id="ee99a-227">Не удалось определить значение поля, например, для нового неназначенного поля без значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee99a-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-228"><strong>адфлдпермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-229">9 </span><span class="sxs-lookup"><span data-stu-id="ee99a-229">9</span></span></p></td>
<td><p><span data-ttu-id="ee99a-230">При обновлении разрешение на запись данных не разрешится.</span><span class="sxs-lookup"><span data-stu-id="ee99a-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-231"><strong>адфлдинтегритивиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-232">10 </span><span class="sxs-lookup"><span data-stu-id="ee99a-232">10</span></span></p></td>
<td><p><span data-ttu-id="ee99a-233">При обновлении значение поля нарушает целостность столбца.</span><span class="sxs-lookup"><span data-stu-id="ee99a-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-234"><strong>адфлдсчемавиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-235">11 </span><span class="sxs-lookup"><span data-stu-id="ee99a-235">11</span></span></p></td>
<td><p><span data-ttu-id="ee99a-236">При обновлении значение поля нарушает схему столбца.</span><span class="sxs-lookup"><span data-stu-id="ee99a-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee99a-237"><strong>адфлдбадстатус</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-238">12 </span><span class="sxs-lookup"><span data-stu-id="ee99a-238">12</span></span></p></td>
<td><p><span data-ttu-id="ee99a-239">При обновлении — недопустимый параметр Status.</span><span class="sxs-lookup"><span data-stu-id="ee99a-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee99a-240"><strong>адфлддефаулт</strong></span><span class="sxs-lookup"><span data-stu-id="ee99a-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="ee99a-241">13</span><span class="sxs-lookup"><span data-stu-id="ee99a-241">13</span></span></p></td>
<td><p><span data-ttu-id="ee99a-242">При обновлении используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee99a-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

