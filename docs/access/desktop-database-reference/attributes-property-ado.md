---
title: Свойство Attributes (ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6495c70f64930e1b335c603f13e720ad581203a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296985"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="e4eca-102">Свойство Attributes (ADO)</span><span class="sxs-lookup"><span data-stu-id="e4eca-102">Attributes property (ADO)</span></span>


<span data-ttu-id="e4eca-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4eca-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="e4eca-104">Attributes Property</span><span class="sxs-lookup"><span data-stu-id="e4eca-104">Attributes Property</span></span>

<span data-ttu-id="e4eca-105">Указывает одну или несколько характеристик объекта.</span><span class="sxs-lookup"><span data-stu-id="e4eca-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e4eca-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e4eca-106">Settings and return values</span></span>

<span data-ttu-id="e4eca-107">Задает или возвращает значение **типа Long** .</span><span class="sxs-lookup"><span data-stu-id="e4eca-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="e4eca-108">Для объекта [Connection](connection-object-ado.md) свойство **Attributes** доступно для чтения и записи, а его значение может быть суммой одного или нескольких значений [ксактаттрибутинум](xactattributeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eca-108">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values.</span></span> <span data-ttu-id="e4eca-109">Значение по умолчанию — ноль (0).</span><span class="sxs-lookup"><span data-stu-id="e4eca-109">The default is zero (0).</span></span>

<span data-ttu-id="e4eca-110">Для объекта [Parameter](parameter-object-ado.md) свойство **Attributes** доступно для чтения и записи, а его значение может быть суммой одного или нескольких значений [параметераттрибутесенум](parameterattributesenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eca-110">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values.</span></span> <span data-ttu-id="e4eca-111">Значение по умолчанию — **адпарамсигнед**.</span><span class="sxs-lookup"><span data-stu-id="e4eca-111">The default is **adParamSigned**.</span></span>

<span data-ttu-id="e4eca-112">Для объекта [field](field-object-ado.md) свойство **Attributes** может быть суммой одного или нескольких значений [фиелдаттрибутинум](fieldattributeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eca-112">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values.</span></span> <span data-ttu-id="e4eca-113">Однако обычно он доступен только для чтения, но для новых **объектов Field** , добавленных в коллекцию [Fields](fields-collection-ado.md) [записи](record-object-ado.md), **атрибуты** доступны для чтения и записи только после того, как было указано свойство [value](value-property-ado.md) для **поля** и новое **поле** было успешно добавлено поставщиком данных, вызвав метод [Update](update-method-ado.md) коллекции **Fields** .</span><span class="sxs-lookup"><span data-stu-id="e4eca-113">It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="e4eca-114">Для объекта [Property](property-object-ado.md) свойство **Attributes** доступно только для чтения, а его значение может быть суммой одного или нескольких значений [пропертяттрибутесенум](propertyattributesenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eca-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4eca-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4eca-115">Remarks</span></span>

<span data-ttu-id="e4eca-116">Используйте свойство **Attributes** , чтобы задать или вернуть характеристики объектов **подключения** , объектов **параметров** , объектов [полей](field-object-ado.md) или объектов [Property](property-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eca-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="e4eca-117">При задании нескольких атрибутов можно суммировать соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="e4eca-117">When you set multiple attributes, you can sum the appropriate constants.</span></span> <span data-ttu-id="e4eca-118">Если присвоить свойству значение Sum, включая несовместимые константы, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e4eca-118">If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="e4eca-119">**Использование удаленной службы данных** Это свойство недоступно для объекта **подключения** на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="e4eca-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

