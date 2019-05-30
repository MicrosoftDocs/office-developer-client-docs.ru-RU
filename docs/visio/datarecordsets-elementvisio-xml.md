---
title: Элемент RecordSets (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Содержит все элементы Record в документе.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542445"
---
# <a name="datarecordsets-element-visio-xml"></a><span data-ttu-id="fe490-103">Элемент RecordSets (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="fe490-103">DataRecordSets element (Visio XML)</span></span>

<span data-ttu-id="fe490-104">Содержит все элементы **Record** в документе.</span><span class="sxs-lookup"><span data-stu-id="fe490-104">Contains all the **DataRecordset** elements in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fe490-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fe490-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe490-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="fe490-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fe490-107">Датарекордсетс_типе</span><span class="sxs-lookup"><span data-stu-id="fe490-107">DataRecordSets_Type</span></span>](datarecordsets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fe490-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fe490-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fe490-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fe490-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fe490-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fe490-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fe490-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="fe490-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fe490-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="fe490-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fe490-113">Определение</span><span class="sxs-lookup"><span data-stu-id="fe490-113">Definition</span></span>

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fe490-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fe490-114">Elements and attributes</span></span>

<span data-ttu-id="fe490-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fe490-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fe490-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fe490-116">Parent elements</span></span>

<span data-ttu-id="fe490-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="fe490-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe490-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fe490-118">Child elements</span></span>

|<span data-ttu-id="fe490-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fe490-119">**Element**</span></span>|<span data-ttu-id="fe490-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fe490-120">**Type**</span></span>|<span data-ttu-id="fe490-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe490-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fe490-122">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe490-122">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fe490-123">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="fe490-123">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fe490-124">Содержит все элементы **Record** в документе.</span><span class="sxs-lookup"><span data-stu-id="fe490-124">Contains all the **DataRecordset** elements in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fe490-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fe490-125">Attributes</span></span>

|<span data-ttu-id="fe490-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fe490-126">**Attribute**</span></span>|<span data-ttu-id="fe490-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fe490-127">**Type**</span></span>|<span data-ttu-id="fe490-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="fe490-128">**Required**</span></span>|<span data-ttu-id="fe490-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe490-129">**Description**</span></span>|<span data-ttu-id="fe490-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fe490-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fe490-131">Активерекордсетид</span><span class="sxs-lookup"><span data-stu-id="fe490-131">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="fe490-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="fe490-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe490-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="fe490-133">optional</span></span>  <br/> |<span data-ttu-id="fe490-134">ИДЕНТИФИКАТОР активного набора данных в окне " **Внешние данные** " при закрытии окна, чтобы его можно было восстановить при следующем открытии окна.</span><span class="sxs-lookup"><span data-stu-id="fe490-134">The ID of the active data recordset in the **External Data** window when the window closes, so that it can be restored the next time the window opens.</span></span>  <br/> |<span data-ttu-id="fe490-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="fe490-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fe490-136">Датавиндовордер</span><span class="sxs-lookup"><span data-stu-id="fe490-136">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="fe490-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="fe490-137">xsd:string</span></span>  <br/> |<span data-ttu-id="fe490-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="fe490-138">optional</span></span>  <br/> |<span data-ttu-id="fe490-139">Порядок наборов записей данных, отображаемых на вкладках окна " **Внешние данные** ".</span><span class="sxs-lookup"><span data-stu-id="fe490-139">The order of the data recordsets displayed on the tabs of the **External Data** window.</span></span> <span data-ttu-id="fe490-140">Упорядоченный список идентификаторов записей данных, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="fe490-140">An ordered list of data-recordset IDs, separated by semi-colons.</span></span>  <br/> |<span data-ttu-id="fe490-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="fe490-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fe490-142">Некстид</span><span class="sxs-lookup"><span data-stu-id="fe490-142">NextID</span></span>  <br/> |<span data-ttu-id="fe490-143">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="fe490-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fe490-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fe490-144">required</span></span>  <br/> |<span data-ttu-id="fe490-145">Следующий доступный идентификатор для нового набора записей данных.</span><span class="sxs-lookup"><span data-stu-id="fe490-145">The next available ID for a new data recordset.</span></span>  <br/> |<span data-ttu-id="fe490-146">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="fe490-146">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

