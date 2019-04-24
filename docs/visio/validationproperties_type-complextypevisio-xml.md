---
title: Валидатионпропертиес_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355981"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="525c4-102">Валидатионпропертиес_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="525c4-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="525c4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="525c4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="525c4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="525c4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="525c4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="525c4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="525c4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="525c4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="525c4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="525c4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="525c4-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="525c4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="525c4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="525c4-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="525c4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="525c4-110">Elements and attributes</span></span>

<span data-ttu-id="525c4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="525c4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="525c4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="525c4-112">Child elements</span></span>

<span data-ttu-id="525c4-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="525c4-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="525c4-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="525c4-114">Attributes</span></span>

|<span data-ttu-id="525c4-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="525c4-115">**Attribute**</span></span>|<span data-ttu-id="525c4-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="525c4-116">**Type**</span></span>|<span data-ttu-id="525c4-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="525c4-117">**Required**</span></span>|<span data-ttu-id="525c4-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="525c4-118">**Description**</span></span>|<span data-ttu-id="525c4-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="525c4-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="525c4-120">Ластвалидатед</span><span class="sxs-lookup"><span data-stu-id="525c4-120">LastValidated</span></span>  <br/> |<span data-ttu-id="525c4-121">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="525c4-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="525c4-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="525c4-122">required</span></span>  <br/> ||<span data-ttu-id="525c4-123">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="525c4-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="525c4-124">Шовигноред</span><span class="sxs-lookup"><span data-stu-id="525c4-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="525c4-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="525c4-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="525c4-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="525c4-126">required</span></span>  <br/> ||<span data-ttu-id="525c4-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="525c4-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

