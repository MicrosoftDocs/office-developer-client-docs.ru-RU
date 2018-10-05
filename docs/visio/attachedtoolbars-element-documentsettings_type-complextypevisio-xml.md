---
title: Элемент AttachedToolbars (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cd7d8a06-5661-d515-f106-ff8275a04f40
description: Microsoft Visio пользовательского интерфейса (VSU) файл представляющие настраиваемые панели инструментов в кодировке MIME (Multipurpose Internet Mail Extensions).
ms.openlocfilehash: a769204c7e13bacc147689803b31bf898e6de71a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388464"
---
# <a name="attachedtoolbars-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="f9fc9-103">Элемент AttachedToolbars (DocumentSettings_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f9fc9-103">AttachedToolbars element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f9fc9-104">Microsoft Visio пользовательского интерфейса (VSU) файл представляющие настраиваемые панели инструментов в кодировке MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="f9fc9-104">A MIME (Multipurpose Internet Mail Extensions) encoded Microsoft Visio user interface (VSU) file representing custom toolbars.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9fc9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f9fc9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9fc9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f9fc9-107">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="f9fc9-107">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f9fc9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f9fc9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f9fc9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f9fc9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f9fc9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f9fc9-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="f9fc9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9fc9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f9fc9-113">Definition</span></span>

```XML
< xs:element name="AttachedToolbars" type="AttachedToolbars_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f9fc9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f9fc9-114">Elements and attributes</span></span>

<span data-ttu-id="f9fc9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f9fc9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f9fc9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f9fc9-116">Parent elements</span></span>

|<span data-ttu-id="f9fc9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-117">**Element**</span></span>|<span data-ttu-id="f9fc9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-118">**Type**</span></span>|<span data-ttu-id="f9fc9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f9fc9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9fc9-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="f9fc9-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f9fc9-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f9fc9-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f9fc9-122">Содержит элементы, которые определяют параметры документов.</span><span class="sxs-lookup"><span data-stu-id="f9fc9-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f9fc9-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f9fc9-123">Child elements</span></span>

<span data-ttu-id="f9fc9-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="f9fc9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9fc9-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f9fc9-125">Attributes</span></span>

<span data-ttu-id="f9fc9-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="f9fc9-126">None.</span></span>
  

