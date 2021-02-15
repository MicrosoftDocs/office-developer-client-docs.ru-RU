---
title: Иерархические наборы записей в XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0aafaa1f7f49d34d647ec0f733e68de21cb5369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292015"
---
# <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="245a1-102">Иерархические наборы записей в XML</span><span class="sxs-lookup"><span data-stu-id="245a1-102">Hierarchical Recordsets in XML</span></span>


<span data-ttu-id="245a1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="245a1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="245a1-104">Иерархические наборы записей в XML</span><span class="sxs-lookup"><span data-stu-id="245a1-104">Hierarchical Recordsets in XML</span></span>

<span data-ttu-id="245a1-105">ADO позволяет сохранять иерархические объекты **Recordset** в XML.</span><span class="sxs-lookup"><span data-stu-id="245a1-105">ADO allows persistence of hierarchical **Recordset** objects into XML.</span></span> <span data-ttu-id="245a1-106">При иерархических **объектах Recordset** значение поля в родительском наборе **записей является** другим **объектом Recordset.**</span><span class="sxs-lookup"><span data-stu-id="245a1-106">With hierarchical **Recordset** objects, the value of a field in the parent **Recordset** is another **Recordset**.</span></span> <span data-ttu-id="245a1-107">Такие поля представлены в потоке XML в качестве не атрибута, а в качестве элементов.</span><span class="sxs-lookup"><span data-stu-id="245a1-107">Such fields are represented as child elements in the XML stream rather than an attribute.</span></span> <span data-ttu-id="245a1-108">Этот пример демонстрируется в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="245a1-108">The following example demonstrates this case:</span></span>

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

<span data-ttu-id="245a1-109">Ниже приводится формат XML сохраняемого **наборов записей:**</span><span class="sxs-lookup"><span data-stu-id="245a1-109">The following is the XML format of the persisted **Recordset**:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

<span data-ttu-id="245a1-110">Точный порядок столбцов в родительском наборе **записей** не является очевидным, если он сохраняется таким образом.</span><span class="sxs-lookup"><span data-stu-id="245a1-110">The exact order of the columns in the parent **Recordset** is not obvious when it is persisted in this manner.</span></span> <span data-ttu-id="245a1-111">Любое поле в родительском может содержать набор **записей.**</span><span class="sxs-lookup"><span data-stu-id="245a1-111">Any field in the parent may contain a child **Recordset**.</span></span> <span data-ttu-id="245a1-112">Поставщик сохраняемости сначала сохраняет все скалярные столбцы в  качестве атрибутов, а затем сохраняет все "столбцы" наборов записей в качестве элементов родительской строки.</span><span class="sxs-lookup"><span data-stu-id="245a1-112">The Persistence Provider persists out all scalar columns first as attributes and then persists out all child **Recordset** "columns" as child elements of the parent row.</span></span> <span data-ttu-id="245a1-113">Порядковую позицию поля в  родительском наборе записей можно получить, изсмотрев определение схемы **для recordset.**</span><span class="sxs-lookup"><span data-stu-id="245a1-113">The ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset**.</span></span> <span data-ttu-id="245a1-114">Каждое поле имеет свойство OLE DB **rs:number,** определенное в пространстве имен схемы **Recordset,** которое содержит порядковые номера для этого поля.</span><span class="sxs-lookup"><span data-stu-id="245a1-114">Every field has an OLE DB property, **rs:number**, defined in the **Recordset** schema namespace that contains the ordinal number for that field.</span></span>

<span data-ttu-id="245a1-115">Имена всех полей в  этом наборе записей совмещены  с именем поля в родительском наборе записей, который содержит этот child.</span><span class="sxs-lookup"><span data-stu-id="245a1-115">The names of all fields in the child **Recordset** are concatenated with the name of the field in the parent **Recordset** that contains this child.</span></span> <span data-ttu-id="245a1-116">Это гарантирует отсутствие столкновений имен в случаях, когда  родительский и родительский записи содержат поле, полученное из двух разных таблиц, но именуется в единственном числе.</span><span class="sxs-lookup"><span data-stu-id="245a1-116">This is to ensure that there are no name collisions in cases where parent and child **Recordsets** both contain a field that is obtained from two different tables but is named singularly.</span></span>

<span data-ttu-id="245a1-117">При сохранении иерархических **записей** в XML следует учитывать следующие ограничения в ADO:</span><span class="sxs-lookup"><span data-stu-id="245a1-117">When saving hierarchical **Recordsets** into XML, you should be aware of the following restrictions in ADO:</span></span>

  - <span data-ttu-id="245a1-118">Иерархический набор **записей с** ожидающих обновлений нельзя сохранить в XML.</span><span class="sxs-lookup"><span data-stu-id="245a1-118">A hierarchical **Recordset** with pending updates cannot be persisted into XML.</span></span>

  - <span data-ttu-id="245a1-119">Иерархический набор **записей,** созданный с помощью параметризованной команды фигуры, нельзя сохранить (в формате XML или ADTG).</span><span class="sxs-lookup"><span data-stu-id="245a1-119">A hierarchical **Recordset** created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</span></span>

  - <span data-ttu-id="245a1-120">В настоящее время ADO сохраняет отношение между родительским и потомком **Recordsets** как большой двоичный объект (BLOB).</span><span class="sxs-lookup"><span data-stu-id="245a1-120">ADO currently saves the relationship between the parent and the child **Recordsets** as a binary large object (BLOB).</span></span> <span data-ttu-id="245a1-121">XML-теги для описания этой связи еще не определены в пространстве имен схемы наборов строк.</span><span class="sxs-lookup"><span data-stu-id="245a1-121">XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</span></span>

  - <span data-ttu-id="245a1-122">При сохранении иерархического **наборов** записей вместе с ним сохраняются все его наборы записей. </span><span class="sxs-lookup"><span data-stu-id="245a1-122">When a hierarchical **Recordset** is saved, all child **Recordsets** are saved along with it.</span></span> <span data-ttu-id="245a1-123">Если текущий **набор записей является** child of another **Recordset,** его родительский набор не будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="245a1-123">If the current **Recordset** is a child of another **Recordset**, its parent is not saved.</span></span> <span data-ttu-id="245a1-124">Сохраняются **все наборы записей,** которые формируют подпотее текущего **наборов** записей.</span><span class="sxs-lookup"><span data-stu-id="245a1-124">All child **Recordsets** that form the subtree of the current **Recordset** are saved.</span></span>

<span data-ttu-id="245a1-125">При повторном **повторном** открытие иерархического наборов записей из формата, сохраняемого в XML, необходимо помнить о следующих ограничениях:</span><span class="sxs-lookup"><span data-stu-id="245a1-125">When a hierarchical **Recordset** is reopened from its XML-persisted format, you must be aware of the following limitations:</span></span>

  - <span data-ttu-id="245a1-126">Если родительская запись содержит записи, для которых нет соответствующих родительских записей, эти строки не записываюются в XML-представлении иерархического **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="245a1-126">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical **Recordset**.</span></span> <span data-ttu-id="245a1-127">Таким образом, эти строки будут потеряны при повторном повторном открытие **наборе записей** из его сохраняемой области.</span><span class="sxs-lookup"><span data-stu-id="245a1-127">Thus, these rows will be lost when the **Recordset** is reopened from its persisted location.</span></span>

  - <span data-ttu-id="245a1-128">Если у родительской записи есть ссылки на несколько родительских записей, то при повторном подмножество записей может содержать повторяющиеся записи. </span><span class="sxs-lookup"><span data-stu-id="245a1-128">If a child record has references to more than one parent record, then on reopening the **Recordset**, the child **Recordset** may contain duplicate records.</span></span> <span data-ttu-id="245a1-129">Однако эти дубликаты будут видны только в том случае, если пользователь работает непосредственно с этим набором строк.</span><span class="sxs-lookup"><span data-stu-id="245a1-129">However, these duplicates will only be visible if the user works directly with the underlying child rowset.</span></span> <span data-ttu-id="245a1-130">Если для навигации по  набору записей (единственный способ навигации по ADO) используется глава, дубликаты не видны.</span><span class="sxs-lookup"><span data-stu-id="245a1-130">If a chapter is used to navigate the child **Recordset** (that is the only way to navigate through ADO), the duplicates are not visible.</span></span>

