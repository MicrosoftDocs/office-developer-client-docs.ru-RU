---
title: XactAttributeEnum (Справочник по для настольных баз данных Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a44546a63583a03bd40b9e86405c3d560b3a94e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482459"
---
# <a name="xactattributeenum"></a><span data-ttu-id="0c295-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="0c295-102">XactAttributeEnum</span></span>


<span data-ttu-id="0c295-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c295-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0c295-104">Задает атрибуты транзакций объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0c295-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c295-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0c295-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0c295-106">Значение</span><span class="sxs-lookup"><span data-stu-id="0c295-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0c295-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0c295-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c295-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="0c295-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="0c295-109">262144</span><span class="sxs-lookup"><span data-stu-id="0c295-109">262144</span></span></p></td>
<td><p><span data-ttu-id="0c295-110">Выполняет сохранение прерывания — то есть, вызов <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> автоматически запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="0c295-110">Performs retaining aborts — that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="0c295-111">Не все поставщики поддерживают это.</span><span class="sxs-lookup"><span data-stu-id="0c295-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c295-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="0c295-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="0c295-113">131072</span><span class="sxs-lookup"><span data-stu-id="0c295-113">131072</span></span></p></td>
<td><p><span data-ttu-id="0c295-114">Выполняет сохранение фиксирует — то есть, вызов <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> автоматически запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="0c295-114">Performs retaining commits — that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="0c295-115">Не все поставщики поддерживают это.</span><span class="sxs-lookup"><span data-stu-id="0c295-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0c295-116">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="0c295-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="0c295-117">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0c295-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c295-118">Constant</span><span class="sxs-lookup"><span data-stu-id="0c295-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c295-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="0c295-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c295-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="0c295-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

