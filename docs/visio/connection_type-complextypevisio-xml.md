---
title: Коннектион_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: a63f3b22dc7020cd25326fc24ae5cb770f23285b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319609"
---
# <a name="connectiontype-complextype-visio-xml"></a><span data-ttu-id="71802-102">Коннектион_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="71802-102">Connection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="71802-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="71802-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71802-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="71802-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="71802-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="71802-105">**Schema file**</span></span> <br/> |<span data-ttu-id="71802-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="71802-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="71802-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="71802-107">**Extension base**</span></span> <br/> |<span data-ttu-id="71802-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="71802-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71802-109">Определение</span><span class="sxs-lookup"><span data-stu-id="71802-109">Definition</span></span>

```XML
          <xs:complexType name="Connection_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ConnectionRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="71802-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="71802-110">Elements and attributes</span></span>

<span data-ttu-id="71802-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="71802-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="71802-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="71802-112">Child elements</span></span>

|<span data-ttu-id="71802-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="71802-113">**Element**</span></span>|<span data-ttu-id="71802-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="71802-114">**Type**</span></span>|<span data-ttu-id="71802-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71802-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71802-116">Row</span><span class="sxs-lookup"><span data-stu-id="71802-116">Row</span></span>](row-element-connection-sectionvisio-xml.md) <br/> |[<span data-ttu-id="71802-117">Коннектионров_типе</span><span class="sxs-lookup"><span data-stu-id="71802-117">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="71802-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="71802-118">Attributes</span></span>

<span data-ttu-id="71802-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="71802-119">None.</span></span>
  

