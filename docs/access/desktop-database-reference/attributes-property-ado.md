---
title: Attributes Property (ADO)
TOCTitle: Attributes Property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9fa17593a5606d288e519969ff63f10a1df229ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480364"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="3ddf2-102">Attributes Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ddf2-102">Attributes Property (ADO)</span></span>


<span data-ttu-id="3ddf2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ddf2-103">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="3ddf2-104">Свойство Attributes</span><span class="sxs-lookup"><span data-stu-id="3ddf2-104">Attributes Property</span></span>

<span data-ttu-id="3ddf2-105">Указывает один или несколько характеристик объекта.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3ddf2-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3ddf2-106">Settings and Return Values</span></span>

<span data-ttu-id="3ddf2-107">Задает или возвращает значение типа **Long** .</span><span class="sxs-lookup"><span data-stu-id="3ddf2-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="3ddf2-108">Объект [подключения](connection-object-ado.md) является ли данное свойство **атрибуты** чтения и записи и его значение может быть сумма одно или несколько значений [XactAttributeEnum](xactattributeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="3ddf2-108">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values.</span></span> <span data-ttu-id="3ddf2-109">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="3ddf2-109">The default is zero (0).</span></span>

<span data-ttu-id="3ddf2-110">Свойство **Attributes** — чтение и запись объект [параметра](parameter-object-ado.md) и его значение может быть сумма [ParameterAttributesEnum](parameterattributesenum.md) любого одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-110">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values.</span></span> <span data-ttu-id="3ddf2-111">Значение по умолчанию — **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-111">The default is **adParamSigned**.</span></span>

<span data-ttu-id="3ddf2-112">Для объекта [поля](field-object-ado.md) свойство **Attributes** может быть сумма одно или несколько значений [FieldAttributeEnum](fieldattributeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="3ddf2-112">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values.</span></span> <span data-ttu-id="3ddf2-113">Обычно только для чтения, однако для новых объектов **полей** , которые добавляются коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **атрибуты** чтения и записи только в том случае, если свойство [Value](value-property-ado.md) для **поля** не указан и новое **поле** успешно добавлена поставщиком данных путем вызова метода [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="3ddf2-113">It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="3ddf2-114">Для [Свойства](property-object-ado.md) объекта свойство **Attributes** доступен только для чтения и его значение может быть сумма [PropertyAttributesEnum](propertyattributesenum.md) любого одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddf2-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3ddf2-115">Remarks</span></span>

<span data-ttu-id="3ddf2-116">Используйте свойство **Attributes** задает или возвращает характеристик объекты **подключения** , объекты **параметров** , объекты [поля](field-object-ado.md) и [Свойства](property-object-ado.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="3ddf2-117">При указании нескольких атрибутов можно суммирования соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-117">When you set multiple attributes, you can sum the appropriate constants.</span></span> <span data-ttu-id="3ddf2-118">Если задать значение свойства для сумм, включая несовместимые константы, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-118">If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="3ddf2-119">**Службы удаленных данных об использовании** Это свойство недоступно на объект **подключения** со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="3ddf2-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

