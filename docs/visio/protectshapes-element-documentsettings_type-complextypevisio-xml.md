---
title: Элемент Протектшапес (Документсеттингс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e3835fc6-0ae6-b8c3-b1d0-bf893d4a9470
description: Указывает, запрещается ли пользователю выбирать фигуры, для которых для элемента LockSelect задано значение 1.
ms.openlocfilehash: 9f7910123c00a8fd4f5ce47ef099c8c6581f8c07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346804"
---
# <a name="protectshapes-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="c9977-103">Элемент Протектшапес (Документсеттингс_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c9977-103">ProtectShapes element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c9977-104">Указывает, запрещается ли пользователю выбирать фигуры, для которых для элемента **LockSelect** задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="c9977-104">Specifies whether the user is prevented from selecting shapes that have their **LockSelect** element set to 1.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c9977-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c9977-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9977-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c9977-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c9977-107">Протектшапес_типе</span><span class="sxs-lookup"><span data-stu-id="c9977-107">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c9977-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c9977-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c9977-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c9977-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c9977-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c9977-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c9977-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c9977-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c9977-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="c9977-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9977-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c9977-113">Definition</span></span>

```XML
< xs:element name="ProtectShapes" type="ProtectShapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c9977-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c9977-114">Elements and attributes</span></span>

<span data-ttu-id="c9977-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c9977-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c9977-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c9977-116">Parent elements</span></span>

|<span data-ttu-id="c9977-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c9977-117">**Element**</span></span>|<span data-ttu-id="c9977-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c9977-118">**Type**</span></span>|<span data-ttu-id="c9977-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c9977-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c9977-120">Документсеттингс</span><span class="sxs-lookup"><span data-stu-id="c9977-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9977-121">Документсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="c9977-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c9977-122">Содержит элементы, определяющие параметры документа.</span><span class="sxs-lookup"><span data-stu-id="c9977-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c9977-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c9977-123">Child elements</span></span>

<span data-ttu-id="c9977-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="c9977-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9977-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c9977-125">Attributes</span></span>

<span data-ttu-id="c9977-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="c9977-126">None.</span></span>
  

