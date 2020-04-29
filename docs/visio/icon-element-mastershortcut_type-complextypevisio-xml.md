---
title: Элемент Icon (MasterShortcut_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: Задает двоичный значок закодированного двоичного расширения MIME (в формате ICO) для элемента MasterShortcut в документе.
ms.openlocfilehash: 6d223da406dd914c84aafdd3d37846c1ab30bb4e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541500"
---
# <a name="icon-element-mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="6b8ed-103">Элемент Icon (MasterShortcut_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="6b8ed-103">Icon element (MasterShortcut_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6b8ed-104">Задает двоичный значок закодированного двоичного расширения MIME (в формате ICO) для элемента MasterShortcut в документе.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b8ed-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b8ed-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b8ed-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b8ed-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="6b8ed-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b8ed-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b8ed-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b8ed-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6b8ed-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b8ed-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b8ed-112">Главные. XML</span><span class="sxs-lookup"><span data-stu-id="6b8ed-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b8ed-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6b8ed-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b8ed-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b8ed-114">Elements and attributes</span></span>

<span data-ttu-id="6b8ed-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b8ed-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6b8ed-116">Parent elements</span></span>

|<span data-ttu-id="6b8ed-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-117">**Element**</span></span>|<span data-ttu-id="6b8ed-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-118">**Type**</span></span>|<span data-ttu-id="6b8ed-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b8ed-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b8ed-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="6b8ed-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b8ed-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="6b8ed-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b8ed-122">Указывает неиспользуемый основной формат.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6b8ed-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b8ed-123">Child elements</span></span>

<span data-ttu-id="6b8ed-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b8ed-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b8ed-125">Attributes</span></span>

<span data-ttu-id="6b8ed-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="6b8ed-126">None.</span></span>
  

