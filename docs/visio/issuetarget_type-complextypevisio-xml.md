---
title: IssueTarget_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393770"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="84012-102">IssueTarget_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="84012-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="84012-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="84012-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84012-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="84012-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="84012-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="84012-105">**Schema file**</span></span> <br/> |<span data-ttu-id="84012-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="84012-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="84012-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="84012-107">**Extension base**</span></span> <br/> |<span data-ttu-id="84012-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="84012-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="84012-109">Определение</span><span class="sxs-lookup"><span data-stu-id="84012-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="84012-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="84012-110">Elements and attributes</span></span>

<span data-ttu-id="84012-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="84012-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="84012-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="84012-112">Child elements</span></span>

<span data-ttu-id="84012-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="84012-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84012-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="84012-114">Attributes</span></span>

|<span data-ttu-id="84012-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="84012-115">**Attribute**</span></span>|<span data-ttu-id="84012-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="84012-116">**Type**</span></span>|<span data-ttu-id="84012-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="84012-117">**Required**</span></span>|<span data-ttu-id="84012-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="84012-118">**Description**</span></span>|<span data-ttu-id="84012-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="84012-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="84012-120">PageID</span><span class="sxs-lookup"><span data-stu-id="84012-120">PageID</span></span>  <br/> |<span data-ttu-id="84012-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="84012-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="84012-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="84012-122">required</span></span>  <br/> ||<span data-ttu-id="84012-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="84012-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="84012-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="84012-124">ShapeID</span></span>  <br/> |<span data-ttu-id="84012-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="84012-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="84012-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="84012-126">required</span></span>  <br/> ||<span data-ttu-id="84012-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="84012-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

