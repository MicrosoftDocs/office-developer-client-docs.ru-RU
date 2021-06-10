---
title: Свойство Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287477"
---
# <a name="precision-property-ado"></a><span data-ttu-id="ae2a1-102">Свойство Precision (ADO)</span><span class="sxs-lookup"><span data-stu-id="ae2a1-102">Precision property (ADO)</span></span>


<span data-ttu-id="ae2a1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae2a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae2a1-104">Указывает степень точности числимых значений в объекте [Parameter](parameter-object-ado.md) или числовые объекты [Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ae2a1-104">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ae2a1-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="ae2a1-105">Settings and return values</span></span>

<span data-ttu-id="ae2a1-106">Задает или возвращает значение **Byte,** которое указывает максимальное число цифр, используемых для представления значений.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-106">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2a1-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae2a1-107">Remarks</span></span>

<span data-ttu-id="ae2a1-108">Используйте свойство **Precision,** чтобы определить максимальное число цифр, используемых для представления значений для численного объекта **Параметр** или **Поле.**</span><span class="sxs-lookup"><span data-stu-id="ae2a1-108">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="ae2a1-109">Значение — чтение или записи на **объекте Параметр.**</span><span class="sxs-lookup"><span data-stu-id="ae2a1-109">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="ae2a1-110">Для объекта **Field** **точность** обычно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-110">For a **Field** object, **Precision** is normally read-only.</span></span> <span data-ttu-id="ae2a1-111">Однако для новых  объектов [](value-property-ado.md)  **Field,** которые были [](fields-collection-ado.md) добавлены в  коллекцию Полей записи, [](record-object-ado.md)точность считывалась или записывалась только после того, как было задано свойство Value для поля и поставщик данных успешно добавил новое поле, позвонив [методу Update](update-method-ado.md) коллекции **Fields.**</span><span class="sxs-lookup"><span data-stu-id="ae2a1-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

