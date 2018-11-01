---
title: Свойство NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb2c799fd7c9d1cc74c6081c10f7a8d356e79faf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876017"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="4d14a-102">Свойство NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="4d14a-102">NumericScale property (ADO)</span></span>


<span data-ttu-id="4d14a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d14a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d14a-104">Указывает масштаб числовых значений в объекте [параметра](parameter-object-ado.md) или [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4d14a-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4d14a-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4d14a-105">Settings and return values</span></span>

<span data-ttu-id="4d14a-106">Задает или возвращает **битное** значение, указывающее количество десятичных разрядов, к которым будут разрешены числовых значений.</span><span class="sxs-lookup"><span data-stu-id="4d14a-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d14a-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d14a-107">Remarks</span></span>

<span data-ttu-id="4d14a-108">Свойство **NumericScale** определяет количество цифр справа от десятичной запятой будет использоваться для представления значений для числовых объекта **параметра** или **поля** .</span><span class="sxs-lookup"><span data-stu-id="4d14a-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="4d14a-109">Для **параметра** объектов свойство **NumericScale** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="4d14a-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="4d14a-110">Для объекта **поля** **NumericScale** обычно доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4d14a-110">For a **Field** object, **NumericScale** is normally read-only.</span></span> <span data-ttu-id="4d14a-111">Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **NumericScale** — чтение и запись только после указано [значение](value-property-ado.md) свойства для **поля** и поставщика данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="4d14a-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

