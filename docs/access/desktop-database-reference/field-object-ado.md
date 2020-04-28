---
title: Объект Field — объекты данных ActiveX (ADO)
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
# <a name="field-object-ado"></a><span data-ttu-id="d01e5-102">Объект Field (ADO)</span><span class="sxs-lookup"><span data-stu-id="d01e5-102">Field object (ADO)</span></span>


<span data-ttu-id="d01e5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d01e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d01e5-104">Представляет столбец данных с общим типом данных.</span><span class="sxs-lookup"><span data-stu-id="d01e5-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d01e5-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d01e5-105">Remarks</span></span>

<span data-ttu-id="d01e5-106">Каждый объект **field** соответствует столбцу в [наборе записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d01e5-106">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="d01e5-107">Свойство [value](value-property-ado.md) объекта **field** используется для задания или возвращения данных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d01e5-107">You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record.</span></span> <span data-ttu-id="d01e5-108">В зависимости от функциональных возможностей, предоставляемых поставщиком, некоторые коллекции, методы или свойства объекта **field** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="d01e5-108">Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="d01e5-109">В коллекциях, методах и свойствах объекта **field** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d01e5-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="d01e5-110">Возвращает имя поля со свойством [Name](name-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="d01e5-111">Просмотрите или измените данные в поле со свойством **value** .</span><span class="sxs-lookup"><span data-stu-id="d01e5-111">View or change the data in the field with the **Value** property.</span></span> <span data-ttu-id="d01e5-112">**Value** является свойством по умолчанию объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="d01e5-112">**Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="d01e5-113">Возвращает основные характеристики поля с помощью свойств [Type](type-property-ado.md), [Precision](precision-property-ado.md)и [NumericScale](numericscale-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="d01e5-114">Возврат объявленного размера поля с помощью свойства [DefinedSize](definedsize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="d01e5-115">Возвращает фактический размер данных в заданном поле с помощью свойства [ActualSize](actualsize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="d01e5-116">Определите, какие типы функциональных возможностей поддерживаются для данного поля с помощью свойства [Attributes](attributes-property-ado.md) и коллекции [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="d01e5-117">Управлять значениями полей с длинными двоичными или длинными символьными данными с помощью [методов](getchunk-method-ado.md) [AppendChunk и](appendchunk-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d01e5-118">Если поставщик поддерживает пакетные обновления, разрешите несоответствия в значениях полей во время пакетного обновления с помощью свойств [originalValue](originalvalue-property-ado.md) и [UnderlyingValue](underlyingvalue-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d01e5-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="d01e5-119">Все свойства метаданных (**Name**, **Type**, **DefinedSize**, **Precision**и **NumericScale**) доступны до открытия **набора записей**объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="d01e5-119">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**.</span></span> <span data-ttu-id="d01e5-120">Их настройка в это время полезна для динамического создания форм.</span><span class="sxs-lookup"><span data-stu-id="d01e5-120">Setting them at that time is useful for dynamically constructing forms.</span></span>

