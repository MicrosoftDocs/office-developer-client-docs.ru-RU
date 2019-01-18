---
title: Объект Parameter (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6f3acd4af280f30706e35eb7ecda1dee11aa7d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708517"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="eea61-102">Объект Parameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="eea61-102">Parameter object (ADO)</span></span>


<span data-ttu-id="eea61-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eea61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eea61-104">Представляет параметр или аргумент, связанной с объектом [команды](command-object-ado.md) на основе параметризованный запрос или хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="eea61-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea61-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="eea61-105">Remarks</span></span>

<span data-ttu-id="eea61-106">Многие поставщики поддерживают параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="eea61-106">Many providers support parameterized commands.</span></span> <span data-ttu-id="eea61-107">Ниже приведены команды, в которых нужное действие определяется один раз, но переменные (или параметров) используются для изменения некоторые сведения команды.</span><span class="sxs-lookup"><span data-stu-id="eea61-107">These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command.</span></span> <span data-ttu-id="eea61-108">Например источников данных можно использовать параметр для определения условий соответствия предложение WHERE, и другая, чтобы определить имя столбца для СОРТИРОВКИ BY.</span><span class="sxs-lookup"><span data-stu-id="eea61-108">For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="eea61-109">Объекты **параметров** представляют параметры, связанные с параметризованные запросы или/out аргументы и возвращаемые значения хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="eea61-109">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures.</span></span> <span data-ttu-id="eea61-110">В зависимости от функциональности поставщика некоторые семейств сайтов, методы и свойства **параметра** объект не может быть доступно.</span><span class="sxs-lookup"><span data-stu-id="eea61-110">Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="eea61-111">С помощью семейства сайтов, методы и свойства объекта **параметра** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="eea61-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="eea61-112">Установить или возвращает имя параметра с помощью свойства [Name](name-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="eea61-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="eea61-113">Установить или возвращаемое значение параметра с помощью свойства [Value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="eea61-113">Set or return the value of a parameter with the [Value](value-property-ado.md) property.</span></span> <span data-ttu-id="eea61-114">**Значение** является свойством по умолчанию объекта **параметров** .</span><span class="sxs-lookup"><span data-stu-id="eea61-114">**Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="eea61-115">Задать или вернуть характеристики параметра с [атрибутами](attributes-property-ado.md), [направление](direction-property-ado.md), [точность](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [размер](size-property-ado.md)и [Тип](type-property-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="eea61-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="eea61-116">Передайте длинный двоичный или символ данных параметр с помощью метода [AppendChunk](appendchunk-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="eea61-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="eea61-117">Атрибуты поставщика доступа с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="eea61-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="eea61-118">Если знать имена, свойства параметров, связанных с хранимую процедуру или параметризованный запрос, необходимо вызвать метод [CreateParameter](createparameter-method-ado.md) можно использовать для создания объектов **параметров** с соответствующими параметрами свойств и метод [Append](append-method-ado.md) используется для добавления их в коллекцию [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="eea61-118">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="eea61-119">Это позволяет задать и возвращаемые значения параметра без необходимости для вызова метода [обновления](refresh-method-ado.md) на коллекцию **параметров** для получения сведений о параметрах от поставщика, потенциально ресурсоемких операции.</span><span class="sxs-lookup"><span data-stu-id="eea61-119">This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

