---
title: Using ADO with ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492efdcef5f71daf50ac84eec5e61ef4ed07fd5a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481625"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="30a9b-102">Using ADO with ADO MD</span><span class="sxs-lookup"><span data-stu-id="30a9b-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="30a9b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="30a9b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="30a9b-104">ADO и ADO MD, связанных с ними, но отдельные объектных моделей.</span><span class="sxs-lookup"><span data-stu-id="30a9b-104">ADO and ADO MD are related but separate object models.</span></span> <span data-ttu-id="30a9b-105">ADO предоставляет объекты для подключения к источникам данных, выполнение команд, получение табличных данных и метаданных схемы в табличном формате и просмотра сведений об ошибках поставщика.</span><span class="sxs-lookup"><span data-stu-id="30a9b-105">ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information.</span></span> <span data-ttu-id="30a9b-106">ADO MD предоставляет объекты для извлечения многомерных данных и Просмотр многомерных схемы метаданных.</span><span class="sxs-lookup"><span data-stu-id="30a9b-106">ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="30a9b-107">При работе с MDP можно использовать ADO, ADO MD или оба вместе с приложением.</span><span class="sxs-lookup"><span data-stu-id="30a9b-107">When working with an MDP you may choose to use ADO, ADO MD, or both with your application.</span></span> <span data-ttu-id="30a9b-108">С учетом обе библиотеки в проекте, будут иметь полный доступ к функциональные возможности, предоставляемые вашей MDP.</span><span class="sxs-lookup"><span data-stu-id="30a9b-108">By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="30a9b-109">Часто бывает полезно для потребителей для получения плоская, табличного представления многомерного набора данных.</span><span class="sxs-lookup"><span data-stu-id="30a9b-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="30a9b-110">Это можно сделать с помощью объекта ADO [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="30a9b-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="30a9b-111">Укажите источник для вашей [ячеек](cellset-object-ado-md.md) в качестве ***источника*** параметра для метода [Open](open-method-ado-recordset.md) **набора записей**, а не как источник ADO MD **ячеек**.</span><span class="sxs-lookup"><span data-stu-id="30a9b-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="30a9b-112">Также можно использовать для просмотра метаданных схемы в табличном представлении, а не как иерархия объектов.</span><span class="sxs-lookup"><span data-stu-id="30a9b-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="30a9b-113">Метод ADO [OpenSchema](openschema-method-ado.md) на объект [подключения](connection-object-ado.md) позволяет пользователю открывать **набора записей** , содержащий сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="30a9b-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="30a9b-114">Параметр ***QueryType*** метода **OpenSchema** имеет несколько значений [SchemaEnum](schemaenum.md) , связанных с MDPs.</span><span class="sxs-lookup"><span data-stu-id="30a9b-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="30a9b-115">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="30a9b-115">These values are:</span></span>

  - <span data-ttu-id="30a9b-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="30a9b-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="30a9b-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="30a9b-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="30a9b-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="30a9b-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="30a9b-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="30a9b-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="30a9b-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="30a9b-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="30a9b-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="30a9b-121">**adSchemaMembers**</span></span>

<span data-ttu-id="30a9b-122">Чтобы использовать значения перечислений ADO с ADO MD свойствам и методам, проект должен содержать ссылки ADO и ADO MD библиотек.</span><span class="sxs-lookup"><span data-stu-id="30a9b-122">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries.</span></span> <span data-ttu-id="30a9b-123">Например можно использовать значения перечисления **adState** ADO со свойством ADO MD [состояние](state-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="30a9b-123">For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property.</span></span> <span data-ttu-id="30a9b-124">Дополнительные сведения о создании ссылки на библиотеки обратитесь к документации вашего средство разработки.</span><span class="sxs-lookup"><span data-stu-id="30a9b-124">For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="30a9b-125">Дополнительные сведения о ADO объекты и методы содержатся в разделе [Справочник по API ADO](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="30a9b-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

