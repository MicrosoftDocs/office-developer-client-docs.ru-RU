---
title: XML Persistence Format
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7825d55c6f0c2f900f61a325265dce048f965e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308283"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="80dd7-102">Формат сохранения XML</span><span class="sxs-lookup"><span data-stu-id="80dd7-102">XML persistence format</span></span>

<span data-ttu-id="80dd7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80dd7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="80dd7-104">XML Persistence Format</span><span class="sxs-lookup"><span data-stu-id="80dd7-104">XML Persistence Format</span></span>

<span data-ttu-id="80dd7-105">ADO использует кодировку UTF-8 для XML-потока, который он сохраняет.</span><span class="sxs-lookup"><span data-stu-id="80dd7-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="80dd7-106">Формат ADO XML разбивается на два раздела: раздел схемы, за которым следует раздел Data.</span><span class="sxs-lookup"><span data-stu-id="80dd7-106">The ADO XML format is broken into two sections, a schema section followed by the data section.</span></span> <span data-ttu-id="80dd7-107">Ниже приведен пример XML-файла для таблицы грузоотправителей из базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="80dd7-107">The following is an example XML file for the Shippers table from the Northwind database.</span></span> <span data-ttu-id="80dd7-108">В этом примере рассматриваются различные части XML-кода.</span><span class="sxs-lookup"><span data-stu-id="80dd7-108">Various parts of the XML are discussed following the example.</span></span>

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

<span data-ttu-id="80dd7-109">В схеме показаны объявления пространств имен, раздела схемы и раздела данных.</span><span class="sxs-lookup"><span data-stu-id="80dd7-109">The schema shows the declarations of namespaces, the schema section, and the data section.</span></span> <span data-ttu-id="80dd7-110">Раздел Schema содержит определения для строки, Шипперид, CompanyName и телефона.</span><span class="sxs-lookup"><span data-stu-id="80dd7-110">The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="80dd7-111">Определения схемы соответствуют спецификации XML-данных и могут быть полностью проверены (хотя проверка не будет выполняться в Internet Explorer 5).</span><span class="sxs-lookup"><span data-stu-id="80dd7-111">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5).</span></span> <span data-ttu-id="80dd7-112">Эту спецификацию можно просмотреть на странице [W3C по XMLDATA](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="80dd7-112">You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span> <span data-ttu-id="80dd7-113">XML-Data — это единственный поддерживаемый формат схемы для сохраняемого **набора записей** в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="80dd7-113">XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="80dd7-114">Раздел данных содержит три строки, содержащие сведения о грузоотправителях.</span><span class="sxs-lookup"><span data-stu-id="80dd7-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="80dd7-115">Для пустого набора строк раздел Data может быть пустым, но должны присутствовать `<rs:data>` Теги.</span><span class="sxs-lookup"><span data-stu-id="80dd7-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="80dd7-116">Без данных вы можете написать сокращенную форму тега простым `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="80dd7-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="80dd7-117">Любой тег с префиксом RS указывает на то, что он находится в пространстве имен, определенном с помощью параметра urn: schemas-microsoft-com: Rowset.</span><span class="sxs-lookup"><span data-stu-id="80dd7-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="80dd7-118">Полное определение этой схемы определено в приложении в этом документе.</span><span class="sxs-lookup"><span data-stu-id="80dd7-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="80dd7-119">XML Persistence Format</span><span class="sxs-lookup"><span data-stu-id="80dd7-119">XML Persistence Format</span></span>

<span data-ttu-id="80dd7-120">ADO использует кодировку UTF-8 для XML-потока, который он сохраняет.</span><span class="sxs-lookup"><span data-stu-id="80dd7-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="80dd7-121">Формат ADO XML разбивается на два раздела: раздел схемы, за которым следует раздел Data.</span><span class="sxs-lookup"><span data-stu-id="80dd7-121">The ADO XML format is broken into two sections, a schema section followed by the data section.</span></span> <span data-ttu-id="80dd7-122">Ниже приведен пример XML-файла для таблицы грузоотправителей из базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="80dd7-122">The following is an example XML file for the Shippers table from the Northwind database.</span></span> <span data-ttu-id="80dd7-123">В этом примере рассматриваются различные части XML-кода.</span><span class="sxs-lookup"><span data-stu-id="80dd7-123">Various parts of the XML are discussed following the example.</span></span>

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

<span data-ttu-id="80dd7-124">В схеме показаны объявления пространств имен, раздела схемы и раздела данных.</span><span class="sxs-lookup"><span data-stu-id="80dd7-124">The schema shows the declarations of namespaces, the schema section, and the data section.</span></span> <span data-ttu-id="80dd7-125">Раздел Schema содержит определения для строки, Шипперид, CompanyName и телефона.</span><span class="sxs-lookup"><span data-stu-id="80dd7-125">The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="80dd7-126">Определения схемы соответствуют спецификации XML-данных и могут быть полностью проверены (хотя проверка не будет выполняться в Internet Explorer 5).</span><span class="sxs-lookup"><span data-stu-id="80dd7-126">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5).</span></span> <span data-ttu-id="80dd7-127">Эту спецификацию можно просмотреть на странице [W3C по XMLDATA](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="80dd7-127">You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span> <span data-ttu-id="80dd7-128">XML-Data — это единственный поддерживаемый формат схемы для сохраняемого **набора записей** в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="80dd7-128">XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="80dd7-129">Раздел данных содержит три строки, содержащие сведения о грузоотправителях.</span><span class="sxs-lookup"><span data-stu-id="80dd7-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="80dd7-130">Для пустого набора строк раздел Data может быть пустым, но должны присутствовать `<rs:data>` Теги.</span><span class="sxs-lookup"><span data-stu-id="80dd7-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="80dd7-131">Без данных вы можете написать сокращенную форму тега простым `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="80dd7-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="80dd7-132">Любой тег с префиксом RS указывает на то, что он находится в пространстве имен, определенном с помощью параметра urn: schemas-microsoft-com: Rowset.</span><span class="sxs-lookup"><span data-stu-id="80dd7-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="80dd7-133">Полное определение этой схемы определено в приложении в этом документе.</span><span class="sxs-lookup"><span data-stu-id="80dd7-133">The full definition of this schema is defined in the appendix to this document.</span></span>

