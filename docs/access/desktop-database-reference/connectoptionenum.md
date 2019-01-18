---
title: ConnectOptionEnum (Справочник по для настольных баз данных Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699963"
---
# <a name="connectoptionenum"></a><span data-ttu-id="9663c-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="9663c-102">ConnectOptionEnum</span></span>

<span data-ttu-id="9663c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9663c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9663c-104">Указывает, должен ли возвращать метод [Open](open-method-ado-connection.md) объекта [подключения](connection-object-ado.md) после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="9663c-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9663c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="9663c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9663c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9663c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9663c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9663c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9663c-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="9663c-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="9663c-109">16</span><span class="sxs-lookup"><span data-stu-id="9663c-109">16</span></span></p></td>
<td><p><span data-ttu-id="9663c-110">Асинхронно открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="9663c-110">Opens the connection asynchronously.</span></span> <span data-ttu-id="9663c-111">Событие <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> могут быть использованы для определения времени есть подключение.</span><span class="sxs-lookup"><span data-stu-id="9663c-111">The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9663c-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="9663c-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="9663c-113">–1</span><span class="sxs-lookup"><span data-stu-id="9663c-113">-1</span></span></p></td>
<td><p><span data-ttu-id="9663c-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9663c-114">Default.</span></span> <span data-ttu-id="9663c-115">Открывает подключение синхронно.</span><span class="sxs-lookup"><span data-stu-id="9663c-115">Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9663c-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9663c-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="9663c-117">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9663c-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9663c-118">Константа</span><span class="sxs-lookup"><span data-stu-id="9663c-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9663c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="9663c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9663c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="9663c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

