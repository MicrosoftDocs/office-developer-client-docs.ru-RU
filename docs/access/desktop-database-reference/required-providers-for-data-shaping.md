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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306659"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="3504d-102">Необходимые поставщики для формирования данных</span><span class="sxs-lookup"><span data-stu-id="3504d-102">Required providers for data shaping</span></span>

<span data-ttu-id="3504d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3504d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3504d-104">Для формирования данных обычно требуются два поставщика.</span><span class="sxs-lookup"><span data-stu-id="3504d-104">Data shaping typically requires two providers.</span></span> <span data-ttu-id="3504d-105">Поставщик услуг, [Служба формирования данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), возможность формирования данных и поставщик данных, например поставщик OLE DB для SQL Server, предоставляет строки данных для заполнения объекта [Recordset](recordset-object-ado.md)в форме.</span><span class="sxs-lookup"><span data-stu-id="3504d-105">The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="3504d-106">Имя поставщика услуг (Мсдаташапе) можно указать в качестве значения свойства [поставщика](provider-property-ado.md) объекта [подключения](connection-object-ado.md) или строки подключения "Provider = мсдаташапе;".</span><span class="sxs-lookup"><span data-stu-id="3504d-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="3504d-107">Имя поставщика данных можно указать в качестве значения динамического свойства **поставщика данных** , которое добавляется в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** службой формирования данных для OLE DB или зарезервированным словом строки подключения "\**Data Provider = \* \* \* Provider*".</span><span class="sxs-lookup"><span data-stu-id="3504d-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="3504d-108">Поставщик данных не нужен, если **набор записей** не заполняется (например, как в созданном **наборе записей** , где столбцы создаются с помощью ключевого слова New).</span><span class="sxs-lookup"><span data-stu-id="3504d-108">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword).</span></span> <span data-ttu-id="3504d-109">В этом случае укажите "**Data Provider =** None;".</span><span class="sxs-lookup"><span data-stu-id="3504d-109">In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="3504d-110">Пример</span><span class="sxs-lookup"><span data-stu-id="3504d-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

