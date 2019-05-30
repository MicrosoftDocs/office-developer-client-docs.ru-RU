---
title: Валидатионпропертиес_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538517"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="8cd40-102">Валидатионпропертиес_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8cd40-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8cd40-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8cd40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cd40-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8cd40-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8cd40-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8cd40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8cd40-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8cd40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8cd40-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8cd40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8cd40-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8cd40-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8cd40-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8cd40-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8cd40-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8cd40-110">Elements and attributes</span></span>

<span data-ttu-id="8cd40-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8cd40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8cd40-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8cd40-112">Child elements</span></span>

<span data-ttu-id="8cd40-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="8cd40-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8cd40-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8cd40-114">Attributes</span></span>

|<span data-ttu-id="8cd40-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8cd40-115">**Attribute**</span></span>|<span data-ttu-id="8cd40-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8cd40-116">**Type**</span></span>|<span data-ttu-id="8cd40-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8cd40-117">**Required**</span></span>|<span data-ttu-id="8cd40-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8cd40-118">**Description**</span></span>|<span data-ttu-id="8cd40-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8cd40-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8cd40-120">Ластвалидатед</span><span class="sxs-lookup"><span data-stu-id="8cd40-120">LastValidated</span></span>  <br/> |<span data-ttu-id="8cd40-121">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="8cd40-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8cd40-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8cd40-122">required</span></span>  <br/> ||<span data-ttu-id="8cd40-123">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="8cd40-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8cd40-124">Шовигноред</span><span class="sxs-lookup"><span data-stu-id="8cd40-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="8cd40-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="8cd40-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8cd40-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8cd40-126">required</span></span>  <br/> ||<span data-ttu-id="8cd40-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8cd40-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

