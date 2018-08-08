---
title: Значок элемент (MasterShortcut_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: Задает двоичный значок (в формате .ico) кодировке MIME (Multipurpose Internet Mail Extensions) для элемента MasterShortcut в документе.
ms.openlocfilehash: 46ca7c3f6ba733d31823f6b47f083c46dd941c14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813934"
---
# <a name="icon-element-mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="53430-103">Значок элемент (MasterShortcut_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="53430-103">Icon element (MasterShortcut_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="53430-104">Задает двоичный значок (в формате .ico) кодировке MIME (Multipurpose Internet Mail Extensions) для элемента MasterShortcut в документе.</span><span class="sxs-lookup"><span data-stu-id="53430-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53430-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="53430-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53430-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="53430-106">**Element type**</span></span> <br/> |[<span data-ttu-id="53430-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="53430-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="53430-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="53430-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="53430-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="53430-109">**Schema file**</span></span> <br/> |<span data-ttu-id="53430-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="53430-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="53430-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="53430-111">**Document parts**</span></span> <br/> |<span data-ttu-id="53430-112">Masters.XML</span><span class="sxs-lookup"><span data-stu-id="53430-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="53430-113">Определение</span><span class="sxs-lookup"><span data-stu-id="53430-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="53430-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="53430-114">Elements and attributes</span></span>

<span data-ttu-id="53430-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="53430-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="53430-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="53430-116">Parent elements</span></span>

|<span data-ttu-id="53430-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="53430-117">**Element**</span></span>|<span data-ttu-id="53430-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="53430-118">**Type**</span></span>|<span data-ttu-id="53430-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="53430-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="53430-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="53430-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="53430-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="53430-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="53430-122">Задает неиспользуемыми основной формат.</span><span class="sxs-lookup"><span data-stu-id="53430-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="53430-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="53430-123">Child elements</span></span>

<span data-ttu-id="53430-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="53430-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53430-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="53430-125">Attributes</span></span>

<span data-ttu-id="53430-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="53430-126">None.</span></span>
  

