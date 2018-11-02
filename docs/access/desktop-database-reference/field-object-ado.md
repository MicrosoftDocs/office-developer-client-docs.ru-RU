---
title: Поле объекта - ActiveX Data Objects (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d131f2634551c9c2538a87cdc8f15cfa6cc96430
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924872"
---
# <a name="field-object-ado"></a><span data-ttu-id="93d6f-102">Объект Field (ADO)</span><span class="sxs-lookup"><span data-stu-id="93d6f-102">Field object (ADO)</span></span>


<span data-ttu-id="93d6f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93d6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93d6f-104">Представляет столбец данных с типом данных.</span><span class="sxs-lookup"><span data-stu-id="93d6f-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d6f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="93d6f-105">Remarks</span></span>

<span data-ttu-id="93d6f-106">Каждый объект **поля** соответствует столбца в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="93d6f-106">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="93d6f-107">Задает или возвращает данные для текущей записи используйте свойство [Value](value-property-ado.md) объектов **полей** .</span><span class="sxs-lookup"><span data-stu-id="93d6f-107">You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record.</span></span> <span data-ttu-id="93d6f-108">В зависимости от функциональности предоставляет поставщик, некоторые коллекции методов, или свойства объекта **поля** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="93d6f-108">Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="93d6f-109">С помощью семейства сайтов, методы и свойства объекта **поля** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="93d6f-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="93d6f-110">Возвращает имя поля с помощью свойства [Name](name-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="93d6f-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="93d6f-111">Просмотр или изменение данных в поле с помощью свойства **Value** .</span><span class="sxs-lookup"><span data-stu-id="93d6f-111">View or change the data in the field with the **Value** property.</span></span> <span data-ttu-id="93d6f-112">**Значение** является свойством по умолчанию объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="93d6f-112">**Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="93d6f-113">Возвращает основные характеристики поля со свойствами [типа](type-property-ado.md), [точность](precision-property-ado.md)и [NumericScale](numericscale-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="93d6f-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="93d6f-114">Возвращает объявленные размер поля со свойством [DefinedSize](definedsize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="93d6f-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="93d6f-115">В этом поле со свойством [ActualSize](actualsize-property-ado.md) возвращает фактический размер данных.</span><span class="sxs-lookup"><span data-stu-id="93d6f-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="93d6f-116">Определите, какие функциональные возможности поддерживаются для данного поля со свойством [атрибуты](attributes-property-ado.md) и [Свойства](properties-collection-ado.md) коллекции.</span><span class="sxs-lookup"><span data-stu-id="93d6f-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="93d6f-117">Работа с элементами управления значения полей, содержащие данные длинный двоичные или много символов с помощью методов [AppendChunk](appendchunk-method-ado.md) и [GetChunk](getchunk-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="93d6f-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="93d6f-118">Если поставщик поддерживает пакетные обновления, разрешения несоответствий в значения полей во время обновление пакета с помощью свойства [OriginalValue](originalvalue-property-ado.md) и [UnderlyingValue](underlyingvalue-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="93d6f-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="93d6f-119">Все свойства метаданных (**имя**, **Тип**, **DefinedSize**, **точности**и **NumericScale**) доступны перед открытием объекта **поля** **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="93d6f-119">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**.</span></span> <span data-ttu-id="93d6f-120">Задание их в это время полезно для динамического создания форм.</span><span class="sxs-lookup"><span data-stu-id="93d6f-120">Setting them at that time is useful for dynamically constructing forms.</span></span>

