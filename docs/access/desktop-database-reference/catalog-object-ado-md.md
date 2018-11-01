---
title: Объект каталога (ADO MD)
TOCTitle: Catalog Object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9d55969a0f90595f25deac0b01a70bff6fc7c3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879601"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="bba20-102">Объект каталога (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="bba20-102">Catalog Object (ADO MD)</span></span>


<span data-ttu-id="bba20-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bba20-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bba20-104">Содержит многомерные сведения о схеме (то есть, кубов и базовым измерений, иерархии, уровни и элементы) определенного поставщика многомерных данных (MDP).</span><span class="sxs-lookup"><span data-stu-id="bba20-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="bba20-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="bba20-105">Remarks</span></span>

<span data-ttu-id="bba20-106">Со свойствами объекта **каталога** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="bba20-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

  - <span data-ttu-id="bba20-107">Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-ado-md.md) стандартный объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="bba20-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

  - <span data-ttu-id="bba20-108">Определение **каталога** с помощью свойства [Name](name-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="bba20-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="bba20-109">Выполните итерацию по кубов в каталог с помощью коллекции [CubeDefs](cubedefs-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="bba20-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

