---
title: Формат сохранения XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 201ea2b46ad2bb08e631882cebd5419b6b301179
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867750"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="9eda4-102">Формат сохранения XML</span><span class="sxs-lookup"><span data-stu-id="9eda4-102">XML Persistence Format</span></span>

<span data-ttu-id="9eda4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9eda4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="9eda4-104">Формат сохранения XML</span><span class="sxs-lookup"><span data-stu-id="9eda4-104">XML Persistence Format</span></span>

<span data-ttu-id="9eda4-105">В ADO используется кодировка UTF-8 для потока XML, который она повторяется.</span><span class="sxs-lookup"><span data-stu-id="9eda4-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="9eda4-106">Формат ADO XML разбивается на два раздела, раздел схемы, а затем в разделе данных.</span><span class="sxs-lookup"><span data-stu-id="9eda4-106">The ADO XML format is broken into two sections, a schema section followed by the data section.</span></span> <span data-ttu-id="9eda4-107">Ниже приведен пример XML-файла в таблице «Поставщики» из базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="9eda4-107">The following is an example XML file for the Shippers table from the Northwind database.</span></span> <span data-ttu-id="9eda4-108">Различные части XML-код, обсуждаются в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9eda4-108">Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="9eda4-109">Схема показано объявление пространства имен, в разделе схемы и в разделе данных.</span><span class="sxs-lookup"><span data-stu-id="9eda4-109">The schema shows the declarations of namespaces, the schema section, and the data section.</span></span> <span data-ttu-id="9eda4-110">В разделе схема содержит определения для строки, ShipperID, название организации и телефон.</span><span class="sxs-lookup"><span data-stu-id="9eda4-110">The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="9eda4-111">Определения схемы соответствуют спецификации XML-данных и могут быть полностью Подтверждено (Хотя проверка не будет выполнена в Internet Explorer 5).</span><span class="sxs-lookup"><span data-stu-id="9eda4-111">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5).</span></span> <span data-ttu-id="9eda4-112">Можно просматривать спецификация [W3C XMLData Примечание](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="9eda4-112">You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span> <span data-ttu-id="9eda4-113">XML-данных в настоящее время является формат только поддерживаемые схемы для сохранения **записей** .</span><span class="sxs-lookup"><span data-stu-id="9eda4-113">XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="9eda4-114">В разделе данных имеет три строки, содержащие сведения о них.</span><span class="sxs-lookup"><span data-stu-id="9eda4-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="9eda4-115">Для пустой набор строк, в разделе данных может быть пустым, но `<rs:data>` теги, должно быть установлено.</span><span class="sxs-lookup"><span data-stu-id="9eda4-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="9eda4-116">Без данных можно написать сокращение тег просто `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="9eda4-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="9eda4-117">Любой тег начинаются с «rs» указывает, что в пространстве имен, определенные в urn: schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="9eda4-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="9eda4-118">Полное определение схемы определяется в приложении к этому документу.</span><span class="sxs-lookup"><span data-stu-id="9eda4-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="9eda4-119">Формат сохранения XML</span><span class="sxs-lookup"><span data-stu-id="9eda4-119">XML Persistence Format</span></span>

<span data-ttu-id="9eda4-120">В ADO используется кодировка UTF-8 для потока XML, который она повторяется.</span><span class="sxs-lookup"><span data-stu-id="9eda4-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="9eda4-121">Формат ADO XML разбивается на два раздела, раздел схемы, а затем в разделе данных.</span><span class="sxs-lookup"><span data-stu-id="9eda4-121">The ADO XML format is broken into two sections, a schema section followed by the data section.</span></span> <span data-ttu-id="9eda4-122">Ниже приведен пример XML-файла в таблице «Поставщики» из базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="9eda4-122">The following is an example XML file for the Shippers table from the Northwind database.</span></span> <span data-ttu-id="9eda4-123">Различные части XML-код, обсуждаются в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9eda4-123">Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="9eda4-124">Схема показано объявление пространства имен, в разделе схемы и в разделе данных.</span><span class="sxs-lookup"><span data-stu-id="9eda4-124">The schema shows the declarations of namespaces, the schema section, and the data section.</span></span> <span data-ttu-id="9eda4-125">В разделе схема содержит определения для строки, ShipperID, название организации и телефон.</span><span class="sxs-lookup"><span data-stu-id="9eda4-125">The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="9eda4-126">Определения схемы соответствуют спецификации XML-данных и могут быть полностью Подтверждено (Хотя проверка не будет выполнена в Internet Explorer 5).</span><span class="sxs-lookup"><span data-stu-id="9eda4-126">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5).</span></span> <span data-ttu-id="9eda4-127">Можно просматривать спецификация [W3C XMLData Примечание](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="9eda4-127">You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span> <span data-ttu-id="9eda4-128">XML-данных в настоящее время является формат только поддерживаемые схемы для сохранения **записей** .</span><span class="sxs-lookup"><span data-stu-id="9eda4-128">XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="9eda4-129">В разделе данных имеет три строки, содержащие сведения о них.</span><span class="sxs-lookup"><span data-stu-id="9eda4-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="9eda4-130">Для пустой набор строк, в разделе данных может быть пустым, но `<rs:data>` теги, должно быть установлено.</span><span class="sxs-lookup"><span data-stu-id="9eda4-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="9eda4-131">Без данных можно написать сокращение тег просто `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="9eda4-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="9eda4-132">Любой тег начинаются с «rs» указывает, что в пространстве имен, определенные в urn: schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="9eda4-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="9eda4-133">Полное определение схемы определяется в приложении к этому документу.</span><span class="sxs-lookup"><span data-stu-id="9eda4-133">The full definition of this schema is defined in the appendix to this document.</span></span>

