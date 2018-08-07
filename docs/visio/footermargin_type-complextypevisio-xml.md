---
title: FooterMargin_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f2cfa7c9d27940308c95318f8a743a4bdd6cb45f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813815"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="fb4af-102">FooterMargin_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="fb4af-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fb4af-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="fb4af-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb4af-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fb4af-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fb4af-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fb4af-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fb4af-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fb4af-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fb4af-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="fb4af-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fb4af-108">XSD: double</span><span class="sxs-lookup"><span data-stu-id="fb4af-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb4af-109">Определение</span><span class="sxs-lookup"><span data-stu-id="fb4af-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fb4af-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fb4af-110">Elements and attributes</span></span>

<span data-ttu-id="fb4af-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="fb4af-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fb4af-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fb4af-112">Child elements</span></span>

<span data-ttu-id="fb4af-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="fb4af-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb4af-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fb4af-114">Attributes</span></span>

|<span data-ttu-id="fb4af-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fb4af-115">**Attribute**</span></span>|<span data-ttu-id="fb4af-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fb4af-116">**Type**</span></span>|<span data-ttu-id="fb4af-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="fb4af-117">**Required**</span></span>|<span data-ttu-id="fb4af-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fb4af-118">**Description**</span></span>|<span data-ttu-id="fb4af-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fb4af-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb4af-120">Подразделения</span><span class="sxs-lookup"><span data-stu-id="fb4af-120">Unit</span></span>  <br/> |<span data-ttu-id="fb4af-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="fb4af-121">xsd:string</span></span>  <br/> |<span data-ttu-id="fb4af-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="fb4af-122">optional</span></span>  <br/> ||<span data-ttu-id="fb4af-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fb4af-123">Values of the xsd:string type.</span></span>  <br/> |
   

