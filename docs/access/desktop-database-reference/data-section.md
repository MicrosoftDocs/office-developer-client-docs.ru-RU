---
title: Раздел "Данные" (справочник по базам данных Access для настольных ПК)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b8e3baf4d147edcc739e59933da4697c08cdef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295046"
---
# <a name="data-section"></a><span data-ttu-id="4121e-102">Раздел данных</span><span class="sxs-lookup"><span data-stu-id="4121e-102">Data section</span></span>

<span data-ttu-id="4121e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4121e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4121e-104">В разделе данных определяются данные наборов строк, а также ожидающих обновлений, вставки или удаления.</span><span class="sxs-lookup"><span data-stu-id="4121e-104">The data section defines the data of the rowset along with any pending updates, insertions, or deletions.</span></span> <span data-ttu-id="4121e-105">Раздел данных может содержать ноль или больше строк.</span><span class="sxs-lookup"><span data-stu-id="4121e-105">The data section may contain zero or more rows.</span></span> <span data-ttu-id="4121e-106">Он может содержать данные только из одного ряда строк, в котором строка определена схемой.</span><span class="sxs-lookup"><span data-stu-id="4121e-106">It may only contain data from one rowset where the row is defined by the schema.</span></span> <span data-ttu-id="4121e-107">Кроме того, как было отмечено ранее, столбцы без данных могут быть пропущены.</span><span class="sxs-lookup"><span data-stu-id="4121e-107">Also, as noted before, columns without any data may be omitted.</span></span> <span data-ttu-id="4121e-108">Если атрибут или подэлемент используется в разделе данных и эта конструкция не определена в разделе схемы, она игнорируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="4121e-108">If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="4121e-109">String</span><span class="sxs-lookup"><span data-stu-id="4121e-109">String</span></span>

<span data-ttu-id="4121e-110">Зарезервированные символы XML в текстовых данных должны быть заменены соответствующими сущностями символов.</span><span class="sxs-lookup"><span data-stu-id="4121e-110">Reserved XML characters in text data must be replaced with appropriate character entities.</span></span> <span data-ttu-id="4121e-111">Например, в названии компании "Joe's Garage" один символ кавычка должен быть заменен сущностью.</span><span class="sxs-lookup"><span data-stu-id="4121e-111">For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity.</span></span> <span data-ttu-id="4121e-112">Фактическая строка будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="4121e-112">The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="4121e-113">Следующие символы зарезервированы в XML и должны быть заменены сущностями символов: {',",&, \< \> }.</span><span class="sxs-lookup"><span data-stu-id="4121e-113">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="4121e-114">Binary</span><span class="sxs-lookup"><span data-stu-id="4121e-114">Binary</span></span>

<span data-ttu-id="4121e-115">Двоичные данные закодированы в двоичном коде bin.hex (то есть один byte соподержется с двумя символами, по одному символу на каждый прихожий).</span><span class="sxs-lookup"><span data-stu-id="4121e-115">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="4121e-116">DateTime</span><span class="sxs-lookup"><span data-stu-id="4121e-116">DateTime</span></span>

<span data-ttu-id="4121e-117">Формат VT DATE варианта не поддерживается \_ напрямую XML-Data типами данных.</span><span class="sxs-lookup"><span data-stu-id="4121e-117">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="4121e-118">Правильный формат дат с компонентом данных и времени — yyyy-mm-dd **T** чч:мм:сс.</span><span class="sxs-lookup"><span data-stu-id="4121e-118">The correct format for dates with both a data and time component is yyyy-mm-dd **T** hh:mm:ss.</span></span>

<span data-ttu-id="4121e-119">Дополнительные сведения о форматах дат, указанных в XML, см. в заметке [W3C XMLData.](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)</span><span class="sxs-lookup"><span data-stu-id="4121e-119">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="4121e-120">Если спецификация XML-Data определяет два эквивалентных типа данных (например, i4 == int), ADO запишет удобное имя, но прочитает оба.</span><span class="sxs-lookup"><span data-stu-id="4121e-120">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="4121e-121">Управление ожидающие изменения</span><span class="sxs-lookup"><span data-stu-id="4121e-121">Managing pending changes</span></span>

<span data-ttu-id="4121e-122">Набор **записей можно** открыть в режиме немедленного или пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="4121e-122">A **Recordset** can be opened in immediate or batch update mode.</span></span> <span data-ttu-id="4121e-123">При отложенном режиме пакетного обновления с помощью клиентских курсоров все изменения, внесенные в **набор записей,** находятся в состоянии ожидания до тех пор, пока не будет вызван метод **UpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="4121e-123">When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called.</span></span> <span data-ttu-id="4121e-124">Ожидающих изменений также сохраняются при **сохраняемом наборе** записей.</span><span class="sxs-lookup"><span data-stu-id="4121e-124">Pending changes are also persisted when the **Recordset** is saved.</span></span> <span data-ttu-id="4121e-125">В XML они представлены использованием элементов "update", определенных в urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="4121e-125">In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="4121e-126">Кроме того, если можно обновить набор строк, для обновляемого свойства должно быть установлено true в определении строки.</span><span class="sxs-lookup"><span data-stu-id="4121e-126">In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row.</span></span> <span data-ttu-id="4121e-127">Например, чтобы определить, что таблица Shippers содержит ожидающих изменений, определение строки будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4121e-127">For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="4121e-128">Это сообщает поставщику сохраняемости для передачи данных, чтобы ADO можно было создать updatable **объект Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4121e-128">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="4121e-129">В следующих примерах данных показано, как вставки, изменения и удаления выглядят в файле сохраняемом файле:</span><span class="sxs-lookup"><span data-stu-id="4121e-129">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

```xml 
<rs:data> 
  <z:row ShipperID="2" CompanyName="United Package"  
    Phone="(503) 555-3199"/> 
<rs:update> 
  <rs:original> 
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/> 
  </rs:original> 
  <z:row Phone="(503) 552-7134"/> 
</rs:update> 
<rs:insert> 
  <z:row ShipperID="12" CompanyName="Lightning Shipping"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="13" CompanyName="Thunder Overnight"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="14" CompanyName="Blue Angel Air Delivery"  
    Phone="(505) 111-2222"/> 
</rs:insert> 
<rs:delete> 
  <z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/> 
</rs:delete> 
</rs:data> 
```

<span data-ttu-id="4121e-130">Обновление всегда содержит все исходные данные строки, за которыми следуют измененные данные строки.</span><span class="sxs-lookup"><span data-stu-id="4121e-130">An update always contains the entire original row data followed by the changed row data.</span></span> <span data-ttu-id="4121e-131">Измененная строка может содержать все столбцы или только те столбцы, которые были фактически изменены.</span><span class="sxs-lookup"><span data-stu-id="4121e-131">The changed row may contain all of the columns or only those columns that have actually changed.</span></span> <span data-ttu-id="4121e-132">В предыдущем примере строка для Shipper 2 не меняется, тогда как только столбец Phone изменил значения для Shipper 3 и поэтому является единственным столбцом, включенным в измененную строку.</span><span class="sxs-lookup"><span data-stu-id="4121e-132">In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row.</span></span> <span data-ttu-id="4121e-133">Вставленные строки для shippers 12, 13 и 14 объединяется в один тег rs:insert.</span><span class="sxs-lookup"><span data-stu-id="4121e-133">The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag.</span></span> <span data-ttu-id="4121e-134">Обратите внимание, что удаленные строки также могут быть вместе, хотя это не показано выше.</span><span class="sxs-lookup"><span data-stu-id="4121e-134">Note that deleted rows may also be batched together, although this is not shown above.</span></span>

