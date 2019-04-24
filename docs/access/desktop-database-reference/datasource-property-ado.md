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
# <a name="datasource-property-ado"></a><span data-ttu-id="e5d5d-102">Свойство DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="e5d5d-102">DataSource property (ADO)</span></span>


<span data-ttu-id="e5d5d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5d5d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5d5d-104">Указывает объект, содержащий данные, которые должны быть представлены в виде объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d5d-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5d5d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="e5d5d-105">Remarks</span></span>

<span data-ttu-id="e5d5d-106">Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="e5d5d-106">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="e5d5d-107">Среда данных поддерживает коллекции данных (источников данных), содержащие именованные объекты (*элементы данных*), которые будут представлены как объект **Recordset** *.*</span><span class="sxs-lookup"><span data-stu-id="e5d5d-107">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="e5d5d-108">Свойства [DataMember](datamember-property-ado.md) и **DataSource** должны использоваться совместно.</span><span class="sxs-lookup"><span data-stu-id="e5d5d-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="e5d5d-109">Объект, на который указывает ссылка, должен реализовать интерфейс **IDataSource** и должен содержать интерфейс **IRowset** .</span><span class="sxs-lookup"><span data-stu-id="e5d5d-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="e5d5d-110">**Usage**</span><span class="sxs-lookup"><span data-stu-id="e5d5d-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
