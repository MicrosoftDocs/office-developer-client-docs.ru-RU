---
title: Фиелд_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c346fb8d-f247-4a14-19cd-9368ec86ce3f
ms.openlocfilehash: e67ea9dd5eed1892888ccd59c2ade1d95bd5d79e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542368"
---
# <a name="fieldtype-complextype-visio-xml"></a><span data-ttu-id="ca246-102">Фиелд_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="ca246-102">Field_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ca246-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ca246-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca246-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ca246-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ca246-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ca246-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ca246-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ca246-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ca246-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ca246-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ca246-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="ca246-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca246-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ca246-109">Definition</span></span>

```XML
          <xs:complexType name="Field_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FieldRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca246-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca246-110">Elements and attributes</span></span>

<span data-ttu-id="ca246-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ca246-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ca246-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ca246-112">Child elements</span></span>

|<span data-ttu-id="ca246-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ca246-113">**Element**</span></span>|<span data-ttu-id="ca246-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca246-114">**Type**</span></span>|<span data-ttu-id="ca246-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca246-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca246-116">Row</span><span class="sxs-lookup"><span data-stu-id="ca246-116">Row</span></span>](row-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ca246-117">Фиелдров_типе</span><span class="sxs-lookup"><span data-stu-id="ca246-117">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ca246-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca246-118">Attributes</span></span>

<span data-ttu-id="ca246-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="ca246-119">None.</span></span>
  

