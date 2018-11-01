---
title: Раздел данных (Справочник по для настольных баз данных Access)
TOCTitle: Data Section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74406232a6f7d458eebb242f3f341bd4e3ccc583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882856"
---
# <a name="data-section"></a><span data-ttu-id="780af-102">Раздел данных</span><span class="sxs-lookup"><span data-stu-id="780af-102">Data Section</span></span>

<span data-ttu-id="780af-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="780af-103">**Applies to**: Access 2013, Office 2013</span></span>
 
## <a name="data-section"></a><span data-ttu-id="780af-104">Раздел данных</span><span class="sxs-lookup"><span data-stu-id="780af-104">Data Section</span></span>

<span data-ttu-id="780af-105">В разделе данных определяет данных набор строк, а также все ожидающие обновления, вставка или удаление.</span><span class="sxs-lookup"><span data-stu-id="780af-105">The data section defines the data of the rowset along with any pending updates, insertions, or deletions.</span></span> <span data-ttu-id="780af-106">В разделе данных может содержать ноль или несколько строк.</span><span class="sxs-lookup"><span data-stu-id="780af-106">The data section may contain zero or more rows.</span></span> <span data-ttu-id="780af-107">Он может содержать только данные из один набор строк, где строка определяется в схеме.</span><span class="sxs-lookup"><span data-stu-id="780af-107">It may only contain data from one rowset where the row is defined by the schema.</span></span> <span data-ttu-id="780af-108">Кроме того как было отмечено ранее, можно опустить столбцы данных.</span><span class="sxs-lookup"><span data-stu-id="780af-108">Also, as noted before, columns without any data may be omitted.</span></span> <span data-ttu-id="780af-109">Если атрибут или вложенный элемент используется в разделе данные и этой конструкции не было определено в разделе схемы, он игнорируется без уведомления.</span><span class="sxs-lookup"><span data-stu-id="780af-109">If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="780af-110">Строка</span><span class="sxs-lookup"><span data-stu-id="780af-110">String</span></span>

<span data-ttu-id="780af-111">Зарезервированные символы XML в текстовых данных должно быть заменено сущности знаков.</span><span class="sxs-lookup"><span data-stu-id="780af-111">Reserved XML characters in text data must be replaced with appropriate character entities.</span></span> <span data-ttu-id="780af-112">Например в поле имя компании «Джо видео» символов одинарные кавычки необходимо заменить сущности.</span><span class="sxs-lookup"><span data-stu-id="780af-112">For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity.</span></span> <span data-ttu-id="780af-113">Фактические строки будет иметь вид:</span><span class="sxs-lookup"><span data-stu-id="780af-113">The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="780af-114">Следующие символы зарезервированы в формате XML и должен быть заменен сущности знаков: {",» &,\<,\>}.</span><span class="sxs-lookup"><span data-stu-id="780af-114">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="780af-115">Двоичный</span><span class="sxs-lookup"><span data-stu-id="780af-115">Binary</span></span>

<span data-ttu-id="780af-116">Двоичные данные — bin.hex кодировке (то есть, сопоставляется один байт два символов, один символ в каждом байта).</span><span class="sxs-lookup"><span data-stu-id="780af-116">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="780af-117">DateTime</span><span class="sxs-lookup"><span data-stu-id="780af-117">DateTime</span></span>

<span data-ttu-id="780af-118">Тип variant VT\_формат даты не поддерживается напрямую с типами данных XML-данных.</span><span class="sxs-lookup"><span data-stu-id="780af-118">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="780af-119">Правильный формат даты, времени и данные компонента: гггг мм дд чч**T**.</span><span class="sxs-lookup"><span data-stu-id="780af-119">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="780af-120">Дополнительные сведения о форматах даты, указанного идентификатором XML можно [W3C XMLData Примечание](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="780af-120">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="780af-121">Когда спецификации XML-данных определяет два типа данных (например, i4 == int), ADO будет записывать понятное имя, но чтение в обоих.</span><span class="sxs-lookup"><span data-stu-id="780af-121">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="780af-122">Управление ожидающих изменений</span><span class="sxs-lookup"><span data-stu-id="780af-122">Managing Pending Changes</span></span>

<span data-ttu-id="780af-123">**Набор записей** можно открыть в интерпретации или режим пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="780af-123">A **Recordset** can be opened in immediate or batch update mode.</span></span> <span data-ttu-id="780af-124">При открытии в режим пакета обновления с помощью записей на стороне клиента, все изменения, внесенные в **набор записей** , в состоянии ожидания, пока не будет вызван метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="780af-124">When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called.</span></span> <span data-ttu-id="780af-125">Ожидающие изменения, также сохраняются при сохранении **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="780af-125">Pending changes are also persisted when the **Recordset** is saved.</span></span> <span data-ttu-id="780af-126">В XML, они представлены в виде использования «обновления» элементы, определенные в urn: schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="780af-126">In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="780af-127">Кроме того, если набор строк могут быть обновлены, обновляемое свойство должно быть присвоено значение true, если в определении строки.</span><span class="sxs-lookup"><span data-stu-id="780af-127">In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row.</span></span> <span data-ttu-id="780af-128">Например чтобы определить, что в таблице «Поставщики» содержит ожидающих изменений, определение строки будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="780af-128">For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="780af-129">Это указывает поставщика службы сохранения для предоставления данных, чтобы ADO можно создать обновляемый объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="780af-129">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="780af-130">Следующие примеры данных приведен пример добавления, изменения и удаления в файле постоянных:</span><span class="sxs-lookup"><span data-stu-id="780af-130">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

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

<span data-ttu-id="780af-131">Обновление всегда содержит всю строку данные исходного и измененной строки данных.</span><span class="sxs-lookup"><span data-stu-id="780af-131">An update always contains the entire original row data followed by the changed row data.</span></span> <span data-ttu-id="780af-132">Измененная строка может содержать все столбцы или только столбцы, которые фактически были изменены.</span><span class="sxs-lookup"><span data-stu-id="780af-132">The changed row may contain all of the columns or only those columns that have actually changed.</span></span> <span data-ttu-id="780af-133">В предыдущем примере строка для доставки 2 не изменяется, пока только столбец телефона был изменен значений для отправителя 3, поэтому оно только столбец, включенный в измененной строки.</span><span class="sxs-lookup"><span data-stu-id="780af-133">In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row.</span></span> <span data-ttu-id="780af-134">Вставка строк для поставщиков 12, 13 и 14 являются пакетной вместе в рамках одного rs: Вставка тега.</span><span class="sxs-lookup"><span data-stu-id="780af-134">The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag.</span></span> <span data-ttu-id="780af-135">Обратите внимание на то, что удаленных строк может также быть группировать, хотя это не показано выше.</span><span class="sxs-lookup"><span data-stu-id="780af-135">Note that deleted rows may also be batched together, although this is not shown above.</span></span>

