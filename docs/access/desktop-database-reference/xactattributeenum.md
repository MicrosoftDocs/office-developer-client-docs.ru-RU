---
title: XactAttributeEnum (Справочник по для настольных баз данных Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 28b81c45921120b8a3cd8768d22559355d8ff623
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870494"
---
# <a name="xactattributeenum"></a><span data-ttu-id="1a8ba-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="1a8ba-102">XactAttributeEnum</span></span>

<span data-ttu-id="1a8ba-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a8ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a8ba-104">Задает атрибуты транзакций объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8ba-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a8ba-105">Константа</span><span class="sxs-lookup"><span data-stu-id="1a8ba-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1a8ba-106">Значение</span><span class="sxs-lookup"><span data-stu-id="1a8ba-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1a8ba-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1a8ba-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a8ba-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="1a8ba-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="1a8ba-109">262144</span><span class="sxs-lookup"><span data-stu-id="1a8ba-109">262144</span></span></p></td>
<td><p><span data-ttu-id="1a8ba-110">Выполняет сохранение прерывания; то есть вызов <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> автоматически запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="1a8ba-111">Не все поставщики поддерживают это.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a8ba-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="1a8ba-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="1a8ba-113">131072</span><span class="sxs-lookup"><span data-stu-id="1a8ba-113">131072</span></span></p></td>
<td><p><span data-ttu-id="1a8ba-114">Выполняет сохранение фиксирует; то есть вызов <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> автоматически запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="1a8ba-115">Не все поставщики поддерживают это.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1a8ba-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1a8ba-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="1a8ba-117">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1a8ba-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a8ba-118">Constant</span><span class="sxs-lookup"><span data-stu-id="1a8ba-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a8ba-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="1a8ba-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a8ba-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="1a8ba-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

