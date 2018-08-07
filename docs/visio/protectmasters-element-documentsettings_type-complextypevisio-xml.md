---
title: Элемент ProtectMasters (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Указывает, является ли пользователь, которым запрещен создание, изменение или удаление образцов фигур. Пользователь по-прежнему может создавать новые фигуры из главной формы, независимо от того, этот параметр.
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814488"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="94635-104">Элемент ProtectMasters (DocumentSettings_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="94635-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="94635-105">Указывает, является ли пользователь, которым запрещен создание, изменение или удаление образцов фигур.</span><span class="sxs-lookup"><span data-stu-id="94635-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="94635-106">Пользователь по-прежнему может создавать новые фигуры из главной формы, независимо от того, этот параметр.</span><span class="sxs-lookup"><span data-stu-id="94635-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="94635-107">Диапазон допустимых значений для этого элемента — "0" или "1".</span><span class="sxs-lookup"><span data-stu-id="94635-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="94635-108">Значение "0" Указывает, что пользователи создание, изменение и удаление образцов фигур.</span><span class="sxs-lookup"><span data-stu-id="94635-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="94635-109">Значение "1" Указывает, что пользователи не могут создать, изменить и удалить основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="94635-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94635-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="94635-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94635-111">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="94635-111">**Element type**</span></span> <br/> |[<span data-ttu-id="94635-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="94635-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="94635-113">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="94635-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="94635-114">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="94635-114">**Schema file**</span></span> <br/> |<span data-ttu-id="94635-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="94635-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="94635-116">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="94635-116">**Document parts**</span></span> <br/> |<span data-ttu-id="94635-117">Document.XML</span><span class="sxs-lookup"><span data-stu-id="94635-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94635-118">Определение</span><span class="sxs-lookup"><span data-stu-id="94635-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="94635-119">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="94635-119">Elements and attributes</span></span>

<span data-ttu-id="94635-120">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="94635-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="94635-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="94635-121">Parent elements</span></span>

|<span data-ttu-id="94635-122">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="94635-122">**Element**</span></span>|<span data-ttu-id="94635-123">**Тип**</span><span class="sxs-lookup"><span data-stu-id="94635-123">**Type**</span></span>|<span data-ttu-id="94635-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="94635-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="94635-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="94635-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="94635-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="94635-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94635-127">Содержит элементы, которые определяют параметры документов.</span><span class="sxs-lookup"><span data-stu-id="94635-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94635-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="94635-128">Child elements</span></span>

<span data-ttu-id="94635-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="94635-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94635-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="94635-130">Attributes</span></span>

<span data-ttu-id="94635-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="94635-131">None.</span></span>
  

