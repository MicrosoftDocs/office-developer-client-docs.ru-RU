---
title: Объект Property (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302921"
---
# <a name="property-object-ado"></a><span data-ttu-id="09371-102">Объект Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="09371-102">Property object (ADO)</span></span>


<span data-ttu-id="09371-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09371-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09371-104">Представляет динамическую характеристику объекта ADO, определенного поставщиком.</span><span class="sxs-lookup"><span data-stu-id="09371-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="09371-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="09371-105">Remarks</span></span>

<span data-ttu-id="09371-106">У объектов ADO есть два типа свойств: встроенные и динамические.</span><span class="sxs-lookup"><span data-stu-id="09371-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="09371-107">Встроенные свойства — это свойства, реализованные в ADO и сразу же доступные любому новому объекту с использованием синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="09371-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="09371-108">Они не отображаются как **объекты Property** в коллекции [свойств](properties-collection-ado.md) объекта, поэтому хотя их значения можно изменить, изменить их характеристики нельзя.</span><span class="sxs-lookup"><span data-stu-id="09371-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="09371-109">Динамические свойства определяются поставщиком данных и отображаются в коллекции **свойств** соответствующего объекта ADO.</span><span class="sxs-lookup"><span data-stu-id="09371-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="09371-110">Например, свойство, определенное поставщику, может указывать, поддерживает ли объект [Recordset](recordset-object-ado.md) транзакции или обновление.</span><span class="sxs-lookup"><span data-stu-id="09371-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="09371-111">Эти дополнительные свойства будут отображаться как **объекты Property** в коллекции **свойств** этого объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="09371-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="09371-112">Ссылки на динамические свойства можно использовать только в коллекции с помощью синтаксиса MyObject.Properties(0) или MyObject.Properties("Name").</span><span class="sxs-lookup"><span data-stu-id="09371-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="09371-113">Невозможно удалить свойство любого типа.</span><span class="sxs-lookup"><span data-stu-id="09371-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="09371-114">**Динамический объект Property** имеет четыре собственных встроенных свойства:</span><span class="sxs-lookup"><span data-stu-id="09371-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="09371-115">Свойство [Name](name-property-ado.md) — это строка, определяемая свойством.</span><span class="sxs-lookup"><span data-stu-id="09371-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="09371-116">Свойство [Type](type-property-ado.md) — это integer, которое указывает тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="09371-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="09371-117">Свойство [Value](value-property-ado.md) — это вариант, содержащий параметр свойства.</span><span class="sxs-lookup"><span data-stu-id="09371-117">The [Value](value-property-ado.md) property is a variant that contains the property setting.</span></span> <span data-ttu-id="09371-118">**Значение** является свойством по умолчанию для объекта **Property.**</span><span class="sxs-lookup"><span data-stu-id="09371-118">**Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="09371-119">Свойство [Attributes](attributes-property-ado.md) — это длинное значение, которое указывает характеристики свойства, характерного для поставщика.</span><span class="sxs-lookup"><span data-stu-id="09371-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

