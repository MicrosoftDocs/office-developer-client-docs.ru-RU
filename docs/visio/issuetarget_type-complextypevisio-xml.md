---
title: IssueTarget_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: b9e69edc5bd30ede969bc77d43501a4473e9f69e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814001"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="c6ca0-102">IssueTarget_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c6ca0-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c6ca0-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c6ca0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6ca0-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c6ca0-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c6ca0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c6ca0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c6ca0-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c6ca0-108">Нет</span><span class="sxs-lookup"><span data-stu-id="c6ca0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6ca0-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c6ca0-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c6ca0-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6ca0-110">Elements and attributes</span></span>

<span data-ttu-id="c6ca0-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="c6ca0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c6ca0-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c6ca0-112">Child elements</span></span>

<span data-ttu-id="c6ca0-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="c6ca0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6ca0-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6ca0-114">Attributes</span></span>

|<span data-ttu-id="c6ca0-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-115">**Attribute**</span></span>|<span data-ttu-id="c6ca0-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-116">**Type**</span></span>|<span data-ttu-id="c6ca0-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-117">**Required**</span></span>|<span data-ttu-id="c6ca0-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-118">**Description**</span></span>|<span data-ttu-id="c6ca0-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c6ca0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6ca0-120">PageID</span><span class="sxs-lookup"><span data-stu-id="c6ca0-120">PageID</span></span>  <br/> |<span data-ttu-id="c6ca0-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c6ca0-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c6ca0-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c6ca0-122">required</span></span>  <br/> ||<span data-ttu-id="c6ca0-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c6ca0-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c6ca0-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="c6ca0-124">ShapeID</span></span>  <br/> |<span data-ttu-id="c6ca0-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c6ca0-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c6ca0-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c6ca0-126">required</span></span>  <br/> ||<span data-ttu-id="c6ca0-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c6ca0-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

