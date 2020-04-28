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
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="7595b-102">Использование ADO с ADO MD</span><span class="sxs-lookup"><span data-stu-id="7595b-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="7595b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7595b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7595b-104">ADO и ADO MD являются связанными, но отдельными объектными моделями.</span><span class="sxs-lookup"><span data-stu-id="7595b-104">ADO and ADO MD are related but separate object models.</span></span> <span data-ttu-id="7595b-105">ADO предоставляет объекты для подключения к источникам данных, выполнения команд, извлечения табличных данных и метаданных схемы в табличном формате и просмотра сведений об ошибках поставщика.</span><span class="sxs-lookup"><span data-stu-id="7595b-105">ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information.</span></span> <span data-ttu-id="7595b-106">ADO MD предоставляет объекты для получения многомерных данных и просмотра метаданных многомерных схем.</span><span class="sxs-lookup"><span data-stu-id="7595b-106">ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="7595b-107">При работе с МДП вы можете использовать ADO, ADO MD или и то, и другое вместе с приложением.</span><span class="sxs-lookup"><span data-stu-id="7595b-107">When working with an MDP you may choose to use ADO, ADO MD, or both with your application.</span></span> <span data-ttu-id="7595b-108">Ссылаясь на обе библиотеки в проекте, вы получите полный доступ к функциональным возможностям, предоставляемым вашим МДП.</span><span class="sxs-lookup"><span data-stu-id="7595b-108">By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="7595b-109">Часто пользователи могут получить плоское табличное представление многомерного набора данных.</span><span class="sxs-lookup"><span data-stu-id="7595b-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="7595b-110">Это можно сделать с помощью объекта [Recordset](recordset-object-ado.md) объекта ADO.</span><span class="sxs-lookup"><span data-stu-id="7595b-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="7595b-111">Укажите источник для набора [ячеек](cellset-object-ado-md.md) в качестве ***исходного*** параметра для метода [Open](open-method-ado-recordset.md) объекта Recordset, а не источника для **набора** **ячеек**ADO MD.</span><span class="sxs-lookup"><span data-stu-id="7595b-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="7595b-112">Также может быть полезен Просмотр метаданных схемы в табличном представлении, а не в виде иерархии объектов.</span><span class="sxs-lookup"><span data-stu-id="7595b-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="7595b-113">Метод ADO [OpenSchema](openschema-method-ado.md) для объекта [Connection](connection-object-ado.md) позволяет пользователю открыть объект **Recordset** , содержащий сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="7595b-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="7595b-114">Параметр ***куеритипе*** метода **OpenSchema** имеет несколько значений [счемаенум](schemaenum.md) , которые относятся только к мдпс.</span><span class="sxs-lookup"><span data-stu-id="7595b-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="7595b-115">Эти значения:</span><span class="sxs-lookup"><span data-stu-id="7595b-115">These values are:</span></span>

  - <span data-ttu-id="7595b-116">**адсчемакубес**</span><span class="sxs-lookup"><span data-stu-id="7595b-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="7595b-117">**адсчемадименсионс**</span><span class="sxs-lookup"><span data-stu-id="7595b-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="7595b-118">**адсчемахиерарчиес**</span><span class="sxs-lookup"><span data-stu-id="7595b-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="7595b-119">**адсчемалевелс**</span><span class="sxs-lookup"><span data-stu-id="7595b-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="7595b-120">**адсчемамеасурес**</span><span class="sxs-lookup"><span data-stu-id="7595b-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="7595b-121">**адсчемамемберс**</span><span class="sxs-lookup"><span data-stu-id="7595b-121">**adSchemaMembers**</span></span>

<span data-ttu-id="7595b-122">Чтобы использовать значения перечисления ADO с помощью свойств или методов ADO MD, проект должен ссылаться на библиотеки ADO и ADO MD.</span><span class="sxs-lookup"><span data-stu-id="7595b-122">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries.</span></span> <span data-ttu-id="7595b-123">Например, вы можете использовать значения перечисления ADO **адстате** с помощью свойства ADO MD [State](state-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="7595b-123">For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property.</span></span> <span data-ttu-id="7595b-124">Для получения дополнительных сведений об установке ссылок на библиотеки, ознакомьтесь с документацией по средству разработки.</span><span class="sxs-lookup"><span data-stu-id="7595b-124">For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="7595b-125">Дополнительные сведения об объектах и методах ADO приведены в статье [Справочник по API ADO](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7595b-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

