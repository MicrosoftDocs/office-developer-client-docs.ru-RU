---
title: Значок элемент (Master_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80061e7d-dbcb-f7a1-b63a-052eee4ec7d7
description: Указывает кодировке MIME (Multipurpose Internet Mail Extensions) двоичные значок (в формате .ico) для шаблона элемента в документе.
ms.openlocfilehash: 80d9089442318c834a9a211941187588359f7041
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395758"
---
# <a name="icon-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="b78e5-103">Значок элемент (Master_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b78e5-103">Icon element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b78e5-104">Указывает кодировке MIME (Multipurpose Internet Mail Extensions) двоичные значок (в формате .ico) для шаблона элемента в документе.</span><span class="sxs-lookup"><span data-stu-id="b78e5-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a Master element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b78e5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b78e5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b78e5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b78e5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b78e5-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="b78e5-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b78e5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b78e5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b78e5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b78e5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b78e5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b78e5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b78e5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b78e5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b78e5-112">Masters.XML</span><span class="sxs-lookup"><span data-stu-id="b78e5-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b78e5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b78e5-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b78e5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b78e5-114">Elements and attributes</span></span>

<span data-ttu-id="b78e5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b78e5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b78e5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b78e5-116">Parent elements</span></span>

|<span data-ttu-id="b78e5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b78e5-117">**Element**</span></span>|<span data-ttu-id="b78e5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b78e5-118">**Type**</span></span>|<span data-ttu-id="b78e5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b78e5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b78e5-120">Master</span><span class="sxs-lookup"><span data-stu-id="b78e5-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b78e5-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="b78e5-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b78e5-122">Задает шаблон документа.</span><span class="sxs-lookup"><span data-stu-id="b78e5-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b78e5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b78e5-123">Child elements</span></span>

<span data-ttu-id="b78e5-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b78e5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b78e5-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b78e5-125">Attributes</span></span>

<span data-ttu-id="b78e5-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="b78e5-126">None.</span></span>
  

