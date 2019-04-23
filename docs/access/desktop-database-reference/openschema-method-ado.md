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
# <a name="openschema-method-ado"></a><span data-ttu-id="7235b-102">Метод OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="7235b-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="7235b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7235b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7235b-104">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="7235b-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="7235b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7235b-105">Syntax</span></span>

<span data-ttu-id="7235b-106">\**Set \* \* \*\* = *Подключение к*набору записей. OpenSchema (* куеритипе \*, *условия*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="7235b-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="7235b-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7235b-107">Return values</span></span>

<span data-ttu-id="7235b-108">Возвращает объект [Recordset](recordset-object-ado.md) , содержащий сведения о схеме.</span><span class="sxs-lookup"><span data-stu-id="7235b-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="7235b-109">**Набор записей** будет открыт как статический курсор, предназначенный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7235b-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="7235b-110">*Куеритипе* определяет, какие столбцы отображаются в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="7235b-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="7235b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7235b-111">Parameters</span></span>

|<span data-ttu-id="7235b-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="7235b-112">Parameter</span></span>|<span data-ttu-id="7235b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7235b-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7235b-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="7235b-114">*QueryType*</span></span> |<span data-ttu-id="7235b-115">Любое значение [счемаенум](schemaenum.md) , представляющее тип выполняемого запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="7235b-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="7235b-116">*Критерий*</span><span class="sxs-lookup"><span data-stu-id="7235b-116">*Criteria*</span></span> |<span data-ttu-id="7235b-117">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="7235b-117">Optional.</span></span> <span data-ttu-id="7235b-118">Массив ограничений запроса для каждого параметра *куеритипе* , как показано в **счемаенум**.</span><span class="sxs-lookup"><span data-stu-id="7235b-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="7235b-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="7235b-119">*SchemaID*</span></span> |<span data-ttu-id="7235b-120">GUID запроса поставщика — схемы, не определенного спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7235b-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="7235b-121">Этот параметр является обязательным, если для *куеритипе* задано значение **адсчемапровидерспеЦифик**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="7235b-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7235b-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="7235b-122">Remarks</span></span>

<span data-ttu-id="7235b-123">Метод **OpenSchema** возвращает сведения об источнике данных, например о таблицах, которые находятся в источнике данных, столбцах в таблицах и типах данных, которые поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7235b-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="7235b-124">Аргумент *куеритипе* — это идентификатор GUID, который указывает, что возвращаются столбцы (схемы).</span><span class="sxs-lookup"><span data-stu-id="7235b-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="7235b-125">Спецификация OLE DB содержит полный список схем.</span><span class="sxs-lookup"><span data-stu-id="7235b-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="7235b-126">Аргумент *условия_отбора* позволяет ограничить результаты запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="7235b-126">The *Criteria* argument limits the results of a schema query.</span></span> <span data-ttu-id="7235b-127">*Условие* определяет массив значений, которые должны присутствовать в соответствующем подмножестве столбцов, называемых *столбцами ограничений*, в результирующем **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="7235b-127">*Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="7235b-128">Константа **адсчемапровидерспеЦифик** используется для аргумента *куеритипе* , если поставщик определяет собственные нестандартные запросы схемы за пределом, указанным выше.</span><span class="sxs-lookup"><span data-stu-id="7235b-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="7235b-129">При использовании этой константы аргумент *SchemaID* необходим для передачи GUID выполняемого запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="7235b-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="7235b-130">Если для *куеритипе* задано значение **АдсчемапровидерспеЦифик** , но *SchemaID* не указано, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7235b-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="7235b-131">Поставщики не являются обязательными для поддержки всех запросов стандартных схем OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7235b-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="7235b-132">В частности, спецификации OLE DB требуются только **адсчематаблес**, **адсчемаколумнс**и **адсчемапровидертипес** .</span><span class="sxs-lookup"><span data-stu-id="7235b-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="7235b-133">Тем не менее, поставщику не требуется поддерживать ограничения *критериев* , указанные выше для этих запросов схемы.</span><span class="sxs-lookup"><span data-stu-id="7235b-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="7235b-134">**Использование удаленной службы данных** Метод **OpenSchema** недоступен для объекта [подключения](connection-object-ado.md) на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="7235b-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="7235b-135">В Visual Basic столбцы, которые содержат 4-разрядное целое число без знака (DBTYPE UI4) в **наборе записей** , возвращенном из метода **OpenSchema** в объекте **Connection** , не могут сравниваться с другими переменными.</span><span class="sxs-lookup"><span data-stu-id="7235b-135">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables.</span></span> <span data-ttu-id="7235b-136">Дополнительные сведения о типах данных OLE DB приведены в главе 13 и приложении A *Справочника программиста Microsoft OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="7235b-136">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


