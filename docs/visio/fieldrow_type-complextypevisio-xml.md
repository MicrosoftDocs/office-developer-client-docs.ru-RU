---
title: Фиелдров_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: 5f59ca23fa83d98622624cc20544f9b482ce5378
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322563"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="93a98-102">Фиелдров_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="93a98-102">FieldRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="93a98-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="93a98-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93a98-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="93a98-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="93a98-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="93a98-105">**Schema file**</span></span> <br/> |<span data-ttu-id="93a98-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="93a98-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="93a98-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="93a98-107">**Extension base**</span></span> <br/> |<span data-ttu-id="93a98-108">Индекседров_типе</span><span class="sxs-lookup"><span data-stu-id="93a98-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93a98-109">Определение</span><span class="sxs-lookup"><span data-stu-id="93a98-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="93a98-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="93a98-110">Elements and attributes</span></span>

<span data-ttu-id="93a98-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="93a98-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="93a98-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="93a98-112">Child elements</span></span>

|<span data-ttu-id="93a98-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="93a98-113">**Element**</span></span>|<span data-ttu-id="93a98-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="93a98-114">**Type**</span></span>|<span data-ttu-id="93a98-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93a98-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93a98-116">Cell</span><span class="sxs-lookup"><span data-stu-id="93a98-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="93a98-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="93a98-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="93a98-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="93a98-118">Attributes</span></span>

<span data-ttu-id="93a98-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="93a98-119">None.</span></span>
  

