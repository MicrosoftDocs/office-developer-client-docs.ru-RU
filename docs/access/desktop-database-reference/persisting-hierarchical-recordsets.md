---
title: Сохранение иерархических наборов записей
TOCTitle: Persisting Hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c990ef345ed8e10223757ded958b1b8a0f60eb26
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877382"
---
# <a name="persisting-hierarchical-recordsets"></a><span data-ttu-id="d258a-102">Сохранение иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="d258a-102">Persisting Hierarchical Recordsets</span></span>


<span data-ttu-id="d258a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d258a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d258a-104">Иерархическая **записей** можно сохранить файл в формате ADTG или XML, вызвав метод [Save](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d258a-104">You can save a hierarchical **Recordset** to a file in either ADTG or XML format by calling the [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="d258a-105">Тем не менее, два ограничения при сохранении иерархических s **записей**в формате XML: не могут сохранять в формате XML, если иерархических **записей** содержит ожидающие обновления и не могут сохранять параметризованный иерархических **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d258a-105">However, two limitations apply when saving hierarchical **Recordset**s in XML format: You cannot save in XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="d258a-106">Дополнительные сведения о поставщике данных формирования см [Служба формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) и служба формирования данных OLE DB(OLE DB).</span><span class="sxs-lookup"><span data-stu-id="d258a-106">For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).</span></span>

