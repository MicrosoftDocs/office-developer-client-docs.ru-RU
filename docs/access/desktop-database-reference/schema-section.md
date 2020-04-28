---
title: Раздел Schema (Справочник по базам данных Access на компьютере)
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
# <a name="schema-section"></a><span data-ttu-id="2371f-102">Раздел схемы</span><span class="sxs-lookup"><span data-stu-id="2371f-102">Schema section</span></span>

<span data-ttu-id="2371f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2371f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="2371f-104">Schema Section</span><span class="sxs-lookup"><span data-stu-id="2371f-104">Schema Section</span></span>

<span data-ttu-id="2371f-105">Раздел схемы является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2371f-105">The schema section is required.</span></span> <span data-ttu-id="2371f-106">Как показано в предыдущем примере, ADO записывает подробные метаданные для каждого столбца, чтобы сохранить семантику значений данных, насколько это возможно для обновления.</span><span class="sxs-lookup"><span data-stu-id="2371f-106">As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating.</span></span> <span data-ttu-id="2371f-107">Однако для загрузки в XML для ADO требуются только имена столбцов и набор строк, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="2371f-107">However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong.</span></span> <span data-ttu-id="2371f-108">Ниже приведен пример минимальной схемы:</span><span class="sxs-lookup"><span data-stu-id="2371f-108">Here is an example of a minimal schema:</span></span>

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

<span data-ttu-id="2371f-109">В вышеприведенном случае ADO будет рассматривать данные как строки переменной длины, так как в схему не включены сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="2371f-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="2371f-110">Создание псевдонимов для имен столбцов</span><span class="sxs-lookup"><span data-stu-id="2371f-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="2371f-111">Атрибут **RS: Name** позволяет создать псевдоним для имени столбца, чтобы понятное имя отображалось в сведениях о столбцах, предоставляемых набором строк, и в разделе Data можно использовать более короткое имя.</span><span class="sxs-lookup"><span data-stu-id="2371f-111">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section.</span></span> <span data-ttu-id="2371f-112">Например, приведенная выше схема может быть изменена для сопоставления Шипперид с S1, CompanyName — S2, а телефон — для S3 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2371f-112">For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

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

<span data-ttu-id="2371f-113">Затем в разделе Data строка будет использовать атрибут **Name** (не **RS: Name**), чтобы ссылаться на этот столбец:</span><span class="sxs-lookup"><span data-stu-id="2371f-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="2371f-114">Создание псевдонимов для имен столбцов является обязательным, если имя столбца не является допустимым атрибутом или именем тега в XML.</span><span class="sxs-lookup"><span data-stu-id="2371f-114">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML.</span></span> <span data-ttu-id="2371f-115">Например, "Last Name" должен иметь псевдоним, так как имена с вложенными пробелами являются недопустимыми атрибутами.</span><span class="sxs-lookup"><span data-stu-id="2371f-115">For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes.</span></span> <span data-ttu-id="2371f-116">Следующая строка не будет правильно обработана средством синтаксического анализа XML, поэтому необходимо создать псевдоним для другого имени, у которого нет внедренного пространства:</span><span class="sxs-lookup"><span data-stu-id="2371f-116">The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="2371f-117">Любое значение, используемое для атрибута **Name** , должно постоянно использоваться в каждой позиции, на которую ссылается столбец, в схеме и в разделах данных XML-документа.</span><span class="sxs-lookup"><span data-stu-id="2371f-117">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document.</span></span> <span data-ttu-id="2371f-118">В следующем примере показано согласованное использование S1:</span><span class="sxs-lookup"><span data-stu-id="2371f-118">The following example shows the consistent use of s1:</span></span>

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

<span data-ttu-id="2371f-119">Аналогично, так как псевдоним для CompanyName не определен, CompanyName должен использоваться единообразно во всем документе.</span><span class="sxs-lookup"><span data-stu-id="2371f-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="2371f-120">Типы данных</span><span class="sxs-lookup"><span data-stu-id="2371f-120">Data Types</span></span>

<span data-ttu-id="2371f-121">Вы можете применить тип данных к столбцу с атрибутом **DT: Type** .</span><span class="sxs-lookup"><span data-stu-id="2371f-121">You can apply a data type to a column with the **dt:type** attribute.</span></span> <span data-ttu-id="2371f-122">Вы можете указать тип данных двумя способами: либо укажите атрибут **DT: Type** непосредственно в самом определении столбца, либо используйте конструкцию **с:дататипе** в качестве вложенного элемента определения столбца.</span><span class="sxs-lookup"><span data-stu-id="2371f-122">You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition.</span></span> <span data-ttu-id="2371f-123">For example,</span><span class="sxs-lookup"><span data-stu-id="2371f-123">For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="2371f-124">эквивалентно</span><span class="sxs-lookup"><span data-stu-id="2371f-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="2371f-125">Если опустить атрибут **DT: Type** полностью из определения строки, то по умолчанию типом столбца будет строка переменной длины.</span><span class="sxs-lookup"><span data-stu-id="2371f-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="2371f-126">Если у вас больше сведений о типе, чем просто имя типа (например, **DT: MaxLength**), то для использования дочернего элемента **с:дататипе** становится более удобочитаемым.</span><span class="sxs-lookup"><span data-stu-id="2371f-126">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element.</span></span> <span data-ttu-id="2371f-127">Тем не менее, это просто соглашение, а не требование.</span><span class="sxs-lookup"><span data-stu-id="2371f-127">This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="2371f-128">В следующих примерах показано, как включить сведения о типах в схему:</span><span class="sxs-lookup"><span data-stu-id="2371f-128">The following examples show further how to include type information in your schema:</span></span>

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

<span data-ttu-id="2371f-129">Во втором примере используется незаметное использование атрибута **RS: фикседленгс** .</span><span class="sxs-lookup"><span data-stu-id="2371f-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="2371f-130">Столбец с атрибутом **RS: фикседленгс** , для которого задано значение true, указывает, что длина данных должна быть определена в схеме.</span><span class="sxs-lookup"><span data-stu-id="2371f-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="2371f-131">В этом случае допустимым значением идентификатора заголовка\_является "123456", как "123".</span><span class="sxs-lookup"><span data-stu-id="2371f-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="2371f-132">Однако "123" не является допустимым, так как его длина равна 3, а не 6.</span><span class="sxs-lookup"><span data-stu-id="2371f-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="2371f-133">Более полное описание свойства **фикседленгс** показано в руководстве программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2371f-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="2371f-134">Обработка значений NULL</span><span class="sxs-lookup"><span data-stu-id="2371f-134">Handling Nulls</span></span>

<span data-ttu-id="2371f-135">Значения NULL обрабатываются атрибутом **RS: майбенулл** .</span><span class="sxs-lookup"><span data-stu-id="2371f-135">Null values are handled by the **rs:maybenull** attribute.</span></span> <span data-ttu-id="2371f-136">Если для этого атрибута задано значение true, то содержимое столбца может содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="2371f-136">If this attribute is set to true, the contents of the column may contain a null value.</span></span> <span data-ttu-id="2371f-137">Кроме того, если столбец не найден в строке данных, то пользователь, считывающий данные из набора строк, будет получать значение NULL из элемента **IRowset:: GetData ()**.</span><span class="sxs-lookup"><span data-stu-id="2371f-137">Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**.</span></span> <span data-ttu-id="2371f-138">Обратите внимание на следующие определения столбцов из таблицы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="2371f-138">Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="2371f-139">Определение разрешает для CompanyName значение null, но Шипперид не может содержать значение null.</span><span class="sxs-lookup"><span data-stu-id="2371f-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="2371f-140">Если раздел Data содержит следующую строку, то поставщик сохраняемости настроил состояние данных для столбца CompanyName на константу состояния OLE DB ДБСТАТУС\_S\_IsNull:</span><span class="sxs-lookup"><span data-stu-id="2371f-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="2371f-141">Если строка была полностью пустой, то поставщик сохраняемости возвратит состояние OLE DB\_дбстатус E\_недоступно для шипперид и Дбстатус\_S\_IsNull для CompanyName.</span><span class="sxs-lookup"><span data-stu-id="2371f-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="2371f-142">Обратите внимание, что строка нулевой длины не совпадает со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="2371f-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="2371f-143">Для предыдущей строки поставщик сохраняемости будет возвращать состояние OLE DB ДБСТАТУС\_S\_ОК для обоих столбцов.</span><span class="sxs-lookup"><span data-stu-id="2371f-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="2371f-144">В этом случае названием CompanyName является просто "" (строка нулевой длины).</span><span class="sxs-lookup"><span data-stu-id="2371f-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="2371f-145">Для получения дополнительных сведений о конструкциях OLE DB, доступных для использования в схеме XML-документа для OLE DB, ознакомьтесь с определением "urn: schemas-microsoft-com: RowSet" и руководством программиста по OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2371f-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>

