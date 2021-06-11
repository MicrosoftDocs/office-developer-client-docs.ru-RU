---
title: IssueTarget_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: 38c73e54ff75e94468cfb95258f1fde510d8019a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542144"
---
# <a name="issuetarget_type-complextype-visio-xml"></a><span data-ttu-id="de5f6-102">IssueTarget_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="de5f6-102">IssueTarget_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="de5f6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="de5f6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de5f6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="de5f6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="de5f6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="de5f6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="de5f6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="de5f6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="de5f6-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="de5f6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="de5f6-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="de5f6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="de5f6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="de5f6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="de5f6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="de5f6-110">Elements and attributes</span></span>

<span data-ttu-id="de5f6-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="de5f6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="de5f6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="de5f6-112">Child elements</span></span>

<span data-ttu-id="de5f6-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="de5f6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de5f6-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="de5f6-114">Attributes</span></span>

|<span data-ttu-id="de5f6-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="de5f6-115">**Attribute**</span></span>|<span data-ttu-id="de5f6-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="de5f6-116">**Type**</span></span>|<span data-ttu-id="de5f6-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="de5f6-117">**Required**</span></span>|<span data-ttu-id="de5f6-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de5f6-118">**Description**</span></span>|<span data-ttu-id="de5f6-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="de5f6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="de5f6-120">PageID</span><span class="sxs-lookup"><span data-stu-id="de5f6-120">PageID</span></span>  <br/> |<span data-ttu-id="de5f6-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="de5f6-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="de5f6-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="de5f6-122">required</span></span>  <br/> ||<span data-ttu-id="de5f6-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="de5f6-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="de5f6-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="de5f6-124">ShapeID</span></span>  <br/> |<span data-ttu-id="de5f6-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="de5f6-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="de5f6-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="de5f6-126">required</span></span>  <br/> ||<span data-ttu-id="de5f6-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="de5f6-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

