---
title: Раздел схемы (Справочник по для настольных баз данных Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd1a67ebd992d90abf182c042bd3d68a6d0d4ce2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482589"
---
# <a name="schema-section"></a><span data-ttu-id="30e62-102">Schema Section</span><span class="sxs-lookup"><span data-stu-id="30e62-102">Schema Section</span></span>

<span data-ttu-id="30e62-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="30e62-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="30e62-104">Schema Section</span><span class="sxs-lookup"><span data-stu-id="30e62-104">Schema Section</span></span>

<span data-ttu-id="30e62-105">В разделе Схема является обязательным.</span><span class="sxs-lookup"><span data-stu-id="30e62-105">The schema section is required.</span></span> <span data-ttu-id="30e62-106">Как показано в предыдущем примере, ADO выводит подробные метаданных каждого столбца, чтобы сохранить как можно больше для обновления семантика значений данных.</span><span class="sxs-lookup"><span data-stu-id="30e62-106">As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating.</span></span> <span data-ttu-id="30e62-107">Тем не менее для загрузки в XML-КОДЕ ADO требуются только имена столбцов и строк, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="30e62-107">However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong.</span></span> <span data-ttu-id="30e62-108">Ниже приведен пример минимальной схемы:</span><span class="sxs-lookup"><span data-stu-id="30e62-108">Here is an example of a minimal schema:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

<span data-ttu-id="30e62-109">В случае выше ADO рассматривать данные как строки переменной длины, так как нет информации о типах включен в схеме.</span><span class="sxs-lookup"><span data-stu-id="30e62-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="30e62-110">Создание псевдонимов для имен столбцов</span><span class="sxs-lookup"><span data-stu-id="30e62-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="30e62-111">Атрибут **rs: имя** позволяет создать псевдоним для имени столбца, чтобы это понятное имя может отображаться в столбец сведения, предоставляемые элементом набор строк и более короткое имя могут быть использованы в разделе данных.</span><span class="sxs-lookup"><span data-stu-id="30e62-111">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section.</span></span> <span data-ttu-id="30e62-112">Например схемы, указанной выше может быть изменено сопоставьте ShipperID s1 CompanyName для s2, и номера на s3 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="30e62-112">For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

<span data-ttu-id="30e62-113">Затем в разделе данных строки использовать атрибут **name** (не **rs: имя**) для ссылки на этот столбец:</span><span class="sxs-lookup"><span data-stu-id="30e62-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="30e62-114">Создание псевдонимов для имен столбцов является обязательным, каждый раз, когда имя столбца не является допустимым именем атрибут или тега в формате XML.</span><span class="sxs-lookup"><span data-stu-id="30e62-114">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML.</span></span> <span data-ttu-id="30e62-115">Например, «Фамилия» имеет псевдоним из-за незаконную атрибуты имен с пробелы.</span><span class="sxs-lookup"><span data-stu-id="30e62-115">For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes.</span></span> <span data-ttu-id="30e62-116">Следующая строка больше не обрабатывается правильно средство синтаксического анализа XML, поэтому необходимо создать псевдоним для другое имя, для которого не пробелы:</span><span class="sxs-lookup"><span data-stu-id="30e62-116">The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="30e62-117">Любое значение, используйте для атрибута **name** должен использоваться постоянно на каждом месте, что ссылку на столбец в разделах схема и данные XML-документа.</span><span class="sxs-lookup"><span data-stu-id="30e62-117">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document.</span></span> <span data-ttu-id="30e62-118">В следующем примере показано согласованное использование s1:</span><span class="sxs-lookup"><span data-stu-id="30e62-118">The following example shows the consistent use of s1:</span></span>

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

<span data-ttu-id="30e62-119">Аналогично поскольку псевдоним, не заданных для CompanyName выше, CompanyName должен использоваться постоянно в документе.</span><span class="sxs-lookup"><span data-stu-id="30e62-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="30e62-120">Типы данных</span><span class="sxs-lookup"><span data-stu-id="30e62-120">Data Types</span></span>

<span data-ttu-id="30e62-121">Тип данных можно применять в столбец с помощью атрибута **dt:type** .</span><span class="sxs-lookup"><span data-stu-id="30e62-121">You can apply a data type to a column with the **dt:type** attribute.</span></span> <span data-ttu-id="30e62-122">Тип данных можно указать двумя способами: Укажите атрибут **dt:type** непосредственно на определение столбца самого или использовать конструкцию **s:datatype** в качестве вложенного элемента определение столбца.</span><span class="sxs-lookup"><span data-stu-id="30e62-122">You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition.</span></span> <span data-ttu-id="30e62-123">Например:</span><span class="sxs-lookup"><span data-stu-id="30e62-123">For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="30e62-124">соответствует</span><span class="sxs-lookup"><span data-stu-id="30e62-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="30e62-125">Если опустить атрибут **dt:type** из определения строки по умолчанию, тип столбца будет строка переменной длины.</span><span class="sxs-lookup"><span data-stu-id="30e62-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="30e62-126">Если у вас есть Дополнительные сведения о типе, чем просто имя типа (например, **dt:maxLength**), становится более удобным для чтения, чтобы использовать дочерний элемент **s:datatype** .</span><span class="sxs-lookup"><span data-stu-id="30e62-126">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element.</span></span> <span data-ttu-id="30e62-127">Это просто соглашение, тем не менее и не является обязательным требованием.</span><span class="sxs-lookup"><span data-stu-id="30e62-127">This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="30e62-128">В приведенных ниже примерах Далее показано, как для включения информации о типах в схеме:</span><span class="sxs-lookup"><span data-stu-id="30e62-128">The following examples show further how to include type information in your schema:</span></span>

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

<span data-ttu-id="30e62-129">Существует тонкой использования атрибута **rs: fixedlength** во втором примере.</span><span class="sxs-lookup"><span data-stu-id="30e62-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="30e62-130">Столбец с помощью атрибута **rs: fixedlength** значение true означает, что данные должны иметь длину, определенном в схеме.</span><span class="sxs-lookup"><span data-stu-id="30e62-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="30e62-131">В этом случае юридическом значение для заголовка\_идентификатор является «123456», как «123».</span><span class="sxs-lookup"><span data-stu-id="30e62-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="30e62-132">Тем не менее «123» не будет допустимым, так как его длина 3, не 6.</span><span class="sxs-lookup"><span data-stu-id="30e62-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="30e62-133">В руководстве программиста OLE DB для более полное описание свойства **fixedlength** .</span><span class="sxs-lookup"><span data-stu-id="30e62-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="30e62-134">Обработка значения NULL</span><span class="sxs-lookup"><span data-stu-id="30e62-134">Handling Nulls</span></span>

<span data-ttu-id="30e62-135">Пустые значения обрабатываются в атрибуте **rs: maybenull** .</span><span class="sxs-lookup"><span data-stu-id="30e62-135">Null values are handled by the **rs:maybenull** attribute.</span></span> <span data-ttu-id="30e62-136">Если этот атрибут имеет значение true, содержимое столбца может содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="30e62-136">If this attribute is set to true, the contents of the column may contain a null value.</span></span> <span data-ttu-id="30e62-137">Кроме того Если столбец не найден в строку данных, пользователь, чтение данных из строк получит значение null, состояние из **IRowset::GetData()**.</span><span class="sxs-lookup"><span data-stu-id="30e62-137">Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**.</span></span> <span data-ttu-id="30e62-138">Рассмотрим следующие определения столбца из таблицы «Поставщики».</span><span class="sxs-lookup"><span data-stu-id="30e62-138">Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="30e62-139">Определение позволяет CompanyName должен иметь значение null, но ShipperID не может содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="30e62-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="30e62-140">В разделе данных содержит следующие строки, поставщика службы сохранения установить состояние данных для столбца CompanyName значение состояния OLE DB константу DBSTATUS\_S\_ISNULL:</span><span class="sxs-lookup"><span data-stu-id="30e62-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="30e62-141">Если строка совершенно пустым, как показано ниже, поставщика службы сохранения вернет статус OLE DB DBSTATUS\_E\_НЕДОСТУПЕН для ShipperID и DBSTATUS\_S\_ISNULL для CompanyName.</span><span class="sxs-lookup"><span data-stu-id="30e62-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="30e62-142">Обратите внимание на то, что строка нулевой длины не то же, что значение null.</span><span class="sxs-lookup"><span data-stu-id="30e62-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="30e62-143">Для предыдущего строки поставщика службы сохранения Возвращает статус OLE DB DBSTATUS\_S\_ОК для обоих столбцов.</span><span class="sxs-lookup"><span data-stu-id="30e62-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="30e62-144">Имя компании в данном случае — это просто «» (строка нулевой длины).</span><span class="sxs-lookup"><span data-stu-id="30e62-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="30e62-145">Для дополнительных сведений о OLE DB создает доступным для использования в схеме XML-документа для OLE DB, просмотреть определение «urn: schemas-microsoft-com:rowset» и руководство программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="30e62-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>

