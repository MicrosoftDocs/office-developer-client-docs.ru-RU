---
title: Объект Catalog (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713089"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="6e18e-102">Объект Catalog (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6e18e-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="6e18e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e18e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e18e-104">Содержит многомерные сведения о схеме (то есть, кубов и базовым измерений, иерархии, уровни и элементы) определенного поставщика многомерных данных (MDP).</span><span class="sxs-lookup"><span data-stu-id="6e18e-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e18e-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e18e-105">Remarks</span></span>

<span data-ttu-id="6e18e-106">Со свойствами объекта **каталога** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="6e18e-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

- <span data-ttu-id="6e18e-107">Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-ado-md.md) стандартный объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="6e18e-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

- <span data-ttu-id="6e18e-108">Определение **каталога** с помощью свойства [Name](name-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="6e18e-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="6e18e-109">Выполните итерацию по кубов в каталог с помощью коллекции [CubeDefs](cubedefs-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="6e18e-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

