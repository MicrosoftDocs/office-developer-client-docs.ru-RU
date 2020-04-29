---
title: RefreshConflict_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542830"
---
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="81f2c-102">RefreshConflict_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="81f2c-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="81f2c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="81f2c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81f2c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="81f2c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="81f2c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="81f2c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="81f2c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="81f2c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="81f2c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="81f2c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="81f2c-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="81f2c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81f2c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="81f2c-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="81f2c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="81f2c-110">Elements and attributes</span></span>

<span data-ttu-id="81f2c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="81f2c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="81f2c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="81f2c-112">Child elements</span></span>

<span data-ttu-id="81f2c-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="81f2c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81f2c-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="81f2c-114">Attributes</span></span>

|<span data-ttu-id="81f2c-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="81f2c-115">**Attribute**</span></span>|<span data-ttu-id="81f2c-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="81f2c-116">**Type**</span></span>|<span data-ttu-id="81f2c-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="81f2c-117">**Required**</span></span>|<span data-ttu-id="81f2c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81f2c-118">**Description**</span></span>|<span data-ttu-id="81f2c-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="81f2c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="81f2c-120">PageID</span><span class="sxs-lookup"><span data-stu-id="81f2c-120">PageID</span></span>  <br/> |<span data-ttu-id="81f2c-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="81f2c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81f2c-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="81f2c-122">required</span></span>  <br/> ||<span data-ttu-id="81f2c-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="81f2c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="81f2c-124">RowID</span><span class="sxs-lookup"><span data-stu-id="81f2c-124">RowID</span></span>  <br/> |<span data-ttu-id="81f2c-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="81f2c-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81f2c-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="81f2c-126">required</span></span>  <br/> ||<span data-ttu-id="81f2c-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="81f2c-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="81f2c-128">шапеид</span><span class="sxs-lookup"><span data-stu-id="81f2c-128">ShapeID</span></span>  <br/> |<span data-ttu-id="81f2c-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="81f2c-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81f2c-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="81f2c-130">required</span></span>  <br/> ||<span data-ttu-id="81f2c-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="81f2c-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

