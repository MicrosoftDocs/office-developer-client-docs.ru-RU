---
title: Свойство NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288555"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="9bbcc-102">Свойство NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="9bbcc-102">NumericScale property (ADO)</span></span>


<span data-ttu-id="9bbcc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bbcc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bbcc-104">Указывает масштаб числовые значения в объекте [Parameter](parameter-object-ado.md) или [Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9bbcc-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9bbcc-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9bbcc-105">Settings and return values</span></span>

<span data-ttu-id="9bbcc-106">Задает или возвращает значение **byte,** которое указывает количество десятичных значений, в которых будут разрешаться числимые значения.</span><span class="sxs-lookup"><span data-stu-id="9bbcc-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bbcc-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="9bbcc-107">Remarks</span></span>

<span data-ttu-id="9bbcc-108">Используйте свойство **NumericScale,** чтобы определить, сколько цифр справа от десятичной точки будет использоваться  для представления значений для числимого параметра или объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="9bbcc-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="9bbcc-109">Для **объектов Parameter** свойство **NumericScale** имеет свойство read/write.</span><span class="sxs-lookup"><span data-stu-id="9bbcc-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="9bbcc-110">Для объекта **Field** **NumericScale** обычно имеет только чтение.</span><span class="sxs-lookup"><span data-stu-id="9bbcc-110">For a **Field** object, **NumericScale** is normally read-only.</span></span> <span data-ttu-id="9bbcc-111">Однако для новых объектов **Field,** которые были добавлены в коллекцию [Fields](fields-collection-ado.md) записи,  **NumericScale** считывать и записывать только после того,  как свойство [Value](value-property-ado.md) для поля было задано и поставщик данных успешно добавил новое поле путем вызова метода [Update](update-method-ado.md) коллекции **Fields.** [](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="9bbcc-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

