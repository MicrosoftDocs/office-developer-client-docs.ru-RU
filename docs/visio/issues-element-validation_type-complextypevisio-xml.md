---
title: Элемент "проблемы" (Валидатион_типе complexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Содержит все элементы Issue для документа.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339489"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="fc80b-103">Элемент "проблемы" (Валидатион_типе complexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="fc80b-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fc80b-104">Содержит все элементы Issue для документа.</span><span class="sxs-lookup"><span data-stu-id="fc80b-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc80b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fc80b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc80b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="fc80b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fc80b-107">Иссуес_типе</span><span class="sxs-lookup"><span data-stu-id="fc80b-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fc80b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fc80b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fc80b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fc80b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fc80b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fc80b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fc80b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="fc80b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fc80b-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="fc80b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc80b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="fc80b-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc80b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fc80b-114">Elements and attributes</span></span>

<span data-ttu-id="fc80b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fc80b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fc80b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fc80b-116">Parent elements</span></span>

|<span data-ttu-id="fc80b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fc80b-117">**Element**</span></span>|<span data-ttu-id="fc80b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fc80b-118">**Type**</span></span>|<span data-ttu-id="fc80b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc80b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc80b-120">Validation</span><span class="sxs-lookup"><span data-stu-id="fc80b-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="fc80b-121">Валидатион_типе</span><span class="sxs-lookup"><span data-stu-id="fc80b-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fc80b-122">Сохраняет сведения о проверке схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="fc80b-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fc80b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fc80b-123">Child elements</span></span>

|<span data-ttu-id="fc80b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fc80b-124">**Element**</span></span>|<span data-ttu-id="fc80b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fc80b-125">**Type**</span></span>|<span data-ttu-id="fc80b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc80b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc80b-127">Проблема</span><span class="sxs-lookup"><span data-stu-id="fc80b-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fc80b-128">Иссуе_типе</span><span class="sxs-lookup"><span data-stu-id="fc80b-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fc80b-129">Представляет одну ошибку проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="fc80b-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fc80b-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fc80b-130">Attributes</span></span>

<span data-ttu-id="fc80b-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="fc80b-131">None.</span></span>
  

