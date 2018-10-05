---
title: Элемент CustomMenusFile (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: Содержит имя файла Microsoft Visio пользовательского интерфейса (.vsu), который определяет пользовательские меню и сочетания клавиш для документа.
ms.openlocfilehash: 347660abab266493254b4dc2b47150f3b80fd371
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394388"
---
# <a name="custommenusfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="5d0cf-103">Элемент CustomMenusFile (DocumentSettings_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5d0cf-103">CustomMenusFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5d0cf-104">Содержит имя файла Microsoft Visio пользовательского интерфейса (.vsu), который определяет пользовательские меню и сочетания клавиш для документа.</span><span class="sxs-lookup"><span data-stu-id="5d0cf-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d0cf-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5d0cf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d0cf-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5d0cf-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="5d0cf-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5d0cf-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5d0cf-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5d0cf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5d0cf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5d0cf-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5d0cf-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="5d0cf-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d0cf-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5d0cf-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5d0cf-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5d0cf-114">Elements and attributes</span></span>

<span data-ttu-id="5d0cf-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5d0cf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5d0cf-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5d0cf-116">Parent elements</span></span>

|<span data-ttu-id="5d0cf-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-117">**Element**</span></span>|<span data-ttu-id="5d0cf-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-118">**Type**</span></span>|<span data-ttu-id="5d0cf-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d0cf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d0cf-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="5d0cf-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d0cf-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5d0cf-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5d0cf-122">Содержит элементы, которые определяют параметры документов.</span><span class="sxs-lookup"><span data-stu-id="5d0cf-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d0cf-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5d0cf-123">Child elements</span></span>

<span data-ttu-id="5d0cf-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="5d0cf-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d0cf-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5d0cf-125">Attributes</span></span>

<span data-ttu-id="5d0cf-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="5d0cf-126">None.</span></span>
  

