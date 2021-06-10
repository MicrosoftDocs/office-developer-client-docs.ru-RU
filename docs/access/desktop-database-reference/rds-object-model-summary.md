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
# <a name="rds-object-model-summary"></a><span data-ttu-id="f4dcf-102">Сводка по объектной модели RDS</span><span class="sxs-lookup"><span data-stu-id="f4dcf-102">RDS object model summary</span></span>


<span data-ttu-id="f4dcf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4dcf-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4dcf-104">Объект</span><span class="sxs-lookup"><span data-stu-id="f4dcf-104">Object</span></span></p></th>
<th><p><span data-ttu-id="f4dcf-105">Описание</span><span class="sxs-lookup"><span data-stu-id="f4dcf-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4dcf-106"><a href="dataspace-object-rds.md">RDS. DataSpace</a></span><span class="sxs-lookup"><span data-stu-id="f4dcf-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="f4dcf-107">Этот объект содержит метод получения прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-107">This object contains a method to obtain a server proxy.</span></span> <span data-ttu-id="f4dcf-108">Прокси-сервер может быть по умолчанию или настраиваемой серверной программой (бизнес-объектом).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-108">The proxy may be the default or a custom server program (business object).</span></span> <span data-ttu-id="f4dcf-109">Серверная программа может вызываться в Интернете, интрасети, локальной сети или локальной библиотеке динамических ссылок.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-109">The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4dcf-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="f4dcf-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="f4dcf-111">Этот объект представляет серверную программу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-111">This object represents the default server program.</span></span> <span data-ttu-id="f4dcf-112">Он выполняет ирисовку данных RDS по умолчанию и поведение обновления.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-112">It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4dcf-113"><a href="datacontrol-object-rds.md">RDS. DataControl</a></span><span class="sxs-lookup"><span data-stu-id="f4dcf-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="f4dcf-114">Этот объект может автоматически вызывать <strong>RDS. Объекты DataSpace</strong> и <strong>RDSServer.DataFactory.</strong></span><span class="sxs-lookup"><span data-stu-id="f4dcf-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="f4dcf-115">Используйте этот объект, чтобы вызвать по умолчанию сбор данных RDS или обновление поведения.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="f4dcf-116">Этот объект также предоставляет средства визуального управления для доступа к возвращенным <strong>объекту Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="f4dcf-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

