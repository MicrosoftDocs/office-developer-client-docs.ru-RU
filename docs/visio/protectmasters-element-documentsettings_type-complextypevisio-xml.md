---
title: Элемент Протектмастерс (Документсеттингс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Указывает, запрещено ли пользователю создавать, редактировать или удалять основные фигуры. Пользователь по-прежнему может создавать новые фигуры из основной фигуры независимо от этого параметра.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540695"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="1da2e-104">Элемент Протектмастерс (Документсеттингс_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1da2e-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1da2e-105">Указывает, запрещено ли пользователю создавать, редактировать или удалять основные фигуры.</span><span class="sxs-lookup"><span data-stu-id="1da2e-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="1da2e-106">Пользователь по-прежнему может создавать новые фигуры из основной фигуры независимо от этого параметра.</span><span class="sxs-lookup"><span data-stu-id="1da2e-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="1da2e-107">Диапазон допустимых значений для этого элемента: "0" или "1".</span><span class="sxs-lookup"><span data-stu-id="1da2e-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="1da2e-108">Значение "0" указывает на то, что пользователи могут создавать, изменять или удалять основные фигуры.</span><span class="sxs-lookup"><span data-stu-id="1da2e-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="1da2e-109">Значение "1" указывает на то, что пользователи не могут создавать, изменять или удалять основные фигуры.</span><span class="sxs-lookup"><span data-stu-id="1da2e-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1da2e-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1da2e-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1da2e-111">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="1da2e-111">**Element type**</span></span> <br/> |[<span data-ttu-id="1da2e-112">Протектмастерс_типе</span><span class="sxs-lookup"><span data-stu-id="1da2e-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1da2e-113">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1da2e-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1da2e-114">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1da2e-114">**Schema file**</span></span> <br/> |<span data-ttu-id="1da2e-115">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1da2e-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1da2e-116">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="1da2e-116">**Document parts**</span></span> <br/> |<span data-ttu-id="1da2e-117">Document. XML</span><span class="sxs-lookup"><span data-stu-id="1da2e-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1da2e-118">Определение</span><span class="sxs-lookup"><span data-stu-id="1da2e-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1da2e-119">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1da2e-119">Elements and attributes</span></span>

<span data-ttu-id="1da2e-120">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1da2e-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1da2e-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1da2e-121">Parent elements</span></span>

|<span data-ttu-id="1da2e-122">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1da2e-122">**Element**</span></span>|<span data-ttu-id="1da2e-123">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1da2e-123">**Type**</span></span>|<span data-ttu-id="1da2e-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1da2e-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1da2e-125">Документсеттингс</span><span class="sxs-lookup"><span data-stu-id="1da2e-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1da2e-126">Документсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="1da2e-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1da2e-127">Содержит элементы, определяющие параметры документа.</span><span class="sxs-lookup"><span data-stu-id="1da2e-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1da2e-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1da2e-128">Child elements</span></span>

<span data-ttu-id="1da2e-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="1da2e-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1da2e-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1da2e-130">Attributes</span></span>

<span data-ttu-id="1da2e-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="1da2e-131">None.</span></span>
  

