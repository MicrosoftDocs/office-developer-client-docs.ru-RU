---
title: Коннектоптионенум (Справочник по базам данных Access на компьютере)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295683"
---
# <a name="connectoptionenum"></a><span data-ttu-id="586b2-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="586b2-102">ConnectOptionEnum</span></span>

<span data-ttu-id="586b2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="586b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="586b2-104">Указывает, должен ли метод [Open](open-method-ado-connection.md) объекта [Connection](connection-object-ado.md) возвращаться (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="586b2-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="586b2-105">Константа</span><span class="sxs-lookup"><span data-stu-id="586b2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="586b2-106">Значение</span><span class="sxs-lookup"><span data-stu-id="586b2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="586b2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="586b2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="586b2-108"><strong>Адасинкконнект</strong></span><span class="sxs-lookup"><span data-stu-id="586b2-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="586b2-109">столбцов</span><span class="sxs-lookup"><span data-stu-id="586b2-109">16</span></span></p></td>
<td><p><span data-ttu-id="586b2-110">Асинхронно открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="586b2-110">Opens the connection asynchronously.</span></span> <span data-ttu-id="586b2-111">Событие <a href="connectcomplete-and-disconnect-events-ado.md">события connectcomplete</a> можно использовать для определения доступности подключения.</span><span class="sxs-lookup"><span data-stu-id="586b2-111">The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="586b2-112"><strong>АдконнектунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="586b2-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="586b2-113">–1</span><span class="sxs-lookup"><span data-stu-id="586b2-113">-1</span></span></p></td>
<td><p><span data-ttu-id="586b2-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="586b2-114">Default.</span></span> <span data-ttu-id="586b2-115">Синхронно открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="586b2-115">Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="586b2-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="586b2-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="586b2-117">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="586b2-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="586b2-118">Константа</span><span class="sxs-lookup"><span data-stu-id="586b2-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="586b2-119">Адоенумс. Коннектоптион. АСИНККОННЕКТ</span><span class="sxs-lookup"><span data-stu-id="586b2-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="586b2-120">Адоенумс. Коннектоптион. КОННЕКТУНСПЕЦИФИЕД</span><span class="sxs-lookup"><span data-stu-id="586b2-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

