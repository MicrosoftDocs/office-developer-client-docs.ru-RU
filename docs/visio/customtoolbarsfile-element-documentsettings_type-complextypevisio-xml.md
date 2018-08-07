---
title: Элемент CustomToolbarsFile (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: Содержит имя файла интерфейса (.vsu) пользователя Microsoft Visio, который определяет пользовательские панели инструментов и строки состояния для документа.
ms.openlocfilehash: 46abc567d2135815a82b4efec47a7bd77d0763cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813532"
---
# <a name="customtoolbarsfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="acd51-103">Элемент CustomToolbarsFile (DocumentSettings_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="acd51-103">CustomToolbarsFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="acd51-104">Содержит имя файла интерфейса (.vsu) пользователя Microsoft Visio, который определяет пользовательские панели инструментов и строки состояния для документа.</span><span class="sxs-lookup"><span data-stu-id="acd51-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acd51-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="acd51-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acd51-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="acd51-106">**Element type**</span></span> <br/> |[<span data-ttu-id="acd51-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="acd51-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="acd51-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="acd51-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="acd51-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="acd51-109">**Schema file**</span></span> <br/> |<span data-ttu-id="acd51-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="acd51-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="acd51-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="acd51-111">**Document parts**</span></span> <br/> |<span data-ttu-id="acd51-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="acd51-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acd51-113">Определение</span><span class="sxs-lookup"><span data-stu-id="acd51-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="acd51-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="acd51-114">Elements and attributes</span></span>

<span data-ttu-id="acd51-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="acd51-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="acd51-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="acd51-116">Parent elements</span></span>

|<span data-ttu-id="acd51-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="acd51-117">**Element**</span></span>|<span data-ttu-id="acd51-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="acd51-118">**Type**</span></span>|<span data-ttu-id="acd51-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="acd51-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acd51-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="acd51-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acd51-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="acd51-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acd51-122">Содержит элементы, которые определяют параметры документов.</span><span class="sxs-lookup"><span data-stu-id="acd51-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="acd51-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="acd51-123">Child elements</span></span>

<span data-ttu-id="acd51-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="acd51-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acd51-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="acd51-125">Attributes</span></span>

<span data-ttu-id="acd51-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="acd51-126">None.</span></span>
  

