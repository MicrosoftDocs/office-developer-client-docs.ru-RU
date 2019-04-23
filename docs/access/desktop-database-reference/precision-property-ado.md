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
# <a name="precision-property-ado"></a><span data-ttu-id="44877-102">Свойство Precision (ADO)</span><span class="sxs-lookup"><span data-stu-id="44877-102">Precision property (ADO)</span></span>


<span data-ttu-id="44877-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44877-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44877-104">Указывает степень точности для числовых значений в объекте [Parameter](parameter-object-ado.md) или числовых объектах [полей](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="44877-104">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="44877-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="44877-105">Settings and return values</span></span>

<span data-ttu-id="44877-106">Задает или возвращает значение **типа Byte** , указывающее максимальное количество цифр, используемых для представления значений.</span><span class="sxs-lookup"><span data-stu-id="44877-106">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="44877-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="44877-107">Remarks</span></span>

<span data-ttu-id="44877-108">Используйте свойство **Precision** для определения максимального числа цифр, используемых для представления значений числового **параметра** или объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="44877-108">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="44877-109">Значение доступно для чтения и записи в объекте **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="44877-109">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="44877-110">Для объекта **field** **точность** обычно доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="44877-110">For a **Field** object, **Precision** is normally read-only.</span></span> <span data-ttu-id="44877-111">Тем не менее, для новых объектов **field** , добавленных в коллекцию [Fields](fields-collection-ado.md) [записи](record-object-ado.md), **точность** доступна только после того, как было указано свойство [value](value-property-ado.md) для **поля** , и у поставщика данных новое **поле** успешно добавлено путем вызова метода [Update](update-method-ado.md) коллекции Fields. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="44877-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

