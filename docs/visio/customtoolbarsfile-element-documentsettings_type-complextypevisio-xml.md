---
title: Элемент CustomToolbarsFile (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: Содержит имя файла пользовательского интерфейса Microsoft Visio (VSU), который определяет настраиваемые панели инструментов и панели состояния для документа.
ms.openlocfilehash: c374bc571163936ccdd4812bcf58a8db19a81f1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539236"
---
# <a name="customtoolbarsfile-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="ae91a-103">Элемент CustomToolbarsFile (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ae91a-103">CustomToolbarsFile element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ae91a-104">Содержит имя файла пользовательского интерфейса Microsoft Visio (VSU), который определяет настраиваемые панели инструментов и панели состояния для документа.</span><span class="sxs-lookup"><span data-stu-id="ae91a-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae91a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ae91a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae91a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ae91a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ae91a-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="ae91a-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ae91a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ae91a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ae91a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ae91a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ae91a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ae91a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ae91a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ae91a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ae91a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="ae91a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae91a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ae91a-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ae91a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ae91a-114">Elements and attributes</span></span>

<span data-ttu-id="ae91a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ae91a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ae91a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ae91a-116">Parent elements</span></span>

|<span data-ttu-id="ae91a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ae91a-117">**Element**</span></span>|<span data-ttu-id="ae91a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ae91a-118">**Type**</span></span>|<span data-ttu-id="ae91a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae91a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae91a-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="ae91a-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae91a-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ae91a-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae91a-122">Содержит элементы, определяющие параметры документа.</span><span class="sxs-lookup"><span data-stu-id="ae91a-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae91a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ae91a-123">Child elements</span></span>

<span data-ttu-id="ae91a-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="ae91a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae91a-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ae91a-125">Attributes</span></span>

<span data-ttu-id="ae91a-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="ae91a-126">None.</span></span>
  

