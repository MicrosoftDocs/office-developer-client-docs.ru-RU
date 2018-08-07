---
title: HeaderMargin_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 70b16680446af8973605d24f41b69778a1ec2c2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813902"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="24074-102">HeaderMargin_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="24074-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="24074-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="24074-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24074-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="24074-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="24074-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="24074-105">**Schema file**</span></span> <br/> |<span data-ttu-id="24074-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="24074-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="24074-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="24074-107">**Extension base**</span></span> <br/> |<span data-ttu-id="24074-108">XSD: double</span><span class="sxs-lookup"><span data-stu-id="24074-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24074-109">Определение</span><span class="sxs-lookup"><span data-stu-id="24074-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24074-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="24074-110">Elements and attributes</span></span>

<span data-ttu-id="24074-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="24074-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="24074-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="24074-112">Child elements</span></span>

<span data-ttu-id="24074-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="24074-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24074-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="24074-114">Attributes</span></span>

|<span data-ttu-id="24074-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="24074-115">**Attribute**</span></span>|<span data-ttu-id="24074-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="24074-116">**Type**</span></span>|<span data-ttu-id="24074-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="24074-117">**Required**</span></span>|<span data-ttu-id="24074-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24074-118">**Description**</span></span>|<span data-ttu-id="24074-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="24074-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="24074-120">Подразделения</span><span class="sxs-lookup"><span data-stu-id="24074-120">Unit</span></span>  <br/> |<span data-ttu-id="24074-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="24074-121">xsd:string</span></span>  <br/> |<span data-ttu-id="24074-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="24074-122">optional</span></span>  <br/> ||<span data-ttu-id="24074-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="24074-123">Values of the xsd:string type.</span></span>  <br/> |
   

