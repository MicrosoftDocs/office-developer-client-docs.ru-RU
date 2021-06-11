---
title: Элемент ProtectMasters (DocumentSettings_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Указывает, не мешает ли пользователю создавать, редактировать или удалять мастер-фигуры. Пользователь по-прежнему может создавать новые фигуры из мастер-формы, независимо от этого параметра.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540695"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="a1994-104">Элемент ProtectMasters (DocumentSettings_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a1994-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a1994-105">Указывает, не мешает ли пользователю создавать, редактировать или удалять мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="a1994-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="a1994-106">Пользователь по-прежнему может создавать новые фигуры из мастер-формы, независимо от этого параметра.</span><span class="sxs-lookup"><span data-stu-id="a1994-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="a1994-107">Диапазон возможных значений для этого элемента : "0" или "1".</span><span class="sxs-lookup"><span data-stu-id="a1994-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="a1994-108">Значение "0" указывает, что пользователи могут создавать, редактировать или удалять мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="a1994-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="a1994-109">Значение "1" указывает на то, что пользователи не могут создавать, изменять или удалять мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="a1994-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1994-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a1994-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1994-111">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a1994-111">**Element type**</span></span> <br/> |[<span data-ttu-id="a1994-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="a1994-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a1994-113">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a1994-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a1994-114">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a1994-114">**Schema file**</span></span> <br/> |<span data-ttu-id="a1994-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a1994-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a1994-116">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="a1994-116">**Document parts**</span></span> <br/> |<span data-ttu-id="a1994-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="a1994-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1994-118">Определение</span><span class="sxs-lookup"><span data-stu-id="a1994-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a1994-119">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1994-119">Elements and attributes</span></span>

<span data-ttu-id="a1994-120">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a1994-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a1994-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a1994-121">Parent elements</span></span>

|<span data-ttu-id="a1994-122">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a1994-122">**Element**</span></span>|<span data-ttu-id="a1994-123">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a1994-123">**Type**</span></span>|<span data-ttu-id="a1994-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1994-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1994-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="a1994-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1994-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a1994-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1994-127">Содержит элементы, указывающие параметры документов.</span><span class="sxs-lookup"><span data-stu-id="a1994-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a1994-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a1994-128">Child elements</span></span>

<span data-ttu-id="a1994-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="a1994-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1994-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1994-130">Attributes</span></span>

<span data-ttu-id="a1994-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="a1994-131">None.</span></span>
  

