---
title: Использование ADO с ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312749"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="cdfa6-102">Использование ADO с ADO MD</span><span class="sxs-lookup"><span data-stu-id="cdfa6-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="cdfa6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdfa6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cdfa6-104">ADO и ADO MD — это связанные, но отдельные объектные модели.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-104">ADO and ADO MD are related but separate object models.</span></span> <span data-ttu-id="cdfa6-105">ADO предоставляет объекты для подключения к источникам данных, выполнения команд, получения табличные данные и метаданных схемы в табличные форматы и просмотра сведений об ошибках поставщика.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-105">ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information.</span></span> <span data-ttu-id="cdfa6-106">ADO MD предоставляет объекты для инициации многомерных данных и просмотра метаданных многомерной схемы.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-106">ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="cdfa6-107">При работе с MDP вы можете использовать ADO, ADO MD или оба приложения.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-107">When working with an MDP you may choose to use ADO, ADO MD, or both with your application.</span></span> <span data-ttu-id="cdfa6-108">Ссылаясь на обе библиотеки проекта, вы сможете получить полный доступ к функциям, предоставляемым MDP.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-108">By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="cdfa6-109">Пользователям часто полезно получить плоское табличные представления многомерного наборов данных.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="cdfa6-110">Это можно сделать с помощью объекта ADO [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="cdfa6-111">Укажите источник ячейки [в](cellset-object-ado-md.md) качестве параметра ***Source*** для метода [Open](open-method-ado-recordset.md) в **наборе** записей, а не в качестве источника для ячейки ADO **MD.**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="cdfa6-112">Также может быть полезно просматривать метаданные схемы в таблическом представлении, а не в виде иерархии объектов.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="cdfa6-113">Метод ADO [OpenSchema](openschema-method-ado.md) объекта [Connection](connection-object-ado.md) позволяет пользователю открыть набор **записей,** содержащий сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="cdfa6-114">Параметр ***QueryType*** метода **OpenSchema** имеет несколько значений [SchemaEnum,](schemaenum.md) которые относятся к MDP.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="cdfa6-115">Эти значения:</span><span class="sxs-lookup"><span data-stu-id="cdfa6-115">These values are:</span></span>

  - <span data-ttu-id="cdfa6-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="cdfa6-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="cdfa6-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="cdfa6-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="cdfa6-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="cdfa6-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="cdfa6-121">**adSchemaMembers**</span></span>

<span data-ttu-id="cdfa6-122">Чтобы использовать значения из enum ADO со свойствами или методами ADO MD, проект должен ссылаться на библиотеки ADO и ADO MD.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-122">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries.</span></span> <span data-ttu-id="cdfa6-123">Например, можно использовать значения из enum ADO **adState** со свойством ADO MD [State.](state-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-123">For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property.</span></span> <span data-ttu-id="cdfa6-124">Дополнительные сведения о создании ссылок на библиотеки см. в документации средства разработки.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-124">For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="cdfa6-125">Дополнительные сведения об объектах и методах ADO см. в справочнике [по ADO API.](ado-api-reference.md)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

