---
title: Элемент CustomMenusFile (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: Содержит имя файла Microsoft Visio пользовательского интерфейса (.vsu), который определяет пользовательские меню и сочетания клавиш для документа.
ms.openlocfilehash: 2044c7e300dc51df8b8cd03ef861391d04494e0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813510"
---
# <a name="custommenusfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="7dc07-103">Элемент CustomMenusFile (DocumentSettings_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7dc07-103">CustomMenusFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7dc07-104">Содержит имя файла Microsoft Visio пользовательского интерфейса (.vsu), который определяет пользовательские меню и сочетания клавиш для документа.</span><span class="sxs-lookup"><span data-stu-id="7dc07-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7dc07-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7dc07-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dc07-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7dc07-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7dc07-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="7dc07-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7dc07-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7dc07-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7dc07-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7dc07-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7dc07-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7dc07-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7dc07-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="7dc07-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7dc07-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="7dc07-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7dc07-113">Определение</span><span class="sxs-lookup"><span data-stu-id="7dc07-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7dc07-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7dc07-114">Elements and attributes</span></span>

<span data-ttu-id="7dc07-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="7dc07-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7dc07-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7dc07-116">Parent elements</span></span>

|<span data-ttu-id="7dc07-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7dc07-117">**Element**</span></span>|<span data-ttu-id="7dc07-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7dc07-118">**Type**</span></span>|<span data-ttu-id="7dc07-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7dc07-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7dc07-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="7dc07-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7dc07-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7dc07-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7dc07-122">Содержит элементы, которые определяют параметры документов.</span><span class="sxs-lookup"><span data-stu-id="7dc07-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7dc07-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7dc07-123">Child elements</span></span>

<span data-ttu-id="7dc07-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="7dc07-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dc07-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7dc07-125">Attributes</span></span>

<span data-ttu-id="7dc07-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="7dc07-126">None.</span></span>
  

