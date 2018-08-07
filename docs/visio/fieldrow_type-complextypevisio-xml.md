---
title: FieldRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: c0b3dab3cf173db65f0408a2142309d1679f5104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813729"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="36beb-102">FieldRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="36beb-102">FieldRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="36beb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="36beb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36beb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="36beb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36beb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="36beb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36beb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36beb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36beb-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="36beb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36beb-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="36beb-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36beb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="36beb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="36beb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="36beb-110">Elements and attributes</span></span>

<span data-ttu-id="36beb-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="36beb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36beb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36beb-112">Child elements</span></span>

|<span data-ttu-id="36beb-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="36beb-113">**Element**</span></span>|<span data-ttu-id="36beb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="36beb-114">**Type**</span></span>|<span data-ttu-id="36beb-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36beb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36beb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="36beb-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="36beb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="36beb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36beb-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36beb-118">Attributes</span></span>

<span data-ttu-id="36beb-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="36beb-119">None.</span></span>
  

