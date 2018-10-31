---
title: XactAttributeEnum (Справочник по для настольных баз данных Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 2d39cc24feb377cf61e7c2d0a39e11513f4c0616
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864062"
---
# <a name="xactattributeenum"></a><span data-ttu-id="05e6b-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="05e6b-102">XactAttributeEnum</span></span>

<span data-ttu-id="05e6b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05e6b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05e6b-104">Задает атрибуты транзакций объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="05e6b-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05e6b-105">Константа</span><span class="sxs-lookup"><span data-stu-id="05e6b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="05e6b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="05e6b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="05e6b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="05e6b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05e6b-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="05e6b-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="05e6b-109">262144</span><span class="sxs-lookup"><span data-stu-id="05e6b-109">262144</span></span></p></td>
<td><p><span data-ttu-id="05e6b-110">Выполняет сохранение прерывания; то есть вызов <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> автоматически запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="05e6b-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="05e6b-111">Не все поставщики поддерживают это.</span><span class="sxs-lookup"><span data-stu-id="05e6b-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05e6b-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="05e6b-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="05e6b-113">131072</span><span class="sxs-lookup"><span data-stu-id="05e6b-113">131072</span></span></p></td>
<td><p><span data-ttu-id="05e6b-114">Выполняет сохранение фиксирует; то есть вызов <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> автоматически запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="05e6b-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="05e6b-115">Не все поставщики поддерживают это.</span><span class="sxs-lookup"><span data-stu-id="05e6b-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="05e6b-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="05e6b-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="05e6b-117">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="05e6b-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05e6b-118">Constant</span><span class="sxs-lookup"><span data-stu-id="05e6b-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05e6b-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="05e6b-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05e6b-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="05e6b-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

