---
title: Объект Каталог (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296593"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="a17af-102">Объект Каталог (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a17af-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="a17af-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a17af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a17af-104">Содержит многомерные сведения о схеме (т. е. кубов и их ниже, иерархий, уровней и членов), специфичные для многомерного поставщика данных (MDP).</span><span class="sxs-lookup"><span data-stu-id="a17af-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="a17af-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="a17af-105">Remarks</span></span>

<span data-ttu-id="a17af-106">С коллекциями и свойствами объекта **Каталог** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="a17af-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

- <span data-ttu-id="a17af-107">Откройте каталог, установив свойство [ActiveConnection](activeconnection-property-ado-md.md) на стандартный объект ADO [Connection](connection-object-ado.md) или допустимую строку подключения.</span><span class="sxs-lookup"><span data-stu-id="a17af-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

- <span data-ttu-id="a17af-108">Определите **каталог** с [свойством Name.](name-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="a17af-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="a17af-109">Итерировать кубов в каталоге с помощью [коллекции CubeDefs.](cubedefs-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="a17af-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

