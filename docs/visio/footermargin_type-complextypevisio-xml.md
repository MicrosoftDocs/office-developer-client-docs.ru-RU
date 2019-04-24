---
title: Футермаргин_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346048"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="4a6ba-102">Футермаргин_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4a6ba-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4a6ba-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4a6ba-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a6ba-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4a6ba-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4a6ba-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4a6ba-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4a6ba-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4a6ba-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="4a6ba-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a6ba-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4a6ba-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4a6ba-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4a6ba-110">Elements and attributes</span></span>

<span data-ttu-id="4a6ba-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4a6ba-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4a6ba-112">Child elements</span></span>

<span data-ttu-id="4a6ba-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a6ba-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4a6ba-114">Attributes</span></span>

|<span data-ttu-id="4a6ba-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-115">**Attribute**</span></span>|<span data-ttu-id="4a6ba-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-116">**Type**</span></span>|<span data-ttu-id="4a6ba-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-117">**Required**</span></span>|<span data-ttu-id="4a6ba-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-118">**Description**</span></span>|<span data-ttu-id="4a6ba-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4a6ba-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a6ba-120">Устройств</span><span class="sxs-lookup"><span data-stu-id="4a6ba-120">Unit</span></span>  <br/> |<span data-ttu-id="4a6ba-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4a6ba-121">xsd:string</span></span>  <br/> |<span data-ttu-id="4a6ba-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="4a6ba-122">optional</span></span>  <br/> ||<span data-ttu-id="4a6ba-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-123">Values of the xsd:string type.</span></span>  <br/> |
   

