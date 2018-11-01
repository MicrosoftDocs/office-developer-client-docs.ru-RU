---
title: Свойство Type (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 646284877722baf9aec6bb591b071667fdf9cc1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867729"
---
# <a name="type-property-ado"></a><span data-ttu-id="7749d-102">Свойство Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="7749d-102">Type property (ADO)</span></span>


<span data-ttu-id="7749d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7749d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7749d-104">Указывает тип действующие или тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="7749d-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7749d-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7749d-105">Settings and return values</span></span>

<span data-ttu-id="7749d-106">Задает или возвращает значение [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="7749d-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7749d-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="7749d-107">Remarks</span></span>

<span data-ttu-id="7749d-108">Для **параметра** объектов свойство **Type** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="7749d-108">For **Parameter** objects, the **Type** property is read/write.</span></span> <span data-ttu-id="7749d-109">Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md) **Тип** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и поставщик данных имеет успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="7749d-109">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="7749d-110">Для всех других объектов свойство **Type** — только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7749d-110">For all other objects, the **Type** property is read-only.</span></span>

