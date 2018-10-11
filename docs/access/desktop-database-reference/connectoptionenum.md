---
title: ConnectOptionEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2e8439099732cd3e1e9aa7531f5ae3be25d7ebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480109"
---
# <a name="connectoptionenum"></a><span data-ttu-id="45c17-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="45c17-102">ConnectOptionEnum</span></span>


<span data-ttu-id="45c17-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="45c17-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45c17-104">Указывает, должен ли возвращать метод [Open](open-method-ado-connection.md) объекта [подключения](connection-object-ado.md) после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="45c17-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45c17-105">Константа</span><span class="sxs-lookup"><span data-stu-id="45c17-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="45c17-106">Значение</span><span class="sxs-lookup"><span data-stu-id="45c17-106">Value</span></span></p></th>
<th><p><span data-ttu-id="45c17-107">Описание</span><span class="sxs-lookup"><span data-stu-id="45c17-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45c17-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="45c17-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="45c17-109">16</span><span class="sxs-lookup"><span data-stu-id="45c17-109">16</span></span></p></td>
<td><p><span data-ttu-id="45c17-110">Асинхронно открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="45c17-110">Opens the connection asynchronously.</span></span> <span data-ttu-id="45c17-111">Событие <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> могут быть использованы для определения времени есть подключение.</span><span class="sxs-lookup"><span data-stu-id="45c17-111">The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c17-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="45c17-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="45c17-113">-1</span><span class="sxs-lookup"><span data-stu-id="45c17-113">-1</span></span></p></td>
<td><p><span data-ttu-id="45c17-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45c17-114">Default.</span></span> <span data-ttu-id="45c17-115">Открывает подключение синхронно.</span><span class="sxs-lookup"><span data-stu-id="45c17-115">Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45c17-116">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="45c17-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="45c17-117">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="45c17-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45c17-118">Constant</span><span class="sxs-lookup"><span data-stu-id="45c17-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45c17-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="45c17-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c17-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="45c17-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

