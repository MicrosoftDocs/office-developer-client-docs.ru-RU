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
# <a name="openschema-method-ado"></a><span data-ttu-id="748f6-102">Метод OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="748f6-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="748f6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="748f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="748f6-104">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="748f6-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="748f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="748f6-105">Syntax</span></span>

<span data-ttu-id="748f6-106">**Набор\*\*\*записей*  =  *подключение*. OpenSchema*(QueryType\*, *Criteria*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="748f6-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="748f6-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="748f6-107">Return values</span></span>

<span data-ttu-id="748f6-108">Возвращает объект [Recordset,](recordset-object-ado.md) содержащий сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="748f6-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="748f6-109">**Recordset** будет открыт в качестве статического курсора только для чтения.</span><span class="sxs-lookup"><span data-stu-id="748f6-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="748f6-110">*QueryType* определяет, какие столбцы отображаются в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="748f6-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="748f6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="748f6-111">Parameters</span></span>

|<span data-ttu-id="748f6-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="748f6-112">Parameter</span></span>|<span data-ttu-id="748f6-113">Описание</span><span class="sxs-lookup"><span data-stu-id="748f6-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="748f6-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="748f6-114">*QueryType*</span></span> |<span data-ttu-id="748f6-115">Любое [значение SchemaEnum,](schemaenum.md) которое представляет тип запроса схемы для выполнения.</span><span class="sxs-lookup"><span data-stu-id="748f6-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="748f6-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="748f6-116">*Criteria*</span></span> |<span data-ttu-id="748f6-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="748f6-117">Optional.</span></span> <span data-ttu-id="748f6-118">Массив ограничений запросов для каждого *параметра QueryType,* как указано в **SchemaEnum.**</span><span class="sxs-lookup"><span data-stu-id="748f6-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="748f6-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="748f6-119">*SchemaID*</span></span> |<span data-ttu-id="748f6-120">GUID для запроса схемы поставщика, не определенного спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="748f6-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="748f6-121">Этот параметр необходим, если *в QueryType* задан **параметр adSchemaProviderSpecific;** в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="748f6-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="748f6-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="748f6-122">Remarks</span></span>

<span data-ttu-id="748f6-123">Метод **OpenSchema** возвращает самоописательные сведения об источнике данных, например о таблицах в источнике данных, столбцах в таблицах и поддерживаемых типах данных.</span><span class="sxs-lookup"><span data-stu-id="748f6-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="748f6-124">Аргумент *QueryType* — это GUID, который указывает возвращенные столбцы (схемы).</span><span class="sxs-lookup"><span data-stu-id="748f6-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="748f6-125">Спецификация OLE DB имеет полный список схем.</span><span class="sxs-lookup"><span data-stu-id="748f6-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="748f6-126">Аргумент *Criteria* ограничивает результаты запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="748f6-126">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="748f6-127">*Критерии* заданы массив значений, которые должны возникать в соответствующем подмножеству столбцов, называемых столбцами ограничений, в итоговом **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="748f6-127">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="748f6-128">**Константа adSchemaProviderSpecific** используется для аргумента *QueryType,* если поставщик определяет собственные нестандартные запросы схемы за пределами перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="748f6-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="748f6-129">При этом используется аргумент *SchemaID* для выполнения GUID запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="748f6-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="748f6-130">Если *в QueryType* задана **adSchemaProviderSpecific,** но *схемаid* не представлена, будет допущена ошибка.</span><span class="sxs-lookup"><span data-stu-id="748f6-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="748f6-131">Поставщики не обязаны поддерживать все стандартные запросы схемы OLE DB.</span><span class="sxs-lookup"><span data-stu-id="748f6-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="748f6-132">В частности, спецификация OLE DB требует только **adSchemaTables,** **adSchemaColumns** и **adSchemaProviderTypes.**</span><span class="sxs-lookup"><span data-stu-id="748f6-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="748f6-133">Однако поставщик не обязан поддерживать указанные выше ограничения *по* критериям для этих запросов схемы.</span><span class="sxs-lookup"><span data-stu-id="748f6-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="748f6-134">**Удаленное использование службы данных** Метод **OpenSchema** не доступен для объекта клиентского [подключения.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="748f6-134">**Remote Data Service Usage** The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="748f6-135">В Visual Basic, столбцы с неподписаным набором четырехбайт (DBTYPE UI4) в наборе **Записей,** возвращаемого из метода **OpenSchema** на **объекте Подключение,** не могут сравниться с другими переменными.</span><span class="sxs-lookup"><span data-stu-id="748f6-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables.</span></span> <span data-ttu-id="748f6-136">Дополнительные сведения о типах данных OLE DB см. в главе 13 и приложении A справочника программиста *Microsoft OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="748f6-136">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


