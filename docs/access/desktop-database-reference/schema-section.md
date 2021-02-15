---
title: Раздел схемы (справочник по базе данных Access для настольных ПК)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308941"
---
# <a name="schema-section"></a><span data-ttu-id="b3e65-102">Раздел схемы</span><span class="sxs-lookup"><span data-stu-id="b3e65-102">Schema section</span></span>

<span data-ttu-id="b3e65-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3e65-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="b3e65-104">Schema Section</span><span class="sxs-lookup"><span data-stu-id="b3e65-104">Schema Section</span></span>

<span data-ttu-id="b3e65-105">Раздел схемы является обязательной.</span><span class="sxs-lookup"><span data-stu-id="b3e65-105">The schema section is required.</span></span> <span data-ttu-id="b3e65-106">Как показано в предыдущем примере, ADO записывает подробные метаданные о каждом столбце, чтобы сохранить семантику значений данных как можно больше для обновления.</span><span class="sxs-lookup"><span data-stu-id="b3e65-106">As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating.</span></span> <span data-ttu-id="b3e65-107">Однако для загрузки в XML ADO требуются только имена столбцов и набор строк, к которым они принадлежат.</span><span class="sxs-lookup"><span data-stu-id="b3e65-107">However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong.</span></span> <span data-ttu-id="b3e65-108">Вот пример минимальной схемы:</span><span class="sxs-lookup"><span data-stu-id="b3e65-108">Here is an example of a minimal schema:</span></span>

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

<span data-ttu-id="b3e65-109">В вышеуказанной ситуации ADO будет рассматривать данные как строки переменной длины, так как в схему не включены сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="b3e65-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="b3e65-110">Создание псевдонимов для имен столбцов</span><span class="sxs-lookup"><span data-stu-id="b3e65-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="b3e65-111">Атрибут **rs:name** позволяет создать псевдоним для имени столбца, чтобы в сведениях о столбцах, которые кажутся в наборе строк, может отображаться удобное имя, а в разделе данных может использоваться более короткое имя.</span><span class="sxs-lookup"><span data-stu-id="b3e65-111">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section.</span></span> <span data-ttu-id="b3e65-112">Например, схему выше можно изменить, чтобы соотоставить ShipperID с s1, CompanyName с s2 и Phone на s3 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b3e65-112">For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

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

<span data-ttu-id="b3e65-113">Затем в разделе данных строка будет использовать атрибут **name** (не **rs:name)** для ссылки на этот столбец:</span><span class="sxs-lookup"><span data-stu-id="b3e65-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="b3e65-114">Создание псевдонимов для имен столбцов необходимо, если имя столбца не является юридическим атрибутом или именем тега в XML.</span><span class="sxs-lookup"><span data-stu-id="b3e65-114">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML.</span></span> <span data-ttu-id="b3e65-115">Например, "Фамилия" должна иметь псевдоним, так как имена с внедренными пробелами являются запрещенными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="b3e65-115">For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes.</span></span> <span data-ttu-id="b3e65-116">Следующая строка не будет правильно обработана синтакс помощью синтаксика XML, поэтому необходимо создать псевдоним для другого имени, которое не имеет встроенного пространства:</span><span class="sxs-lookup"><span data-stu-id="b3e65-116">The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="b3e65-117">Любое значение, используемое для атрибута **name,** должно использоваться согласованно в каждом месте, на который ссылается столбец в разделах схемы и данных XML-документа.</span><span class="sxs-lookup"><span data-stu-id="b3e65-117">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document.</span></span> <span data-ttu-id="b3e65-118">В следующем примере показано согласованное использование s1:</span><span class="sxs-lookup"><span data-stu-id="b3e65-118">The following example shows the consistent use of s1:</span></span>

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

<span data-ttu-id="b3e65-119">Аналогичным образом, так как псевдоним для CompanyName не определен выше, CompanyName необходимо использовать согласованно во всем документе.</span><span class="sxs-lookup"><span data-stu-id="b3e65-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="b3e65-120">Типы данных</span><span class="sxs-lookup"><span data-stu-id="b3e65-120">Data Types</span></span>

<span data-ttu-id="b3e65-121">Тип данных можно применить к столбце с атрибутом **dt:type.**</span><span class="sxs-lookup"><span data-stu-id="b3e65-121">You can apply a data type to a column with the **dt:type** attribute.</span></span> <span data-ttu-id="b3e65-122">Тип данных можно указать двумя способами: укажите атрибут **dt:type** непосредственно в самом определении столбца или используйте конструкцию **s:datatype** в качестве вложенного элемента определения столбца.</span><span class="sxs-lookup"><span data-stu-id="b3e65-122">You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition.</span></span> <span data-ttu-id="b3e65-123">Пример.</span><span class="sxs-lookup"><span data-stu-id="b3e65-123">For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="b3e65-124">эквивалентен</span><span class="sxs-lookup"><span data-stu-id="b3e65-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="b3e65-125">Если опустить атрибут **dt:type** полностью из определения строки, по умолчанию тип столбца будет переменной длиной строки.</span><span class="sxs-lookup"><span data-stu-id="b3e65-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="b3e65-126">Если у вас больше сведений о типе, чем просто имя типа (например, **dt:maxLength),** это делает его более учитаемым для использования **элемента s:datatype.**</span><span class="sxs-lookup"><span data-stu-id="b3e65-126">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element.</span></span> <span data-ttu-id="b3e65-127">Однако это просто соглашение, а не требование.</span><span class="sxs-lookup"><span data-stu-id="b3e65-127">This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="b3e65-128">В следующих примерах покажем, как включить сведения о типе в схему:</span><span class="sxs-lookup"><span data-stu-id="b3e65-128">The following examples show further how to include type information in your schema:</span></span>

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

<span data-ttu-id="b3e65-129">Во втором примере атрибут **rs:fixedlength** используется неявно.</span><span class="sxs-lookup"><span data-stu-id="b3e65-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="b3e65-130">Столбец с **атрибутом rs:fixedlength,** установленным как true, означает, что данные должны иметь длину, определяемую в схеме.</span><span class="sxs-lookup"><span data-stu-id="b3e65-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="b3e65-131">В этом случае юридическим значением для ид заголовка является \_ "123456", как "123."</span><span class="sxs-lookup"><span data-stu-id="b3e65-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="b3e65-132">Однако "123" будет не допустимым, так как его длина составляет 3, а не 6.</span><span class="sxs-lookup"><span data-stu-id="b3e65-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="b3e65-133">Более полное описание свойства **fixedlength** см. в руководстве программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b3e65-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="b3e65-134">Обработка NULL</span><span class="sxs-lookup"><span data-stu-id="b3e65-134">Handling Nulls</span></span>

<span data-ttu-id="b3e65-135">Значения NULL обрабатываются атрибутом **rs:maybenull.**</span><span class="sxs-lookup"><span data-stu-id="b3e65-135">Null values are handled by the **rs:maybenull** attribute.</span></span> <span data-ttu-id="b3e65-136">Если для этого атрибута установлено значение true, содержимое столбца может содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="b3e65-136">If this attribute is set to true, the contents of the column may contain a null value.</span></span> <span data-ttu-id="b3e65-137">Кроме того, если столбец не найден в строке данных, пользователь, считывав данные из наборов строк, получит состояние NULL из **IRowset::GetData()**.</span><span class="sxs-lookup"><span data-stu-id="b3e65-137">Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**.</span></span> <span data-ttu-id="b3e65-138">Рассмотрим следующие определения столбцов из таблицы Shippers:</span><span class="sxs-lookup"><span data-stu-id="b3e65-138">Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="b3e65-139">Определение позволяет companyName иметь значение null, но ShipperID не может содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="b3e65-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="b3e65-140">Если в разделе данных содержится следующая строка, поставщик сохраняемости будет устанавливать состояние данных для столбца CompanyName в константе состояния OLE DB DB DBSTATUS \_ S \_ ISNULL:</span><span class="sxs-lookup"><span data-stu-id="b3e65-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="b3e65-141">Если строка была полностью пустой, то поставщик сохраняемости возвратит состояние OLE DB DB DB \_ \_ UNAVAILABLE для ShipperID и DBSTATUS S ISNULL для \_ \_ CompanyName.</span><span class="sxs-lookup"><span data-stu-id="b3e65-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="b3e65-142">Обратите внимание, что строка нулевой длины не является нулевой.</span><span class="sxs-lookup"><span data-stu-id="b3e65-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="b3e65-143">В предыдущей строке поставщик сохраняемости возвращает состояние OLE DB DB DBSTATUS \_ S \_ OK для обоих столбцов.</span><span class="sxs-lookup"><span data-stu-id="b3e65-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="b3e65-144">В данном случае companyName — это просто "" (строка нулевой длины).</span><span class="sxs-lookup"><span data-stu-id="b3e65-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="b3e65-145">Дополнительные сведения о конструкциях OLE DB, доступных для использования в схеме XML-документа для OLE DB, см. в определении "urn:schemas-microsoft-com:rowset" и руководстве программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b3e65-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>

