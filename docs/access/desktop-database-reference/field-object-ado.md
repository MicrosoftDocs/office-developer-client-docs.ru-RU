---
title: Объект field — ActiveX объектов данных (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2bf17029a706ad6902a8a01a14e73183f94d7a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293058"
---
# <a name="field-object-ado"></a><span data-ttu-id="b3616-102">Объект Field (ADO)</span><span class="sxs-lookup"><span data-stu-id="b3616-102">Field object (ADO)</span></span>


<span data-ttu-id="b3616-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3616-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3616-104">Представляет столбец данных с общим типом данных.</span><span class="sxs-lookup"><span data-stu-id="b3616-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3616-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3616-105">Remarks</span></span>

<span data-ttu-id="b3616-106">Каждый объект **Field** соответствует столбцу в [Наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-106">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="b3616-107">Свойство [Value](value-property-ado.md) объектов **Field** используется для набора или возврата данных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b3616-107">You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record.</span></span> <span data-ttu-id="b3616-108">В зависимости от функциональных возможностей, которые предоставляет поставщик, некоторые коллекции, методы или свойства объекта **Field** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="b3616-108">Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="b3616-109">С помощью коллекций, методов и свойств объекта **Field** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="b3616-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="b3616-110">Возвращаем имя поля с [свойством Name.](name-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="b3616-111">Просмотр или изменение данных в поле с помощью **свойства Value.**</span><span class="sxs-lookup"><span data-stu-id="b3616-111">View or change the data in the field with the **Value** property.</span></span> <span data-ttu-id="b3616-112">**Значение** — это свойство по умолчанию объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="b3616-112">**Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="b3616-113">Верни основные характеристики поля с свойствами [Type,](type-property-ado.md) [Precision](precision-property-ado.md)и [NumericScale.](numericscale-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="b3616-114">Возврат объявленного размера поля с [свойством DefinedSize.](definedsize-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="b3616-115">Возврат фактического размера данных в заданное поле с помощью [свойства ActualSize.](actualsize-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="b3616-116">Определите, какие типы функций поддерживаются для данного поля с помощью коллекции свойств и [свойств](properties-collection-ado.md) [Attributes.](attributes-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="b3616-117">Манипулировать значениями полей, содержащих длинные двоичные или длинные данные символов с помощью методов [AppendChunk](appendchunk-method-ado.md) и [GetChunk.](getchunk-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="b3616-118">Если поставщик поддерживает пакетные обновления, устранять несоответствия в значениях полей при пакетном обновлении с свойствами [OriginalValue](originalvalue-property-ado.md) и [UnderlyingValue.](underlyingvalue-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b3616-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="b3616-119">Все свойства метаданных **(Name,** **Type,** **DefinedSize,** **Precision** и **NumericScale)** доступны  перед открытием наборов **записей объекта Field.**</span><span class="sxs-lookup"><span data-stu-id="b3616-119">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**.</span></span> <span data-ttu-id="b3616-120">Установка их в это время полезна для динамического построения форм.</span><span class="sxs-lookup"><span data-stu-id="b3616-120">Setting them at that time is useful for dynamically constructing forms.</span></span>

