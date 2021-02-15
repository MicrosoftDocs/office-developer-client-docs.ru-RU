---
title: Метод OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288338"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="7dde7-102">Метод OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="7dde7-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="7dde7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dde7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dde7-104">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="7dde7-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="7dde7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dde7-105">Syntax</span></span>

<span data-ttu-id="7dde7-106">**Set\*\*\*\*recordset*  =  *connection .* OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="7dde7-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="7dde7-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7dde7-107">Return values</span></span>

<span data-ttu-id="7dde7-108">Возвращает объект [Recordset,](recordset-object-ado.md) содержащий сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="7dde7-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="7dde7-109">Набор **записей** будет открыт в качестве статического курсора только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7dde7-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="7dde7-110">*QueryType* определяет, какие столбцы отображаются в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="7dde7-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dde7-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dde7-111">Parameters</span></span>

|<span data-ttu-id="7dde7-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="7dde7-112">Parameter</span></span>|<span data-ttu-id="7dde7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7dde7-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7dde7-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="7dde7-114">*QueryType*</span></span> |<span data-ttu-id="7dde7-115">Любое [значение SchemaEnum,](schemaenum.md) которое представляет тип запроса схемы для запуска.</span><span class="sxs-lookup"><span data-stu-id="7dde7-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="7dde7-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="7dde7-116">*Criteria*</span></span> |<span data-ttu-id="7dde7-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="7dde7-117">Optional.</span></span> <span data-ttu-id="7dde7-118">Массив ограничений запроса для каждого *параметра QueryType,* как указано **в SchemaEnum.**</span><span class="sxs-lookup"><span data-stu-id="7dde7-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="7dde7-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="7dde7-119">*SchemaID*</span></span> |<span data-ttu-id="7dde7-120">GUID для запроса схемы поставщика, не определенного спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7dde7-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="7dde7-121">Этот параметр обязален, если *параметр QueryType* имеет тип **adSchemaProviderSpecific;** в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="7dde7-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7dde7-122">Заметки</span><span class="sxs-lookup"><span data-stu-id="7dde7-122">Remarks</span></span>

<span data-ttu-id="7dde7-123">Метод **OpenSchema** возвращает самоописательные сведения об источнике данных, такие как таблицы в источнике данных, столбцы в таблицах и поддерживаемые типы данных.</span><span class="sxs-lookup"><span data-stu-id="7dde7-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="7dde7-124">Аргумент *QueryType* — это GUID, который указывает возвращенные столбцы (схемы).</span><span class="sxs-lookup"><span data-stu-id="7dde7-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="7dde7-125">Спецификация OLE DB имеет полный список схем.</span><span class="sxs-lookup"><span data-stu-id="7dde7-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="7dde7-126">Аргумент *Criteria* ограничивает результаты запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="7dde7-126">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="7dde7-127">*Условия* заданы массив значений, которые должны быть в соответствующем подмножество столбцов, называемых столбцы ограничения *,* в итоговом **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="7dde7-127">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="7dde7-128">**Константа adSchemaProviderSpecific** используется для аргумента *QueryType,* если поставщик определяет собственные нестандартные запросы схемы за пределами перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="7dde7-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="7dde7-129">Если используется эта константа, для выполнения запроса схемы требуется аргумент *SchemaID.*</span><span class="sxs-lookup"><span data-stu-id="7dde7-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="7dde7-130">Если *для QueryType* заданы данные **adSchemaProviderSpecific,** но *SchemaID* не предоставлен, будет выдана ошибка.</span><span class="sxs-lookup"><span data-stu-id="7dde7-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="7dde7-131">Поставщики не обязаны поддерживать все запросы стандартной схемы OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7dde7-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="7dde7-132">В частности, спецификация OLE DB требует только **adSchemaTables,** **adSchemaColumns** и **adSchemaProviderTypes.**</span><span class="sxs-lookup"><span data-stu-id="7dde7-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="7dde7-133">Однако поставщик не обязан поддерживать указанные выше ограничения критериев для этих запросов схемы. </span><span class="sxs-lookup"><span data-stu-id="7dde7-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="7dde7-134">**Использование удаленной службы данных** Метод **OpenSchema** не доступен для объекта подключения на [стороне](connection-object-ado.md) клиента.</span><span class="sxs-lookup"><span data-stu-id="7dde7-134">**Remote Data Service Usage** The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="7dde7-135">В Visual Basic столбцы с четырехбайтным неподписаным значением (DBTYPE UI4) в наборе записей, возвращаемом методом **OpenSchema** в объекте  **Connection,** нельзя сравнить с другими переменными.</span><span class="sxs-lookup"><span data-stu-id="7dde7-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables.</span></span> <span data-ttu-id="7dde7-136">Дополнительные сведения о типах данных OLE DB см. в главе 13 и приложении A справочника по программисту *Microsoft OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="7dde7-136">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


