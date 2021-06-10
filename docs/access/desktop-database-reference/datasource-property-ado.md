---
title: Свойство DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294472"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="80e0c-102">Свойство DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="80e0c-102">DataSource property (ADO)</span></span>


<span data-ttu-id="80e0c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80e0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80e0c-104">Указывает объект, содержащий данные, которые будут представлены в качестве [объекта Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="80e0c-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e0c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="80e0c-105">Remarks</span></span>

<span data-ttu-id="80e0c-106">Это свойство используется для создания элементов управления, связанных с данными, с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="80e0c-106">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="80e0c-107">Среда данных поддерживает коллекции данных (источников данных), содержащих именуемые объекты *(участники* данных), которые будут представлены в качестве объекта **Recordset.** </span><span class="sxs-lookup"><span data-stu-id="80e0c-107">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="80e0c-108">Свойства [DataMember](datamember-property-ado.md) и **DataSource** должны использоваться совместно.</span><span class="sxs-lookup"><span data-stu-id="80e0c-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="80e0c-109">Объект, на который ссылается, должен реализовать **интерфейс IDataSource** и содержать **интерфейс IRowset.**</span><span class="sxs-lookup"><span data-stu-id="80e0c-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="80e0c-110">**Использование**</span><span class="sxs-lookup"><span data-stu-id="80e0c-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
