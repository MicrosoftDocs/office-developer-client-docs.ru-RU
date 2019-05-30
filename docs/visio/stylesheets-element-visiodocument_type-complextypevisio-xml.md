---
title: Элемент StyleSheets (Висиодокумент_типе complexType) (XML для Visio)
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
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="801ae-103">Элемент StyleSheets (Висиодокумент_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="801ae-103">StyleSheets element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="801ae-104">Содержит коллекцию элементов StyleSheet для документа.</span><span class="sxs-lookup"><span data-stu-id="801ae-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="801ae-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="801ae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="801ae-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="801ae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="801ae-107">Стилешитс_типе</span><span class="sxs-lookup"><span data-stu-id="801ae-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="801ae-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="801ae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="801ae-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="801ae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="801ae-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="801ae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="801ae-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="801ae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="801ae-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="801ae-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="801ae-113">Определение</span><span class="sxs-lookup"><span data-stu-id="801ae-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="801ae-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="801ae-114">Elements and attributes</span></span>

<span data-ttu-id="801ae-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="801ae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="801ae-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="801ae-116">Parent elements</span></span>

|<span data-ttu-id="801ae-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="801ae-117">**Element**</span></span>|<span data-ttu-id="801ae-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="801ae-118">**Type**</span></span>|<span data-ttu-id="801ae-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="801ae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="801ae-120">Висиодокумент</span><span class="sxs-lookup"><span data-stu-id="801ae-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="801ae-121">Висиодокумент_типе</span><span class="sxs-lookup"><span data-stu-id="801ae-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="801ae-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="801ae-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="801ae-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="801ae-123">Child elements</span></span>

|<span data-ttu-id="801ae-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="801ae-124">**Element**</span></span>|<span data-ttu-id="801ae-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="801ae-125">**Type**</span></span>|<span data-ttu-id="801ae-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="801ae-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="801ae-127">Применение</span><span class="sxs-lookup"><span data-stu-id="801ae-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="801ae-128">Стилешит_типе</span><span class="sxs-lookup"><span data-stu-id="801ae-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="801ae-129">Представляет стиль, определенный в документе.</span><span class="sxs-lookup"><span data-stu-id="801ae-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="801ae-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="801ae-130">Attributes</span></span>

<span data-ttu-id="801ae-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="801ae-131">None.</span></span>
  

