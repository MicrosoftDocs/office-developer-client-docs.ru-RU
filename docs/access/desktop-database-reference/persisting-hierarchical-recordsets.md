---
title: Сохранение иерархических наборов записей
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287582"
---
# <a name="persisting-hierarchical-recordsets"></a><span data-ttu-id="f9059-102">Сохранение иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="f9059-102">Persisting hierarchical Recordsets</span></span>

<span data-ttu-id="f9059-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9059-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9059-104">Иерархический набор записей можно сохранить в файле в формате ADTG или XML, вызывая метод [Save.](save-method-ado.md) </span><span class="sxs-lookup"><span data-stu-id="f9059-104">You can save a hierarchical **Recordset** to a file in either ADTG or XML format by calling the [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="f9059-105">Однако при сохранении иерархического наборов записей в формате XML применяются два  ограничения: невозможно сохранить в XML, если иерархический набор записей содержит ожидающих обновлений и нельзя сохранить параметризованный иерархический набор **записей.** </span><span class="sxs-lookup"><span data-stu-id="f9059-105">However, two limitations apply when saving hierarchical **Recordset** s in XML format: You cannot save in XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="f9059-106">Дополнительные сведения о поставщике формирования данных см. в службах формирования данных Майкрософт для [OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) и Data Shaping Service for OLE DB(OLE DB).</span><span class="sxs-lookup"><span data-stu-id="f9059-106">For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).</span></span>

