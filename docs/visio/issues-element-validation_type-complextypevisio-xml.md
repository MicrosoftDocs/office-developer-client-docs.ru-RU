---
title: Элемент проблемы (Validation_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Содержит все элементы проблему для документа.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400581"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="d623a-103">Элемент проблемы (Validation_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d623a-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d623a-104">Содержит все элементы проблему для документа.</span><span class="sxs-lookup"><span data-stu-id="d623a-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d623a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d623a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d623a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d623a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d623a-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="d623a-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d623a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d623a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d623a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d623a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d623a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d623a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d623a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d623a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d623a-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="d623a-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d623a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d623a-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d623a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d623a-114">Elements and attributes</span></span>

<span data-ttu-id="d623a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d623a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d623a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d623a-116">Parent elements</span></span>

|<span data-ttu-id="d623a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d623a-117">**Element**</span></span>|<span data-ttu-id="d623a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d623a-118">**Type**</span></span>|<span data-ttu-id="d623a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d623a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d623a-120">Проверка</span><span class="sxs-lookup"><span data-stu-id="d623a-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="d623a-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="d623a-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d623a-122">Сохранение информации о проверки схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="d623a-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d623a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d623a-123">Child elements</span></span>

|<span data-ttu-id="d623a-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d623a-124">**Element**</span></span>|<span data-ttu-id="d623a-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d623a-125">**Type**</span></span>|<span data-ttu-id="d623a-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d623a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d623a-127">Проблема</span><span class="sxs-lookup"><span data-stu-id="d623a-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d623a-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="d623a-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d623a-129">Представляет ошибки проверки одного документа.</span><span class="sxs-lookup"><span data-stu-id="d623a-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d623a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d623a-130">Attributes</span></span>

<span data-ttu-id="d623a-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="d623a-131">None.</span></span>
  

