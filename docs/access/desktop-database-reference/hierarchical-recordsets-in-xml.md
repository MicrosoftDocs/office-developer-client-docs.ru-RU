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
# <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="07310-102">Иерархические наборы записей в XML</span><span class="sxs-lookup"><span data-stu-id="07310-102">Hierarchical Recordsets in XML</span></span>


<span data-ttu-id="07310-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07310-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="07310-104">Иерархические наборы записей в XML</span><span class="sxs-lookup"><span data-stu-id="07310-104">Hierarchical Recordsets in XML</span></span>

<span data-ttu-id="07310-105">ADO разрешает сохранение иерархических объектов **Recordset** в XML.</span><span class="sxs-lookup"><span data-stu-id="07310-105">ADO allows persistence of hierarchical **Recordset** objects into XML.</span></span> <span data-ttu-id="07310-106">В иерархических объектах **Recordset** значением поля в родительском **наборе записей** является другой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="07310-106">With hierarchical **Recordset** objects, the value of a field in the parent **Recordset** is another **Recordset**.</span></span> <span data-ttu-id="07310-107">Такие поля представлены как дочерние элементы в потоке XML, а не в атрибуте.</span><span class="sxs-lookup"><span data-stu-id="07310-107">Such fields are represented as child elements in the XML stream rather than an attribute.</span></span> <span data-ttu-id="07310-108">В следующем примере демонстрируется такой сценарий:</span><span class="sxs-lookup"><span data-stu-id="07310-108">The following example demonstrates this case:</span></span>

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

<span data-ttu-id="07310-109">Ниже приведен XML-формат материализованного объекта **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="07310-109">The following is the XML format of the persisted **Recordset**:</span></span>

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

<span data-ttu-id="07310-110">Точный порядок столбцов в родительском **наборе записей** не очевидно, если он сохраняется таким образом.</span><span class="sxs-lookup"><span data-stu-id="07310-110">The exact order of the columns in the parent **Recordset** is not obvious when it is persisted in this manner.</span></span> <span data-ttu-id="07310-111">Любое поле в родительском объекте может содержать дочерний **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="07310-111">Any field in the parent may contain a child **Recordset**.</span></span> <span data-ttu-id="07310-112">Поставщик сохраняемости сохраняет все скалярные столбцы первыми как атрибуты, а затем сохраняет все дочерние элементы \*\*\*\* "Columns" в качестве дочерних элементов родительской строки.</span><span class="sxs-lookup"><span data-stu-id="07310-112">The Persistence Provider persists out all scalar columns first as attributes and then persists out all child **Recordset** "columns" as child elements of the parent row.</span></span> <span data-ttu-id="07310-113">Порядковый номер поля в родительском наборе **записей** можно получить, изучив определение схемы **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="07310-113">The ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset**.</span></span> <span data-ttu-id="07310-114">Каждое поле имеет свойство OLE DB, **RS: Number**, определенное в пространстве имен схемы **набора записей** , которое содержит порядковый номер для этого поля.</span><span class="sxs-lookup"><span data-stu-id="07310-114">Every field has an OLE DB property, **rs:number**, defined in the **Recordset** schema namespace that contains the ordinal number for that field.</span></span>

<span data-ttu-id="07310-115">Имена всех полей в дочернем **наборе записей** сцепляются с именем поля в родительском объекте **Recordset** , содержащем этот дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="07310-115">The names of all fields in the child **Recordset** are concatenated with the name of the field in the parent **Recordset** that contains this child.</span></span> <span data-ttu-id="07310-116">Это необходимо для того, чтобы избежать конфликтов имен в случаях, когда родительские и дочерние **наборы записей** содержат поле, полученное из двух разных таблиц, но с именем в единственном числе.</span><span class="sxs-lookup"><span data-stu-id="07310-116">This is to ensure that there are no name collisions in cases where parent and child **Recordsets** both contain a field that is obtained from two different tables but is named singularly.</span></span>

<span data-ttu-id="07310-117">При сохранении иерархических **наборов записей** в XML следует учитывать следующие ограничения в ADO:</span><span class="sxs-lookup"><span data-stu-id="07310-117">When saving hierarchical **Recordsets** into XML, you should be aware of the following restrictions in ADO:</span></span>

  - <span data-ttu-id="07310-118">Иерархический **набор записей** с ожидающими обновлениями невозможно хранить в XML.</span><span class="sxs-lookup"><span data-stu-id="07310-118">A hierarchical **Recordset** with pending updates cannot be persisted into XML.</span></span>

  - <span data-ttu-id="07310-119">Иерархический **набор записей** , созданный с помощью команды параметризованной фигуры, не может быть PERSISTED (в формате XML или адтг).</span><span class="sxs-lookup"><span data-stu-id="07310-119">A hierarchical **Recordset** created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</span></span>

  - <span data-ttu-id="07310-120">В настоящее время ADO сохраняет отношение между родительским и дочерним **наборАми записей** в виде больших двоичных объектов (BLOB).</span><span class="sxs-lookup"><span data-stu-id="07310-120">ADO currently saves the relationship between the parent and the child **Recordsets** as a binary large object (BLOB).</span></span> <span data-ttu-id="07310-121">Теги XML для описания этого отношения еще не определены в пространстве имен схемы набора строк.</span><span class="sxs-lookup"><span data-stu-id="07310-121">XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</span></span>

  - <span data-ttu-id="07310-122">При сохранении иерархического **набора** записей все доЧерние **наборы записей** сохраняются вместе с ним.</span><span class="sxs-lookup"><span data-stu-id="07310-122">When a hierarchical **Recordset** is saved, all child **Recordsets** are saved along with it.</span></span> <span data-ttu-id="07310-123">Если текущий **набор записей** является дочерним для другого объекта **Recordset**, его родительский элемент не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="07310-123">If the current **Recordset** is a child of another **Recordset**, its parent is not saved.</span></span> <span data-ttu-id="07310-124">Все дочерние **наборы записей** , которые формируют поддерево текущего **набора записей** , сохраняются.</span><span class="sxs-lookup"><span data-stu-id="07310-124">All child **Recordsets** that form the subtree of the current **Recordset** are saved.</span></span>

<span data-ttu-id="07310-125">При повторном открытии иерархического **набора записей** из XML-сохранения формата необходимо учитывать следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="07310-125">When a hierarchical **Recordset** is reopened from its XML-persisted format, you must be aware of the following limitations:</span></span>

  - <span data-ttu-id="07310-126">Если дочерняя запись содержит записи, для которых нет соответствующих родительских записей, эти строки не записываются в XML-представление иерархического объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="07310-126">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical **Recordset**.</span></span> <span data-ttu-id="07310-127">Таким образом, эти строки будут потеряны при повторном открытии **набора записей** из материализованного места.</span><span class="sxs-lookup"><span data-stu-id="07310-127">Thus, these rows will be lost when the **Recordset** is reopened from its persisted location.</span></span>

  - <span data-ttu-id="07310-128">Если дочерняя запись содержит ссылки на несколько родительских записей, то при повторном открытии **набора записей**доЧерний **набор записей** может содержать повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="07310-128">If a child record has references to more than one parent record, then on reopening the **Recordset**, the child **Recordset** may contain duplicate records.</span></span> <span data-ttu-id="07310-129">Однако эти дубликаты будут видны только в том случае, если пользователь работает непосредственно с базовым дочерним набором строк.</span><span class="sxs-lookup"><span data-stu-id="07310-129">However, these duplicates will only be visible if the user works directly with the underlying child rowset.</span></span> <span data-ttu-id="07310-130">Если для навигации по дочернему набору **записей** используется глава (единственный способ навигации по ADO), дубликаты не отображаются.</span><span class="sxs-lookup"><span data-stu-id="07310-130">If a chapter is used to navigate the child **Recordset** (that is the only way to navigate through ADO), the duplicates are not visible.</span></span>

