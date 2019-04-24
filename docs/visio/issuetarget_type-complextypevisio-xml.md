---
title: Иссуетаржет_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314926"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="7d592-102">Иссуетаржет_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7d592-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7d592-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7d592-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d592-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7d592-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7d592-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7d592-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7d592-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7d592-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7d592-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7d592-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7d592-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7d592-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d592-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7d592-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7d592-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7d592-110">Elements and attributes</span></span>

<span data-ttu-id="7d592-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7d592-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d592-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7d592-112">Child elements</span></span>

<span data-ttu-id="7d592-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="7d592-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d592-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7d592-114">Attributes</span></span>

|<span data-ttu-id="7d592-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7d592-115">**Attribute**</span></span>|<span data-ttu-id="7d592-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7d592-116">**Type**</span></span>|<span data-ttu-id="7d592-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7d592-117">**Required**</span></span>|<span data-ttu-id="7d592-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7d592-118">**Description**</span></span>|<span data-ttu-id="7d592-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7d592-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d592-120">PageID</span><span class="sxs-lookup"><span data-stu-id="7d592-120">PageID</span></span>  <br/> |<span data-ttu-id="7d592-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="7d592-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d592-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7d592-122">required</span></span>  <br/> ||<span data-ttu-id="7d592-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="7d592-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d592-124">Шапеид</span><span class="sxs-lookup"><span data-stu-id="7d592-124">ShapeID</span></span>  <br/> |<span data-ttu-id="7d592-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="7d592-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d592-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7d592-126">required</span></span>  <br/> ||<span data-ttu-id="7d592-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="7d592-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

