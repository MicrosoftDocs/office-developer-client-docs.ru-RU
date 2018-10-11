---
title: OpenSchema Method (ADO)
TOCTitle: OpenSchema Method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba0cdb22ee9234e935635038b86ac792dd5753cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483029"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="4369a-102">OpenSchema Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="4369a-102">OpenSchema Method (ADO)</span></span>


<span data-ttu-id="4369a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4369a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="4369a-104">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="4369a-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="4369a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4369a-105">Syntax</span></span>

<span data-ttu-id="4369a-106">**Задайте \*\*\* записей* = *подключения*. OpenSchema (* QueryType \*, *критерии* *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="4369a-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="4369a-107">Return Values</span><span class="sxs-lookup"><span data-stu-id="4369a-107">Return Values</span></span>

<span data-ttu-id="4369a-108">Возвращает объект [набора записей](recordset-object-ado.md) , который содержит сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="4369a-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="4369a-109">Как только для чтения, статический курсор будет открыт **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4369a-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="4369a-110">*QueryType* определяет, какие столбцы должны отображаться в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="4369a-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="4369a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4369a-111">Parameters</span></span>

  - <span data-ttu-id="4369a-112">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="4369a-112">*QueryType*</span></span>

  - <span data-ttu-id="4369a-113">Любое значение [SchemaEnum](schemaenum.md) , представляющий тип запроса схемы для запуска.</span><span class="sxs-lookup"><span data-stu-id="4369a-113">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>

  - <span data-ttu-id="4369a-114">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="4369a-114">*Criteria*</span></span>

  - <span data-ttu-id="4369a-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="4369a-115">Optional.</span></span> <span data-ttu-id="4369a-116">Массив ограничения запроса для каждого варианта *QueryType* , как указано в **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="4369a-116">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>

  - <span data-ttu-id="4369a-117">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="4369a-117">*SchemaID*</span></span>

  - <span data-ttu-id="4369a-118">Идентификатор GUID для запроса поставщика схемы не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4369a-118">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="4369a-119">Этот параметр является обязательным, если *QueryType* задано значение **adSchemaProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="4369a-119">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4369a-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="4369a-120">Remarks</span></span>

<span data-ttu-id="4369a-121">Метод **OpenSchema** возвращает столбцы в таблицах и типы данных, поддерживаемые достаточные описательные сведения об источнике данных, например таблицах, представляют в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="4369a-121">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="4369a-122">Аргумент *QueryType* — это идентификатор GUID, указывающий, возвращаемые столбцы (схемы).</span><span class="sxs-lookup"><span data-stu-id="4369a-122">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="4369a-123">Спецификация OLE DB имеет полный список схем.</span><span class="sxs-lookup"><span data-stu-id="4369a-123">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="4369a-124">Аргумент *Критерий* ограничивает результаты запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="4369a-124">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="4369a-125">*Критерии* указывает массив значений, которые должны выполняться в соответствующем подмножество столбцов, называемых *столбцов ограничения*в результирующий **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="4369a-125">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="4369a-126">Константы **adSchemaProviderSpecific** используется для аргумента *QueryType* , если поставщик определяет собственный нестандартного схемы запросы за пределами перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="4369a-126">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="4369a-127">При использовании этой константы в аргументе *SchemaID* требуется для передачи GUID схемы запроса на выполнение.</span><span class="sxs-lookup"><span data-stu-id="4369a-127">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="4369a-128">Если *QueryType* задано значение **adSchemaProviderSpecific** , но *SchemaID* не указан, будет выдана ошибка.</span><span class="sxs-lookup"><span data-stu-id="4369a-128">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="4369a-129">Поставщики не требуются для поддержки всех запросов стандартной схемы OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4369a-129">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="4369a-130">В частности, только **adSchemaTables**, **adSchemaColumns**и **adSchemaProviderTypes** необходимы спецификации OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4369a-130">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="4369a-131">Тем не менее поставщик не требуется для поддержки ограничения *критерии* , перечисленные выше для таких запросов схемы.</span><span class="sxs-lookup"><span data-stu-id="4369a-131">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="4369a-132">**Службы удаленных данных об использовании** Метод **OpenSchema** не доступен на объект [подключения](connection-object-ado.md) со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="4369a-132">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4369a-133">В Visual Basic столбцов, которые имеют четыре байтовое целое число без знака (DBTYPE UI4) в <STRONG>набор записей</STRONG> , возвращенный методом <STRONG>OpenSchema</STRONG> на объект <STRONG>подключения</STRONG> нельзя сравнивать с другими переменных.</span><span class="sxs-lookup"><span data-stu-id="4369a-133">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables.</span></span> <span data-ttu-id="4369a-134">Дополнительные сведения о типах данных OLE DB видеть главе 13 и приложение A <EM>Microsoft OLE DB Справочник программиста</EM>.</span><span class="sxs-lookup"><span data-stu-id="4369a-134">For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


