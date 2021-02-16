---
title: Элемент StyleSheets (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Содержит коллекцию элементов StyleSheet для документа.
ms.openlocfilehash: 363cb102fb545ffd20601bf0125c22aeb06defa8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541990"
---
# <a name="stylesheets-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="0763c-103">Элемент StyleSheets (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0763c-103">StyleSheets element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0763c-104">Содержит коллекцию элементов StyleSheet для документа.</span><span class="sxs-lookup"><span data-stu-id="0763c-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0763c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0763c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0763c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0763c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0763c-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="0763c-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0763c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0763c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0763c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0763c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0763c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0763c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0763c-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="0763c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0763c-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="0763c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0763c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="0763c-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0763c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0763c-114">Elements and attributes</span></span>

<span data-ttu-id="0763c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0763c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0763c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0763c-116">Parent elements</span></span>

|<span data-ttu-id="0763c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0763c-117">**Element**</span></span>|<span data-ttu-id="0763c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0763c-118">**Type**</span></span>|<span data-ttu-id="0763c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0763c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0763c-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="0763c-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="0763c-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="0763c-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0763c-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="0763c-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0763c-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0763c-123">Child elements</span></span>

|<span data-ttu-id="0763c-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0763c-124">**Element**</span></span>|<span data-ttu-id="0763c-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0763c-125">**Type**</span></span>|<span data-ttu-id="0763c-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0763c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0763c-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="0763c-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0763c-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0763c-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0763c-129">Представляет стиль, определенный в документе.</span><span class="sxs-lookup"><span data-stu-id="0763c-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0763c-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0763c-130">Attributes</span></span>

<span data-ttu-id="0763c-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="0763c-131">None.</span></span>
  

