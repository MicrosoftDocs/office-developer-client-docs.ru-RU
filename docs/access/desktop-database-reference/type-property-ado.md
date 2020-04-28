---
title: Свойство Type (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314016"
---
# <a name="type-property-ado"></a><span data-ttu-id="83976-102">Свойство Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="83976-102">Type property (ADO)</span></span>


<span data-ttu-id="83976-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83976-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83976-104">Указывает операционный тип или тип данных для [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или объекта [Property](property-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="83976-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="83976-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="83976-105">Settings and return values</span></span>

<span data-ttu-id="83976-106">Задает или возвращает значение [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="83976-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83976-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="83976-107">Remarks</span></span>

<span data-ttu-id="83976-108">Для объектов **Parameter** свойство **Type** доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="83976-108">For **Parameter** objects, the **Type** property is read/write.</span></span> <span data-ttu-id="83976-109">Для новых **объектов Field** , добавленных в коллекцию [Fields](fields-collection-ado.md) [записи](record-object-ado.md), **тип** доступен для чтения и записи только после того, как было указано свойство [value](value-property-ado.md) для **поля** , и поставщик данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **Fields** .</span><span class="sxs-lookup"><span data-stu-id="83976-109">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="83976-110">Для всех остальных объектов свойство **Type** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="83976-110">For all other objects, the **Type** property is read-only.</span></span>

