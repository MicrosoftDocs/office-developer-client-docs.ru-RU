---
title: Необходимые поставщики для формирования данных
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706676"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="4bc99-102">Необходимые поставщики для формирования данных</span><span class="sxs-lookup"><span data-stu-id="4bc99-102">Required providers for data shaping</span></span>

<span data-ttu-id="4bc99-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bc99-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bc99-104">Формирование данных обычно требуется двух поставщиков.</span><span class="sxs-lookup"><span data-stu-id="4bc99-104">Data shaping typically requires two providers.</span></span> <span data-ttu-id="4bc99-105">Поставщик услуг [Служба формирования данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)предоставляет функциональные возможности формирования данных и поставщика данных, таких как поставщик OLE DB для SQL Server предоставляет строк данных для заполнения формы [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4bc99-105">The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="4bc99-106">Имя поставщика услуг (MSDataShape) можно указать в качестве значения свойства [подключения](connection-object-ado.md) объект [поставщика](provider-property-ado.md) или ключевое слово строки подключения «поставщик MSDataShape; =».</span><span class="sxs-lookup"><span data-stu-id="4bc99-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="4bc99-107">Имя поставщика данных можно указать в качестве значения свойства динамического **Поставщика данных** , которое добавляется объект **подключения** коллекции [свойств](properties-collection-ado.md) службой формирования данных для OLE DB или ключевое слово строки подключения «\* *Поставщик данных = \*\*\* поставщика*«.</span><span class="sxs-lookup"><span data-stu-id="4bc99-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="4bc99-108">Поставщик данных не является обязательным, если не содержит **записей** (например, как и создано **записей** место, где столбцы создаются с помощью нового ключевого слова).</span><span class="sxs-lookup"><span data-stu-id="4bc99-108">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword).</span></span> <span data-ttu-id="4bc99-109">В этом случае указать "**Поставщик данных =** none;».</span><span class="sxs-lookup"><span data-stu-id="4bc99-109">In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="4bc99-110">Пример</span><span class="sxs-lookup"><span data-stu-id="4bc99-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

