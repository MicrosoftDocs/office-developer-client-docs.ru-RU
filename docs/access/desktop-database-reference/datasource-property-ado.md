---
title: Свойство DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a6b889deb9ccf713c2313b207387be8f6b1681b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868163"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="997b8-102">Свойство DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="997b8-102">DataSource property (ADO)</span></span>


<span data-ttu-id="997b8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="997b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="997b8-104">Указывает объект, который содержит данные в виде объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="997b8-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="997b8-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="997b8-105">Remarks</span></span>

<span data-ttu-id="997b8-106">Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="997b8-106">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="997b8-107">Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект **набора записей** *.*</span><span class="sxs-lookup"><span data-stu-id="997b8-107">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="997b8-108">Свойства **DataSource** и [DataMember](datamember-property-ado.md) должен использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="997b8-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="997b8-109">Объект, на который необходимо реализовать интерфейс **IDataSource** и должна содержать интерфейс **IRowset** .</span><span class="sxs-lookup"><span data-stu-id="997b8-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="997b8-110">**Использование**</span><span class="sxs-lookup"><span data-stu-id="997b8-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
