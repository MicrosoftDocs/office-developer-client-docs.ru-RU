---
title: Свойство Value (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00b82706d934356621ac1e41fffca61ec88e081f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305896"
---
# <a name="value-property-ado"></a><span data-ttu-id="83d4e-102">Свойство Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="83d4e-102">Value property (ADO)</span></span>

<span data-ttu-id="83d4e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83d4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83d4e-104">Указывает значение, назначенное [полю](field-object-ado.md), [параметру](parameter-object-ado.md)или объекту [Property](property-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="83d4e-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="83d4e-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="83d4e-105">Settings and return values</span></span>

<span data-ttu-id="83d4e-106">Задает или возвращает значение **типа Variant** , которое указывает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="83d4e-106">Sets or returns a **Variant** value that indicates the value of the object.</span></span> <span data-ttu-id="83d4e-107">Значение по умолчанию зависит от свойства [Type](type-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="83d4e-107">Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d4e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="83d4e-108">Remarks</span></span>

<span data-ttu-id="83d4e-109">Используйте свойство **value** , чтобы задать или вернуть данные из объектов **field** , чтобы задать или вернуть значения параметров с помощью объектов **Parameter** или задать или вернуть параметры свойств с помощью объектов **Property** .</span><span class="sxs-lookup"><span data-stu-id="83d4e-109">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects.</span></span> <span data-ttu-id="83d4e-110">Независимо от того, является ли свойство **value** доступно для чтения и записи или только для чтения, зависит от множества факторов — просмотрите разделы, посвященные соответствующим объектам, для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="83d4e-110">Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="83d4e-111">С помощью ADO можно задавать и возвращать длинные двоичные данные со свойством **value** .</span><span class="sxs-lookup"><span data-stu-id="83d4e-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="83d4e-112">Для объектов **Parameter** ADO читает свойство **value** только один раз от поставщика.</span><span class="sxs-lookup"><span data-stu-id="83d4e-112">For **Parameter** objects, ADO reads the **Value** property only once from the provider.</span></span> <span data-ttu-id="83d4e-113">Если команда содержит **параметр** , свойство **value** которого пустое, и создан [набор записей](recordset-object-ado.md) из команды, убедитесь, что сначала закрывается **набор записей** , прежде чем будет получено свойство **value** .</span><span class="sxs-lookup"><span data-stu-id="83d4e-113">If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property.</span></span> <span data-ttu-id="83d4e-114">В противном случае для некоторых поставщиков свойство **value** может быть пустым и не будет содержать правильное значение.</span><span class="sxs-lookup"><span data-stu-id="83d4e-114">Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="83d4e-115">Для новых объектов **field** , добавленных в коллекцию Fields [](fields-collection-ado.md) объекта [Record](record-object-ado.md) , свойство **value** должно быть задано до того, как можно будет указать другие свойства **поля** .</span><span class="sxs-lookup"><span data-stu-id="83d4e-115">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified.</span></span> <span data-ttu-id="83d4e-116">Во-первых, в коллекции Fields должно быть назначено и [Обновлено](update-method-ado.md) определенное значение свойства \*\*\*\* **value** .</span><span class="sxs-lookup"><span data-stu-id="83d4e-116">First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called.</span></span> <span data-ttu-id="83d4e-117">Затем можно получить доступ к другим свойствам, таким как [Type](type-property-ado.md) или [Attributes](attributes-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="83d4e-117">Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

