---
title: Required Providers for Data Shaping
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41b8c7b34aa8a0da7a360dbdca5b396bb9f2b4b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482892"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="b3bef-102">Required Providers for Data Shaping</span><span class="sxs-lookup"><span data-stu-id="b3bef-102">Required Providers for Data Shaping</span></span>


<span data-ttu-id="b3bef-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3bef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3bef-104">Формирование данных обычно требуется двух поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b3bef-104">Data shaping typically requires two providers.</span></span> <span data-ttu-id="b3bef-105">Поставщик услуг [Служба формирования данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)предоставляет функциональные возможности формирования данных и поставщика данных, таких как поставщик OLE DB для SQL Server предоставляет строк данных для заполнения формы [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b3bef-105">The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="b3bef-106">Имя поставщика услуг (MSDataShape) можно указать в качестве значения свойства [подключения](connection-object-ado.md) объект [поставщика](provider-property-ado.md) или ключевое слово строки подключения «поставщик MSDataShape; =».</span><span class="sxs-lookup"><span data-stu-id="b3bef-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="b3bef-107">Имя поставщика данных можно указать в качестве значения свойства динамического **Поставщика данных** , которое добавляется объект **подключения** коллекции [свойств](properties-collection-ado.md) службой формирования данных для OLE DB или ключевое слово строки подключения «\* *Поставщик данных = \*\*\* поставщика*«.</span><span class="sxs-lookup"><span data-stu-id="b3bef-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="b3bef-108">Поставщик данных не является обязательным, если не содержит **записей** (например, как и создано **записей** место, где столбцы создаются с помощью нового ключевого слова).</span><span class="sxs-lookup"><span data-stu-id="b3bef-108">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword).</span></span> <span data-ttu-id="b3bef-109">В этом случае указать "**Поставщик данных =** none;».</span><span class="sxs-lookup"><span data-stu-id="b3bef-109">In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="b3bef-110">Пример</span><span class="sxs-lookup"><span data-stu-id="b3bef-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

