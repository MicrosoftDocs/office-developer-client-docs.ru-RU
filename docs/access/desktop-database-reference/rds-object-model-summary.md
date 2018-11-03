---
title: Сводка по объектной модели RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13ca1f9bfd9dc507ce921de58bed17e933fbeaeb
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947933"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="bf634-102">Сводка по объектной модели RDS</span><span class="sxs-lookup"><span data-stu-id="bf634-102">RDS object model summary</span></span>


<span data-ttu-id="bf634-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf634-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf634-104">Объект</span><span class="sxs-lookup"><span data-stu-id="bf634-104">Object</span></span></p></th>
<th><p><span data-ttu-id="bf634-105">Описание</span><span class="sxs-lookup"><span data-stu-id="bf634-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf634-106"><a href="dataspace-object-rds.md">RDS. Пространства данных</a></span><span class="sxs-lookup"><span data-stu-id="bf634-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="bf634-107">Этот объект содержит метод для получения прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="bf634-107">This object contains a method to obtain a server proxy.</span></span> <span data-ttu-id="bf634-108">Прокси-сервер может быть по умолчанию или настраиваемый серверный программы (бизнес-объект).</span><span class="sxs-lookup"><span data-stu-id="bf634-108">The proxy may be the default or a custom server program (business object).</span></span> <span data-ttu-id="bf634-109">Программы сервера, могут быть вызваны Интернета, интрасети, локальной сети или быть локальной библиотеки динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="bf634-109">The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf634-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="bf634-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="bf634-111">Этот объект представляет программы сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bf634-111">This object represents the default server program.</span></span> <span data-ttu-id="bf634-112">Оно выполняет поведение по умолчанию служб удаленных рабочих СТОЛОВ данных извлечения и обновления.</span><span class="sxs-lookup"><span data-stu-id="bf634-112">It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf634-113"><a href="datacontrol-object-rds.md">RDS. DataControl</a></span><span class="sxs-lookup"><span data-stu-id="bf634-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="bf634-114">Этот объект можно вызвать автоматически <strong>RDS. Пространства данных</strong> и <strong>RDSServer.DataFactory</strong> объектов.</span><span class="sxs-lookup"><span data-stu-id="bf634-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="bf634-115">Этот объект можно используйте для вызова по умолчанию поведение извлечения или обновления данных служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="bf634-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="bf634-116">Этот объект также предоставляет средства для визуальные элементы управления для доступа к возвращенного объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="bf634-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

