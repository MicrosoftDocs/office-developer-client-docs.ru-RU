---
title: HeaderMargin_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 2d4a1fb15172d86a7843616679df4177d6f8292b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539091"
---
# <a name="headermargin_type-complextype-visio-xml"></a><span data-ttu-id="f609c-102">HeaderMargin_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="f609c-102">HeaderMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f609c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f609c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f609c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f609c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f609c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f609c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f609c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f609c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f609c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f609c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f609c-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="f609c-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f609c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f609c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f609c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f609c-110">Elements and attributes</span></span>

<span data-ttu-id="f609c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f609c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f609c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f609c-112">Child elements</span></span>

<span data-ttu-id="f609c-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f609c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f609c-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f609c-114">Attributes</span></span>

|<span data-ttu-id="f609c-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f609c-115">**Attribute**</span></span>|<span data-ttu-id="f609c-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f609c-116">**Type**</span></span>|<span data-ttu-id="f609c-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f609c-117">**Required**</span></span>|<span data-ttu-id="f609c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f609c-118">**Description**</span></span>|<span data-ttu-id="f609c-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f609c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f609c-120">Устройств</span><span class="sxs-lookup"><span data-stu-id="f609c-120">Unit</span></span>  <br/> |<span data-ttu-id="f609c-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f609c-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f609c-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="f609c-122">optional</span></span>  <br/> ||<span data-ttu-id="f609c-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f609c-123">Values of the xsd:string type.</span></span>  <br/> |
   

