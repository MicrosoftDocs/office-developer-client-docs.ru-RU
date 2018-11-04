---
title: Метод OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a204f6e86a1c50be49400430f53dd99468668a9e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950001"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="a1441-102">Метод OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="a1441-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="a1441-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1441-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1441-104">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="a1441-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="a1441-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1441-105">Syntax</span></span>

<span data-ttu-id="a1441-106">**Задайте \*\*\* записей* = *подключения*. OpenSchema (* QueryType \*, *критерии* *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="a1441-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="a1441-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a1441-107">Return values</span></span>

<span data-ttu-id="a1441-108">Возвращает объект [набора записей](recordset-object-ado.md) , который содержит сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="a1441-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="a1441-109">Как только для чтения, статический курсор будет открыт **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a1441-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="a1441-110">*QueryType* определяет, какие столбцы должны отображаться в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="a1441-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1441-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1441-111">Parameters</span></span>

|<span data-ttu-id="a1441-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="a1441-112">Parameter</span></span>|<span data-ttu-id="a1441-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a1441-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a1441-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="a1441-114">*QueryType*</span></span> |<span data-ttu-id="a1441-115">Любое значение [SchemaEnum](schemaenum.md) , представляющий тип запроса схемы для запуска.</span><span class="sxs-lookup"><span data-stu-id="a1441-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="a1441-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="a1441-116">*Criteria*</span></span> |<span data-ttu-id="a1441-117">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="a1441-117">Optional.</span></span> <span data-ttu-id="a1441-118">Массив ограничения запроса для каждого варианта *QueryType* , как указано в **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="a1441-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="a1441-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="a1441-119">*SchemaID*</span></span> |<span data-ttu-id="a1441-120">Идентификатор GUID для запроса поставщика схемы не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a1441-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="a1441-121">Этот параметр является обязательным, если *QueryType* задано значение **adSchemaProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="a1441-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a1441-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1441-122">Remarks</span></span>

<span data-ttu-id="a1441-123">Метод **OpenSchema** возвращает столбцы в таблицах и типы данных, поддерживаемые достаточные описательные сведения об источнике данных, например таблицах, представляют в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="a1441-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="a1441-124">Аргумент *QueryType* — это идентификатор GUID, указывающий, возвращаемые столбцы (схемы).</span><span class="sxs-lookup"><span data-stu-id="a1441-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="a1441-125">Спецификация OLE DB имеет полный список схем.</span><span class="sxs-lookup"><span data-stu-id="a1441-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="a1441-126">Аргумент *Критерий* ограничивает результаты запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="a1441-126">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="a1441-127">*Критерии* указывает массив значений, которые должны выполняться в соответствующем подмножество столбцов, называемых *столбцов ограничения*в результирующий **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="a1441-127">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="a1441-128">Константы **adSchemaProviderSpecific** используется для аргумента *QueryType* , если поставщик определяет собственный нестандартного схемы запросы за пределами перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="a1441-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="a1441-129">При использовании этой константы в аргументе *SchemaID* требуется для передачи GUID схемы запроса на выполнение.</span><span class="sxs-lookup"><span data-stu-id="a1441-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="a1441-130">Если *QueryType* задано значение **adSchemaProviderSpecific** , но *SchemaID* не указан, будет выдана ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1441-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="a1441-131">Поставщики не требуются для поддержки всех запросов стандартной схемы OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a1441-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="a1441-132">В частности, только **adSchemaTables**, **adSchemaColumns**и **adSchemaProviderTypes** необходимы спецификации OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a1441-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="a1441-133">Тем не менее поставщик не требуется для поддержки ограничения *критерии* , перечисленные выше для таких запросов схемы.</span><span class="sxs-lookup"><span data-stu-id="a1441-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="a1441-134">**Службы удаленных данных об использовании** Метод **OpenSchema** не доступен на объект [подключения](connection-object-ado.md) со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="a1441-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a1441-135">В Visual Basic столбцов, которые имеют четыре байтовое целое число без знака (DBTYPE UI4) в <STRONG>набор записей</STRONG> , возвращенный методом <STRONG>OpenSchema</STRONG> на объект <STRONG>подключения</STRONG> нельзя сравнивать с другими переменных.</span><span class="sxs-lookup"><span data-stu-id="a1441-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables.</span></span> <span data-ttu-id="a1441-136">Дополнительные сведения о типах данных OLE DB видеть главе 13 и приложение A <EM>Microsoft OLE DB Справочник программиста</EM>.</span><span class="sxs-lookup"><span data-stu-id="a1441-136">For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


