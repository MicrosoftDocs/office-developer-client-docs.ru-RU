---
title: Элемент ProtectBkgnds (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99b7d89e-b482-ef19-1683-667095f8114a
description: Указывает, не мешает ли пользователю удалять или изменять фоновые страницы.
ms.openlocfilehash: b053eca7b669b60bedd34bc4a6798f9b9182b529
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540751"
---
# <a name="protectbkgnds-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="4c55c-103">Элемент ProtectBkgnds (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4c55c-103">ProtectBkgnds element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4c55c-104">Указывает, не мешает ли пользователю удалять или изменять фоновые страницы.</span><span class="sxs-lookup"><span data-stu-id="4c55c-104">Specifies whether the user is prevented from deleting or editing background pages.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c55c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4c55c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c55c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4c55c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4c55c-107">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="4c55c-107">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4c55c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4c55c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4c55c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4c55c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4c55c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4c55c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4c55c-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="4c55c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4c55c-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="4c55c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c55c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4c55c-113">Definition</span></span>

```XML
< xs:element name="ProtectBkgnds" type="ProtectBkgnds_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c55c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4c55c-114">Elements and attributes</span></span>

<span data-ttu-id="4c55c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4c55c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4c55c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4c55c-116">Parent elements</span></span>

|<span data-ttu-id="4c55c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4c55c-117">**Element**</span></span>|<span data-ttu-id="4c55c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4c55c-118">**Type**</span></span>|<span data-ttu-id="4c55c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c55c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c55c-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="4c55c-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c55c-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4c55c-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4c55c-122">Содержит элементы, указывающие параметры документов.</span><span class="sxs-lookup"><span data-stu-id="4c55c-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4c55c-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4c55c-123">Child elements</span></span>

<span data-ttu-id="4c55c-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="4c55c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c55c-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4c55c-125">Attributes</span></span>

<span data-ttu-id="4c55c-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="4c55c-126">None.</span></span>
  

