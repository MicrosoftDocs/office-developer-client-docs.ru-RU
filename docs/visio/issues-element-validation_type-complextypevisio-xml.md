---
title: Элемент Issues (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Содержит все элементы Issue для документа.
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542942"
---
# <a name="issues-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="b8c92-103">Элемент Issues (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b8c92-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b8c92-104">Содержит все элементы Issue для документа.</span><span class="sxs-lookup"><span data-stu-id="b8c92-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8c92-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b8c92-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8c92-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b8c92-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b8c92-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b8c92-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b8c92-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b8c92-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b8c92-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b8c92-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b8c92-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b8c92-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b8c92-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b8c92-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b8c92-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="b8c92-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8c92-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b8c92-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b8c92-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b8c92-114">Elements and attributes</span></span>

<span data-ttu-id="b8c92-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b8c92-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b8c92-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b8c92-116">Parent elements</span></span>

|<span data-ttu-id="b8c92-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b8c92-117">**Element**</span></span>|<span data-ttu-id="b8c92-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b8c92-118">**Type**</span></span>|<span data-ttu-id="b8c92-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8c92-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8c92-120">Validation</span><span class="sxs-lookup"><span data-stu-id="b8c92-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="b8c92-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="b8c92-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8c92-122">Хранит сведения о проверке схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="b8c92-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b8c92-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b8c92-123">Child elements</span></span>

|<span data-ttu-id="b8c92-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b8c92-124">**Element**</span></span>|<span data-ttu-id="b8c92-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b8c92-125">**Type**</span></span>|<span data-ttu-id="b8c92-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8c92-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8c92-127">Проблема</span><span class="sxs-lookup"><span data-stu-id="b8c92-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8c92-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="b8c92-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8c92-129">Представляет одну проблему проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="b8c92-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b8c92-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b8c92-130">Attributes</span></span>

<span data-ttu-id="b8c92-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="b8c92-131">None.</span></span>
  

