---
title: User_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d3970d90-6beb-1f59-256f-ace6a9865b59
ms.openlocfilehash: fcf222d1fe18f4d862ca8ae124d422caf7bdc36d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538573"
---
# <a name="user_type-complextype-visio-xml"></a><span data-ttu-id="e67fe-102">User_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e67fe-102">User_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e67fe-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e67fe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e67fe-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e67fe-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e67fe-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e67fe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e67fe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e67fe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e67fe-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="e67fe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e67fe-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="e67fe-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e67fe-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e67fe-109">Definition</span></span>

```XML
          <xs:complexType name="User_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="UserRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e67fe-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e67fe-110">Elements and attributes</span></span>

<span data-ttu-id="e67fe-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e67fe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e67fe-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e67fe-112">Child elements</span></span>

|<span data-ttu-id="e67fe-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e67fe-113">**Element**</span></span>|<span data-ttu-id="e67fe-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e67fe-114">**Type**</span></span>|<span data-ttu-id="e67fe-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e67fe-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e67fe-116">Row</span><span class="sxs-lookup"><span data-stu-id="e67fe-116">Row</span></span>](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e67fe-117">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="e67fe-117">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e67fe-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e67fe-118">Attributes</span></span>

<span data-ttu-id="e67fe-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="e67fe-119">None.</span></span>
  

