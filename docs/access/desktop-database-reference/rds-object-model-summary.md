---
title: Сводка по объектной модели RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300877"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="cb91c-102">Сводка по объектной модели RDS</span><span class="sxs-lookup"><span data-stu-id="cb91c-102">RDS object model summary</span></span>


<span data-ttu-id="cb91c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb91c-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb91c-104">Object</span><span class="sxs-lookup"><span data-stu-id="cb91c-104">Object</span></span></p></th>
<th><p><span data-ttu-id="cb91c-105">Описание</span><span class="sxs-lookup"><span data-stu-id="cb91c-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb91c-106"><a href="dataspace-object-rds.md">Рабочих. DataSpace</a></span><span class="sxs-lookup"><span data-stu-id="cb91c-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="cb91c-107">Этот объект содержит метод получения прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cb91c-107">This object contains a method to obtain a server proxy.</span></span> <span data-ttu-id="cb91c-108">Прокси-сервер может быть установлен по умолчанию или настраиваемой серверной программой (бизнес-объектом).</span><span class="sxs-lookup"><span data-stu-id="cb91c-108">The proxy may be the default or a custom server program (business object).</span></span> <span data-ttu-id="cb91c-109">Серверная программа может быть вызвана в Интернете, интрасети, локальной сети или локальной библиотеке динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="cb91c-109">The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb91c-110"><a href="datafactory-object-rdsserver.md">Рдссервер. факт.</a></span><span class="sxs-lookup"><span data-stu-id="cb91c-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="cb91c-111">Этот объект представляет программу сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb91c-111">This object represents the default server program.</span></span> <span data-ttu-id="cb91c-112">Он выполняет процесс получения и обновления данных RDS, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb91c-112">It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb91c-113"><a href="datacontrol-object-rds.md">Рабочих. DataControl</a></span><span class="sxs-lookup"><span data-stu-id="cb91c-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="cb91c-114">Этот объект может автоматически вызывать <strong>RDS. Объект Space</strong> и <strong>рдссервер.</strong> объект фактов.</span><span class="sxs-lookup"><span data-stu-id="cb91c-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="cb91c-115">Используйте этот объект, чтобы вызвать процесс получения или обновления данных RDS, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb91c-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="cb91c-116">Этот объект также предоставляет средства для визуальных элементов управления для доступа к возвращенному объекту <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="cb91c-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

