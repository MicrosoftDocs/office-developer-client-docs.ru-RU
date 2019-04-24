---
title: Раздел Data (Справочник по базам данных Access на компьютере)
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
# <a name="data-section"></a><span data-ttu-id="e69b9-102">Раздел данных</span><span class="sxs-lookup"><span data-stu-id="e69b9-102">Data section</span></span>

<span data-ttu-id="e69b9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e69b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e69b9-104">Раздел Data определяет данные набора строк вместе с ожидающими обновлениями, вставками или удалением.</span><span class="sxs-lookup"><span data-stu-id="e69b9-104">The data section defines the data of the rowset along with any pending updates, insertions, or deletions.</span></span> <span data-ttu-id="e69b9-105">Раздел Data может содержать ноль или более строк.</span><span class="sxs-lookup"><span data-stu-id="e69b9-105">The data section may contain zero or more rows.</span></span> <span data-ttu-id="e69b9-106">Он может содержать только данные из одного набора, где строка определяется схемой.</span><span class="sxs-lookup"><span data-stu-id="e69b9-106">It may only contain data from one rowset where the row is defined by the schema.</span></span> <span data-ttu-id="e69b9-107">Кроме того, как отмечалось ранее, столбцы без данных могут быть опущены.</span><span class="sxs-lookup"><span data-stu-id="e69b9-107">Also, as noted before, columns without any data may be omitted.</span></span> <span data-ttu-id="e69b9-108">Если в разделе данных используется атрибут или подэлемент, и эта конструкция не определена в разделе схемы, она игнорируется без уведомления.</span><span class="sxs-lookup"><span data-stu-id="e69b9-108">If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="e69b9-109">Строка</span><span class="sxs-lookup"><span data-stu-id="e69b9-109">String</span></span>

<span data-ttu-id="e69b9-110">ЗаРезервированные XML-символы в текстовых данных должны быть заменены соответствующими сущностями знаков.</span><span class="sxs-lookup"><span data-stu-id="e69b9-110">Reserved XML characters in text data must be replaced with appropriate character entities.</span></span> <span data-ttu-id="e69b9-111">Например, в названии компании Джо "Джо", символ одинарной кавычки должен быть заменен на сущность.</span><span class="sxs-lookup"><span data-stu-id="e69b9-111">For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity.</span></span> <span data-ttu-id="e69b9-112">Фактическая строка будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e69b9-112">The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="e69b9-113">Следующие символы зарезервированы в XML и должны быть заменены сущностями символов: {",", _Амп_\<,\>,}.</span><span class="sxs-lookup"><span data-stu-id="e69b9-113">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="e69b9-114">Binary</span><span class="sxs-lookup"><span data-stu-id="e69b9-114">Binary</span></span>

<span data-ttu-id="e69b9-115">Двоичные данные имеют кодировку bin. hex (то есть один байт сопоставляется с двумя символами, по одному символу на каждую штуку).</span><span class="sxs-lookup"><span data-stu-id="e69b9-115">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="e69b9-116">DateTime</span><span class="sxs-lookup"><span data-stu-id="e69b9-116">DateTime</span></span>

<span data-ttu-id="e69b9-117">Формат Variant VT\_не поддерживается ТИПАМИ данных XML-данных.</span><span class="sxs-lookup"><span data-stu-id="e69b9-117">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="e69b9-118">Правильный формат для дат с компонентом данных и временем — гггг-мм-дд**T**чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="e69b9-118">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="e69b9-119">Для получения дополнительных сведений о форматах дат, заданных в формате XML, ознакомьтесь со статьей [W3C XMLDATA Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="e69b9-119">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="e69b9-120">Когда спецификация XML-Data определяет два эквивалентных типа данных (например, I4 = = int), ADO записывает понятное имя, но прочитает их в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="e69b9-120">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="e69b9-121">Управление ожидающими изменениями</span><span class="sxs-lookup"><span data-stu-id="e69b9-121">Managing pending changes</span></span>

<span data-ttu-id="e69b9-122">Объект **Recordset** можно открыть в режиме немедленных или пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="e69b9-122">A **Recordset** can be opened in immediate or batch update mode.</span></span> <span data-ttu-id="e69b9-123">При открытии в режиме пакетного обновления с клиентскими курсорами все изменения, внесенные в **набор записей** , находятся в состоянии ожидания, пока не будет вызван метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="e69b9-123">When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called.</span></span> <span data-ttu-id="e69b9-124">Ожидающие изменения также сохраняются при сохранении объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="e69b9-124">Pending changes are also persisted when the **Recordset** is saved.</span></span> <span data-ttu-id="e69b9-125">В XML они представлены с помощью элементов "Update", определенных в urn: schemas-microsoft-com: Rowset.</span><span class="sxs-lookup"><span data-stu-id="e69b9-125">In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="e69b9-126">Кроме того, если набор строк можно обновить, свойство с возможностью обновления должно иметь значение true в определении строки.</span><span class="sxs-lookup"><span data-stu-id="e69b9-126">In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row.</span></span> <span data-ttu-id="e69b9-127">Например, чтобы определить, что таблица грузоотправителей содержит ожидающие изменения, определение строки будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e69b9-127">For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="e69b9-128">При этом поставщик сохраняемости покажет данные, чтобы ADO мог создать обновляемый объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="e69b9-128">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="e69b9-129">В следующих примерах данных показано, как при вставке, изменении и удалении отображаются в материализованном файле:</span><span class="sxs-lookup"><span data-stu-id="e69b9-129">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

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

<span data-ttu-id="e69b9-130">Обновление всегда содержит данные исходной строки целиком, за которыми следуют измененные данные строки.</span><span class="sxs-lookup"><span data-stu-id="e69b9-130">An update always contains the entire original row data followed by the changed row data.</span></span> <span data-ttu-id="e69b9-131">В измененной строке могут содержаться все столбцы или только те столбцы, которые действительно изменились.</span><span class="sxs-lookup"><span data-stu-id="e69b9-131">The changed row may contain all of the columns or only those columns that have actually changed.</span></span> <span data-ttu-id="e69b9-132">В предыдущем примере строка для грузоотправителя 2 не изменяется, а только столбец Phone имеет измененные значения для грузоотправителя 3, и поэтому в измененной строке включен единственный столбец.</span><span class="sxs-lookup"><span data-stu-id="e69b9-132">In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row.</span></span> <span data-ttu-id="e69b9-133">Вставленные строки для грузоотправителей 12, 13 и 14 объединяются в один RS: INSERT Tag.</span><span class="sxs-lookup"><span data-stu-id="e69b9-133">The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag.</span></span> <span data-ttu-id="e69b9-134">Обратите внимание, что удаленные строки также могут быть объединены в пакет, хотя это не показано выше.</span><span class="sxs-lookup"><span data-stu-id="e69b9-134">Note that deleted rows may also be batched together, although this is not shown above.</span></span>

