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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288079"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="70c4e-102">Объект Parameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="70c4e-102">Parameter object (ADO)</span></span>


<span data-ttu-id="70c4e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70c4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70c4e-104">Представляет параметр или аргумент, связанный с объектом [Command](command-object-ado.md) на основе параметризованного запроса или хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="70c4e-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="70c4e-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="70c4e-105">Remarks</span></span>

<span data-ttu-id="70c4e-106">Многие поставщики поддерживают параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="70c4e-106">Many providers support parameterized commands.</span></span> <span data-ttu-id="70c4e-107">Это команды, в которых нужное действие определено один раз, но переменные (или параметры) используются для изменения некоторых сведений о команде.</span><span class="sxs-lookup"><span data-stu-id="70c4e-107">These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command.</span></span> <span data-ttu-id="70c4e-108">Например, инструкция SQL SELECT может использовать параметр для определения условия соответствия предложения WHERE, а другое — для определения имени столбца для предложения SORT BY.</span><span class="sxs-lookup"><span data-stu-id="70c4e-108">For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="70c4e-109">Объект **Parameter** представляет параметры, связанные с параметризованными запросами, а также аргументы in/out и возвращаемые значения хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="70c4e-109">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures.</span></span> <span data-ttu-id="70c4e-110">В зависимости от функциональных возможностей поставщика некоторые коллекции, методы или свойства объекта **Parameter** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="70c4e-110">Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="70c4e-111">С помощью коллекций, методов и свойств объекта **Parameter** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="70c4e-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="70c4e-112">Задайте или верните имя параметра с помощью свойства [Name](name-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70c4e-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="70c4e-113">Задайте или возвратите значение параметра со свойством [value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70c4e-113">Set or return the value of a parameter with the [Value](value-property-ado.md) property.</span></span> <span data-ttu-id="70c4e-114">**Value** является свойством по умолчанию для объекта **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="70c4e-114">**Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="70c4e-115">Задайте или возвращает характеристики параметров с помощью [](attributes-property-ado.md)свойств Attributes, [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [size](size-property-ado.md)и [Type](type-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70c4e-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="70c4e-116">Передача длинных двоичных или символьных данных в параметр с помощью метода [AppendChunk](appendchunk-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70c4e-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="70c4e-117">Доступ к атрибутам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70c4e-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="70c4e-118">Если вы знаете имена и свойства параметров, связанных с хранимой процедурой или параметризованным запросом, который вы хотите вызвать, можно использовать метод [CreateParameter](createparameter-method-ado.md) для создания объектов **Parameter** с соответствующими параметрами свойства и Используйте метод [append](append-method-ado.md) , чтобы добавить их в коллекцию [Parameters](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="70c4e-118">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection.</span></span> <span data-ttu-id="70c4e-119">Это позволяет задавать и возвращать значения параметров, не выполняя вызов метода [Refresh](refresh-method-ado.md) коллекции **Parameters** для получения сведений о параметрах от поставщика, потенциально требовательных к ресурсам операций.</span><span class="sxs-lookup"><span data-stu-id="70c4e-119">This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

