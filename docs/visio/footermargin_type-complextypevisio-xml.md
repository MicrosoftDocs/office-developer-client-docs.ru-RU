---
title: FooterMargin_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398936"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="1a160-102">FooterMargin_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1a160-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1a160-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1a160-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a160-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1a160-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1a160-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1a160-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1a160-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1a160-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1a160-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1a160-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1a160-108">XSD: double</span><span class="sxs-lookup"><span data-stu-id="1a160-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a160-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1a160-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1a160-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1a160-110">Elements and attributes</span></span>

<span data-ttu-id="1a160-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1a160-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1a160-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1a160-112">Child elements</span></span>

<span data-ttu-id="1a160-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="1a160-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a160-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1a160-114">Attributes</span></span>

|<span data-ttu-id="1a160-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1a160-115">**Attribute**</span></span>|<span data-ttu-id="1a160-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1a160-116">**Type**</span></span>|<span data-ttu-id="1a160-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1a160-117">**Required**</span></span>|<span data-ttu-id="1a160-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1a160-118">**Description**</span></span>|<span data-ttu-id="1a160-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1a160-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1a160-120">Подразделения</span><span class="sxs-lookup"><span data-stu-id="1a160-120">Unit</span></span>  <br/> |<span data-ttu-id="1a160-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1a160-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1a160-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="1a160-122">optional</span></span>  <br/> ||<span data-ttu-id="1a160-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1a160-123">Values of the xsd:string type.</span></span>  <br/> |
   

