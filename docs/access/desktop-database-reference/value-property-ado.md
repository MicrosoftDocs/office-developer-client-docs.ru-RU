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
# <a name="value-property-ado"></a><span data-ttu-id="d7ff7-102">Свойство Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7ff7-102">Value property (ADO)</span></span>

<span data-ttu-id="d7ff7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7ff7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7ff7-104">Указывает значение, назначенное объекту [Field,](field-object-ado.md) [Parameter](parameter-object-ado.md)или [Property.](property-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d7ff7-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d7ff7-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d7ff7-105">Settings and return values</span></span>

<span data-ttu-id="d7ff7-106">Задает или возвращает значение **Variant,** которое указывает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="d7ff7-106">Sets or returns a **Variant** value that indicates the value of the object.</span></span> <span data-ttu-id="d7ff7-107">Значение по умолчанию зависит от свойства [Type.](type-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d7ff7-107">Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ff7-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="d7ff7-108">Remarks</span></span>

<span data-ttu-id="d7ff7-109">Используйте свойство **Value,** чтобы устанавливать или возвращать данные из объектов **Field,** устанавливать или возвращать значения параметров с помощью объектов **Parameter,** а также устанавливать или возвращать параметры свойств с **объектами Property.**</span><span class="sxs-lookup"><span data-stu-id="d7ff7-109">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects.</span></span> <span data-ttu-id="d7ff7-110">То, является ли свойство **Value** чтением, чтением или только чтением, зависит от множества факторов. Дополнительные сведения см. в соответствующих темах объекта.</span><span class="sxs-lookup"><span data-stu-id="d7ff7-110">Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="d7ff7-111">ADO позволяет устанавливать и возвращать длинные двоичные данные со **свойством Value.**</span><span class="sxs-lookup"><span data-stu-id="d7ff7-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="d7ff7-112">Для **объектов Parameter** ADO считыет свойство **Value** только один раз от поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7ff7-112">For **Parameter** objects, ADO reads the **Value** property only once from the provider.</span></span> <span data-ttu-id="d7ff7-113">Если команда содержит  параметр, свойство **Value** которого пусто, и создается набор записей из команды, убедитесь, что сначала закройте **recordset** перед искомым [](recordset-object-ado.md) **свойством Value.**</span><span class="sxs-lookup"><span data-stu-id="d7ff7-113">If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property.</span></span> <span data-ttu-id="d7ff7-114">В противном случае для некоторых поставщиков свойство **Value** может быть пустым и содержать неправильное значение.</span><span class="sxs-lookup"><span data-stu-id="d7ff7-114">Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="d7ff7-115">Для новых объектов **Field,** которые были добавлены в коллекцию [Fields](fields-collection-ado.md) объекта [Record,](record-object-ado.md)  свойство **Value** должно быть задано до того, как могут быть указаны другие свойства Field.</span><span class="sxs-lookup"><span data-stu-id="d7ff7-115">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified.</span></span> <span data-ttu-id="d7ff7-116">Во-первых, должно быть назначено определенное [](update-method-ado.md) значение для свойства **Value** и вызвано обновление коллекции **Fields.**</span><span class="sxs-lookup"><span data-stu-id="d7ff7-116">First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called.</span></span> <span data-ttu-id="d7ff7-117">Затем можно получить доступ к другим свойствам, таким как [Type](type-property-ado.md) или [Attributes.](attributes-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d7ff7-117">Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

